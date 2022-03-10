<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `caddy`

-	[`caddy:2`](#caddy2)
-	[`caddy:2-alpine`](#caddy2-alpine)
-	[`caddy:2-builder`](#caddy2-builder)
-	[`caddy:2-builder-alpine`](#caddy2-builder-alpine)
-	[`caddy:2-builder-windowsservercore-1809`](#caddy2-builder-windowsservercore-1809)
-	[`caddy:2-windowsservercore`](#caddy2-windowsservercore)
-	[`caddy:2-windowsservercore-1809`](#caddy2-windowsservercore-1809)
-	[`caddy:2.4.6`](#caddy246)
-	[`caddy:2.4.6-alpine`](#caddy246-alpine)
-	[`caddy:2.4.6-builder`](#caddy246-builder)
-	[`caddy:2.4.6-builder-alpine`](#caddy246-builder-alpine)
-	[`caddy:2.4.6-builder-windowsservercore-1809`](#caddy246-builder-windowsservercore-1809)
-	[`caddy:2.4.6-windowsservercore`](#caddy246-windowsservercore)
-	[`caddy:2.4.6-windowsservercore-1809`](#caddy246-windowsservercore-1809)
-	[`caddy:2.5.0-beta.1`](#caddy250-beta1)
-	[`caddy:2.5.0-beta.1-alpine`](#caddy250-beta1-alpine)
-	[`caddy:2.5.0-beta.1-builder`](#caddy250-beta1-builder)
-	[`caddy:2.5.0-beta.1-builder-alpine`](#caddy250-beta1-builder-alpine)
-	[`caddy:2.5.0-beta.1-builder-windowsservercore-1809`](#caddy250-beta1-builder-windowsservercore-1809)
-	[`caddy:2.5.0-beta.1-builder-windowsservercore-ltsc2022`](#caddy250-beta1-builder-windowsservercore-ltsc2022)
-	[`caddy:2.5.0-beta.1-windowsservercore`](#caddy250-beta1-windowsservercore)
-	[`caddy:2.5.0-beta.1-windowsservercore-1809`](#caddy250-beta1-windowsservercore-1809)
-	[`caddy:2.5.0-beta.1-windowsservercore-ltsc2022`](#caddy250-beta1-windowsservercore-ltsc2022)
-	[`caddy:alpine`](#caddyalpine)
-	[`caddy:builder`](#caddybuilder)
-	[`caddy:builder-alpine`](#caddybuilder-alpine)
-	[`caddy:builder-windowsservercore-1809`](#caddybuilder-windowsservercore-1809)
-	[`caddy:latest`](#caddylatest)
-	[`caddy:windowsservercore`](#caddywindowsservercore)
-	[`caddy:windowsservercore-1809`](#caddywindowsservercore-1809)

## `caddy:2`

```console
$ docker pull caddy@sha256:184338dab192cd97f7c61b66c021c5709b2418e4826182f553ae09099f5082a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2686; amd64
	-	windows version 10.0.14393.5006; amd64

### `caddy:2` - linux; amd64

```console
$ docker pull caddy@sha256:7da0f90273e1961d9c38d26809f84d4ef3cdc9b4fc330a9cab22015d7c9e8228
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14856906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439af64db48912c0a446444aae0e357183264ff08e1154fa105d5ee082e0bf13`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:54:17 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 12 Nov 2021 21:54:18 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Fri, 12 Nov 2021 21:54:19 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 12 Nov 2021 21:54:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 12 Nov 2021 21:54:23 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:54:23 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 12 Nov 2021 21:54:23 GMT
ENV XDG_DATA_HOME=/data
# Fri, 12 Nov 2021 21:54:23 GMT
VOLUME [/config]
# Fri, 12 Nov 2021 21:54:24 GMT
VOLUME [/data]
# Fri, 12 Nov 2021 21:54:24 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Fri, 12 Nov 2021 21:54:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 12 Nov 2021 21:54:24 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 12 Nov 2021 21:54:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 12 Nov 2021 21:54:25 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 12 Nov 2021 21:54:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 12 Nov 2021 21:54:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 12 Nov 2021 21:54:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 12 Nov 2021 21:54:25 GMT
EXPOSE 80
# Fri, 12 Nov 2021 21:54:26 GMT
EXPOSE 443
# Fri, 12 Nov 2021 21:54:26 GMT
EXPOSE 2019
# Fri, 12 Nov 2021 21:54:26 GMT
WORKDIR /srv
# Fri, 12 Nov 2021 21:54:26 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ccae726125d77e2fd3891c69c8f663d5fe63d8ad4a67deb284e2c589334497`  
		Last Modified: Fri, 12 Nov 2021 21:54:48 GMT  
		Size: 301.5 KB (301497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de6a61c89acc2147364721befe6e6bf957963713d1ddc4bc6c4a35f7b4b4e0a`  
		Last Modified: Fri, 12 Nov 2021 21:54:48 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ed957bdc008c4cc475fcaeb053cdb7fbcc83f49184fca8013d87cf9d395518`  
		Last Modified: Fri, 12 Nov 2021 21:54:50 GMT  
		Size: 11.7 MB (11726445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae44c2d42ddcf77445d391f491713e6384b933553eb234ceb0d9b3e66c5b33f`  
		Last Modified: Fri, 12 Nov 2021 21:54:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:caa4910dc3572e3ba3888fda3f7f5ed69c8c575461d29e528a6b453c0ba90522
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14068833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358685e491b9f796f29e9b70a0a43f619fa034e7bcd995cf738d811cf8e4ebe9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:07:54 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 12 Nov 2021 17:07:57 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Fri, 12 Nov 2021 17:07:57 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 12 Nov 2021 17:08:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 12 Nov 2021 17:08:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 17:08:04 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 12 Nov 2021 17:08:05 GMT
ENV XDG_DATA_HOME=/data
# Fri, 12 Nov 2021 17:08:05 GMT
VOLUME [/config]
# Fri, 12 Nov 2021 17:08:06 GMT
VOLUME [/data]
# Fri, 12 Nov 2021 17:08:06 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Fri, 12 Nov 2021 17:08:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 12 Nov 2021 17:08:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 12 Nov 2021 17:08:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 12 Nov 2021 17:08:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 12 Nov 2021 17:08:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 12 Nov 2021 17:08:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 12 Nov 2021 17:08:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 12 Nov 2021 17:08:10 GMT
EXPOSE 80
# Fri, 12 Nov 2021 17:08:10 GMT
EXPOSE 443
# Fri, 12 Nov 2021 17:08:11 GMT
EXPOSE 2019
# Fri, 12 Nov 2021 17:08:11 GMT
WORKDIR /srv
# Fri, 12 Nov 2021 17:08:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d466a8f7766a93ea57a37532240c4a8c0e21cdb1f731360b1d21022b74f840f1`  
		Last Modified: Fri, 12 Nov 2021 17:09:28 GMT  
		Size: 301.7 KB (301671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082eb2081a4e07ea8cd0a36b4c3e7fee48ac23e2f6e8b7f95659e9a7465012fb`  
		Last Modified: Fri, 12 Nov 2021 17:09:27 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3790fd0e6afb978b6d8b451eaea5ab3e59b48913548a910853b31bc234bfed1c`  
		Last Modified: Fri, 12 Nov 2021 17:09:35 GMT  
		Size: 11.1 MB (11125784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe30a92d02271e636688f49fc9e1b382f2836b2c4578c29a993dc5111eb0b927`  
		Last Modified: Fri, 12 Nov 2021 17:09:27 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:5211ef3cdd2abf233de36a5e914b3ea2a649f0ec2164e5c63dd96c0cf870004e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13852151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389ecbea3a7d6a7b6a98da18b9b565046f2629b6c4af69a7d20d5cabcd1562d5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 11:43:41 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 13 Nov 2021 11:43:44 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 13 Nov 2021 11:43:44 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 13 Nov 2021 11:43:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 13 Nov 2021 11:43:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 11:43:51 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 13 Nov 2021 11:43:51 GMT
ENV XDG_DATA_HOME=/data
# Sat, 13 Nov 2021 11:43:52 GMT
VOLUME [/config]
# Sat, 13 Nov 2021 11:43:52 GMT
VOLUME [/data]
# Sat, 13 Nov 2021 11:43:53 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 13 Nov 2021 11:43:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 13 Nov 2021 11:43:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 13 Nov 2021 11:43:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 13 Nov 2021 11:43:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 13 Nov 2021 11:43:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 13 Nov 2021 11:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 13 Nov 2021 11:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 13 Nov 2021 11:43:57 GMT
EXPOSE 80
# Sat, 13 Nov 2021 11:43:57 GMT
EXPOSE 443
# Sat, 13 Nov 2021 11:43:58 GMT
EXPOSE 2019
# Sat, 13 Nov 2021 11:43:58 GMT
WORKDIR /srv
# Sat, 13 Nov 2021 11:43:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5663fa07ca1dcac265e40e084d2e40771a9084e9b30309c275bf810e87a3b53a`  
		Last Modified: Sat, 13 Nov 2021 11:45:26 GMT  
		Size: 300.8 KB (300831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf8bc3ddae458c10861b1ef0a30a6c8e97ea3a7135680ced673a2532a4c043e`  
		Last Modified: Sat, 13 Nov 2021 11:45:25 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afb06d1223418bbdf22f64f5a3a57962ad6570d931f931ab8df015439fb0c7a`  
		Last Modified: Sat, 13 Nov 2021 11:45:33 GMT  
		Size: 11.1 MB (11106718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a00e0b33a8465343d1f7f61ffec47a7c7aaad34402170530d9e9ebbb4ac5665`  
		Last Modified: Sat, 13 Nov 2021 11:45:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:8c2b7f01f3d14048e888946dd85b972ac76d22490107d999f6df18399ab76f25
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13763680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e48a5247e105a4ecd7f6a7b3f6bfe21fe6633146de42ad9bd4197b3222b920d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 11:18:37 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 13 Nov 2021 11:18:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 13 Nov 2021 11:18:40 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 13 Nov 2021 11:18:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 13 Nov 2021 11:18:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 11:18:44 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 13 Nov 2021 11:18:45 GMT
ENV XDG_DATA_HOME=/data
# Sat, 13 Nov 2021 11:18:46 GMT
VOLUME [/config]
# Sat, 13 Nov 2021 11:18:47 GMT
VOLUME [/data]
# Sat, 13 Nov 2021 11:18:48 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 13 Nov 2021 11:18:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 13 Nov 2021 11:18:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 13 Nov 2021 11:18:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 13 Nov 2021 11:18:52 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 13 Nov 2021 11:18:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 13 Nov 2021 11:18:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 13 Nov 2021 11:18:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 13 Nov 2021 11:18:56 GMT
EXPOSE 80
# Sat, 13 Nov 2021 11:18:57 GMT
EXPOSE 443
# Sat, 13 Nov 2021 11:18:58 GMT
EXPOSE 2019
# Sat, 13 Nov 2021 11:18:59 GMT
WORKDIR /srv
# Sat, 13 Nov 2021 11:19:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e205c63fa7e1c7a1060c29f8600bf90d965a1d26a1ae313210de738d08649d0`  
		Last Modified: Sat, 13 Nov 2021 11:19:44 GMT  
		Size: 301.4 KB (301450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674f75736ea40598c6df0d5460f914bf940c50952e8f106cdb674f9d98e8c5bb`  
		Last Modified: Sat, 13 Nov 2021 11:19:44 GMT  
		Size: 5.8 KB (5750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e004593c132f71a51cbd6967cf29bac3fc607c79fa8d967253c2f79461442641`  
		Last Modified: Sat, 13 Nov 2021 11:19:45 GMT  
		Size: 10.7 MB (10738627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51900aef2f22db52e1c14e6dd7f645241d02abef12b8ef2b377595f11b77055b`  
		Last Modified: Sat, 13 Nov 2021 11:19:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; ppc64le

```console
$ docker pull caddy@sha256:b47a92735f1a101ce7087f2fc6f8b33614226b32c4507de0de8a4b6b34d84504
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13429323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bbba192f1381ae73d2265be6a6b84d7539131fcc66399931bd66ff97ff83f5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 21:18:00 GMT
ADD file:4d45063079cb28a34f1e382fddb22f156ac99d5449aa05ed37cb653c1f7b80f2 in / 
# Fri, 12 Nov 2021 21:18:01 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 15:14:03 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 13 Nov 2021 15:14:24 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 13 Nov 2021 15:14:33 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 13 Nov 2021 15:14:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 13 Nov 2021 15:14:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 15:14:54 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 13 Nov 2021 15:14:58 GMT
ENV XDG_DATA_HOME=/data
# Sat, 13 Nov 2021 15:15:03 GMT
VOLUME [/config]
# Sat, 13 Nov 2021 15:15:05 GMT
VOLUME [/data]
# Sat, 13 Nov 2021 15:15:09 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 13 Nov 2021 15:15:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 13 Nov 2021 15:15:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 13 Nov 2021 15:15:19 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 13 Nov 2021 15:15:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 13 Nov 2021 15:15:26 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 13 Nov 2021 15:15:30 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 13 Nov 2021 15:15:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 13 Nov 2021 15:15:35 GMT
EXPOSE 80
# Sat, 13 Nov 2021 15:15:37 GMT
EXPOSE 443
# Sat, 13 Nov 2021 15:15:40 GMT
EXPOSE 2019
# Sat, 13 Nov 2021 15:15:42 GMT
WORKDIR /srv
# Sat, 13 Nov 2021 15:15:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:72940440c1ab65eca4d38846164719ffde4b147543cc658d041407a925b13368`  
		Last Modified: Fri, 12 Nov 2021 21:19:32 GMT  
		Size: 2.8 MB (2817467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aca7d05e49e358a035d0dd6f471c0d19419c9cc97646fff4e82578d2c488237`  
		Last Modified: Sat, 13 Nov 2021 15:16:26 GMT  
		Size: 303.6 KB (303607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc78b04675eccc541ab8678fe7221460039d23c40f04c02d41e150f256c4368`  
		Last Modified: Sat, 13 Nov 2021 15:16:25 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f289e05d8a93edbe6667d481e3a61908205bf58c77aa2ddf18b09f740724a8cd`  
		Last Modified: Sat, 13 Nov 2021 15:16:28 GMT  
		Size: 10.3 MB (10302268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd68deeff259e1bcfa76db665a6a52747267383f87bb506b77fbb409529ae3c8`  
		Last Modified: Sat, 13 Nov 2021 15:16:25 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; s390x

```console
$ docker pull caddy@sha256:5ac69c24193df6b0d9b0c13816ce3861b720b62721901b0eb7446bd41ae86a3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14240890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753d56e00623363d01fede6cee26039f1b7efc2f64fccec498168291c9b9ea6b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 04:01:37 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 13 Nov 2021 04:01:38 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 13 Nov 2021 04:01:38 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 13 Nov 2021 04:01:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 13 Nov 2021 04:01:42 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 04:01:42 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 13 Nov 2021 04:01:42 GMT
ENV XDG_DATA_HOME=/data
# Sat, 13 Nov 2021 04:01:42 GMT
VOLUME [/config]
# Sat, 13 Nov 2021 04:01:42 GMT
VOLUME [/data]
# Sat, 13 Nov 2021 04:01:42 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 13 Nov 2021 04:01:44 GMT
EXPOSE 80
# Sat, 13 Nov 2021 04:01:44 GMT
EXPOSE 443
# Sat, 13 Nov 2021 04:01:44 GMT
EXPOSE 2019
# Sat, 13 Nov 2021 04:01:44 GMT
WORKDIR /srv
# Sat, 13 Nov 2021 04:01:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0267ca443b43155e255c1a3bb35bab8ac5b561ddc2d0e768868f13274c7ab32d`  
		Last Modified: Sat, 13 Nov 2021 04:02:28 GMT  
		Size: 301.9 KB (301922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9c9c616a8868c7845a4a9d56e876f1bf42c37dac31b80761370b9af366e4c1`  
		Last Modified: Sat, 13 Nov 2021 04:02:28 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0dfff2c7fb2b8bde893d14f4d66fe6d6e8bee6115e0f4f691f7698d17a51f7`  
		Last Modified: Sat, 13 Nov 2021 04:02:29 GMT  
		Size: 11.3 MB (11323710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc9ba4f178258a6de34c95f9f50fb0fd89e093f552c493cd511cfb5fc39a433`  
		Last Modified: Sat, 13 Nov 2021 04:02:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:f2de2d90885f8cb6d12c79d914e354b41f6bfebc22ba3390096ae69fac380cf5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2728251838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8705f493a3ce58fda2b9ada4d3d27639c9f13835f1fb8d85ecdf795e69dae46a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:20:26 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:20:27 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:21:52 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:21:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:21:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:21:55 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:21:56 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:21:57 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:21:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:21:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:22:00 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:22:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:22:02 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:22:05 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:22:06 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:22:07 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:23:12 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:23:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99d892d6329e540cd98b358cc2f8085a7e6579538de9b4afa3ce0d11a03116`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 365.4 KB (365439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fb2be6c676c8f3e743cd43ec6b238646cf9f8b89a6fb1bde29f9bb52a7296c`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9b968486191ed8bb4a6c85eb678e32bbb062d8998e636e7706431be6e25f51`  
		Last Modified: Wed, 09 Mar 2022 18:29:07 GMT  
		Size: 12.1 MB (12115400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63f0ecb87a49981ac55c8495d8beed3b58d3b15e31ff4ba1140b0176e551265`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5249439459c9b885575d1a0c5c0df8c3e99649414b3c09ef4054e22fab54b584`  
		Last Modified: Wed, 09 Mar 2022 18:29:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69ab39aec279710b6bf7b4581cafe49878e70beff74d4a5e342eea02e60ce60`  
		Last Modified: Wed, 09 Mar 2022 18:29:02 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb81ca26c7a917813faca1d4cb92e1f41e642701d1199c9811ae8f9294e5b6f`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f5adb02b69cdd17e3acff1b0ea61317020c331399b0cb57fa34da5c09956e3`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e95a1158bc8e4066b6eb4211e7e898c86431c53c76c4752dfd7ce0a15cfc48`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579759f42b06baed2eb773c9cf8d6709e48e71afc07751fb3d45f7e4df9d819a`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e477dc674aa75d9872e80416c27f642531913f63b1598f0920a821c8b6cb535c`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03c9bb84aaf51c973e2ae3990a6b45ac835195b5eaae35799354b2aee8dfc2e`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23add58da280a0f09c755eaccccd5ecc95dc65993558d933f499b4c3378c9f70`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e3da14e3fcc65b938eef87893e57b0daa81c012c8789265cd784fb2f3cfcf7`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34cb18e7475b74cb46643f516f65cbd77fa161c461d753b4e62e076f7b221e5`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbd804e2eb98213ed819900a23753f3f2d662eb72c30a86dbbb51bcecc3cebc`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49b05954d4ea193b3f85228739d529bbc2a811204d8b6e22440c97977addbdf`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a3a3abbfe3563eaed35b97ad1ed309a3f4e744f968d0b6f6deaf68211f2fc8`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53542589ba9c33b651da4be35de7384a168d4936d08bb046a632a4d644b46c9e`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 293.3 KB (293252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149ac7945e26171c6dfe9e316c21027eb072f4fd72819f8b80a32eada8275ae2`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.14393.5006; amd64

```console
$ docker pull caddy@sha256:7f8374457a1c63677174631c3a8ea273702e069b924b615f44292250b7e2d8c1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6289879706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba40202b27c7479ec2d1d1618860745715dbfcabf489c651e5f04e826c286f72`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sat, 05 Mar 2022 03:39:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Mar 2022 18:23:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:24:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:24:49 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:26:02 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:26:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:26:04 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:26:05 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:26:06 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:26:07 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:26:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:26:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:26:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:26:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:26:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:26:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:26:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:26:14 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:26:15 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:26:16 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:26:54 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:26:55 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0fe465a8df276d07bd592c9424c00276a476fb7f74be6f867256b07fba31212d`  
		Size: 2.2 GB (2207094901 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c66997424475af0399fffec7897bad20e40b8309c56761077b30f5d9495f4db3`  
		Last Modified: Wed, 09 Mar 2022 18:29:32 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31f3b05b8f63dd42b4881a4c3d384691cc281678a86e0836d0c32819a344b5d`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 345.5 KB (345470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9855b50f056bb89da3373dfb2c128c8cf2515840c723a9027f0c01bb0eb91d`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b715cda286f032f4b113aefacf8b42874e8bed4dbe0080772b9d6cc1e91fc4`  
		Last Modified: Wed, 09 Mar 2022 18:29:43 GMT  
		Size: 12.1 MB (12134708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e40c1797eb55c98999e616bff73129a77843c7cf7667787950662180cbd90b`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d12359d4309d649fc7f0131974324ede0eb7aa11d1cd6f5d47000f9e14363b`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1783134869b6be42026ea8457c2f07dcacd3e029eaa283e48e798ce94929111`  
		Last Modified: Wed, 09 Mar 2022 18:29:28 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7104f8aa42fca009aaea2d885dfc7a0ea9acd8b7670cd9a90929f355d29cb5bf`  
		Last Modified: Wed, 09 Mar 2022 18:29:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ee03e2f86a2587a31a03418808435e9804fd324f95c981776b71ac5541f122`  
		Last Modified: Wed, 09 Mar 2022 18:29:28 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617c8eb23f7d35a0012ac7a3ce817bb49edda99eb16da9e4a9e6897617ded26d`  
		Last Modified: Wed, 09 Mar 2022 18:29:27 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85694b0569ffdf58e2f716205756d0a9eab45456d0ef23c2bbc8cb5816b99c1a`  
		Last Modified: Wed, 09 Mar 2022 18:29:27 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe2abbbf56f3d370ddba372e974d4765e074ee94fa8b1e4037b1cbf9d4a1e04`  
		Last Modified: Wed, 09 Mar 2022 18:29:26 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d4deaae43ac0785c4ccfb22ba187f33035f3041d44d770e8864cab157c1fe8`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7c04adc036f7a25c1c5a61895ba945aac263098d741203cb43e6b3b32174ef`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582d555a149be3d9ce42e33942b905cc2c8b9ebdc0dd1de51709fd7276c1e3ae`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b57929590127351973d44b26f950891ee7b918dc352a68098193a5d4fce629`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71478b5420cbbbea1bb0a6e617445f903203fac8965dfc6e2c41932cbb7f2acb`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b709c8c0d2fb364fd66993072fd79d4d28cda233a5d991b74680a1f80b1563`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c82093ad8180c0667cf71cdf92b8ead740771d5f2f5efda695fc67b815056d9`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34076b974bce5f92149f3e2eb58dc898a74d7ca4c563c20c4308f51a3f25212`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 293.4 KB (293417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e27086943ac64711a35c0e493db7b82a4faa0d65d5e80a91104238aba4845e2`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:1659785ea84188c3ad22a6c1f96f463d167a4b81318d71f4bb6e3d37dbe73908
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
$ docker pull caddy@sha256:7da0f90273e1961d9c38d26809f84d4ef3cdc9b4fc330a9cab22015d7c9e8228
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14856906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439af64db48912c0a446444aae0e357183264ff08e1154fa105d5ee082e0bf13`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:54:17 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 12 Nov 2021 21:54:18 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Fri, 12 Nov 2021 21:54:19 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 12 Nov 2021 21:54:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 12 Nov 2021 21:54:23 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:54:23 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 12 Nov 2021 21:54:23 GMT
ENV XDG_DATA_HOME=/data
# Fri, 12 Nov 2021 21:54:23 GMT
VOLUME [/config]
# Fri, 12 Nov 2021 21:54:24 GMT
VOLUME [/data]
# Fri, 12 Nov 2021 21:54:24 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Fri, 12 Nov 2021 21:54:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 12 Nov 2021 21:54:24 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 12 Nov 2021 21:54:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 12 Nov 2021 21:54:25 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 12 Nov 2021 21:54:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 12 Nov 2021 21:54:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 12 Nov 2021 21:54:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 12 Nov 2021 21:54:25 GMT
EXPOSE 80
# Fri, 12 Nov 2021 21:54:26 GMT
EXPOSE 443
# Fri, 12 Nov 2021 21:54:26 GMT
EXPOSE 2019
# Fri, 12 Nov 2021 21:54:26 GMT
WORKDIR /srv
# Fri, 12 Nov 2021 21:54:26 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ccae726125d77e2fd3891c69c8f663d5fe63d8ad4a67deb284e2c589334497`  
		Last Modified: Fri, 12 Nov 2021 21:54:48 GMT  
		Size: 301.5 KB (301497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de6a61c89acc2147364721befe6e6bf957963713d1ddc4bc6c4a35f7b4b4e0a`  
		Last Modified: Fri, 12 Nov 2021 21:54:48 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ed957bdc008c4cc475fcaeb053cdb7fbcc83f49184fca8013d87cf9d395518`  
		Last Modified: Fri, 12 Nov 2021 21:54:50 GMT  
		Size: 11.7 MB (11726445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae44c2d42ddcf77445d391f491713e6384b933553eb234ceb0d9b3e66c5b33f`  
		Last Modified: Fri, 12 Nov 2021 21:54:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:caa4910dc3572e3ba3888fda3f7f5ed69c8c575461d29e528a6b453c0ba90522
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14068833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358685e491b9f796f29e9b70a0a43f619fa034e7bcd995cf738d811cf8e4ebe9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:07:54 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 12 Nov 2021 17:07:57 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Fri, 12 Nov 2021 17:07:57 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 12 Nov 2021 17:08:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 12 Nov 2021 17:08:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 17:08:04 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 12 Nov 2021 17:08:05 GMT
ENV XDG_DATA_HOME=/data
# Fri, 12 Nov 2021 17:08:05 GMT
VOLUME [/config]
# Fri, 12 Nov 2021 17:08:06 GMT
VOLUME [/data]
# Fri, 12 Nov 2021 17:08:06 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Fri, 12 Nov 2021 17:08:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 12 Nov 2021 17:08:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 12 Nov 2021 17:08:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 12 Nov 2021 17:08:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 12 Nov 2021 17:08:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 12 Nov 2021 17:08:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 12 Nov 2021 17:08:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 12 Nov 2021 17:08:10 GMT
EXPOSE 80
# Fri, 12 Nov 2021 17:08:10 GMT
EXPOSE 443
# Fri, 12 Nov 2021 17:08:11 GMT
EXPOSE 2019
# Fri, 12 Nov 2021 17:08:11 GMT
WORKDIR /srv
# Fri, 12 Nov 2021 17:08:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d466a8f7766a93ea57a37532240c4a8c0e21cdb1f731360b1d21022b74f840f1`  
		Last Modified: Fri, 12 Nov 2021 17:09:28 GMT  
		Size: 301.7 KB (301671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082eb2081a4e07ea8cd0a36b4c3e7fee48ac23e2f6e8b7f95659e9a7465012fb`  
		Last Modified: Fri, 12 Nov 2021 17:09:27 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3790fd0e6afb978b6d8b451eaea5ab3e59b48913548a910853b31bc234bfed1c`  
		Last Modified: Fri, 12 Nov 2021 17:09:35 GMT  
		Size: 11.1 MB (11125784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe30a92d02271e636688f49fc9e1b382f2836b2c4578c29a993dc5111eb0b927`  
		Last Modified: Fri, 12 Nov 2021 17:09:27 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:5211ef3cdd2abf233de36a5e914b3ea2a649f0ec2164e5c63dd96c0cf870004e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13852151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389ecbea3a7d6a7b6a98da18b9b565046f2629b6c4af69a7d20d5cabcd1562d5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 11:43:41 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 13 Nov 2021 11:43:44 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 13 Nov 2021 11:43:44 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 13 Nov 2021 11:43:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 13 Nov 2021 11:43:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 11:43:51 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 13 Nov 2021 11:43:51 GMT
ENV XDG_DATA_HOME=/data
# Sat, 13 Nov 2021 11:43:52 GMT
VOLUME [/config]
# Sat, 13 Nov 2021 11:43:52 GMT
VOLUME [/data]
# Sat, 13 Nov 2021 11:43:53 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 13 Nov 2021 11:43:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 13 Nov 2021 11:43:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 13 Nov 2021 11:43:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 13 Nov 2021 11:43:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 13 Nov 2021 11:43:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 13 Nov 2021 11:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 13 Nov 2021 11:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 13 Nov 2021 11:43:57 GMT
EXPOSE 80
# Sat, 13 Nov 2021 11:43:57 GMT
EXPOSE 443
# Sat, 13 Nov 2021 11:43:58 GMT
EXPOSE 2019
# Sat, 13 Nov 2021 11:43:58 GMT
WORKDIR /srv
# Sat, 13 Nov 2021 11:43:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5663fa07ca1dcac265e40e084d2e40771a9084e9b30309c275bf810e87a3b53a`  
		Last Modified: Sat, 13 Nov 2021 11:45:26 GMT  
		Size: 300.8 KB (300831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf8bc3ddae458c10861b1ef0a30a6c8e97ea3a7135680ced673a2532a4c043e`  
		Last Modified: Sat, 13 Nov 2021 11:45:25 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afb06d1223418bbdf22f64f5a3a57962ad6570d931f931ab8df015439fb0c7a`  
		Last Modified: Sat, 13 Nov 2021 11:45:33 GMT  
		Size: 11.1 MB (11106718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a00e0b33a8465343d1f7f61ffec47a7c7aaad34402170530d9e9ebbb4ac5665`  
		Last Modified: Sat, 13 Nov 2021 11:45:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:8c2b7f01f3d14048e888946dd85b972ac76d22490107d999f6df18399ab76f25
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13763680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e48a5247e105a4ecd7f6a7b3f6bfe21fe6633146de42ad9bd4197b3222b920d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 11:18:37 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 13 Nov 2021 11:18:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 13 Nov 2021 11:18:40 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 13 Nov 2021 11:18:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 13 Nov 2021 11:18:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 11:18:44 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 13 Nov 2021 11:18:45 GMT
ENV XDG_DATA_HOME=/data
# Sat, 13 Nov 2021 11:18:46 GMT
VOLUME [/config]
# Sat, 13 Nov 2021 11:18:47 GMT
VOLUME [/data]
# Sat, 13 Nov 2021 11:18:48 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 13 Nov 2021 11:18:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 13 Nov 2021 11:18:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 13 Nov 2021 11:18:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 13 Nov 2021 11:18:52 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 13 Nov 2021 11:18:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 13 Nov 2021 11:18:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 13 Nov 2021 11:18:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 13 Nov 2021 11:18:56 GMT
EXPOSE 80
# Sat, 13 Nov 2021 11:18:57 GMT
EXPOSE 443
# Sat, 13 Nov 2021 11:18:58 GMT
EXPOSE 2019
# Sat, 13 Nov 2021 11:18:59 GMT
WORKDIR /srv
# Sat, 13 Nov 2021 11:19:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e205c63fa7e1c7a1060c29f8600bf90d965a1d26a1ae313210de738d08649d0`  
		Last Modified: Sat, 13 Nov 2021 11:19:44 GMT  
		Size: 301.4 KB (301450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674f75736ea40598c6df0d5460f914bf940c50952e8f106cdb674f9d98e8c5bb`  
		Last Modified: Sat, 13 Nov 2021 11:19:44 GMT  
		Size: 5.8 KB (5750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e004593c132f71a51cbd6967cf29bac3fc607c79fa8d967253c2f79461442641`  
		Last Modified: Sat, 13 Nov 2021 11:19:45 GMT  
		Size: 10.7 MB (10738627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51900aef2f22db52e1c14e6dd7f645241d02abef12b8ef2b377595f11b77055b`  
		Last Modified: Sat, 13 Nov 2021 11:19:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:b47a92735f1a101ce7087f2fc6f8b33614226b32c4507de0de8a4b6b34d84504
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13429323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bbba192f1381ae73d2265be6a6b84d7539131fcc66399931bd66ff97ff83f5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 21:18:00 GMT
ADD file:4d45063079cb28a34f1e382fddb22f156ac99d5449aa05ed37cb653c1f7b80f2 in / 
# Fri, 12 Nov 2021 21:18:01 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 15:14:03 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 13 Nov 2021 15:14:24 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 13 Nov 2021 15:14:33 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 13 Nov 2021 15:14:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 13 Nov 2021 15:14:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 15:14:54 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 13 Nov 2021 15:14:58 GMT
ENV XDG_DATA_HOME=/data
# Sat, 13 Nov 2021 15:15:03 GMT
VOLUME [/config]
# Sat, 13 Nov 2021 15:15:05 GMT
VOLUME [/data]
# Sat, 13 Nov 2021 15:15:09 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 13 Nov 2021 15:15:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 13 Nov 2021 15:15:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 13 Nov 2021 15:15:19 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 13 Nov 2021 15:15:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 13 Nov 2021 15:15:26 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 13 Nov 2021 15:15:30 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 13 Nov 2021 15:15:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 13 Nov 2021 15:15:35 GMT
EXPOSE 80
# Sat, 13 Nov 2021 15:15:37 GMT
EXPOSE 443
# Sat, 13 Nov 2021 15:15:40 GMT
EXPOSE 2019
# Sat, 13 Nov 2021 15:15:42 GMT
WORKDIR /srv
# Sat, 13 Nov 2021 15:15:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:72940440c1ab65eca4d38846164719ffde4b147543cc658d041407a925b13368`  
		Last Modified: Fri, 12 Nov 2021 21:19:32 GMT  
		Size: 2.8 MB (2817467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aca7d05e49e358a035d0dd6f471c0d19419c9cc97646fff4e82578d2c488237`  
		Last Modified: Sat, 13 Nov 2021 15:16:26 GMT  
		Size: 303.6 KB (303607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc78b04675eccc541ab8678fe7221460039d23c40f04c02d41e150f256c4368`  
		Last Modified: Sat, 13 Nov 2021 15:16:25 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f289e05d8a93edbe6667d481e3a61908205bf58c77aa2ddf18b09f740724a8cd`  
		Last Modified: Sat, 13 Nov 2021 15:16:28 GMT  
		Size: 10.3 MB (10302268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd68deeff259e1bcfa76db665a6a52747267383f87bb506b77fbb409529ae3c8`  
		Last Modified: Sat, 13 Nov 2021 15:16:25 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:5ac69c24193df6b0d9b0c13816ce3861b720b62721901b0eb7446bd41ae86a3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14240890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753d56e00623363d01fede6cee26039f1b7efc2f64fccec498168291c9b9ea6b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 04:01:37 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 13 Nov 2021 04:01:38 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 13 Nov 2021 04:01:38 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 13 Nov 2021 04:01:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 13 Nov 2021 04:01:42 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 04:01:42 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 13 Nov 2021 04:01:42 GMT
ENV XDG_DATA_HOME=/data
# Sat, 13 Nov 2021 04:01:42 GMT
VOLUME [/config]
# Sat, 13 Nov 2021 04:01:42 GMT
VOLUME [/data]
# Sat, 13 Nov 2021 04:01:42 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 13 Nov 2021 04:01:44 GMT
EXPOSE 80
# Sat, 13 Nov 2021 04:01:44 GMT
EXPOSE 443
# Sat, 13 Nov 2021 04:01:44 GMT
EXPOSE 2019
# Sat, 13 Nov 2021 04:01:44 GMT
WORKDIR /srv
# Sat, 13 Nov 2021 04:01:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0267ca443b43155e255c1a3bb35bab8ac5b561ddc2d0e768868f13274c7ab32d`  
		Last Modified: Sat, 13 Nov 2021 04:02:28 GMT  
		Size: 301.9 KB (301922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9c9c616a8868c7845a4a9d56e876f1bf42c37dac31b80761370b9af366e4c1`  
		Last Modified: Sat, 13 Nov 2021 04:02:28 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0dfff2c7fb2b8bde893d14f4d66fe6d6e8bee6115e0f4f691f7698d17a51f7`  
		Last Modified: Sat, 13 Nov 2021 04:02:29 GMT  
		Size: 11.3 MB (11323710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc9ba4f178258a6de34c95f9f50fb0fd89e093f552c493cd511cfb5fc39a433`  
		Last Modified: Sat, 13 Nov 2021 04:02:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:aeb897e44b8614b95c66f1f00fb2a09b58a8fcb9c4b060e361a5493e626b6b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2686; amd64
	-	windows version 10.0.14393.4886; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:9c6a77c878ea39bd367c8c7e73f1a75a6ce97101bef0f3de7e288934b4de519e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121354364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c3a82ad51f9b44b272a32de82576c64480a940db9877dd465101c921e11593`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:21:45 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 04:21:46 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 04:21:47 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 01:05:33 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 01:08:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 01:08:13 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 01:08:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 01:08:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 01:08:14 GMT
WORKDIR /go
# Fri, 04 Mar 2022 04:22:25 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 04 Mar 2022 04:22:25 GMT
ENV XCADDY_VERSION=v0.2.0
# Fri, 04 Mar 2022 04:22:26 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 04 Mar 2022 04:22:26 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 04 Mar 2022 04:22:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 04 Mar 2022 04:22:27 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 04 Mar 2022 04:22:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666ba61612fd7c93393f9a5bc1751d8a9929e32d51501dba691da9e8232bc87b`  
		Last Modified: Tue, 30 Nov 2021 04:36:04 GMT  
		Size: 282.2 KB (282159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed8ca4862056a130f714accb3538decfa0663fec84e635d8b5a0a3305353dee`  
		Last Modified: Tue, 30 Nov 2021 04:36:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141c1ce2f203145a20c1b4550c662f943266dc7dbf7e15ee911b06456e2326da`  
		Last Modified: Fri, 04 Mar 2022 01:21:28 GMT  
		Size: 110.2 MB (110186591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4c7319106ffbcda864c88220ef7a19e3da3b571fa08e0be968efe7fbd9465f`  
		Last Modified: Fri, 04 Mar 2022 01:21:14 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0f327525fd9ac01a04ccd2c1530800b0c51b68d8821a2904e3d066d8663b3f`  
		Last Modified: Fri, 04 Mar 2022 04:22:46 GMT  
		Size: 6.8 MB (6821521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd85b87242bfb046d67955057b47bfdc6f774636e6b8334022ed51fe020a6301`  
		Last Modified: Fri, 04 Mar 2022 04:22:45 GMT  
		Size: 1.2 MB (1244966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32b29093c0b4e0e55e5212230f0fda6566f59ae3e6f91d6ae6b39363b0e7860`  
		Last Modified: Fri, 04 Mar 2022 04:22:45 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:f7e1a9b85365f550da1a0a03bbc6f0dc1c5930d86fcb7e857919ed50708462d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115838871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71a25849e386c048c58fcafd1884613238beacc8243d9fcdddddddbd10b458a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 02:32:18 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 02:32:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 02:32:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 22:50:05 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 03 Mar 2022 22:53:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 03 Mar 2022 22:53:52 GMT
ENV GOPATH=/go
# Thu, 03 Mar 2022 22:53:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 22:53:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 03 Mar 2022 22:53:54 GMT
WORKDIR /go
# Thu, 03 Mar 2022 23:28:42 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:49:51 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:49:52 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 22:49:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:49:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:49:55 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:49:55 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228ad0256439cce3fe9db355991b0557f55241d8cca8690f4f741e1c2d8fb8b9`  
		Last Modified: Tue, 30 Nov 2021 02:47:28 GMT  
		Size: 282.1 KB (282105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cab2a064767512d7d354e806cbd8b24ffefc15e06eeb7d4b127e7f6cddb6b40`  
		Last Modified: Tue, 30 Nov 2021 02:47:28 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798ddefed71bfdadb9d2b02c26fb7579e437fcf60f8af3f7cefed7967580d7da`  
		Last Modified: Thu, 03 Mar 2022 23:08:07 GMT  
		Size: 105.1 MB (105068635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7451a2cdc06b1d637a7e3849503cd56318bc1eb291dc792a6294cec777a31980`  
		Last Modified: Thu, 03 Mar 2022 23:06:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3489c6c0bcd6d649e4760550c8033a06b697ff4490644c130dde6501db25ab26`  
		Last Modified: Thu, 03 Mar 2022 23:29:55 GMT  
		Size: 6.7 MB (6677482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6889976625624adb9a9c5b111609959fe4da102919177fa9c53a23d173175d6`  
		Last Modified: Thu, 10 Mar 2022 22:51:59 GMT  
		Size: 1.2 MB (1178508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79172ebfda03823b62d347d32a6755fe56f0f8809466f11895c5a7d7ae48c3b0`  
		Last Modified: Thu, 10 Mar 2022 22:51:58 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:06e29bc1ce4d22e988eca705e6e4faf2ec70661ffb2a448a334e8b557068dd68
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114698943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14dc63acb649973c1c8c9f6f76def65c297a511f53a12f94af418ebc1c8da64e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:10:37 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 04:10:39 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 04:10:39 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:51:53 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 00:55:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 00:55:09 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 00:55:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:55:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 00:55:12 GMT
WORKDIR /go
# Fri, 04 Mar 2022 06:45:24 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:57:52 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:57:53 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 22:57:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:57:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:57:56 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:57:56 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f21e2af73375430a6481f93a61f3df4f9de38c985f83b27293f8aace16d6b5`  
		Last Modified: Tue, 30 Nov 2021 04:33:33 GMT  
		Size: 281.2 KB (281248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cec97f9b59f8579851b3f2c1523c8a96065c591f5961858420e92bf9d424d2`  
		Last Modified: Tue, 30 Nov 2021 04:33:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edfb2fbd38ed3972211201867b2a8e18c8dc23b141d716828e9914c61276ecd`  
		Last Modified: Fri, 04 Mar 2022 01:19:22 GMT  
		Size: 104.9 MB (104853230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a4329e8253fda916ae04b5a3c4d217f5f24639ce303c8a3f2b24588f490196`  
		Last Modified: Fri, 04 Mar 2022 01:18:12 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c608e2c7ee3c9ef36153815e881ac6bc5cf7ff68862fcddf588d11054f20923`  
		Last Modified: Fri, 04 Mar 2022 06:46:39 GMT  
		Size: 6.0 MB (5952263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca89b858a1ebd99c4675cae20c8f5c5e60653a6d2a307ec0bcd6e2e3b448d087`  
		Last Modified: Thu, 10 Mar 2022 23:00:00 GMT  
		Size: 1.2 MB (1176718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9c6a4e7cfb70b12bfb81a4fced64fb3d181017de696421ab4178c208f5defa`  
		Last Modified: Thu, 10 Mar 2022 22:59:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:ee6d440f72726b2d9d29a604a97ab0cc23505e8eccc68c64133eba5da0ef12de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115495270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9fe816e095b9092b887d34923435e91de44876c56fc189162c309a48f541ca`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 01:54:59 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 01:55:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 01:55:01 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 02:29:42 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 02:31:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 02:31:06 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 02:31:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 02:31:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 02:31:09 GMT
WORKDIR /go
# Fri, 04 Mar 2022 03:10:53 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:39:34 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:39:34 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 22:39:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:39:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:39:38 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:39:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a89e8eeedd549875510e5e4e14010906a58878526814e6df25d14009856c6ff`  
		Last Modified: Tue, 30 Nov 2021 02:05:10 GMT  
		Size: 281.9 KB (281899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94645a83ff95687e6f078c140cfcac8def006923ed4019ef74fa189e6d9f0b14`  
		Last Modified: Tue, 30 Nov 2021 02:05:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caad3c9267df5b5261016d2d8843a47ffd88678a81f5e2363c426640adaf2029`  
		Last Modified: Fri, 04 Mar 2022 02:41:55 GMT  
		Size: 104.4 MB (104422515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e36f09527def3bbe5253cea2be9051532cf4a71f0df8fec8a85c922ce640c36`  
		Last Modified: Fri, 04 Mar 2022 02:41:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336ffb45c2b4e74ba78ba96c6f82f7fec126618bbacdc0fa27c7d3677b5aa6f1`  
		Last Modified: Fri, 04 Mar 2022 03:11:32 GMT  
		Size: 6.9 MB (6926057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acd88183c62587770b090ffe6a970e05212ee61f949af7bad8e6edcb5743f0a`  
		Last Modified: Thu, 10 Mar 2022 22:40:54 GMT  
		Size: 1.1 MB (1148678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb0f9bf906b045657c360d551af06aa0af8bee7cbeb2e646cafa48abc2ac878`  
		Last Modified: Thu, 10 Mar 2022 22:40:54 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:4a53d3e10c18d0855f3ec5c9ec6dfb598f1a562d0828ec62b238370646e46e8a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114325817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251761ef86f00954d0b3d990c694bdcc74f14f6488585eef034148425fed6f23`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 03:17:54 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 03:17:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 03:18:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:12:42 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 00:15:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 00:15:47 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 00:15:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:15:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 00:15:58 GMT
WORKDIR /go
# Fri, 04 Mar 2022 07:20:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 04 Mar 2022 07:20:21 GMT
ENV XCADDY_VERSION=v0.2.0
# Fri, 04 Mar 2022 07:20:27 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 04 Mar 2022 07:20:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 04 Mar 2022 07:20:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 04 Mar 2022 07:20:51 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 04 Mar 2022 07:20:57 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28be42a6852cc2108ddba1e4252671ae20275780a6ff73b1038699f59da2ac20`  
		Last Modified: Tue, 30 Nov 2021 03:35:16 GMT  
		Size: 284.0 KB (284020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d744d6799a13f2f7a7f85e040ddf0cc8b671a7cc5572b7049c3e1da8139b349`  
		Last Modified: Tue, 30 Nov 2021 03:35:15 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3620d170b59e9b8337616ec72da9ade5c2471d3b0cf50e3a538e6171d5d813a4`  
		Last Modified: Fri, 04 Mar 2022 00:33:32 GMT  
		Size: 102.8 MB (102785250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bec6e3bcdb44b28a2f07f58bc175553abc87d573010ff47564a72aff7749eb5`  
		Last Modified: Fri, 04 Mar 2022 00:33:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75230c4358c070669508567379db20aa0f6acf5775eb391f81394cc567994d4`  
		Last Modified: Fri, 04 Mar 2022 07:21:55 GMT  
		Size: 7.3 MB (7321033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29c6375e4c4e1312ebfadd212ce4b17f7f002743d73d01fca882a24eba618ac`  
		Last Modified: Fri, 04 Mar 2022 07:21:54 GMT  
		Size: 1.1 MB (1120019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47ae1c41cc141d20ffc3fe6ecccea9ac5fb48eefdeab0dec835beb21c731ac4`  
		Last Modified: Fri, 04 Mar 2022 07:21:54 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:43996cf55b905a5c54ef7cc5f9192ec4077d75694985c130d4866c3c9a537109
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118763072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad0782969bd455fc3ed6f62197dd5e0686ae55f02024605d501e975ceaf4c99`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:07:57 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 04:07:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 04:07:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 23:09:57 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 03 Mar 2022 23:12:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 03 Mar 2022 23:12:29 GMT
ENV GOPATH=/go
# Thu, 03 Mar 2022 23:12:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 23:12:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 03 Mar 2022 23:12:29 GMT
WORKDIR /go
# Fri, 04 Mar 2022 00:05:09 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:41:34 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:41:35 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 22:41:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:41:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:41:36 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:41:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66787da5af638f8523e4694d81d38c2ca7c0a262f4cb8d78c46f7d64833bbaa0`  
		Last Modified: Tue, 30 Nov 2021 04:17:43 GMT  
		Size: 282.4 KB (282378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406f41068af489d7950f1a75d72455e702ed7da98dad21d9267448257b6a2ddc`  
		Last Modified: Tue, 30 Nov 2021 04:17:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee9a2e8145f1c142e4295add6c8c87e35418763276db9058b5b7ed0cc175e80`  
		Last Modified: Thu, 03 Mar 2022 23:26:10 GMT  
		Size: 107.7 MB (107739292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1f97ab22dac5e8b60c0770634135f40d0eba00b3f8a5bd5de06c0b1f34676d`  
		Last Modified: Thu, 03 Mar 2022 23:25:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5bcd397c1a177db9a5bf9729e85c6d9a4a1a63fe402e4e054b80d981f46080`  
		Last Modified: Fri, 04 Mar 2022 00:05:47 GMT  
		Size: 6.9 MB (6930956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d87e4b5eaf820e1c3e543e167ee9e5db5c696e7841ea413858457b48b15e52c`  
		Last Modified: Thu, 10 Mar 2022 22:42:44 GMT  
		Size: 1.2 MB (1203783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16912306174cfd07dbe9e0cf2ce772627716514cc6055ff20659a6479af1548`  
		Last Modified: Thu, 10 Mar 2022 22:42:44 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:c485fc87f90e75e6405dc43fcc37c2ade914702f8ed320b630861e35ccd420f3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2888375962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a30a1f214b7532e10adc147e08b39a03f124d3aa580118b82b5e517d5aa4dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 13:17:25 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Mar 2022 13:17:26 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Mar 2022 13:17:27 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Mar 2022 13:17:28 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Mar 2022 13:19:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:19:56 GMT
ENV GOPATH=C:\go
# Wed, 09 Mar 2022 13:20:52 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Mar 2022 13:35:10 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 09 Mar 2022 13:38:26 GMT
RUN $url = 'https://dl.google.com/go/go1.17.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '85ccf2608dca6ea9a46b6538c9e75e7cf2aebdf502379843b248e26b8bb110be'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:38:28 GMT
WORKDIR C:\go
# Wed, 09 Mar 2022 18:27:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:27:12 GMT
ENV XCADDY_VERSION=v0.2.0
# Wed, 09 Mar 2022 18:27:14 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:27:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 09 Mar 2022 18:28:10 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 09 Mar 2022 18:28:11 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7705bbffd7dc00934e935de0e00e09a7b0da55d66c596622f094495478dd71`  
		Last Modified: Wed, 09 Mar 2022 14:04:13 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be7ff0bb187d149a5cf3c76e1ec444d0e07c6606f67b2c921c67ec91829ea03`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876223f25b257577440a80fdee021b43c33ce3c56be9a20b2ddeaede95240522`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991eea244b9c3a1849c84748425dd9e9fbf9ec359ad9329796131b929239ffa4`  
		Last Modified: Wed, 09 Mar 2022 14:04:11 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b4c7c9740eb99bf626b312aa69396db3d186c5bd0e092b01c078ca7248e386`  
		Last Modified: Wed, 09 Mar 2022 14:04:40 GMT  
		Size: 25.5 MB (25454695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f6c8a4d4848c21636a48a69a569a5372ec4890ea029f1f620dda76078bdcef`  
		Last Modified: Wed, 09 Mar 2022 14:04:09 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ac6d527939082add6d21652ba4888acc5a6e7607365168d8e61fb1485339cb`  
		Last Modified: Wed, 09 Mar 2022 14:04:10 GMT  
		Size: 313.6 KB (313592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37aeceb8c2e5bb3c500129bcf20c3f8aea8c68c353e6714a63a225ed1546e8a1`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d88cd595dc7580d72420b7288c52d4b32201045a13dda1a7b943d9a3468adef`  
		Last Modified: Wed, 09 Mar 2022 14:13:05 GMT  
		Size: 145.5 MB (145488847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be492983ee2b2c9128ce0c732c441ae5fbd203cdb71c94faa253c24b01750c90`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa7b09ca61eb1fbafacee427b430b0879ad4da23e62e430a3fe6a66f181f642`  
		Last Modified: Wed, 09 Mar 2022 18:30:00 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468156ad0978bb8919deb642986d1eb42a6e00ea9c3294930a526771ff120f59`  
		Last Modified: Wed, 09 Mar 2022 18:29:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13b17cf7c5867462fbdd3605d90437e19301e9a4d3d41cf90d2c1561c689c50`  
		Last Modified: Wed, 09 Mar 2022 18:29:58 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a1eca5bdf4cf75e747993b512d64c980670337f17807b0daeac5ec4bb41d26`  
		Last Modified: Wed, 09 Mar 2022 18:29:58 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8171f34c3c578dc87b1d9cc5911249fb1f03964352906509faf9492d07cca7c0`  
		Last Modified: Wed, 09 Mar 2022 18:29:58 GMT  
		Size: 1.6 MB (1647844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8937298adab332653decbee0cd826d99541996c5098544285d35579c47c367a`  
		Last Modified: Wed, 09 Mar 2022 18:29:58 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.14393.4886; amd64

```console
$ docker pull caddy@sha256:22cae5265f5cb60aa10f7a056b9281b4e61d0e14f16b5454f5b90f8c14e10e6f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6455446654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4079b70701d5a0ca0af10a7038d5f468c00e36871a95feb8e6e4926bda5e7d00`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 06 Jan 2022 14:33:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Jan 2022 19:14:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Jan 2022 23:34:03 GMT
ENV GIT_VERSION=2.23.0
# Tue, 11 Jan 2022 23:34:05 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 11 Jan 2022 23:34:06 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 11 Jan 2022 23:34:07 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 11 Jan 2022 23:35:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 11 Jan 2022 23:35:42 GMT
ENV GOPATH=C:\go
# Tue, 11 Jan 2022 23:36:45 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Jan 2022 23:57:30 GMT
ENV GOLANG_VERSION=1.17.6
# Wed, 12 Jan 2022 00:01:53 GMT
RUN $url = 'https://dl.google.com/go/go1.17.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '5bf8f87aec7edfc08e6bc845f1c30dba6de32b863f89ae46553ff4bbcc1d4954'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 12 Jan 2022 00:01:55 GMT
WORKDIR C:\go
# Wed, 12 Jan 2022 06:32:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jan 2022 06:32:49 GMT
ENV XCADDY_VERSION=v0.2.0
# Wed, 12 Jan 2022 06:32:50 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 12 Jan 2022 06:32:51 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 12 Jan 2022 06:33:57 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 12 Jan 2022 06:33:58 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8428508ffd63b4af1ba690ec41e82a116f10ec6c3fb70962348f5448d42e5835`  
		Size: 2.2 GB (2208216859 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9b5116c05ddf6ecb5a348f7628e3f3264afbb9909d86798316dbaff4a0e991a2`  
		Last Modified: Tue, 11 Jan 2022 19:35:13 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2caa59a1aaa1c092020bbca2ed4bb1396365f4d9d04ddbbd111ee689414c97a`  
		Last Modified: Wed, 12 Jan 2022 00:35:16 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9fe19533bf1afd7f80fd9cf407f00011eff59836d40dcceb1896e75ea99bf5`  
		Last Modified: Wed, 12 Jan 2022 00:35:13 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40700bafb918466fc1727b2e59ec5eb21d347affb09989cc72ac6db12220b882`  
		Last Modified: Wed, 12 Jan 2022 00:35:12 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3180faaeb4219e7d41bb57faeebe12d142e8e246bac5ab81c8ef38499116de13`  
		Last Modified: Wed, 12 Jan 2022 00:35:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6189cfcbd5a7447e171b486da44213e8ff4721ecbf15998668c0b32e6fb06aaa`  
		Last Modified: Wed, 12 Jan 2022 00:35:18 GMT  
		Size: 25.4 MB (25440280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4766ed70813b67e83228fa314c288fe9a1998bb85cbbd29f2a4b0518e49a7c15`  
		Last Modified: Wed, 12 Jan 2022 00:35:09 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8f2e04b601edd119e847cbb2468052ab4681cd44bf4e9bbdf9b6c3f792d0ae`  
		Last Modified: Wed, 12 Jan 2022 00:35:09 GMT  
		Size: 306.6 KB (306585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef103850c637e1ce1f8d175e0c4b5c7d6c2a3a29d2b8ad15bed8eab49be3dde0`  
		Last Modified: Wed, 12 Jan 2022 00:39:29 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce1f406ac407910a0724e1fbad6ed8772a277ce69316a98a2defcebb5320504`  
		Last Modified: Wed, 12 Jan 2022 00:40:03 GMT  
		Size: 149.8 MB (149846909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdefe1352ad86026fe87510dd97f9a9acdbb5a700fc6a8aea2bd6eaa3194bd6`  
		Last Modified: Wed, 12 Jan 2022 00:39:28 GMT  
		Size: 1.6 KB (1562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1578c0afb3c1729e44264a61a125be686ed8e738b033a03917b80f62aea0ed46`  
		Last Modified: Wed, 12 Jan 2022 06:35:55 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0d89ba8c66caec659fce7ea59e230983c2e8129e3026228cce6945904233cf`  
		Last Modified: Wed, 12 Jan 2022 06:35:53 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e135d2e9e9a157d6d87f8f0e5e9cf6aef249cd9aac5e2b4313784e2d31664990`  
		Last Modified: Wed, 12 Jan 2022 06:35:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715ab69f5d21664707eee604a40f003fbd665f65c14431d564a82a614b277496`  
		Last Modified: Wed, 12 Jan 2022 06:35:53 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833db9ca0e9e1914a35515e476460cdd0bcc36174f85c13dd8646945c5199cde`  
		Last Modified: Wed, 12 Jan 2022 06:35:53 GMT  
		Size: 1.6 MB (1631613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c57f5273b431c8d65b59b81e63af176c5126e1b0d33f4d7b4ece422a1e01562`  
		Last Modified: Wed, 12 Jan 2022 06:35:53 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:81586ffc8035d6323a8f32f47db99a14c976beeeaba313cee4b752d63944db5b
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
$ docker pull caddy@sha256:9c6a77c878ea39bd367c8c7e73f1a75a6ce97101bef0f3de7e288934b4de519e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121354364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c3a82ad51f9b44b272a32de82576c64480a940db9877dd465101c921e11593`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:21:45 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 04:21:46 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 04:21:47 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 01:05:33 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 01:08:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 01:08:13 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 01:08:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 01:08:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 01:08:14 GMT
WORKDIR /go
# Fri, 04 Mar 2022 04:22:25 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 04 Mar 2022 04:22:25 GMT
ENV XCADDY_VERSION=v0.2.0
# Fri, 04 Mar 2022 04:22:26 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 04 Mar 2022 04:22:26 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 04 Mar 2022 04:22:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 04 Mar 2022 04:22:27 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 04 Mar 2022 04:22:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666ba61612fd7c93393f9a5bc1751d8a9929e32d51501dba691da9e8232bc87b`  
		Last Modified: Tue, 30 Nov 2021 04:36:04 GMT  
		Size: 282.2 KB (282159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed8ca4862056a130f714accb3538decfa0663fec84e635d8b5a0a3305353dee`  
		Last Modified: Tue, 30 Nov 2021 04:36:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141c1ce2f203145a20c1b4550c662f943266dc7dbf7e15ee911b06456e2326da`  
		Last Modified: Fri, 04 Mar 2022 01:21:28 GMT  
		Size: 110.2 MB (110186591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4c7319106ffbcda864c88220ef7a19e3da3b571fa08e0be968efe7fbd9465f`  
		Last Modified: Fri, 04 Mar 2022 01:21:14 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0f327525fd9ac01a04ccd2c1530800b0c51b68d8821a2904e3d066d8663b3f`  
		Last Modified: Fri, 04 Mar 2022 04:22:46 GMT  
		Size: 6.8 MB (6821521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd85b87242bfb046d67955057b47bfdc6f774636e6b8334022ed51fe020a6301`  
		Last Modified: Fri, 04 Mar 2022 04:22:45 GMT  
		Size: 1.2 MB (1244966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32b29093c0b4e0e55e5212230f0fda6566f59ae3e6f91d6ae6b39363b0e7860`  
		Last Modified: Fri, 04 Mar 2022 04:22:45 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:f7e1a9b85365f550da1a0a03bbc6f0dc1c5930d86fcb7e857919ed50708462d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115838871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71a25849e386c048c58fcafd1884613238beacc8243d9fcdddddddbd10b458a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 02:32:18 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 02:32:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 02:32:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 22:50:05 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 03 Mar 2022 22:53:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 03 Mar 2022 22:53:52 GMT
ENV GOPATH=/go
# Thu, 03 Mar 2022 22:53:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 22:53:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 03 Mar 2022 22:53:54 GMT
WORKDIR /go
# Thu, 03 Mar 2022 23:28:42 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:49:51 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:49:52 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 22:49:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:49:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:49:55 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:49:55 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228ad0256439cce3fe9db355991b0557f55241d8cca8690f4f741e1c2d8fb8b9`  
		Last Modified: Tue, 30 Nov 2021 02:47:28 GMT  
		Size: 282.1 KB (282105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cab2a064767512d7d354e806cbd8b24ffefc15e06eeb7d4b127e7f6cddb6b40`  
		Last Modified: Tue, 30 Nov 2021 02:47:28 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798ddefed71bfdadb9d2b02c26fb7579e437fcf60f8af3f7cefed7967580d7da`  
		Last Modified: Thu, 03 Mar 2022 23:08:07 GMT  
		Size: 105.1 MB (105068635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7451a2cdc06b1d637a7e3849503cd56318bc1eb291dc792a6294cec777a31980`  
		Last Modified: Thu, 03 Mar 2022 23:06:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3489c6c0bcd6d649e4760550c8033a06b697ff4490644c130dde6501db25ab26`  
		Last Modified: Thu, 03 Mar 2022 23:29:55 GMT  
		Size: 6.7 MB (6677482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6889976625624adb9a9c5b111609959fe4da102919177fa9c53a23d173175d6`  
		Last Modified: Thu, 10 Mar 2022 22:51:59 GMT  
		Size: 1.2 MB (1178508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79172ebfda03823b62d347d32a6755fe56f0f8809466f11895c5a7d7ae48c3b0`  
		Last Modified: Thu, 10 Mar 2022 22:51:58 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:06e29bc1ce4d22e988eca705e6e4faf2ec70661ffb2a448a334e8b557068dd68
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114698943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14dc63acb649973c1c8c9f6f76def65c297a511f53a12f94af418ebc1c8da64e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:10:37 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 04:10:39 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 04:10:39 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:51:53 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 00:55:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 00:55:09 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 00:55:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:55:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 00:55:12 GMT
WORKDIR /go
# Fri, 04 Mar 2022 06:45:24 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:57:52 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:57:53 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 22:57:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:57:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:57:56 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:57:56 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f21e2af73375430a6481f93a61f3df4f9de38c985f83b27293f8aace16d6b5`  
		Last Modified: Tue, 30 Nov 2021 04:33:33 GMT  
		Size: 281.2 KB (281248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cec97f9b59f8579851b3f2c1523c8a96065c591f5961858420e92bf9d424d2`  
		Last Modified: Tue, 30 Nov 2021 04:33:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edfb2fbd38ed3972211201867b2a8e18c8dc23b141d716828e9914c61276ecd`  
		Last Modified: Fri, 04 Mar 2022 01:19:22 GMT  
		Size: 104.9 MB (104853230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a4329e8253fda916ae04b5a3c4d217f5f24639ce303c8a3f2b24588f490196`  
		Last Modified: Fri, 04 Mar 2022 01:18:12 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c608e2c7ee3c9ef36153815e881ac6bc5cf7ff68862fcddf588d11054f20923`  
		Last Modified: Fri, 04 Mar 2022 06:46:39 GMT  
		Size: 6.0 MB (5952263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca89b858a1ebd99c4675cae20c8f5c5e60653a6d2a307ec0bcd6e2e3b448d087`  
		Last Modified: Thu, 10 Mar 2022 23:00:00 GMT  
		Size: 1.2 MB (1176718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9c6a4e7cfb70b12bfb81a4fced64fb3d181017de696421ab4178c208f5defa`  
		Last Modified: Thu, 10 Mar 2022 22:59:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:ee6d440f72726b2d9d29a604a97ab0cc23505e8eccc68c64133eba5da0ef12de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115495270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9fe816e095b9092b887d34923435e91de44876c56fc189162c309a48f541ca`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 01:54:59 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 01:55:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 01:55:01 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 02:29:42 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 02:31:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 02:31:06 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 02:31:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 02:31:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 02:31:09 GMT
WORKDIR /go
# Fri, 04 Mar 2022 03:10:53 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:39:34 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:39:34 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 22:39:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:39:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:39:38 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:39:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a89e8eeedd549875510e5e4e14010906a58878526814e6df25d14009856c6ff`  
		Last Modified: Tue, 30 Nov 2021 02:05:10 GMT  
		Size: 281.9 KB (281899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94645a83ff95687e6f078c140cfcac8def006923ed4019ef74fa189e6d9f0b14`  
		Last Modified: Tue, 30 Nov 2021 02:05:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caad3c9267df5b5261016d2d8843a47ffd88678a81f5e2363c426640adaf2029`  
		Last Modified: Fri, 04 Mar 2022 02:41:55 GMT  
		Size: 104.4 MB (104422515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e36f09527def3bbe5253cea2be9051532cf4a71f0df8fec8a85c922ce640c36`  
		Last Modified: Fri, 04 Mar 2022 02:41:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336ffb45c2b4e74ba78ba96c6f82f7fec126618bbacdc0fa27c7d3677b5aa6f1`  
		Last Modified: Fri, 04 Mar 2022 03:11:32 GMT  
		Size: 6.9 MB (6926057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acd88183c62587770b090ffe6a970e05212ee61f949af7bad8e6edcb5743f0a`  
		Last Modified: Thu, 10 Mar 2022 22:40:54 GMT  
		Size: 1.1 MB (1148678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb0f9bf906b045657c360d551af06aa0af8bee7cbeb2e646cafa48abc2ac878`  
		Last Modified: Thu, 10 Mar 2022 22:40:54 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:4a53d3e10c18d0855f3ec5c9ec6dfb598f1a562d0828ec62b238370646e46e8a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114325817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251761ef86f00954d0b3d990c694bdcc74f14f6488585eef034148425fed6f23`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 03:17:54 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 03:17:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 03:18:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:12:42 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 00:15:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 00:15:47 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 00:15:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:15:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 00:15:58 GMT
WORKDIR /go
# Fri, 04 Mar 2022 07:20:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 04 Mar 2022 07:20:21 GMT
ENV XCADDY_VERSION=v0.2.0
# Fri, 04 Mar 2022 07:20:27 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 04 Mar 2022 07:20:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 04 Mar 2022 07:20:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 04 Mar 2022 07:20:51 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 04 Mar 2022 07:20:57 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28be42a6852cc2108ddba1e4252671ae20275780a6ff73b1038699f59da2ac20`  
		Last Modified: Tue, 30 Nov 2021 03:35:16 GMT  
		Size: 284.0 KB (284020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d744d6799a13f2f7a7f85e040ddf0cc8b671a7cc5572b7049c3e1da8139b349`  
		Last Modified: Tue, 30 Nov 2021 03:35:15 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3620d170b59e9b8337616ec72da9ade5c2471d3b0cf50e3a538e6171d5d813a4`  
		Last Modified: Fri, 04 Mar 2022 00:33:32 GMT  
		Size: 102.8 MB (102785250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bec6e3bcdb44b28a2f07f58bc175553abc87d573010ff47564a72aff7749eb5`  
		Last Modified: Fri, 04 Mar 2022 00:33:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75230c4358c070669508567379db20aa0f6acf5775eb391f81394cc567994d4`  
		Last Modified: Fri, 04 Mar 2022 07:21:55 GMT  
		Size: 7.3 MB (7321033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29c6375e4c4e1312ebfadd212ce4b17f7f002743d73d01fca882a24eba618ac`  
		Last Modified: Fri, 04 Mar 2022 07:21:54 GMT  
		Size: 1.1 MB (1120019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47ae1c41cc141d20ffc3fe6ecccea9ac5fb48eefdeab0dec835beb21c731ac4`  
		Last Modified: Fri, 04 Mar 2022 07:21:54 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:43996cf55b905a5c54ef7cc5f9192ec4077d75694985c130d4866c3c9a537109
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118763072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad0782969bd455fc3ed6f62197dd5e0686ae55f02024605d501e975ceaf4c99`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:07:57 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 04:07:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 04:07:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 23:09:57 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 03 Mar 2022 23:12:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 03 Mar 2022 23:12:29 GMT
ENV GOPATH=/go
# Thu, 03 Mar 2022 23:12:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 23:12:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 03 Mar 2022 23:12:29 GMT
WORKDIR /go
# Fri, 04 Mar 2022 00:05:09 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:41:34 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:41:35 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 22:41:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:41:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:41:36 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:41:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66787da5af638f8523e4694d81d38c2ca7c0a262f4cb8d78c46f7d64833bbaa0`  
		Last Modified: Tue, 30 Nov 2021 04:17:43 GMT  
		Size: 282.4 KB (282378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406f41068af489d7950f1a75d72455e702ed7da98dad21d9267448257b6a2ddc`  
		Last Modified: Tue, 30 Nov 2021 04:17:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee9a2e8145f1c142e4295add6c8c87e35418763276db9058b5b7ed0cc175e80`  
		Last Modified: Thu, 03 Mar 2022 23:26:10 GMT  
		Size: 107.7 MB (107739292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1f97ab22dac5e8b60c0770634135f40d0eba00b3f8a5bd5de06c0b1f34676d`  
		Last Modified: Thu, 03 Mar 2022 23:25:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5bcd397c1a177db9a5bf9729e85c6d9a4a1a63fe402e4e054b80d981f46080`  
		Last Modified: Fri, 04 Mar 2022 00:05:47 GMT  
		Size: 6.9 MB (6930956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d87e4b5eaf820e1c3e543e167ee9e5db5c696e7841ea413858457b48b15e52c`  
		Last Modified: Thu, 10 Mar 2022 22:42:44 GMT  
		Size: 1.2 MB (1203783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16912306174cfd07dbe9e0cf2ce772627716514cc6055ff20659a6479af1548`  
		Last Modified: Thu, 10 Mar 2022 22:42:44 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:a4ace300fa0bb8e20564cf55f2e5b24c38f86b8cb8c1f57a3c64f014a6243d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:c485fc87f90e75e6405dc43fcc37c2ade914702f8ed320b630861e35ccd420f3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2888375962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a30a1f214b7532e10adc147e08b39a03f124d3aa580118b82b5e517d5aa4dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 13:17:25 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Mar 2022 13:17:26 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Mar 2022 13:17:27 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Mar 2022 13:17:28 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Mar 2022 13:19:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:19:56 GMT
ENV GOPATH=C:\go
# Wed, 09 Mar 2022 13:20:52 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Mar 2022 13:35:10 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 09 Mar 2022 13:38:26 GMT
RUN $url = 'https://dl.google.com/go/go1.17.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '85ccf2608dca6ea9a46b6538c9e75e7cf2aebdf502379843b248e26b8bb110be'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:38:28 GMT
WORKDIR C:\go
# Wed, 09 Mar 2022 18:27:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:27:12 GMT
ENV XCADDY_VERSION=v0.2.0
# Wed, 09 Mar 2022 18:27:14 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:27:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 09 Mar 2022 18:28:10 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 09 Mar 2022 18:28:11 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7705bbffd7dc00934e935de0e00e09a7b0da55d66c596622f094495478dd71`  
		Last Modified: Wed, 09 Mar 2022 14:04:13 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be7ff0bb187d149a5cf3c76e1ec444d0e07c6606f67b2c921c67ec91829ea03`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876223f25b257577440a80fdee021b43c33ce3c56be9a20b2ddeaede95240522`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991eea244b9c3a1849c84748425dd9e9fbf9ec359ad9329796131b929239ffa4`  
		Last Modified: Wed, 09 Mar 2022 14:04:11 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b4c7c9740eb99bf626b312aa69396db3d186c5bd0e092b01c078ca7248e386`  
		Last Modified: Wed, 09 Mar 2022 14:04:40 GMT  
		Size: 25.5 MB (25454695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f6c8a4d4848c21636a48a69a569a5372ec4890ea029f1f620dda76078bdcef`  
		Last Modified: Wed, 09 Mar 2022 14:04:09 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ac6d527939082add6d21652ba4888acc5a6e7607365168d8e61fb1485339cb`  
		Last Modified: Wed, 09 Mar 2022 14:04:10 GMT  
		Size: 313.6 KB (313592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37aeceb8c2e5bb3c500129bcf20c3f8aea8c68c353e6714a63a225ed1546e8a1`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d88cd595dc7580d72420b7288c52d4b32201045a13dda1a7b943d9a3468adef`  
		Last Modified: Wed, 09 Mar 2022 14:13:05 GMT  
		Size: 145.5 MB (145488847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be492983ee2b2c9128ce0c732c441ae5fbd203cdb71c94faa253c24b01750c90`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa7b09ca61eb1fbafacee427b430b0879ad4da23e62e430a3fe6a66f181f642`  
		Last Modified: Wed, 09 Mar 2022 18:30:00 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468156ad0978bb8919deb642986d1eb42a6e00ea9c3294930a526771ff120f59`  
		Last Modified: Wed, 09 Mar 2022 18:29:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13b17cf7c5867462fbdd3605d90437e19301e9a4d3d41cf90d2c1561c689c50`  
		Last Modified: Wed, 09 Mar 2022 18:29:58 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a1eca5bdf4cf75e747993b512d64c980670337f17807b0daeac5ec4bb41d26`  
		Last Modified: Wed, 09 Mar 2022 18:29:58 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8171f34c3c578dc87b1d9cc5911249fb1f03964352906509faf9492d07cca7c0`  
		Last Modified: Wed, 09 Mar 2022 18:29:58 GMT  
		Size: 1.6 MB (1647844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8937298adab332653decbee0cd826d99541996c5098544285d35579c47c367a`  
		Last Modified: Wed, 09 Mar 2022 18:29:58 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:5f89b604764eb0c53217da81ffe958b02f108847507c400542ef623d0c3acb06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2686; amd64
	-	windows version 10.0.14393.5006; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:f2de2d90885f8cb6d12c79d914e354b41f6bfebc22ba3390096ae69fac380cf5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2728251838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8705f493a3ce58fda2b9ada4d3d27639c9f13835f1fb8d85ecdf795e69dae46a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:20:26 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:20:27 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:21:52 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:21:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:21:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:21:55 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:21:56 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:21:57 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:21:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:21:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:22:00 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:22:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:22:02 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:22:05 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:22:06 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:22:07 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:23:12 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:23:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99d892d6329e540cd98b358cc2f8085a7e6579538de9b4afa3ce0d11a03116`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 365.4 KB (365439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fb2be6c676c8f3e743cd43ec6b238646cf9f8b89a6fb1bde29f9bb52a7296c`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9b968486191ed8bb4a6c85eb678e32bbb062d8998e636e7706431be6e25f51`  
		Last Modified: Wed, 09 Mar 2022 18:29:07 GMT  
		Size: 12.1 MB (12115400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63f0ecb87a49981ac55c8495d8beed3b58d3b15e31ff4ba1140b0176e551265`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5249439459c9b885575d1a0c5c0df8c3e99649414b3c09ef4054e22fab54b584`  
		Last Modified: Wed, 09 Mar 2022 18:29:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69ab39aec279710b6bf7b4581cafe49878e70beff74d4a5e342eea02e60ce60`  
		Last Modified: Wed, 09 Mar 2022 18:29:02 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb81ca26c7a917813faca1d4cb92e1f41e642701d1199c9811ae8f9294e5b6f`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f5adb02b69cdd17e3acff1b0ea61317020c331399b0cb57fa34da5c09956e3`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e95a1158bc8e4066b6eb4211e7e898c86431c53c76c4752dfd7ce0a15cfc48`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579759f42b06baed2eb773c9cf8d6709e48e71afc07751fb3d45f7e4df9d819a`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e477dc674aa75d9872e80416c27f642531913f63b1598f0920a821c8b6cb535c`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03c9bb84aaf51c973e2ae3990a6b45ac835195b5eaae35799354b2aee8dfc2e`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23add58da280a0f09c755eaccccd5ecc95dc65993558d933f499b4c3378c9f70`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e3da14e3fcc65b938eef87893e57b0daa81c012c8789265cd784fb2f3cfcf7`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34cb18e7475b74cb46643f516f65cbd77fa161c461d753b4e62e076f7b221e5`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbd804e2eb98213ed819900a23753f3f2d662eb72c30a86dbbb51bcecc3cebc`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49b05954d4ea193b3f85228739d529bbc2a811204d8b6e22440c97977addbdf`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a3a3abbfe3563eaed35b97ad1ed309a3f4e744f968d0b6f6deaf68211f2fc8`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53542589ba9c33b651da4be35de7384a168d4936d08bb046a632a4d644b46c9e`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 293.3 KB (293252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149ac7945e26171c6dfe9e316c21027eb072f4fd72819f8b80a32eada8275ae2`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.14393.5006; amd64

```console
$ docker pull caddy@sha256:7f8374457a1c63677174631c3a8ea273702e069b924b615f44292250b7e2d8c1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6289879706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba40202b27c7479ec2d1d1618860745715dbfcabf489c651e5f04e826c286f72`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sat, 05 Mar 2022 03:39:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Mar 2022 18:23:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:24:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:24:49 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:26:02 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:26:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:26:04 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:26:05 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:26:06 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:26:07 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:26:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:26:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:26:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:26:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:26:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:26:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:26:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:26:14 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:26:15 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:26:16 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:26:54 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:26:55 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0fe465a8df276d07bd592c9424c00276a476fb7f74be6f867256b07fba31212d`  
		Size: 2.2 GB (2207094901 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c66997424475af0399fffec7897bad20e40b8309c56761077b30f5d9495f4db3`  
		Last Modified: Wed, 09 Mar 2022 18:29:32 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31f3b05b8f63dd42b4881a4c3d384691cc281678a86e0836d0c32819a344b5d`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 345.5 KB (345470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9855b50f056bb89da3373dfb2c128c8cf2515840c723a9027f0c01bb0eb91d`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b715cda286f032f4b113aefacf8b42874e8bed4dbe0080772b9d6cc1e91fc4`  
		Last Modified: Wed, 09 Mar 2022 18:29:43 GMT  
		Size: 12.1 MB (12134708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e40c1797eb55c98999e616bff73129a77843c7cf7667787950662180cbd90b`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d12359d4309d649fc7f0131974324ede0eb7aa11d1cd6f5d47000f9e14363b`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1783134869b6be42026ea8457c2f07dcacd3e029eaa283e48e798ce94929111`  
		Last Modified: Wed, 09 Mar 2022 18:29:28 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7104f8aa42fca009aaea2d885dfc7a0ea9acd8b7670cd9a90929f355d29cb5bf`  
		Last Modified: Wed, 09 Mar 2022 18:29:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ee03e2f86a2587a31a03418808435e9804fd324f95c981776b71ac5541f122`  
		Last Modified: Wed, 09 Mar 2022 18:29:28 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617c8eb23f7d35a0012ac7a3ce817bb49edda99eb16da9e4a9e6897617ded26d`  
		Last Modified: Wed, 09 Mar 2022 18:29:27 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85694b0569ffdf58e2f716205756d0a9eab45456d0ef23c2bbc8cb5816b99c1a`  
		Last Modified: Wed, 09 Mar 2022 18:29:27 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe2abbbf56f3d370ddba372e974d4765e074ee94fa8b1e4037b1cbf9d4a1e04`  
		Last Modified: Wed, 09 Mar 2022 18:29:26 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d4deaae43ac0785c4ccfb22ba187f33035f3041d44d770e8864cab157c1fe8`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7c04adc036f7a25c1c5a61895ba945aac263098d741203cb43e6b3b32174ef`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582d555a149be3d9ce42e33942b905cc2c8b9ebdc0dd1de51709fd7276c1e3ae`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b57929590127351973d44b26f950891ee7b918dc352a68098193a5d4fce629`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71478b5420cbbbea1bb0a6e617445f903203fac8965dfc6e2c41932cbb7f2acb`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b709c8c0d2fb364fd66993072fd79d4d28cda233a5d991b74680a1f80b1563`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c82093ad8180c0667cf71cdf92b8ead740771d5f2f5efda695fc67b815056d9`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34076b974bce5f92149f3e2eb58dc898a74d7ca4c563c20c4308f51a3f25212`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 293.4 KB (293417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e27086943ac64711a35c0e493db7b82a4faa0d65d5e80a91104238aba4845e2`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:a3ba1d80239cc342421e0b3a6a6adba859191852e94c30047402f2ac1cc24407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:f2de2d90885f8cb6d12c79d914e354b41f6bfebc22ba3390096ae69fac380cf5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2728251838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8705f493a3ce58fda2b9ada4d3d27639c9f13835f1fb8d85ecdf795e69dae46a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:20:26 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:20:27 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:21:52 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:21:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:21:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:21:55 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:21:56 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:21:57 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:21:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:21:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:22:00 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:22:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:22:02 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:22:05 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:22:06 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:22:07 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:23:12 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:23:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99d892d6329e540cd98b358cc2f8085a7e6579538de9b4afa3ce0d11a03116`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 365.4 KB (365439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fb2be6c676c8f3e743cd43ec6b238646cf9f8b89a6fb1bde29f9bb52a7296c`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9b968486191ed8bb4a6c85eb678e32bbb062d8998e636e7706431be6e25f51`  
		Last Modified: Wed, 09 Mar 2022 18:29:07 GMT  
		Size: 12.1 MB (12115400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63f0ecb87a49981ac55c8495d8beed3b58d3b15e31ff4ba1140b0176e551265`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5249439459c9b885575d1a0c5c0df8c3e99649414b3c09ef4054e22fab54b584`  
		Last Modified: Wed, 09 Mar 2022 18:29:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69ab39aec279710b6bf7b4581cafe49878e70beff74d4a5e342eea02e60ce60`  
		Last Modified: Wed, 09 Mar 2022 18:29:02 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb81ca26c7a917813faca1d4cb92e1f41e642701d1199c9811ae8f9294e5b6f`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f5adb02b69cdd17e3acff1b0ea61317020c331399b0cb57fa34da5c09956e3`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e95a1158bc8e4066b6eb4211e7e898c86431c53c76c4752dfd7ce0a15cfc48`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579759f42b06baed2eb773c9cf8d6709e48e71afc07751fb3d45f7e4df9d819a`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e477dc674aa75d9872e80416c27f642531913f63b1598f0920a821c8b6cb535c`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03c9bb84aaf51c973e2ae3990a6b45ac835195b5eaae35799354b2aee8dfc2e`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23add58da280a0f09c755eaccccd5ecc95dc65993558d933f499b4c3378c9f70`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e3da14e3fcc65b938eef87893e57b0daa81c012c8789265cd784fb2f3cfcf7`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34cb18e7475b74cb46643f516f65cbd77fa161c461d753b4e62e076f7b221e5`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbd804e2eb98213ed819900a23753f3f2d662eb72c30a86dbbb51bcecc3cebc`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49b05954d4ea193b3f85228739d529bbc2a811204d8b6e22440c97977addbdf`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a3a3abbfe3563eaed35b97ad1ed309a3f4e744f968d0b6f6deaf68211f2fc8`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53542589ba9c33b651da4be35de7384a168d4936d08bb046a632a4d644b46c9e`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 293.3 KB (293252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149ac7945e26171c6dfe9e316c21027eb072f4fd72819f8b80a32eada8275ae2`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.6`

```console
$ docker pull caddy@sha256:184338dab192cd97f7c61b66c021c5709b2418e4826182f553ae09099f5082a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2686; amd64
	-	windows version 10.0.14393.5006; amd64

### `caddy:2.4.6` - linux; amd64

```console
$ docker pull caddy@sha256:7da0f90273e1961d9c38d26809f84d4ef3cdc9b4fc330a9cab22015d7c9e8228
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14856906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439af64db48912c0a446444aae0e357183264ff08e1154fa105d5ee082e0bf13`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:54:17 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 12 Nov 2021 21:54:18 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Fri, 12 Nov 2021 21:54:19 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 12 Nov 2021 21:54:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 12 Nov 2021 21:54:23 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:54:23 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 12 Nov 2021 21:54:23 GMT
ENV XDG_DATA_HOME=/data
# Fri, 12 Nov 2021 21:54:23 GMT
VOLUME [/config]
# Fri, 12 Nov 2021 21:54:24 GMT
VOLUME [/data]
# Fri, 12 Nov 2021 21:54:24 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Fri, 12 Nov 2021 21:54:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 12 Nov 2021 21:54:24 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 12 Nov 2021 21:54:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 12 Nov 2021 21:54:25 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 12 Nov 2021 21:54:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 12 Nov 2021 21:54:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 12 Nov 2021 21:54:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 12 Nov 2021 21:54:25 GMT
EXPOSE 80
# Fri, 12 Nov 2021 21:54:26 GMT
EXPOSE 443
# Fri, 12 Nov 2021 21:54:26 GMT
EXPOSE 2019
# Fri, 12 Nov 2021 21:54:26 GMT
WORKDIR /srv
# Fri, 12 Nov 2021 21:54:26 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ccae726125d77e2fd3891c69c8f663d5fe63d8ad4a67deb284e2c589334497`  
		Last Modified: Fri, 12 Nov 2021 21:54:48 GMT  
		Size: 301.5 KB (301497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de6a61c89acc2147364721befe6e6bf957963713d1ddc4bc6c4a35f7b4b4e0a`  
		Last Modified: Fri, 12 Nov 2021 21:54:48 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ed957bdc008c4cc475fcaeb053cdb7fbcc83f49184fca8013d87cf9d395518`  
		Last Modified: Fri, 12 Nov 2021 21:54:50 GMT  
		Size: 11.7 MB (11726445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae44c2d42ddcf77445d391f491713e6384b933553eb234ceb0d9b3e66c5b33f`  
		Last Modified: Fri, 12 Nov 2021 21:54:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - linux; arm variant v6

```console
$ docker pull caddy@sha256:caa4910dc3572e3ba3888fda3f7f5ed69c8c575461d29e528a6b453c0ba90522
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14068833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358685e491b9f796f29e9b70a0a43f619fa034e7bcd995cf738d811cf8e4ebe9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:07:54 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 12 Nov 2021 17:07:57 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Fri, 12 Nov 2021 17:07:57 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 12 Nov 2021 17:08:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 12 Nov 2021 17:08:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 17:08:04 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 12 Nov 2021 17:08:05 GMT
ENV XDG_DATA_HOME=/data
# Fri, 12 Nov 2021 17:08:05 GMT
VOLUME [/config]
# Fri, 12 Nov 2021 17:08:06 GMT
VOLUME [/data]
# Fri, 12 Nov 2021 17:08:06 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Fri, 12 Nov 2021 17:08:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 12 Nov 2021 17:08:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 12 Nov 2021 17:08:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 12 Nov 2021 17:08:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 12 Nov 2021 17:08:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 12 Nov 2021 17:08:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 12 Nov 2021 17:08:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 12 Nov 2021 17:08:10 GMT
EXPOSE 80
# Fri, 12 Nov 2021 17:08:10 GMT
EXPOSE 443
# Fri, 12 Nov 2021 17:08:11 GMT
EXPOSE 2019
# Fri, 12 Nov 2021 17:08:11 GMT
WORKDIR /srv
# Fri, 12 Nov 2021 17:08:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d466a8f7766a93ea57a37532240c4a8c0e21cdb1f731360b1d21022b74f840f1`  
		Last Modified: Fri, 12 Nov 2021 17:09:28 GMT  
		Size: 301.7 KB (301671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082eb2081a4e07ea8cd0a36b4c3e7fee48ac23e2f6e8b7f95659e9a7465012fb`  
		Last Modified: Fri, 12 Nov 2021 17:09:27 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3790fd0e6afb978b6d8b451eaea5ab3e59b48913548a910853b31bc234bfed1c`  
		Last Modified: Fri, 12 Nov 2021 17:09:35 GMT  
		Size: 11.1 MB (11125784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe30a92d02271e636688f49fc9e1b382f2836b2c4578c29a993dc5111eb0b927`  
		Last Modified: Fri, 12 Nov 2021 17:09:27 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - linux; arm variant v7

```console
$ docker pull caddy@sha256:5211ef3cdd2abf233de36a5e914b3ea2a649f0ec2164e5c63dd96c0cf870004e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13852151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389ecbea3a7d6a7b6a98da18b9b565046f2629b6c4af69a7d20d5cabcd1562d5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 11:43:41 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 13 Nov 2021 11:43:44 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 13 Nov 2021 11:43:44 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 13 Nov 2021 11:43:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 13 Nov 2021 11:43:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 11:43:51 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 13 Nov 2021 11:43:51 GMT
ENV XDG_DATA_HOME=/data
# Sat, 13 Nov 2021 11:43:52 GMT
VOLUME [/config]
# Sat, 13 Nov 2021 11:43:52 GMT
VOLUME [/data]
# Sat, 13 Nov 2021 11:43:53 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 13 Nov 2021 11:43:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 13 Nov 2021 11:43:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 13 Nov 2021 11:43:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 13 Nov 2021 11:43:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 13 Nov 2021 11:43:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 13 Nov 2021 11:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 13 Nov 2021 11:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 13 Nov 2021 11:43:57 GMT
EXPOSE 80
# Sat, 13 Nov 2021 11:43:57 GMT
EXPOSE 443
# Sat, 13 Nov 2021 11:43:58 GMT
EXPOSE 2019
# Sat, 13 Nov 2021 11:43:58 GMT
WORKDIR /srv
# Sat, 13 Nov 2021 11:43:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5663fa07ca1dcac265e40e084d2e40771a9084e9b30309c275bf810e87a3b53a`  
		Last Modified: Sat, 13 Nov 2021 11:45:26 GMT  
		Size: 300.8 KB (300831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf8bc3ddae458c10861b1ef0a30a6c8e97ea3a7135680ced673a2532a4c043e`  
		Last Modified: Sat, 13 Nov 2021 11:45:25 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afb06d1223418bbdf22f64f5a3a57962ad6570d931f931ab8df015439fb0c7a`  
		Last Modified: Sat, 13 Nov 2021 11:45:33 GMT  
		Size: 11.1 MB (11106718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a00e0b33a8465343d1f7f61ffec47a7c7aaad34402170530d9e9ebbb4ac5665`  
		Last Modified: Sat, 13 Nov 2021 11:45:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:8c2b7f01f3d14048e888946dd85b972ac76d22490107d999f6df18399ab76f25
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13763680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e48a5247e105a4ecd7f6a7b3f6bfe21fe6633146de42ad9bd4197b3222b920d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 11:18:37 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 13 Nov 2021 11:18:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 13 Nov 2021 11:18:40 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 13 Nov 2021 11:18:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 13 Nov 2021 11:18:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 11:18:44 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 13 Nov 2021 11:18:45 GMT
ENV XDG_DATA_HOME=/data
# Sat, 13 Nov 2021 11:18:46 GMT
VOLUME [/config]
# Sat, 13 Nov 2021 11:18:47 GMT
VOLUME [/data]
# Sat, 13 Nov 2021 11:18:48 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 13 Nov 2021 11:18:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 13 Nov 2021 11:18:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 13 Nov 2021 11:18:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 13 Nov 2021 11:18:52 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 13 Nov 2021 11:18:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 13 Nov 2021 11:18:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 13 Nov 2021 11:18:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 13 Nov 2021 11:18:56 GMT
EXPOSE 80
# Sat, 13 Nov 2021 11:18:57 GMT
EXPOSE 443
# Sat, 13 Nov 2021 11:18:58 GMT
EXPOSE 2019
# Sat, 13 Nov 2021 11:18:59 GMT
WORKDIR /srv
# Sat, 13 Nov 2021 11:19:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e205c63fa7e1c7a1060c29f8600bf90d965a1d26a1ae313210de738d08649d0`  
		Last Modified: Sat, 13 Nov 2021 11:19:44 GMT  
		Size: 301.4 KB (301450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674f75736ea40598c6df0d5460f914bf940c50952e8f106cdb674f9d98e8c5bb`  
		Last Modified: Sat, 13 Nov 2021 11:19:44 GMT  
		Size: 5.8 KB (5750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e004593c132f71a51cbd6967cf29bac3fc607c79fa8d967253c2f79461442641`  
		Last Modified: Sat, 13 Nov 2021 11:19:45 GMT  
		Size: 10.7 MB (10738627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51900aef2f22db52e1c14e6dd7f645241d02abef12b8ef2b377595f11b77055b`  
		Last Modified: Sat, 13 Nov 2021 11:19:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - linux; ppc64le

```console
$ docker pull caddy@sha256:b47a92735f1a101ce7087f2fc6f8b33614226b32c4507de0de8a4b6b34d84504
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13429323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bbba192f1381ae73d2265be6a6b84d7539131fcc66399931bd66ff97ff83f5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 21:18:00 GMT
ADD file:4d45063079cb28a34f1e382fddb22f156ac99d5449aa05ed37cb653c1f7b80f2 in / 
# Fri, 12 Nov 2021 21:18:01 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 15:14:03 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 13 Nov 2021 15:14:24 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 13 Nov 2021 15:14:33 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 13 Nov 2021 15:14:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 13 Nov 2021 15:14:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 15:14:54 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 13 Nov 2021 15:14:58 GMT
ENV XDG_DATA_HOME=/data
# Sat, 13 Nov 2021 15:15:03 GMT
VOLUME [/config]
# Sat, 13 Nov 2021 15:15:05 GMT
VOLUME [/data]
# Sat, 13 Nov 2021 15:15:09 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 13 Nov 2021 15:15:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 13 Nov 2021 15:15:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 13 Nov 2021 15:15:19 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 13 Nov 2021 15:15:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 13 Nov 2021 15:15:26 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 13 Nov 2021 15:15:30 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 13 Nov 2021 15:15:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 13 Nov 2021 15:15:35 GMT
EXPOSE 80
# Sat, 13 Nov 2021 15:15:37 GMT
EXPOSE 443
# Sat, 13 Nov 2021 15:15:40 GMT
EXPOSE 2019
# Sat, 13 Nov 2021 15:15:42 GMT
WORKDIR /srv
# Sat, 13 Nov 2021 15:15:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:72940440c1ab65eca4d38846164719ffde4b147543cc658d041407a925b13368`  
		Last Modified: Fri, 12 Nov 2021 21:19:32 GMT  
		Size: 2.8 MB (2817467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aca7d05e49e358a035d0dd6f471c0d19419c9cc97646fff4e82578d2c488237`  
		Last Modified: Sat, 13 Nov 2021 15:16:26 GMT  
		Size: 303.6 KB (303607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc78b04675eccc541ab8678fe7221460039d23c40f04c02d41e150f256c4368`  
		Last Modified: Sat, 13 Nov 2021 15:16:25 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f289e05d8a93edbe6667d481e3a61908205bf58c77aa2ddf18b09f740724a8cd`  
		Last Modified: Sat, 13 Nov 2021 15:16:28 GMT  
		Size: 10.3 MB (10302268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd68deeff259e1bcfa76db665a6a52747267383f87bb506b77fbb409529ae3c8`  
		Last Modified: Sat, 13 Nov 2021 15:16:25 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - linux; s390x

```console
$ docker pull caddy@sha256:5ac69c24193df6b0d9b0c13816ce3861b720b62721901b0eb7446bd41ae86a3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14240890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753d56e00623363d01fede6cee26039f1b7efc2f64fccec498168291c9b9ea6b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 04:01:37 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 13 Nov 2021 04:01:38 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 13 Nov 2021 04:01:38 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 13 Nov 2021 04:01:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 13 Nov 2021 04:01:42 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 04:01:42 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 13 Nov 2021 04:01:42 GMT
ENV XDG_DATA_HOME=/data
# Sat, 13 Nov 2021 04:01:42 GMT
VOLUME [/config]
# Sat, 13 Nov 2021 04:01:42 GMT
VOLUME [/data]
# Sat, 13 Nov 2021 04:01:42 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 13 Nov 2021 04:01:44 GMT
EXPOSE 80
# Sat, 13 Nov 2021 04:01:44 GMT
EXPOSE 443
# Sat, 13 Nov 2021 04:01:44 GMT
EXPOSE 2019
# Sat, 13 Nov 2021 04:01:44 GMT
WORKDIR /srv
# Sat, 13 Nov 2021 04:01:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0267ca443b43155e255c1a3bb35bab8ac5b561ddc2d0e768868f13274c7ab32d`  
		Last Modified: Sat, 13 Nov 2021 04:02:28 GMT  
		Size: 301.9 KB (301922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9c9c616a8868c7845a4a9d56e876f1bf42c37dac31b80761370b9af366e4c1`  
		Last Modified: Sat, 13 Nov 2021 04:02:28 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0dfff2c7fb2b8bde893d14f4d66fe6d6e8bee6115e0f4f691f7698d17a51f7`  
		Last Modified: Sat, 13 Nov 2021 04:02:29 GMT  
		Size: 11.3 MB (11323710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc9ba4f178258a6de34c95f9f50fb0fd89e093f552c493cd511cfb5fc39a433`  
		Last Modified: Sat, 13 Nov 2021 04:02:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:f2de2d90885f8cb6d12c79d914e354b41f6bfebc22ba3390096ae69fac380cf5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2728251838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8705f493a3ce58fda2b9ada4d3d27639c9f13835f1fb8d85ecdf795e69dae46a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:20:26 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:20:27 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:21:52 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:21:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:21:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:21:55 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:21:56 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:21:57 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:21:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:21:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:22:00 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:22:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:22:02 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:22:05 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:22:06 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:22:07 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:23:12 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:23:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99d892d6329e540cd98b358cc2f8085a7e6579538de9b4afa3ce0d11a03116`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 365.4 KB (365439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fb2be6c676c8f3e743cd43ec6b238646cf9f8b89a6fb1bde29f9bb52a7296c`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9b968486191ed8bb4a6c85eb678e32bbb062d8998e636e7706431be6e25f51`  
		Last Modified: Wed, 09 Mar 2022 18:29:07 GMT  
		Size: 12.1 MB (12115400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63f0ecb87a49981ac55c8495d8beed3b58d3b15e31ff4ba1140b0176e551265`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5249439459c9b885575d1a0c5c0df8c3e99649414b3c09ef4054e22fab54b584`  
		Last Modified: Wed, 09 Mar 2022 18:29:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69ab39aec279710b6bf7b4581cafe49878e70beff74d4a5e342eea02e60ce60`  
		Last Modified: Wed, 09 Mar 2022 18:29:02 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb81ca26c7a917813faca1d4cb92e1f41e642701d1199c9811ae8f9294e5b6f`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f5adb02b69cdd17e3acff1b0ea61317020c331399b0cb57fa34da5c09956e3`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e95a1158bc8e4066b6eb4211e7e898c86431c53c76c4752dfd7ce0a15cfc48`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579759f42b06baed2eb773c9cf8d6709e48e71afc07751fb3d45f7e4df9d819a`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e477dc674aa75d9872e80416c27f642531913f63b1598f0920a821c8b6cb535c`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03c9bb84aaf51c973e2ae3990a6b45ac835195b5eaae35799354b2aee8dfc2e`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23add58da280a0f09c755eaccccd5ecc95dc65993558d933f499b4c3378c9f70`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e3da14e3fcc65b938eef87893e57b0daa81c012c8789265cd784fb2f3cfcf7`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34cb18e7475b74cb46643f516f65cbd77fa161c461d753b4e62e076f7b221e5`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbd804e2eb98213ed819900a23753f3f2d662eb72c30a86dbbb51bcecc3cebc`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49b05954d4ea193b3f85228739d529bbc2a811204d8b6e22440c97977addbdf`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a3a3abbfe3563eaed35b97ad1ed309a3f4e744f968d0b6f6deaf68211f2fc8`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53542589ba9c33b651da4be35de7384a168d4936d08bb046a632a4d644b46c9e`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 293.3 KB (293252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149ac7945e26171c6dfe9e316c21027eb072f4fd72819f8b80a32eada8275ae2`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - windows version 10.0.14393.5006; amd64

```console
$ docker pull caddy@sha256:7f8374457a1c63677174631c3a8ea273702e069b924b615f44292250b7e2d8c1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6289879706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba40202b27c7479ec2d1d1618860745715dbfcabf489c651e5f04e826c286f72`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sat, 05 Mar 2022 03:39:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Mar 2022 18:23:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:24:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:24:49 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:26:02 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:26:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:26:04 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:26:05 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:26:06 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:26:07 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:26:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:26:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:26:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:26:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:26:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:26:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:26:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:26:14 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:26:15 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:26:16 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:26:54 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:26:55 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0fe465a8df276d07bd592c9424c00276a476fb7f74be6f867256b07fba31212d`  
		Size: 2.2 GB (2207094901 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c66997424475af0399fffec7897bad20e40b8309c56761077b30f5d9495f4db3`  
		Last Modified: Wed, 09 Mar 2022 18:29:32 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31f3b05b8f63dd42b4881a4c3d384691cc281678a86e0836d0c32819a344b5d`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 345.5 KB (345470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9855b50f056bb89da3373dfb2c128c8cf2515840c723a9027f0c01bb0eb91d`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b715cda286f032f4b113aefacf8b42874e8bed4dbe0080772b9d6cc1e91fc4`  
		Last Modified: Wed, 09 Mar 2022 18:29:43 GMT  
		Size: 12.1 MB (12134708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e40c1797eb55c98999e616bff73129a77843c7cf7667787950662180cbd90b`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d12359d4309d649fc7f0131974324ede0eb7aa11d1cd6f5d47000f9e14363b`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1783134869b6be42026ea8457c2f07dcacd3e029eaa283e48e798ce94929111`  
		Last Modified: Wed, 09 Mar 2022 18:29:28 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7104f8aa42fca009aaea2d885dfc7a0ea9acd8b7670cd9a90929f355d29cb5bf`  
		Last Modified: Wed, 09 Mar 2022 18:29:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ee03e2f86a2587a31a03418808435e9804fd324f95c981776b71ac5541f122`  
		Last Modified: Wed, 09 Mar 2022 18:29:28 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617c8eb23f7d35a0012ac7a3ce817bb49edda99eb16da9e4a9e6897617ded26d`  
		Last Modified: Wed, 09 Mar 2022 18:29:27 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85694b0569ffdf58e2f716205756d0a9eab45456d0ef23c2bbc8cb5816b99c1a`  
		Last Modified: Wed, 09 Mar 2022 18:29:27 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe2abbbf56f3d370ddba372e974d4765e074ee94fa8b1e4037b1cbf9d4a1e04`  
		Last Modified: Wed, 09 Mar 2022 18:29:26 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d4deaae43ac0785c4ccfb22ba187f33035f3041d44d770e8864cab157c1fe8`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7c04adc036f7a25c1c5a61895ba945aac263098d741203cb43e6b3b32174ef`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582d555a149be3d9ce42e33942b905cc2c8b9ebdc0dd1de51709fd7276c1e3ae`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b57929590127351973d44b26f950891ee7b918dc352a68098193a5d4fce629`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71478b5420cbbbea1bb0a6e617445f903203fac8965dfc6e2c41932cbb7f2acb`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b709c8c0d2fb364fd66993072fd79d4d28cda233a5d991b74680a1f80b1563`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c82093ad8180c0667cf71cdf92b8ead740771d5f2f5efda695fc67b815056d9`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34076b974bce5f92149f3e2eb58dc898a74d7ca4c563c20c4308f51a3f25212`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 293.4 KB (293417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e27086943ac64711a35c0e493db7b82a4faa0d65d5e80a91104238aba4845e2`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.6-alpine`

```console
$ docker pull caddy@sha256:1659785ea84188c3ad22a6c1f96f463d167a4b81318d71f4bb6e3d37dbe73908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.4.6-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:7da0f90273e1961d9c38d26809f84d4ef3cdc9b4fc330a9cab22015d7c9e8228
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14856906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439af64db48912c0a446444aae0e357183264ff08e1154fa105d5ee082e0bf13`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:54:17 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 12 Nov 2021 21:54:18 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Fri, 12 Nov 2021 21:54:19 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 12 Nov 2021 21:54:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 12 Nov 2021 21:54:23 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:54:23 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 12 Nov 2021 21:54:23 GMT
ENV XDG_DATA_HOME=/data
# Fri, 12 Nov 2021 21:54:23 GMT
VOLUME [/config]
# Fri, 12 Nov 2021 21:54:24 GMT
VOLUME [/data]
# Fri, 12 Nov 2021 21:54:24 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Fri, 12 Nov 2021 21:54:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 12 Nov 2021 21:54:24 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 12 Nov 2021 21:54:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 12 Nov 2021 21:54:25 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 12 Nov 2021 21:54:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 12 Nov 2021 21:54:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 12 Nov 2021 21:54:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 12 Nov 2021 21:54:25 GMT
EXPOSE 80
# Fri, 12 Nov 2021 21:54:26 GMT
EXPOSE 443
# Fri, 12 Nov 2021 21:54:26 GMT
EXPOSE 2019
# Fri, 12 Nov 2021 21:54:26 GMT
WORKDIR /srv
# Fri, 12 Nov 2021 21:54:26 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ccae726125d77e2fd3891c69c8f663d5fe63d8ad4a67deb284e2c589334497`  
		Last Modified: Fri, 12 Nov 2021 21:54:48 GMT  
		Size: 301.5 KB (301497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de6a61c89acc2147364721befe6e6bf957963713d1ddc4bc6c4a35f7b4b4e0a`  
		Last Modified: Fri, 12 Nov 2021 21:54:48 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ed957bdc008c4cc475fcaeb053cdb7fbcc83f49184fca8013d87cf9d395518`  
		Last Modified: Fri, 12 Nov 2021 21:54:50 GMT  
		Size: 11.7 MB (11726445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae44c2d42ddcf77445d391f491713e6384b933553eb234ceb0d9b3e66c5b33f`  
		Last Modified: Fri, 12 Nov 2021 21:54:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:caa4910dc3572e3ba3888fda3f7f5ed69c8c575461d29e528a6b453c0ba90522
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14068833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358685e491b9f796f29e9b70a0a43f619fa034e7bcd995cf738d811cf8e4ebe9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:07:54 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 12 Nov 2021 17:07:57 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Fri, 12 Nov 2021 17:07:57 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 12 Nov 2021 17:08:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 12 Nov 2021 17:08:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 17:08:04 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 12 Nov 2021 17:08:05 GMT
ENV XDG_DATA_HOME=/data
# Fri, 12 Nov 2021 17:08:05 GMT
VOLUME [/config]
# Fri, 12 Nov 2021 17:08:06 GMT
VOLUME [/data]
# Fri, 12 Nov 2021 17:08:06 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Fri, 12 Nov 2021 17:08:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 12 Nov 2021 17:08:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 12 Nov 2021 17:08:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 12 Nov 2021 17:08:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 12 Nov 2021 17:08:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 12 Nov 2021 17:08:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 12 Nov 2021 17:08:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 12 Nov 2021 17:08:10 GMT
EXPOSE 80
# Fri, 12 Nov 2021 17:08:10 GMT
EXPOSE 443
# Fri, 12 Nov 2021 17:08:11 GMT
EXPOSE 2019
# Fri, 12 Nov 2021 17:08:11 GMT
WORKDIR /srv
# Fri, 12 Nov 2021 17:08:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d466a8f7766a93ea57a37532240c4a8c0e21cdb1f731360b1d21022b74f840f1`  
		Last Modified: Fri, 12 Nov 2021 17:09:28 GMT  
		Size: 301.7 KB (301671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082eb2081a4e07ea8cd0a36b4c3e7fee48ac23e2f6e8b7f95659e9a7465012fb`  
		Last Modified: Fri, 12 Nov 2021 17:09:27 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3790fd0e6afb978b6d8b451eaea5ab3e59b48913548a910853b31bc234bfed1c`  
		Last Modified: Fri, 12 Nov 2021 17:09:35 GMT  
		Size: 11.1 MB (11125784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe30a92d02271e636688f49fc9e1b382f2836b2c4578c29a993dc5111eb0b927`  
		Last Modified: Fri, 12 Nov 2021 17:09:27 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:5211ef3cdd2abf233de36a5e914b3ea2a649f0ec2164e5c63dd96c0cf870004e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13852151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389ecbea3a7d6a7b6a98da18b9b565046f2629b6c4af69a7d20d5cabcd1562d5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 11:43:41 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 13 Nov 2021 11:43:44 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 13 Nov 2021 11:43:44 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 13 Nov 2021 11:43:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 13 Nov 2021 11:43:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 11:43:51 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 13 Nov 2021 11:43:51 GMT
ENV XDG_DATA_HOME=/data
# Sat, 13 Nov 2021 11:43:52 GMT
VOLUME [/config]
# Sat, 13 Nov 2021 11:43:52 GMT
VOLUME [/data]
# Sat, 13 Nov 2021 11:43:53 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 13 Nov 2021 11:43:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 13 Nov 2021 11:43:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 13 Nov 2021 11:43:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 13 Nov 2021 11:43:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 13 Nov 2021 11:43:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 13 Nov 2021 11:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 13 Nov 2021 11:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 13 Nov 2021 11:43:57 GMT
EXPOSE 80
# Sat, 13 Nov 2021 11:43:57 GMT
EXPOSE 443
# Sat, 13 Nov 2021 11:43:58 GMT
EXPOSE 2019
# Sat, 13 Nov 2021 11:43:58 GMT
WORKDIR /srv
# Sat, 13 Nov 2021 11:43:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5663fa07ca1dcac265e40e084d2e40771a9084e9b30309c275bf810e87a3b53a`  
		Last Modified: Sat, 13 Nov 2021 11:45:26 GMT  
		Size: 300.8 KB (300831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf8bc3ddae458c10861b1ef0a30a6c8e97ea3a7135680ced673a2532a4c043e`  
		Last Modified: Sat, 13 Nov 2021 11:45:25 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afb06d1223418bbdf22f64f5a3a57962ad6570d931f931ab8df015439fb0c7a`  
		Last Modified: Sat, 13 Nov 2021 11:45:33 GMT  
		Size: 11.1 MB (11106718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a00e0b33a8465343d1f7f61ffec47a7c7aaad34402170530d9e9ebbb4ac5665`  
		Last Modified: Sat, 13 Nov 2021 11:45:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:8c2b7f01f3d14048e888946dd85b972ac76d22490107d999f6df18399ab76f25
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13763680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e48a5247e105a4ecd7f6a7b3f6bfe21fe6633146de42ad9bd4197b3222b920d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 11:18:37 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 13 Nov 2021 11:18:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 13 Nov 2021 11:18:40 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 13 Nov 2021 11:18:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 13 Nov 2021 11:18:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 11:18:44 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 13 Nov 2021 11:18:45 GMT
ENV XDG_DATA_HOME=/data
# Sat, 13 Nov 2021 11:18:46 GMT
VOLUME [/config]
# Sat, 13 Nov 2021 11:18:47 GMT
VOLUME [/data]
# Sat, 13 Nov 2021 11:18:48 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 13 Nov 2021 11:18:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 13 Nov 2021 11:18:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 13 Nov 2021 11:18:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 13 Nov 2021 11:18:52 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 13 Nov 2021 11:18:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 13 Nov 2021 11:18:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 13 Nov 2021 11:18:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 13 Nov 2021 11:18:56 GMT
EXPOSE 80
# Sat, 13 Nov 2021 11:18:57 GMT
EXPOSE 443
# Sat, 13 Nov 2021 11:18:58 GMT
EXPOSE 2019
# Sat, 13 Nov 2021 11:18:59 GMT
WORKDIR /srv
# Sat, 13 Nov 2021 11:19:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e205c63fa7e1c7a1060c29f8600bf90d965a1d26a1ae313210de738d08649d0`  
		Last Modified: Sat, 13 Nov 2021 11:19:44 GMT  
		Size: 301.4 KB (301450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674f75736ea40598c6df0d5460f914bf940c50952e8f106cdb674f9d98e8c5bb`  
		Last Modified: Sat, 13 Nov 2021 11:19:44 GMT  
		Size: 5.8 KB (5750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e004593c132f71a51cbd6967cf29bac3fc607c79fa8d967253c2f79461442641`  
		Last Modified: Sat, 13 Nov 2021 11:19:45 GMT  
		Size: 10.7 MB (10738627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51900aef2f22db52e1c14e6dd7f645241d02abef12b8ef2b377595f11b77055b`  
		Last Modified: Sat, 13 Nov 2021 11:19:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:b47a92735f1a101ce7087f2fc6f8b33614226b32c4507de0de8a4b6b34d84504
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13429323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bbba192f1381ae73d2265be6a6b84d7539131fcc66399931bd66ff97ff83f5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 21:18:00 GMT
ADD file:4d45063079cb28a34f1e382fddb22f156ac99d5449aa05ed37cb653c1f7b80f2 in / 
# Fri, 12 Nov 2021 21:18:01 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 15:14:03 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 13 Nov 2021 15:14:24 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 13 Nov 2021 15:14:33 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 13 Nov 2021 15:14:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 13 Nov 2021 15:14:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 15:14:54 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 13 Nov 2021 15:14:58 GMT
ENV XDG_DATA_HOME=/data
# Sat, 13 Nov 2021 15:15:03 GMT
VOLUME [/config]
# Sat, 13 Nov 2021 15:15:05 GMT
VOLUME [/data]
# Sat, 13 Nov 2021 15:15:09 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 13 Nov 2021 15:15:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 13 Nov 2021 15:15:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 13 Nov 2021 15:15:19 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 13 Nov 2021 15:15:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 13 Nov 2021 15:15:26 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 13 Nov 2021 15:15:30 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 13 Nov 2021 15:15:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 13 Nov 2021 15:15:35 GMT
EXPOSE 80
# Sat, 13 Nov 2021 15:15:37 GMT
EXPOSE 443
# Sat, 13 Nov 2021 15:15:40 GMT
EXPOSE 2019
# Sat, 13 Nov 2021 15:15:42 GMT
WORKDIR /srv
# Sat, 13 Nov 2021 15:15:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:72940440c1ab65eca4d38846164719ffde4b147543cc658d041407a925b13368`  
		Last Modified: Fri, 12 Nov 2021 21:19:32 GMT  
		Size: 2.8 MB (2817467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aca7d05e49e358a035d0dd6f471c0d19419c9cc97646fff4e82578d2c488237`  
		Last Modified: Sat, 13 Nov 2021 15:16:26 GMT  
		Size: 303.6 KB (303607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc78b04675eccc541ab8678fe7221460039d23c40f04c02d41e150f256c4368`  
		Last Modified: Sat, 13 Nov 2021 15:16:25 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f289e05d8a93edbe6667d481e3a61908205bf58c77aa2ddf18b09f740724a8cd`  
		Last Modified: Sat, 13 Nov 2021 15:16:28 GMT  
		Size: 10.3 MB (10302268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd68deeff259e1bcfa76db665a6a52747267383f87bb506b77fbb409529ae3c8`  
		Last Modified: Sat, 13 Nov 2021 15:16:25 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:5ac69c24193df6b0d9b0c13816ce3861b720b62721901b0eb7446bd41ae86a3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14240890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753d56e00623363d01fede6cee26039f1b7efc2f64fccec498168291c9b9ea6b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 04:01:37 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 13 Nov 2021 04:01:38 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 13 Nov 2021 04:01:38 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 13 Nov 2021 04:01:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 13 Nov 2021 04:01:42 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 04:01:42 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 13 Nov 2021 04:01:42 GMT
ENV XDG_DATA_HOME=/data
# Sat, 13 Nov 2021 04:01:42 GMT
VOLUME [/config]
# Sat, 13 Nov 2021 04:01:42 GMT
VOLUME [/data]
# Sat, 13 Nov 2021 04:01:42 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 13 Nov 2021 04:01:44 GMT
EXPOSE 80
# Sat, 13 Nov 2021 04:01:44 GMT
EXPOSE 443
# Sat, 13 Nov 2021 04:01:44 GMT
EXPOSE 2019
# Sat, 13 Nov 2021 04:01:44 GMT
WORKDIR /srv
# Sat, 13 Nov 2021 04:01:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0267ca443b43155e255c1a3bb35bab8ac5b561ddc2d0e768868f13274c7ab32d`  
		Last Modified: Sat, 13 Nov 2021 04:02:28 GMT  
		Size: 301.9 KB (301922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9c9c616a8868c7845a4a9d56e876f1bf42c37dac31b80761370b9af366e4c1`  
		Last Modified: Sat, 13 Nov 2021 04:02:28 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0dfff2c7fb2b8bde893d14f4d66fe6d6e8bee6115e0f4f691f7698d17a51f7`  
		Last Modified: Sat, 13 Nov 2021 04:02:29 GMT  
		Size: 11.3 MB (11323710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc9ba4f178258a6de34c95f9f50fb0fd89e093f552c493cd511cfb5fc39a433`  
		Last Modified: Sat, 13 Nov 2021 04:02:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.6-builder`

```console
$ docker pull caddy@sha256:aeb897e44b8614b95c66f1f00fb2a09b58a8fcb9c4b060e361a5493e626b6b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2686; amd64
	-	windows version 10.0.14393.4886; amd64

### `caddy:2.4.6-builder` - linux; amd64

```console
$ docker pull caddy@sha256:9c6a77c878ea39bd367c8c7e73f1a75a6ce97101bef0f3de7e288934b4de519e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121354364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c3a82ad51f9b44b272a32de82576c64480a940db9877dd465101c921e11593`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:21:45 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 04:21:46 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 04:21:47 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 01:05:33 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 01:08:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 01:08:13 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 01:08:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 01:08:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 01:08:14 GMT
WORKDIR /go
# Fri, 04 Mar 2022 04:22:25 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 04 Mar 2022 04:22:25 GMT
ENV XCADDY_VERSION=v0.2.0
# Fri, 04 Mar 2022 04:22:26 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 04 Mar 2022 04:22:26 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 04 Mar 2022 04:22:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 04 Mar 2022 04:22:27 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 04 Mar 2022 04:22:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666ba61612fd7c93393f9a5bc1751d8a9929e32d51501dba691da9e8232bc87b`  
		Last Modified: Tue, 30 Nov 2021 04:36:04 GMT  
		Size: 282.2 KB (282159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed8ca4862056a130f714accb3538decfa0663fec84e635d8b5a0a3305353dee`  
		Last Modified: Tue, 30 Nov 2021 04:36:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141c1ce2f203145a20c1b4550c662f943266dc7dbf7e15ee911b06456e2326da`  
		Last Modified: Fri, 04 Mar 2022 01:21:28 GMT  
		Size: 110.2 MB (110186591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4c7319106ffbcda864c88220ef7a19e3da3b571fa08e0be968efe7fbd9465f`  
		Last Modified: Fri, 04 Mar 2022 01:21:14 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0f327525fd9ac01a04ccd2c1530800b0c51b68d8821a2904e3d066d8663b3f`  
		Last Modified: Fri, 04 Mar 2022 04:22:46 GMT  
		Size: 6.8 MB (6821521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd85b87242bfb046d67955057b47bfdc6f774636e6b8334022ed51fe020a6301`  
		Last Modified: Fri, 04 Mar 2022 04:22:45 GMT  
		Size: 1.2 MB (1244966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32b29093c0b4e0e55e5212230f0fda6566f59ae3e6f91d6ae6b39363b0e7860`  
		Last Modified: Fri, 04 Mar 2022 04:22:45 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:f7e1a9b85365f550da1a0a03bbc6f0dc1c5930d86fcb7e857919ed50708462d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115838871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71a25849e386c048c58fcafd1884613238beacc8243d9fcdddddddbd10b458a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 02:32:18 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 02:32:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 02:32:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 22:50:05 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 03 Mar 2022 22:53:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 03 Mar 2022 22:53:52 GMT
ENV GOPATH=/go
# Thu, 03 Mar 2022 22:53:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 22:53:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 03 Mar 2022 22:53:54 GMT
WORKDIR /go
# Thu, 03 Mar 2022 23:28:42 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:49:51 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:49:52 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 22:49:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:49:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:49:55 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:49:55 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228ad0256439cce3fe9db355991b0557f55241d8cca8690f4f741e1c2d8fb8b9`  
		Last Modified: Tue, 30 Nov 2021 02:47:28 GMT  
		Size: 282.1 KB (282105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cab2a064767512d7d354e806cbd8b24ffefc15e06eeb7d4b127e7f6cddb6b40`  
		Last Modified: Tue, 30 Nov 2021 02:47:28 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798ddefed71bfdadb9d2b02c26fb7579e437fcf60f8af3f7cefed7967580d7da`  
		Last Modified: Thu, 03 Mar 2022 23:08:07 GMT  
		Size: 105.1 MB (105068635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7451a2cdc06b1d637a7e3849503cd56318bc1eb291dc792a6294cec777a31980`  
		Last Modified: Thu, 03 Mar 2022 23:06:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3489c6c0bcd6d649e4760550c8033a06b697ff4490644c130dde6501db25ab26`  
		Last Modified: Thu, 03 Mar 2022 23:29:55 GMT  
		Size: 6.7 MB (6677482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6889976625624adb9a9c5b111609959fe4da102919177fa9c53a23d173175d6`  
		Last Modified: Thu, 10 Mar 2022 22:51:59 GMT  
		Size: 1.2 MB (1178508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79172ebfda03823b62d347d32a6755fe56f0f8809466f11895c5a7d7ae48c3b0`  
		Last Modified: Thu, 10 Mar 2022 22:51:58 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:06e29bc1ce4d22e988eca705e6e4faf2ec70661ffb2a448a334e8b557068dd68
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114698943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14dc63acb649973c1c8c9f6f76def65c297a511f53a12f94af418ebc1c8da64e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:10:37 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 04:10:39 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 04:10:39 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:51:53 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 00:55:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 00:55:09 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 00:55:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:55:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 00:55:12 GMT
WORKDIR /go
# Fri, 04 Mar 2022 06:45:24 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:57:52 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:57:53 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 22:57:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:57:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:57:56 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:57:56 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f21e2af73375430a6481f93a61f3df4f9de38c985f83b27293f8aace16d6b5`  
		Last Modified: Tue, 30 Nov 2021 04:33:33 GMT  
		Size: 281.2 KB (281248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cec97f9b59f8579851b3f2c1523c8a96065c591f5961858420e92bf9d424d2`  
		Last Modified: Tue, 30 Nov 2021 04:33:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edfb2fbd38ed3972211201867b2a8e18c8dc23b141d716828e9914c61276ecd`  
		Last Modified: Fri, 04 Mar 2022 01:19:22 GMT  
		Size: 104.9 MB (104853230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a4329e8253fda916ae04b5a3c4d217f5f24639ce303c8a3f2b24588f490196`  
		Last Modified: Fri, 04 Mar 2022 01:18:12 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c608e2c7ee3c9ef36153815e881ac6bc5cf7ff68862fcddf588d11054f20923`  
		Last Modified: Fri, 04 Mar 2022 06:46:39 GMT  
		Size: 6.0 MB (5952263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca89b858a1ebd99c4675cae20c8f5c5e60653a6d2a307ec0bcd6e2e3b448d087`  
		Last Modified: Thu, 10 Mar 2022 23:00:00 GMT  
		Size: 1.2 MB (1176718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9c6a4e7cfb70b12bfb81a4fced64fb3d181017de696421ab4178c208f5defa`  
		Last Modified: Thu, 10 Mar 2022 22:59:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:ee6d440f72726b2d9d29a604a97ab0cc23505e8eccc68c64133eba5da0ef12de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115495270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9fe816e095b9092b887d34923435e91de44876c56fc189162c309a48f541ca`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 01:54:59 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 01:55:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 01:55:01 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 02:29:42 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 02:31:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 02:31:06 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 02:31:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 02:31:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 02:31:09 GMT
WORKDIR /go
# Fri, 04 Mar 2022 03:10:53 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:39:34 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:39:34 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 22:39:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:39:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:39:38 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:39:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a89e8eeedd549875510e5e4e14010906a58878526814e6df25d14009856c6ff`  
		Last Modified: Tue, 30 Nov 2021 02:05:10 GMT  
		Size: 281.9 KB (281899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94645a83ff95687e6f078c140cfcac8def006923ed4019ef74fa189e6d9f0b14`  
		Last Modified: Tue, 30 Nov 2021 02:05:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caad3c9267df5b5261016d2d8843a47ffd88678a81f5e2363c426640adaf2029`  
		Last Modified: Fri, 04 Mar 2022 02:41:55 GMT  
		Size: 104.4 MB (104422515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e36f09527def3bbe5253cea2be9051532cf4a71f0df8fec8a85c922ce640c36`  
		Last Modified: Fri, 04 Mar 2022 02:41:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336ffb45c2b4e74ba78ba96c6f82f7fec126618bbacdc0fa27c7d3677b5aa6f1`  
		Last Modified: Fri, 04 Mar 2022 03:11:32 GMT  
		Size: 6.9 MB (6926057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acd88183c62587770b090ffe6a970e05212ee61f949af7bad8e6edcb5743f0a`  
		Last Modified: Thu, 10 Mar 2022 22:40:54 GMT  
		Size: 1.1 MB (1148678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb0f9bf906b045657c360d551af06aa0af8bee7cbeb2e646cafa48abc2ac878`  
		Last Modified: Thu, 10 Mar 2022 22:40:54 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:4a53d3e10c18d0855f3ec5c9ec6dfb598f1a562d0828ec62b238370646e46e8a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114325817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251761ef86f00954d0b3d990c694bdcc74f14f6488585eef034148425fed6f23`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 03:17:54 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 03:17:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 03:18:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:12:42 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 00:15:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 00:15:47 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 00:15:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:15:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 00:15:58 GMT
WORKDIR /go
# Fri, 04 Mar 2022 07:20:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 04 Mar 2022 07:20:21 GMT
ENV XCADDY_VERSION=v0.2.0
# Fri, 04 Mar 2022 07:20:27 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 04 Mar 2022 07:20:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 04 Mar 2022 07:20:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 04 Mar 2022 07:20:51 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 04 Mar 2022 07:20:57 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28be42a6852cc2108ddba1e4252671ae20275780a6ff73b1038699f59da2ac20`  
		Last Modified: Tue, 30 Nov 2021 03:35:16 GMT  
		Size: 284.0 KB (284020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d744d6799a13f2f7a7f85e040ddf0cc8b671a7cc5572b7049c3e1da8139b349`  
		Last Modified: Tue, 30 Nov 2021 03:35:15 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3620d170b59e9b8337616ec72da9ade5c2471d3b0cf50e3a538e6171d5d813a4`  
		Last Modified: Fri, 04 Mar 2022 00:33:32 GMT  
		Size: 102.8 MB (102785250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bec6e3bcdb44b28a2f07f58bc175553abc87d573010ff47564a72aff7749eb5`  
		Last Modified: Fri, 04 Mar 2022 00:33:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75230c4358c070669508567379db20aa0f6acf5775eb391f81394cc567994d4`  
		Last Modified: Fri, 04 Mar 2022 07:21:55 GMT  
		Size: 7.3 MB (7321033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29c6375e4c4e1312ebfadd212ce4b17f7f002743d73d01fca882a24eba618ac`  
		Last Modified: Fri, 04 Mar 2022 07:21:54 GMT  
		Size: 1.1 MB (1120019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47ae1c41cc141d20ffc3fe6ecccea9ac5fb48eefdeab0dec835beb21c731ac4`  
		Last Modified: Fri, 04 Mar 2022 07:21:54 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - linux; s390x

```console
$ docker pull caddy@sha256:43996cf55b905a5c54ef7cc5f9192ec4077d75694985c130d4866c3c9a537109
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118763072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad0782969bd455fc3ed6f62197dd5e0686ae55f02024605d501e975ceaf4c99`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:07:57 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 04:07:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 04:07:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 23:09:57 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 03 Mar 2022 23:12:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 03 Mar 2022 23:12:29 GMT
ENV GOPATH=/go
# Thu, 03 Mar 2022 23:12:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 23:12:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 03 Mar 2022 23:12:29 GMT
WORKDIR /go
# Fri, 04 Mar 2022 00:05:09 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:41:34 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:41:35 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 22:41:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:41:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:41:36 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:41:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66787da5af638f8523e4694d81d38c2ca7c0a262f4cb8d78c46f7d64833bbaa0`  
		Last Modified: Tue, 30 Nov 2021 04:17:43 GMT  
		Size: 282.4 KB (282378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406f41068af489d7950f1a75d72455e702ed7da98dad21d9267448257b6a2ddc`  
		Last Modified: Tue, 30 Nov 2021 04:17:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee9a2e8145f1c142e4295add6c8c87e35418763276db9058b5b7ed0cc175e80`  
		Last Modified: Thu, 03 Mar 2022 23:26:10 GMT  
		Size: 107.7 MB (107739292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1f97ab22dac5e8b60c0770634135f40d0eba00b3f8a5bd5de06c0b1f34676d`  
		Last Modified: Thu, 03 Mar 2022 23:25:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5bcd397c1a177db9a5bf9729e85c6d9a4a1a63fe402e4e054b80d981f46080`  
		Last Modified: Fri, 04 Mar 2022 00:05:47 GMT  
		Size: 6.9 MB (6930956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d87e4b5eaf820e1c3e543e167ee9e5db5c696e7841ea413858457b48b15e52c`  
		Last Modified: Thu, 10 Mar 2022 22:42:44 GMT  
		Size: 1.2 MB (1203783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16912306174cfd07dbe9e0cf2ce772627716514cc6055ff20659a6479af1548`  
		Last Modified: Thu, 10 Mar 2022 22:42:44 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:c485fc87f90e75e6405dc43fcc37c2ade914702f8ed320b630861e35ccd420f3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2888375962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a30a1f214b7532e10adc147e08b39a03f124d3aa580118b82b5e517d5aa4dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 13:17:25 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Mar 2022 13:17:26 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Mar 2022 13:17:27 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Mar 2022 13:17:28 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Mar 2022 13:19:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:19:56 GMT
ENV GOPATH=C:\go
# Wed, 09 Mar 2022 13:20:52 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Mar 2022 13:35:10 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 09 Mar 2022 13:38:26 GMT
RUN $url = 'https://dl.google.com/go/go1.17.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '85ccf2608dca6ea9a46b6538c9e75e7cf2aebdf502379843b248e26b8bb110be'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:38:28 GMT
WORKDIR C:\go
# Wed, 09 Mar 2022 18:27:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:27:12 GMT
ENV XCADDY_VERSION=v0.2.0
# Wed, 09 Mar 2022 18:27:14 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:27:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 09 Mar 2022 18:28:10 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 09 Mar 2022 18:28:11 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7705bbffd7dc00934e935de0e00e09a7b0da55d66c596622f094495478dd71`  
		Last Modified: Wed, 09 Mar 2022 14:04:13 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be7ff0bb187d149a5cf3c76e1ec444d0e07c6606f67b2c921c67ec91829ea03`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876223f25b257577440a80fdee021b43c33ce3c56be9a20b2ddeaede95240522`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991eea244b9c3a1849c84748425dd9e9fbf9ec359ad9329796131b929239ffa4`  
		Last Modified: Wed, 09 Mar 2022 14:04:11 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b4c7c9740eb99bf626b312aa69396db3d186c5bd0e092b01c078ca7248e386`  
		Last Modified: Wed, 09 Mar 2022 14:04:40 GMT  
		Size: 25.5 MB (25454695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f6c8a4d4848c21636a48a69a569a5372ec4890ea029f1f620dda76078bdcef`  
		Last Modified: Wed, 09 Mar 2022 14:04:09 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ac6d527939082add6d21652ba4888acc5a6e7607365168d8e61fb1485339cb`  
		Last Modified: Wed, 09 Mar 2022 14:04:10 GMT  
		Size: 313.6 KB (313592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37aeceb8c2e5bb3c500129bcf20c3f8aea8c68c353e6714a63a225ed1546e8a1`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d88cd595dc7580d72420b7288c52d4b32201045a13dda1a7b943d9a3468adef`  
		Last Modified: Wed, 09 Mar 2022 14:13:05 GMT  
		Size: 145.5 MB (145488847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be492983ee2b2c9128ce0c732c441ae5fbd203cdb71c94faa253c24b01750c90`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa7b09ca61eb1fbafacee427b430b0879ad4da23e62e430a3fe6a66f181f642`  
		Last Modified: Wed, 09 Mar 2022 18:30:00 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468156ad0978bb8919deb642986d1eb42a6e00ea9c3294930a526771ff120f59`  
		Last Modified: Wed, 09 Mar 2022 18:29:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13b17cf7c5867462fbdd3605d90437e19301e9a4d3d41cf90d2c1561c689c50`  
		Last Modified: Wed, 09 Mar 2022 18:29:58 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a1eca5bdf4cf75e747993b512d64c980670337f17807b0daeac5ec4bb41d26`  
		Last Modified: Wed, 09 Mar 2022 18:29:58 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8171f34c3c578dc87b1d9cc5911249fb1f03964352906509faf9492d07cca7c0`  
		Last Modified: Wed, 09 Mar 2022 18:29:58 GMT  
		Size: 1.6 MB (1647844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8937298adab332653decbee0cd826d99541996c5098544285d35579c47c367a`  
		Last Modified: Wed, 09 Mar 2022 18:29:58 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - windows version 10.0.14393.4886; amd64

```console
$ docker pull caddy@sha256:22cae5265f5cb60aa10f7a056b9281b4e61d0e14f16b5454f5b90f8c14e10e6f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6455446654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4079b70701d5a0ca0af10a7038d5f468c00e36871a95feb8e6e4926bda5e7d00`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 06 Jan 2022 14:33:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Jan 2022 19:14:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Jan 2022 23:34:03 GMT
ENV GIT_VERSION=2.23.0
# Tue, 11 Jan 2022 23:34:05 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 11 Jan 2022 23:34:06 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 11 Jan 2022 23:34:07 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 11 Jan 2022 23:35:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 11 Jan 2022 23:35:42 GMT
ENV GOPATH=C:\go
# Tue, 11 Jan 2022 23:36:45 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Jan 2022 23:57:30 GMT
ENV GOLANG_VERSION=1.17.6
# Wed, 12 Jan 2022 00:01:53 GMT
RUN $url = 'https://dl.google.com/go/go1.17.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '5bf8f87aec7edfc08e6bc845f1c30dba6de32b863f89ae46553ff4bbcc1d4954'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 12 Jan 2022 00:01:55 GMT
WORKDIR C:\go
# Wed, 12 Jan 2022 06:32:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jan 2022 06:32:49 GMT
ENV XCADDY_VERSION=v0.2.0
# Wed, 12 Jan 2022 06:32:50 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 12 Jan 2022 06:32:51 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 12 Jan 2022 06:33:57 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 12 Jan 2022 06:33:58 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8428508ffd63b4af1ba690ec41e82a116f10ec6c3fb70962348f5448d42e5835`  
		Size: 2.2 GB (2208216859 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9b5116c05ddf6ecb5a348f7628e3f3264afbb9909d86798316dbaff4a0e991a2`  
		Last Modified: Tue, 11 Jan 2022 19:35:13 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2caa59a1aaa1c092020bbca2ed4bb1396365f4d9d04ddbbd111ee689414c97a`  
		Last Modified: Wed, 12 Jan 2022 00:35:16 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9fe19533bf1afd7f80fd9cf407f00011eff59836d40dcceb1896e75ea99bf5`  
		Last Modified: Wed, 12 Jan 2022 00:35:13 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40700bafb918466fc1727b2e59ec5eb21d347affb09989cc72ac6db12220b882`  
		Last Modified: Wed, 12 Jan 2022 00:35:12 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3180faaeb4219e7d41bb57faeebe12d142e8e246bac5ab81c8ef38499116de13`  
		Last Modified: Wed, 12 Jan 2022 00:35:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6189cfcbd5a7447e171b486da44213e8ff4721ecbf15998668c0b32e6fb06aaa`  
		Last Modified: Wed, 12 Jan 2022 00:35:18 GMT  
		Size: 25.4 MB (25440280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4766ed70813b67e83228fa314c288fe9a1998bb85cbbd29f2a4b0518e49a7c15`  
		Last Modified: Wed, 12 Jan 2022 00:35:09 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8f2e04b601edd119e847cbb2468052ab4681cd44bf4e9bbdf9b6c3f792d0ae`  
		Last Modified: Wed, 12 Jan 2022 00:35:09 GMT  
		Size: 306.6 KB (306585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef103850c637e1ce1f8d175e0c4b5c7d6c2a3a29d2b8ad15bed8eab49be3dde0`  
		Last Modified: Wed, 12 Jan 2022 00:39:29 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce1f406ac407910a0724e1fbad6ed8772a277ce69316a98a2defcebb5320504`  
		Last Modified: Wed, 12 Jan 2022 00:40:03 GMT  
		Size: 149.8 MB (149846909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdefe1352ad86026fe87510dd97f9a9acdbb5a700fc6a8aea2bd6eaa3194bd6`  
		Last Modified: Wed, 12 Jan 2022 00:39:28 GMT  
		Size: 1.6 KB (1562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1578c0afb3c1729e44264a61a125be686ed8e738b033a03917b80f62aea0ed46`  
		Last Modified: Wed, 12 Jan 2022 06:35:55 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0d89ba8c66caec659fce7ea59e230983c2e8129e3026228cce6945904233cf`  
		Last Modified: Wed, 12 Jan 2022 06:35:53 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e135d2e9e9a157d6d87f8f0e5e9cf6aef249cd9aac5e2b4313784e2d31664990`  
		Last Modified: Wed, 12 Jan 2022 06:35:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715ab69f5d21664707eee604a40f003fbd665f65c14431d564a82a614b277496`  
		Last Modified: Wed, 12 Jan 2022 06:35:53 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833db9ca0e9e1914a35515e476460cdd0bcc36174f85c13dd8646945c5199cde`  
		Last Modified: Wed, 12 Jan 2022 06:35:53 GMT  
		Size: 1.6 MB (1631613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c57f5273b431c8d65b59b81e63af176c5126e1b0d33f4d7b4ece422a1e01562`  
		Last Modified: Wed, 12 Jan 2022 06:35:53 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.6-builder-alpine`

```console
$ docker pull caddy@sha256:81586ffc8035d6323a8f32f47db99a14c976beeeaba313cee4b752d63944db5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.4.6-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:9c6a77c878ea39bd367c8c7e73f1a75a6ce97101bef0f3de7e288934b4de519e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121354364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c3a82ad51f9b44b272a32de82576c64480a940db9877dd465101c921e11593`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:21:45 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 04:21:46 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 04:21:47 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 01:05:33 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 01:08:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 01:08:13 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 01:08:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 01:08:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 01:08:14 GMT
WORKDIR /go
# Fri, 04 Mar 2022 04:22:25 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 04 Mar 2022 04:22:25 GMT
ENV XCADDY_VERSION=v0.2.0
# Fri, 04 Mar 2022 04:22:26 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 04 Mar 2022 04:22:26 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 04 Mar 2022 04:22:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 04 Mar 2022 04:22:27 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 04 Mar 2022 04:22:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666ba61612fd7c93393f9a5bc1751d8a9929e32d51501dba691da9e8232bc87b`  
		Last Modified: Tue, 30 Nov 2021 04:36:04 GMT  
		Size: 282.2 KB (282159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed8ca4862056a130f714accb3538decfa0663fec84e635d8b5a0a3305353dee`  
		Last Modified: Tue, 30 Nov 2021 04:36:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141c1ce2f203145a20c1b4550c662f943266dc7dbf7e15ee911b06456e2326da`  
		Last Modified: Fri, 04 Mar 2022 01:21:28 GMT  
		Size: 110.2 MB (110186591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4c7319106ffbcda864c88220ef7a19e3da3b571fa08e0be968efe7fbd9465f`  
		Last Modified: Fri, 04 Mar 2022 01:21:14 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0f327525fd9ac01a04ccd2c1530800b0c51b68d8821a2904e3d066d8663b3f`  
		Last Modified: Fri, 04 Mar 2022 04:22:46 GMT  
		Size: 6.8 MB (6821521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd85b87242bfb046d67955057b47bfdc6f774636e6b8334022ed51fe020a6301`  
		Last Modified: Fri, 04 Mar 2022 04:22:45 GMT  
		Size: 1.2 MB (1244966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32b29093c0b4e0e55e5212230f0fda6566f59ae3e6f91d6ae6b39363b0e7860`  
		Last Modified: Fri, 04 Mar 2022 04:22:45 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:f7e1a9b85365f550da1a0a03bbc6f0dc1c5930d86fcb7e857919ed50708462d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115838871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71a25849e386c048c58fcafd1884613238beacc8243d9fcdddddddbd10b458a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 02:32:18 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 02:32:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 02:32:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 22:50:05 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 03 Mar 2022 22:53:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 03 Mar 2022 22:53:52 GMT
ENV GOPATH=/go
# Thu, 03 Mar 2022 22:53:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 22:53:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 03 Mar 2022 22:53:54 GMT
WORKDIR /go
# Thu, 03 Mar 2022 23:28:42 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:49:51 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:49:52 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 22:49:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:49:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:49:55 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:49:55 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228ad0256439cce3fe9db355991b0557f55241d8cca8690f4f741e1c2d8fb8b9`  
		Last Modified: Tue, 30 Nov 2021 02:47:28 GMT  
		Size: 282.1 KB (282105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cab2a064767512d7d354e806cbd8b24ffefc15e06eeb7d4b127e7f6cddb6b40`  
		Last Modified: Tue, 30 Nov 2021 02:47:28 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798ddefed71bfdadb9d2b02c26fb7579e437fcf60f8af3f7cefed7967580d7da`  
		Last Modified: Thu, 03 Mar 2022 23:08:07 GMT  
		Size: 105.1 MB (105068635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7451a2cdc06b1d637a7e3849503cd56318bc1eb291dc792a6294cec777a31980`  
		Last Modified: Thu, 03 Mar 2022 23:06:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3489c6c0bcd6d649e4760550c8033a06b697ff4490644c130dde6501db25ab26`  
		Last Modified: Thu, 03 Mar 2022 23:29:55 GMT  
		Size: 6.7 MB (6677482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6889976625624adb9a9c5b111609959fe4da102919177fa9c53a23d173175d6`  
		Last Modified: Thu, 10 Mar 2022 22:51:59 GMT  
		Size: 1.2 MB (1178508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79172ebfda03823b62d347d32a6755fe56f0f8809466f11895c5a7d7ae48c3b0`  
		Last Modified: Thu, 10 Mar 2022 22:51:58 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:06e29bc1ce4d22e988eca705e6e4faf2ec70661ffb2a448a334e8b557068dd68
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114698943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14dc63acb649973c1c8c9f6f76def65c297a511f53a12f94af418ebc1c8da64e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:10:37 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 04:10:39 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 04:10:39 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:51:53 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 00:55:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 00:55:09 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 00:55:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:55:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 00:55:12 GMT
WORKDIR /go
# Fri, 04 Mar 2022 06:45:24 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:57:52 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:57:53 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 22:57:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:57:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:57:56 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:57:56 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f21e2af73375430a6481f93a61f3df4f9de38c985f83b27293f8aace16d6b5`  
		Last Modified: Tue, 30 Nov 2021 04:33:33 GMT  
		Size: 281.2 KB (281248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cec97f9b59f8579851b3f2c1523c8a96065c591f5961858420e92bf9d424d2`  
		Last Modified: Tue, 30 Nov 2021 04:33:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edfb2fbd38ed3972211201867b2a8e18c8dc23b141d716828e9914c61276ecd`  
		Last Modified: Fri, 04 Mar 2022 01:19:22 GMT  
		Size: 104.9 MB (104853230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a4329e8253fda916ae04b5a3c4d217f5f24639ce303c8a3f2b24588f490196`  
		Last Modified: Fri, 04 Mar 2022 01:18:12 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c608e2c7ee3c9ef36153815e881ac6bc5cf7ff68862fcddf588d11054f20923`  
		Last Modified: Fri, 04 Mar 2022 06:46:39 GMT  
		Size: 6.0 MB (5952263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca89b858a1ebd99c4675cae20c8f5c5e60653a6d2a307ec0bcd6e2e3b448d087`  
		Last Modified: Thu, 10 Mar 2022 23:00:00 GMT  
		Size: 1.2 MB (1176718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9c6a4e7cfb70b12bfb81a4fced64fb3d181017de696421ab4178c208f5defa`  
		Last Modified: Thu, 10 Mar 2022 22:59:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:ee6d440f72726b2d9d29a604a97ab0cc23505e8eccc68c64133eba5da0ef12de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115495270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9fe816e095b9092b887d34923435e91de44876c56fc189162c309a48f541ca`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 01:54:59 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 01:55:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 01:55:01 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 02:29:42 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 02:31:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 02:31:06 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 02:31:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 02:31:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 02:31:09 GMT
WORKDIR /go
# Fri, 04 Mar 2022 03:10:53 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:39:34 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:39:34 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 22:39:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:39:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:39:38 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:39:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a89e8eeedd549875510e5e4e14010906a58878526814e6df25d14009856c6ff`  
		Last Modified: Tue, 30 Nov 2021 02:05:10 GMT  
		Size: 281.9 KB (281899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94645a83ff95687e6f078c140cfcac8def006923ed4019ef74fa189e6d9f0b14`  
		Last Modified: Tue, 30 Nov 2021 02:05:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caad3c9267df5b5261016d2d8843a47ffd88678a81f5e2363c426640adaf2029`  
		Last Modified: Fri, 04 Mar 2022 02:41:55 GMT  
		Size: 104.4 MB (104422515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e36f09527def3bbe5253cea2be9051532cf4a71f0df8fec8a85c922ce640c36`  
		Last Modified: Fri, 04 Mar 2022 02:41:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336ffb45c2b4e74ba78ba96c6f82f7fec126618bbacdc0fa27c7d3677b5aa6f1`  
		Last Modified: Fri, 04 Mar 2022 03:11:32 GMT  
		Size: 6.9 MB (6926057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acd88183c62587770b090ffe6a970e05212ee61f949af7bad8e6edcb5743f0a`  
		Last Modified: Thu, 10 Mar 2022 22:40:54 GMT  
		Size: 1.1 MB (1148678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb0f9bf906b045657c360d551af06aa0af8bee7cbeb2e646cafa48abc2ac878`  
		Last Modified: Thu, 10 Mar 2022 22:40:54 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:4a53d3e10c18d0855f3ec5c9ec6dfb598f1a562d0828ec62b238370646e46e8a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114325817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251761ef86f00954d0b3d990c694bdcc74f14f6488585eef034148425fed6f23`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 03:17:54 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 03:17:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 03:18:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:12:42 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 00:15:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 00:15:47 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 00:15:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:15:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 00:15:58 GMT
WORKDIR /go
# Fri, 04 Mar 2022 07:20:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 04 Mar 2022 07:20:21 GMT
ENV XCADDY_VERSION=v0.2.0
# Fri, 04 Mar 2022 07:20:27 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 04 Mar 2022 07:20:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 04 Mar 2022 07:20:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 04 Mar 2022 07:20:51 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 04 Mar 2022 07:20:57 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28be42a6852cc2108ddba1e4252671ae20275780a6ff73b1038699f59da2ac20`  
		Last Modified: Tue, 30 Nov 2021 03:35:16 GMT  
		Size: 284.0 KB (284020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d744d6799a13f2f7a7f85e040ddf0cc8b671a7cc5572b7049c3e1da8139b349`  
		Last Modified: Tue, 30 Nov 2021 03:35:15 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3620d170b59e9b8337616ec72da9ade5c2471d3b0cf50e3a538e6171d5d813a4`  
		Last Modified: Fri, 04 Mar 2022 00:33:32 GMT  
		Size: 102.8 MB (102785250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bec6e3bcdb44b28a2f07f58bc175553abc87d573010ff47564a72aff7749eb5`  
		Last Modified: Fri, 04 Mar 2022 00:33:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75230c4358c070669508567379db20aa0f6acf5775eb391f81394cc567994d4`  
		Last Modified: Fri, 04 Mar 2022 07:21:55 GMT  
		Size: 7.3 MB (7321033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29c6375e4c4e1312ebfadd212ce4b17f7f002743d73d01fca882a24eba618ac`  
		Last Modified: Fri, 04 Mar 2022 07:21:54 GMT  
		Size: 1.1 MB (1120019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47ae1c41cc141d20ffc3fe6ecccea9ac5fb48eefdeab0dec835beb21c731ac4`  
		Last Modified: Fri, 04 Mar 2022 07:21:54 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:43996cf55b905a5c54ef7cc5f9192ec4077d75694985c130d4866c3c9a537109
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118763072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad0782969bd455fc3ed6f62197dd5e0686ae55f02024605d501e975ceaf4c99`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:07:57 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 04:07:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 04:07:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 23:09:57 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 03 Mar 2022 23:12:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 03 Mar 2022 23:12:29 GMT
ENV GOPATH=/go
# Thu, 03 Mar 2022 23:12:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 23:12:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 03 Mar 2022 23:12:29 GMT
WORKDIR /go
# Fri, 04 Mar 2022 00:05:09 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:41:34 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:41:35 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 22:41:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:41:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:41:36 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:41:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66787da5af638f8523e4694d81d38c2ca7c0a262f4cb8d78c46f7d64833bbaa0`  
		Last Modified: Tue, 30 Nov 2021 04:17:43 GMT  
		Size: 282.4 KB (282378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406f41068af489d7950f1a75d72455e702ed7da98dad21d9267448257b6a2ddc`  
		Last Modified: Tue, 30 Nov 2021 04:17:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee9a2e8145f1c142e4295add6c8c87e35418763276db9058b5b7ed0cc175e80`  
		Last Modified: Thu, 03 Mar 2022 23:26:10 GMT  
		Size: 107.7 MB (107739292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1f97ab22dac5e8b60c0770634135f40d0eba00b3f8a5bd5de06c0b1f34676d`  
		Last Modified: Thu, 03 Mar 2022 23:25:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5bcd397c1a177db9a5bf9729e85c6d9a4a1a63fe402e4e054b80d981f46080`  
		Last Modified: Fri, 04 Mar 2022 00:05:47 GMT  
		Size: 6.9 MB (6930956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d87e4b5eaf820e1c3e543e167ee9e5db5c696e7841ea413858457b48b15e52c`  
		Last Modified: Thu, 10 Mar 2022 22:42:44 GMT  
		Size: 1.2 MB (1203783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16912306174cfd07dbe9e0cf2ce772627716514cc6055ff20659a6479af1548`  
		Last Modified: Thu, 10 Mar 2022 22:42:44 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.6-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:a4ace300fa0bb8e20564cf55f2e5b24c38f86b8cb8c1f57a3c64f014a6243d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `caddy:2.4.6-builder-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:c485fc87f90e75e6405dc43fcc37c2ade914702f8ed320b630861e35ccd420f3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2888375962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a30a1f214b7532e10adc147e08b39a03f124d3aa580118b82b5e517d5aa4dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 13:17:25 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Mar 2022 13:17:26 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Mar 2022 13:17:27 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Mar 2022 13:17:28 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Mar 2022 13:19:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:19:56 GMT
ENV GOPATH=C:\go
# Wed, 09 Mar 2022 13:20:52 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Mar 2022 13:35:10 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 09 Mar 2022 13:38:26 GMT
RUN $url = 'https://dl.google.com/go/go1.17.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '85ccf2608dca6ea9a46b6538c9e75e7cf2aebdf502379843b248e26b8bb110be'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:38:28 GMT
WORKDIR C:\go
# Wed, 09 Mar 2022 18:27:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:27:12 GMT
ENV XCADDY_VERSION=v0.2.0
# Wed, 09 Mar 2022 18:27:14 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:27:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 09 Mar 2022 18:28:10 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 09 Mar 2022 18:28:11 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7705bbffd7dc00934e935de0e00e09a7b0da55d66c596622f094495478dd71`  
		Last Modified: Wed, 09 Mar 2022 14:04:13 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be7ff0bb187d149a5cf3c76e1ec444d0e07c6606f67b2c921c67ec91829ea03`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876223f25b257577440a80fdee021b43c33ce3c56be9a20b2ddeaede95240522`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991eea244b9c3a1849c84748425dd9e9fbf9ec359ad9329796131b929239ffa4`  
		Last Modified: Wed, 09 Mar 2022 14:04:11 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b4c7c9740eb99bf626b312aa69396db3d186c5bd0e092b01c078ca7248e386`  
		Last Modified: Wed, 09 Mar 2022 14:04:40 GMT  
		Size: 25.5 MB (25454695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f6c8a4d4848c21636a48a69a569a5372ec4890ea029f1f620dda76078bdcef`  
		Last Modified: Wed, 09 Mar 2022 14:04:09 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ac6d527939082add6d21652ba4888acc5a6e7607365168d8e61fb1485339cb`  
		Last Modified: Wed, 09 Mar 2022 14:04:10 GMT  
		Size: 313.6 KB (313592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37aeceb8c2e5bb3c500129bcf20c3f8aea8c68c353e6714a63a225ed1546e8a1`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d88cd595dc7580d72420b7288c52d4b32201045a13dda1a7b943d9a3468adef`  
		Last Modified: Wed, 09 Mar 2022 14:13:05 GMT  
		Size: 145.5 MB (145488847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be492983ee2b2c9128ce0c732c441ae5fbd203cdb71c94faa253c24b01750c90`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa7b09ca61eb1fbafacee427b430b0879ad4da23e62e430a3fe6a66f181f642`  
		Last Modified: Wed, 09 Mar 2022 18:30:00 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468156ad0978bb8919deb642986d1eb42a6e00ea9c3294930a526771ff120f59`  
		Last Modified: Wed, 09 Mar 2022 18:29:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13b17cf7c5867462fbdd3605d90437e19301e9a4d3d41cf90d2c1561c689c50`  
		Last Modified: Wed, 09 Mar 2022 18:29:58 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a1eca5bdf4cf75e747993b512d64c980670337f17807b0daeac5ec4bb41d26`  
		Last Modified: Wed, 09 Mar 2022 18:29:58 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8171f34c3c578dc87b1d9cc5911249fb1f03964352906509faf9492d07cca7c0`  
		Last Modified: Wed, 09 Mar 2022 18:29:58 GMT  
		Size: 1.6 MB (1647844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8937298adab332653decbee0cd826d99541996c5098544285d35579c47c367a`  
		Last Modified: Wed, 09 Mar 2022 18:29:58 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.6-windowsservercore`

```console
$ docker pull caddy@sha256:5f89b604764eb0c53217da81ffe958b02f108847507c400542ef623d0c3acb06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2686; amd64
	-	windows version 10.0.14393.5006; amd64

### `caddy:2.4.6-windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:f2de2d90885f8cb6d12c79d914e354b41f6bfebc22ba3390096ae69fac380cf5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2728251838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8705f493a3ce58fda2b9ada4d3d27639c9f13835f1fb8d85ecdf795e69dae46a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:20:26 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:20:27 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:21:52 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:21:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:21:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:21:55 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:21:56 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:21:57 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:21:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:21:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:22:00 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:22:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:22:02 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:22:05 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:22:06 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:22:07 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:23:12 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:23:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99d892d6329e540cd98b358cc2f8085a7e6579538de9b4afa3ce0d11a03116`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 365.4 KB (365439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fb2be6c676c8f3e743cd43ec6b238646cf9f8b89a6fb1bde29f9bb52a7296c`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9b968486191ed8bb4a6c85eb678e32bbb062d8998e636e7706431be6e25f51`  
		Last Modified: Wed, 09 Mar 2022 18:29:07 GMT  
		Size: 12.1 MB (12115400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63f0ecb87a49981ac55c8495d8beed3b58d3b15e31ff4ba1140b0176e551265`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5249439459c9b885575d1a0c5c0df8c3e99649414b3c09ef4054e22fab54b584`  
		Last Modified: Wed, 09 Mar 2022 18:29:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69ab39aec279710b6bf7b4581cafe49878e70beff74d4a5e342eea02e60ce60`  
		Last Modified: Wed, 09 Mar 2022 18:29:02 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb81ca26c7a917813faca1d4cb92e1f41e642701d1199c9811ae8f9294e5b6f`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f5adb02b69cdd17e3acff1b0ea61317020c331399b0cb57fa34da5c09956e3`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e95a1158bc8e4066b6eb4211e7e898c86431c53c76c4752dfd7ce0a15cfc48`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579759f42b06baed2eb773c9cf8d6709e48e71afc07751fb3d45f7e4df9d819a`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e477dc674aa75d9872e80416c27f642531913f63b1598f0920a821c8b6cb535c`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03c9bb84aaf51c973e2ae3990a6b45ac835195b5eaae35799354b2aee8dfc2e`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23add58da280a0f09c755eaccccd5ecc95dc65993558d933f499b4c3378c9f70`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e3da14e3fcc65b938eef87893e57b0daa81c012c8789265cd784fb2f3cfcf7`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34cb18e7475b74cb46643f516f65cbd77fa161c461d753b4e62e076f7b221e5`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbd804e2eb98213ed819900a23753f3f2d662eb72c30a86dbbb51bcecc3cebc`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49b05954d4ea193b3f85228739d529bbc2a811204d8b6e22440c97977addbdf`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a3a3abbfe3563eaed35b97ad1ed309a3f4e744f968d0b6f6deaf68211f2fc8`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53542589ba9c33b651da4be35de7384a168d4936d08bb046a632a4d644b46c9e`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 293.3 KB (293252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149ac7945e26171c6dfe9e316c21027eb072f4fd72819f8b80a32eada8275ae2`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-windowsservercore` - windows version 10.0.14393.5006; amd64

```console
$ docker pull caddy@sha256:7f8374457a1c63677174631c3a8ea273702e069b924b615f44292250b7e2d8c1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6289879706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba40202b27c7479ec2d1d1618860745715dbfcabf489c651e5f04e826c286f72`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sat, 05 Mar 2022 03:39:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Mar 2022 18:23:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:24:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:24:49 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:26:02 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:26:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:26:04 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:26:05 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:26:06 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:26:07 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:26:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:26:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:26:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:26:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:26:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:26:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:26:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:26:14 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:26:15 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:26:16 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:26:54 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:26:55 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0fe465a8df276d07bd592c9424c00276a476fb7f74be6f867256b07fba31212d`  
		Size: 2.2 GB (2207094901 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c66997424475af0399fffec7897bad20e40b8309c56761077b30f5d9495f4db3`  
		Last Modified: Wed, 09 Mar 2022 18:29:32 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31f3b05b8f63dd42b4881a4c3d384691cc281678a86e0836d0c32819a344b5d`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 345.5 KB (345470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9855b50f056bb89da3373dfb2c128c8cf2515840c723a9027f0c01bb0eb91d`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b715cda286f032f4b113aefacf8b42874e8bed4dbe0080772b9d6cc1e91fc4`  
		Last Modified: Wed, 09 Mar 2022 18:29:43 GMT  
		Size: 12.1 MB (12134708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e40c1797eb55c98999e616bff73129a77843c7cf7667787950662180cbd90b`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d12359d4309d649fc7f0131974324ede0eb7aa11d1cd6f5d47000f9e14363b`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1783134869b6be42026ea8457c2f07dcacd3e029eaa283e48e798ce94929111`  
		Last Modified: Wed, 09 Mar 2022 18:29:28 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7104f8aa42fca009aaea2d885dfc7a0ea9acd8b7670cd9a90929f355d29cb5bf`  
		Last Modified: Wed, 09 Mar 2022 18:29:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ee03e2f86a2587a31a03418808435e9804fd324f95c981776b71ac5541f122`  
		Last Modified: Wed, 09 Mar 2022 18:29:28 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617c8eb23f7d35a0012ac7a3ce817bb49edda99eb16da9e4a9e6897617ded26d`  
		Last Modified: Wed, 09 Mar 2022 18:29:27 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85694b0569ffdf58e2f716205756d0a9eab45456d0ef23c2bbc8cb5816b99c1a`  
		Last Modified: Wed, 09 Mar 2022 18:29:27 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe2abbbf56f3d370ddba372e974d4765e074ee94fa8b1e4037b1cbf9d4a1e04`  
		Last Modified: Wed, 09 Mar 2022 18:29:26 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d4deaae43ac0785c4ccfb22ba187f33035f3041d44d770e8864cab157c1fe8`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7c04adc036f7a25c1c5a61895ba945aac263098d741203cb43e6b3b32174ef`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582d555a149be3d9ce42e33942b905cc2c8b9ebdc0dd1de51709fd7276c1e3ae`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b57929590127351973d44b26f950891ee7b918dc352a68098193a5d4fce629`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71478b5420cbbbea1bb0a6e617445f903203fac8965dfc6e2c41932cbb7f2acb`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b709c8c0d2fb364fd66993072fd79d4d28cda233a5d991b74680a1f80b1563`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c82093ad8180c0667cf71cdf92b8ead740771d5f2f5efda695fc67b815056d9`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34076b974bce5f92149f3e2eb58dc898a74d7ca4c563c20c4308f51a3f25212`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 293.4 KB (293417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e27086943ac64711a35c0e493db7b82a4faa0d65d5e80a91104238aba4845e2`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.6-windowsservercore-1809`

```console
$ docker pull caddy@sha256:a3ba1d80239cc342421e0b3a6a6adba859191852e94c30047402f2ac1cc24407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `caddy:2.4.6-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:f2de2d90885f8cb6d12c79d914e354b41f6bfebc22ba3390096ae69fac380cf5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2728251838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8705f493a3ce58fda2b9ada4d3d27639c9f13835f1fb8d85ecdf795e69dae46a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:20:26 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:20:27 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:21:52 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:21:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:21:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:21:55 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:21:56 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:21:57 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:21:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:21:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:22:00 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:22:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:22:02 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:22:05 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:22:06 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:22:07 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:23:12 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:23:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99d892d6329e540cd98b358cc2f8085a7e6579538de9b4afa3ce0d11a03116`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 365.4 KB (365439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fb2be6c676c8f3e743cd43ec6b238646cf9f8b89a6fb1bde29f9bb52a7296c`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9b968486191ed8bb4a6c85eb678e32bbb062d8998e636e7706431be6e25f51`  
		Last Modified: Wed, 09 Mar 2022 18:29:07 GMT  
		Size: 12.1 MB (12115400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63f0ecb87a49981ac55c8495d8beed3b58d3b15e31ff4ba1140b0176e551265`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5249439459c9b885575d1a0c5c0df8c3e99649414b3c09ef4054e22fab54b584`  
		Last Modified: Wed, 09 Mar 2022 18:29:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69ab39aec279710b6bf7b4581cafe49878e70beff74d4a5e342eea02e60ce60`  
		Last Modified: Wed, 09 Mar 2022 18:29:02 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb81ca26c7a917813faca1d4cb92e1f41e642701d1199c9811ae8f9294e5b6f`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f5adb02b69cdd17e3acff1b0ea61317020c331399b0cb57fa34da5c09956e3`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e95a1158bc8e4066b6eb4211e7e898c86431c53c76c4752dfd7ce0a15cfc48`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579759f42b06baed2eb773c9cf8d6709e48e71afc07751fb3d45f7e4df9d819a`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e477dc674aa75d9872e80416c27f642531913f63b1598f0920a821c8b6cb535c`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03c9bb84aaf51c973e2ae3990a6b45ac835195b5eaae35799354b2aee8dfc2e`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23add58da280a0f09c755eaccccd5ecc95dc65993558d933f499b4c3378c9f70`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e3da14e3fcc65b938eef87893e57b0daa81c012c8789265cd784fb2f3cfcf7`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34cb18e7475b74cb46643f516f65cbd77fa161c461d753b4e62e076f7b221e5`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbd804e2eb98213ed819900a23753f3f2d662eb72c30a86dbbb51bcecc3cebc`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49b05954d4ea193b3f85228739d529bbc2a811204d8b6e22440c97977addbdf`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a3a3abbfe3563eaed35b97ad1ed309a3f4e744f968d0b6f6deaf68211f2fc8`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53542589ba9c33b651da4be35de7384a168d4936d08bb046a632a4d644b46c9e`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 293.3 KB (293252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149ac7945e26171c6dfe9e316c21027eb072f4fd72819f8b80a32eada8275ae2`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.5.0-beta.1`

```console
$ docker pull caddy@sha256:dd171832461cbe38b2f56f6cf4488f3d5fde9e681caea8cdf0728a5f604a73b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `caddy:2.5.0-beta.1` - linux; arm variant v6

```console
$ docker pull caddy@sha256:e1d77af6df8603afa0cac8e0866667f468fdc3f72329fc4bac1a8e0c0cbfa20c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14460763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e16f161519650e469a1367ecdcbcedf8b9a375ec7f30a5f4858eaeb9779e8b7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Thu, 10 Mar 2022 22:50:13 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 10 Mar 2022 22:50:15 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 10 Mar 2022 22:50:16 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 22:50:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 10 Mar 2022 22:50:21 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Mar 2022 22:50:22 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 10 Mar 2022 22:50:22 GMT
ENV XDG_DATA_HOME=/data
# Thu, 10 Mar 2022 22:50:22 GMT
VOLUME [/config]
# Thu, 10 Mar 2022 22:50:23 GMT
VOLUME [/data]
# Thu, 10 Mar 2022 22:50:23 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Thu, 10 Mar 2022 22:50:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 10 Mar 2022 22:50:24 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 10 Mar 2022 22:50:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 10 Mar 2022 22:50:25 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 10 Mar 2022 22:50:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 10 Mar 2022 22:50:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 10 Mar 2022 22:50:26 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 10 Mar 2022 22:50:26 GMT
EXPOSE 80
# Thu, 10 Mar 2022 22:50:27 GMT
EXPOSE 443
# Thu, 10 Mar 2022 22:50:27 GMT
EXPOSE 2019
# Thu, 10 Mar 2022 22:50:28 GMT
WORKDIR /srv
# Thu, 10 Mar 2022 22:50:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d7f86a3b6a0e3f45d86cbcff0d121dc2b8a30dfcd1f4afe028b67f899742dd`  
		Last Modified: Thu, 10 Mar 2022 22:52:15 GMT  
		Size: 291.7 KB (291714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6754b852c421f207e13c88027a365911c2ce7547016cb5667ab0bd83afdd78db`  
		Last Modified: Thu, 10 Mar 2022 22:52:14 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d50c21af6a09cd895f3174abc3124a07248dfd64c4a78020edd0a7a62b689f`  
		Last Modified: Thu, 10 Mar 2022 22:52:22 GMT  
		Size: 11.5 MB (11531644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b56fb8ece7173ff3f78204b7d316c8d0e91ff5797c2f128ea3719532755566b`  
		Last Modified: Thu, 10 Mar 2022 22:52:14 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1` - linux; arm variant v7

```console
$ docker pull caddy@sha256:1bd12a832c8b9ef90b31c2037e4cc2bba48a1b2ff8f722993bb0a51359dcec88
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14243415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5193f0213996802c5ecf621611c41ca486634776b62c490f6ce3a63f8c459d5d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Thu, 10 Mar 2022 22:58:14 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 10 Mar 2022 22:58:17 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 10 Mar 2022 22:58:17 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 22:58:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 10 Mar 2022 22:58:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Mar 2022 22:58:23 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 10 Mar 2022 22:58:23 GMT
ENV XDG_DATA_HOME=/data
# Thu, 10 Mar 2022 22:58:24 GMT
VOLUME [/config]
# Thu, 10 Mar 2022 22:58:24 GMT
VOLUME [/data]
# Thu, 10 Mar 2022 22:58:24 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Thu, 10 Mar 2022 22:58:25 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 10 Mar 2022 22:58:25 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 10 Mar 2022 22:58:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 10 Mar 2022 22:58:26 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 10 Mar 2022 22:58:26 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 10 Mar 2022 22:58:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 10 Mar 2022 22:58:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 10 Mar 2022 22:58:28 GMT
EXPOSE 80
# Thu, 10 Mar 2022 22:58:28 GMT
EXPOSE 443
# Thu, 10 Mar 2022 22:58:29 GMT
EXPOSE 2019
# Thu, 10 Mar 2022 22:58:29 GMT
WORKDIR /srv
# Thu, 10 Mar 2022 22:58:29 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b7983ef4055364abada1e9d90961200fa12a940e65618e3deae6d94ef1de00`  
		Last Modified: Thu, 10 Mar 2022 23:00:17 GMT  
		Size: 290.7 KB (290698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683efd57d03b0caa68cb8294af9eacbd8a767d0bf033826ef6cb630d49e7746f`  
		Last Modified: Thu, 10 Mar 2022 23:00:17 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d266cd1399712df50a883c327a923a84535e481bd04e192cd2242e630eb35761`  
		Last Modified: Thu, 10 Mar 2022 23:00:24 GMT  
		Size: 11.5 MB (11511970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d21aebeed4d46b8af4d3498e63ea84a09fc0a8baca111e15eddb8223c4468d1`  
		Last Modified: Thu, 10 Mar 2022 23:00:17 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:926a4905f150b0c5f0e3af4a0fb8499c250040fd76d6a10b0caba77cedda4906
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14150649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd6a34ea54b24370b92bc5e69ed5e8883b415c07b33a5fb0411af6fda6cc448`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Thu, 10 Mar 2022 22:39:46 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 10 Mar 2022 22:39:48 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 10 Mar 2022 22:39:49 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 22:39:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 10 Mar 2022 22:39:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Mar 2022 22:39:53 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 10 Mar 2022 22:39:54 GMT
ENV XDG_DATA_HOME=/data
# Thu, 10 Mar 2022 22:39:55 GMT
VOLUME [/config]
# Thu, 10 Mar 2022 22:39:56 GMT
VOLUME [/data]
# Thu, 10 Mar 2022 22:39:57 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Thu, 10 Mar 2022 22:39:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 10 Mar 2022 22:39:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 10 Mar 2022 22:40:00 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 10 Mar 2022 22:40:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 10 Mar 2022 22:40:02 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 10 Mar 2022 22:40:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 10 Mar 2022 22:40:04 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 10 Mar 2022 22:40:05 GMT
EXPOSE 80
# Thu, 10 Mar 2022 22:40:06 GMT
EXPOSE 443
# Thu, 10 Mar 2022 22:40:07 GMT
EXPOSE 2019
# Thu, 10 Mar 2022 22:40:08 GMT
WORKDIR /srv
# Thu, 10 Mar 2022 22:40:09 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341f5c6df96a51fba8688cf172735f506dc6d217d6980a726e379207bd340479`  
		Last Modified: Thu, 10 Mar 2022 22:41:08 GMT  
		Size: 291.3 KB (291312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7dd361c9a8eddc2de6308df834d1c0ead713a2002cc63e09c1db3289cea6e8`  
		Last Modified: Thu, 10 Mar 2022 22:41:08 GMT  
		Size: 5.8 KB (5752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bb8aa7a1559d414d7419eb9f3d4de311531be8c728dedf757673582c478e68`  
		Last Modified: Thu, 10 Mar 2022 22:41:10 GMT  
		Size: 11.1 MB (11137998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5140397d04adfeb03f93bc807ef0be5f81c06dab593417424fbc4387b123f3a5`  
		Last Modified: Thu, 10 Mar 2022 22:41:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1` - linux; s390x

```console
$ docker pull caddy@sha256:a31b274a2eee69b3f4e035f8e298cd136f84943d7262c12613e6d6b8694c9e8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14633245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb2815c3839014e86a19f7c9ca632f8da1125e05b51de29ab5e64caddeccf58`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Thu, 10 Mar 2022 22:41:46 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 10 Mar 2022 22:41:48 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 10 Mar 2022 22:41:48 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 22:41:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 10 Mar 2022 22:41:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Mar 2022 22:41:51 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 10 Mar 2022 22:41:51 GMT
ENV XDG_DATA_HOME=/data
# Thu, 10 Mar 2022 22:41:52 GMT
VOLUME [/config]
# Thu, 10 Mar 2022 22:41:52 GMT
VOLUME [/data]
# Thu, 10 Mar 2022 22:41:52 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Thu, 10 Mar 2022 22:41:52 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 10 Mar 2022 22:41:52 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 10 Mar 2022 22:41:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 10 Mar 2022 22:41:52 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 10 Mar 2022 22:41:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 10 Mar 2022 22:41:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 10 Mar 2022 22:41:53 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 10 Mar 2022 22:41:53 GMT
EXPOSE 80
# Thu, 10 Mar 2022 22:41:53 GMT
EXPOSE 443
# Thu, 10 Mar 2022 22:41:53 GMT
EXPOSE 2019
# Thu, 10 Mar 2022 22:41:53 GMT
WORKDIR /srv
# Thu, 10 Mar 2022 22:41:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c9c83e4654ae545552a5c4ce045b21c0ae08af0b51008766e99912f260a41b`  
		Last Modified: Thu, 10 Mar 2022 22:42:53 GMT  
		Size: 291.8 KB (291831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb10ce05d5a54c9e9e97db29c0f900617aa6c8ca42f6306895ed22a2d0b65954`  
		Last Modified: Thu, 10 Mar 2022 22:42:53 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b63897f7c6ba88d70c2f8a66b6b7c56f7e1ea6aeeb29447f43a6745b4f7b9a2`  
		Last Modified: Thu, 10 Mar 2022 22:42:55 GMT  
		Size: 11.7 MB (11729487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7485c28d0c46c85a0a7f50096c24d5fdf21e71f7a8037ad11d818f9c8a44dc`  
		Last Modified: Thu, 10 Mar 2022 22:42:53 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.5.0-beta.1-alpine`

```console
$ docker pull caddy@sha256:dd171832461cbe38b2f56f6cf4488f3d5fde9e681caea8cdf0728a5f604a73b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `caddy:2.5.0-beta.1-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:e1d77af6df8603afa0cac8e0866667f468fdc3f72329fc4bac1a8e0c0cbfa20c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14460763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e16f161519650e469a1367ecdcbcedf8b9a375ec7f30a5f4858eaeb9779e8b7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Thu, 10 Mar 2022 22:50:13 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 10 Mar 2022 22:50:15 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 10 Mar 2022 22:50:16 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 22:50:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 10 Mar 2022 22:50:21 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Mar 2022 22:50:22 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 10 Mar 2022 22:50:22 GMT
ENV XDG_DATA_HOME=/data
# Thu, 10 Mar 2022 22:50:22 GMT
VOLUME [/config]
# Thu, 10 Mar 2022 22:50:23 GMT
VOLUME [/data]
# Thu, 10 Mar 2022 22:50:23 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Thu, 10 Mar 2022 22:50:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 10 Mar 2022 22:50:24 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 10 Mar 2022 22:50:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 10 Mar 2022 22:50:25 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 10 Mar 2022 22:50:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 10 Mar 2022 22:50:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 10 Mar 2022 22:50:26 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 10 Mar 2022 22:50:26 GMT
EXPOSE 80
# Thu, 10 Mar 2022 22:50:27 GMT
EXPOSE 443
# Thu, 10 Mar 2022 22:50:27 GMT
EXPOSE 2019
# Thu, 10 Mar 2022 22:50:28 GMT
WORKDIR /srv
# Thu, 10 Mar 2022 22:50:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d7f86a3b6a0e3f45d86cbcff0d121dc2b8a30dfcd1f4afe028b67f899742dd`  
		Last Modified: Thu, 10 Mar 2022 22:52:15 GMT  
		Size: 291.7 KB (291714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6754b852c421f207e13c88027a365911c2ce7547016cb5667ab0bd83afdd78db`  
		Last Modified: Thu, 10 Mar 2022 22:52:14 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d50c21af6a09cd895f3174abc3124a07248dfd64c4a78020edd0a7a62b689f`  
		Last Modified: Thu, 10 Mar 2022 22:52:22 GMT  
		Size: 11.5 MB (11531644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b56fb8ece7173ff3f78204b7d316c8d0e91ff5797c2f128ea3719532755566b`  
		Last Modified: Thu, 10 Mar 2022 22:52:14 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:1bd12a832c8b9ef90b31c2037e4cc2bba48a1b2ff8f722993bb0a51359dcec88
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14243415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5193f0213996802c5ecf621611c41ca486634776b62c490f6ce3a63f8c459d5d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Thu, 10 Mar 2022 22:58:14 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 10 Mar 2022 22:58:17 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 10 Mar 2022 22:58:17 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 22:58:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 10 Mar 2022 22:58:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Mar 2022 22:58:23 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 10 Mar 2022 22:58:23 GMT
ENV XDG_DATA_HOME=/data
# Thu, 10 Mar 2022 22:58:24 GMT
VOLUME [/config]
# Thu, 10 Mar 2022 22:58:24 GMT
VOLUME [/data]
# Thu, 10 Mar 2022 22:58:24 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Thu, 10 Mar 2022 22:58:25 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 10 Mar 2022 22:58:25 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 10 Mar 2022 22:58:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 10 Mar 2022 22:58:26 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 10 Mar 2022 22:58:26 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 10 Mar 2022 22:58:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 10 Mar 2022 22:58:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 10 Mar 2022 22:58:28 GMT
EXPOSE 80
# Thu, 10 Mar 2022 22:58:28 GMT
EXPOSE 443
# Thu, 10 Mar 2022 22:58:29 GMT
EXPOSE 2019
# Thu, 10 Mar 2022 22:58:29 GMT
WORKDIR /srv
# Thu, 10 Mar 2022 22:58:29 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b7983ef4055364abada1e9d90961200fa12a940e65618e3deae6d94ef1de00`  
		Last Modified: Thu, 10 Mar 2022 23:00:17 GMT  
		Size: 290.7 KB (290698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683efd57d03b0caa68cb8294af9eacbd8a767d0bf033826ef6cb630d49e7746f`  
		Last Modified: Thu, 10 Mar 2022 23:00:17 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d266cd1399712df50a883c327a923a84535e481bd04e192cd2242e630eb35761`  
		Last Modified: Thu, 10 Mar 2022 23:00:24 GMT  
		Size: 11.5 MB (11511970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d21aebeed4d46b8af4d3498e63ea84a09fc0a8baca111e15eddb8223c4468d1`  
		Last Modified: Thu, 10 Mar 2022 23:00:17 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:926a4905f150b0c5f0e3af4a0fb8499c250040fd76d6a10b0caba77cedda4906
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14150649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd6a34ea54b24370b92bc5e69ed5e8883b415c07b33a5fb0411af6fda6cc448`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Thu, 10 Mar 2022 22:39:46 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 10 Mar 2022 22:39:48 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 10 Mar 2022 22:39:49 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 22:39:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 10 Mar 2022 22:39:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Mar 2022 22:39:53 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 10 Mar 2022 22:39:54 GMT
ENV XDG_DATA_HOME=/data
# Thu, 10 Mar 2022 22:39:55 GMT
VOLUME [/config]
# Thu, 10 Mar 2022 22:39:56 GMT
VOLUME [/data]
# Thu, 10 Mar 2022 22:39:57 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Thu, 10 Mar 2022 22:39:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 10 Mar 2022 22:39:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 10 Mar 2022 22:40:00 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 10 Mar 2022 22:40:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 10 Mar 2022 22:40:02 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 10 Mar 2022 22:40:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 10 Mar 2022 22:40:04 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 10 Mar 2022 22:40:05 GMT
EXPOSE 80
# Thu, 10 Mar 2022 22:40:06 GMT
EXPOSE 443
# Thu, 10 Mar 2022 22:40:07 GMT
EXPOSE 2019
# Thu, 10 Mar 2022 22:40:08 GMT
WORKDIR /srv
# Thu, 10 Mar 2022 22:40:09 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341f5c6df96a51fba8688cf172735f506dc6d217d6980a726e379207bd340479`  
		Last Modified: Thu, 10 Mar 2022 22:41:08 GMT  
		Size: 291.3 KB (291312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7dd361c9a8eddc2de6308df834d1c0ead713a2002cc63e09c1db3289cea6e8`  
		Last Modified: Thu, 10 Mar 2022 22:41:08 GMT  
		Size: 5.8 KB (5752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bb8aa7a1559d414d7419eb9f3d4de311531be8c728dedf757673582c478e68`  
		Last Modified: Thu, 10 Mar 2022 22:41:10 GMT  
		Size: 11.1 MB (11137998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5140397d04adfeb03f93bc807ef0be5f81c06dab593417424fbc4387b123f3a5`  
		Last Modified: Thu, 10 Mar 2022 22:41:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:a31b274a2eee69b3f4e035f8e298cd136f84943d7262c12613e6d6b8694c9e8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14633245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb2815c3839014e86a19f7c9ca632f8da1125e05b51de29ab5e64caddeccf58`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Thu, 10 Mar 2022 22:41:46 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 10 Mar 2022 22:41:48 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 10 Mar 2022 22:41:48 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 22:41:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4624dd27b7b53a0b82e17bfb64901eece99ffd943af888f3815e20e0b55c1aaadc15c6f517d985ffcf911e21ef9cb78a044661407a6d4e3c543f2cceede53f7e' ;; 		armhf)   binArch='armv6'; checksum='8615a6aacd10cb2e74f169ae1756ecd8508521791e511f8eca0dfc05f312aae5822b209787f4917c722a01e943f9317b35c8aa436c9086239e564079ef270078' ;; 		armv7)   binArch='armv7'; checksum='dc7c70efaaed0df7c6af959dd61ce79cae8d1217c6a8a68196eaef92438bd51a019f40dbc4e2f112c8ef8d01312d2e7bc8efc40d5e91342b8dba78ed2407e7da' ;; 		aarch64) binArch='arm64'; checksum='50065feb4b20f1c6f2fb4305047f8cd5eca8eb6dae478944c93078402905513c715c5bbbad43a3c90a766c6b75bb18de53023a8e07238733d6436a8a18960162' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c36537aa861ae9bb41db661ed8dd2e04c1904bd25a0d600b5ee2aa94f8ab7724bc3003e8708f7a41204b42d30b80b53e9655f0bf8fd91bfea36f75d5ddd76534' ;; 		s390x)   binArch='s390x'; checksum='26d6be36fb481e2483308cbd97a20b1c1ebc4d332157b9ff440edb33f825787cd205bf5f5a2fdaef1c214fb8a3c2a497db8fd8b58844d885d83f223f119c4034' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.5.0-beta.1/caddy_2.5.0-beta.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 10 Mar 2022 22:41:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 10 Mar 2022 22:41:51 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 10 Mar 2022 22:41:51 GMT
ENV XDG_DATA_HOME=/data
# Thu, 10 Mar 2022 22:41:52 GMT
VOLUME [/config]
# Thu, 10 Mar 2022 22:41:52 GMT
VOLUME [/data]
# Thu, 10 Mar 2022 22:41:52 GMT
LABEL org.opencontainers.image.version=v2.5.0-beta.1
# Thu, 10 Mar 2022 22:41:52 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 10 Mar 2022 22:41:52 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 10 Mar 2022 22:41:52 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 10 Mar 2022 22:41:52 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 10 Mar 2022 22:41:52 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 10 Mar 2022 22:41:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 10 Mar 2022 22:41:53 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 10 Mar 2022 22:41:53 GMT
EXPOSE 80
# Thu, 10 Mar 2022 22:41:53 GMT
EXPOSE 443
# Thu, 10 Mar 2022 22:41:53 GMT
EXPOSE 2019
# Thu, 10 Mar 2022 22:41:53 GMT
WORKDIR /srv
# Thu, 10 Mar 2022 22:41:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c9c83e4654ae545552a5c4ce045b21c0ae08af0b51008766e99912f260a41b`  
		Last Modified: Thu, 10 Mar 2022 22:42:53 GMT  
		Size: 291.8 KB (291831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb10ce05d5a54c9e9e97db29c0f900617aa6c8ca42f6306895ed22a2d0b65954`  
		Last Modified: Thu, 10 Mar 2022 22:42:53 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b63897f7c6ba88d70c2f8a66b6b7c56f7e1ea6aeeb29447f43a6745b4f7b9a2`  
		Last Modified: Thu, 10 Mar 2022 22:42:55 GMT  
		Size: 11.7 MB (11729487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7485c28d0c46c85a0a7f50096c24d5fdf21e71f7a8037ad11d818f9c8a44dc`  
		Last Modified: Thu, 10 Mar 2022 22:42:53 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.5.0-beta.1-builder`

```console
$ docker pull caddy@sha256:cd2211486e003b20619901f53800448d3d6a946ea0be46160c86d292ae20d889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `caddy:2.5.0-beta.1-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:b42936fa4029bc5a50133779ab670a49933240fdd5c8ff71d5e61254323961d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115838873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3478d84b75ea9ac76f04d0845fddc67e614e9911c8bbd6c10ebaf2c5321c5c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 02:32:18 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 02:32:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 02:32:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 22:50:05 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 03 Mar 2022 22:53:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 03 Mar 2022 22:53:52 GMT
ENV GOPATH=/go
# Thu, 03 Mar 2022 22:53:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 22:53:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 03 Mar 2022 22:53:54 GMT
WORKDIR /go
# Thu, 03 Mar 2022 23:28:42 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:49:51 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:50:39 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 22:50:40 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:50:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:50:43 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:50:43 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228ad0256439cce3fe9db355991b0557f55241d8cca8690f4f741e1c2d8fb8b9`  
		Last Modified: Tue, 30 Nov 2021 02:47:28 GMT  
		Size: 282.1 KB (282105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cab2a064767512d7d354e806cbd8b24ffefc15e06eeb7d4b127e7f6cddb6b40`  
		Last Modified: Tue, 30 Nov 2021 02:47:28 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798ddefed71bfdadb9d2b02c26fb7579e437fcf60f8af3f7cefed7967580d7da`  
		Last Modified: Thu, 03 Mar 2022 23:08:07 GMT  
		Size: 105.1 MB (105068635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7451a2cdc06b1d637a7e3849503cd56318bc1eb291dc792a6294cec777a31980`  
		Last Modified: Thu, 03 Mar 2022 23:06:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3489c6c0bcd6d649e4760550c8033a06b697ff4490644c130dde6501db25ab26`  
		Last Modified: Thu, 03 Mar 2022 23:29:55 GMT  
		Size: 6.7 MB (6677482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354620fed1855bf84eb0c7e209e4dd726fa89b06345297641e7aef200fc1d102`  
		Last Modified: Thu, 10 Mar 2022 22:52:30 GMT  
		Size: 1.2 MB (1178509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b21dccedf604c2267e8b48019d615961c412624cda224a8f30b404f106b344c`  
		Last Modified: Thu, 10 Mar 2022 22:52:29 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:0dd3796e91e0c363bfa60c2686654387822ffde8d1c947858478a19ddf69b1a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114698936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f97510234afb910e65acea53e13785b9a9913108edfa6cf77d6e1eb22801ef`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:10:37 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 04:10:39 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 04:10:39 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:51:53 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 00:55:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 00:55:09 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 00:55:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:55:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 00:55:12 GMT
WORKDIR /go
# Fri, 04 Mar 2022 06:45:24 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:57:52 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:58:41 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 22:58:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:58:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:58:44 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:58:45 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f21e2af73375430a6481f93a61f3df4f9de38c985f83b27293f8aace16d6b5`  
		Last Modified: Tue, 30 Nov 2021 04:33:33 GMT  
		Size: 281.2 KB (281248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cec97f9b59f8579851b3f2c1523c8a96065c591f5961858420e92bf9d424d2`  
		Last Modified: Tue, 30 Nov 2021 04:33:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edfb2fbd38ed3972211201867b2a8e18c8dc23b141d716828e9914c61276ecd`  
		Last Modified: Fri, 04 Mar 2022 01:19:22 GMT  
		Size: 104.9 MB (104853230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a4329e8253fda916ae04b5a3c4d217f5f24639ce303c8a3f2b24588f490196`  
		Last Modified: Fri, 04 Mar 2022 01:18:12 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c608e2c7ee3c9ef36153815e881ac6bc5cf7ff68862fcddf588d11054f20923`  
		Last Modified: Fri, 04 Mar 2022 06:46:39 GMT  
		Size: 6.0 MB (5952263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9458a6ce9b36ca305d267e9900e0bff59a1b78100638baf55f4d66d526685ce7`  
		Last Modified: Thu, 10 Mar 2022 23:00:32 GMT  
		Size: 1.2 MB (1176712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072d4018278756213f8759c62690aaaff01fba5526093892c4b41d8f51e8a1b7`  
		Last Modified: Thu, 10 Mar 2022 23:00:31 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:e91a1e0edd0cee256287a0a5e33cf7f411247e6206514d18b5d0b7c2fa914777
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115495271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2040ca07b37ced795152df231c92a5c17caa5da07686736abd98a96ed4705aaa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 01:54:59 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 01:55:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 01:55:01 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 02:29:42 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 02:31:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 02:31:06 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 02:31:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 02:31:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 02:31:09 GMT
WORKDIR /go
# Fri, 04 Mar 2022 03:10:53 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:39:34 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:40:16 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 22:40:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:40:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:40:20 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:40:20 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a89e8eeedd549875510e5e4e14010906a58878526814e6df25d14009856c6ff`  
		Last Modified: Tue, 30 Nov 2021 02:05:10 GMT  
		Size: 281.9 KB (281899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94645a83ff95687e6f078c140cfcac8def006923ed4019ef74fa189e6d9f0b14`  
		Last Modified: Tue, 30 Nov 2021 02:05:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caad3c9267df5b5261016d2d8843a47ffd88678a81f5e2363c426640adaf2029`  
		Last Modified: Fri, 04 Mar 2022 02:41:55 GMT  
		Size: 104.4 MB (104422515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e36f09527def3bbe5253cea2be9051532cf4a71f0df8fec8a85c922ce640c36`  
		Last Modified: Fri, 04 Mar 2022 02:41:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336ffb45c2b4e74ba78ba96c6f82f7fec126618bbacdc0fa27c7d3677b5aa6f1`  
		Last Modified: Fri, 04 Mar 2022 03:11:32 GMT  
		Size: 6.9 MB (6926057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fca57ebddc8893d9d5eb58bdda9ac5fc826d78ec10d2d1a18610c2f75aed40`  
		Last Modified: Thu, 10 Mar 2022 22:41:18 GMT  
		Size: 1.1 MB (1148678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc764824108ad7f417a5eac762104a6775124fec2be01892bdd66823671a2262`  
		Last Modified: Thu, 10 Mar 2022 22:41:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder` - linux; s390x

```console
$ docker pull caddy@sha256:35e6ee5f4a04bfbb95d06bd2830aab68eb09dba3a7b1870a912a70f0efa03194
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118763072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a46c7a3939f0c106655b22b682163ab4884afed9978cc15755541680941ad8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:07:57 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 04:07:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 04:07:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 23:09:57 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 03 Mar 2022 23:12:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 03 Mar 2022 23:12:29 GMT
ENV GOPATH=/go
# Thu, 03 Mar 2022 23:12:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 23:12:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 03 Mar 2022 23:12:29 GMT
WORKDIR /go
# Fri, 04 Mar 2022 00:05:09 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:41:34 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:42:00 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 22:42:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:42:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:42:01 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:42:01 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66787da5af638f8523e4694d81d38c2ca7c0a262f4cb8d78c46f7d64833bbaa0`  
		Last Modified: Tue, 30 Nov 2021 04:17:43 GMT  
		Size: 282.4 KB (282378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406f41068af489d7950f1a75d72455e702ed7da98dad21d9267448257b6a2ddc`  
		Last Modified: Tue, 30 Nov 2021 04:17:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee9a2e8145f1c142e4295add6c8c87e35418763276db9058b5b7ed0cc175e80`  
		Last Modified: Thu, 03 Mar 2022 23:26:10 GMT  
		Size: 107.7 MB (107739292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1f97ab22dac5e8b60c0770634135f40d0eba00b3f8a5bd5de06c0b1f34676d`  
		Last Modified: Thu, 03 Mar 2022 23:25:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5bcd397c1a177db9a5bf9729e85c6d9a4a1a63fe402e4e054b80d981f46080`  
		Last Modified: Fri, 04 Mar 2022 00:05:47 GMT  
		Size: 6.9 MB (6930956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90663d288776acfbf06dbb36afe189a229998e039919210d411b42141314a46b`  
		Last Modified: Thu, 10 Mar 2022 22:43:00 GMT  
		Size: 1.2 MB (1203783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2510db48e13b57a2728b4e11b9cc08eca24e7818906772746bb6b52d31cc20c8`  
		Last Modified: Thu, 10 Mar 2022 22:43:00 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.5.0-beta.1-builder-alpine`

```console
$ docker pull caddy@sha256:cd2211486e003b20619901f53800448d3d6a946ea0be46160c86d292ae20d889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `caddy:2.5.0-beta.1-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:b42936fa4029bc5a50133779ab670a49933240fdd5c8ff71d5e61254323961d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115838873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3478d84b75ea9ac76f04d0845fddc67e614e9911c8bbd6c10ebaf2c5321c5c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 02:32:18 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 02:32:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 02:32:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 22:50:05 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 03 Mar 2022 22:53:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 03 Mar 2022 22:53:52 GMT
ENV GOPATH=/go
# Thu, 03 Mar 2022 22:53:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 22:53:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 03 Mar 2022 22:53:54 GMT
WORKDIR /go
# Thu, 03 Mar 2022 23:28:42 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:49:51 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:50:39 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 22:50:40 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:50:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:50:43 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:50:43 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228ad0256439cce3fe9db355991b0557f55241d8cca8690f4f741e1c2d8fb8b9`  
		Last Modified: Tue, 30 Nov 2021 02:47:28 GMT  
		Size: 282.1 KB (282105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cab2a064767512d7d354e806cbd8b24ffefc15e06eeb7d4b127e7f6cddb6b40`  
		Last Modified: Tue, 30 Nov 2021 02:47:28 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798ddefed71bfdadb9d2b02c26fb7579e437fcf60f8af3f7cefed7967580d7da`  
		Last Modified: Thu, 03 Mar 2022 23:08:07 GMT  
		Size: 105.1 MB (105068635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7451a2cdc06b1d637a7e3849503cd56318bc1eb291dc792a6294cec777a31980`  
		Last Modified: Thu, 03 Mar 2022 23:06:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3489c6c0bcd6d649e4760550c8033a06b697ff4490644c130dde6501db25ab26`  
		Last Modified: Thu, 03 Mar 2022 23:29:55 GMT  
		Size: 6.7 MB (6677482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354620fed1855bf84eb0c7e209e4dd726fa89b06345297641e7aef200fc1d102`  
		Last Modified: Thu, 10 Mar 2022 22:52:30 GMT  
		Size: 1.2 MB (1178509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b21dccedf604c2267e8b48019d615961c412624cda224a8f30b404f106b344c`  
		Last Modified: Thu, 10 Mar 2022 22:52:29 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:0dd3796e91e0c363bfa60c2686654387822ffde8d1c947858478a19ddf69b1a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114698936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f97510234afb910e65acea53e13785b9a9913108edfa6cf77d6e1eb22801ef`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:10:37 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 04:10:39 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 04:10:39 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:51:53 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 00:55:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 00:55:09 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 00:55:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:55:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 00:55:12 GMT
WORKDIR /go
# Fri, 04 Mar 2022 06:45:24 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:57:52 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:58:41 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 22:58:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:58:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:58:44 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:58:45 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f21e2af73375430a6481f93a61f3df4f9de38c985f83b27293f8aace16d6b5`  
		Last Modified: Tue, 30 Nov 2021 04:33:33 GMT  
		Size: 281.2 KB (281248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cec97f9b59f8579851b3f2c1523c8a96065c591f5961858420e92bf9d424d2`  
		Last Modified: Tue, 30 Nov 2021 04:33:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edfb2fbd38ed3972211201867b2a8e18c8dc23b141d716828e9914c61276ecd`  
		Last Modified: Fri, 04 Mar 2022 01:19:22 GMT  
		Size: 104.9 MB (104853230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a4329e8253fda916ae04b5a3c4d217f5f24639ce303c8a3f2b24588f490196`  
		Last Modified: Fri, 04 Mar 2022 01:18:12 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c608e2c7ee3c9ef36153815e881ac6bc5cf7ff68862fcddf588d11054f20923`  
		Last Modified: Fri, 04 Mar 2022 06:46:39 GMT  
		Size: 6.0 MB (5952263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9458a6ce9b36ca305d267e9900e0bff59a1b78100638baf55f4d66d526685ce7`  
		Last Modified: Thu, 10 Mar 2022 23:00:32 GMT  
		Size: 1.2 MB (1176712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072d4018278756213f8759c62690aaaff01fba5526093892c4b41d8f51e8a1b7`  
		Last Modified: Thu, 10 Mar 2022 23:00:31 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:e91a1e0edd0cee256287a0a5e33cf7f411247e6206514d18b5d0b7c2fa914777
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115495271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2040ca07b37ced795152df231c92a5c17caa5da07686736abd98a96ed4705aaa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 01:54:59 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 01:55:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 01:55:01 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 02:29:42 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 02:31:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 02:31:06 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 02:31:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 02:31:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 02:31:09 GMT
WORKDIR /go
# Fri, 04 Mar 2022 03:10:53 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:39:34 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:40:16 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 22:40:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:40:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:40:20 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:40:20 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a89e8eeedd549875510e5e4e14010906a58878526814e6df25d14009856c6ff`  
		Last Modified: Tue, 30 Nov 2021 02:05:10 GMT  
		Size: 281.9 KB (281899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94645a83ff95687e6f078c140cfcac8def006923ed4019ef74fa189e6d9f0b14`  
		Last Modified: Tue, 30 Nov 2021 02:05:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caad3c9267df5b5261016d2d8843a47ffd88678a81f5e2363c426640adaf2029`  
		Last Modified: Fri, 04 Mar 2022 02:41:55 GMT  
		Size: 104.4 MB (104422515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e36f09527def3bbe5253cea2be9051532cf4a71f0df8fec8a85c922ce640c36`  
		Last Modified: Fri, 04 Mar 2022 02:41:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336ffb45c2b4e74ba78ba96c6f82f7fec126618bbacdc0fa27c7d3677b5aa6f1`  
		Last Modified: Fri, 04 Mar 2022 03:11:32 GMT  
		Size: 6.9 MB (6926057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fca57ebddc8893d9d5eb58bdda9ac5fc826d78ec10d2d1a18610c2f75aed40`  
		Last Modified: Thu, 10 Mar 2022 22:41:18 GMT  
		Size: 1.1 MB (1148678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc764824108ad7f417a5eac762104a6775124fec2be01892bdd66823671a2262`  
		Last Modified: Thu, 10 Mar 2022 22:41:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.5.0-beta.1-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:35e6ee5f4a04bfbb95d06bd2830aab68eb09dba3a7b1870a912a70f0efa03194
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118763072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a46c7a3939f0c106655b22b682163ab4884afed9978cc15755541680941ad8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:07:57 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 04:07:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 04:07:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 23:09:57 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 03 Mar 2022 23:12:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 03 Mar 2022 23:12:29 GMT
ENV GOPATH=/go
# Thu, 03 Mar 2022 23:12:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 23:12:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 03 Mar 2022 23:12:29 GMT
WORKDIR /go
# Fri, 04 Mar 2022 00:05:09 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:41:34 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:42:00 GMT
ENV CADDY_VERSION=v2.5.0-beta.1
# Thu, 10 Mar 2022 22:42:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:42:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:42:01 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:42:01 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66787da5af638f8523e4694d81d38c2ca7c0a262f4cb8d78c46f7d64833bbaa0`  
		Last Modified: Tue, 30 Nov 2021 04:17:43 GMT  
		Size: 282.4 KB (282378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406f41068af489d7950f1a75d72455e702ed7da98dad21d9267448257b6a2ddc`  
		Last Modified: Tue, 30 Nov 2021 04:17:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee9a2e8145f1c142e4295add6c8c87e35418763276db9058b5b7ed0cc175e80`  
		Last Modified: Thu, 03 Mar 2022 23:26:10 GMT  
		Size: 107.7 MB (107739292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1f97ab22dac5e8b60c0770634135f40d0eba00b3f8a5bd5de06c0b1f34676d`  
		Last Modified: Thu, 03 Mar 2022 23:25:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5bcd397c1a177db9a5bf9729e85c6d9a4a1a63fe402e4e054b80d981f46080`  
		Last Modified: Fri, 04 Mar 2022 00:05:47 GMT  
		Size: 6.9 MB (6930956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90663d288776acfbf06dbb36afe189a229998e039919210d411b42141314a46b`  
		Last Modified: Thu, 10 Mar 2022 22:43:00 GMT  
		Size: 1.2 MB (1203783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2510db48e13b57a2728b4e11b9cc08eca24e7818906772746bb6b52d31cc20c8`  
		Last Modified: Thu, 10 Mar 2022 22:43:00 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.5.0-beta.1-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `caddy:2.5.0-beta.1-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `caddy:2.5.0-beta.1-windowsservercore`

```console
$ docker pull caddy@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `caddy:2.5.0-beta.1-windowsservercore-1809`

```console
$ docker pull caddy@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `caddy:2.5.0-beta.1-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `caddy:alpine`

```console
$ docker pull caddy@sha256:1659785ea84188c3ad22a6c1f96f463d167a4b81318d71f4bb6e3d37dbe73908
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
$ docker pull caddy@sha256:7da0f90273e1961d9c38d26809f84d4ef3cdc9b4fc330a9cab22015d7c9e8228
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14856906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439af64db48912c0a446444aae0e357183264ff08e1154fa105d5ee082e0bf13`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:54:17 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 12 Nov 2021 21:54:18 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Fri, 12 Nov 2021 21:54:19 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 12 Nov 2021 21:54:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 12 Nov 2021 21:54:23 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:54:23 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 12 Nov 2021 21:54:23 GMT
ENV XDG_DATA_HOME=/data
# Fri, 12 Nov 2021 21:54:23 GMT
VOLUME [/config]
# Fri, 12 Nov 2021 21:54:24 GMT
VOLUME [/data]
# Fri, 12 Nov 2021 21:54:24 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Fri, 12 Nov 2021 21:54:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 12 Nov 2021 21:54:24 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 12 Nov 2021 21:54:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 12 Nov 2021 21:54:25 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 12 Nov 2021 21:54:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 12 Nov 2021 21:54:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 12 Nov 2021 21:54:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 12 Nov 2021 21:54:25 GMT
EXPOSE 80
# Fri, 12 Nov 2021 21:54:26 GMT
EXPOSE 443
# Fri, 12 Nov 2021 21:54:26 GMT
EXPOSE 2019
# Fri, 12 Nov 2021 21:54:26 GMT
WORKDIR /srv
# Fri, 12 Nov 2021 21:54:26 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ccae726125d77e2fd3891c69c8f663d5fe63d8ad4a67deb284e2c589334497`  
		Last Modified: Fri, 12 Nov 2021 21:54:48 GMT  
		Size: 301.5 KB (301497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de6a61c89acc2147364721befe6e6bf957963713d1ddc4bc6c4a35f7b4b4e0a`  
		Last Modified: Fri, 12 Nov 2021 21:54:48 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ed957bdc008c4cc475fcaeb053cdb7fbcc83f49184fca8013d87cf9d395518`  
		Last Modified: Fri, 12 Nov 2021 21:54:50 GMT  
		Size: 11.7 MB (11726445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae44c2d42ddcf77445d391f491713e6384b933553eb234ceb0d9b3e66c5b33f`  
		Last Modified: Fri, 12 Nov 2021 21:54:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:caa4910dc3572e3ba3888fda3f7f5ed69c8c575461d29e528a6b453c0ba90522
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14068833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358685e491b9f796f29e9b70a0a43f619fa034e7bcd995cf738d811cf8e4ebe9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:07:54 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 12 Nov 2021 17:07:57 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Fri, 12 Nov 2021 17:07:57 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 12 Nov 2021 17:08:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 12 Nov 2021 17:08:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 17:08:04 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 12 Nov 2021 17:08:05 GMT
ENV XDG_DATA_HOME=/data
# Fri, 12 Nov 2021 17:08:05 GMT
VOLUME [/config]
# Fri, 12 Nov 2021 17:08:06 GMT
VOLUME [/data]
# Fri, 12 Nov 2021 17:08:06 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Fri, 12 Nov 2021 17:08:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 12 Nov 2021 17:08:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 12 Nov 2021 17:08:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 12 Nov 2021 17:08:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 12 Nov 2021 17:08:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 12 Nov 2021 17:08:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 12 Nov 2021 17:08:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 12 Nov 2021 17:08:10 GMT
EXPOSE 80
# Fri, 12 Nov 2021 17:08:10 GMT
EXPOSE 443
# Fri, 12 Nov 2021 17:08:11 GMT
EXPOSE 2019
# Fri, 12 Nov 2021 17:08:11 GMT
WORKDIR /srv
# Fri, 12 Nov 2021 17:08:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d466a8f7766a93ea57a37532240c4a8c0e21cdb1f731360b1d21022b74f840f1`  
		Last Modified: Fri, 12 Nov 2021 17:09:28 GMT  
		Size: 301.7 KB (301671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082eb2081a4e07ea8cd0a36b4c3e7fee48ac23e2f6e8b7f95659e9a7465012fb`  
		Last Modified: Fri, 12 Nov 2021 17:09:27 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3790fd0e6afb978b6d8b451eaea5ab3e59b48913548a910853b31bc234bfed1c`  
		Last Modified: Fri, 12 Nov 2021 17:09:35 GMT  
		Size: 11.1 MB (11125784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe30a92d02271e636688f49fc9e1b382f2836b2c4578c29a993dc5111eb0b927`  
		Last Modified: Fri, 12 Nov 2021 17:09:27 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:5211ef3cdd2abf233de36a5e914b3ea2a649f0ec2164e5c63dd96c0cf870004e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13852151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389ecbea3a7d6a7b6a98da18b9b565046f2629b6c4af69a7d20d5cabcd1562d5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 11:43:41 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 13 Nov 2021 11:43:44 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 13 Nov 2021 11:43:44 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 13 Nov 2021 11:43:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 13 Nov 2021 11:43:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 11:43:51 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 13 Nov 2021 11:43:51 GMT
ENV XDG_DATA_HOME=/data
# Sat, 13 Nov 2021 11:43:52 GMT
VOLUME [/config]
# Sat, 13 Nov 2021 11:43:52 GMT
VOLUME [/data]
# Sat, 13 Nov 2021 11:43:53 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 13 Nov 2021 11:43:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 13 Nov 2021 11:43:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 13 Nov 2021 11:43:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 13 Nov 2021 11:43:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 13 Nov 2021 11:43:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 13 Nov 2021 11:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 13 Nov 2021 11:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 13 Nov 2021 11:43:57 GMT
EXPOSE 80
# Sat, 13 Nov 2021 11:43:57 GMT
EXPOSE 443
# Sat, 13 Nov 2021 11:43:58 GMT
EXPOSE 2019
# Sat, 13 Nov 2021 11:43:58 GMT
WORKDIR /srv
# Sat, 13 Nov 2021 11:43:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5663fa07ca1dcac265e40e084d2e40771a9084e9b30309c275bf810e87a3b53a`  
		Last Modified: Sat, 13 Nov 2021 11:45:26 GMT  
		Size: 300.8 KB (300831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf8bc3ddae458c10861b1ef0a30a6c8e97ea3a7135680ced673a2532a4c043e`  
		Last Modified: Sat, 13 Nov 2021 11:45:25 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afb06d1223418bbdf22f64f5a3a57962ad6570d931f931ab8df015439fb0c7a`  
		Last Modified: Sat, 13 Nov 2021 11:45:33 GMT  
		Size: 11.1 MB (11106718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a00e0b33a8465343d1f7f61ffec47a7c7aaad34402170530d9e9ebbb4ac5665`  
		Last Modified: Sat, 13 Nov 2021 11:45:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:8c2b7f01f3d14048e888946dd85b972ac76d22490107d999f6df18399ab76f25
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13763680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e48a5247e105a4ecd7f6a7b3f6bfe21fe6633146de42ad9bd4197b3222b920d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 11:18:37 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 13 Nov 2021 11:18:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 13 Nov 2021 11:18:40 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 13 Nov 2021 11:18:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 13 Nov 2021 11:18:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 11:18:44 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 13 Nov 2021 11:18:45 GMT
ENV XDG_DATA_HOME=/data
# Sat, 13 Nov 2021 11:18:46 GMT
VOLUME [/config]
# Sat, 13 Nov 2021 11:18:47 GMT
VOLUME [/data]
# Sat, 13 Nov 2021 11:18:48 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 13 Nov 2021 11:18:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 13 Nov 2021 11:18:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 13 Nov 2021 11:18:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 13 Nov 2021 11:18:52 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 13 Nov 2021 11:18:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 13 Nov 2021 11:18:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 13 Nov 2021 11:18:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 13 Nov 2021 11:18:56 GMT
EXPOSE 80
# Sat, 13 Nov 2021 11:18:57 GMT
EXPOSE 443
# Sat, 13 Nov 2021 11:18:58 GMT
EXPOSE 2019
# Sat, 13 Nov 2021 11:18:59 GMT
WORKDIR /srv
# Sat, 13 Nov 2021 11:19:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e205c63fa7e1c7a1060c29f8600bf90d965a1d26a1ae313210de738d08649d0`  
		Last Modified: Sat, 13 Nov 2021 11:19:44 GMT  
		Size: 301.4 KB (301450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674f75736ea40598c6df0d5460f914bf940c50952e8f106cdb674f9d98e8c5bb`  
		Last Modified: Sat, 13 Nov 2021 11:19:44 GMT  
		Size: 5.8 KB (5750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e004593c132f71a51cbd6967cf29bac3fc607c79fa8d967253c2f79461442641`  
		Last Modified: Sat, 13 Nov 2021 11:19:45 GMT  
		Size: 10.7 MB (10738627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51900aef2f22db52e1c14e6dd7f645241d02abef12b8ef2b377595f11b77055b`  
		Last Modified: Sat, 13 Nov 2021 11:19:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:b47a92735f1a101ce7087f2fc6f8b33614226b32c4507de0de8a4b6b34d84504
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13429323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bbba192f1381ae73d2265be6a6b84d7539131fcc66399931bd66ff97ff83f5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 21:18:00 GMT
ADD file:4d45063079cb28a34f1e382fddb22f156ac99d5449aa05ed37cb653c1f7b80f2 in / 
# Fri, 12 Nov 2021 21:18:01 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 15:14:03 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 13 Nov 2021 15:14:24 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 13 Nov 2021 15:14:33 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 13 Nov 2021 15:14:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 13 Nov 2021 15:14:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 15:14:54 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 13 Nov 2021 15:14:58 GMT
ENV XDG_DATA_HOME=/data
# Sat, 13 Nov 2021 15:15:03 GMT
VOLUME [/config]
# Sat, 13 Nov 2021 15:15:05 GMT
VOLUME [/data]
# Sat, 13 Nov 2021 15:15:09 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 13 Nov 2021 15:15:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 13 Nov 2021 15:15:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 13 Nov 2021 15:15:19 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 13 Nov 2021 15:15:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 13 Nov 2021 15:15:26 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 13 Nov 2021 15:15:30 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 13 Nov 2021 15:15:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 13 Nov 2021 15:15:35 GMT
EXPOSE 80
# Sat, 13 Nov 2021 15:15:37 GMT
EXPOSE 443
# Sat, 13 Nov 2021 15:15:40 GMT
EXPOSE 2019
# Sat, 13 Nov 2021 15:15:42 GMT
WORKDIR /srv
# Sat, 13 Nov 2021 15:15:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:72940440c1ab65eca4d38846164719ffde4b147543cc658d041407a925b13368`  
		Last Modified: Fri, 12 Nov 2021 21:19:32 GMT  
		Size: 2.8 MB (2817467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aca7d05e49e358a035d0dd6f471c0d19419c9cc97646fff4e82578d2c488237`  
		Last Modified: Sat, 13 Nov 2021 15:16:26 GMT  
		Size: 303.6 KB (303607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc78b04675eccc541ab8678fe7221460039d23c40f04c02d41e150f256c4368`  
		Last Modified: Sat, 13 Nov 2021 15:16:25 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f289e05d8a93edbe6667d481e3a61908205bf58c77aa2ddf18b09f740724a8cd`  
		Last Modified: Sat, 13 Nov 2021 15:16:28 GMT  
		Size: 10.3 MB (10302268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd68deeff259e1bcfa76db665a6a52747267383f87bb506b77fbb409529ae3c8`  
		Last Modified: Sat, 13 Nov 2021 15:16:25 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:5ac69c24193df6b0d9b0c13816ce3861b720b62721901b0eb7446bd41ae86a3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14240890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753d56e00623363d01fede6cee26039f1b7efc2f64fccec498168291c9b9ea6b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 04:01:37 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 13 Nov 2021 04:01:38 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 13 Nov 2021 04:01:38 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 13 Nov 2021 04:01:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 13 Nov 2021 04:01:42 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 04:01:42 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 13 Nov 2021 04:01:42 GMT
ENV XDG_DATA_HOME=/data
# Sat, 13 Nov 2021 04:01:42 GMT
VOLUME [/config]
# Sat, 13 Nov 2021 04:01:42 GMT
VOLUME [/data]
# Sat, 13 Nov 2021 04:01:42 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 13 Nov 2021 04:01:44 GMT
EXPOSE 80
# Sat, 13 Nov 2021 04:01:44 GMT
EXPOSE 443
# Sat, 13 Nov 2021 04:01:44 GMT
EXPOSE 2019
# Sat, 13 Nov 2021 04:01:44 GMT
WORKDIR /srv
# Sat, 13 Nov 2021 04:01:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0267ca443b43155e255c1a3bb35bab8ac5b561ddc2d0e768868f13274c7ab32d`  
		Last Modified: Sat, 13 Nov 2021 04:02:28 GMT  
		Size: 301.9 KB (301922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9c9c616a8868c7845a4a9d56e876f1bf42c37dac31b80761370b9af366e4c1`  
		Last Modified: Sat, 13 Nov 2021 04:02:28 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0dfff2c7fb2b8bde893d14f4d66fe6d6e8bee6115e0f4f691f7698d17a51f7`  
		Last Modified: Sat, 13 Nov 2021 04:02:29 GMT  
		Size: 11.3 MB (11323710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc9ba4f178258a6de34c95f9f50fb0fd89e093f552c493cd511cfb5fc39a433`  
		Last Modified: Sat, 13 Nov 2021 04:02:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder`

```console
$ docker pull caddy@sha256:aeb897e44b8614b95c66f1f00fb2a09b58a8fcb9c4b060e361a5493e626b6b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2686; amd64
	-	windows version 10.0.14393.4886; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:9c6a77c878ea39bd367c8c7e73f1a75a6ce97101bef0f3de7e288934b4de519e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121354364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c3a82ad51f9b44b272a32de82576c64480a940db9877dd465101c921e11593`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:21:45 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 04:21:46 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 04:21:47 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 01:05:33 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 01:08:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 01:08:13 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 01:08:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 01:08:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 01:08:14 GMT
WORKDIR /go
# Fri, 04 Mar 2022 04:22:25 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 04 Mar 2022 04:22:25 GMT
ENV XCADDY_VERSION=v0.2.0
# Fri, 04 Mar 2022 04:22:26 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 04 Mar 2022 04:22:26 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 04 Mar 2022 04:22:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 04 Mar 2022 04:22:27 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 04 Mar 2022 04:22:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666ba61612fd7c93393f9a5bc1751d8a9929e32d51501dba691da9e8232bc87b`  
		Last Modified: Tue, 30 Nov 2021 04:36:04 GMT  
		Size: 282.2 KB (282159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed8ca4862056a130f714accb3538decfa0663fec84e635d8b5a0a3305353dee`  
		Last Modified: Tue, 30 Nov 2021 04:36:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141c1ce2f203145a20c1b4550c662f943266dc7dbf7e15ee911b06456e2326da`  
		Last Modified: Fri, 04 Mar 2022 01:21:28 GMT  
		Size: 110.2 MB (110186591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4c7319106ffbcda864c88220ef7a19e3da3b571fa08e0be968efe7fbd9465f`  
		Last Modified: Fri, 04 Mar 2022 01:21:14 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0f327525fd9ac01a04ccd2c1530800b0c51b68d8821a2904e3d066d8663b3f`  
		Last Modified: Fri, 04 Mar 2022 04:22:46 GMT  
		Size: 6.8 MB (6821521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd85b87242bfb046d67955057b47bfdc6f774636e6b8334022ed51fe020a6301`  
		Last Modified: Fri, 04 Mar 2022 04:22:45 GMT  
		Size: 1.2 MB (1244966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32b29093c0b4e0e55e5212230f0fda6566f59ae3e6f91d6ae6b39363b0e7860`  
		Last Modified: Fri, 04 Mar 2022 04:22:45 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:f7e1a9b85365f550da1a0a03bbc6f0dc1c5930d86fcb7e857919ed50708462d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115838871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71a25849e386c048c58fcafd1884613238beacc8243d9fcdddddddbd10b458a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 02:32:18 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 02:32:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 02:32:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 22:50:05 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 03 Mar 2022 22:53:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 03 Mar 2022 22:53:52 GMT
ENV GOPATH=/go
# Thu, 03 Mar 2022 22:53:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 22:53:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 03 Mar 2022 22:53:54 GMT
WORKDIR /go
# Thu, 03 Mar 2022 23:28:42 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:49:51 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:49:52 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 22:49:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:49:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:49:55 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:49:55 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228ad0256439cce3fe9db355991b0557f55241d8cca8690f4f741e1c2d8fb8b9`  
		Last Modified: Tue, 30 Nov 2021 02:47:28 GMT  
		Size: 282.1 KB (282105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cab2a064767512d7d354e806cbd8b24ffefc15e06eeb7d4b127e7f6cddb6b40`  
		Last Modified: Tue, 30 Nov 2021 02:47:28 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798ddefed71bfdadb9d2b02c26fb7579e437fcf60f8af3f7cefed7967580d7da`  
		Last Modified: Thu, 03 Mar 2022 23:08:07 GMT  
		Size: 105.1 MB (105068635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7451a2cdc06b1d637a7e3849503cd56318bc1eb291dc792a6294cec777a31980`  
		Last Modified: Thu, 03 Mar 2022 23:06:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3489c6c0bcd6d649e4760550c8033a06b697ff4490644c130dde6501db25ab26`  
		Last Modified: Thu, 03 Mar 2022 23:29:55 GMT  
		Size: 6.7 MB (6677482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6889976625624adb9a9c5b111609959fe4da102919177fa9c53a23d173175d6`  
		Last Modified: Thu, 10 Mar 2022 22:51:59 GMT  
		Size: 1.2 MB (1178508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79172ebfda03823b62d347d32a6755fe56f0f8809466f11895c5a7d7ae48c3b0`  
		Last Modified: Thu, 10 Mar 2022 22:51:58 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:06e29bc1ce4d22e988eca705e6e4faf2ec70661ffb2a448a334e8b557068dd68
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114698943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14dc63acb649973c1c8c9f6f76def65c297a511f53a12f94af418ebc1c8da64e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:10:37 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 04:10:39 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 04:10:39 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:51:53 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 00:55:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 00:55:09 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 00:55:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:55:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 00:55:12 GMT
WORKDIR /go
# Fri, 04 Mar 2022 06:45:24 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:57:52 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:57:53 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 22:57:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:57:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:57:56 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:57:56 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f21e2af73375430a6481f93a61f3df4f9de38c985f83b27293f8aace16d6b5`  
		Last Modified: Tue, 30 Nov 2021 04:33:33 GMT  
		Size: 281.2 KB (281248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cec97f9b59f8579851b3f2c1523c8a96065c591f5961858420e92bf9d424d2`  
		Last Modified: Tue, 30 Nov 2021 04:33:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edfb2fbd38ed3972211201867b2a8e18c8dc23b141d716828e9914c61276ecd`  
		Last Modified: Fri, 04 Mar 2022 01:19:22 GMT  
		Size: 104.9 MB (104853230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a4329e8253fda916ae04b5a3c4d217f5f24639ce303c8a3f2b24588f490196`  
		Last Modified: Fri, 04 Mar 2022 01:18:12 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c608e2c7ee3c9ef36153815e881ac6bc5cf7ff68862fcddf588d11054f20923`  
		Last Modified: Fri, 04 Mar 2022 06:46:39 GMT  
		Size: 6.0 MB (5952263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca89b858a1ebd99c4675cae20c8f5c5e60653a6d2a307ec0bcd6e2e3b448d087`  
		Last Modified: Thu, 10 Mar 2022 23:00:00 GMT  
		Size: 1.2 MB (1176718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9c6a4e7cfb70b12bfb81a4fced64fb3d181017de696421ab4178c208f5defa`  
		Last Modified: Thu, 10 Mar 2022 22:59:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:ee6d440f72726b2d9d29a604a97ab0cc23505e8eccc68c64133eba5da0ef12de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115495270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9fe816e095b9092b887d34923435e91de44876c56fc189162c309a48f541ca`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 01:54:59 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 01:55:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 01:55:01 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 02:29:42 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 02:31:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 02:31:06 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 02:31:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 02:31:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 02:31:09 GMT
WORKDIR /go
# Fri, 04 Mar 2022 03:10:53 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:39:34 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:39:34 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 22:39:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:39:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:39:38 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:39:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a89e8eeedd549875510e5e4e14010906a58878526814e6df25d14009856c6ff`  
		Last Modified: Tue, 30 Nov 2021 02:05:10 GMT  
		Size: 281.9 KB (281899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94645a83ff95687e6f078c140cfcac8def006923ed4019ef74fa189e6d9f0b14`  
		Last Modified: Tue, 30 Nov 2021 02:05:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caad3c9267df5b5261016d2d8843a47ffd88678a81f5e2363c426640adaf2029`  
		Last Modified: Fri, 04 Mar 2022 02:41:55 GMT  
		Size: 104.4 MB (104422515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e36f09527def3bbe5253cea2be9051532cf4a71f0df8fec8a85c922ce640c36`  
		Last Modified: Fri, 04 Mar 2022 02:41:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336ffb45c2b4e74ba78ba96c6f82f7fec126618bbacdc0fa27c7d3677b5aa6f1`  
		Last Modified: Fri, 04 Mar 2022 03:11:32 GMT  
		Size: 6.9 MB (6926057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acd88183c62587770b090ffe6a970e05212ee61f949af7bad8e6edcb5743f0a`  
		Last Modified: Thu, 10 Mar 2022 22:40:54 GMT  
		Size: 1.1 MB (1148678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb0f9bf906b045657c360d551af06aa0af8bee7cbeb2e646cafa48abc2ac878`  
		Last Modified: Thu, 10 Mar 2022 22:40:54 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:4a53d3e10c18d0855f3ec5c9ec6dfb598f1a562d0828ec62b238370646e46e8a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114325817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251761ef86f00954d0b3d990c694bdcc74f14f6488585eef034148425fed6f23`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 03:17:54 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 03:17:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 03:18:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:12:42 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 00:15:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 00:15:47 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 00:15:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:15:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 00:15:58 GMT
WORKDIR /go
# Fri, 04 Mar 2022 07:20:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 04 Mar 2022 07:20:21 GMT
ENV XCADDY_VERSION=v0.2.0
# Fri, 04 Mar 2022 07:20:27 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 04 Mar 2022 07:20:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 04 Mar 2022 07:20:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 04 Mar 2022 07:20:51 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 04 Mar 2022 07:20:57 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28be42a6852cc2108ddba1e4252671ae20275780a6ff73b1038699f59da2ac20`  
		Last Modified: Tue, 30 Nov 2021 03:35:16 GMT  
		Size: 284.0 KB (284020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d744d6799a13f2f7a7f85e040ddf0cc8b671a7cc5572b7049c3e1da8139b349`  
		Last Modified: Tue, 30 Nov 2021 03:35:15 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3620d170b59e9b8337616ec72da9ade5c2471d3b0cf50e3a538e6171d5d813a4`  
		Last Modified: Fri, 04 Mar 2022 00:33:32 GMT  
		Size: 102.8 MB (102785250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bec6e3bcdb44b28a2f07f58bc175553abc87d573010ff47564a72aff7749eb5`  
		Last Modified: Fri, 04 Mar 2022 00:33:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75230c4358c070669508567379db20aa0f6acf5775eb391f81394cc567994d4`  
		Last Modified: Fri, 04 Mar 2022 07:21:55 GMT  
		Size: 7.3 MB (7321033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29c6375e4c4e1312ebfadd212ce4b17f7f002743d73d01fca882a24eba618ac`  
		Last Modified: Fri, 04 Mar 2022 07:21:54 GMT  
		Size: 1.1 MB (1120019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47ae1c41cc141d20ffc3fe6ecccea9ac5fb48eefdeab0dec835beb21c731ac4`  
		Last Modified: Fri, 04 Mar 2022 07:21:54 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:43996cf55b905a5c54ef7cc5f9192ec4077d75694985c130d4866c3c9a537109
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118763072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad0782969bd455fc3ed6f62197dd5e0686ae55f02024605d501e975ceaf4c99`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:07:57 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 04:07:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 04:07:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 23:09:57 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 03 Mar 2022 23:12:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 03 Mar 2022 23:12:29 GMT
ENV GOPATH=/go
# Thu, 03 Mar 2022 23:12:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 23:12:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 03 Mar 2022 23:12:29 GMT
WORKDIR /go
# Fri, 04 Mar 2022 00:05:09 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:41:34 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:41:35 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 22:41:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:41:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:41:36 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:41:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66787da5af638f8523e4694d81d38c2ca7c0a262f4cb8d78c46f7d64833bbaa0`  
		Last Modified: Tue, 30 Nov 2021 04:17:43 GMT  
		Size: 282.4 KB (282378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406f41068af489d7950f1a75d72455e702ed7da98dad21d9267448257b6a2ddc`  
		Last Modified: Tue, 30 Nov 2021 04:17:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee9a2e8145f1c142e4295add6c8c87e35418763276db9058b5b7ed0cc175e80`  
		Last Modified: Thu, 03 Mar 2022 23:26:10 GMT  
		Size: 107.7 MB (107739292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1f97ab22dac5e8b60c0770634135f40d0eba00b3f8a5bd5de06c0b1f34676d`  
		Last Modified: Thu, 03 Mar 2022 23:25:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5bcd397c1a177db9a5bf9729e85c6d9a4a1a63fe402e4e054b80d981f46080`  
		Last Modified: Fri, 04 Mar 2022 00:05:47 GMT  
		Size: 6.9 MB (6930956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d87e4b5eaf820e1c3e543e167ee9e5db5c696e7841ea413858457b48b15e52c`  
		Last Modified: Thu, 10 Mar 2022 22:42:44 GMT  
		Size: 1.2 MB (1203783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16912306174cfd07dbe9e0cf2ce772627716514cc6055ff20659a6479af1548`  
		Last Modified: Thu, 10 Mar 2022 22:42:44 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:c485fc87f90e75e6405dc43fcc37c2ade914702f8ed320b630861e35ccd420f3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2888375962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a30a1f214b7532e10adc147e08b39a03f124d3aa580118b82b5e517d5aa4dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 13:17:25 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Mar 2022 13:17:26 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Mar 2022 13:17:27 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Mar 2022 13:17:28 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Mar 2022 13:19:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:19:56 GMT
ENV GOPATH=C:\go
# Wed, 09 Mar 2022 13:20:52 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Mar 2022 13:35:10 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 09 Mar 2022 13:38:26 GMT
RUN $url = 'https://dl.google.com/go/go1.17.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '85ccf2608dca6ea9a46b6538c9e75e7cf2aebdf502379843b248e26b8bb110be'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:38:28 GMT
WORKDIR C:\go
# Wed, 09 Mar 2022 18:27:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:27:12 GMT
ENV XCADDY_VERSION=v0.2.0
# Wed, 09 Mar 2022 18:27:14 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:27:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 09 Mar 2022 18:28:10 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 09 Mar 2022 18:28:11 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7705bbffd7dc00934e935de0e00e09a7b0da55d66c596622f094495478dd71`  
		Last Modified: Wed, 09 Mar 2022 14:04:13 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be7ff0bb187d149a5cf3c76e1ec444d0e07c6606f67b2c921c67ec91829ea03`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876223f25b257577440a80fdee021b43c33ce3c56be9a20b2ddeaede95240522`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991eea244b9c3a1849c84748425dd9e9fbf9ec359ad9329796131b929239ffa4`  
		Last Modified: Wed, 09 Mar 2022 14:04:11 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b4c7c9740eb99bf626b312aa69396db3d186c5bd0e092b01c078ca7248e386`  
		Last Modified: Wed, 09 Mar 2022 14:04:40 GMT  
		Size: 25.5 MB (25454695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f6c8a4d4848c21636a48a69a569a5372ec4890ea029f1f620dda76078bdcef`  
		Last Modified: Wed, 09 Mar 2022 14:04:09 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ac6d527939082add6d21652ba4888acc5a6e7607365168d8e61fb1485339cb`  
		Last Modified: Wed, 09 Mar 2022 14:04:10 GMT  
		Size: 313.6 KB (313592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37aeceb8c2e5bb3c500129bcf20c3f8aea8c68c353e6714a63a225ed1546e8a1`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d88cd595dc7580d72420b7288c52d4b32201045a13dda1a7b943d9a3468adef`  
		Last Modified: Wed, 09 Mar 2022 14:13:05 GMT  
		Size: 145.5 MB (145488847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be492983ee2b2c9128ce0c732c441ae5fbd203cdb71c94faa253c24b01750c90`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa7b09ca61eb1fbafacee427b430b0879ad4da23e62e430a3fe6a66f181f642`  
		Last Modified: Wed, 09 Mar 2022 18:30:00 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468156ad0978bb8919deb642986d1eb42a6e00ea9c3294930a526771ff120f59`  
		Last Modified: Wed, 09 Mar 2022 18:29:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13b17cf7c5867462fbdd3605d90437e19301e9a4d3d41cf90d2c1561c689c50`  
		Last Modified: Wed, 09 Mar 2022 18:29:58 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a1eca5bdf4cf75e747993b512d64c980670337f17807b0daeac5ec4bb41d26`  
		Last Modified: Wed, 09 Mar 2022 18:29:58 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8171f34c3c578dc87b1d9cc5911249fb1f03964352906509faf9492d07cca7c0`  
		Last Modified: Wed, 09 Mar 2022 18:29:58 GMT  
		Size: 1.6 MB (1647844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8937298adab332653decbee0cd826d99541996c5098544285d35579c47c367a`  
		Last Modified: Wed, 09 Mar 2022 18:29:58 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.14393.4886; amd64

```console
$ docker pull caddy@sha256:22cae5265f5cb60aa10f7a056b9281b4e61d0e14f16b5454f5b90f8c14e10e6f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6455446654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4079b70701d5a0ca0af10a7038d5f468c00e36871a95feb8e6e4926bda5e7d00`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 06 Jan 2022 14:33:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Jan 2022 19:14:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Jan 2022 23:34:03 GMT
ENV GIT_VERSION=2.23.0
# Tue, 11 Jan 2022 23:34:05 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 11 Jan 2022 23:34:06 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 11 Jan 2022 23:34:07 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 11 Jan 2022 23:35:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 11 Jan 2022 23:35:42 GMT
ENV GOPATH=C:\go
# Tue, 11 Jan 2022 23:36:45 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Jan 2022 23:57:30 GMT
ENV GOLANG_VERSION=1.17.6
# Wed, 12 Jan 2022 00:01:53 GMT
RUN $url = 'https://dl.google.com/go/go1.17.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '5bf8f87aec7edfc08e6bc845f1c30dba6de32b863f89ae46553ff4bbcc1d4954'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 12 Jan 2022 00:01:55 GMT
WORKDIR C:\go
# Wed, 12 Jan 2022 06:32:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jan 2022 06:32:49 GMT
ENV XCADDY_VERSION=v0.2.0
# Wed, 12 Jan 2022 06:32:50 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 12 Jan 2022 06:32:51 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 12 Jan 2022 06:33:57 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 12 Jan 2022 06:33:58 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8428508ffd63b4af1ba690ec41e82a116f10ec6c3fb70962348f5448d42e5835`  
		Size: 2.2 GB (2208216859 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9b5116c05ddf6ecb5a348f7628e3f3264afbb9909d86798316dbaff4a0e991a2`  
		Last Modified: Tue, 11 Jan 2022 19:35:13 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2caa59a1aaa1c092020bbca2ed4bb1396365f4d9d04ddbbd111ee689414c97a`  
		Last Modified: Wed, 12 Jan 2022 00:35:16 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9fe19533bf1afd7f80fd9cf407f00011eff59836d40dcceb1896e75ea99bf5`  
		Last Modified: Wed, 12 Jan 2022 00:35:13 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40700bafb918466fc1727b2e59ec5eb21d347affb09989cc72ac6db12220b882`  
		Last Modified: Wed, 12 Jan 2022 00:35:12 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3180faaeb4219e7d41bb57faeebe12d142e8e246bac5ab81c8ef38499116de13`  
		Last Modified: Wed, 12 Jan 2022 00:35:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6189cfcbd5a7447e171b486da44213e8ff4721ecbf15998668c0b32e6fb06aaa`  
		Last Modified: Wed, 12 Jan 2022 00:35:18 GMT  
		Size: 25.4 MB (25440280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4766ed70813b67e83228fa314c288fe9a1998bb85cbbd29f2a4b0518e49a7c15`  
		Last Modified: Wed, 12 Jan 2022 00:35:09 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8f2e04b601edd119e847cbb2468052ab4681cd44bf4e9bbdf9b6c3f792d0ae`  
		Last Modified: Wed, 12 Jan 2022 00:35:09 GMT  
		Size: 306.6 KB (306585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef103850c637e1ce1f8d175e0c4b5c7d6c2a3a29d2b8ad15bed8eab49be3dde0`  
		Last Modified: Wed, 12 Jan 2022 00:39:29 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce1f406ac407910a0724e1fbad6ed8772a277ce69316a98a2defcebb5320504`  
		Last Modified: Wed, 12 Jan 2022 00:40:03 GMT  
		Size: 149.8 MB (149846909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdefe1352ad86026fe87510dd97f9a9acdbb5a700fc6a8aea2bd6eaa3194bd6`  
		Last Modified: Wed, 12 Jan 2022 00:39:28 GMT  
		Size: 1.6 KB (1562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1578c0afb3c1729e44264a61a125be686ed8e738b033a03917b80f62aea0ed46`  
		Last Modified: Wed, 12 Jan 2022 06:35:55 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0d89ba8c66caec659fce7ea59e230983c2e8129e3026228cce6945904233cf`  
		Last Modified: Wed, 12 Jan 2022 06:35:53 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e135d2e9e9a157d6d87f8f0e5e9cf6aef249cd9aac5e2b4313784e2d31664990`  
		Last Modified: Wed, 12 Jan 2022 06:35:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715ab69f5d21664707eee604a40f003fbd665f65c14431d564a82a614b277496`  
		Last Modified: Wed, 12 Jan 2022 06:35:53 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833db9ca0e9e1914a35515e476460cdd0bcc36174f85c13dd8646945c5199cde`  
		Last Modified: Wed, 12 Jan 2022 06:35:53 GMT  
		Size: 1.6 MB (1631613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c57f5273b431c8d65b59b81e63af176c5126e1b0d33f4d7b4ece422a1e01562`  
		Last Modified: Wed, 12 Jan 2022 06:35:53 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:81586ffc8035d6323a8f32f47db99a14c976beeeaba313cee4b752d63944db5b
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
$ docker pull caddy@sha256:9c6a77c878ea39bd367c8c7e73f1a75a6ce97101bef0f3de7e288934b4de519e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121354364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c3a82ad51f9b44b272a32de82576c64480a940db9877dd465101c921e11593`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:21:45 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 04:21:46 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 04:21:47 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 01:05:33 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 01:08:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 01:08:13 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 01:08:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 01:08:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 01:08:14 GMT
WORKDIR /go
# Fri, 04 Mar 2022 04:22:25 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 04 Mar 2022 04:22:25 GMT
ENV XCADDY_VERSION=v0.2.0
# Fri, 04 Mar 2022 04:22:26 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 04 Mar 2022 04:22:26 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 04 Mar 2022 04:22:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 04 Mar 2022 04:22:27 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 04 Mar 2022 04:22:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666ba61612fd7c93393f9a5bc1751d8a9929e32d51501dba691da9e8232bc87b`  
		Last Modified: Tue, 30 Nov 2021 04:36:04 GMT  
		Size: 282.2 KB (282159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed8ca4862056a130f714accb3538decfa0663fec84e635d8b5a0a3305353dee`  
		Last Modified: Tue, 30 Nov 2021 04:36:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141c1ce2f203145a20c1b4550c662f943266dc7dbf7e15ee911b06456e2326da`  
		Last Modified: Fri, 04 Mar 2022 01:21:28 GMT  
		Size: 110.2 MB (110186591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4c7319106ffbcda864c88220ef7a19e3da3b571fa08e0be968efe7fbd9465f`  
		Last Modified: Fri, 04 Mar 2022 01:21:14 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0f327525fd9ac01a04ccd2c1530800b0c51b68d8821a2904e3d066d8663b3f`  
		Last Modified: Fri, 04 Mar 2022 04:22:46 GMT  
		Size: 6.8 MB (6821521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd85b87242bfb046d67955057b47bfdc6f774636e6b8334022ed51fe020a6301`  
		Last Modified: Fri, 04 Mar 2022 04:22:45 GMT  
		Size: 1.2 MB (1244966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32b29093c0b4e0e55e5212230f0fda6566f59ae3e6f91d6ae6b39363b0e7860`  
		Last Modified: Fri, 04 Mar 2022 04:22:45 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:f7e1a9b85365f550da1a0a03bbc6f0dc1c5930d86fcb7e857919ed50708462d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115838871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71a25849e386c048c58fcafd1884613238beacc8243d9fcdddddddbd10b458a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 02:32:18 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 02:32:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 02:32:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 22:50:05 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 03 Mar 2022 22:53:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 03 Mar 2022 22:53:52 GMT
ENV GOPATH=/go
# Thu, 03 Mar 2022 22:53:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 22:53:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 03 Mar 2022 22:53:54 GMT
WORKDIR /go
# Thu, 03 Mar 2022 23:28:42 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:49:51 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:49:52 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 22:49:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:49:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:49:55 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:49:55 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228ad0256439cce3fe9db355991b0557f55241d8cca8690f4f741e1c2d8fb8b9`  
		Last Modified: Tue, 30 Nov 2021 02:47:28 GMT  
		Size: 282.1 KB (282105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cab2a064767512d7d354e806cbd8b24ffefc15e06eeb7d4b127e7f6cddb6b40`  
		Last Modified: Tue, 30 Nov 2021 02:47:28 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798ddefed71bfdadb9d2b02c26fb7579e437fcf60f8af3f7cefed7967580d7da`  
		Last Modified: Thu, 03 Mar 2022 23:08:07 GMT  
		Size: 105.1 MB (105068635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7451a2cdc06b1d637a7e3849503cd56318bc1eb291dc792a6294cec777a31980`  
		Last Modified: Thu, 03 Mar 2022 23:06:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3489c6c0bcd6d649e4760550c8033a06b697ff4490644c130dde6501db25ab26`  
		Last Modified: Thu, 03 Mar 2022 23:29:55 GMT  
		Size: 6.7 MB (6677482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6889976625624adb9a9c5b111609959fe4da102919177fa9c53a23d173175d6`  
		Last Modified: Thu, 10 Mar 2022 22:51:59 GMT  
		Size: 1.2 MB (1178508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79172ebfda03823b62d347d32a6755fe56f0f8809466f11895c5a7d7ae48c3b0`  
		Last Modified: Thu, 10 Mar 2022 22:51:58 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:06e29bc1ce4d22e988eca705e6e4faf2ec70661ffb2a448a334e8b557068dd68
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114698943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14dc63acb649973c1c8c9f6f76def65c297a511f53a12f94af418ebc1c8da64e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:10:37 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 04:10:39 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 04:10:39 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:51:53 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 00:55:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 00:55:09 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 00:55:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:55:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 00:55:12 GMT
WORKDIR /go
# Fri, 04 Mar 2022 06:45:24 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:57:52 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:57:53 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 22:57:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:57:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:57:56 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:57:56 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f21e2af73375430a6481f93a61f3df4f9de38c985f83b27293f8aace16d6b5`  
		Last Modified: Tue, 30 Nov 2021 04:33:33 GMT  
		Size: 281.2 KB (281248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cec97f9b59f8579851b3f2c1523c8a96065c591f5961858420e92bf9d424d2`  
		Last Modified: Tue, 30 Nov 2021 04:33:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edfb2fbd38ed3972211201867b2a8e18c8dc23b141d716828e9914c61276ecd`  
		Last Modified: Fri, 04 Mar 2022 01:19:22 GMT  
		Size: 104.9 MB (104853230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a4329e8253fda916ae04b5a3c4d217f5f24639ce303c8a3f2b24588f490196`  
		Last Modified: Fri, 04 Mar 2022 01:18:12 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c608e2c7ee3c9ef36153815e881ac6bc5cf7ff68862fcddf588d11054f20923`  
		Last Modified: Fri, 04 Mar 2022 06:46:39 GMT  
		Size: 6.0 MB (5952263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca89b858a1ebd99c4675cae20c8f5c5e60653a6d2a307ec0bcd6e2e3b448d087`  
		Last Modified: Thu, 10 Mar 2022 23:00:00 GMT  
		Size: 1.2 MB (1176718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9c6a4e7cfb70b12bfb81a4fced64fb3d181017de696421ab4178c208f5defa`  
		Last Modified: Thu, 10 Mar 2022 22:59:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:ee6d440f72726b2d9d29a604a97ab0cc23505e8eccc68c64133eba5da0ef12de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115495270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9fe816e095b9092b887d34923435e91de44876c56fc189162c309a48f541ca`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 01:54:59 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 01:55:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 01:55:01 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 02:29:42 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 02:31:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 02:31:06 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 02:31:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 02:31:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 02:31:09 GMT
WORKDIR /go
# Fri, 04 Mar 2022 03:10:53 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:39:34 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:39:34 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 22:39:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:39:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:39:38 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:39:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a89e8eeedd549875510e5e4e14010906a58878526814e6df25d14009856c6ff`  
		Last Modified: Tue, 30 Nov 2021 02:05:10 GMT  
		Size: 281.9 KB (281899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94645a83ff95687e6f078c140cfcac8def006923ed4019ef74fa189e6d9f0b14`  
		Last Modified: Tue, 30 Nov 2021 02:05:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caad3c9267df5b5261016d2d8843a47ffd88678a81f5e2363c426640adaf2029`  
		Last Modified: Fri, 04 Mar 2022 02:41:55 GMT  
		Size: 104.4 MB (104422515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e36f09527def3bbe5253cea2be9051532cf4a71f0df8fec8a85c922ce640c36`  
		Last Modified: Fri, 04 Mar 2022 02:41:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336ffb45c2b4e74ba78ba96c6f82f7fec126618bbacdc0fa27c7d3677b5aa6f1`  
		Last Modified: Fri, 04 Mar 2022 03:11:32 GMT  
		Size: 6.9 MB (6926057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acd88183c62587770b090ffe6a970e05212ee61f949af7bad8e6edcb5743f0a`  
		Last Modified: Thu, 10 Mar 2022 22:40:54 GMT  
		Size: 1.1 MB (1148678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb0f9bf906b045657c360d551af06aa0af8bee7cbeb2e646cafa48abc2ac878`  
		Last Modified: Thu, 10 Mar 2022 22:40:54 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:4a53d3e10c18d0855f3ec5c9ec6dfb598f1a562d0828ec62b238370646e46e8a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114325817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251761ef86f00954d0b3d990c694bdcc74f14f6488585eef034148425fed6f23`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 03:17:54 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 03:17:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 03:18:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:12:42 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 00:15:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Fri, 04 Mar 2022 00:15:47 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 00:15:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:15:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 00:15:58 GMT
WORKDIR /go
# Fri, 04 Mar 2022 07:20:10 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 04 Mar 2022 07:20:21 GMT
ENV XCADDY_VERSION=v0.2.0
# Fri, 04 Mar 2022 07:20:27 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 04 Mar 2022 07:20:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 04 Mar 2022 07:20:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 04 Mar 2022 07:20:51 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 04 Mar 2022 07:20:57 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28be42a6852cc2108ddba1e4252671ae20275780a6ff73b1038699f59da2ac20`  
		Last Modified: Tue, 30 Nov 2021 03:35:16 GMT  
		Size: 284.0 KB (284020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d744d6799a13f2f7a7f85e040ddf0cc8b671a7cc5572b7049c3e1da8139b349`  
		Last Modified: Tue, 30 Nov 2021 03:35:15 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3620d170b59e9b8337616ec72da9ade5c2471d3b0cf50e3a538e6171d5d813a4`  
		Last Modified: Fri, 04 Mar 2022 00:33:32 GMT  
		Size: 102.8 MB (102785250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bec6e3bcdb44b28a2f07f58bc175553abc87d573010ff47564a72aff7749eb5`  
		Last Modified: Fri, 04 Mar 2022 00:33:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75230c4358c070669508567379db20aa0f6acf5775eb391f81394cc567994d4`  
		Last Modified: Fri, 04 Mar 2022 07:21:55 GMT  
		Size: 7.3 MB (7321033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29c6375e4c4e1312ebfadd212ce4b17f7f002743d73d01fca882a24eba618ac`  
		Last Modified: Fri, 04 Mar 2022 07:21:54 GMT  
		Size: 1.1 MB (1120019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47ae1c41cc141d20ffc3fe6ecccea9ac5fb48eefdeab0dec835beb21c731ac4`  
		Last Modified: Fri, 04 Mar 2022 07:21:54 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:43996cf55b905a5c54ef7cc5f9192ec4077d75694985c130d4866c3c9a537109
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118763072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad0782969bd455fc3ed6f62197dd5e0686ae55f02024605d501e975ceaf4c99`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:07:57 GMT
RUN apk add --no-cache ca-certificates
# Tue, 30 Nov 2021 04:07:57 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 30 Nov 2021 04:07:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 23:09:57 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 03 Mar 2022 23:12:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 03 Mar 2022 23:12:29 GMT
ENV GOPATH=/go
# Thu, 03 Mar 2022 23:12:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 23:12:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 03 Mar 2022 23:12:29 GMT
WORKDIR /go
# Fri, 04 Mar 2022 00:05:09 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 10 Mar 2022 22:41:34 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 10 Mar 2022 22:41:35 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 10 Mar 2022 22:41:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Mar 2022 22:41:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 10 Mar 2022 22:41:36 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 10 Mar 2022 22:41:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66787da5af638f8523e4694d81d38c2ca7c0a262f4cb8d78c46f7d64833bbaa0`  
		Last Modified: Tue, 30 Nov 2021 04:17:43 GMT  
		Size: 282.4 KB (282378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406f41068af489d7950f1a75d72455e702ed7da98dad21d9267448257b6a2ddc`  
		Last Modified: Tue, 30 Nov 2021 04:17:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee9a2e8145f1c142e4295add6c8c87e35418763276db9058b5b7ed0cc175e80`  
		Last Modified: Thu, 03 Mar 2022 23:26:10 GMT  
		Size: 107.7 MB (107739292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1f97ab22dac5e8b60c0770634135f40d0eba00b3f8a5bd5de06c0b1f34676d`  
		Last Modified: Thu, 03 Mar 2022 23:25:57 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5bcd397c1a177db9a5bf9729e85c6d9a4a1a63fe402e4e054b80d981f46080`  
		Last Modified: Fri, 04 Mar 2022 00:05:47 GMT  
		Size: 6.9 MB (6930956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d87e4b5eaf820e1c3e543e167ee9e5db5c696e7841ea413858457b48b15e52c`  
		Last Modified: Thu, 10 Mar 2022 22:42:44 GMT  
		Size: 1.2 MB (1203783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16912306174cfd07dbe9e0cf2ce772627716514cc6055ff20659a6479af1548`  
		Last Modified: Thu, 10 Mar 2022 22:42:44 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:a4ace300fa0bb8e20564cf55f2e5b24c38f86b8cb8c1f57a3c64f014a6243d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:c485fc87f90e75e6405dc43fcc37c2ade914702f8ed320b630861e35ccd420f3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2888375962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a30a1f214b7532e10adc147e08b39a03f124d3aa580118b82b5e517d5aa4dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 13:17:25 GMT
ENV GIT_VERSION=2.23.0
# Wed, 09 Mar 2022 13:17:26 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 09 Mar 2022 13:17:27 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 09 Mar 2022 13:17:28 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 09 Mar 2022 13:19:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:19:56 GMT
ENV GOPATH=C:\go
# Wed, 09 Mar 2022 13:20:52 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Mar 2022 13:35:10 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 09 Mar 2022 13:38:26 GMT
RUN $url = 'https://dl.google.com/go/go1.17.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '85ccf2608dca6ea9a46b6538c9e75e7cf2aebdf502379843b248e26b8bb110be'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Mar 2022 13:38:28 GMT
WORKDIR C:\go
# Wed, 09 Mar 2022 18:27:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:27:12 GMT
ENV XCADDY_VERSION=v0.2.0
# Wed, 09 Mar 2022 18:27:14 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:27:14 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 09 Mar 2022 18:28:10 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 09 Mar 2022 18:28:11 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7705bbffd7dc00934e935de0e00e09a7b0da55d66c596622f094495478dd71`  
		Last Modified: Wed, 09 Mar 2022 14:04:13 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be7ff0bb187d149a5cf3c76e1ec444d0e07c6606f67b2c921c67ec91829ea03`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876223f25b257577440a80fdee021b43c33ce3c56be9a20b2ddeaede95240522`  
		Last Modified: Wed, 09 Mar 2022 14:04:12 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991eea244b9c3a1849c84748425dd9e9fbf9ec359ad9329796131b929239ffa4`  
		Last Modified: Wed, 09 Mar 2022 14:04:11 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b4c7c9740eb99bf626b312aa69396db3d186c5bd0e092b01c078ca7248e386`  
		Last Modified: Wed, 09 Mar 2022 14:04:40 GMT  
		Size: 25.5 MB (25454695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f6c8a4d4848c21636a48a69a569a5372ec4890ea029f1f620dda76078bdcef`  
		Last Modified: Wed, 09 Mar 2022 14:04:09 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ac6d527939082add6d21652ba4888acc5a6e7607365168d8e61fb1485339cb`  
		Last Modified: Wed, 09 Mar 2022 14:04:10 GMT  
		Size: 313.6 KB (313592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37aeceb8c2e5bb3c500129bcf20c3f8aea8c68c353e6714a63a225ed1546e8a1`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d88cd595dc7580d72420b7288c52d4b32201045a13dda1a7b943d9a3468adef`  
		Last Modified: Wed, 09 Mar 2022 14:13:05 GMT  
		Size: 145.5 MB (145488847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be492983ee2b2c9128ce0c732c441ae5fbd203cdb71c94faa253c24b01750c90`  
		Last Modified: Wed, 09 Mar 2022 14:12:20 GMT  
		Size: 1.5 KB (1523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa7b09ca61eb1fbafacee427b430b0879ad4da23e62e430a3fe6a66f181f642`  
		Last Modified: Wed, 09 Mar 2022 18:30:00 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468156ad0978bb8919deb642986d1eb42a6e00ea9c3294930a526771ff120f59`  
		Last Modified: Wed, 09 Mar 2022 18:29:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13b17cf7c5867462fbdd3605d90437e19301e9a4d3d41cf90d2c1561c689c50`  
		Last Modified: Wed, 09 Mar 2022 18:29:58 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a1eca5bdf4cf75e747993b512d64c980670337f17807b0daeac5ec4bb41d26`  
		Last Modified: Wed, 09 Mar 2022 18:29:58 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8171f34c3c578dc87b1d9cc5911249fb1f03964352906509faf9492d07cca7c0`  
		Last Modified: Wed, 09 Mar 2022 18:29:58 GMT  
		Size: 1.6 MB (1647844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8937298adab332653decbee0cd826d99541996c5098544285d35579c47c367a`  
		Last Modified: Wed, 09 Mar 2022 18:29:58 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:184338dab192cd97f7c61b66c021c5709b2418e4826182f553ae09099f5082a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2686; amd64
	-	windows version 10.0.14393.5006; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:7da0f90273e1961d9c38d26809f84d4ef3cdc9b4fc330a9cab22015d7c9e8228
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14856906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439af64db48912c0a446444aae0e357183264ff08e1154fa105d5ee082e0bf13`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:54:17 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 12 Nov 2021 21:54:18 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Fri, 12 Nov 2021 21:54:19 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 12 Nov 2021 21:54:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 12 Nov 2021 21:54:23 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:54:23 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 12 Nov 2021 21:54:23 GMT
ENV XDG_DATA_HOME=/data
# Fri, 12 Nov 2021 21:54:23 GMT
VOLUME [/config]
# Fri, 12 Nov 2021 21:54:24 GMT
VOLUME [/data]
# Fri, 12 Nov 2021 21:54:24 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Fri, 12 Nov 2021 21:54:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 12 Nov 2021 21:54:24 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 12 Nov 2021 21:54:24 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 12 Nov 2021 21:54:25 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 12 Nov 2021 21:54:25 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 12 Nov 2021 21:54:25 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 12 Nov 2021 21:54:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 12 Nov 2021 21:54:25 GMT
EXPOSE 80
# Fri, 12 Nov 2021 21:54:26 GMT
EXPOSE 443
# Fri, 12 Nov 2021 21:54:26 GMT
EXPOSE 2019
# Fri, 12 Nov 2021 21:54:26 GMT
WORKDIR /srv
# Fri, 12 Nov 2021 21:54:26 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ccae726125d77e2fd3891c69c8f663d5fe63d8ad4a67deb284e2c589334497`  
		Last Modified: Fri, 12 Nov 2021 21:54:48 GMT  
		Size: 301.5 KB (301497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de6a61c89acc2147364721befe6e6bf957963713d1ddc4bc6c4a35f7b4b4e0a`  
		Last Modified: Fri, 12 Nov 2021 21:54:48 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ed957bdc008c4cc475fcaeb053cdb7fbcc83f49184fca8013d87cf9d395518`  
		Last Modified: Fri, 12 Nov 2021 21:54:50 GMT  
		Size: 11.7 MB (11726445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae44c2d42ddcf77445d391f491713e6384b933553eb234ceb0d9b3e66c5b33f`  
		Last Modified: Fri, 12 Nov 2021 21:54:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:caa4910dc3572e3ba3888fda3f7f5ed69c8c575461d29e528a6b453c0ba90522
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14068833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358685e491b9f796f29e9b70a0a43f619fa034e7bcd995cf738d811cf8e4ebe9`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:07:54 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 12 Nov 2021 17:07:57 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Fri, 12 Nov 2021 17:07:57 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 12 Nov 2021 17:08:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 12 Nov 2021 17:08:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 17:08:04 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 12 Nov 2021 17:08:05 GMT
ENV XDG_DATA_HOME=/data
# Fri, 12 Nov 2021 17:08:05 GMT
VOLUME [/config]
# Fri, 12 Nov 2021 17:08:06 GMT
VOLUME [/data]
# Fri, 12 Nov 2021 17:08:06 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Fri, 12 Nov 2021 17:08:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 12 Nov 2021 17:08:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 12 Nov 2021 17:08:08 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 12 Nov 2021 17:08:08 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 12 Nov 2021 17:08:09 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 12 Nov 2021 17:08:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 12 Nov 2021 17:08:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 12 Nov 2021 17:08:10 GMT
EXPOSE 80
# Fri, 12 Nov 2021 17:08:10 GMT
EXPOSE 443
# Fri, 12 Nov 2021 17:08:11 GMT
EXPOSE 2019
# Fri, 12 Nov 2021 17:08:11 GMT
WORKDIR /srv
# Fri, 12 Nov 2021 17:08:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d466a8f7766a93ea57a37532240c4a8c0e21cdb1f731360b1d21022b74f840f1`  
		Last Modified: Fri, 12 Nov 2021 17:09:28 GMT  
		Size: 301.7 KB (301671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082eb2081a4e07ea8cd0a36b4c3e7fee48ac23e2f6e8b7f95659e9a7465012fb`  
		Last Modified: Fri, 12 Nov 2021 17:09:27 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3790fd0e6afb978b6d8b451eaea5ab3e59b48913548a910853b31bc234bfed1c`  
		Last Modified: Fri, 12 Nov 2021 17:09:35 GMT  
		Size: 11.1 MB (11125784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe30a92d02271e636688f49fc9e1b382f2836b2c4578c29a993dc5111eb0b927`  
		Last Modified: Fri, 12 Nov 2021 17:09:27 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:5211ef3cdd2abf233de36a5e914b3ea2a649f0ec2164e5c63dd96c0cf870004e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13852151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389ecbea3a7d6a7b6a98da18b9b565046f2629b6c4af69a7d20d5cabcd1562d5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 11:43:41 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 13 Nov 2021 11:43:44 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 13 Nov 2021 11:43:44 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 13 Nov 2021 11:43:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 13 Nov 2021 11:43:51 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 11:43:51 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 13 Nov 2021 11:43:51 GMT
ENV XDG_DATA_HOME=/data
# Sat, 13 Nov 2021 11:43:52 GMT
VOLUME [/config]
# Sat, 13 Nov 2021 11:43:52 GMT
VOLUME [/data]
# Sat, 13 Nov 2021 11:43:53 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 13 Nov 2021 11:43:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 13 Nov 2021 11:43:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 13 Nov 2021 11:43:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 13 Nov 2021 11:43:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 13 Nov 2021 11:43:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 13 Nov 2021 11:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 13 Nov 2021 11:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 13 Nov 2021 11:43:57 GMT
EXPOSE 80
# Sat, 13 Nov 2021 11:43:57 GMT
EXPOSE 443
# Sat, 13 Nov 2021 11:43:58 GMT
EXPOSE 2019
# Sat, 13 Nov 2021 11:43:58 GMT
WORKDIR /srv
# Sat, 13 Nov 2021 11:43:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5663fa07ca1dcac265e40e084d2e40771a9084e9b30309c275bf810e87a3b53a`  
		Last Modified: Sat, 13 Nov 2021 11:45:26 GMT  
		Size: 300.8 KB (300831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf8bc3ddae458c10861b1ef0a30a6c8e97ea3a7135680ced673a2532a4c043e`  
		Last Modified: Sat, 13 Nov 2021 11:45:25 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afb06d1223418bbdf22f64f5a3a57962ad6570d931f931ab8df015439fb0c7a`  
		Last Modified: Sat, 13 Nov 2021 11:45:33 GMT  
		Size: 11.1 MB (11106718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a00e0b33a8465343d1f7f61ffec47a7c7aaad34402170530d9e9ebbb4ac5665`  
		Last Modified: Sat, 13 Nov 2021 11:45:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:8c2b7f01f3d14048e888946dd85b972ac76d22490107d999f6df18399ab76f25
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13763680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e48a5247e105a4ecd7f6a7b3f6bfe21fe6633146de42ad9bd4197b3222b920d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 11:18:37 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 13 Nov 2021 11:18:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 13 Nov 2021 11:18:40 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 13 Nov 2021 11:18:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 13 Nov 2021 11:18:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 11:18:44 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 13 Nov 2021 11:18:45 GMT
ENV XDG_DATA_HOME=/data
# Sat, 13 Nov 2021 11:18:46 GMT
VOLUME [/config]
# Sat, 13 Nov 2021 11:18:47 GMT
VOLUME [/data]
# Sat, 13 Nov 2021 11:18:48 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 13 Nov 2021 11:18:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 13 Nov 2021 11:18:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 13 Nov 2021 11:18:51 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 13 Nov 2021 11:18:52 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 13 Nov 2021 11:18:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 13 Nov 2021 11:18:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 13 Nov 2021 11:18:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 13 Nov 2021 11:18:56 GMT
EXPOSE 80
# Sat, 13 Nov 2021 11:18:57 GMT
EXPOSE 443
# Sat, 13 Nov 2021 11:18:58 GMT
EXPOSE 2019
# Sat, 13 Nov 2021 11:18:59 GMT
WORKDIR /srv
# Sat, 13 Nov 2021 11:19:00 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e205c63fa7e1c7a1060c29f8600bf90d965a1d26a1ae313210de738d08649d0`  
		Last Modified: Sat, 13 Nov 2021 11:19:44 GMT  
		Size: 301.4 KB (301450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674f75736ea40598c6df0d5460f914bf940c50952e8f106cdb674f9d98e8c5bb`  
		Last Modified: Sat, 13 Nov 2021 11:19:44 GMT  
		Size: 5.8 KB (5750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e004593c132f71a51cbd6967cf29bac3fc607c79fa8d967253c2f79461442641`  
		Last Modified: Sat, 13 Nov 2021 11:19:45 GMT  
		Size: 10.7 MB (10738627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51900aef2f22db52e1c14e6dd7f645241d02abef12b8ef2b377595f11b77055b`  
		Last Modified: Sat, 13 Nov 2021 11:19:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:b47a92735f1a101ce7087f2fc6f8b33614226b32c4507de0de8a4b6b34d84504
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13429323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bbba192f1381ae73d2265be6a6b84d7539131fcc66399931bd66ff97ff83f5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 21:18:00 GMT
ADD file:4d45063079cb28a34f1e382fddb22f156ac99d5449aa05ed37cb653c1f7b80f2 in / 
# Fri, 12 Nov 2021 21:18:01 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 15:14:03 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 13 Nov 2021 15:14:24 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 13 Nov 2021 15:14:33 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 13 Nov 2021 15:14:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 13 Nov 2021 15:14:52 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 15:14:54 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 13 Nov 2021 15:14:58 GMT
ENV XDG_DATA_HOME=/data
# Sat, 13 Nov 2021 15:15:03 GMT
VOLUME [/config]
# Sat, 13 Nov 2021 15:15:05 GMT
VOLUME [/data]
# Sat, 13 Nov 2021 15:15:09 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 13 Nov 2021 15:15:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 13 Nov 2021 15:15:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 13 Nov 2021 15:15:19 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 13 Nov 2021 15:15:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 13 Nov 2021 15:15:26 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 13 Nov 2021 15:15:30 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 13 Nov 2021 15:15:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 13 Nov 2021 15:15:35 GMT
EXPOSE 80
# Sat, 13 Nov 2021 15:15:37 GMT
EXPOSE 443
# Sat, 13 Nov 2021 15:15:40 GMT
EXPOSE 2019
# Sat, 13 Nov 2021 15:15:42 GMT
WORKDIR /srv
# Sat, 13 Nov 2021 15:15:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:72940440c1ab65eca4d38846164719ffde4b147543cc658d041407a925b13368`  
		Last Modified: Fri, 12 Nov 2021 21:19:32 GMT  
		Size: 2.8 MB (2817467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aca7d05e49e358a035d0dd6f471c0d19419c9cc97646fff4e82578d2c488237`  
		Last Modified: Sat, 13 Nov 2021 15:16:26 GMT  
		Size: 303.6 KB (303607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc78b04675eccc541ab8678fe7221460039d23c40f04c02d41e150f256c4368`  
		Last Modified: Sat, 13 Nov 2021 15:16:25 GMT  
		Size: 5.8 KB (5828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f289e05d8a93edbe6667d481e3a61908205bf58c77aa2ddf18b09f740724a8cd`  
		Last Modified: Sat, 13 Nov 2021 15:16:28 GMT  
		Size: 10.3 MB (10302268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd68deeff259e1bcfa76db665a6a52747267383f87bb506b77fbb409529ae3c8`  
		Last Modified: Sat, 13 Nov 2021 15:16:25 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:5ac69c24193df6b0d9b0c13816ce3861b720b62721901b0eb7446bd41ae86a3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14240890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753d56e00623363d01fede6cee26039f1b7efc2f64fccec498168291c9b9ea6b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 04:01:37 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 13 Nov 2021 04:01:38 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 13 Nov 2021 04:01:38 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 13 Nov 2021 04:01:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 13 Nov 2021 04:01:42 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 04:01:42 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 13 Nov 2021 04:01:42 GMT
ENV XDG_DATA_HOME=/data
# Sat, 13 Nov 2021 04:01:42 GMT
VOLUME [/config]
# Sat, 13 Nov 2021 04:01:42 GMT
VOLUME [/data]
# Sat, 13 Nov 2021 04:01:42 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 13 Nov 2021 04:01:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 13 Nov 2021 04:01:44 GMT
EXPOSE 80
# Sat, 13 Nov 2021 04:01:44 GMT
EXPOSE 443
# Sat, 13 Nov 2021 04:01:44 GMT
EXPOSE 2019
# Sat, 13 Nov 2021 04:01:44 GMT
WORKDIR /srv
# Sat, 13 Nov 2021 04:01:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0267ca443b43155e255c1a3bb35bab8ac5b561ddc2d0e768868f13274c7ab32d`  
		Last Modified: Sat, 13 Nov 2021 04:02:28 GMT  
		Size: 301.9 KB (301922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9c9c616a8868c7845a4a9d56e876f1bf42c37dac31b80761370b9af366e4c1`  
		Last Modified: Sat, 13 Nov 2021 04:02:28 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0dfff2c7fb2b8bde893d14f4d66fe6d6e8bee6115e0f4f691f7698d17a51f7`  
		Last Modified: Sat, 13 Nov 2021 04:02:29 GMT  
		Size: 11.3 MB (11323710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc9ba4f178258a6de34c95f9f50fb0fd89e093f552c493cd511cfb5fc39a433`  
		Last Modified: Sat, 13 Nov 2021 04:02:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:f2de2d90885f8cb6d12c79d914e354b41f6bfebc22ba3390096ae69fac380cf5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2728251838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8705f493a3ce58fda2b9ada4d3d27639c9f13835f1fb8d85ecdf795e69dae46a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:20:26 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:20:27 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:21:52 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:21:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:21:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:21:55 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:21:56 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:21:57 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:21:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:21:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:22:00 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:22:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:22:02 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:22:05 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:22:06 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:22:07 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:23:12 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:23:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99d892d6329e540cd98b358cc2f8085a7e6579538de9b4afa3ce0d11a03116`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 365.4 KB (365439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fb2be6c676c8f3e743cd43ec6b238646cf9f8b89a6fb1bde29f9bb52a7296c`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9b968486191ed8bb4a6c85eb678e32bbb062d8998e636e7706431be6e25f51`  
		Last Modified: Wed, 09 Mar 2022 18:29:07 GMT  
		Size: 12.1 MB (12115400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63f0ecb87a49981ac55c8495d8beed3b58d3b15e31ff4ba1140b0176e551265`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5249439459c9b885575d1a0c5c0df8c3e99649414b3c09ef4054e22fab54b584`  
		Last Modified: Wed, 09 Mar 2022 18:29:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69ab39aec279710b6bf7b4581cafe49878e70beff74d4a5e342eea02e60ce60`  
		Last Modified: Wed, 09 Mar 2022 18:29:02 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb81ca26c7a917813faca1d4cb92e1f41e642701d1199c9811ae8f9294e5b6f`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f5adb02b69cdd17e3acff1b0ea61317020c331399b0cb57fa34da5c09956e3`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e95a1158bc8e4066b6eb4211e7e898c86431c53c76c4752dfd7ce0a15cfc48`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579759f42b06baed2eb773c9cf8d6709e48e71afc07751fb3d45f7e4df9d819a`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e477dc674aa75d9872e80416c27f642531913f63b1598f0920a821c8b6cb535c`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03c9bb84aaf51c973e2ae3990a6b45ac835195b5eaae35799354b2aee8dfc2e`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23add58da280a0f09c755eaccccd5ecc95dc65993558d933f499b4c3378c9f70`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e3da14e3fcc65b938eef87893e57b0daa81c012c8789265cd784fb2f3cfcf7`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34cb18e7475b74cb46643f516f65cbd77fa161c461d753b4e62e076f7b221e5`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbd804e2eb98213ed819900a23753f3f2d662eb72c30a86dbbb51bcecc3cebc`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49b05954d4ea193b3f85228739d529bbc2a811204d8b6e22440c97977addbdf`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a3a3abbfe3563eaed35b97ad1ed309a3f4e744f968d0b6f6deaf68211f2fc8`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53542589ba9c33b651da4be35de7384a168d4936d08bb046a632a4d644b46c9e`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 293.3 KB (293252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149ac7945e26171c6dfe9e316c21027eb072f4fd72819f8b80a32eada8275ae2`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.14393.5006; amd64

```console
$ docker pull caddy@sha256:7f8374457a1c63677174631c3a8ea273702e069b924b615f44292250b7e2d8c1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6289879706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba40202b27c7479ec2d1d1618860745715dbfcabf489c651e5f04e826c286f72`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sat, 05 Mar 2022 03:39:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Mar 2022 18:23:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:24:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:24:49 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:26:02 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:26:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:26:04 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:26:05 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:26:06 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:26:07 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:26:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:26:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:26:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:26:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:26:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:26:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:26:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:26:14 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:26:15 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:26:16 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:26:54 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:26:55 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0fe465a8df276d07bd592c9424c00276a476fb7f74be6f867256b07fba31212d`  
		Size: 2.2 GB (2207094901 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c66997424475af0399fffec7897bad20e40b8309c56761077b30f5d9495f4db3`  
		Last Modified: Wed, 09 Mar 2022 18:29:32 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31f3b05b8f63dd42b4881a4c3d384691cc281678a86e0836d0c32819a344b5d`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 345.5 KB (345470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9855b50f056bb89da3373dfb2c128c8cf2515840c723a9027f0c01bb0eb91d`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b715cda286f032f4b113aefacf8b42874e8bed4dbe0080772b9d6cc1e91fc4`  
		Last Modified: Wed, 09 Mar 2022 18:29:43 GMT  
		Size: 12.1 MB (12134708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e40c1797eb55c98999e616bff73129a77843c7cf7667787950662180cbd90b`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d12359d4309d649fc7f0131974324ede0eb7aa11d1cd6f5d47000f9e14363b`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1783134869b6be42026ea8457c2f07dcacd3e029eaa283e48e798ce94929111`  
		Last Modified: Wed, 09 Mar 2022 18:29:28 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7104f8aa42fca009aaea2d885dfc7a0ea9acd8b7670cd9a90929f355d29cb5bf`  
		Last Modified: Wed, 09 Mar 2022 18:29:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ee03e2f86a2587a31a03418808435e9804fd324f95c981776b71ac5541f122`  
		Last Modified: Wed, 09 Mar 2022 18:29:28 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617c8eb23f7d35a0012ac7a3ce817bb49edda99eb16da9e4a9e6897617ded26d`  
		Last Modified: Wed, 09 Mar 2022 18:29:27 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85694b0569ffdf58e2f716205756d0a9eab45456d0ef23c2bbc8cb5816b99c1a`  
		Last Modified: Wed, 09 Mar 2022 18:29:27 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe2abbbf56f3d370ddba372e974d4765e074ee94fa8b1e4037b1cbf9d4a1e04`  
		Last Modified: Wed, 09 Mar 2022 18:29:26 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d4deaae43ac0785c4ccfb22ba187f33035f3041d44d770e8864cab157c1fe8`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7c04adc036f7a25c1c5a61895ba945aac263098d741203cb43e6b3b32174ef`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582d555a149be3d9ce42e33942b905cc2c8b9ebdc0dd1de51709fd7276c1e3ae`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b57929590127351973d44b26f950891ee7b918dc352a68098193a5d4fce629`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71478b5420cbbbea1bb0a6e617445f903203fac8965dfc6e2c41932cbb7f2acb`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b709c8c0d2fb364fd66993072fd79d4d28cda233a5d991b74680a1f80b1563`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c82093ad8180c0667cf71cdf92b8ead740771d5f2f5efda695fc67b815056d9`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34076b974bce5f92149f3e2eb58dc898a74d7ca4c563c20c4308f51a3f25212`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 293.4 KB (293417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e27086943ac64711a35c0e493db7b82a4faa0d65d5e80a91104238aba4845e2`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:5f89b604764eb0c53217da81ffe958b02f108847507c400542ef623d0c3acb06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2686; amd64
	-	windows version 10.0.14393.5006; amd64

### `caddy:windowsservercore` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:f2de2d90885f8cb6d12c79d914e354b41f6bfebc22ba3390096ae69fac380cf5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2728251838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8705f493a3ce58fda2b9ada4d3d27639c9f13835f1fb8d85ecdf795e69dae46a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:20:26 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:20:27 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:21:52 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:21:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:21:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:21:55 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:21:56 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:21:57 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:21:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:21:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:22:00 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:22:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:22:02 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:22:05 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:22:06 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:22:07 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:23:12 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:23:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99d892d6329e540cd98b358cc2f8085a7e6579538de9b4afa3ce0d11a03116`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 365.4 KB (365439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fb2be6c676c8f3e743cd43ec6b238646cf9f8b89a6fb1bde29f9bb52a7296c`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9b968486191ed8bb4a6c85eb678e32bbb062d8998e636e7706431be6e25f51`  
		Last Modified: Wed, 09 Mar 2022 18:29:07 GMT  
		Size: 12.1 MB (12115400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63f0ecb87a49981ac55c8495d8beed3b58d3b15e31ff4ba1140b0176e551265`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5249439459c9b885575d1a0c5c0df8c3e99649414b3c09ef4054e22fab54b584`  
		Last Modified: Wed, 09 Mar 2022 18:29:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69ab39aec279710b6bf7b4581cafe49878e70beff74d4a5e342eea02e60ce60`  
		Last Modified: Wed, 09 Mar 2022 18:29:02 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb81ca26c7a917813faca1d4cb92e1f41e642701d1199c9811ae8f9294e5b6f`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f5adb02b69cdd17e3acff1b0ea61317020c331399b0cb57fa34da5c09956e3`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e95a1158bc8e4066b6eb4211e7e898c86431c53c76c4752dfd7ce0a15cfc48`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579759f42b06baed2eb773c9cf8d6709e48e71afc07751fb3d45f7e4df9d819a`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e477dc674aa75d9872e80416c27f642531913f63b1598f0920a821c8b6cb535c`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03c9bb84aaf51c973e2ae3990a6b45ac835195b5eaae35799354b2aee8dfc2e`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23add58da280a0f09c755eaccccd5ecc95dc65993558d933f499b4c3378c9f70`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e3da14e3fcc65b938eef87893e57b0daa81c012c8789265cd784fb2f3cfcf7`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34cb18e7475b74cb46643f516f65cbd77fa161c461d753b4e62e076f7b221e5`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbd804e2eb98213ed819900a23753f3f2d662eb72c30a86dbbb51bcecc3cebc`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49b05954d4ea193b3f85228739d529bbc2a811204d8b6e22440c97977addbdf`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a3a3abbfe3563eaed35b97ad1ed309a3f4e744f968d0b6f6deaf68211f2fc8`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53542589ba9c33b651da4be35de7384a168d4936d08bb046a632a4d644b46c9e`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 293.3 KB (293252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149ac7945e26171c6dfe9e316c21027eb072f4fd72819f8b80a32eada8275ae2`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.14393.5006; amd64

```console
$ docker pull caddy@sha256:7f8374457a1c63677174631c3a8ea273702e069b924b615f44292250b7e2d8c1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6289879706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba40202b27c7479ec2d1d1618860745715dbfcabf489c651e5f04e826c286f72`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sat, 05 Mar 2022 03:39:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Mar 2022 18:23:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:24:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:24:49 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:26:02 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:26:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:26:04 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:26:05 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:26:06 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:26:07 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:26:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:26:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:26:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:26:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:26:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:26:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:26:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:26:14 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:26:15 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:26:16 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:26:54 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:26:55 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0fe465a8df276d07bd592c9424c00276a476fb7f74be6f867256b07fba31212d`  
		Size: 2.2 GB (2207094901 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c66997424475af0399fffec7897bad20e40b8309c56761077b30f5d9495f4db3`  
		Last Modified: Wed, 09 Mar 2022 18:29:32 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31f3b05b8f63dd42b4881a4c3d384691cc281678a86e0836d0c32819a344b5d`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 345.5 KB (345470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9855b50f056bb89da3373dfb2c128c8cf2515840c723a9027f0c01bb0eb91d`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b715cda286f032f4b113aefacf8b42874e8bed4dbe0080772b9d6cc1e91fc4`  
		Last Modified: Wed, 09 Mar 2022 18:29:43 GMT  
		Size: 12.1 MB (12134708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e40c1797eb55c98999e616bff73129a77843c7cf7667787950662180cbd90b`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d12359d4309d649fc7f0131974324ede0eb7aa11d1cd6f5d47000f9e14363b`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1783134869b6be42026ea8457c2f07dcacd3e029eaa283e48e798ce94929111`  
		Last Modified: Wed, 09 Mar 2022 18:29:28 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7104f8aa42fca009aaea2d885dfc7a0ea9acd8b7670cd9a90929f355d29cb5bf`  
		Last Modified: Wed, 09 Mar 2022 18:29:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ee03e2f86a2587a31a03418808435e9804fd324f95c981776b71ac5541f122`  
		Last Modified: Wed, 09 Mar 2022 18:29:28 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617c8eb23f7d35a0012ac7a3ce817bb49edda99eb16da9e4a9e6897617ded26d`  
		Last Modified: Wed, 09 Mar 2022 18:29:27 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85694b0569ffdf58e2f716205756d0a9eab45456d0ef23c2bbc8cb5816b99c1a`  
		Last Modified: Wed, 09 Mar 2022 18:29:27 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe2abbbf56f3d370ddba372e974d4765e074ee94fa8b1e4037b1cbf9d4a1e04`  
		Last Modified: Wed, 09 Mar 2022 18:29:26 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d4deaae43ac0785c4ccfb22ba187f33035f3041d44d770e8864cab157c1fe8`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7c04adc036f7a25c1c5a61895ba945aac263098d741203cb43e6b3b32174ef`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582d555a149be3d9ce42e33942b905cc2c8b9ebdc0dd1de51709fd7276c1e3ae`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b57929590127351973d44b26f950891ee7b918dc352a68098193a5d4fce629`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71478b5420cbbbea1bb0a6e617445f903203fac8965dfc6e2c41932cbb7f2acb`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b709c8c0d2fb364fd66993072fd79d4d28cda233a5d991b74680a1f80b1563`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c82093ad8180c0667cf71cdf92b8ead740771d5f2f5efda695fc67b815056d9`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34076b974bce5f92149f3e2eb58dc898a74d7ca4c563c20c4308f51a3f25212`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 293.4 KB (293417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e27086943ac64711a35c0e493db7b82a4faa0d65d5e80a91104238aba4845e2`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:a3ba1d80239cc342421e0b3a6a6adba859191852e94c30047402f2ac1cc24407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull caddy@sha256:f2de2d90885f8cb6d12c79d914e354b41f6bfebc22ba3390096ae69fac380cf5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2728251838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8705f493a3ce58fda2b9ada4d3d27639c9f13835f1fb8d85ecdf795e69dae46a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Mar 2022 15:05:04 GMT
RUN Install update 1809-amd64
# Tue, 08 Mar 2022 19:31:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:20:26 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:20:27 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:21:52 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:21:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:21:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:21:55 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:21:56 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:21:57 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:21:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:21:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:22:00 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:22:01 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:22:02 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:22:03 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:22:05 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:22:06 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:22:07 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:23:12 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:23:13 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a6173b79e25f2ebc0ed51b0ac32a6f65ca5a3bbfcbeab8b74a6c24324121dea`  
		Size: 997.1 MB (997119751 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a42bef5ec276ee3f8dd3545bf050f4ab85c8191392884f5d5ad6af6ae6e2eed2`  
		Last Modified: Tue, 08 Mar 2022 20:01:19 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef99d892d6329e540cd98b358cc2f8085a7e6579538de9b4afa3ce0d11a03116`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 365.4 KB (365439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fb2be6c676c8f3e743cd43ec6b238646cf9f8b89a6fb1bde29f9bb52a7296c`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9b968486191ed8bb4a6c85eb678e32bbb062d8998e636e7706431be6e25f51`  
		Last Modified: Wed, 09 Mar 2022 18:29:07 GMT  
		Size: 12.1 MB (12115400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63f0ecb87a49981ac55c8495d8beed3b58d3b15e31ff4ba1140b0176e551265`  
		Last Modified: Wed, 09 Mar 2022 18:29:04 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5249439459c9b885575d1a0c5c0df8c3e99649414b3c09ef4054e22fab54b584`  
		Last Modified: Wed, 09 Mar 2022 18:29:03 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69ab39aec279710b6bf7b4581cafe49878e70beff74d4a5e342eea02e60ce60`  
		Last Modified: Wed, 09 Mar 2022 18:29:02 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb81ca26c7a917813faca1d4cb92e1f41e642701d1199c9811ae8f9294e5b6f`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f5adb02b69cdd17e3acff1b0ea61317020c331399b0cb57fa34da5c09956e3`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e95a1158bc8e4066b6eb4211e7e898c86431c53c76c4752dfd7ce0a15cfc48`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579759f42b06baed2eb773c9cf8d6709e48e71afc07751fb3d45f7e4df9d819a`  
		Last Modified: Wed, 09 Mar 2022 18:29:01 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e477dc674aa75d9872e80416c27f642531913f63b1598f0920a821c8b6cb535c`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03c9bb84aaf51c973e2ae3990a6b45ac835195b5eaae35799354b2aee8dfc2e`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23add58da280a0f09c755eaccccd5ecc95dc65993558d933f499b4c3378c9f70`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e3da14e3fcc65b938eef87893e57b0daa81c012c8789265cd784fb2f3cfcf7`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34cb18e7475b74cb46643f516f65cbd77fa161c461d753b4e62e076f7b221e5`  
		Last Modified: Wed, 09 Mar 2022 18:28:59 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbd804e2eb98213ed819900a23753f3f2d662eb72c30a86dbbb51bcecc3cebc`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49b05954d4ea193b3f85228739d529bbc2a811204d8b6e22440c97977addbdf`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a3a3abbfe3563eaed35b97ad1ed309a3f4e744f968d0b6f6deaf68211f2fc8`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53542589ba9c33b651da4be35de7384a168d4936d08bb046a632a4d644b46c9e`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 293.3 KB (293252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149ac7945e26171c6dfe9e316c21027eb072f4fd72819f8b80a32eada8275ae2`  
		Last Modified: Wed, 09 Mar 2022 18:28:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
