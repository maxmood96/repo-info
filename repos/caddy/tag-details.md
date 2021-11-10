<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `caddy`

-	[`caddy:2`](#caddy2)
-	[`caddy:2-alpine`](#caddy2-alpine)
-	[`caddy:2-builder`](#caddy2-builder)
-	[`caddy:2-builder-alpine`](#caddy2-builder-alpine)
-	[`caddy:2-builder-windowsservercore-1809`](#caddy2-builder-windowsservercore-1809)
-	[`caddy:2-builder-windowsservercore-ltsc2016`](#caddy2-builder-windowsservercore-ltsc2016)
-	[`caddy:2-windowsservercore`](#caddy2-windowsservercore)
-	[`caddy:2-windowsservercore-1809`](#caddy2-windowsservercore-1809)
-	[`caddy:2-windowsservercore-ltsc2016`](#caddy2-windowsservercore-ltsc2016)
-	[`caddy:2.4.6`](#caddy246)
-	[`caddy:2.4.6-alpine`](#caddy246-alpine)
-	[`caddy:2.4.6-builder`](#caddy246-builder)
-	[`caddy:2.4.6-builder-alpine`](#caddy246-builder-alpine)
-	[`caddy:2.4.6-builder-windowsservercore-1809`](#caddy246-builder-windowsservercore-1809)
-	[`caddy:2.4.6-builder-windowsservercore-ltsc2016`](#caddy246-builder-windowsservercore-ltsc2016)
-	[`caddy:2.4.6-windowsservercore`](#caddy246-windowsservercore)
-	[`caddy:2.4.6-windowsservercore-1809`](#caddy246-windowsservercore-1809)
-	[`caddy:2.4.6-windowsservercore-ltsc2016`](#caddy246-windowsservercore-ltsc2016)
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
$ docker pull caddy@sha256:b82736e58560e3c1591c6205ddd9f44a5a11edebb1341a2e8cfe05b2617daa47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `caddy:2` - linux; amd64

```console
$ docker pull caddy@sha256:85a8daaf3706e847da86d456fb722edacb72a32360d333febccbf208f08e2be6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14847925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332a21201a47e70a89875163c9e41f0e78d6514d6e64aae618c3e2cc79b5e35d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:19:30 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:19:31 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:22:07 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:22:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:22:12 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:22:12 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:22:12 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:22:12 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:22:13 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:22:13 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:22:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:22:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:22:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:22:15 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:22:16 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:22:16 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:22:16 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:22:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d9d63a262eb117d9f55cf667904b985eb6dd9830783f17146a17a107a7ee19`  
		Last Modified: Tue, 07 Sep 2021 19:20:03 GMT  
		Size: 301.0 KB (301044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d54a459a500730b7153882903986d92e877f472e9d6ead142fab9dcb6464e1`  
		Last Modified: Tue, 07 Sep 2021 19:20:04 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12929046016b5f7547cb262dd7e97132958593eff9f30a3062729ed87f5f764f`  
		Last Modified: Tue, 09 Nov 2021 00:22:50 GMT  
		Size: 11.7 MB (11726452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2abe024ef8ac2567e428b8c753253b9670be99dad8f46607c895df6577f60ee`  
		Last Modified: Tue, 09 Nov 2021 00:22:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:84282af6d453c14c7875598e935faa6d1e7605067a6a212f69227bed1b97ae91
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14060404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4a22469cd1950a4d76a71bd95254b6b70d97f1d46d0ab846d9561937d7cee8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:49:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:49:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:49:32 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:49:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:49:39 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:49:39 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:49:40 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:49:40 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:49:41 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:49:41 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:49:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:49:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:49:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:49:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:49:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:49:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:49:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:49:45 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:49:45 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:49:46 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:49:46 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:49:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f254033e1bbf10f9a1641b6005ee6ae290bdec377e00d2e5290e33dc0eb8f9b6`  
		Last Modified: Tue, 07 Sep 2021 19:51:17 GMT  
		Size: 301.2 KB (301188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28038de9754eec9aa2df09a34c0d7029c335199166de56398d21fb595fd289dd`  
		Last Modified: Tue, 07 Sep 2021 19:51:17 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d17cc2aea86ad912ecd44f746238a440abd651aacc69ff04dcfdfa5e93193bb`  
		Last Modified: Tue, 09 Nov 2021 00:51:15 GMT  
		Size: 11.1 MB (11125785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cde1922177a05c9ac9c3cdb88d2492158258e3ddc64a6168bf7aa3d2087c3f5`  
		Last Modified: Tue, 09 Nov 2021 00:51:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:fb17cbc78aa551976f55685ba43b474671da9323631920b2411ef3ba47986f62
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13843483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9933538b9e4061a71c69dda3c1ac39f499b0a0c09fc86871a60a60b72576e0c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:57:36 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:57:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:57:30 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:57:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:57:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:57:37 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:57:37 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:57:38 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:57:38 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:57:39 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:57:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:57:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:57:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:57:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:57:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:57:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:57:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:57:42 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:57:43 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:57:43 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:57:44 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:57:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98c39987cd6455919d7455feed9aba93a44659ef658fbef5d4d52500beddac5`  
		Last Modified: Tue, 07 Sep 2021 19:59:13 GMT  
		Size: 300.4 KB (300356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e223cb6b0d911c9cc6575c496bc4f96f1968db869a8a07694f3f49897920f264`  
		Last Modified: Tue, 07 Sep 2021 19:59:13 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d8001745b5a3dedaa6b3a2bef5234f8612ac3d942269d2e18abbc1bfae84c8`  
		Last Modified: Tue, 09 Nov 2021 00:59:12 GMT  
		Size: 11.1 MB (11106727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bfb11f4ca256c6f83e7d7f05fdc548ce544492b765b72bad8fff802e114ec0`  
		Last Modified: Tue, 09 Nov 2021 00:59:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:dcc03368e7ff328ba4159eca9d88c2cb33e3ef4d8aaf9cec550f4f924c032616
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13757357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fca8f72561cf76363cdb806b321face6a1c9831e94d96c4966828a26b19962b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 14 Oct 2021 01:35:26 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 14 Oct 2021 01:35:28 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:39:19 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:39:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:39:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:39:23 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:39:24 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:39:25 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:39:26 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:39:27 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:39:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:39:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:39:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:39:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:39:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:39:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:39:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:39:35 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:39:36 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:39:37 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:39:38 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:39:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdae6629f9c73c56d66409172a1dcab55f533f8b62eb70c990c8e2cabcd7695`  
		Last Modified: Thu, 14 Oct 2021 01:36:31 GMT  
		Size: 301.0 KB (300992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3c515fae4831ae5dd272bcc27d7d3d3011d0f880b795b0aed1ce8c389c96bf`  
		Last Modified: Thu, 14 Oct 2021 01:36:30 GMT  
		Size: 5.8 KB (5752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce648197b75d827f9704483ccbcc884912ffb6a25728a39ddd0f717c3d534a46`  
		Last Modified: Tue, 09 Nov 2021 00:40:20 GMT  
		Size: 10.7 MB (10738633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d3751262c3b44d86e469c50ed19d1a632a37d420e471e3653d9c26c8d51ba6`  
		Last Modified: Tue, 09 Nov 2021 00:40:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; ppc64le

```console
$ docker pull caddy@sha256:b1f36f28cb28be8e03baf5e564e8813cf57f65a907533db61acec3fc2ff7d337
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13423700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927f64bc8094cd853e2649145f44cf5cbc699568c2066c650c61db9865417dc5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:16:42 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:16:56 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 02:38:59 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 02:39:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 02:39:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 02:39:43 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 02:39:47 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 02:39:58 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 02:40:04 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 02:40:16 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 02:40:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 02:40:30 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 02:40:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 02:40:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 02:40:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 02:41:01 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 02:41:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 02:41:31 GMT
EXPOSE 80
# Tue, 09 Nov 2021 02:41:42 GMT
EXPOSE 443
# Tue, 09 Nov 2021 02:41:49 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 02:41:57 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 02:42:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d32e3566fcaa11540498ebdd9ecc55cd2e2dca73a6b62317657a9e75749272`  
		Last Modified: Tue, 07 Sep 2021 19:21:13 GMT  
		Size: 303.2 KB (303162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a831abca68890cbd7a89171bb93c9af5c1b102852f0f1f3326ff7c104ced90`  
		Last Modified: Tue, 07 Sep 2021 19:21:12 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef4a0928ede6ae0f23c1a955b08d450770842d163d8152b4ad7cb9333b4ac5b`  
		Last Modified: Tue, 09 Nov 2021 02:43:36 GMT  
		Size: 10.3 MB (10302268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6dff47d769c4013cb3ed7545b165cd303bac49d09576d80c78bfa8d9353b1bb`  
		Last Modified: Tue, 09 Nov 2021 02:43:34 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; s390x

```console
$ docker pull caddy@sha256:7ceecb66639b47e4acb3acc566018228f83534b5a49f4a5306f4a6ae995cd13f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14234623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82585988e83eb76f3ebc0d2bb5323c9663491e28faa0819aa54296c142e686b3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:41:29 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:41:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:41:22 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:41:25 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:41:26 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:41:26 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:41:26 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:41:26 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:41:27 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:41:27 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:41:27 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:41:27 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:41:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9c7d5d2c4319fc2386cc1a009e57751b8d7a7d807ae0e867e4d6273e06731d`  
		Last Modified: Tue, 07 Sep 2021 19:42:43 GMT  
		Size: 301.5 KB (301462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c7b669e195c7cce7cf6d957130645125c1171c464622ceaa01378d18f24e37`  
		Last Modified: Tue, 07 Sep 2021 19:42:43 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931bdaaeb048d3dff8468154aa9eceea8e363d63dc61208df60553535bfe8f85`  
		Last Modified: Tue, 09 Nov 2021 00:42:20 GMT  
		Size: 11.3 MB (11323714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f913866909777fce146b3d1c6a81b811018e4bd5ba8ecd4d29168eb9dcced`  
		Last Modified: Tue, 09 Nov 2021 00:42:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.17763.2300; amd64

```console
$ docker pull caddy@sha256:4a8d9dccf760a0249237dfcf9726c0eb1b06e0b19f5ff67cf8718f8da29507c5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718934999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea4590fabf41404b64c9e90299fd322ac88350fd817d631f26264b5915ed362`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:12:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Nov 2021 20:12:21 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:13:18 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Nov 2021 20:13:19 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Nov 2021 20:13:20 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Nov 2021 20:13:21 GMT
VOLUME [c:/config]
# Wed, 10 Nov 2021 20:13:22 GMT
VOLUME [c:/data]
# Wed, 10 Nov 2021 20:13:23 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 10 Nov 2021 20:13:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Nov 2021 20:13:25 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Nov 2021 20:13:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Nov 2021 20:13:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Nov 2021 20:13:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Nov 2021 20:13:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Nov 2021 20:13:30 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Nov 2021 20:13:31 GMT
EXPOSE 80
# Wed, 10 Nov 2021 20:13:32 GMT
EXPOSE 443
# Wed, 10 Nov 2021 20:13:33 GMT
EXPOSE 2019
# Wed, 10 Nov 2021 20:14:19 GMT
RUN caddy version
# Wed, 10 Nov 2021 20:14:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b6e8b6a9caee6f47bdb32f6ec53fd2836fc02cddea3324c72caf380622fc31`  
		Last Modified: Wed, 10 Nov 2021 20:20:37 GMT  
		Size: 370.6 KB (370576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0308f92ecf7a222e22b826cf5c198551ffc380b76ee3e8de67da904b4b02f873`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05df7693285564a1ff855781db06d1dab2fa702b5492fd55461fc675cefb47b6`  
		Last Modified: Wed, 10 Nov 2021 20:20:50 GMT  
		Size: 12.1 MB (12127869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a1d26d8d7789115491377813de4a8a0c15aa4772e3b22b229a4a061f4994d5`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766e31d6b0534ea731f651ccd59e3397360e7878802aaf90257635b0edd37086`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b6f52680a8e584e06bb957343f7acef41f8863af076fed0c94c583f6a6a8ea`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3be75f11ed2b624d7b0d85454d91e6ba425c4b11d179b44611f0353c75976a5`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bb0fed8a1d238828c7b967ddc9453e83dc38e811f50de90a87ca4a79677e3e`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3343adb9cf1bed7b331007eea1fb0bfdcdcc2a11c2c295d513a73d451d338298`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655ad263ab440756e44a5b758408a577f4ba4e960ae9daec72945afc3047553f`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09b8e61a4bbdc190857116fd8fc09cd71a5409e0bf984c7a033272b2ef5f5bb`  
		Last Modified: Wed, 10 Nov 2021 20:20:32 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9723996732fa25ff5ef95b4bd85c9ddf6dfd27408fe9e220bf0156031ade487d`  
		Last Modified: Wed, 10 Nov 2021 20:20:32 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d58c78cd1d1a8562bd34f68b10ada8622f98bf19ad87174e2a3810657e48e70`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67885c8112bf51b21d408141b4bf3b2e13f08f96cdcd873dc6ca1310bdf08f65`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77274081e32b6ce8f84a136cb45008f07cd542a8f2fa0cb8a355331280e27248`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acafd6faed9e989da5b7ca4bcf5d704b15d86d0b5076b645224a578b5453eb61`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109d2337e42e4f8cfc28c01475b5d1ab49d1e776006c622915ec2166c8fead72`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ee8d0bd71b0b4f05c46aa89f1434f50b4685f23ab7e0e092ae5f46e1d150ad`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd8ebab410bbbe5d576ac2f9ec8f4f2b9d251ae4a307bc8c11bb47165553f63`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 290.2 KB (290194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a550a1217bcfc790088e7a6d4f32ebdea15bae25f297c4683cb3dfc3e6c72e4d`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.14393.4770; amd64

```console
$ docker pull caddy@sha256:2c091f3638b3d3948ffa8c2d95a9be662e858768ffc52e366872371a68d003a1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6285957464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fb2d13bfaf3ee5703b28aa6d939cbfac5b14658e1e3e91bbae594e1c4b22a2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:15:34 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Nov 2021 20:15:35 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:16:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Nov 2021 20:16:39 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Nov 2021 20:16:40 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Nov 2021 20:16:41 GMT
VOLUME [c:/config]
# Wed, 10 Nov 2021 20:16:42 GMT
VOLUME [c:/data]
# Wed, 10 Nov 2021 20:16:43 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 10 Nov 2021 20:16:44 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Nov 2021 20:16:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Nov 2021 20:16:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Nov 2021 20:16:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Nov 2021 20:16:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Nov 2021 20:16:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Nov 2021 20:16:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Nov 2021 20:16:50 GMT
EXPOSE 80
# Wed, 10 Nov 2021 20:16:51 GMT
EXPOSE 443
# Wed, 10 Nov 2021 20:16:52 GMT
EXPOSE 2019
# Wed, 10 Nov 2021 20:17:30 GMT
RUN caddy version
# Wed, 10 Nov 2021 20:17:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224cfcc2d1317d73465188f71867febbba9a64bbfcdf83b35bccd662bdb25748`  
		Last Modified: Wed, 10 Nov 2021 20:21:11 GMT  
		Size: 366.8 KB (366836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98f673e7fe75a29f4060341dab79e20ad059162395f10fb1fc2504379d12f22`  
		Last Modified: Wed, 10 Nov 2021 20:21:10 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6dc3d9f8e8e85985894d372a912cae2cbc64cc10540262498597bbe8cad8c31`  
		Last Modified: Wed, 10 Nov 2021 20:21:24 GMT  
		Size: 12.2 MB (12158174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197a3f340985e5e76e3ae77fcbb9e208f521abbad0cfb8921d27d4afe569f280`  
		Last Modified: Wed, 10 Nov 2021 20:21:13 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1443a981044b58af1bae85624fffe4dde7c1759e6a5f930ddaf2eb70bc3185dd`  
		Last Modified: Wed, 10 Nov 2021 20:21:10 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1b023614dd84860e7a4fdd1855131b5478b9b747a40fc9383467934e48e310`  
		Last Modified: Wed, 10 Nov 2021 20:21:09 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daca4ab6367b318ae3a2df27bbe0c53c12ee1a0196fc4f43a43ec47acd74c7c`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a288866cea4075f0f825973ce9d3369dd9411f73c325ed870a5233b383476dbc`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea1c63b1b4cb8f39b59025d926f384679d17bb660eceafe7f7c9418dcdfad61`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b25f60f98964a2d03947e1dac0b01388ad6c9c65497e546f8efe7f2fdcd35e`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d10f21fe32d5dd37a74db003c1119b2aaba639690b10ad4c46d22e2699140fc`  
		Last Modified: Wed, 10 Nov 2021 20:21:06 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4bd5845100c889806835753480fb0016610fbfab35d197c6aa641d73c114ed`  
		Last Modified: Wed, 10 Nov 2021 20:21:06 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190767770423c20b77f963553559cfa26d18b490228ad11c4f9fcf62e6dcefd7`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab0412df33f87a4e77ce1ef8afc68a04cd9a9a56ce9a21e3494f4e4f7c1083a`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80edcc113a751c789aee343b18fdb12c9099cd642cf099ab6a962c7cb0bce8b`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d513b74afabeb0e8050ca955cdf8b72040cabc21350ab394862808bd4382649`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc99c5e78f676bc2fed853c2d43f71dedcbf29fe3a6f69f5d0bc1eabca7f8e98`  
		Last Modified: Wed, 10 Nov 2021 20:21:04 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1532dfe2f3d7f9a4d2eed5ac842a7b54e160fb4d856388e1153d0c6488bab749`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c6594f3623b09c0359fe4347b1981678cebb55cebad4bd683d4bc059e0a201`  
		Last Modified: Wed, 10 Nov 2021 20:21:04 GMT  
		Size: 316.3 KB (316295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c07c5e836014edc4e052889ecbe945aa470b434f2563726bd4f9684da37bfc1`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:dbc76d658f90c3ce8f96d6a3ccc918d1694c586003eae68a6cf2282ce2ecf2ef
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
$ docker pull caddy@sha256:85a8daaf3706e847da86d456fb722edacb72a32360d333febccbf208f08e2be6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14847925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332a21201a47e70a89875163c9e41f0e78d6514d6e64aae618c3e2cc79b5e35d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:19:30 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:19:31 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:22:07 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:22:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:22:12 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:22:12 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:22:12 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:22:12 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:22:13 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:22:13 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:22:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:22:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:22:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:22:15 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:22:16 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:22:16 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:22:16 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:22:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d9d63a262eb117d9f55cf667904b985eb6dd9830783f17146a17a107a7ee19`  
		Last Modified: Tue, 07 Sep 2021 19:20:03 GMT  
		Size: 301.0 KB (301044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d54a459a500730b7153882903986d92e877f472e9d6ead142fab9dcb6464e1`  
		Last Modified: Tue, 07 Sep 2021 19:20:04 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12929046016b5f7547cb262dd7e97132958593eff9f30a3062729ed87f5f764f`  
		Last Modified: Tue, 09 Nov 2021 00:22:50 GMT  
		Size: 11.7 MB (11726452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2abe024ef8ac2567e428b8c753253b9670be99dad8f46607c895df6577f60ee`  
		Last Modified: Tue, 09 Nov 2021 00:22:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:84282af6d453c14c7875598e935faa6d1e7605067a6a212f69227bed1b97ae91
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14060404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4a22469cd1950a4d76a71bd95254b6b70d97f1d46d0ab846d9561937d7cee8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:49:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:49:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:49:32 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:49:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:49:39 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:49:39 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:49:40 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:49:40 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:49:41 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:49:41 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:49:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:49:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:49:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:49:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:49:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:49:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:49:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:49:45 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:49:45 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:49:46 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:49:46 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:49:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f254033e1bbf10f9a1641b6005ee6ae290bdec377e00d2e5290e33dc0eb8f9b6`  
		Last Modified: Tue, 07 Sep 2021 19:51:17 GMT  
		Size: 301.2 KB (301188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28038de9754eec9aa2df09a34c0d7029c335199166de56398d21fb595fd289dd`  
		Last Modified: Tue, 07 Sep 2021 19:51:17 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d17cc2aea86ad912ecd44f746238a440abd651aacc69ff04dcfdfa5e93193bb`  
		Last Modified: Tue, 09 Nov 2021 00:51:15 GMT  
		Size: 11.1 MB (11125785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cde1922177a05c9ac9c3cdb88d2492158258e3ddc64a6168bf7aa3d2087c3f5`  
		Last Modified: Tue, 09 Nov 2021 00:51:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:fb17cbc78aa551976f55685ba43b474671da9323631920b2411ef3ba47986f62
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13843483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9933538b9e4061a71c69dda3c1ac39f499b0a0c09fc86871a60a60b72576e0c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:57:36 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:57:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:57:30 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:57:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:57:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:57:37 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:57:37 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:57:38 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:57:38 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:57:39 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:57:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:57:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:57:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:57:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:57:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:57:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:57:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:57:42 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:57:43 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:57:43 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:57:44 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:57:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98c39987cd6455919d7455feed9aba93a44659ef658fbef5d4d52500beddac5`  
		Last Modified: Tue, 07 Sep 2021 19:59:13 GMT  
		Size: 300.4 KB (300356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e223cb6b0d911c9cc6575c496bc4f96f1968db869a8a07694f3f49897920f264`  
		Last Modified: Tue, 07 Sep 2021 19:59:13 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d8001745b5a3dedaa6b3a2bef5234f8612ac3d942269d2e18abbc1bfae84c8`  
		Last Modified: Tue, 09 Nov 2021 00:59:12 GMT  
		Size: 11.1 MB (11106727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bfb11f4ca256c6f83e7d7f05fdc548ce544492b765b72bad8fff802e114ec0`  
		Last Modified: Tue, 09 Nov 2021 00:59:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:dcc03368e7ff328ba4159eca9d88c2cb33e3ef4d8aaf9cec550f4f924c032616
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13757357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fca8f72561cf76363cdb806b321face6a1c9831e94d96c4966828a26b19962b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 14 Oct 2021 01:35:26 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 14 Oct 2021 01:35:28 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:39:19 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:39:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:39:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:39:23 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:39:24 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:39:25 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:39:26 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:39:27 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:39:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:39:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:39:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:39:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:39:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:39:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:39:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:39:35 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:39:36 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:39:37 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:39:38 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:39:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdae6629f9c73c56d66409172a1dcab55f533f8b62eb70c990c8e2cabcd7695`  
		Last Modified: Thu, 14 Oct 2021 01:36:31 GMT  
		Size: 301.0 KB (300992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3c515fae4831ae5dd272bcc27d7d3d3011d0f880b795b0aed1ce8c389c96bf`  
		Last Modified: Thu, 14 Oct 2021 01:36:30 GMT  
		Size: 5.8 KB (5752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce648197b75d827f9704483ccbcc884912ffb6a25728a39ddd0f717c3d534a46`  
		Last Modified: Tue, 09 Nov 2021 00:40:20 GMT  
		Size: 10.7 MB (10738633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d3751262c3b44d86e469c50ed19d1a632a37d420e471e3653d9c26c8d51ba6`  
		Last Modified: Tue, 09 Nov 2021 00:40:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:b1f36f28cb28be8e03baf5e564e8813cf57f65a907533db61acec3fc2ff7d337
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13423700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927f64bc8094cd853e2649145f44cf5cbc699568c2066c650c61db9865417dc5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:16:42 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:16:56 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 02:38:59 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 02:39:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 02:39:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 02:39:43 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 02:39:47 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 02:39:58 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 02:40:04 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 02:40:16 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 02:40:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 02:40:30 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 02:40:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 02:40:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 02:40:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 02:41:01 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 02:41:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 02:41:31 GMT
EXPOSE 80
# Tue, 09 Nov 2021 02:41:42 GMT
EXPOSE 443
# Tue, 09 Nov 2021 02:41:49 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 02:41:57 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 02:42:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d32e3566fcaa11540498ebdd9ecc55cd2e2dca73a6b62317657a9e75749272`  
		Last Modified: Tue, 07 Sep 2021 19:21:13 GMT  
		Size: 303.2 KB (303162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a831abca68890cbd7a89171bb93c9af5c1b102852f0f1f3326ff7c104ced90`  
		Last Modified: Tue, 07 Sep 2021 19:21:12 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef4a0928ede6ae0f23c1a955b08d450770842d163d8152b4ad7cb9333b4ac5b`  
		Last Modified: Tue, 09 Nov 2021 02:43:36 GMT  
		Size: 10.3 MB (10302268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6dff47d769c4013cb3ed7545b165cd303bac49d09576d80c78bfa8d9353b1bb`  
		Last Modified: Tue, 09 Nov 2021 02:43:34 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:7ceecb66639b47e4acb3acc566018228f83534b5a49f4a5306f4a6ae995cd13f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14234623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82585988e83eb76f3ebc0d2bb5323c9663491e28faa0819aa54296c142e686b3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:41:29 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:41:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:41:22 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:41:25 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:41:26 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:41:26 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:41:26 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:41:26 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:41:27 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:41:27 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:41:27 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:41:27 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:41:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9c7d5d2c4319fc2386cc1a009e57751b8d7a7d807ae0e867e4d6273e06731d`  
		Last Modified: Tue, 07 Sep 2021 19:42:43 GMT  
		Size: 301.5 KB (301462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c7b669e195c7cce7cf6d957130645125c1171c464622ceaa01378d18f24e37`  
		Last Modified: Tue, 07 Sep 2021 19:42:43 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931bdaaeb048d3dff8468154aa9eceea8e363d63dc61208df60553535bfe8f85`  
		Last Modified: Tue, 09 Nov 2021 00:42:20 GMT  
		Size: 11.3 MB (11323714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f913866909777fce146b3d1c6a81b811018e4bd5ba8ecd4d29168eb9dcced`  
		Last Modified: Tue, 09 Nov 2021 00:42:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:ff70e636e338c1d1bf2761dc49582a08edc8e7edf86f6591bae3ede81eebcd6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:58018b2f6a30dbb45e39be3761a09af004a551296f8f92bf31bef97687b15742
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121074719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8dc98d3747bd25bdd8b095b563b0cfa728096f1be09b7e50f5d2f81dc350be4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Mon, 30 Aug 2021 21:44:05 GMT
RUN apk add --no-cache ca-certificates
# Mon, 30 Aug 2021 21:44:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 30 Aug 2021 21:44:06 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:20:44 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:22:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:22:49 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:22:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:22:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:22:50 GMT
WORKDIR /go
# Thu, 04 Nov 2021 20:51:38 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 20:51:38 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:22:21 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:22:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:22:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:22:24 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31adcdaf11c89113a810db23d523e549d634d7de695a72b0ce98a1f912101262`  
		Last Modified: Mon, 30 Aug 2021 22:01:00 GMT  
		Size: 281.5 KB (281508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b176561691ea11cfe541f3ee363a3aa67e3649eb3273bea62ebeea713eaecd`  
		Last Modified: Mon, 30 Aug 2021 22:00:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d416b4d4fcca0271f31d7d73ef5910b705bc9c7e6c47e2849f526c61323bba9`  
		Last Modified: Thu, 04 Nov 2021 20:33:02 GMT  
		Size: 110.1 MB (110106449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b6b52ae600093bcea2a88e347c180ddf79cf361a229c968ab134f79566115b`  
		Last Modified: Thu, 04 Nov 2021 20:32:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ce64c87030110c9e1fb28a88d6de9ab21bc642f56da365e029fef45bd40449`  
		Last Modified: Thu, 04 Nov 2021 20:52:00 GMT  
		Size: 6.6 MB (6626626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4745adbe391f6c84dabb01d0b9f46dcb4c3835b37d657188312f964bf2428113`  
		Last Modified: Tue, 09 Nov 2021 00:23:02 GMT  
		Size: 1.2 MB (1244972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29111d85c26db67c047d940076de17d7fa99ab44f4facbb7102429b421060b91`  
		Last Modified: Tue, 09 Nov 2021 00:23:02 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a321aa86f856c91169d31a96a1181ca0fb15d4fa785b01fd4f1db0a76ac5f438
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115556079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1759314115af8681edae8afa8c25d576e2bf7c430e2fcf6bdae1a6f520f4b6f5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Mon, 30 Aug 2021 21:49:40 GMT
RUN apk add --no-cache ca-certificates
# Mon, 30 Aug 2021 21:49:41 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 30 Aug 2021 21:49:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:50:01 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:53:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:53:24 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:53:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:53:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:53:27 GMT
WORKDIR /go
# Thu, 04 Nov 2021 21:26:48 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 21:26:48 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:50:03 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:50:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:50:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:50:07 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:50:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb221a547a2f49a13c3bbe14f37b0474b2066cece57c67c2fbc1fb07d89aad51`  
		Last Modified: Mon, 30 Aug 2021 22:04:54 GMT  
		Size: 281.7 KB (281671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2968f26f7f14fe309f1a7a85ad968b81a7daa93c078322a84eb5c4192326828`  
		Last Modified: Mon, 30 Aug 2021 22:04:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1662a83909f5aff655c7be6da1ffd97a579ec92c5839159187d230df4db0c304`  
		Last Modified: Thu, 04 Nov 2021 21:06:10 GMT  
		Size: 105.0 MB (104982787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247cd469be037fb4ffd6898dfee7159dc4dbb17525c62f11540b77badda787fe`  
		Last Modified: Thu, 04 Nov 2021 21:05:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52d5113b58e9eea7126b6573a103c6174f77e3f086440c6b60d013feeae55c9`  
		Last Modified: Thu, 04 Nov 2021 21:28:00 GMT  
		Size: 6.5 MB (6485880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053aa7bf00b68e2dd2854ce3cf420395833093ba5dbf21fcbe716d7c14129a82`  
		Last Modified: Tue, 09 Nov 2021 00:51:31 GMT  
		Size: 1.2 MB (1177578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba84a71092e7a8161d2aa6cb90f140a7a6a7ee304fd1143a4bedc91bdb8a3430`  
		Last Modified: Tue, 09 Nov 2021 00:51:30 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:898867984c20de5d0a90810f09c3aa0d59c45b55c878d65fa1986002494be562
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114460716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f422bda8d34cfaad33778dcbf74db88e84c362e26c97e5ecb7e52bc0aed977c2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Mon, 30 Aug 2021 23:51:38 GMT
RUN apk add --no-cache ca-certificates
# Mon, 30 Aug 2021 23:51:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 30 Aug 2021 23:51:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:00:39 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 21:03:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 21:03:56 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 21:03:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:03:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 21:03:59 GMT
WORKDIR /go
# Thu, 04 Nov 2021 22:24:32 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 22:24:32 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:58:01 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:58:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:58:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:58:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:58:05 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9417f62ae10851eaf03f096c21f2848fdfe2517baf1faffe0a25f4a1f9853e31`  
		Last Modified: Tue, 31 Aug 2021 00:14:21 GMT  
		Size: 280.8 KB (280829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15fcbf7d3458d8a294b9a3c72856e5e7ba1372b93f8fc485abecc73f5a8c9b6`  
		Last Modified: Tue, 31 Aug 2021 00:14:21 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83145a0dc91bcfd39d1372eacfa0b0edd49fbd853a8805d09bc3c801ec17707`  
		Last Modified: Thu, 04 Nov 2021 21:24:35 GMT  
		Size: 104.8 MB (104787212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56a13d9f75fefe8df6818c553071626370c07285a8579c71d061dd3958ab9e9`  
		Last Modified: Thu, 04 Nov 2021 21:09:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a883856d1a9eb72feb215725e23c34ff4e13cc0bdba2c76df4ff5a281950a34d`  
		Last Modified: Thu, 04 Nov 2021 22:25:46 GMT  
		Size: 5.8 MB (5785275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce6cdc3c3bebb2bf176add262391b9b35a554c02e1031b6809d950661a432fe`  
		Last Modified: Tue, 09 Nov 2021 00:59:28 GMT  
		Size: 1.2 MB (1176263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699c5f30dbc0681a9241c9e446110c0ff7a3228da9ef73377eddfec9167018af`  
		Last Modified: Tue, 09 Nov 2021 00:59:27 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:465390cedcb9fff08eb002c4722d69e56f05c3c60f953da3cfb449ae162140c6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115238050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eddb3be5e644425a129daa8ef25fa1990904790212c12c1037f9acff4e54e6d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Tue, 12 Oct 2021 19:50:31 GMT
RUN apk add --no-cache ca-certificates
# Tue, 12 Oct 2021 19:50:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 12 Oct 2021 19:50:33 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:44:49 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:46:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:46:13 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:46:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:46:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:46:16 GMT
WORKDIR /go
# Thu, 04 Nov 2021 21:13:57 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 21:13:58 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:39:47 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:39:47 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:39:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:39:51 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:39:51 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb74239f2a0c13b654df471372048f7785978cbe6bf5ddc6773d88218ad689f0`  
		Last Modified: Tue, 12 Oct 2021 19:56:27 GMT  
		Size: 281.5 KB (281470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8ec004bf6b17206854367316e34aa51b7f5ff2f447e6c66498b2922dfad207`  
		Last Modified: Tue, 12 Oct 2021 19:56:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2dd7c0ce8a9709408ba750c27f660c1821df16fc1588b83103c14f5c982410`  
		Last Modified: Thu, 04 Nov 2021 20:55:18 GMT  
		Size: 104.4 MB (104362226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51b802c83dca96aee9527f6b9430dfb8d84cc63a0dfb77abd3fc70b35661b68`  
		Last Modified: Thu, 04 Nov 2021 20:55:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b82d2b3afe06ceb5e9038414bd86eaa29b64d9ca539a8d7f0a9a97d89c0ec4`  
		Last Modified: Thu, 04 Nov 2021 21:14:36 GMT  
		Size: 6.7 MB (6733703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6348d8e1d75893311f870eec10215eaead24e452e1ad2a6ae81e2b276e3cca2`  
		Last Modified: Tue, 09 Nov 2021 00:40:33 GMT  
		Size: 1.1 MB (1148135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a51eb07dd20f1949799c418f754133ca1fc5b646673e8ac9d111563dbc589f0`  
		Last Modified: Tue, 09 Nov 2021 00:40:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:2336a18de17f2c4072c9c0307696854edf929dcb82a60b90f55259a69eeb600a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (114036993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b00aa91420fc4f22cea6aab5ff77b36da6f5a53aa4614f04c4434e09de4e6f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Tue, 31 Aug 2021 00:28:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 31 Aug 2021 00:29:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 31 Aug 2021 00:29:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:35:29 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 21:37:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 21:38:07 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 21:38:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:38:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 21:38:27 GMT
WORKDIR /go
# Thu, 04 Nov 2021 23:44:35 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 23:44:36 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 02:42:23 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 02:42:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 02:42:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 02:42:49 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 02:42:55 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4539d90ff594fe73c1a1e31b2230e539a965f33143a3c9fbd89507336ed283c2`  
		Last Modified: Tue, 31 Aug 2021 00:52:27 GMT  
		Size: 283.6 KB (283640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a17d0ec6ff5411e524016f0ac7033cf7a0a8935f7a5e299d4d7acaad208b26`  
		Last Modified: Tue, 31 Aug 2021 00:52:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34c4f0757f32d139833674c31fd061ecab0806960999b78a42e97fccf03c17b`  
		Last Modified: Thu, 04 Nov 2021 21:55:32 GMT  
		Size: 102.7 MB (102722966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f044c2212367ff5cf5f5f5c673ad6d3feae574970990f8f78507c3ac07e3640`  
		Last Modified: Thu, 04 Nov 2021 21:54:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428a3c7c0c1bff96a1ad7f93a7663935ca506020c92db68c2c71b978a2e6ed00`  
		Last Modified: Thu, 04 Nov 2021 23:45:27 GMT  
		Size: 7.1 MB (7097367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c99d2cd9325e8349becf942ed19b5842c0c2199ce5cbca707223e3419ebb52`  
		Last Modified: Tue, 09 Nov 2021 02:43:49 GMT  
		Size: 1.1 MB (1120017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2118cc3ec9b4efe4249b876ec149d807c563e41337b16031f2189b0934bb4744`  
		Last Modified: Tue, 09 Nov 2021 02:43:52 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:504417781112a6da613e5dbf96701f333e86c02c15ee528bcfc69a914cb5b99c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118475563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6cfef420950dbccc42ede323157843e6c2451cefbb4b472fc259ac9e90a0708`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Mon, 30 Aug 2021 21:44:33 GMT
RUN apk add --no-cache ca-certificates
# Mon, 30 Aug 2021 21:44:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 30 Aug 2021 21:44:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:42:32 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:44:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:44:06 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:44:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:44:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:44:07 GMT
WORKDIR /go
# Thu, 04 Nov 2021 21:16:26 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 21:16:27 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:41:36 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:41:36 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:41:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:41:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:41:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316d1588ef06afb0d7a96646bb3a1367bce295885797fd976945ed318a4eb9c`  
		Last Modified: Mon, 30 Aug 2021 21:59:27 GMT  
		Size: 281.9 KB (281927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e156a554eded13f9baa4042fb4d12b879560bebfd8aca837bf0b52669f7932`  
		Last Modified: Mon, 30 Aug 2021 21:59:26 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe04792d0475ac041009f3ca62bcc0dc03a26292d21b32216bc2f3e666c2d5b`  
		Last Modified: Thu, 04 Nov 2021 20:52:06 GMT  
		Size: 107.7 MB (107663718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6416455ccb8f772096f018fb9032102e6439950a45d68d4188fdfde5d9a87ded`  
		Last Modified: Thu, 04 Nov 2021 20:51:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6952a3ac2d6398e7268d236bf7d0cee103719b380aebea5fb6aabd2e45c04ed1`  
		Last Modified: Thu, 04 Nov 2021 21:17:06 GMT  
		Size: 6.7 MB (6722226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39fdad6edb5004df0acf851fcf3b0cf9d8cdfeaa9913d04f595517236869eef`  
		Last Modified: Tue, 09 Nov 2021 00:42:30 GMT  
		Size: 1.2 MB (1203510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0be2e59b91c38d78efc2f40a152bdd89dd964e653984267002b1453226e9d2e`  
		Last Modified: Tue, 09 Nov 2021 00:42:30 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.2300; amd64

```console
$ docker pull caddy@sha256:4d2914c283fcdb42d19719132d7efbfbfe7ad8af1d9cd5c071bf854233987587
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2878964819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b401c7e3582848bc6ccadc1c70895573764efb0f83732c2863411e9419c08c35`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 13:26:17 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Nov 2021 13:26:18 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Nov 2021 13:26:19 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Nov 2021 13:26:20 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Nov 2021 13:27:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:27:38 GMT
ENV GOPATH=C:\go
# Wed, 10 Nov 2021 13:28:31 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Nov 2021 13:28:32 GMT
ENV GOLANG_VERSION=1.17.3
# Wed, 10 Nov 2021 13:31:30 GMT
RUN $url = 'https://dl.google.com/go/go1.17.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e78684b955742e215926204afc6ed62b9d165b509e25a687d62902516f08726b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:31:35 GMT
WORKDIR C:\go
# Wed, 10 Nov 2021 20:17:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:17:50 GMT
ENV XCADDY_VERSION=v0.2.0
# Wed, 10 Nov 2021 20:17:51 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:17:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Nov 2021 20:18:44 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Nov 2021 20:18:45 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f32622fe466bd678a47b75fa13ebb7781336e6a776a22f424036aa8e91fe1d`  
		Last Modified: Wed, 10 Nov 2021 14:05:07 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d684ea4a6b52df2d3b5c7f7876e3b784ff1def8eb60f9637d920f4e0e7870b`  
		Last Modified: Wed, 10 Nov 2021 14:05:03 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ff61f0f89258dd1f49b766ef30baddd8f3e3821737778748ba95b52c1a480c`  
		Last Modified: Wed, 10 Nov 2021 14:05:03 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16dc9a497b44a664b28524686ca0e75c6a244af505429f54f80a6aaa96c7af9`  
		Last Modified: Wed, 10 Nov 2021 14:05:04 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e724f5e2b6e2fb2598ad100e7efa9cf30fe013f56537a5587d8e8868ae82d50`  
		Last Modified: Wed, 10 Nov 2021 14:05:09 GMT  
		Size: 25.4 MB (25446198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84e37bf01f689e54241d5e76695c5cbcc3313f3f8a85748e9d086c6cf3e4c3d`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f6ed9286b06435dae34f3d3e03f2c62a4415e3703740a83381b4ac0a3d1804`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 325.4 KB (325448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd53ef82415224427ba6005a3993a50da833e74dd65f413ede222760ab73155`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322051166b18395731c110a7ced59dc83924ac45736b482be8611e491ce9be22`  
		Last Modified: Wed, 10 Nov 2021 14:05:34 GMT  
		Size: 145.4 MB (145394728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7588b640c5b448c06e31f55936d39ebd92c0050d9b2daf5a86f09841d0ac6e68`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab8b7df216099a8c01f65cacfd0d07bfb8fe6ef211d5dbc6b897ceab643aa54`  
		Last Modified: Wed, 10 Nov 2021 20:21:41 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e1af14b4ab45cfdf867d71debb12ba16dc9770a11af54ec694004f8828280f`  
		Last Modified: Wed, 10 Nov 2021 20:21:38 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18305c1b79b992f30e786ccaa7379fba16154663b28f19d088c9b1750fe53f12`  
		Last Modified: Wed, 10 Nov 2021 20:21:38 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c926d89c22fc6adf4e181145a724ed23dacf28e12d58b7e7f75d69c4239ea2f0`  
		Last Modified: Wed, 10 Nov 2021 20:21:38 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb704654cf062fe78ae7674ea38cb7e81ac8f2b26f74c295489abf19dd4d206`  
		Last Modified: Wed, 10 Nov 2021 20:21:39 GMT  
		Size: 1.7 MB (1658702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da89e3439fa9c9e9d4cde6c4aca2fb1796d9dfceec37d31d351e2005a188b389`  
		Last Modified: Wed, 10 Nov 2021 20:21:38 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.14393.4770; amd64

```console
$ docker pull caddy@sha256:96a88b09cecf23cff2a8006ea25f1e037f50d01a9c74d2d3769f8bb228d2b768
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6450468916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fcd7b2f02771fd0b23831a7e603a01713fad078e5e205d745958ee47f638e5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 13:31:46 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Nov 2021 13:31:47 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Nov 2021 13:31:48 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Nov 2021 13:31:49 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Nov 2021 13:33:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:33:37 GMT
ENV GOPATH=C:\go
# Wed, 10 Nov 2021 13:34:34 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Nov 2021 13:34:35 GMT
ENV GOLANG_VERSION=1.17.3
# Wed, 10 Nov 2021 13:37:32 GMT
RUN $url = 'https://dl.google.com/go/go1.17.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e78684b955742e215926204afc6ed62b9d165b509e25a687d62902516f08726b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:37:37 GMT
WORKDIR C:\go
# Wed, 10 Nov 2021 20:18:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:18:53 GMT
ENV XCADDY_VERSION=v0.2.0
# Wed, 10 Nov 2021 20:18:54 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:18:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Nov 2021 20:19:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Nov 2021 20:19:56 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a0c69f83a30944f5afdc948b3583f1418f71f3ae5a02382610f0898eb501f9`  
		Last Modified: Wed, 10 Nov 2021 14:05:54 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e4bea9e4e2ccac41591b4aed9981453c554ca498a23d01a69638d6ccab7016`  
		Last Modified: Wed, 10 Nov 2021 14:05:52 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b36358e1913c99dc66fbbca2e4c0f8472796bf33ceeb7fdc02d2b7096b1208d`  
		Last Modified: Wed, 10 Nov 2021 14:05:52 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d071f5d45753629193f76196d769df9ff71ce3a39e5b10a16ff571cdb071a902`  
		Last Modified: Wed, 10 Nov 2021 14:05:52 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79602be6489be8a0e5e82221cae33eae5692897081a79bfe959604121e2d0a4`  
		Last Modified: Wed, 10 Nov 2021 14:06:20 GMT  
		Size: 25.4 MB (25448073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30d749fb8ba78fba5cce783b8cbe233632a2ba5965d4b67168111396620aaa0`  
		Last Modified: Wed, 10 Nov 2021 14:05:50 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f08b5963e19f3d28aa336d06434d4efec179b4b813e4aa4222ab064bc180f7`  
		Last Modified: Wed, 10 Nov 2021 14:05:50 GMT  
		Size: 354.9 KB (354902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f381a7ed29624957c6a0c2539069229be83423497216e9b19872996d3eace018`  
		Last Modified: Wed, 10 Nov 2021 14:05:49 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9184646a18b279b69062ae625cf768031d03c297beca44a465b8265af80e7116`  
		Last Modified: Wed, 10 Nov 2021 14:06:25 GMT  
		Size: 149.9 MB (149917271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e2acfda5cf05f260961ec16cee7c5c9e5573783c8298319e6b38846cb3b98b`  
		Last Modified: Wed, 10 Nov 2021 14:05:49 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f8275e6d67e00182a573a1fea89b6fbafd29fdd9e6991bec289907772e366`  
		Last Modified: Wed, 10 Nov 2021 20:21:59 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f675d50b479c34b5e127a7560cec6198d6c06464747188b22904543e0919ffe`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dba2d80865d737653a9a4ff2db1fcac88ce9bf3521d9e7f6dc8116fd16a99b`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272648eb620ef88b428e4aac8f782d100c4e64bb6f14073ee16b5b89a3b12967`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b51ab7213b8db3f0e51ace7c64b811e81a3d838148d7c41c3a58a9ffd1eb66`  
		Last Modified: Wed, 10 Nov 2021 20:21:58 GMT  
		Size: 1.6 MB (1639511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd676bfb740256d3eae7ac606f73a7d0ad09121f54eacd3ffdeff570e4b73bd1`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:79350de5d5c17d2eea90b4a8d8b8fdf5e200d7b3173a1bcb4b52ac4c7c7b901c
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
$ docker pull caddy@sha256:58018b2f6a30dbb45e39be3761a09af004a551296f8f92bf31bef97687b15742
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121074719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8dc98d3747bd25bdd8b095b563b0cfa728096f1be09b7e50f5d2f81dc350be4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Mon, 30 Aug 2021 21:44:05 GMT
RUN apk add --no-cache ca-certificates
# Mon, 30 Aug 2021 21:44:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 30 Aug 2021 21:44:06 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:20:44 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:22:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:22:49 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:22:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:22:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:22:50 GMT
WORKDIR /go
# Thu, 04 Nov 2021 20:51:38 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 20:51:38 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:22:21 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:22:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:22:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:22:24 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31adcdaf11c89113a810db23d523e549d634d7de695a72b0ce98a1f912101262`  
		Last Modified: Mon, 30 Aug 2021 22:01:00 GMT  
		Size: 281.5 KB (281508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b176561691ea11cfe541f3ee363a3aa67e3649eb3273bea62ebeea713eaecd`  
		Last Modified: Mon, 30 Aug 2021 22:00:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d416b4d4fcca0271f31d7d73ef5910b705bc9c7e6c47e2849f526c61323bba9`  
		Last Modified: Thu, 04 Nov 2021 20:33:02 GMT  
		Size: 110.1 MB (110106449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b6b52ae600093bcea2a88e347c180ddf79cf361a229c968ab134f79566115b`  
		Last Modified: Thu, 04 Nov 2021 20:32:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ce64c87030110c9e1fb28a88d6de9ab21bc642f56da365e029fef45bd40449`  
		Last Modified: Thu, 04 Nov 2021 20:52:00 GMT  
		Size: 6.6 MB (6626626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4745adbe391f6c84dabb01d0b9f46dcb4c3835b37d657188312f964bf2428113`  
		Last Modified: Tue, 09 Nov 2021 00:23:02 GMT  
		Size: 1.2 MB (1244972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29111d85c26db67c047d940076de17d7fa99ab44f4facbb7102429b421060b91`  
		Last Modified: Tue, 09 Nov 2021 00:23:02 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a321aa86f856c91169d31a96a1181ca0fb15d4fa785b01fd4f1db0a76ac5f438
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115556079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1759314115af8681edae8afa8c25d576e2bf7c430e2fcf6bdae1a6f520f4b6f5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Mon, 30 Aug 2021 21:49:40 GMT
RUN apk add --no-cache ca-certificates
# Mon, 30 Aug 2021 21:49:41 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 30 Aug 2021 21:49:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:50:01 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:53:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:53:24 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:53:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:53:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:53:27 GMT
WORKDIR /go
# Thu, 04 Nov 2021 21:26:48 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 21:26:48 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:50:03 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:50:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:50:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:50:07 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:50:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb221a547a2f49a13c3bbe14f37b0474b2066cece57c67c2fbc1fb07d89aad51`  
		Last Modified: Mon, 30 Aug 2021 22:04:54 GMT  
		Size: 281.7 KB (281671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2968f26f7f14fe309f1a7a85ad968b81a7daa93c078322a84eb5c4192326828`  
		Last Modified: Mon, 30 Aug 2021 22:04:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1662a83909f5aff655c7be6da1ffd97a579ec92c5839159187d230df4db0c304`  
		Last Modified: Thu, 04 Nov 2021 21:06:10 GMT  
		Size: 105.0 MB (104982787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247cd469be037fb4ffd6898dfee7159dc4dbb17525c62f11540b77badda787fe`  
		Last Modified: Thu, 04 Nov 2021 21:05:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52d5113b58e9eea7126b6573a103c6174f77e3f086440c6b60d013feeae55c9`  
		Last Modified: Thu, 04 Nov 2021 21:28:00 GMT  
		Size: 6.5 MB (6485880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053aa7bf00b68e2dd2854ce3cf420395833093ba5dbf21fcbe716d7c14129a82`  
		Last Modified: Tue, 09 Nov 2021 00:51:31 GMT  
		Size: 1.2 MB (1177578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba84a71092e7a8161d2aa6cb90f140a7a6a7ee304fd1143a4bedc91bdb8a3430`  
		Last Modified: Tue, 09 Nov 2021 00:51:30 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:898867984c20de5d0a90810f09c3aa0d59c45b55c878d65fa1986002494be562
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114460716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f422bda8d34cfaad33778dcbf74db88e84c362e26c97e5ecb7e52bc0aed977c2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Mon, 30 Aug 2021 23:51:38 GMT
RUN apk add --no-cache ca-certificates
# Mon, 30 Aug 2021 23:51:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 30 Aug 2021 23:51:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:00:39 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 21:03:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 21:03:56 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 21:03:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:03:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 21:03:59 GMT
WORKDIR /go
# Thu, 04 Nov 2021 22:24:32 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 22:24:32 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:58:01 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:58:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:58:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:58:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:58:05 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9417f62ae10851eaf03f096c21f2848fdfe2517baf1faffe0a25f4a1f9853e31`  
		Last Modified: Tue, 31 Aug 2021 00:14:21 GMT  
		Size: 280.8 KB (280829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15fcbf7d3458d8a294b9a3c72856e5e7ba1372b93f8fc485abecc73f5a8c9b6`  
		Last Modified: Tue, 31 Aug 2021 00:14:21 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83145a0dc91bcfd39d1372eacfa0b0edd49fbd853a8805d09bc3c801ec17707`  
		Last Modified: Thu, 04 Nov 2021 21:24:35 GMT  
		Size: 104.8 MB (104787212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56a13d9f75fefe8df6818c553071626370c07285a8579c71d061dd3958ab9e9`  
		Last Modified: Thu, 04 Nov 2021 21:09:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a883856d1a9eb72feb215725e23c34ff4e13cc0bdba2c76df4ff5a281950a34d`  
		Last Modified: Thu, 04 Nov 2021 22:25:46 GMT  
		Size: 5.8 MB (5785275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce6cdc3c3bebb2bf176add262391b9b35a554c02e1031b6809d950661a432fe`  
		Last Modified: Tue, 09 Nov 2021 00:59:28 GMT  
		Size: 1.2 MB (1176263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699c5f30dbc0681a9241c9e446110c0ff7a3228da9ef73377eddfec9167018af`  
		Last Modified: Tue, 09 Nov 2021 00:59:27 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:465390cedcb9fff08eb002c4722d69e56f05c3c60f953da3cfb449ae162140c6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115238050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eddb3be5e644425a129daa8ef25fa1990904790212c12c1037f9acff4e54e6d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Tue, 12 Oct 2021 19:50:31 GMT
RUN apk add --no-cache ca-certificates
# Tue, 12 Oct 2021 19:50:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 12 Oct 2021 19:50:33 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:44:49 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:46:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:46:13 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:46:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:46:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:46:16 GMT
WORKDIR /go
# Thu, 04 Nov 2021 21:13:57 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 21:13:58 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:39:47 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:39:47 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:39:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:39:51 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:39:51 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb74239f2a0c13b654df471372048f7785978cbe6bf5ddc6773d88218ad689f0`  
		Last Modified: Tue, 12 Oct 2021 19:56:27 GMT  
		Size: 281.5 KB (281470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8ec004bf6b17206854367316e34aa51b7f5ff2f447e6c66498b2922dfad207`  
		Last Modified: Tue, 12 Oct 2021 19:56:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2dd7c0ce8a9709408ba750c27f660c1821df16fc1588b83103c14f5c982410`  
		Last Modified: Thu, 04 Nov 2021 20:55:18 GMT  
		Size: 104.4 MB (104362226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51b802c83dca96aee9527f6b9430dfb8d84cc63a0dfb77abd3fc70b35661b68`  
		Last Modified: Thu, 04 Nov 2021 20:55:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b82d2b3afe06ceb5e9038414bd86eaa29b64d9ca539a8d7f0a9a97d89c0ec4`  
		Last Modified: Thu, 04 Nov 2021 21:14:36 GMT  
		Size: 6.7 MB (6733703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6348d8e1d75893311f870eec10215eaead24e452e1ad2a6ae81e2b276e3cca2`  
		Last Modified: Tue, 09 Nov 2021 00:40:33 GMT  
		Size: 1.1 MB (1148135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a51eb07dd20f1949799c418f754133ca1fc5b646673e8ac9d111563dbc589f0`  
		Last Modified: Tue, 09 Nov 2021 00:40:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:2336a18de17f2c4072c9c0307696854edf929dcb82a60b90f55259a69eeb600a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (114036993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b00aa91420fc4f22cea6aab5ff77b36da6f5a53aa4614f04c4434e09de4e6f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Tue, 31 Aug 2021 00:28:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 31 Aug 2021 00:29:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 31 Aug 2021 00:29:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:35:29 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 21:37:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 21:38:07 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 21:38:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:38:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 21:38:27 GMT
WORKDIR /go
# Thu, 04 Nov 2021 23:44:35 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 23:44:36 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 02:42:23 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 02:42:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 02:42:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 02:42:49 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 02:42:55 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4539d90ff594fe73c1a1e31b2230e539a965f33143a3c9fbd89507336ed283c2`  
		Last Modified: Tue, 31 Aug 2021 00:52:27 GMT  
		Size: 283.6 KB (283640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a17d0ec6ff5411e524016f0ac7033cf7a0a8935f7a5e299d4d7acaad208b26`  
		Last Modified: Tue, 31 Aug 2021 00:52:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34c4f0757f32d139833674c31fd061ecab0806960999b78a42e97fccf03c17b`  
		Last Modified: Thu, 04 Nov 2021 21:55:32 GMT  
		Size: 102.7 MB (102722966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f044c2212367ff5cf5f5f5c673ad6d3feae574970990f8f78507c3ac07e3640`  
		Last Modified: Thu, 04 Nov 2021 21:54:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428a3c7c0c1bff96a1ad7f93a7663935ca506020c92db68c2c71b978a2e6ed00`  
		Last Modified: Thu, 04 Nov 2021 23:45:27 GMT  
		Size: 7.1 MB (7097367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c99d2cd9325e8349becf942ed19b5842c0c2199ce5cbca707223e3419ebb52`  
		Last Modified: Tue, 09 Nov 2021 02:43:49 GMT  
		Size: 1.1 MB (1120017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2118cc3ec9b4efe4249b876ec149d807c563e41337b16031f2189b0934bb4744`  
		Last Modified: Tue, 09 Nov 2021 02:43:52 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:504417781112a6da613e5dbf96701f333e86c02c15ee528bcfc69a914cb5b99c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118475563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6cfef420950dbccc42ede323157843e6c2451cefbb4b472fc259ac9e90a0708`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Mon, 30 Aug 2021 21:44:33 GMT
RUN apk add --no-cache ca-certificates
# Mon, 30 Aug 2021 21:44:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 30 Aug 2021 21:44:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:42:32 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:44:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:44:06 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:44:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:44:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:44:07 GMT
WORKDIR /go
# Thu, 04 Nov 2021 21:16:26 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 21:16:27 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:41:36 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:41:36 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:41:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:41:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:41:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316d1588ef06afb0d7a96646bb3a1367bce295885797fd976945ed318a4eb9c`  
		Last Modified: Mon, 30 Aug 2021 21:59:27 GMT  
		Size: 281.9 KB (281927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e156a554eded13f9baa4042fb4d12b879560bebfd8aca837bf0b52669f7932`  
		Last Modified: Mon, 30 Aug 2021 21:59:26 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe04792d0475ac041009f3ca62bcc0dc03a26292d21b32216bc2f3e666c2d5b`  
		Last Modified: Thu, 04 Nov 2021 20:52:06 GMT  
		Size: 107.7 MB (107663718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6416455ccb8f772096f018fb9032102e6439950a45d68d4188fdfde5d9a87ded`  
		Last Modified: Thu, 04 Nov 2021 20:51:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6952a3ac2d6398e7268d236bf7d0cee103719b380aebea5fb6aabd2e45c04ed1`  
		Last Modified: Thu, 04 Nov 2021 21:17:06 GMT  
		Size: 6.7 MB (6722226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39fdad6edb5004df0acf851fcf3b0cf9d8cdfeaa9913d04f595517236869eef`  
		Last Modified: Tue, 09 Nov 2021 00:42:30 GMT  
		Size: 1.2 MB (1203510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0be2e59b91c38d78efc2f40a152bdd89dd964e653984267002b1453226e9d2e`  
		Last Modified: Tue, 09 Nov 2021 00:42:30 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:8bdbf970abe748608ce652f507707eccf33bc6cd57a25e6bdfaec47ae0353860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull caddy@sha256:4d2914c283fcdb42d19719132d7efbfbfe7ad8af1d9cd5c071bf854233987587
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2878964819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b401c7e3582848bc6ccadc1c70895573764efb0f83732c2863411e9419c08c35`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 13:26:17 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Nov 2021 13:26:18 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Nov 2021 13:26:19 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Nov 2021 13:26:20 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Nov 2021 13:27:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:27:38 GMT
ENV GOPATH=C:\go
# Wed, 10 Nov 2021 13:28:31 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Nov 2021 13:28:32 GMT
ENV GOLANG_VERSION=1.17.3
# Wed, 10 Nov 2021 13:31:30 GMT
RUN $url = 'https://dl.google.com/go/go1.17.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e78684b955742e215926204afc6ed62b9d165b509e25a687d62902516f08726b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:31:35 GMT
WORKDIR C:\go
# Wed, 10 Nov 2021 20:17:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:17:50 GMT
ENV XCADDY_VERSION=v0.2.0
# Wed, 10 Nov 2021 20:17:51 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:17:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Nov 2021 20:18:44 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Nov 2021 20:18:45 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f32622fe466bd678a47b75fa13ebb7781336e6a776a22f424036aa8e91fe1d`  
		Last Modified: Wed, 10 Nov 2021 14:05:07 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d684ea4a6b52df2d3b5c7f7876e3b784ff1def8eb60f9637d920f4e0e7870b`  
		Last Modified: Wed, 10 Nov 2021 14:05:03 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ff61f0f89258dd1f49b766ef30baddd8f3e3821737778748ba95b52c1a480c`  
		Last Modified: Wed, 10 Nov 2021 14:05:03 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16dc9a497b44a664b28524686ca0e75c6a244af505429f54f80a6aaa96c7af9`  
		Last Modified: Wed, 10 Nov 2021 14:05:04 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e724f5e2b6e2fb2598ad100e7efa9cf30fe013f56537a5587d8e8868ae82d50`  
		Last Modified: Wed, 10 Nov 2021 14:05:09 GMT  
		Size: 25.4 MB (25446198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84e37bf01f689e54241d5e76695c5cbcc3313f3f8a85748e9d086c6cf3e4c3d`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f6ed9286b06435dae34f3d3e03f2c62a4415e3703740a83381b4ac0a3d1804`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 325.4 KB (325448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd53ef82415224427ba6005a3993a50da833e74dd65f413ede222760ab73155`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322051166b18395731c110a7ced59dc83924ac45736b482be8611e491ce9be22`  
		Last Modified: Wed, 10 Nov 2021 14:05:34 GMT  
		Size: 145.4 MB (145394728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7588b640c5b448c06e31f55936d39ebd92c0050d9b2daf5a86f09841d0ac6e68`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab8b7df216099a8c01f65cacfd0d07bfb8fe6ef211d5dbc6b897ceab643aa54`  
		Last Modified: Wed, 10 Nov 2021 20:21:41 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e1af14b4ab45cfdf867d71debb12ba16dc9770a11af54ec694004f8828280f`  
		Last Modified: Wed, 10 Nov 2021 20:21:38 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18305c1b79b992f30e786ccaa7379fba16154663b28f19d088c9b1750fe53f12`  
		Last Modified: Wed, 10 Nov 2021 20:21:38 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c926d89c22fc6adf4e181145a724ed23dacf28e12d58b7e7f75d69c4239ea2f0`  
		Last Modified: Wed, 10 Nov 2021 20:21:38 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb704654cf062fe78ae7674ea38cb7e81ac8f2b26f74c295489abf19dd4d206`  
		Last Modified: Wed, 10 Nov 2021 20:21:39 GMT  
		Size: 1.7 MB (1658702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da89e3439fa9c9e9d4cde6c4aca2fb1796d9dfceec37d31d351e2005a188b389`  
		Last Modified: Wed, 10 Nov 2021 20:21:38 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:616283cce0c82245c2685b723e1f9538d1c4e926a9ad143dd66bf0e299b64ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `caddy:2-builder-windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull caddy@sha256:96a88b09cecf23cff2a8006ea25f1e037f50d01a9c74d2d3769f8bb228d2b768
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6450468916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fcd7b2f02771fd0b23831a7e603a01713fad078e5e205d745958ee47f638e5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 13:31:46 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Nov 2021 13:31:47 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Nov 2021 13:31:48 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Nov 2021 13:31:49 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Nov 2021 13:33:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:33:37 GMT
ENV GOPATH=C:\go
# Wed, 10 Nov 2021 13:34:34 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Nov 2021 13:34:35 GMT
ENV GOLANG_VERSION=1.17.3
# Wed, 10 Nov 2021 13:37:32 GMT
RUN $url = 'https://dl.google.com/go/go1.17.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e78684b955742e215926204afc6ed62b9d165b509e25a687d62902516f08726b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:37:37 GMT
WORKDIR C:\go
# Wed, 10 Nov 2021 20:18:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:18:53 GMT
ENV XCADDY_VERSION=v0.2.0
# Wed, 10 Nov 2021 20:18:54 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:18:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Nov 2021 20:19:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Nov 2021 20:19:56 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a0c69f83a30944f5afdc948b3583f1418f71f3ae5a02382610f0898eb501f9`  
		Last Modified: Wed, 10 Nov 2021 14:05:54 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e4bea9e4e2ccac41591b4aed9981453c554ca498a23d01a69638d6ccab7016`  
		Last Modified: Wed, 10 Nov 2021 14:05:52 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b36358e1913c99dc66fbbca2e4c0f8472796bf33ceeb7fdc02d2b7096b1208d`  
		Last Modified: Wed, 10 Nov 2021 14:05:52 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d071f5d45753629193f76196d769df9ff71ce3a39e5b10a16ff571cdb071a902`  
		Last Modified: Wed, 10 Nov 2021 14:05:52 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79602be6489be8a0e5e82221cae33eae5692897081a79bfe959604121e2d0a4`  
		Last Modified: Wed, 10 Nov 2021 14:06:20 GMT  
		Size: 25.4 MB (25448073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30d749fb8ba78fba5cce783b8cbe233632a2ba5965d4b67168111396620aaa0`  
		Last Modified: Wed, 10 Nov 2021 14:05:50 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f08b5963e19f3d28aa336d06434d4efec179b4b813e4aa4222ab064bc180f7`  
		Last Modified: Wed, 10 Nov 2021 14:05:50 GMT  
		Size: 354.9 KB (354902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f381a7ed29624957c6a0c2539069229be83423497216e9b19872996d3eace018`  
		Last Modified: Wed, 10 Nov 2021 14:05:49 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9184646a18b279b69062ae625cf768031d03c297beca44a465b8265af80e7116`  
		Last Modified: Wed, 10 Nov 2021 14:06:25 GMT  
		Size: 149.9 MB (149917271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e2acfda5cf05f260961ec16cee7c5c9e5573783c8298319e6b38846cb3b98b`  
		Last Modified: Wed, 10 Nov 2021 14:05:49 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f8275e6d67e00182a573a1fea89b6fbafd29fdd9e6991bec289907772e366`  
		Last Modified: Wed, 10 Nov 2021 20:21:59 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f675d50b479c34b5e127a7560cec6198d6c06464747188b22904543e0919ffe`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dba2d80865d737653a9a4ff2db1fcac88ce9bf3521d9e7f6dc8116fd16a99b`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272648eb620ef88b428e4aac8f782d100c4e64bb6f14073ee16b5b89a3b12967`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b51ab7213b8db3f0e51ace7c64b811e81a3d838148d7c41c3a58a9ffd1eb66`  
		Last Modified: Wed, 10 Nov 2021 20:21:58 GMT  
		Size: 1.6 MB (1639511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd676bfb740256d3eae7ac606f73a7d0ad09121f54eacd3ffdeff570e4b73bd1`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:3864aebe0cb9d8ec8b0707762c6637cf9ad27a88bde3be6f9d0842eb01a19666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull caddy@sha256:4a8d9dccf760a0249237dfcf9726c0eb1b06e0b19f5ff67cf8718f8da29507c5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718934999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea4590fabf41404b64c9e90299fd322ac88350fd817d631f26264b5915ed362`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:12:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Nov 2021 20:12:21 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:13:18 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Nov 2021 20:13:19 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Nov 2021 20:13:20 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Nov 2021 20:13:21 GMT
VOLUME [c:/config]
# Wed, 10 Nov 2021 20:13:22 GMT
VOLUME [c:/data]
# Wed, 10 Nov 2021 20:13:23 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 10 Nov 2021 20:13:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Nov 2021 20:13:25 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Nov 2021 20:13:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Nov 2021 20:13:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Nov 2021 20:13:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Nov 2021 20:13:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Nov 2021 20:13:30 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Nov 2021 20:13:31 GMT
EXPOSE 80
# Wed, 10 Nov 2021 20:13:32 GMT
EXPOSE 443
# Wed, 10 Nov 2021 20:13:33 GMT
EXPOSE 2019
# Wed, 10 Nov 2021 20:14:19 GMT
RUN caddy version
# Wed, 10 Nov 2021 20:14:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b6e8b6a9caee6f47bdb32f6ec53fd2836fc02cddea3324c72caf380622fc31`  
		Last Modified: Wed, 10 Nov 2021 20:20:37 GMT  
		Size: 370.6 KB (370576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0308f92ecf7a222e22b826cf5c198551ffc380b76ee3e8de67da904b4b02f873`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05df7693285564a1ff855781db06d1dab2fa702b5492fd55461fc675cefb47b6`  
		Last Modified: Wed, 10 Nov 2021 20:20:50 GMT  
		Size: 12.1 MB (12127869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a1d26d8d7789115491377813de4a8a0c15aa4772e3b22b229a4a061f4994d5`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766e31d6b0534ea731f651ccd59e3397360e7878802aaf90257635b0edd37086`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b6f52680a8e584e06bb957343f7acef41f8863af076fed0c94c583f6a6a8ea`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3be75f11ed2b624d7b0d85454d91e6ba425c4b11d179b44611f0353c75976a5`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bb0fed8a1d238828c7b967ddc9453e83dc38e811f50de90a87ca4a79677e3e`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3343adb9cf1bed7b331007eea1fb0bfdcdcc2a11c2c295d513a73d451d338298`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655ad263ab440756e44a5b758408a577f4ba4e960ae9daec72945afc3047553f`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09b8e61a4bbdc190857116fd8fc09cd71a5409e0bf984c7a033272b2ef5f5bb`  
		Last Modified: Wed, 10 Nov 2021 20:20:32 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9723996732fa25ff5ef95b4bd85c9ddf6dfd27408fe9e220bf0156031ade487d`  
		Last Modified: Wed, 10 Nov 2021 20:20:32 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d58c78cd1d1a8562bd34f68b10ada8622f98bf19ad87174e2a3810657e48e70`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67885c8112bf51b21d408141b4bf3b2e13f08f96cdcd873dc6ca1310bdf08f65`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77274081e32b6ce8f84a136cb45008f07cd542a8f2fa0cb8a355331280e27248`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acafd6faed9e989da5b7ca4bcf5d704b15d86d0b5076b645224a578b5453eb61`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109d2337e42e4f8cfc28c01475b5d1ab49d1e776006c622915ec2166c8fead72`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ee8d0bd71b0b4f05c46aa89f1434f50b4685f23ab7e0e092ae5f46e1d150ad`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd8ebab410bbbe5d576ac2f9ec8f4f2b9d251ae4a307bc8c11bb47165553f63`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 290.2 KB (290194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a550a1217bcfc790088e7a6d4f32ebdea15bae25f297c4683cb3dfc3e6c72e4d`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.14393.4770; amd64

```console
$ docker pull caddy@sha256:2c091f3638b3d3948ffa8c2d95a9be662e858768ffc52e366872371a68d003a1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6285957464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fb2d13bfaf3ee5703b28aa6d939cbfac5b14658e1e3e91bbae594e1c4b22a2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:15:34 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Nov 2021 20:15:35 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:16:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Nov 2021 20:16:39 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Nov 2021 20:16:40 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Nov 2021 20:16:41 GMT
VOLUME [c:/config]
# Wed, 10 Nov 2021 20:16:42 GMT
VOLUME [c:/data]
# Wed, 10 Nov 2021 20:16:43 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 10 Nov 2021 20:16:44 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Nov 2021 20:16:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Nov 2021 20:16:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Nov 2021 20:16:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Nov 2021 20:16:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Nov 2021 20:16:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Nov 2021 20:16:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Nov 2021 20:16:50 GMT
EXPOSE 80
# Wed, 10 Nov 2021 20:16:51 GMT
EXPOSE 443
# Wed, 10 Nov 2021 20:16:52 GMT
EXPOSE 2019
# Wed, 10 Nov 2021 20:17:30 GMT
RUN caddy version
# Wed, 10 Nov 2021 20:17:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224cfcc2d1317d73465188f71867febbba9a64bbfcdf83b35bccd662bdb25748`  
		Last Modified: Wed, 10 Nov 2021 20:21:11 GMT  
		Size: 366.8 KB (366836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98f673e7fe75a29f4060341dab79e20ad059162395f10fb1fc2504379d12f22`  
		Last Modified: Wed, 10 Nov 2021 20:21:10 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6dc3d9f8e8e85985894d372a912cae2cbc64cc10540262498597bbe8cad8c31`  
		Last Modified: Wed, 10 Nov 2021 20:21:24 GMT  
		Size: 12.2 MB (12158174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197a3f340985e5e76e3ae77fcbb9e208f521abbad0cfb8921d27d4afe569f280`  
		Last Modified: Wed, 10 Nov 2021 20:21:13 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1443a981044b58af1bae85624fffe4dde7c1759e6a5f930ddaf2eb70bc3185dd`  
		Last Modified: Wed, 10 Nov 2021 20:21:10 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1b023614dd84860e7a4fdd1855131b5478b9b747a40fc9383467934e48e310`  
		Last Modified: Wed, 10 Nov 2021 20:21:09 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daca4ab6367b318ae3a2df27bbe0c53c12ee1a0196fc4f43a43ec47acd74c7c`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a288866cea4075f0f825973ce9d3369dd9411f73c325ed870a5233b383476dbc`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea1c63b1b4cb8f39b59025d926f384679d17bb660eceafe7f7c9418dcdfad61`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b25f60f98964a2d03947e1dac0b01388ad6c9c65497e546f8efe7f2fdcd35e`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d10f21fe32d5dd37a74db003c1119b2aaba639690b10ad4c46d22e2699140fc`  
		Last Modified: Wed, 10 Nov 2021 20:21:06 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4bd5845100c889806835753480fb0016610fbfab35d197c6aa641d73c114ed`  
		Last Modified: Wed, 10 Nov 2021 20:21:06 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190767770423c20b77f963553559cfa26d18b490228ad11c4f9fcf62e6dcefd7`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab0412df33f87a4e77ce1ef8afc68a04cd9a9a56ce9a21e3494f4e4f7c1083a`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80edcc113a751c789aee343b18fdb12c9099cd642cf099ab6a962c7cb0bce8b`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d513b74afabeb0e8050ca955cdf8b72040cabc21350ab394862808bd4382649`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc99c5e78f676bc2fed853c2d43f71dedcbf29fe3a6f69f5d0bc1eabca7f8e98`  
		Last Modified: Wed, 10 Nov 2021 20:21:04 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1532dfe2f3d7f9a4d2eed5ac842a7b54e160fb4d856388e1153d0c6488bab749`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c6594f3623b09c0359fe4347b1981678cebb55cebad4bd683d4bc059e0a201`  
		Last Modified: Wed, 10 Nov 2021 20:21:04 GMT  
		Size: 316.3 KB (316295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c07c5e836014edc4e052889ecbe945aa470b434f2563726bd4f9684da37bfc1`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:4d8f28e3fbdc28a6ebdf57a867626560f0651157d3cf1cddaa279a9f57c34c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull caddy@sha256:4a8d9dccf760a0249237dfcf9726c0eb1b06e0b19f5ff67cf8718f8da29507c5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718934999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea4590fabf41404b64c9e90299fd322ac88350fd817d631f26264b5915ed362`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:12:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Nov 2021 20:12:21 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:13:18 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Nov 2021 20:13:19 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Nov 2021 20:13:20 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Nov 2021 20:13:21 GMT
VOLUME [c:/config]
# Wed, 10 Nov 2021 20:13:22 GMT
VOLUME [c:/data]
# Wed, 10 Nov 2021 20:13:23 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 10 Nov 2021 20:13:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Nov 2021 20:13:25 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Nov 2021 20:13:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Nov 2021 20:13:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Nov 2021 20:13:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Nov 2021 20:13:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Nov 2021 20:13:30 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Nov 2021 20:13:31 GMT
EXPOSE 80
# Wed, 10 Nov 2021 20:13:32 GMT
EXPOSE 443
# Wed, 10 Nov 2021 20:13:33 GMT
EXPOSE 2019
# Wed, 10 Nov 2021 20:14:19 GMT
RUN caddy version
# Wed, 10 Nov 2021 20:14:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b6e8b6a9caee6f47bdb32f6ec53fd2836fc02cddea3324c72caf380622fc31`  
		Last Modified: Wed, 10 Nov 2021 20:20:37 GMT  
		Size: 370.6 KB (370576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0308f92ecf7a222e22b826cf5c198551ffc380b76ee3e8de67da904b4b02f873`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05df7693285564a1ff855781db06d1dab2fa702b5492fd55461fc675cefb47b6`  
		Last Modified: Wed, 10 Nov 2021 20:20:50 GMT  
		Size: 12.1 MB (12127869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a1d26d8d7789115491377813de4a8a0c15aa4772e3b22b229a4a061f4994d5`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766e31d6b0534ea731f651ccd59e3397360e7878802aaf90257635b0edd37086`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b6f52680a8e584e06bb957343f7acef41f8863af076fed0c94c583f6a6a8ea`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3be75f11ed2b624d7b0d85454d91e6ba425c4b11d179b44611f0353c75976a5`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bb0fed8a1d238828c7b967ddc9453e83dc38e811f50de90a87ca4a79677e3e`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3343adb9cf1bed7b331007eea1fb0bfdcdcc2a11c2c295d513a73d451d338298`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655ad263ab440756e44a5b758408a577f4ba4e960ae9daec72945afc3047553f`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09b8e61a4bbdc190857116fd8fc09cd71a5409e0bf984c7a033272b2ef5f5bb`  
		Last Modified: Wed, 10 Nov 2021 20:20:32 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9723996732fa25ff5ef95b4bd85c9ddf6dfd27408fe9e220bf0156031ade487d`  
		Last Modified: Wed, 10 Nov 2021 20:20:32 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d58c78cd1d1a8562bd34f68b10ada8622f98bf19ad87174e2a3810657e48e70`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67885c8112bf51b21d408141b4bf3b2e13f08f96cdcd873dc6ca1310bdf08f65`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77274081e32b6ce8f84a136cb45008f07cd542a8f2fa0cb8a355331280e27248`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acafd6faed9e989da5b7ca4bcf5d704b15d86d0b5076b645224a578b5453eb61`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109d2337e42e4f8cfc28c01475b5d1ab49d1e776006c622915ec2166c8fead72`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ee8d0bd71b0b4f05c46aa89f1434f50b4685f23ab7e0e092ae5f46e1d150ad`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd8ebab410bbbe5d576ac2f9ec8f4f2b9d251ae4a307bc8c11bb47165553f63`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 290.2 KB (290194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a550a1217bcfc790088e7a6d4f32ebdea15bae25f297c4683cb3dfc3e6c72e4d`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:b399e4134eac2ed1e68a9f6d12fa6c2f89351edd4b13f45e687d84ee2c8c7891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `caddy:2-windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull caddy@sha256:2c091f3638b3d3948ffa8c2d95a9be662e858768ffc52e366872371a68d003a1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6285957464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fb2d13bfaf3ee5703b28aa6d939cbfac5b14658e1e3e91bbae594e1c4b22a2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:15:34 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Nov 2021 20:15:35 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:16:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Nov 2021 20:16:39 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Nov 2021 20:16:40 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Nov 2021 20:16:41 GMT
VOLUME [c:/config]
# Wed, 10 Nov 2021 20:16:42 GMT
VOLUME [c:/data]
# Wed, 10 Nov 2021 20:16:43 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 10 Nov 2021 20:16:44 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Nov 2021 20:16:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Nov 2021 20:16:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Nov 2021 20:16:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Nov 2021 20:16:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Nov 2021 20:16:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Nov 2021 20:16:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Nov 2021 20:16:50 GMT
EXPOSE 80
# Wed, 10 Nov 2021 20:16:51 GMT
EXPOSE 443
# Wed, 10 Nov 2021 20:16:52 GMT
EXPOSE 2019
# Wed, 10 Nov 2021 20:17:30 GMT
RUN caddy version
# Wed, 10 Nov 2021 20:17:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224cfcc2d1317d73465188f71867febbba9a64bbfcdf83b35bccd662bdb25748`  
		Last Modified: Wed, 10 Nov 2021 20:21:11 GMT  
		Size: 366.8 KB (366836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98f673e7fe75a29f4060341dab79e20ad059162395f10fb1fc2504379d12f22`  
		Last Modified: Wed, 10 Nov 2021 20:21:10 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6dc3d9f8e8e85985894d372a912cae2cbc64cc10540262498597bbe8cad8c31`  
		Last Modified: Wed, 10 Nov 2021 20:21:24 GMT  
		Size: 12.2 MB (12158174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197a3f340985e5e76e3ae77fcbb9e208f521abbad0cfb8921d27d4afe569f280`  
		Last Modified: Wed, 10 Nov 2021 20:21:13 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1443a981044b58af1bae85624fffe4dde7c1759e6a5f930ddaf2eb70bc3185dd`  
		Last Modified: Wed, 10 Nov 2021 20:21:10 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1b023614dd84860e7a4fdd1855131b5478b9b747a40fc9383467934e48e310`  
		Last Modified: Wed, 10 Nov 2021 20:21:09 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daca4ab6367b318ae3a2df27bbe0c53c12ee1a0196fc4f43a43ec47acd74c7c`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a288866cea4075f0f825973ce9d3369dd9411f73c325ed870a5233b383476dbc`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea1c63b1b4cb8f39b59025d926f384679d17bb660eceafe7f7c9418dcdfad61`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b25f60f98964a2d03947e1dac0b01388ad6c9c65497e546f8efe7f2fdcd35e`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d10f21fe32d5dd37a74db003c1119b2aaba639690b10ad4c46d22e2699140fc`  
		Last Modified: Wed, 10 Nov 2021 20:21:06 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4bd5845100c889806835753480fb0016610fbfab35d197c6aa641d73c114ed`  
		Last Modified: Wed, 10 Nov 2021 20:21:06 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190767770423c20b77f963553559cfa26d18b490228ad11c4f9fcf62e6dcefd7`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab0412df33f87a4e77ce1ef8afc68a04cd9a9a56ce9a21e3494f4e4f7c1083a`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80edcc113a751c789aee343b18fdb12c9099cd642cf099ab6a962c7cb0bce8b`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d513b74afabeb0e8050ca955cdf8b72040cabc21350ab394862808bd4382649`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc99c5e78f676bc2fed853c2d43f71dedcbf29fe3a6f69f5d0bc1eabca7f8e98`  
		Last Modified: Wed, 10 Nov 2021 20:21:04 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1532dfe2f3d7f9a4d2eed5ac842a7b54e160fb4d856388e1153d0c6488bab749`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c6594f3623b09c0359fe4347b1981678cebb55cebad4bd683d4bc059e0a201`  
		Last Modified: Wed, 10 Nov 2021 20:21:04 GMT  
		Size: 316.3 KB (316295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c07c5e836014edc4e052889ecbe945aa470b434f2563726bd4f9684da37bfc1`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.6`

```console
$ docker pull caddy@sha256:b82736e58560e3c1591c6205ddd9f44a5a11edebb1341a2e8cfe05b2617daa47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `caddy:2.4.6` - linux; amd64

```console
$ docker pull caddy@sha256:85a8daaf3706e847da86d456fb722edacb72a32360d333febccbf208f08e2be6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14847925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332a21201a47e70a89875163c9e41f0e78d6514d6e64aae618c3e2cc79b5e35d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:19:30 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:19:31 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:22:07 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:22:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:22:12 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:22:12 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:22:12 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:22:12 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:22:13 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:22:13 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:22:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:22:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:22:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:22:15 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:22:16 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:22:16 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:22:16 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:22:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d9d63a262eb117d9f55cf667904b985eb6dd9830783f17146a17a107a7ee19`  
		Last Modified: Tue, 07 Sep 2021 19:20:03 GMT  
		Size: 301.0 KB (301044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d54a459a500730b7153882903986d92e877f472e9d6ead142fab9dcb6464e1`  
		Last Modified: Tue, 07 Sep 2021 19:20:04 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12929046016b5f7547cb262dd7e97132958593eff9f30a3062729ed87f5f764f`  
		Last Modified: Tue, 09 Nov 2021 00:22:50 GMT  
		Size: 11.7 MB (11726452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2abe024ef8ac2567e428b8c753253b9670be99dad8f46607c895df6577f60ee`  
		Last Modified: Tue, 09 Nov 2021 00:22:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - linux; arm variant v6

```console
$ docker pull caddy@sha256:84282af6d453c14c7875598e935faa6d1e7605067a6a212f69227bed1b97ae91
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14060404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4a22469cd1950a4d76a71bd95254b6b70d97f1d46d0ab846d9561937d7cee8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:49:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:49:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:49:32 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:49:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:49:39 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:49:39 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:49:40 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:49:40 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:49:41 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:49:41 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:49:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:49:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:49:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:49:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:49:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:49:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:49:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:49:45 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:49:45 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:49:46 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:49:46 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:49:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f254033e1bbf10f9a1641b6005ee6ae290bdec377e00d2e5290e33dc0eb8f9b6`  
		Last Modified: Tue, 07 Sep 2021 19:51:17 GMT  
		Size: 301.2 KB (301188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28038de9754eec9aa2df09a34c0d7029c335199166de56398d21fb595fd289dd`  
		Last Modified: Tue, 07 Sep 2021 19:51:17 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d17cc2aea86ad912ecd44f746238a440abd651aacc69ff04dcfdfa5e93193bb`  
		Last Modified: Tue, 09 Nov 2021 00:51:15 GMT  
		Size: 11.1 MB (11125785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cde1922177a05c9ac9c3cdb88d2492158258e3ddc64a6168bf7aa3d2087c3f5`  
		Last Modified: Tue, 09 Nov 2021 00:51:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - linux; arm variant v7

```console
$ docker pull caddy@sha256:fb17cbc78aa551976f55685ba43b474671da9323631920b2411ef3ba47986f62
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13843483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9933538b9e4061a71c69dda3c1ac39f499b0a0c09fc86871a60a60b72576e0c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:57:36 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:57:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:57:30 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:57:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:57:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:57:37 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:57:37 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:57:38 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:57:38 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:57:39 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:57:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:57:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:57:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:57:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:57:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:57:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:57:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:57:42 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:57:43 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:57:43 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:57:44 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:57:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98c39987cd6455919d7455feed9aba93a44659ef658fbef5d4d52500beddac5`  
		Last Modified: Tue, 07 Sep 2021 19:59:13 GMT  
		Size: 300.4 KB (300356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e223cb6b0d911c9cc6575c496bc4f96f1968db869a8a07694f3f49897920f264`  
		Last Modified: Tue, 07 Sep 2021 19:59:13 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d8001745b5a3dedaa6b3a2bef5234f8612ac3d942269d2e18abbc1bfae84c8`  
		Last Modified: Tue, 09 Nov 2021 00:59:12 GMT  
		Size: 11.1 MB (11106727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bfb11f4ca256c6f83e7d7f05fdc548ce544492b765b72bad8fff802e114ec0`  
		Last Modified: Tue, 09 Nov 2021 00:59:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:dcc03368e7ff328ba4159eca9d88c2cb33e3ef4d8aaf9cec550f4f924c032616
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13757357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fca8f72561cf76363cdb806b321face6a1c9831e94d96c4966828a26b19962b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 14 Oct 2021 01:35:26 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 14 Oct 2021 01:35:28 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:39:19 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:39:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:39:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:39:23 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:39:24 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:39:25 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:39:26 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:39:27 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:39:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:39:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:39:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:39:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:39:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:39:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:39:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:39:35 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:39:36 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:39:37 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:39:38 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:39:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdae6629f9c73c56d66409172a1dcab55f533f8b62eb70c990c8e2cabcd7695`  
		Last Modified: Thu, 14 Oct 2021 01:36:31 GMT  
		Size: 301.0 KB (300992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3c515fae4831ae5dd272bcc27d7d3d3011d0f880b795b0aed1ce8c389c96bf`  
		Last Modified: Thu, 14 Oct 2021 01:36:30 GMT  
		Size: 5.8 KB (5752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce648197b75d827f9704483ccbcc884912ffb6a25728a39ddd0f717c3d534a46`  
		Last Modified: Tue, 09 Nov 2021 00:40:20 GMT  
		Size: 10.7 MB (10738633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d3751262c3b44d86e469c50ed19d1a632a37d420e471e3653d9c26c8d51ba6`  
		Last Modified: Tue, 09 Nov 2021 00:40:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - linux; ppc64le

```console
$ docker pull caddy@sha256:b1f36f28cb28be8e03baf5e564e8813cf57f65a907533db61acec3fc2ff7d337
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13423700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927f64bc8094cd853e2649145f44cf5cbc699568c2066c650c61db9865417dc5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:16:42 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:16:56 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 02:38:59 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 02:39:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 02:39:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 02:39:43 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 02:39:47 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 02:39:58 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 02:40:04 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 02:40:16 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 02:40:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 02:40:30 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 02:40:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 02:40:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 02:40:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 02:41:01 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 02:41:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 02:41:31 GMT
EXPOSE 80
# Tue, 09 Nov 2021 02:41:42 GMT
EXPOSE 443
# Tue, 09 Nov 2021 02:41:49 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 02:41:57 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 02:42:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d32e3566fcaa11540498ebdd9ecc55cd2e2dca73a6b62317657a9e75749272`  
		Last Modified: Tue, 07 Sep 2021 19:21:13 GMT  
		Size: 303.2 KB (303162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a831abca68890cbd7a89171bb93c9af5c1b102852f0f1f3326ff7c104ced90`  
		Last Modified: Tue, 07 Sep 2021 19:21:12 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef4a0928ede6ae0f23c1a955b08d450770842d163d8152b4ad7cb9333b4ac5b`  
		Last Modified: Tue, 09 Nov 2021 02:43:36 GMT  
		Size: 10.3 MB (10302268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6dff47d769c4013cb3ed7545b165cd303bac49d09576d80c78bfa8d9353b1bb`  
		Last Modified: Tue, 09 Nov 2021 02:43:34 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - linux; s390x

```console
$ docker pull caddy@sha256:7ceecb66639b47e4acb3acc566018228f83534b5a49f4a5306f4a6ae995cd13f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14234623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82585988e83eb76f3ebc0d2bb5323c9663491e28faa0819aa54296c142e686b3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:41:29 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:41:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:41:22 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:41:25 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:41:26 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:41:26 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:41:26 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:41:26 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:41:27 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:41:27 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:41:27 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:41:27 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:41:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9c7d5d2c4319fc2386cc1a009e57751b8d7a7d807ae0e867e4d6273e06731d`  
		Last Modified: Tue, 07 Sep 2021 19:42:43 GMT  
		Size: 301.5 KB (301462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c7b669e195c7cce7cf6d957130645125c1171c464622ceaa01378d18f24e37`  
		Last Modified: Tue, 07 Sep 2021 19:42:43 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931bdaaeb048d3dff8468154aa9eceea8e363d63dc61208df60553535bfe8f85`  
		Last Modified: Tue, 09 Nov 2021 00:42:20 GMT  
		Size: 11.3 MB (11323714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f913866909777fce146b3d1c6a81b811018e4bd5ba8ecd4d29168eb9dcced`  
		Last Modified: Tue, 09 Nov 2021 00:42:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - windows version 10.0.17763.2300; amd64

```console
$ docker pull caddy@sha256:4a8d9dccf760a0249237dfcf9726c0eb1b06e0b19f5ff67cf8718f8da29507c5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718934999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea4590fabf41404b64c9e90299fd322ac88350fd817d631f26264b5915ed362`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:12:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Nov 2021 20:12:21 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:13:18 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Nov 2021 20:13:19 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Nov 2021 20:13:20 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Nov 2021 20:13:21 GMT
VOLUME [c:/config]
# Wed, 10 Nov 2021 20:13:22 GMT
VOLUME [c:/data]
# Wed, 10 Nov 2021 20:13:23 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 10 Nov 2021 20:13:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Nov 2021 20:13:25 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Nov 2021 20:13:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Nov 2021 20:13:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Nov 2021 20:13:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Nov 2021 20:13:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Nov 2021 20:13:30 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Nov 2021 20:13:31 GMT
EXPOSE 80
# Wed, 10 Nov 2021 20:13:32 GMT
EXPOSE 443
# Wed, 10 Nov 2021 20:13:33 GMT
EXPOSE 2019
# Wed, 10 Nov 2021 20:14:19 GMT
RUN caddy version
# Wed, 10 Nov 2021 20:14:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b6e8b6a9caee6f47bdb32f6ec53fd2836fc02cddea3324c72caf380622fc31`  
		Last Modified: Wed, 10 Nov 2021 20:20:37 GMT  
		Size: 370.6 KB (370576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0308f92ecf7a222e22b826cf5c198551ffc380b76ee3e8de67da904b4b02f873`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05df7693285564a1ff855781db06d1dab2fa702b5492fd55461fc675cefb47b6`  
		Last Modified: Wed, 10 Nov 2021 20:20:50 GMT  
		Size: 12.1 MB (12127869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a1d26d8d7789115491377813de4a8a0c15aa4772e3b22b229a4a061f4994d5`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766e31d6b0534ea731f651ccd59e3397360e7878802aaf90257635b0edd37086`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b6f52680a8e584e06bb957343f7acef41f8863af076fed0c94c583f6a6a8ea`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3be75f11ed2b624d7b0d85454d91e6ba425c4b11d179b44611f0353c75976a5`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bb0fed8a1d238828c7b967ddc9453e83dc38e811f50de90a87ca4a79677e3e`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3343adb9cf1bed7b331007eea1fb0bfdcdcc2a11c2c295d513a73d451d338298`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655ad263ab440756e44a5b758408a577f4ba4e960ae9daec72945afc3047553f`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09b8e61a4bbdc190857116fd8fc09cd71a5409e0bf984c7a033272b2ef5f5bb`  
		Last Modified: Wed, 10 Nov 2021 20:20:32 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9723996732fa25ff5ef95b4bd85c9ddf6dfd27408fe9e220bf0156031ade487d`  
		Last Modified: Wed, 10 Nov 2021 20:20:32 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d58c78cd1d1a8562bd34f68b10ada8622f98bf19ad87174e2a3810657e48e70`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67885c8112bf51b21d408141b4bf3b2e13f08f96cdcd873dc6ca1310bdf08f65`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77274081e32b6ce8f84a136cb45008f07cd542a8f2fa0cb8a355331280e27248`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acafd6faed9e989da5b7ca4bcf5d704b15d86d0b5076b645224a578b5453eb61`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109d2337e42e4f8cfc28c01475b5d1ab49d1e776006c622915ec2166c8fead72`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ee8d0bd71b0b4f05c46aa89f1434f50b4685f23ab7e0e092ae5f46e1d150ad`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd8ebab410bbbe5d576ac2f9ec8f4f2b9d251ae4a307bc8c11bb47165553f63`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 290.2 KB (290194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a550a1217bcfc790088e7a6d4f32ebdea15bae25f297c4683cb3dfc3e6c72e4d`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6` - windows version 10.0.14393.4770; amd64

```console
$ docker pull caddy@sha256:2c091f3638b3d3948ffa8c2d95a9be662e858768ffc52e366872371a68d003a1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6285957464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fb2d13bfaf3ee5703b28aa6d939cbfac5b14658e1e3e91bbae594e1c4b22a2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:15:34 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Nov 2021 20:15:35 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:16:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Nov 2021 20:16:39 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Nov 2021 20:16:40 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Nov 2021 20:16:41 GMT
VOLUME [c:/config]
# Wed, 10 Nov 2021 20:16:42 GMT
VOLUME [c:/data]
# Wed, 10 Nov 2021 20:16:43 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 10 Nov 2021 20:16:44 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Nov 2021 20:16:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Nov 2021 20:16:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Nov 2021 20:16:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Nov 2021 20:16:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Nov 2021 20:16:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Nov 2021 20:16:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Nov 2021 20:16:50 GMT
EXPOSE 80
# Wed, 10 Nov 2021 20:16:51 GMT
EXPOSE 443
# Wed, 10 Nov 2021 20:16:52 GMT
EXPOSE 2019
# Wed, 10 Nov 2021 20:17:30 GMT
RUN caddy version
# Wed, 10 Nov 2021 20:17:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224cfcc2d1317d73465188f71867febbba9a64bbfcdf83b35bccd662bdb25748`  
		Last Modified: Wed, 10 Nov 2021 20:21:11 GMT  
		Size: 366.8 KB (366836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98f673e7fe75a29f4060341dab79e20ad059162395f10fb1fc2504379d12f22`  
		Last Modified: Wed, 10 Nov 2021 20:21:10 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6dc3d9f8e8e85985894d372a912cae2cbc64cc10540262498597bbe8cad8c31`  
		Last Modified: Wed, 10 Nov 2021 20:21:24 GMT  
		Size: 12.2 MB (12158174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197a3f340985e5e76e3ae77fcbb9e208f521abbad0cfb8921d27d4afe569f280`  
		Last Modified: Wed, 10 Nov 2021 20:21:13 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1443a981044b58af1bae85624fffe4dde7c1759e6a5f930ddaf2eb70bc3185dd`  
		Last Modified: Wed, 10 Nov 2021 20:21:10 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1b023614dd84860e7a4fdd1855131b5478b9b747a40fc9383467934e48e310`  
		Last Modified: Wed, 10 Nov 2021 20:21:09 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daca4ab6367b318ae3a2df27bbe0c53c12ee1a0196fc4f43a43ec47acd74c7c`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a288866cea4075f0f825973ce9d3369dd9411f73c325ed870a5233b383476dbc`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea1c63b1b4cb8f39b59025d926f384679d17bb660eceafe7f7c9418dcdfad61`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b25f60f98964a2d03947e1dac0b01388ad6c9c65497e546f8efe7f2fdcd35e`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d10f21fe32d5dd37a74db003c1119b2aaba639690b10ad4c46d22e2699140fc`  
		Last Modified: Wed, 10 Nov 2021 20:21:06 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4bd5845100c889806835753480fb0016610fbfab35d197c6aa641d73c114ed`  
		Last Modified: Wed, 10 Nov 2021 20:21:06 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190767770423c20b77f963553559cfa26d18b490228ad11c4f9fcf62e6dcefd7`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab0412df33f87a4e77ce1ef8afc68a04cd9a9a56ce9a21e3494f4e4f7c1083a`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80edcc113a751c789aee343b18fdb12c9099cd642cf099ab6a962c7cb0bce8b`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d513b74afabeb0e8050ca955cdf8b72040cabc21350ab394862808bd4382649`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc99c5e78f676bc2fed853c2d43f71dedcbf29fe3a6f69f5d0bc1eabca7f8e98`  
		Last Modified: Wed, 10 Nov 2021 20:21:04 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1532dfe2f3d7f9a4d2eed5ac842a7b54e160fb4d856388e1153d0c6488bab749`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c6594f3623b09c0359fe4347b1981678cebb55cebad4bd683d4bc059e0a201`  
		Last Modified: Wed, 10 Nov 2021 20:21:04 GMT  
		Size: 316.3 KB (316295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c07c5e836014edc4e052889ecbe945aa470b434f2563726bd4f9684da37bfc1`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.6-alpine`

```console
$ docker pull caddy@sha256:dbc76d658f90c3ce8f96d6a3ccc918d1694c586003eae68a6cf2282ce2ecf2ef
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
$ docker pull caddy@sha256:85a8daaf3706e847da86d456fb722edacb72a32360d333febccbf208f08e2be6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14847925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332a21201a47e70a89875163c9e41f0e78d6514d6e64aae618c3e2cc79b5e35d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:19:30 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:19:31 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:22:07 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:22:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:22:12 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:22:12 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:22:12 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:22:12 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:22:13 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:22:13 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:22:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:22:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:22:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:22:15 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:22:16 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:22:16 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:22:16 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:22:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d9d63a262eb117d9f55cf667904b985eb6dd9830783f17146a17a107a7ee19`  
		Last Modified: Tue, 07 Sep 2021 19:20:03 GMT  
		Size: 301.0 KB (301044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d54a459a500730b7153882903986d92e877f472e9d6ead142fab9dcb6464e1`  
		Last Modified: Tue, 07 Sep 2021 19:20:04 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12929046016b5f7547cb262dd7e97132958593eff9f30a3062729ed87f5f764f`  
		Last Modified: Tue, 09 Nov 2021 00:22:50 GMT  
		Size: 11.7 MB (11726452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2abe024ef8ac2567e428b8c753253b9670be99dad8f46607c895df6577f60ee`  
		Last Modified: Tue, 09 Nov 2021 00:22:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:84282af6d453c14c7875598e935faa6d1e7605067a6a212f69227bed1b97ae91
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14060404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4a22469cd1950a4d76a71bd95254b6b70d97f1d46d0ab846d9561937d7cee8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:49:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:49:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:49:32 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:49:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:49:39 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:49:39 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:49:40 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:49:40 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:49:41 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:49:41 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:49:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:49:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:49:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:49:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:49:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:49:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:49:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:49:45 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:49:45 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:49:46 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:49:46 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:49:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f254033e1bbf10f9a1641b6005ee6ae290bdec377e00d2e5290e33dc0eb8f9b6`  
		Last Modified: Tue, 07 Sep 2021 19:51:17 GMT  
		Size: 301.2 KB (301188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28038de9754eec9aa2df09a34c0d7029c335199166de56398d21fb595fd289dd`  
		Last Modified: Tue, 07 Sep 2021 19:51:17 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d17cc2aea86ad912ecd44f746238a440abd651aacc69ff04dcfdfa5e93193bb`  
		Last Modified: Tue, 09 Nov 2021 00:51:15 GMT  
		Size: 11.1 MB (11125785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cde1922177a05c9ac9c3cdb88d2492158258e3ddc64a6168bf7aa3d2087c3f5`  
		Last Modified: Tue, 09 Nov 2021 00:51:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:fb17cbc78aa551976f55685ba43b474671da9323631920b2411ef3ba47986f62
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13843483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9933538b9e4061a71c69dda3c1ac39f499b0a0c09fc86871a60a60b72576e0c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:57:36 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:57:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:57:30 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:57:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:57:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:57:37 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:57:37 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:57:38 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:57:38 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:57:39 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:57:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:57:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:57:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:57:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:57:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:57:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:57:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:57:42 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:57:43 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:57:43 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:57:44 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:57:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98c39987cd6455919d7455feed9aba93a44659ef658fbef5d4d52500beddac5`  
		Last Modified: Tue, 07 Sep 2021 19:59:13 GMT  
		Size: 300.4 KB (300356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e223cb6b0d911c9cc6575c496bc4f96f1968db869a8a07694f3f49897920f264`  
		Last Modified: Tue, 07 Sep 2021 19:59:13 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d8001745b5a3dedaa6b3a2bef5234f8612ac3d942269d2e18abbc1bfae84c8`  
		Last Modified: Tue, 09 Nov 2021 00:59:12 GMT  
		Size: 11.1 MB (11106727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bfb11f4ca256c6f83e7d7f05fdc548ce544492b765b72bad8fff802e114ec0`  
		Last Modified: Tue, 09 Nov 2021 00:59:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:dcc03368e7ff328ba4159eca9d88c2cb33e3ef4d8aaf9cec550f4f924c032616
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13757357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fca8f72561cf76363cdb806b321face6a1c9831e94d96c4966828a26b19962b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 14 Oct 2021 01:35:26 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 14 Oct 2021 01:35:28 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:39:19 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:39:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:39:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:39:23 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:39:24 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:39:25 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:39:26 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:39:27 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:39:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:39:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:39:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:39:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:39:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:39:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:39:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:39:35 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:39:36 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:39:37 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:39:38 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:39:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdae6629f9c73c56d66409172a1dcab55f533f8b62eb70c990c8e2cabcd7695`  
		Last Modified: Thu, 14 Oct 2021 01:36:31 GMT  
		Size: 301.0 KB (300992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3c515fae4831ae5dd272bcc27d7d3d3011d0f880b795b0aed1ce8c389c96bf`  
		Last Modified: Thu, 14 Oct 2021 01:36:30 GMT  
		Size: 5.8 KB (5752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce648197b75d827f9704483ccbcc884912ffb6a25728a39ddd0f717c3d534a46`  
		Last Modified: Tue, 09 Nov 2021 00:40:20 GMT  
		Size: 10.7 MB (10738633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d3751262c3b44d86e469c50ed19d1a632a37d420e471e3653d9c26c8d51ba6`  
		Last Modified: Tue, 09 Nov 2021 00:40:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:b1f36f28cb28be8e03baf5e564e8813cf57f65a907533db61acec3fc2ff7d337
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13423700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927f64bc8094cd853e2649145f44cf5cbc699568c2066c650c61db9865417dc5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:16:42 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:16:56 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 02:38:59 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 02:39:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 02:39:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 02:39:43 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 02:39:47 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 02:39:58 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 02:40:04 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 02:40:16 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 02:40:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 02:40:30 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 02:40:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 02:40:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 02:40:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 02:41:01 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 02:41:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 02:41:31 GMT
EXPOSE 80
# Tue, 09 Nov 2021 02:41:42 GMT
EXPOSE 443
# Tue, 09 Nov 2021 02:41:49 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 02:41:57 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 02:42:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d32e3566fcaa11540498ebdd9ecc55cd2e2dca73a6b62317657a9e75749272`  
		Last Modified: Tue, 07 Sep 2021 19:21:13 GMT  
		Size: 303.2 KB (303162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a831abca68890cbd7a89171bb93c9af5c1b102852f0f1f3326ff7c104ced90`  
		Last Modified: Tue, 07 Sep 2021 19:21:12 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef4a0928ede6ae0f23c1a955b08d450770842d163d8152b4ad7cb9333b4ac5b`  
		Last Modified: Tue, 09 Nov 2021 02:43:36 GMT  
		Size: 10.3 MB (10302268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6dff47d769c4013cb3ed7545b165cd303bac49d09576d80c78bfa8d9353b1bb`  
		Last Modified: Tue, 09 Nov 2021 02:43:34 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:7ceecb66639b47e4acb3acc566018228f83534b5a49f4a5306f4a6ae995cd13f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14234623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82585988e83eb76f3ebc0d2bb5323c9663491e28faa0819aa54296c142e686b3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:41:29 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:41:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:41:22 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:41:25 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:41:26 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:41:26 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:41:26 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:41:26 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:41:27 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:41:27 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:41:27 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:41:27 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:41:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9c7d5d2c4319fc2386cc1a009e57751b8d7a7d807ae0e867e4d6273e06731d`  
		Last Modified: Tue, 07 Sep 2021 19:42:43 GMT  
		Size: 301.5 KB (301462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c7b669e195c7cce7cf6d957130645125c1171c464622ceaa01378d18f24e37`  
		Last Modified: Tue, 07 Sep 2021 19:42:43 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931bdaaeb048d3dff8468154aa9eceea8e363d63dc61208df60553535bfe8f85`  
		Last Modified: Tue, 09 Nov 2021 00:42:20 GMT  
		Size: 11.3 MB (11323714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f913866909777fce146b3d1c6a81b811018e4bd5ba8ecd4d29168eb9dcced`  
		Last Modified: Tue, 09 Nov 2021 00:42:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.6-builder`

```console
$ docker pull caddy@sha256:ff70e636e338c1d1bf2761dc49582a08edc8e7edf86f6591bae3ede81eebcd6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `caddy:2.4.6-builder` - linux; amd64

```console
$ docker pull caddy@sha256:58018b2f6a30dbb45e39be3761a09af004a551296f8f92bf31bef97687b15742
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121074719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8dc98d3747bd25bdd8b095b563b0cfa728096f1be09b7e50f5d2f81dc350be4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Mon, 30 Aug 2021 21:44:05 GMT
RUN apk add --no-cache ca-certificates
# Mon, 30 Aug 2021 21:44:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 30 Aug 2021 21:44:06 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:20:44 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:22:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:22:49 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:22:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:22:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:22:50 GMT
WORKDIR /go
# Thu, 04 Nov 2021 20:51:38 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 20:51:38 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:22:21 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:22:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:22:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:22:24 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31adcdaf11c89113a810db23d523e549d634d7de695a72b0ce98a1f912101262`  
		Last Modified: Mon, 30 Aug 2021 22:01:00 GMT  
		Size: 281.5 KB (281508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b176561691ea11cfe541f3ee363a3aa67e3649eb3273bea62ebeea713eaecd`  
		Last Modified: Mon, 30 Aug 2021 22:00:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d416b4d4fcca0271f31d7d73ef5910b705bc9c7e6c47e2849f526c61323bba9`  
		Last Modified: Thu, 04 Nov 2021 20:33:02 GMT  
		Size: 110.1 MB (110106449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b6b52ae600093bcea2a88e347c180ddf79cf361a229c968ab134f79566115b`  
		Last Modified: Thu, 04 Nov 2021 20:32:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ce64c87030110c9e1fb28a88d6de9ab21bc642f56da365e029fef45bd40449`  
		Last Modified: Thu, 04 Nov 2021 20:52:00 GMT  
		Size: 6.6 MB (6626626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4745adbe391f6c84dabb01d0b9f46dcb4c3835b37d657188312f964bf2428113`  
		Last Modified: Tue, 09 Nov 2021 00:23:02 GMT  
		Size: 1.2 MB (1244972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29111d85c26db67c047d940076de17d7fa99ab44f4facbb7102429b421060b91`  
		Last Modified: Tue, 09 Nov 2021 00:23:02 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a321aa86f856c91169d31a96a1181ca0fb15d4fa785b01fd4f1db0a76ac5f438
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115556079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1759314115af8681edae8afa8c25d576e2bf7c430e2fcf6bdae1a6f520f4b6f5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Mon, 30 Aug 2021 21:49:40 GMT
RUN apk add --no-cache ca-certificates
# Mon, 30 Aug 2021 21:49:41 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 30 Aug 2021 21:49:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:50:01 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:53:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:53:24 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:53:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:53:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:53:27 GMT
WORKDIR /go
# Thu, 04 Nov 2021 21:26:48 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 21:26:48 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:50:03 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:50:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:50:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:50:07 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:50:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb221a547a2f49a13c3bbe14f37b0474b2066cece57c67c2fbc1fb07d89aad51`  
		Last Modified: Mon, 30 Aug 2021 22:04:54 GMT  
		Size: 281.7 KB (281671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2968f26f7f14fe309f1a7a85ad968b81a7daa93c078322a84eb5c4192326828`  
		Last Modified: Mon, 30 Aug 2021 22:04:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1662a83909f5aff655c7be6da1ffd97a579ec92c5839159187d230df4db0c304`  
		Last Modified: Thu, 04 Nov 2021 21:06:10 GMT  
		Size: 105.0 MB (104982787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247cd469be037fb4ffd6898dfee7159dc4dbb17525c62f11540b77badda787fe`  
		Last Modified: Thu, 04 Nov 2021 21:05:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52d5113b58e9eea7126b6573a103c6174f77e3f086440c6b60d013feeae55c9`  
		Last Modified: Thu, 04 Nov 2021 21:28:00 GMT  
		Size: 6.5 MB (6485880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053aa7bf00b68e2dd2854ce3cf420395833093ba5dbf21fcbe716d7c14129a82`  
		Last Modified: Tue, 09 Nov 2021 00:51:31 GMT  
		Size: 1.2 MB (1177578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba84a71092e7a8161d2aa6cb90f140a7a6a7ee304fd1143a4bedc91bdb8a3430`  
		Last Modified: Tue, 09 Nov 2021 00:51:30 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:898867984c20de5d0a90810f09c3aa0d59c45b55c878d65fa1986002494be562
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114460716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f422bda8d34cfaad33778dcbf74db88e84c362e26c97e5ecb7e52bc0aed977c2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Mon, 30 Aug 2021 23:51:38 GMT
RUN apk add --no-cache ca-certificates
# Mon, 30 Aug 2021 23:51:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 30 Aug 2021 23:51:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:00:39 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 21:03:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 21:03:56 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 21:03:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:03:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 21:03:59 GMT
WORKDIR /go
# Thu, 04 Nov 2021 22:24:32 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 22:24:32 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:58:01 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:58:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:58:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:58:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:58:05 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9417f62ae10851eaf03f096c21f2848fdfe2517baf1faffe0a25f4a1f9853e31`  
		Last Modified: Tue, 31 Aug 2021 00:14:21 GMT  
		Size: 280.8 KB (280829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15fcbf7d3458d8a294b9a3c72856e5e7ba1372b93f8fc485abecc73f5a8c9b6`  
		Last Modified: Tue, 31 Aug 2021 00:14:21 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83145a0dc91bcfd39d1372eacfa0b0edd49fbd853a8805d09bc3c801ec17707`  
		Last Modified: Thu, 04 Nov 2021 21:24:35 GMT  
		Size: 104.8 MB (104787212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56a13d9f75fefe8df6818c553071626370c07285a8579c71d061dd3958ab9e9`  
		Last Modified: Thu, 04 Nov 2021 21:09:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a883856d1a9eb72feb215725e23c34ff4e13cc0bdba2c76df4ff5a281950a34d`  
		Last Modified: Thu, 04 Nov 2021 22:25:46 GMT  
		Size: 5.8 MB (5785275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce6cdc3c3bebb2bf176add262391b9b35a554c02e1031b6809d950661a432fe`  
		Last Modified: Tue, 09 Nov 2021 00:59:28 GMT  
		Size: 1.2 MB (1176263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699c5f30dbc0681a9241c9e446110c0ff7a3228da9ef73377eddfec9167018af`  
		Last Modified: Tue, 09 Nov 2021 00:59:27 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:465390cedcb9fff08eb002c4722d69e56f05c3c60f953da3cfb449ae162140c6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115238050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eddb3be5e644425a129daa8ef25fa1990904790212c12c1037f9acff4e54e6d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Tue, 12 Oct 2021 19:50:31 GMT
RUN apk add --no-cache ca-certificates
# Tue, 12 Oct 2021 19:50:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 12 Oct 2021 19:50:33 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:44:49 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:46:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:46:13 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:46:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:46:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:46:16 GMT
WORKDIR /go
# Thu, 04 Nov 2021 21:13:57 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 21:13:58 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:39:47 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:39:47 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:39:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:39:51 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:39:51 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb74239f2a0c13b654df471372048f7785978cbe6bf5ddc6773d88218ad689f0`  
		Last Modified: Tue, 12 Oct 2021 19:56:27 GMT  
		Size: 281.5 KB (281470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8ec004bf6b17206854367316e34aa51b7f5ff2f447e6c66498b2922dfad207`  
		Last Modified: Tue, 12 Oct 2021 19:56:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2dd7c0ce8a9709408ba750c27f660c1821df16fc1588b83103c14f5c982410`  
		Last Modified: Thu, 04 Nov 2021 20:55:18 GMT  
		Size: 104.4 MB (104362226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51b802c83dca96aee9527f6b9430dfb8d84cc63a0dfb77abd3fc70b35661b68`  
		Last Modified: Thu, 04 Nov 2021 20:55:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b82d2b3afe06ceb5e9038414bd86eaa29b64d9ca539a8d7f0a9a97d89c0ec4`  
		Last Modified: Thu, 04 Nov 2021 21:14:36 GMT  
		Size: 6.7 MB (6733703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6348d8e1d75893311f870eec10215eaead24e452e1ad2a6ae81e2b276e3cca2`  
		Last Modified: Tue, 09 Nov 2021 00:40:33 GMT  
		Size: 1.1 MB (1148135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a51eb07dd20f1949799c418f754133ca1fc5b646673e8ac9d111563dbc589f0`  
		Last Modified: Tue, 09 Nov 2021 00:40:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:2336a18de17f2c4072c9c0307696854edf929dcb82a60b90f55259a69eeb600a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (114036993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b00aa91420fc4f22cea6aab5ff77b36da6f5a53aa4614f04c4434e09de4e6f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Tue, 31 Aug 2021 00:28:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 31 Aug 2021 00:29:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 31 Aug 2021 00:29:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:35:29 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 21:37:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 21:38:07 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 21:38:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:38:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 21:38:27 GMT
WORKDIR /go
# Thu, 04 Nov 2021 23:44:35 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 23:44:36 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 02:42:23 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 02:42:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 02:42:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 02:42:49 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 02:42:55 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4539d90ff594fe73c1a1e31b2230e539a965f33143a3c9fbd89507336ed283c2`  
		Last Modified: Tue, 31 Aug 2021 00:52:27 GMT  
		Size: 283.6 KB (283640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a17d0ec6ff5411e524016f0ac7033cf7a0a8935f7a5e299d4d7acaad208b26`  
		Last Modified: Tue, 31 Aug 2021 00:52:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34c4f0757f32d139833674c31fd061ecab0806960999b78a42e97fccf03c17b`  
		Last Modified: Thu, 04 Nov 2021 21:55:32 GMT  
		Size: 102.7 MB (102722966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f044c2212367ff5cf5f5f5c673ad6d3feae574970990f8f78507c3ac07e3640`  
		Last Modified: Thu, 04 Nov 2021 21:54:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428a3c7c0c1bff96a1ad7f93a7663935ca506020c92db68c2c71b978a2e6ed00`  
		Last Modified: Thu, 04 Nov 2021 23:45:27 GMT  
		Size: 7.1 MB (7097367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c99d2cd9325e8349becf942ed19b5842c0c2199ce5cbca707223e3419ebb52`  
		Last Modified: Tue, 09 Nov 2021 02:43:49 GMT  
		Size: 1.1 MB (1120017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2118cc3ec9b4efe4249b876ec149d807c563e41337b16031f2189b0934bb4744`  
		Last Modified: Tue, 09 Nov 2021 02:43:52 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - linux; s390x

```console
$ docker pull caddy@sha256:504417781112a6da613e5dbf96701f333e86c02c15ee528bcfc69a914cb5b99c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118475563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6cfef420950dbccc42ede323157843e6c2451cefbb4b472fc259ac9e90a0708`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Mon, 30 Aug 2021 21:44:33 GMT
RUN apk add --no-cache ca-certificates
# Mon, 30 Aug 2021 21:44:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 30 Aug 2021 21:44:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:42:32 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:44:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:44:06 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:44:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:44:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:44:07 GMT
WORKDIR /go
# Thu, 04 Nov 2021 21:16:26 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 21:16:27 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:41:36 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:41:36 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:41:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:41:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:41:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316d1588ef06afb0d7a96646bb3a1367bce295885797fd976945ed318a4eb9c`  
		Last Modified: Mon, 30 Aug 2021 21:59:27 GMT  
		Size: 281.9 KB (281927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e156a554eded13f9baa4042fb4d12b879560bebfd8aca837bf0b52669f7932`  
		Last Modified: Mon, 30 Aug 2021 21:59:26 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe04792d0475ac041009f3ca62bcc0dc03a26292d21b32216bc2f3e666c2d5b`  
		Last Modified: Thu, 04 Nov 2021 20:52:06 GMT  
		Size: 107.7 MB (107663718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6416455ccb8f772096f018fb9032102e6439950a45d68d4188fdfde5d9a87ded`  
		Last Modified: Thu, 04 Nov 2021 20:51:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6952a3ac2d6398e7268d236bf7d0cee103719b380aebea5fb6aabd2e45c04ed1`  
		Last Modified: Thu, 04 Nov 2021 21:17:06 GMT  
		Size: 6.7 MB (6722226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39fdad6edb5004df0acf851fcf3b0cf9d8cdfeaa9913d04f595517236869eef`  
		Last Modified: Tue, 09 Nov 2021 00:42:30 GMT  
		Size: 1.2 MB (1203510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0be2e59b91c38d78efc2f40a152bdd89dd964e653984267002b1453226e9d2e`  
		Last Modified: Tue, 09 Nov 2021 00:42:30 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - windows version 10.0.17763.2300; amd64

```console
$ docker pull caddy@sha256:4d2914c283fcdb42d19719132d7efbfbfe7ad8af1d9cd5c071bf854233987587
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2878964819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b401c7e3582848bc6ccadc1c70895573764efb0f83732c2863411e9419c08c35`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 13:26:17 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Nov 2021 13:26:18 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Nov 2021 13:26:19 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Nov 2021 13:26:20 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Nov 2021 13:27:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:27:38 GMT
ENV GOPATH=C:\go
# Wed, 10 Nov 2021 13:28:31 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Nov 2021 13:28:32 GMT
ENV GOLANG_VERSION=1.17.3
# Wed, 10 Nov 2021 13:31:30 GMT
RUN $url = 'https://dl.google.com/go/go1.17.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e78684b955742e215926204afc6ed62b9d165b509e25a687d62902516f08726b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:31:35 GMT
WORKDIR C:\go
# Wed, 10 Nov 2021 20:17:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:17:50 GMT
ENV XCADDY_VERSION=v0.2.0
# Wed, 10 Nov 2021 20:17:51 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:17:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Nov 2021 20:18:44 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Nov 2021 20:18:45 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f32622fe466bd678a47b75fa13ebb7781336e6a776a22f424036aa8e91fe1d`  
		Last Modified: Wed, 10 Nov 2021 14:05:07 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d684ea4a6b52df2d3b5c7f7876e3b784ff1def8eb60f9637d920f4e0e7870b`  
		Last Modified: Wed, 10 Nov 2021 14:05:03 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ff61f0f89258dd1f49b766ef30baddd8f3e3821737778748ba95b52c1a480c`  
		Last Modified: Wed, 10 Nov 2021 14:05:03 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16dc9a497b44a664b28524686ca0e75c6a244af505429f54f80a6aaa96c7af9`  
		Last Modified: Wed, 10 Nov 2021 14:05:04 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e724f5e2b6e2fb2598ad100e7efa9cf30fe013f56537a5587d8e8868ae82d50`  
		Last Modified: Wed, 10 Nov 2021 14:05:09 GMT  
		Size: 25.4 MB (25446198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84e37bf01f689e54241d5e76695c5cbcc3313f3f8a85748e9d086c6cf3e4c3d`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f6ed9286b06435dae34f3d3e03f2c62a4415e3703740a83381b4ac0a3d1804`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 325.4 KB (325448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd53ef82415224427ba6005a3993a50da833e74dd65f413ede222760ab73155`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322051166b18395731c110a7ced59dc83924ac45736b482be8611e491ce9be22`  
		Last Modified: Wed, 10 Nov 2021 14:05:34 GMT  
		Size: 145.4 MB (145394728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7588b640c5b448c06e31f55936d39ebd92c0050d9b2daf5a86f09841d0ac6e68`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab8b7df216099a8c01f65cacfd0d07bfb8fe6ef211d5dbc6b897ceab643aa54`  
		Last Modified: Wed, 10 Nov 2021 20:21:41 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e1af14b4ab45cfdf867d71debb12ba16dc9770a11af54ec694004f8828280f`  
		Last Modified: Wed, 10 Nov 2021 20:21:38 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18305c1b79b992f30e786ccaa7379fba16154663b28f19d088c9b1750fe53f12`  
		Last Modified: Wed, 10 Nov 2021 20:21:38 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c926d89c22fc6adf4e181145a724ed23dacf28e12d58b7e7f75d69c4239ea2f0`  
		Last Modified: Wed, 10 Nov 2021 20:21:38 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb704654cf062fe78ae7674ea38cb7e81ac8f2b26f74c295489abf19dd4d206`  
		Last Modified: Wed, 10 Nov 2021 20:21:39 GMT  
		Size: 1.7 MB (1658702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da89e3439fa9c9e9d4cde6c4aca2fb1796d9dfceec37d31d351e2005a188b389`  
		Last Modified: Wed, 10 Nov 2021 20:21:38 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder` - windows version 10.0.14393.4770; amd64

```console
$ docker pull caddy@sha256:96a88b09cecf23cff2a8006ea25f1e037f50d01a9c74d2d3769f8bb228d2b768
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6450468916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fcd7b2f02771fd0b23831a7e603a01713fad078e5e205d745958ee47f638e5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 13:31:46 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Nov 2021 13:31:47 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Nov 2021 13:31:48 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Nov 2021 13:31:49 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Nov 2021 13:33:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:33:37 GMT
ENV GOPATH=C:\go
# Wed, 10 Nov 2021 13:34:34 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Nov 2021 13:34:35 GMT
ENV GOLANG_VERSION=1.17.3
# Wed, 10 Nov 2021 13:37:32 GMT
RUN $url = 'https://dl.google.com/go/go1.17.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e78684b955742e215926204afc6ed62b9d165b509e25a687d62902516f08726b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:37:37 GMT
WORKDIR C:\go
# Wed, 10 Nov 2021 20:18:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:18:53 GMT
ENV XCADDY_VERSION=v0.2.0
# Wed, 10 Nov 2021 20:18:54 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:18:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Nov 2021 20:19:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Nov 2021 20:19:56 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a0c69f83a30944f5afdc948b3583f1418f71f3ae5a02382610f0898eb501f9`  
		Last Modified: Wed, 10 Nov 2021 14:05:54 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e4bea9e4e2ccac41591b4aed9981453c554ca498a23d01a69638d6ccab7016`  
		Last Modified: Wed, 10 Nov 2021 14:05:52 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b36358e1913c99dc66fbbca2e4c0f8472796bf33ceeb7fdc02d2b7096b1208d`  
		Last Modified: Wed, 10 Nov 2021 14:05:52 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d071f5d45753629193f76196d769df9ff71ce3a39e5b10a16ff571cdb071a902`  
		Last Modified: Wed, 10 Nov 2021 14:05:52 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79602be6489be8a0e5e82221cae33eae5692897081a79bfe959604121e2d0a4`  
		Last Modified: Wed, 10 Nov 2021 14:06:20 GMT  
		Size: 25.4 MB (25448073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30d749fb8ba78fba5cce783b8cbe233632a2ba5965d4b67168111396620aaa0`  
		Last Modified: Wed, 10 Nov 2021 14:05:50 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f08b5963e19f3d28aa336d06434d4efec179b4b813e4aa4222ab064bc180f7`  
		Last Modified: Wed, 10 Nov 2021 14:05:50 GMT  
		Size: 354.9 KB (354902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f381a7ed29624957c6a0c2539069229be83423497216e9b19872996d3eace018`  
		Last Modified: Wed, 10 Nov 2021 14:05:49 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9184646a18b279b69062ae625cf768031d03c297beca44a465b8265af80e7116`  
		Last Modified: Wed, 10 Nov 2021 14:06:25 GMT  
		Size: 149.9 MB (149917271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e2acfda5cf05f260961ec16cee7c5c9e5573783c8298319e6b38846cb3b98b`  
		Last Modified: Wed, 10 Nov 2021 14:05:49 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f8275e6d67e00182a573a1fea89b6fbafd29fdd9e6991bec289907772e366`  
		Last Modified: Wed, 10 Nov 2021 20:21:59 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f675d50b479c34b5e127a7560cec6198d6c06464747188b22904543e0919ffe`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dba2d80865d737653a9a4ff2db1fcac88ce9bf3521d9e7f6dc8116fd16a99b`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272648eb620ef88b428e4aac8f782d100c4e64bb6f14073ee16b5b89a3b12967`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b51ab7213b8db3f0e51ace7c64b811e81a3d838148d7c41c3a58a9ffd1eb66`  
		Last Modified: Wed, 10 Nov 2021 20:21:58 GMT  
		Size: 1.6 MB (1639511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd676bfb740256d3eae7ac606f73a7d0ad09121f54eacd3ffdeff570e4b73bd1`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.6-builder-alpine`

```console
$ docker pull caddy@sha256:79350de5d5c17d2eea90b4a8d8b8fdf5e200d7b3173a1bcb4b52ac4c7c7b901c
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
$ docker pull caddy@sha256:58018b2f6a30dbb45e39be3761a09af004a551296f8f92bf31bef97687b15742
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121074719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8dc98d3747bd25bdd8b095b563b0cfa728096f1be09b7e50f5d2f81dc350be4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Mon, 30 Aug 2021 21:44:05 GMT
RUN apk add --no-cache ca-certificates
# Mon, 30 Aug 2021 21:44:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 30 Aug 2021 21:44:06 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:20:44 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:22:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:22:49 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:22:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:22:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:22:50 GMT
WORKDIR /go
# Thu, 04 Nov 2021 20:51:38 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 20:51:38 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:22:21 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:22:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:22:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:22:24 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31adcdaf11c89113a810db23d523e549d634d7de695a72b0ce98a1f912101262`  
		Last Modified: Mon, 30 Aug 2021 22:01:00 GMT  
		Size: 281.5 KB (281508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b176561691ea11cfe541f3ee363a3aa67e3649eb3273bea62ebeea713eaecd`  
		Last Modified: Mon, 30 Aug 2021 22:00:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d416b4d4fcca0271f31d7d73ef5910b705bc9c7e6c47e2849f526c61323bba9`  
		Last Modified: Thu, 04 Nov 2021 20:33:02 GMT  
		Size: 110.1 MB (110106449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b6b52ae600093bcea2a88e347c180ddf79cf361a229c968ab134f79566115b`  
		Last Modified: Thu, 04 Nov 2021 20:32:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ce64c87030110c9e1fb28a88d6de9ab21bc642f56da365e029fef45bd40449`  
		Last Modified: Thu, 04 Nov 2021 20:52:00 GMT  
		Size: 6.6 MB (6626626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4745adbe391f6c84dabb01d0b9f46dcb4c3835b37d657188312f964bf2428113`  
		Last Modified: Tue, 09 Nov 2021 00:23:02 GMT  
		Size: 1.2 MB (1244972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29111d85c26db67c047d940076de17d7fa99ab44f4facbb7102429b421060b91`  
		Last Modified: Tue, 09 Nov 2021 00:23:02 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a321aa86f856c91169d31a96a1181ca0fb15d4fa785b01fd4f1db0a76ac5f438
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115556079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1759314115af8681edae8afa8c25d576e2bf7c430e2fcf6bdae1a6f520f4b6f5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Mon, 30 Aug 2021 21:49:40 GMT
RUN apk add --no-cache ca-certificates
# Mon, 30 Aug 2021 21:49:41 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 30 Aug 2021 21:49:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:50:01 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:53:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:53:24 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:53:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:53:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:53:27 GMT
WORKDIR /go
# Thu, 04 Nov 2021 21:26:48 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 21:26:48 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:50:03 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:50:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:50:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:50:07 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:50:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb221a547a2f49a13c3bbe14f37b0474b2066cece57c67c2fbc1fb07d89aad51`  
		Last Modified: Mon, 30 Aug 2021 22:04:54 GMT  
		Size: 281.7 KB (281671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2968f26f7f14fe309f1a7a85ad968b81a7daa93c078322a84eb5c4192326828`  
		Last Modified: Mon, 30 Aug 2021 22:04:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1662a83909f5aff655c7be6da1ffd97a579ec92c5839159187d230df4db0c304`  
		Last Modified: Thu, 04 Nov 2021 21:06:10 GMT  
		Size: 105.0 MB (104982787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247cd469be037fb4ffd6898dfee7159dc4dbb17525c62f11540b77badda787fe`  
		Last Modified: Thu, 04 Nov 2021 21:05:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52d5113b58e9eea7126b6573a103c6174f77e3f086440c6b60d013feeae55c9`  
		Last Modified: Thu, 04 Nov 2021 21:28:00 GMT  
		Size: 6.5 MB (6485880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053aa7bf00b68e2dd2854ce3cf420395833093ba5dbf21fcbe716d7c14129a82`  
		Last Modified: Tue, 09 Nov 2021 00:51:31 GMT  
		Size: 1.2 MB (1177578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba84a71092e7a8161d2aa6cb90f140a7a6a7ee304fd1143a4bedc91bdb8a3430`  
		Last Modified: Tue, 09 Nov 2021 00:51:30 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:898867984c20de5d0a90810f09c3aa0d59c45b55c878d65fa1986002494be562
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114460716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f422bda8d34cfaad33778dcbf74db88e84c362e26c97e5ecb7e52bc0aed977c2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Mon, 30 Aug 2021 23:51:38 GMT
RUN apk add --no-cache ca-certificates
# Mon, 30 Aug 2021 23:51:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 30 Aug 2021 23:51:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:00:39 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 21:03:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 21:03:56 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 21:03:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:03:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 21:03:59 GMT
WORKDIR /go
# Thu, 04 Nov 2021 22:24:32 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 22:24:32 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:58:01 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:58:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:58:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:58:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:58:05 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9417f62ae10851eaf03f096c21f2848fdfe2517baf1faffe0a25f4a1f9853e31`  
		Last Modified: Tue, 31 Aug 2021 00:14:21 GMT  
		Size: 280.8 KB (280829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15fcbf7d3458d8a294b9a3c72856e5e7ba1372b93f8fc485abecc73f5a8c9b6`  
		Last Modified: Tue, 31 Aug 2021 00:14:21 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83145a0dc91bcfd39d1372eacfa0b0edd49fbd853a8805d09bc3c801ec17707`  
		Last Modified: Thu, 04 Nov 2021 21:24:35 GMT  
		Size: 104.8 MB (104787212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56a13d9f75fefe8df6818c553071626370c07285a8579c71d061dd3958ab9e9`  
		Last Modified: Thu, 04 Nov 2021 21:09:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a883856d1a9eb72feb215725e23c34ff4e13cc0bdba2c76df4ff5a281950a34d`  
		Last Modified: Thu, 04 Nov 2021 22:25:46 GMT  
		Size: 5.8 MB (5785275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce6cdc3c3bebb2bf176add262391b9b35a554c02e1031b6809d950661a432fe`  
		Last Modified: Tue, 09 Nov 2021 00:59:28 GMT  
		Size: 1.2 MB (1176263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699c5f30dbc0681a9241c9e446110c0ff7a3228da9ef73377eddfec9167018af`  
		Last Modified: Tue, 09 Nov 2021 00:59:27 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:465390cedcb9fff08eb002c4722d69e56f05c3c60f953da3cfb449ae162140c6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115238050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eddb3be5e644425a129daa8ef25fa1990904790212c12c1037f9acff4e54e6d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Tue, 12 Oct 2021 19:50:31 GMT
RUN apk add --no-cache ca-certificates
# Tue, 12 Oct 2021 19:50:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 12 Oct 2021 19:50:33 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:44:49 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:46:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:46:13 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:46:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:46:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:46:16 GMT
WORKDIR /go
# Thu, 04 Nov 2021 21:13:57 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 21:13:58 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:39:47 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:39:47 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:39:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:39:51 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:39:51 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb74239f2a0c13b654df471372048f7785978cbe6bf5ddc6773d88218ad689f0`  
		Last Modified: Tue, 12 Oct 2021 19:56:27 GMT  
		Size: 281.5 KB (281470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8ec004bf6b17206854367316e34aa51b7f5ff2f447e6c66498b2922dfad207`  
		Last Modified: Tue, 12 Oct 2021 19:56:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2dd7c0ce8a9709408ba750c27f660c1821df16fc1588b83103c14f5c982410`  
		Last Modified: Thu, 04 Nov 2021 20:55:18 GMT  
		Size: 104.4 MB (104362226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51b802c83dca96aee9527f6b9430dfb8d84cc63a0dfb77abd3fc70b35661b68`  
		Last Modified: Thu, 04 Nov 2021 20:55:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b82d2b3afe06ceb5e9038414bd86eaa29b64d9ca539a8d7f0a9a97d89c0ec4`  
		Last Modified: Thu, 04 Nov 2021 21:14:36 GMT  
		Size: 6.7 MB (6733703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6348d8e1d75893311f870eec10215eaead24e452e1ad2a6ae81e2b276e3cca2`  
		Last Modified: Tue, 09 Nov 2021 00:40:33 GMT  
		Size: 1.1 MB (1148135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a51eb07dd20f1949799c418f754133ca1fc5b646673e8ac9d111563dbc589f0`  
		Last Modified: Tue, 09 Nov 2021 00:40:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:2336a18de17f2c4072c9c0307696854edf929dcb82a60b90f55259a69eeb600a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (114036993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b00aa91420fc4f22cea6aab5ff77b36da6f5a53aa4614f04c4434e09de4e6f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Tue, 31 Aug 2021 00:28:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 31 Aug 2021 00:29:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 31 Aug 2021 00:29:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:35:29 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 21:37:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 21:38:07 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 21:38:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:38:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 21:38:27 GMT
WORKDIR /go
# Thu, 04 Nov 2021 23:44:35 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 23:44:36 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 02:42:23 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 02:42:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 02:42:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 02:42:49 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 02:42:55 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4539d90ff594fe73c1a1e31b2230e539a965f33143a3c9fbd89507336ed283c2`  
		Last Modified: Tue, 31 Aug 2021 00:52:27 GMT  
		Size: 283.6 KB (283640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a17d0ec6ff5411e524016f0ac7033cf7a0a8935f7a5e299d4d7acaad208b26`  
		Last Modified: Tue, 31 Aug 2021 00:52:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34c4f0757f32d139833674c31fd061ecab0806960999b78a42e97fccf03c17b`  
		Last Modified: Thu, 04 Nov 2021 21:55:32 GMT  
		Size: 102.7 MB (102722966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f044c2212367ff5cf5f5f5c673ad6d3feae574970990f8f78507c3ac07e3640`  
		Last Modified: Thu, 04 Nov 2021 21:54:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428a3c7c0c1bff96a1ad7f93a7663935ca506020c92db68c2c71b978a2e6ed00`  
		Last Modified: Thu, 04 Nov 2021 23:45:27 GMT  
		Size: 7.1 MB (7097367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c99d2cd9325e8349becf942ed19b5842c0c2199ce5cbca707223e3419ebb52`  
		Last Modified: Tue, 09 Nov 2021 02:43:49 GMT  
		Size: 1.1 MB (1120017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2118cc3ec9b4efe4249b876ec149d807c563e41337b16031f2189b0934bb4744`  
		Last Modified: Tue, 09 Nov 2021 02:43:52 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:504417781112a6da613e5dbf96701f333e86c02c15ee528bcfc69a914cb5b99c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118475563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6cfef420950dbccc42ede323157843e6c2451cefbb4b472fc259ac9e90a0708`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Mon, 30 Aug 2021 21:44:33 GMT
RUN apk add --no-cache ca-certificates
# Mon, 30 Aug 2021 21:44:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 30 Aug 2021 21:44:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:42:32 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:44:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:44:06 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:44:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:44:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:44:07 GMT
WORKDIR /go
# Thu, 04 Nov 2021 21:16:26 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 21:16:27 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:41:36 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:41:36 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:41:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:41:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:41:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316d1588ef06afb0d7a96646bb3a1367bce295885797fd976945ed318a4eb9c`  
		Last Modified: Mon, 30 Aug 2021 21:59:27 GMT  
		Size: 281.9 KB (281927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e156a554eded13f9baa4042fb4d12b879560bebfd8aca837bf0b52669f7932`  
		Last Modified: Mon, 30 Aug 2021 21:59:26 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe04792d0475ac041009f3ca62bcc0dc03a26292d21b32216bc2f3e666c2d5b`  
		Last Modified: Thu, 04 Nov 2021 20:52:06 GMT  
		Size: 107.7 MB (107663718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6416455ccb8f772096f018fb9032102e6439950a45d68d4188fdfde5d9a87ded`  
		Last Modified: Thu, 04 Nov 2021 20:51:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6952a3ac2d6398e7268d236bf7d0cee103719b380aebea5fb6aabd2e45c04ed1`  
		Last Modified: Thu, 04 Nov 2021 21:17:06 GMT  
		Size: 6.7 MB (6722226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39fdad6edb5004df0acf851fcf3b0cf9d8cdfeaa9913d04f595517236869eef`  
		Last Modified: Tue, 09 Nov 2021 00:42:30 GMT  
		Size: 1.2 MB (1203510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0be2e59b91c38d78efc2f40a152bdd89dd964e653984267002b1453226e9d2e`  
		Last Modified: Tue, 09 Nov 2021 00:42:30 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.6-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:8bdbf970abe748608ce652f507707eccf33bc6cd57a25e6bdfaec47ae0353860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `caddy:2.4.6-builder-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull caddy@sha256:4d2914c283fcdb42d19719132d7efbfbfe7ad8af1d9cd5c071bf854233987587
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2878964819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b401c7e3582848bc6ccadc1c70895573764efb0f83732c2863411e9419c08c35`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 13:26:17 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Nov 2021 13:26:18 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Nov 2021 13:26:19 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Nov 2021 13:26:20 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Nov 2021 13:27:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:27:38 GMT
ENV GOPATH=C:\go
# Wed, 10 Nov 2021 13:28:31 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Nov 2021 13:28:32 GMT
ENV GOLANG_VERSION=1.17.3
# Wed, 10 Nov 2021 13:31:30 GMT
RUN $url = 'https://dl.google.com/go/go1.17.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e78684b955742e215926204afc6ed62b9d165b509e25a687d62902516f08726b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:31:35 GMT
WORKDIR C:\go
# Wed, 10 Nov 2021 20:17:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:17:50 GMT
ENV XCADDY_VERSION=v0.2.0
# Wed, 10 Nov 2021 20:17:51 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:17:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Nov 2021 20:18:44 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Nov 2021 20:18:45 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f32622fe466bd678a47b75fa13ebb7781336e6a776a22f424036aa8e91fe1d`  
		Last Modified: Wed, 10 Nov 2021 14:05:07 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d684ea4a6b52df2d3b5c7f7876e3b784ff1def8eb60f9637d920f4e0e7870b`  
		Last Modified: Wed, 10 Nov 2021 14:05:03 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ff61f0f89258dd1f49b766ef30baddd8f3e3821737778748ba95b52c1a480c`  
		Last Modified: Wed, 10 Nov 2021 14:05:03 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16dc9a497b44a664b28524686ca0e75c6a244af505429f54f80a6aaa96c7af9`  
		Last Modified: Wed, 10 Nov 2021 14:05:04 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e724f5e2b6e2fb2598ad100e7efa9cf30fe013f56537a5587d8e8868ae82d50`  
		Last Modified: Wed, 10 Nov 2021 14:05:09 GMT  
		Size: 25.4 MB (25446198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84e37bf01f689e54241d5e76695c5cbcc3313f3f8a85748e9d086c6cf3e4c3d`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f6ed9286b06435dae34f3d3e03f2c62a4415e3703740a83381b4ac0a3d1804`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 325.4 KB (325448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd53ef82415224427ba6005a3993a50da833e74dd65f413ede222760ab73155`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322051166b18395731c110a7ced59dc83924ac45736b482be8611e491ce9be22`  
		Last Modified: Wed, 10 Nov 2021 14:05:34 GMT  
		Size: 145.4 MB (145394728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7588b640c5b448c06e31f55936d39ebd92c0050d9b2daf5a86f09841d0ac6e68`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab8b7df216099a8c01f65cacfd0d07bfb8fe6ef211d5dbc6b897ceab643aa54`  
		Last Modified: Wed, 10 Nov 2021 20:21:41 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e1af14b4ab45cfdf867d71debb12ba16dc9770a11af54ec694004f8828280f`  
		Last Modified: Wed, 10 Nov 2021 20:21:38 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18305c1b79b992f30e786ccaa7379fba16154663b28f19d088c9b1750fe53f12`  
		Last Modified: Wed, 10 Nov 2021 20:21:38 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c926d89c22fc6adf4e181145a724ed23dacf28e12d58b7e7f75d69c4239ea2f0`  
		Last Modified: Wed, 10 Nov 2021 20:21:38 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb704654cf062fe78ae7674ea38cb7e81ac8f2b26f74c295489abf19dd4d206`  
		Last Modified: Wed, 10 Nov 2021 20:21:39 GMT  
		Size: 1.7 MB (1658702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da89e3439fa9c9e9d4cde6c4aca2fb1796d9dfceec37d31d351e2005a188b389`  
		Last Modified: Wed, 10 Nov 2021 20:21:38 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.6-builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:616283cce0c82245c2685b723e1f9538d1c4e926a9ad143dd66bf0e299b64ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `caddy:2.4.6-builder-windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull caddy@sha256:96a88b09cecf23cff2a8006ea25f1e037f50d01a9c74d2d3769f8bb228d2b768
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6450468916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fcd7b2f02771fd0b23831a7e603a01713fad078e5e205d745958ee47f638e5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 13:31:46 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Nov 2021 13:31:47 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Nov 2021 13:31:48 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Nov 2021 13:31:49 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Nov 2021 13:33:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:33:37 GMT
ENV GOPATH=C:\go
# Wed, 10 Nov 2021 13:34:34 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Nov 2021 13:34:35 GMT
ENV GOLANG_VERSION=1.17.3
# Wed, 10 Nov 2021 13:37:32 GMT
RUN $url = 'https://dl.google.com/go/go1.17.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e78684b955742e215926204afc6ed62b9d165b509e25a687d62902516f08726b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:37:37 GMT
WORKDIR C:\go
# Wed, 10 Nov 2021 20:18:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:18:53 GMT
ENV XCADDY_VERSION=v0.2.0
# Wed, 10 Nov 2021 20:18:54 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:18:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Nov 2021 20:19:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Nov 2021 20:19:56 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a0c69f83a30944f5afdc948b3583f1418f71f3ae5a02382610f0898eb501f9`  
		Last Modified: Wed, 10 Nov 2021 14:05:54 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e4bea9e4e2ccac41591b4aed9981453c554ca498a23d01a69638d6ccab7016`  
		Last Modified: Wed, 10 Nov 2021 14:05:52 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b36358e1913c99dc66fbbca2e4c0f8472796bf33ceeb7fdc02d2b7096b1208d`  
		Last Modified: Wed, 10 Nov 2021 14:05:52 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d071f5d45753629193f76196d769df9ff71ce3a39e5b10a16ff571cdb071a902`  
		Last Modified: Wed, 10 Nov 2021 14:05:52 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79602be6489be8a0e5e82221cae33eae5692897081a79bfe959604121e2d0a4`  
		Last Modified: Wed, 10 Nov 2021 14:06:20 GMT  
		Size: 25.4 MB (25448073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30d749fb8ba78fba5cce783b8cbe233632a2ba5965d4b67168111396620aaa0`  
		Last Modified: Wed, 10 Nov 2021 14:05:50 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f08b5963e19f3d28aa336d06434d4efec179b4b813e4aa4222ab064bc180f7`  
		Last Modified: Wed, 10 Nov 2021 14:05:50 GMT  
		Size: 354.9 KB (354902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f381a7ed29624957c6a0c2539069229be83423497216e9b19872996d3eace018`  
		Last Modified: Wed, 10 Nov 2021 14:05:49 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9184646a18b279b69062ae625cf768031d03c297beca44a465b8265af80e7116`  
		Last Modified: Wed, 10 Nov 2021 14:06:25 GMT  
		Size: 149.9 MB (149917271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e2acfda5cf05f260961ec16cee7c5c9e5573783c8298319e6b38846cb3b98b`  
		Last Modified: Wed, 10 Nov 2021 14:05:49 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f8275e6d67e00182a573a1fea89b6fbafd29fdd9e6991bec289907772e366`  
		Last Modified: Wed, 10 Nov 2021 20:21:59 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f675d50b479c34b5e127a7560cec6198d6c06464747188b22904543e0919ffe`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dba2d80865d737653a9a4ff2db1fcac88ce9bf3521d9e7f6dc8116fd16a99b`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272648eb620ef88b428e4aac8f782d100c4e64bb6f14073ee16b5b89a3b12967`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b51ab7213b8db3f0e51ace7c64b811e81a3d838148d7c41c3a58a9ffd1eb66`  
		Last Modified: Wed, 10 Nov 2021 20:21:58 GMT  
		Size: 1.6 MB (1639511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd676bfb740256d3eae7ac606f73a7d0ad09121f54eacd3ffdeff570e4b73bd1`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.6-windowsservercore`

```console
$ docker pull caddy@sha256:3864aebe0cb9d8ec8b0707762c6637cf9ad27a88bde3be6f9d0842eb01a19666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `caddy:2.4.6-windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull caddy@sha256:4a8d9dccf760a0249237dfcf9726c0eb1b06e0b19f5ff67cf8718f8da29507c5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718934999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea4590fabf41404b64c9e90299fd322ac88350fd817d631f26264b5915ed362`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:12:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Nov 2021 20:12:21 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:13:18 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Nov 2021 20:13:19 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Nov 2021 20:13:20 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Nov 2021 20:13:21 GMT
VOLUME [c:/config]
# Wed, 10 Nov 2021 20:13:22 GMT
VOLUME [c:/data]
# Wed, 10 Nov 2021 20:13:23 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 10 Nov 2021 20:13:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Nov 2021 20:13:25 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Nov 2021 20:13:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Nov 2021 20:13:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Nov 2021 20:13:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Nov 2021 20:13:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Nov 2021 20:13:30 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Nov 2021 20:13:31 GMT
EXPOSE 80
# Wed, 10 Nov 2021 20:13:32 GMT
EXPOSE 443
# Wed, 10 Nov 2021 20:13:33 GMT
EXPOSE 2019
# Wed, 10 Nov 2021 20:14:19 GMT
RUN caddy version
# Wed, 10 Nov 2021 20:14:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b6e8b6a9caee6f47bdb32f6ec53fd2836fc02cddea3324c72caf380622fc31`  
		Last Modified: Wed, 10 Nov 2021 20:20:37 GMT  
		Size: 370.6 KB (370576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0308f92ecf7a222e22b826cf5c198551ffc380b76ee3e8de67da904b4b02f873`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05df7693285564a1ff855781db06d1dab2fa702b5492fd55461fc675cefb47b6`  
		Last Modified: Wed, 10 Nov 2021 20:20:50 GMT  
		Size: 12.1 MB (12127869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a1d26d8d7789115491377813de4a8a0c15aa4772e3b22b229a4a061f4994d5`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766e31d6b0534ea731f651ccd59e3397360e7878802aaf90257635b0edd37086`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b6f52680a8e584e06bb957343f7acef41f8863af076fed0c94c583f6a6a8ea`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3be75f11ed2b624d7b0d85454d91e6ba425c4b11d179b44611f0353c75976a5`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bb0fed8a1d238828c7b967ddc9453e83dc38e811f50de90a87ca4a79677e3e`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3343adb9cf1bed7b331007eea1fb0bfdcdcc2a11c2c295d513a73d451d338298`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655ad263ab440756e44a5b758408a577f4ba4e960ae9daec72945afc3047553f`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09b8e61a4bbdc190857116fd8fc09cd71a5409e0bf984c7a033272b2ef5f5bb`  
		Last Modified: Wed, 10 Nov 2021 20:20:32 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9723996732fa25ff5ef95b4bd85c9ddf6dfd27408fe9e220bf0156031ade487d`  
		Last Modified: Wed, 10 Nov 2021 20:20:32 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d58c78cd1d1a8562bd34f68b10ada8622f98bf19ad87174e2a3810657e48e70`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67885c8112bf51b21d408141b4bf3b2e13f08f96cdcd873dc6ca1310bdf08f65`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77274081e32b6ce8f84a136cb45008f07cd542a8f2fa0cb8a355331280e27248`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acafd6faed9e989da5b7ca4bcf5d704b15d86d0b5076b645224a578b5453eb61`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109d2337e42e4f8cfc28c01475b5d1ab49d1e776006c622915ec2166c8fead72`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ee8d0bd71b0b4f05c46aa89f1434f50b4685f23ab7e0e092ae5f46e1d150ad`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd8ebab410bbbe5d576ac2f9ec8f4f2b9d251ae4a307bc8c11bb47165553f63`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 290.2 KB (290194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a550a1217bcfc790088e7a6d4f32ebdea15bae25f297c4683cb3dfc3e6c72e4d`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.4.6-windowsservercore` - windows version 10.0.14393.4770; amd64

```console
$ docker pull caddy@sha256:2c091f3638b3d3948ffa8c2d95a9be662e858768ffc52e366872371a68d003a1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6285957464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fb2d13bfaf3ee5703b28aa6d939cbfac5b14658e1e3e91bbae594e1c4b22a2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:15:34 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Nov 2021 20:15:35 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:16:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Nov 2021 20:16:39 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Nov 2021 20:16:40 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Nov 2021 20:16:41 GMT
VOLUME [c:/config]
# Wed, 10 Nov 2021 20:16:42 GMT
VOLUME [c:/data]
# Wed, 10 Nov 2021 20:16:43 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 10 Nov 2021 20:16:44 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Nov 2021 20:16:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Nov 2021 20:16:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Nov 2021 20:16:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Nov 2021 20:16:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Nov 2021 20:16:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Nov 2021 20:16:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Nov 2021 20:16:50 GMT
EXPOSE 80
# Wed, 10 Nov 2021 20:16:51 GMT
EXPOSE 443
# Wed, 10 Nov 2021 20:16:52 GMT
EXPOSE 2019
# Wed, 10 Nov 2021 20:17:30 GMT
RUN caddy version
# Wed, 10 Nov 2021 20:17:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224cfcc2d1317d73465188f71867febbba9a64bbfcdf83b35bccd662bdb25748`  
		Last Modified: Wed, 10 Nov 2021 20:21:11 GMT  
		Size: 366.8 KB (366836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98f673e7fe75a29f4060341dab79e20ad059162395f10fb1fc2504379d12f22`  
		Last Modified: Wed, 10 Nov 2021 20:21:10 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6dc3d9f8e8e85985894d372a912cae2cbc64cc10540262498597bbe8cad8c31`  
		Last Modified: Wed, 10 Nov 2021 20:21:24 GMT  
		Size: 12.2 MB (12158174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197a3f340985e5e76e3ae77fcbb9e208f521abbad0cfb8921d27d4afe569f280`  
		Last Modified: Wed, 10 Nov 2021 20:21:13 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1443a981044b58af1bae85624fffe4dde7c1759e6a5f930ddaf2eb70bc3185dd`  
		Last Modified: Wed, 10 Nov 2021 20:21:10 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1b023614dd84860e7a4fdd1855131b5478b9b747a40fc9383467934e48e310`  
		Last Modified: Wed, 10 Nov 2021 20:21:09 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daca4ab6367b318ae3a2df27bbe0c53c12ee1a0196fc4f43a43ec47acd74c7c`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a288866cea4075f0f825973ce9d3369dd9411f73c325ed870a5233b383476dbc`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea1c63b1b4cb8f39b59025d926f384679d17bb660eceafe7f7c9418dcdfad61`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b25f60f98964a2d03947e1dac0b01388ad6c9c65497e546f8efe7f2fdcd35e`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d10f21fe32d5dd37a74db003c1119b2aaba639690b10ad4c46d22e2699140fc`  
		Last Modified: Wed, 10 Nov 2021 20:21:06 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4bd5845100c889806835753480fb0016610fbfab35d197c6aa641d73c114ed`  
		Last Modified: Wed, 10 Nov 2021 20:21:06 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190767770423c20b77f963553559cfa26d18b490228ad11c4f9fcf62e6dcefd7`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab0412df33f87a4e77ce1ef8afc68a04cd9a9a56ce9a21e3494f4e4f7c1083a`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80edcc113a751c789aee343b18fdb12c9099cd642cf099ab6a962c7cb0bce8b`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d513b74afabeb0e8050ca955cdf8b72040cabc21350ab394862808bd4382649`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc99c5e78f676bc2fed853c2d43f71dedcbf29fe3a6f69f5d0bc1eabca7f8e98`  
		Last Modified: Wed, 10 Nov 2021 20:21:04 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1532dfe2f3d7f9a4d2eed5ac842a7b54e160fb4d856388e1153d0c6488bab749`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c6594f3623b09c0359fe4347b1981678cebb55cebad4bd683d4bc059e0a201`  
		Last Modified: Wed, 10 Nov 2021 20:21:04 GMT  
		Size: 316.3 KB (316295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c07c5e836014edc4e052889ecbe945aa470b434f2563726bd4f9684da37bfc1`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.6-windowsservercore-1809`

```console
$ docker pull caddy@sha256:4d8f28e3fbdc28a6ebdf57a867626560f0651157d3cf1cddaa279a9f57c34c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `caddy:2.4.6-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull caddy@sha256:4a8d9dccf760a0249237dfcf9726c0eb1b06e0b19f5ff67cf8718f8da29507c5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718934999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea4590fabf41404b64c9e90299fd322ac88350fd817d631f26264b5915ed362`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:12:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Nov 2021 20:12:21 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:13:18 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Nov 2021 20:13:19 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Nov 2021 20:13:20 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Nov 2021 20:13:21 GMT
VOLUME [c:/config]
# Wed, 10 Nov 2021 20:13:22 GMT
VOLUME [c:/data]
# Wed, 10 Nov 2021 20:13:23 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 10 Nov 2021 20:13:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Nov 2021 20:13:25 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Nov 2021 20:13:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Nov 2021 20:13:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Nov 2021 20:13:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Nov 2021 20:13:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Nov 2021 20:13:30 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Nov 2021 20:13:31 GMT
EXPOSE 80
# Wed, 10 Nov 2021 20:13:32 GMT
EXPOSE 443
# Wed, 10 Nov 2021 20:13:33 GMT
EXPOSE 2019
# Wed, 10 Nov 2021 20:14:19 GMT
RUN caddy version
# Wed, 10 Nov 2021 20:14:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b6e8b6a9caee6f47bdb32f6ec53fd2836fc02cddea3324c72caf380622fc31`  
		Last Modified: Wed, 10 Nov 2021 20:20:37 GMT  
		Size: 370.6 KB (370576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0308f92ecf7a222e22b826cf5c198551ffc380b76ee3e8de67da904b4b02f873`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05df7693285564a1ff855781db06d1dab2fa702b5492fd55461fc675cefb47b6`  
		Last Modified: Wed, 10 Nov 2021 20:20:50 GMT  
		Size: 12.1 MB (12127869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a1d26d8d7789115491377813de4a8a0c15aa4772e3b22b229a4a061f4994d5`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766e31d6b0534ea731f651ccd59e3397360e7878802aaf90257635b0edd37086`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b6f52680a8e584e06bb957343f7acef41f8863af076fed0c94c583f6a6a8ea`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3be75f11ed2b624d7b0d85454d91e6ba425c4b11d179b44611f0353c75976a5`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bb0fed8a1d238828c7b967ddc9453e83dc38e811f50de90a87ca4a79677e3e`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3343adb9cf1bed7b331007eea1fb0bfdcdcc2a11c2c295d513a73d451d338298`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655ad263ab440756e44a5b758408a577f4ba4e960ae9daec72945afc3047553f`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09b8e61a4bbdc190857116fd8fc09cd71a5409e0bf984c7a033272b2ef5f5bb`  
		Last Modified: Wed, 10 Nov 2021 20:20:32 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9723996732fa25ff5ef95b4bd85c9ddf6dfd27408fe9e220bf0156031ade487d`  
		Last Modified: Wed, 10 Nov 2021 20:20:32 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d58c78cd1d1a8562bd34f68b10ada8622f98bf19ad87174e2a3810657e48e70`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67885c8112bf51b21d408141b4bf3b2e13f08f96cdcd873dc6ca1310bdf08f65`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77274081e32b6ce8f84a136cb45008f07cd542a8f2fa0cb8a355331280e27248`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acafd6faed9e989da5b7ca4bcf5d704b15d86d0b5076b645224a578b5453eb61`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109d2337e42e4f8cfc28c01475b5d1ab49d1e776006c622915ec2166c8fead72`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ee8d0bd71b0b4f05c46aa89f1434f50b4685f23ab7e0e092ae5f46e1d150ad`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd8ebab410bbbe5d576ac2f9ec8f4f2b9d251ae4a307bc8c11bb47165553f63`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 290.2 KB (290194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a550a1217bcfc790088e7a6d4f32ebdea15bae25f297c4683cb3dfc3e6c72e4d`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.4.6-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:b399e4134eac2ed1e68a9f6d12fa6c2f89351edd4b13f45e687d84ee2c8c7891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `caddy:2.4.6-windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull caddy@sha256:2c091f3638b3d3948ffa8c2d95a9be662e858768ffc52e366872371a68d003a1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6285957464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fb2d13bfaf3ee5703b28aa6d939cbfac5b14658e1e3e91bbae594e1c4b22a2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:15:34 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Nov 2021 20:15:35 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:16:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Nov 2021 20:16:39 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Nov 2021 20:16:40 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Nov 2021 20:16:41 GMT
VOLUME [c:/config]
# Wed, 10 Nov 2021 20:16:42 GMT
VOLUME [c:/data]
# Wed, 10 Nov 2021 20:16:43 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 10 Nov 2021 20:16:44 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Nov 2021 20:16:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Nov 2021 20:16:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Nov 2021 20:16:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Nov 2021 20:16:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Nov 2021 20:16:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Nov 2021 20:16:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Nov 2021 20:16:50 GMT
EXPOSE 80
# Wed, 10 Nov 2021 20:16:51 GMT
EXPOSE 443
# Wed, 10 Nov 2021 20:16:52 GMT
EXPOSE 2019
# Wed, 10 Nov 2021 20:17:30 GMT
RUN caddy version
# Wed, 10 Nov 2021 20:17:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224cfcc2d1317d73465188f71867febbba9a64bbfcdf83b35bccd662bdb25748`  
		Last Modified: Wed, 10 Nov 2021 20:21:11 GMT  
		Size: 366.8 KB (366836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98f673e7fe75a29f4060341dab79e20ad059162395f10fb1fc2504379d12f22`  
		Last Modified: Wed, 10 Nov 2021 20:21:10 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6dc3d9f8e8e85985894d372a912cae2cbc64cc10540262498597bbe8cad8c31`  
		Last Modified: Wed, 10 Nov 2021 20:21:24 GMT  
		Size: 12.2 MB (12158174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197a3f340985e5e76e3ae77fcbb9e208f521abbad0cfb8921d27d4afe569f280`  
		Last Modified: Wed, 10 Nov 2021 20:21:13 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1443a981044b58af1bae85624fffe4dde7c1759e6a5f930ddaf2eb70bc3185dd`  
		Last Modified: Wed, 10 Nov 2021 20:21:10 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1b023614dd84860e7a4fdd1855131b5478b9b747a40fc9383467934e48e310`  
		Last Modified: Wed, 10 Nov 2021 20:21:09 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daca4ab6367b318ae3a2df27bbe0c53c12ee1a0196fc4f43a43ec47acd74c7c`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a288866cea4075f0f825973ce9d3369dd9411f73c325ed870a5233b383476dbc`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea1c63b1b4cb8f39b59025d926f384679d17bb660eceafe7f7c9418dcdfad61`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b25f60f98964a2d03947e1dac0b01388ad6c9c65497e546f8efe7f2fdcd35e`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d10f21fe32d5dd37a74db003c1119b2aaba639690b10ad4c46d22e2699140fc`  
		Last Modified: Wed, 10 Nov 2021 20:21:06 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4bd5845100c889806835753480fb0016610fbfab35d197c6aa641d73c114ed`  
		Last Modified: Wed, 10 Nov 2021 20:21:06 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190767770423c20b77f963553559cfa26d18b490228ad11c4f9fcf62e6dcefd7`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab0412df33f87a4e77ce1ef8afc68a04cd9a9a56ce9a21e3494f4e4f7c1083a`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80edcc113a751c789aee343b18fdb12c9099cd642cf099ab6a962c7cb0bce8b`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d513b74afabeb0e8050ca955cdf8b72040cabc21350ab394862808bd4382649`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc99c5e78f676bc2fed853c2d43f71dedcbf29fe3a6f69f5d0bc1eabca7f8e98`  
		Last Modified: Wed, 10 Nov 2021 20:21:04 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1532dfe2f3d7f9a4d2eed5ac842a7b54e160fb4d856388e1153d0c6488bab749`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c6594f3623b09c0359fe4347b1981678cebb55cebad4bd683d4bc059e0a201`  
		Last Modified: Wed, 10 Nov 2021 20:21:04 GMT  
		Size: 316.3 KB (316295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c07c5e836014edc4e052889ecbe945aa470b434f2563726bd4f9684da37bfc1`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:alpine`

```console
$ docker pull caddy@sha256:dbc76d658f90c3ce8f96d6a3ccc918d1694c586003eae68a6cf2282ce2ecf2ef
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
$ docker pull caddy@sha256:85a8daaf3706e847da86d456fb722edacb72a32360d333febccbf208f08e2be6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14847925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332a21201a47e70a89875163c9e41f0e78d6514d6e64aae618c3e2cc79b5e35d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:19:30 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:19:31 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:22:07 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:22:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:22:12 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:22:12 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:22:12 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:22:12 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:22:13 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:22:13 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:22:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:22:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:22:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:22:15 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:22:16 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:22:16 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:22:16 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:22:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d9d63a262eb117d9f55cf667904b985eb6dd9830783f17146a17a107a7ee19`  
		Last Modified: Tue, 07 Sep 2021 19:20:03 GMT  
		Size: 301.0 KB (301044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d54a459a500730b7153882903986d92e877f472e9d6ead142fab9dcb6464e1`  
		Last Modified: Tue, 07 Sep 2021 19:20:04 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12929046016b5f7547cb262dd7e97132958593eff9f30a3062729ed87f5f764f`  
		Last Modified: Tue, 09 Nov 2021 00:22:50 GMT  
		Size: 11.7 MB (11726452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2abe024ef8ac2567e428b8c753253b9670be99dad8f46607c895df6577f60ee`  
		Last Modified: Tue, 09 Nov 2021 00:22:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:84282af6d453c14c7875598e935faa6d1e7605067a6a212f69227bed1b97ae91
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14060404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4a22469cd1950a4d76a71bd95254b6b70d97f1d46d0ab846d9561937d7cee8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:49:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:49:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:49:32 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:49:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:49:39 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:49:39 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:49:40 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:49:40 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:49:41 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:49:41 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:49:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:49:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:49:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:49:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:49:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:49:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:49:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:49:45 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:49:45 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:49:46 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:49:46 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:49:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f254033e1bbf10f9a1641b6005ee6ae290bdec377e00d2e5290e33dc0eb8f9b6`  
		Last Modified: Tue, 07 Sep 2021 19:51:17 GMT  
		Size: 301.2 KB (301188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28038de9754eec9aa2df09a34c0d7029c335199166de56398d21fb595fd289dd`  
		Last Modified: Tue, 07 Sep 2021 19:51:17 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d17cc2aea86ad912ecd44f746238a440abd651aacc69ff04dcfdfa5e93193bb`  
		Last Modified: Tue, 09 Nov 2021 00:51:15 GMT  
		Size: 11.1 MB (11125785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cde1922177a05c9ac9c3cdb88d2492158258e3ddc64a6168bf7aa3d2087c3f5`  
		Last Modified: Tue, 09 Nov 2021 00:51:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:fb17cbc78aa551976f55685ba43b474671da9323631920b2411ef3ba47986f62
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13843483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9933538b9e4061a71c69dda3c1ac39f499b0a0c09fc86871a60a60b72576e0c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:57:36 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:57:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:57:30 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:57:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:57:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:57:37 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:57:37 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:57:38 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:57:38 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:57:39 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:57:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:57:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:57:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:57:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:57:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:57:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:57:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:57:42 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:57:43 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:57:43 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:57:44 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:57:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98c39987cd6455919d7455feed9aba93a44659ef658fbef5d4d52500beddac5`  
		Last Modified: Tue, 07 Sep 2021 19:59:13 GMT  
		Size: 300.4 KB (300356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e223cb6b0d911c9cc6575c496bc4f96f1968db869a8a07694f3f49897920f264`  
		Last Modified: Tue, 07 Sep 2021 19:59:13 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d8001745b5a3dedaa6b3a2bef5234f8612ac3d942269d2e18abbc1bfae84c8`  
		Last Modified: Tue, 09 Nov 2021 00:59:12 GMT  
		Size: 11.1 MB (11106727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bfb11f4ca256c6f83e7d7f05fdc548ce544492b765b72bad8fff802e114ec0`  
		Last Modified: Tue, 09 Nov 2021 00:59:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:dcc03368e7ff328ba4159eca9d88c2cb33e3ef4d8aaf9cec550f4f924c032616
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13757357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fca8f72561cf76363cdb806b321face6a1c9831e94d96c4966828a26b19962b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 14 Oct 2021 01:35:26 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 14 Oct 2021 01:35:28 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:39:19 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:39:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:39:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:39:23 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:39:24 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:39:25 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:39:26 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:39:27 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:39:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:39:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:39:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:39:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:39:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:39:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:39:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:39:35 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:39:36 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:39:37 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:39:38 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:39:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdae6629f9c73c56d66409172a1dcab55f533f8b62eb70c990c8e2cabcd7695`  
		Last Modified: Thu, 14 Oct 2021 01:36:31 GMT  
		Size: 301.0 KB (300992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3c515fae4831ae5dd272bcc27d7d3d3011d0f880b795b0aed1ce8c389c96bf`  
		Last Modified: Thu, 14 Oct 2021 01:36:30 GMT  
		Size: 5.8 KB (5752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce648197b75d827f9704483ccbcc884912ffb6a25728a39ddd0f717c3d534a46`  
		Last Modified: Tue, 09 Nov 2021 00:40:20 GMT  
		Size: 10.7 MB (10738633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d3751262c3b44d86e469c50ed19d1a632a37d420e471e3653d9c26c8d51ba6`  
		Last Modified: Tue, 09 Nov 2021 00:40:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:b1f36f28cb28be8e03baf5e564e8813cf57f65a907533db61acec3fc2ff7d337
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13423700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927f64bc8094cd853e2649145f44cf5cbc699568c2066c650c61db9865417dc5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:16:42 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:16:56 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 02:38:59 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 02:39:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 02:39:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 02:39:43 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 02:39:47 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 02:39:58 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 02:40:04 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 02:40:16 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 02:40:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 02:40:30 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 02:40:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 02:40:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 02:40:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 02:41:01 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 02:41:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 02:41:31 GMT
EXPOSE 80
# Tue, 09 Nov 2021 02:41:42 GMT
EXPOSE 443
# Tue, 09 Nov 2021 02:41:49 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 02:41:57 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 02:42:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d32e3566fcaa11540498ebdd9ecc55cd2e2dca73a6b62317657a9e75749272`  
		Last Modified: Tue, 07 Sep 2021 19:21:13 GMT  
		Size: 303.2 KB (303162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a831abca68890cbd7a89171bb93c9af5c1b102852f0f1f3326ff7c104ced90`  
		Last Modified: Tue, 07 Sep 2021 19:21:12 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef4a0928ede6ae0f23c1a955b08d450770842d163d8152b4ad7cb9333b4ac5b`  
		Last Modified: Tue, 09 Nov 2021 02:43:36 GMT  
		Size: 10.3 MB (10302268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6dff47d769c4013cb3ed7545b165cd303bac49d09576d80c78bfa8d9353b1bb`  
		Last Modified: Tue, 09 Nov 2021 02:43:34 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:7ceecb66639b47e4acb3acc566018228f83534b5a49f4a5306f4a6ae995cd13f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14234623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82585988e83eb76f3ebc0d2bb5323c9663491e28faa0819aa54296c142e686b3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:41:29 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:41:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:41:22 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:41:25 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:41:26 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:41:26 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:41:26 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:41:26 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:41:27 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:41:27 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:41:27 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:41:27 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:41:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9c7d5d2c4319fc2386cc1a009e57751b8d7a7d807ae0e867e4d6273e06731d`  
		Last Modified: Tue, 07 Sep 2021 19:42:43 GMT  
		Size: 301.5 KB (301462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c7b669e195c7cce7cf6d957130645125c1171c464622ceaa01378d18f24e37`  
		Last Modified: Tue, 07 Sep 2021 19:42:43 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931bdaaeb048d3dff8468154aa9eceea8e363d63dc61208df60553535bfe8f85`  
		Last Modified: Tue, 09 Nov 2021 00:42:20 GMT  
		Size: 11.3 MB (11323714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f913866909777fce146b3d1c6a81b811018e4bd5ba8ecd4d29168eb9dcced`  
		Last Modified: Tue, 09 Nov 2021 00:42:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder`

```console
$ docker pull caddy@sha256:ff70e636e338c1d1bf2761dc49582a08edc8e7edf86f6591bae3ede81eebcd6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:58018b2f6a30dbb45e39be3761a09af004a551296f8f92bf31bef97687b15742
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121074719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8dc98d3747bd25bdd8b095b563b0cfa728096f1be09b7e50f5d2f81dc350be4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Mon, 30 Aug 2021 21:44:05 GMT
RUN apk add --no-cache ca-certificates
# Mon, 30 Aug 2021 21:44:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 30 Aug 2021 21:44:06 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:20:44 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:22:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:22:49 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:22:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:22:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:22:50 GMT
WORKDIR /go
# Thu, 04 Nov 2021 20:51:38 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 20:51:38 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:22:21 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:22:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:22:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:22:24 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31adcdaf11c89113a810db23d523e549d634d7de695a72b0ce98a1f912101262`  
		Last Modified: Mon, 30 Aug 2021 22:01:00 GMT  
		Size: 281.5 KB (281508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b176561691ea11cfe541f3ee363a3aa67e3649eb3273bea62ebeea713eaecd`  
		Last Modified: Mon, 30 Aug 2021 22:00:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d416b4d4fcca0271f31d7d73ef5910b705bc9c7e6c47e2849f526c61323bba9`  
		Last Modified: Thu, 04 Nov 2021 20:33:02 GMT  
		Size: 110.1 MB (110106449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b6b52ae600093bcea2a88e347c180ddf79cf361a229c968ab134f79566115b`  
		Last Modified: Thu, 04 Nov 2021 20:32:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ce64c87030110c9e1fb28a88d6de9ab21bc642f56da365e029fef45bd40449`  
		Last Modified: Thu, 04 Nov 2021 20:52:00 GMT  
		Size: 6.6 MB (6626626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4745adbe391f6c84dabb01d0b9f46dcb4c3835b37d657188312f964bf2428113`  
		Last Modified: Tue, 09 Nov 2021 00:23:02 GMT  
		Size: 1.2 MB (1244972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29111d85c26db67c047d940076de17d7fa99ab44f4facbb7102429b421060b91`  
		Last Modified: Tue, 09 Nov 2021 00:23:02 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a321aa86f856c91169d31a96a1181ca0fb15d4fa785b01fd4f1db0a76ac5f438
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115556079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1759314115af8681edae8afa8c25d576e2bf7c430e2fcf6bdae1a6f520f4b6f5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Mon, 30 Aug 2021 21:49:40 GMT
RUN apk add --no-cache ca-certificates
# Mon, 30 Aug 2021 21:49:41 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 30 Aug 2021 21:49:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:50:01 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:53:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:53:24 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:53:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:53:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:53:27 GMT
WORKDIR /go
# Thu, 04 Nov 2021 21:26:48 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 21:26:48 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:50:03 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:50:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:50:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:50:07 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:50:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb221a547a2f49a13c3bbe14f37b0474b2066cece57c67c2fbc1fb07d89aad51`  
		Last Modified: Mon, 30 Aug 2021 22:04:54 GMT  
		Size: 281.7 KB (281671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2968f26f7f14fe309f1a7a85ad968b81a7daa93c078322a84eb5c4192326828`  
		Last Modified: Mon, 30 Aug 2021 22:04:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1662a83909f5aff655c7be6da1ffd97a579ec92c5839159187d230df4db0c304`  
		Last Modified: Thu, 04 Nov 2021 21:06:10 GMT  
		Size: 105.0 MB (104982787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247cd469be037fb4ffd6898dfee7159dc4dbb17525c62f11540b77badda787fe`  
		Last Modified: Thu, 04 Nov 2021 21:05:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52d5113b58e9eea7126b6573a103c6174f77e3f086440c6b60d013feeae55c9`  
		Last Modified: Thu, 04 Nov 2021 21:28:00 GMT  
		Size: 6.5 MB (6485880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053aa7bf00b68e2dd2854ce3cf420395833093ba5dbf21fcbe716d7c14129a82`  
		Last Modified: Tue, 09 Nov 2021 00:51:31 GMT  
		Size: 1.2 MB (1177578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba84a71092e7a8161d2aa6cb90f140a7a6a7ee304fd1143a4bedc91bdb8a3430`  
		Last Modified: Tue, 09 Nov 2021 00:51:30 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:898867984c20de5d0a90810f09c3aa0d59c45b55c878d65fa1986002494be562
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114460716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f422bda8d34cfaad33778dcbf74db88e84c362e26c97e5ecb7e52bc0aed977c2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Mon, 30 Aug 2021 23:51:38 GMT
RUN apk add --no-cache ca-certificates
# Mon, 30 Aug 2021 23:51:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 30 Aug 2021 23:51:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:00:39 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 21:03:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 21:03:56 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 21:03:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:03:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 21:03:59 GMT
WORKDIR /go
# Thu, 04 Nov 2021 22:24:32 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 22:24:32 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:58:01 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:58:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:58:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:58:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:58:05 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9417f62ae10851eaf03f096c21f2848fdfe2517baf1faffe0a25f4a1f9853e31`  
		Last Modified: Tue, 31 Aug 2021 00:14:21 GMT  
		Size: 280.8 KB (280829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15fcbf7d3458d8a294b9a3c72856e5e7ba1372b93f8fc485abecc73f5a8c9b6`  
		Last Modified: Tue, 31 Aug 2021 00:14:21 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83145a0dc91bcfd39d1372eacfa0b0edd49fbd853a8805d09bc3c801ec17707`  
		Last Modified: Thu, 04 Nov 2021 21:24:35 GMT  
		Size: 104.8 MB (104787212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56a13d9f75fefe8df6818c553071626370c07285a8579c71d061dd3958ab9e9`  
		Last Modified: Thu, 04 Nov 2021 21:09:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a883856d1a9eb72feb215725e23c34ff4e13cc0bdba2c76df4ff5a281950a34d`  
		Last Modified: Thu, 04 Nov 2021 22:25:46 GMT  
		Size: 5.8 MB (5785275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce6cdc3c3bebb2bf176add262391b9b35a554c02e1031b6809d950661a432fe`  
		Last Modified: Tue, 09 Nov 2021 00:59:28 GMT  
		Size: 1.2 MB (1176263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699c5f30dbc0681a9241c9e446110c0ff7a3228da9ef73377eddfec9167018af`  
		Last Modified: Tue, 09 Nov 2021 00:59:27 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:465390cedcb9fff08eb002c4722d69e56f05c3c60f953da3cfb449ae162140c6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115238050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eddb3be5e644425a129daa8ef25fa1990904790212c12c1037f9acff4e54e6d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Tue, 12 Oct 2021 19:50:31 GMT
RUN apk add --no-cache ca-certificates
# Tue, 12 Oct 2021 19:50:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 12 Oct 2021 19:50:33 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:44:49 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:46:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:46:13 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:46:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:46:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:46:16 GMT
WORKDIR /go
# Thu, 04 Nov 2021 21:13:57 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 21:13:58 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:39:47 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:39:47 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:39:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:39:51 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:39:51 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb74239f2a0c13b654df471372048f7785978cbe6bf5ddc6773d88218ad689f0`  
		Last Modified: Tue, 12 Oct 2021 19:56:27 GMT  
		Size: 281.5 KB (281470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8ec004bf6b17206854367316e34aa51b7f5ff2f447e6c66498b2922dfad207`  
		Last Modified: Tue, 12 Oct 2021 19:56:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2dd7c0ce8a9709408ba750c27f660c1821df16fc1588b83103c14f5c982410`  
		Last Modified: Thu, 04 Nov 2021 20:55:18 GMT  
		Size: 104.4 MB (104362226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51b802c83dca96aee9527f6b9430dfb8d84cc63a0dfb77abd3fc70b35661b68`  
		Last Modified: Thu, 04 Nov 2021 20:55:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b82d2b3afe06ceb5e9038414bd86eaa29b64d9ca539a8d7f0a9a97d89c0ec4`  
		Last Modified: Thu, 04 Nov 2021 21:14:36 GMT  
		Size: 6.7 MB (6733703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6348d8e1d75893311f870eec10215eaead24e452e1ad2a6ae81e2b276e3cca2`  
		Last Modified: Tue, 09 Nov 2021 00:40:33 GMT  
		Size: 1.1 MB (1148135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a51eb07dd20f1949799c418f754133ca1fc5b646673e8ac9d111563dbc589f0`  
		Last Modified: Tue, 09 Nov 2021 00:40:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:2336a18de17f2c4072c9c0307696854edf929dcb82a60b90f55259a69eeb600a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (114036993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b00aa91420fc4f22cea6aab5ff77b36da6f5a53aa4614f04c4434e09de4e6f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Tue, 31 Aug 2021 00:28:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 31 Aug 2021 00:29:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 31 Aug 2021 00:29:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:35:29 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 21:37:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 21:38:07 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 21:38:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:38:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 21:38:27 GMT
WORKDIR /go
# Thu, 04 Nov 2021 23:44:35 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 23:44:36 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 02:42:23 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 02:42:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 02:42:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 02:42:49 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 02:42:55 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4539d90ff594fe73c1a1e31b2230e539a965f33143a3c9fbd89507336ed283c2`  
		Last Modified: Tue, 31 Aug 2021 00:52:27 GMT  
		Size: 283.6 KB (283640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a17d0ec6ff5411e524016f0ac7033cf7a0a8935f7a5e299d4d7acaad208b26`  
		Last Modified: Tue, 31 Aug 2021 00:52:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34c4f0757f32d139833674c31fd061ecab0806960999b78a42e97fccf03c17b`  
		Last Modified: Thu, 04 Nov 2021 21:55:32 GMT  
		Size: 102.7 MB (102722966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f044c2212367ff5cf5f5f5c673ad6d3feae574970990f8f78507c3ac07e3640`  
		Last Modified: Thu, 04 Nov 2021 21:54:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428a3c7c0c1bff96a1ad7f93a7663935ca506020c92db68c2c71b978a2e6ed00`  
		Last Modified: Thu, 04 Nov 2021 23:45:27 GMT  
		Size: 7.1 MB (7097367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c99d2cd9325e8349becf942ed19b5842c0c2199ce5cbca707223e3419ebb52`  
		Last Modified: Tue, 09 Nov 2021 02:43:49 GMT  
		Size: 1.1 MB (1120017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2118cc3ec9b4efe4249b876ec149d807c563e41337b16031f2189b0934bb4744`  
		Last Modified: Tue, 09 Nov 2021 02:43:52 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:504417781112a6da613e5dbf96701f333e86c02c15ee528bcfc69a914cb5b99c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118475563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6cfef420950dbccc42ede323157843e6c2451cefbb4b472fc259ac9e90a0708`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Mon, 30 Aug 2021 21:44:33 GMT
RUN apk add --no-cache ca-certificates
# Mon, 30 Aug 2021 21:44:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 30 Aug 2021 21:44:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:42:32 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:44:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:44:06 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:44:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:44:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:44:07 GMT
WORKDIR /go
# Thu, 04 Nov 2021 21:16:26 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 21:16:27 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:41:36 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:41:36 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:41:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:41:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:41:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316d1588ef06afb0d7a96646bb3a1367bce295885797fd976945ed318a4eb9c`  
		Last Modified: Mon, 30 Aug 2021 21:59:27 GMT  
		Size: 281.9 KB (281927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e156a554eded13f9baa4042fb4d12b879560bebfd8aca837bf0b52669f7932`  
		Last Modified: Mon, 30 Aug 2021 21:59:26 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe04792d0475ac041009f3ca62bcc0dc03a26292d21b32216bc2f3e666c2d5b`  
		Last Modified: Thu, 04 Nov 2021 20:52:06 GMT  
		Size: 107.7 MB (107663718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6416455ccb8f772096f018fb9032102e6439950a45d68d4188fdfde5d9a87ded`  
		Last Modified: Thu, 04 Nov 2021 20:51:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6952a3ac2d6398e7268d236bf7d0cee103719b380aebea5fb6aabd2e45c04ed1`  
		Last Modified: Thu, 04 Nov 2021 21:17:06 GMT  
		Size: 6.7 MB (6722226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39fdad6edb5004df0acf851fcf3b0cf9d8cdfeaa9913d04f595517236869eef`  
		Last Modified: Tue, 09 Nov 2021 00:42:30 GMT  
		Size: 1.2 MB (1203510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0be2e59b91c38d78efc2f40a152bdd89dd964e653984267002b1453226e9d2e`  
		Last Modified: Tue, 09 Nov 2021 00:42:30 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.2300; amd64

```console
$ docker pull caddy@sha256:4d2914c283fcdb42d19719132d7efbfbfe7ad8af1d9cd5c071bf854233987587
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2878964819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b401c7e3582848bc6ccadc1c70895573764efb0f83732c2863411e9419c08c35`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 13:26:17 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Nov 2021 13:26:18 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Nov 2021 13:26:19 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Nov 2021 13:26:20 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Nov 2021 13:27:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:27:38 GMT
ENV GOPATH=C:\go
# Wed, 10 Nov 2021 13:28:31 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Nov 2021 13:28:32 GMT
ENV GOLANG_VERSION=1.17.3
# Wed, 10 Nov 2021 13:31:30 GMT
RUN $url = 'https://dl.google.com/go/go1.17.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e78684b955742e215926204afc6ed62b9d165b509e25a687d62902516f08726b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:31:35 GMT
WORKDIR C:\go
# Wed, 10 Nov 2021 20:17:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:17:50 GMT
ENV XCADDY_VERSION=v0.2.0
# Wed, 10 Nov 2021 20:17:51 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:17:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Nov 2021 20:18:44 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Nov 2021 20:18:45 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f32622fe466bd678a47b75fa13ebb7781336e6a776a22f424036aa8e91fe1d`  
		Last Modified: Wed, 10 Nov 2021 14:05:07 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d684ea4a6b52df2d3b5c7f7876e3b784ff1def8eb60f9637d920f4e0e7870b`  
		Last Modified: Wed, 10 Nov 2021 14:05:03 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ff61f0f89258dd1f49b766ef30baddd8f3e3821737778748ba95b52c1a480c`  
		Last Modified: Wed, 10 Nov 2021 14:05:03 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16dc9a497b44a664b28524686ca0e75c6a244af505429f54f80a6aaa96c7af9`  
		Last Modified: Wed, 10 Nov 2021 14:05:04 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e724f5e2b6e2fb2598ad100e7efa9cf30fe013f56537a5587d8e8868ae82d50`  
		Last Modified: Wed, 10 Nov 2021 14:05:09 GMT  
		Size: 25.4 MB (25446198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84e37bf01f689e54241d5e76695c5cbcc3313f3f8a85748e9d086c6cf3e4c3d`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f6ed9286b06435dae34f3d3e03f2c62a4415e3703740a83381b4ac0a3d1804`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 325.4 KB (325448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd53ef82415224427ba6005a3993a50da833e74dd65f413ede222760ab73155`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322051166b18395731c110a7ced59dc83924ac45736b482be8611e491ce9be22`  
		Last Modified: Wed, 10 Nov 2021 14:05:34 GMT  
		Size: 145.4 MB (145394728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7588b640c5b448c06e31f55936d39ebd92c0050d9b2daf5a86f09841d0ac6e68`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab8b7df216099a8c01f65cacfd0d07bfb8fe6ef211d5dbc6b897ceab643aa54`  
		Last Modified: Wed, 10 Nov 2021 20:21:41 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e1af14b4ab45cfdf867d71debb12ba16dc9770a11af54ec694004f8828280f`  
		Last Modified: Wed, 10 Nov 2021 20:21:38 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18305c1b79b992f30e786ccaa7379fba16154663b28f19d088c9b1750fe53f12`  
		Last Modified: Wed, 10 Nov 2021 20:21:38 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c926d89c22fc6adf4e181145a724ed23dacf28e12d58b7e7f75d69c4239ea2f0`  
		Last Modified: Wed, 10 Nov 2021 20:21:38 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb704654cf062fe78ae7674ea38cb7e81ac8f2b26f74c295489abf19dd4d206`  
		Last Modified: Wed, 10 Nov 2021 20:21:39 GMT  
		Size: 1.7 MB (1658702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da89e3439fa9c9e9d4cde6c4aca2fb1796d9dfceec37d31d351e2005a188b389`  
		Last Modified: Wed, 10 Nov 2021 20:21:38 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.14393.4770; amd64

```console
$ docker pull caddy@sha256:96a88b09cecf23cff2a8006ea25f1e037f50d01a9c74d2d3769f8bb228d2b768
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6450468916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fcd7b2f02771fd0b23831a7e603a01713fad078e5e205d745958ee47f638e5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 13:31:46 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Nov 2021 13:31:47 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Nov 2021 13:31:48 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Nov 2021 13:31:49 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Nov 2021 13:33:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:33:37 GMT
ENV GOPATH=C:\go
# Wed, 10 Nov 2021 13:34:34 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Nov 2021 13:34:35 GMT
ENV GOLANG_VERSION=1.17.3
# Wed, 10 Nov 2021 13:37:32 GMT
RUN $url = 'https://dl.google.com/go/go1.17.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e78684b955742e215926204afc6ed62b9d165b509e25a687d62902516f08726b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:37:37 GMT
WORKDIR C:\go
# Wed, 10 Nov 2021 20:18:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:18:53 GMT
ENV XCADDY_VERSION=v0.2.0
# Wed, 10 Nov 2021 20:18:54 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:18:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Nov 2021 20:19:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Nov 2021 20:19:56 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a0c69f83a30944f5afdc948b3583f1418f71f3ae5a02382610f0898eb501f9`  
		Last Modified: Wed, 10 Nov 2021 14:05:54 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e4bea9e4e2ccac41591b4aed9981453c554ca498a23d01a69638d6ccab7016`  
		Last Modified: Wed, 10 Nov 2021 14:05:52 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b36358e1913c99dc66fbbca2e4c0f8472796bf33ceeb7fdc02d2b7096b1208d`  
		Last Modified: Wed, 10 Nov 2021 14:05:52 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d071f5d45753629193f76196d769df9ff71ce3a39e5b10a16ff571cdb071a902`  
		Last Modified: Wed, 10 Nov 2021 14:05:52 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79602be6489be8a0e5e82221cae33eae5692897081a79bfe959604121e2d0a4`  
		Last Modified: Wed, 10 Nov 2021 14:06:20 GMT  
		Size: 25.4 MB (25448073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30d749fb8ba78fba5cce783b8cbe233632a2ba5965d4b67168111396620aaa0`  
		Last Modified: Wed, 10 Nov 2021 14:05:50 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f08b5963e19f3d28aa336d06434d4efec179b4b813e4aa4222ab064bc180f7`  
		Last Modified: Wed, 10 Nov 2021 14:05:50 GMT  
		Size: 354.9 KB (354902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f381a7ed29624957c6a0c2539069229be83423497216e9b19872996d3eace018`  
		Last Modified: Wed, 10 Nov 2021 14:05:49 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9184646a18b279b69062ae625cf768031d03c297beca44a465b8265af80e7116`  
		Last Modified: Wed, 10 Nov 2021 14:06:25 GMT  
		Size: 149.9 MB (149917271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e2acfda5cf05f260961ec16cee7c5c9e5573783c8298319e6b38846cb3b98b`  
		Last Modified: Wed, 10 Nov 2021 14:05:49 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f8275e6d67e00182a573a1fea89b6fbafd29fdd9e6991bec289907772e366`  
		Last Modified: Wed, 10 Nov 2021 20:21:59 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f675d50b479c34b5e127a7560cec6198d6c06464747188b22904543e0919ffe`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dba2d80865d737653a9a4ff2db1fcac88ce9bf3521d9e7f6dc8116fd16a99b`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272648eb620ef88b428e4aac8f782d100c4e64bb6f14073ee16b5b89a3b12967`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b51ab7213b8db3f0e51ace7c64b811e81a3d838148d7c41c3a58a9ffd1eb66`  
		Last Modified: Wed, 10 Nov 2021 20:21:58 GMT  
		Size: 1.6 MB (1639511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd676bfb740256d3eae7ac606f73a7d0ad09121f54eacd3ffdeff570e4b73bd1`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:79350de5d5c17d2eea90b4a8d8b8fdf5e200d7b3173a1bcb4b52ac4c7c7b901c
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
$ docker pull caddy@sha256:58018b2f6a30dbb45e39be3761a09af004a551296f8f92bf31bef97687b15742
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121074719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8dc98d3747bd25bdd8b095b563b0cfa728096f1be09b7e50f5d2f81dc350be4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Mon, 30 Aug 2021 21:44:05 GMT
RUN apk add --no-cache ca-certificates
# Mon, 30 Aug 2021 21:44:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 30 Aug 2021 21:44:06 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:20:44 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:22:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:22:49 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:22:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:22:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:22:50 GMT
WORKDIR /go
# Thu, 04 Nov 2021 20:51:38 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 20:51:38 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:22:21 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:22:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:22:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:22:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:22:24 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31adcdaf11c89113a810db23d523e549d634d7de695a72b0ce98a1f912101262`  
		Last Modified: Mon, 30 Aug 2021 22:01:00 GMT  
		Size: 281.5 KB (281508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b176561691ea11cfe541f3ee363a3aa67e3649eb3273bea62ebeea713eaecd`  
		Last Modified: Mon, 30 Aug 2021 22:00:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d416b4d4fcca0271f31d7d73ef5910b705bc9c7e6c47e2849f526c61323bba9`  
		Last Modified: Thu, 04 Nov 2021 20:33:02 GMT  
		Size: 110.1 MB (110106449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b6b52ae600093bcea2a88e347c180ddf79cf361a229c968ab134f79566115b`  
		Last Modified: Thu, 04 Nov 2021 20:32:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ce64c87030110c9e1fb28a88d6de9ab21bc642f56da365e029fef45bd40449`  
		Last Modified: Thu, 04 Nov 2021 20:52:00 GMT  
		Size: 6.6 MB (6626626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4745adbe391f6c84dabb01d0b9f46dcb4c3835b37d657188312f964bf2428113`  
		Last Modified: Tue, 09 Nov 2021 00:23:02 GMT  
		Size: 1.2 MB (1244972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29111d85c26db67c047d940076de17d7fa99ab44f4facbb7102429b421060b91`  
		Last Modified: Tue, 09 Nov 2021 00:23:02 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:a321aa86f856c91169d31a96a1181ca0fb15d4fa785b01fd4f1db0a76ac5f438
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115556079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1759314115af8681edae8afa8c25d576e2bf7c430e2fcf6bdae1a6f520f4b6f5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Mon, 30 Aug 2021 21:49:40 GMT
RUN apk add --no-cache ca-certificates
# Mon, 30 Aug 2021 21:49:41 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 30 Aug 2021 21:49:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:50:01 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:53:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:53:24 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:53:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:53:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:53:27 GMT
WORKDIR /go
# Thu, 04 Nov 2021 21:26:48 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 21:26:48 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:50:03 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:50:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:50:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:50:07 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:50:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb221a547a2f49a13c3bbe14f37b0474b2066cece57c67c2fbc1fb07d89aad51`  
		Last Modified: Mon, 30 Aug 2021 22:04:54 GMT  
		Size: 281.7 KB (281671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2968f26f7f14fe309f1a7a85ad968b81a7daa93c078322a84eb5c4192326828`  
		Last Modified: Mon, 30 Aug 2021 22:04:54 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1662a83909f5aff655c7be6da1ffd97a579ec92c5839159187d230df4db0c304`  
		Last Modified: Thu, 04 Nov 2021 21:06:10 GMT  
		Size: 105.0 MB (104982787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247cd469be037fb4ffd6898dfee7159dc4dbb17525c62f11540b77badda787fe`  
		Last Modified: Thu, 04 Nov 2021 21:05:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52d5113b58e9eea7126b6573a103c6174f77e3f086440c6b60d013feeae55c9`  
		Last Modified: Thu, 04 Nov 2021 21:28:00 GMT  
		Size: 6.5 MB (6485880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053aa7bf00b68e2dd2854ce3cf420395833093ba5dbf21fcbe716d7c14129a82`  
		Last Modified: Tue, 09 Nov 2021 00:51:31 GMT  
		Size: 1.2 MB (1177578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba84a71092e7a8161d2aa6cb90f140a7a6a7ee304fd1143a4bedc91bdb8a3430`  
		Last Modified: Tue, 09 Nov 2021 00:51:30 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:898867984c20de5d0a90810f09c3aa0d59c45b55c878d65fa1986002494be562
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114460716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f422bda8d34cfaad33778dcbf74db88e84c362e26c97e5ecb7e52bc0aed977c2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Mon, 30 Aug 2021 23:51:38 GMT
RUN apk add --no-cache ca-certificates
# Mon, 30 Aug 2021 23:51:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 30 Aug 2021 23:51:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:00:39 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 21:03:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 21:03:56 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 21:03:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:03:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 21:03:59 GMT
WORKDIR /go
# Thu, 04 Nov 2021 22:24:32 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 22:24:32 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:58:01 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:58:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:58:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:58:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:58:05 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9417f62ae10851eaf03f096c21f2848fdfe2517baf1faffe0a25f4a1f9853e31`  
		Last Modified: Tue, 31 Aug 2021 00:14:21 GMT  
		Size: 280.8 KB (280829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15fcbf7d3458d8a294b9a3c72856e5e7ba1372b93f8fc485abecc73f5a8c9b6`  
		Last Modified: Tue, 31 Aug 2021 00:14:21 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83145a0dc91bcfd39d1372eacfa0b0edd49fbd853a8805d09bc3c801ec17707`  
		Last Modified: Thu, 04 Nov 2021 21:24:35 GMT  
		Size: 104.8 MB (104787212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56a13d9f75fefe8df6818c553071626370c07285a8579c71d061dd3958ab9e9`  
		Last Modified: Thu, 04 Nov 2021 21:09:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a883856d1a9eb72feb215725e23c34ff4e13cc0bdba2c76df4ff5a281950a34d`  
		Last Modified: Thu, 04 Nov 2021 22:25:46 GMT  
		Size: 5.8 MB (5785275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce6cdc3c3bebb2bf176add262391b9b35a554c02e1031b6809d950661a432fe`  
		Last Modified: Tue, 09 Nov 2021 00:59:28 GMT  
		Size: 1.2 MB (1176263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699c5f30dbc0681a9241c9e446110c0ff7a3228da9ef73377eddfec9167018af`  
		Last Modified: Tue, 09 Nov 2021 00:59:27 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:465390cedcb9fff08eb002c4722d69e56f05c3c60f953da3cfb449ae162140c6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115238050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eddb3be5e644425a129daa8ef25fa1990904790212c12c1037f9acff4e54e6d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Tue, 12 Oct 2021 19:50:31 GMT
RUN apk add --no-cache ca-certificates
# Tue, 12 Oct 2021 19:50:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 12 Oct 2021 19:50:33 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:44:49 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:46:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:46:13 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:46:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:46:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:46:16 GMT
WORKDIR /go
# Thu, 04 Nov 2021 21:13:57 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 21:13:58 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:39:47 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:39:47 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:39:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:39:51 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:39:51 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb74239f2a0c13b654df471372048f7785978cbe6bf5ddc6773d88218ad689f0`  
		Last Modified: Tue, 12 Oct 2021 19:56:27 GMT  
		Size: 281.5 KB (281470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8ec004bf6b17206854367316e34aa51b7f5ff2f447e6c66498b2922dfad207`  
		Last Modified: Tue, 12 Oct 2021 19:56:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2dd7c0ce8a9709408ba750c27f660c1821df16fc1588b83103c14f5c982410`  
		Last Modified: Thu, 04 Nov 2021 20:55:18 GMT  
		Size: 104.4 MB (104362226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51b802c83dca96aee9527f6b9430dfb8d84cc63a0dfb77abd3fc70b35661b68`  
		Last Modified: Thu, 04 Nov 2021 20:55:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b82d2b3afe06ceb5e9038414bd86eaa29b64d9ca539a8d7f0a9a97d89c0ec4`  
		Last Modified: Thu, 04 Nov 2021 21:14:36 GMT  
		Size: 6.7 MB (6733703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6348d8e1d75893311f870eec10215eaead24e452e1ad2a6ae81e2b276e3cca2`  
		Last Modified: Tue, 09 Nov 2021 00:40:33 GMT  
		Size: 1.1 MB (1148135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a51eb07dd20f1949799c418f754133ca1fc5b646673e8ac9d111563dbc589f0`  
		Last Modified: Tue, 09 Nov 2021 00:40:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:2336a18de17f2c4072c9c0307696854edf929dcb82a60b90f55259a69eeb600a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (114036993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b00aa91420fc4f22cea6aab5ff77b36da6f5a53aa4614f04c4434e09de4e6f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Tue, 31 Aug 2021 00:28:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 31 Aug 2021 00:29:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 31 Aug 2021 00:29:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:35:29 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 21:37:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 21:38:07 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 21:38:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 21:38:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 21:38:27 GMT
WORKDIR /go
# Thu, 04 Nov 2021 23:44:35 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 23:44:36 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 02:42:23 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 02:42:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 02:42:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 02:42:49 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 02:42:55 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4539d90ff594fe73c1a1e31b2230e539a965f33143a3c9fbd89507336ed283c2`  
		Last Modified: Tue, 31 Aug 2021 00:52:27 GMT  
		Size: 283.6 KB (283640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a17d0ec6ff5411e524016f0ac7033cf7a0a8935f7a5e299d4d7acaad208b26`  
		Last Modified: Tue, 31 Aug 2021 00:52:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34c4f0757f32d139833674c31fd061ecab0806960999b78a42e97fccf03c17b`  
		Last Modified: Thu, 04 Nov 2021 21:55:32 GMT  
		Size: 102.7 MB (102722966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f044c2212367ff5cf5f5f5c673ad6d3feae574970990f8f78507c3ac07e3640`  
		Last Modified: Thu, 04 Nov 2021 21:54:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428a3c7c0c1bff96a1ad7f93a7663935ca506020c92db68c2c71b978a2e6ed00`  
		Last Modified: Thu, 04 Nov 2021 23:45:27 GMT  
		Size: 7.1 MB (7097367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c99d2cd9325e8349becf942ed19b5842c0c2199ce5cbca707223e3419ebb52`  
		Last Modified: Tue, 09 Nov 2021 02:43:49 GMT  
		Size: 1.1 MB (1120017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2118cc3ec9b4efe4249b876ec149d807c563e41337b16031f2189b0934bb4744`  
		Last Modified: Tue, 09 Nov 2021 02:43:52 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:504417781112a6da613e5dbf96701f333e86c02c15ee528bcfc69a914cb5b99c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118475563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6cfef420950dbccc42ede323157843e6c2451cefbb4b472fc259ac9e90a0708`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Mon, 30 Aug 2021 21:44:33 GMT
RUN apk add --no-cache ca-certificates
# Mon, 30 Aug 2021 21:44:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 30 Aug 2021 21:44:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:42:32 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:44:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 04 Nov 2021 20:44:06 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:44:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:44:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:44:07 GMT
WORKDIR /go
# Thu, 04 Nov 2021 21:16:26 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 04 Nov 2021 21:16:27 GMT
ENV XCADDY_VERSION=v0.2.0
# Tue, 09 Nov 2021 00:41:36 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:41:36 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Nov 2021 00:41:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b02fef09e1ea4ec26d87f1d24a442aaf247ca79b391064d7708e080e4bc5e14204381a3c573122b8b5f10de4495cf4e54fd7b90122ed45127673284d9619a0b8' ;; 		armhf)   binArch='armv6'; checksum='735f5327e47d7a4fbc224b305231f211475b26f7a0def11eccabc15c98fc1864f36370de235869a093a3c97a7ebe1ca255a4e64ab4eaf77dae89bd8a28a708a0' ;; 		armv7)   binArch='armv7'; checksum='d013d38f62ca548dcdea532224cd8571975d2b8c9bfcf98fc392907fd97d0ecfd0516d457b32988ef7215c626d51df2c2b6ca17f7c3cc14db656b84d4b1b8304' ;; 		aarch64) binArch='arm64'; checksum='d64fbed9556bf3997951d5337b91eb85b2a3abf3bf6d3e28a838f1977c276e39087e435b6def9a860cdd6d1f0095602374ddedb3e6c382b8a29c7d446623f651' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b304e6129e4928155c1c9eda33b76b43024ba34bd0197445a8dff12b45472f92d96d90b9083525b480d796d94bfe861cc415b4dbaad56cfcc5e6f1c366cc476c' ;; 		s390x)   binArch='s390x'; checksum='ad3b5e27804d77f76429c98babf8df6f3418b613ec94370afc57dab5ed7f9b6492118f6706b01d73f1ff352c3f5618f41cb87dfbc3b089b2230d064bd8153a41' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Nov 2021 00:41:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Nov 2021 00:41:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316d1588ef06afb0d7a96646bb3a1367bce295885797fd976945ed318a4eb9c`  
		Last Modified: Mon, 30 Aug 2021 21:59:27 GMT  
		Size: 281.9 KB (281927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e156a554eded13f9baa4042fb4d12b879560bebfd8aca837bf0b52669f7932`  
		Last Modified: Mon, 30 Aug 2021 21:59:26 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe04792d0475ac041009f3ca62bcc0dc03a26292d21b32216bc2f3e666c2d5b`  
		Last Modified: Thu, 04 Nov 2021 20:52:06 GMT  
		Size: 107.7 MB (107663718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6416455ccb8f772096f018fb9032102e6439950a45d68d4188fdfde5d9a87ded`  
		Last Modified: Thu, 04 Nov 2021 20:51:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6952a3ac2d6398e7268d236bf7d0cee103719b380aebea5fb6aabd2e45c04ed1`  
		Last Modified: Thu, 04 Nov 2021 21:17:06 GMT  
		Size: 6.7 MB (6722226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39fdad6edb5004df0acf851fcf3b0cf9d8cdfeaa9913d04f595517236869eef`  
		Last Modified: Tue, 09 Nov 2021 00:42:30 GMT  
		Size: 1.2 MB (1203510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0be2e59b91c38d78efc2f40a152bdd89dd964e653984267002b1453226e9d2e`  
		Last Modified: Tue, 09 Nov 2021 00:42:30 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:8bdbf970abe748608ce652f507707eccf33bc6cd57a25e6bdfaec47ae0353860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull caddy@sha256:4d2914c283fcdb42d19719132d7efbfbfe7ad8af1d9cd5c071bf854233987587
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2878964819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b401c7e3582848bc6ccadc1c70895573764efb0f83732c2863411e9419c08c35`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 13:26:17 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Nov 2021 13:26:18 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Nov 2021 13:26:19 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Nov 2021 13:26:20 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Nov 2021 13:27:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:27:38 GMT
ENV GOPATH=C:\go
# Wed, 10 Nov 2021 13:28:31 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Nov 2021 13:28:32 GMT
ENV GOLANG_VERSION=1.17.3
# Wed, 10 Nov 2021 13:31:30 GMT
RUN $url = 'https://dl.google.com/go/go1.17.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e78684b955742e215926204afc6ed62b9d165b509e25a687d62902516f08726b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:31:35 GMT
WORKDIR C:\go
# Wed, 10 Nov 2021 20:17:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:17:50 GMT
ENV XCADDY_VERSION=v0.2.0
# Wed, 10 Nov 2021 20:17:51 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:17:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Nov 2021 20:18:44 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Nov 2021 20:18:45 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f32622fe466bd678a47b75fa13ebb7781336e6a776a22f424036aa8e91fe1d`  
		Last Modified: Wed, 10 Nov 2021 14:05:07 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d684ea4a6b52df2d3b5c7f7876e3b784ff1def8eb60f9637d920f4e0e7870b`  
		Last Modified: Wed, 10 Nov 2021 14:05:03 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ff61f0f89258dd1f49b766ef30baddd8f3e3821737778748ba95b52c1a480c`  
		Last Modified: Wed, 10 Nov 2021 14:05:03 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16dc9a497b44a664b28524686ca0e75c6a244af505429f54f80a6aaa96c7af9`  
		Last Modified: Wed, 10 Nov 2021 14:05:04 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e724f5e2b6e2fb2598ad100e7efa9cf30fe013f56537a5587d8e8868ae82d50`  
		Last Modified: Wed, 10 Nov 2021 14:05:09 GMT  
		Size: 25.4 MB (25446198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84e37bf01f689e54241d5e76695c5cbcc3313f3f8a85748e9d086c6cf3e4c3d`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f6ed9286b06435dae34f3d3e03f2c62a4415e3703740a83381b4ac0a3d1804`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 325.4 KB (325448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd53ef82415224427ba6005a3993a50da833e74dd65f413ede222760ab73155`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322051166b18395731c110a7ced59dc83924ac45736b482be8611e491ce9be22`  
		Last Modified: Wed, 10 Nov 2021 14:05:34 GMT  
		Size: 145.4 MB (145394728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7588b640c5b448c06e31f55936d39ebd92c0050d9b2daf5a86f09841d0ac6e68`  
		Last Modified: Wed, 10 Nov 2021 14:05:00 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab8b7df216099a8c01f65cacfd0d07bfb8fe6ef211d5dbc6b897ceab643aa54`  
		Last Modified: Wed, 10 Nov 2021 20:21:41 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e1af14b4ab45cfdf867d71debb12ba16dc9770a11af54ec694004f8828280f`  
		Last Modified: Wed, 10 Nov 2021 20:21:38 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18305c1b79b992f30e786ccaa7379fba16154663b28f19d088c9b1750fe53f12`  
		Last Modified: Wed, 10 Nov 2021 20:21:38 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c926d89c22fc6adf4e181145a724ed23dacf28e12d58b7e7f75d69c4239ea2f0`  
		Last Modified: Wed, 10 Nov 2021 20:21:38 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb704654cf062fe78ae7674ea38cb7e81ac8f2b26f74c295489abf19dd4d206`  
		Last Modified: Wed, 10 Nov 2021 20:21:39 GMT  
		Size: 1.7 MB (1658702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da89e3439fa9c9e9d4cde6c4aca2fb1796d9dfceec37d31d351e2005a188b389`  
		Last Modified: Wed, 10 Nov 2021 20:21:38 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:616283cce0c82245c2685b723e1f9538d1c4e926a9ad143dd66bf0e299b64ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `caddy:builder-windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull caddy@sha256:96a88b09cecf23cff2a8006ea25f1e037f50d01a9c74d2d3769f8bb228d2b768
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6450468916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fcd7b2f02771fd0b23831a7e603a01713fad078e5e205d745958ee47f638e5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 13:31:46 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Nov 2021 13:31:47 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Nov 2021 13:31:48 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Nov 2021 13:31:49 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Nov 2021 13:33:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:33:37 GMT
ENV GOPATH=C:\go
# Wed, 10 Nov 2021 13:34:34 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Nov 2021 13:34:35 GMT
ENV GOLANG_VERSION=1.17.3
# Wed, 10 Nov 2021 13:37:32 GMT
RUN $url = 'https://dl.google.com/go/go1.17.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e78684b955742e215926204afc6ed62b9d165b509e25a687d62902516f08726b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Nov 2021 13:37:37 GMT
WORKDIR C:\go
# Wed, 10 Nov 2021 20:18:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:18:53 GMT
ENV XCADDY_VERSION=v0.2.0
# Wed, 10 Nov 2021 20:18:54 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:18:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Nov 2021 20:19:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Nov 2021 20:19:56 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a0c69f83a30944f5afdc948b3583f1418f71f3ae5a02382610f0898eb501f9`  
		Last Modified: Wed, 10 Nov 2021 14:05:54 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e4bea9e4e2ccac41591b4aed9981453c554ca498a23d01a69638d6ccab7016`  
		Last Modified: Wed, 10 Nov 2021 14:05:52 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b36358e1913c99dc66fbbca2e4c0f8472796bf33ceeb7fdc02d2b7096b1208d`  
		Last Modified: Wed, 10 Nov 2021 14:05:52 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d071f5d45753629193f76196d769df9ff71ce3a39e5b10a16ff571cdb071a902`  
		Last Modified: Wed, 10 Nov 2021 14:05:52 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79602be6489be8a0e5e82221cae33eae5692897081a79bfe959604121e2d0a4`  
		Last Modified: Wed, 10 Nov 2021 14:06:20 GMT  
		Size: 25.4 MB (25448073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30d749fb8ba78fba5cce783b8cbe233632a2ba5965d4b67168111396620aaa0`  
		Last Modified: Wed, 10 Nov 2021 14:05:50 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f08b5963e19f3d28aa336d06434d4efec179b4b813e4aa4222ab064bc180f7`  
		Last Modified: Wed, 10 Nov 2021 14:05:50 GMT  
		Size: 354.9 KB (354902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f381a7ed29624957c6a0c2539069229be83423497216e9b19872996d3eace018`  
		Last Modified: Wed, 10 Nov 2021 14:05:49 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9184646a18b279b69062ae625cf768031d03c297beca44a465b8265af80e7116`  
		Last Modified: Wed, 10 Nov 2021 14:06:25 GMT  
		Size: 149.9 MB (149917271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e2acfda5cf05f260961ec16cee7c5c9e5573783c8298319e6b38846cb3b98b`  
		Last Modified: Wed, 10 Nov 2021 14:05:49 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739f8275e6d67e00182a573a1fea89b6fbafd29fdd9e6991bec289907772e366`  
		Last Modified: Wed, 10 Nov 2021 20:21:59 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f675d50b479c34b5e127a7560cec6198d6c06464747188b22904543e0919ffe`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dba2d80865d737653a9a4ff2db1fcac88ce9bf3521d9e7f6dc8116fd16a99b`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272648eb620ef88b428e4aac8f782d100c4e64bb6f14073ee16b5b89a3b12967`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b51ab7213b8db3f0e51ace7c64b811e81a3d838148d7c41c3a58a9ffd1eb66`  
		Last Modified: Wed, 10 Nov 2021 20:21:58 GMT  
		Size: 1.6 MB (1639511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd676bfb740256d3eae7ac606f73a7d0ad09121f54eacd3ffdeff570e4b73bd1`  
		Last Modified: Wed, 10 Nov 2021 20:21:57 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:b82736e58560e3c1591c6205ddd9f44a5a11edebb1341a2e8cfe05b2617daa47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:85a8daaf3706e847da86d456fb722edacb72a32360d333febccbf208f08e2be6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14847925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332a21201a47e70a89875163c9e41f0e78d6514d6e64aae618c3e2cc79b5e35d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:19:30 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:19:31 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:22:07 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:22:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:22:12 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:22:12 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:22:12 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:22:12 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:22:13 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:22:13 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:22:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:22:14 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:22:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:22:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:22:15 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:22:16 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:22:16 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:22:16 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:22:17 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d9d63a262eb117d9f55cf667904b985eb6dd9830783f17146a17a107a7ee19`  
		Last Modified: Tue, 07 Sep 2021 19:20:03 GMT  
		Size: 301.0 KB (301044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d54a459a500730b7153882903986d92e877f472e9d6ead142fab9dcb6464e1`  
		Last Modified: Tue, 07 Sep 2021 19:20:04 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12929046016b5f7547cb262dd7e97132958593eff9f30a3062729ed87f5f764f`  
		Last Modified: Tue, 09 Nov 2021 00:22:50 GMT  
		Size: 11.7 MB (11726452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2abe024ef8ac2567e428b8c753253b9670be99dad8f46607c895df6577f60ee`  
		Last Modified: Tue, 09 Nov 2021 00:22:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:84282af6d453c14c7875598e935faa6d1e7605067a6a212f69227bed1b97ae91
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14060404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4a22469cd1950a4d76a71bd95254b6b70d97f1d46d0ab846d9561937d7cee8`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:49:32 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:49:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:49:32 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:49:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:49:39 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:49:39 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:49:40 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:49:40 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:49:41 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:49:41 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:49:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:49:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:49:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:49:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:49:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:49:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:49:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:49:45 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:49:45 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:49:46 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:49:46 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:49:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f254033e1bbf10f9a1641b6005ee6ae290bdec377e00d2e5290e33dc0eb8f9b6`  
		Last Modified: Tue, 07 Sep 2021 19:51:17 GMT  
		Size: 301.2 KB (301188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28038de9754eec9aa2df09a34c0d7029c335199166de56398d21fb595fd289dd`  
		Last Modified: Tue, 07 Sep 2021 19:51:17 GMT  
		Size: 5.8 KB (5831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d17cc2aea86ad912ecd44f746238a440abd651aacc69ff04dcfdfa5e93193bb`  
		Last Modified: Tue, 09 Nov 2021 00:51:15 GMT  
		Size: 11.1 MB (11125785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cde1922177a05c9ac9c3cdb88d2492158258e3ddc64a6168bf7aa3d2087c3f5`  
		Last Modified: Tue, 09 Nov 2021 00:51:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:fb17cbc78aa551976f55685ba43b474671da9323631920b2411ef3ba47986f62
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13843483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9933538b9e4061a71c69dda3c1ac39f499b0a0c09fc86871a60a60b72576e0c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:57:36 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:57:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:57:30 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:57:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:57:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:57:37 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:57:37 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:57:38 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:57:38 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:57:39 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:57:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:57:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:57:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:57:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:57:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:57:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:57:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:57:42 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:57:43 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:57:43 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:57:44 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:57:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98c39987cd6455919d7455feed9aba93a44659ef658fbef5d4d52500beddac5`  
		Last Modified: Tue, 07 Sep 2021 19:59:13 GMT  
		Size: 300.4 KB (300356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e223cb6b0d911c9cc6575c496bc4f96f1968db869a8a07694f3f49897920f264`  
		Last Modified: Tue, 07 Sep 2021 19:59:13 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d8001745b5a3dedaa6b3a2bef5234f8612ac3d942269d2e18abbc1bfae84c8`  
		Last Modified: Tue, 09 Nov 2021 00:59:12 GMT  
		Size: 11.1 MB (11106727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bfb11f4ca256c6f83e7d7f05fdc548ce544492b765b72bad8fff802e114ec0`  
		Last Modified: Tue, 09 Nov 2021 00:59:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:dcc03368e7ff328ba4159eca9d88c2cb33e3ef4d8aaf9cec550f4f924c032616
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13757357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fca8f72561cf76363cdb806b321face6a1c9831e94d96c4966828a26b19962b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 14 Oct 2021 01:35:26 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 14 Oct 2021 01:35:28 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:39:19 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:39:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:39:22 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:39:23 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:39:24 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:39:25 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:39:26 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:39:27 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:39:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:39:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:39:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:39:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:39:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:39:33 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:39:34 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:39:35 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:39:36 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:39:37 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:39:38 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:39:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdae6629f9c73c56d66409172a1dcab55f533f8b62eb70c990c8e2cabcd7695`  
		Last Modified: Thu, 14 Oct 2021 01:36:31 GMT  
		Size: 301.0 KB (300992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3c515fae4831ae5dd272bcc27d7d3d3011d0f880b795b0aed1ce8c389c96bf`  
		Last Modified: Thu, 14 Oct 2021 01:36:30 GMT  
		Size: 5.8 KB (5752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce648197b75d827f9704483ccbcc884912ffb6a25728a39ddd0f717c3d534a46`  
		Last Modified: Tue, 09 Nov 2021 00:40:20 GMT  
		Size: 10.7 MB (10738633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d3751262c3b44d86e469c50ed19d1a632a37d420e471e3653d9c26c8d51ba6`  
		Last Modified: Tue, 09 Nov 2021 00:40:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:b1f36f28cb28be8e03baf5e564e8813cf57f65a907533db61acec3fc2ff7d337
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13423700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927f64bc8094cd853e2649145f44cf5cbc699568c2066c650c61db9865417dc5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:16:42 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:16:56 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 02:38:59 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 02:39:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 02:39:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 02:39:43 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 02:39:47 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 02:39:58 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 02:40:04 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 02:40:16 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 02:40:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 02:40:30 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 02:40:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 02:40:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 02:40:54 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 02:41:01 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 02:41:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 02:41:31 GMT
EXPOSE 80
# Tue, 09 Nov 2021 02:41:42 GMT
EXPOSE 443
# Tue, 09 Nov 2021 02:41:49 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 02:41:57 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 02:42:08 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d32e3566fcaa11540498ebdd9ecc55cd2e2dca73a6b62317657a9e75749272`  
		Last Modified: Tue, 07 Sep 2021 19:21:13 GMT  
		Size: 303.2 KB (303162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a831abca68890cbd7a89171bb93c9af5c1b102852f0f1f3326ff7c104ced90`  
		Last Modified: Tue, 07 Sep 2021 19:21:12 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef4a0928ede6ae0f23c1a955b08d450770842d163d8152b4ad7cb9333b4ac5b`  
		Last Modified: Tue, 09 Nov 2021 02:43:36 GMT  
		Size: 10.3 MB (10302268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6dff47d769c4013cb3ed7545b165cd303bac49d09576d80c78bfa8d9353b1bb`  
		Last Modified: Tue, 09 Nov 2021 02:43:34 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:7ceecb66639b47e4acb3acc566018228f83534b5a49f4a5306f4a6ae995cd13f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14234623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82585988e83eb76f3ebc0d2bb5323c9663491e28faa0819aa54296c142e686b3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Tue, 07 Sep 2021 19:41:29 GMT
RUN apk add --no-cache ca-certificates mailcap
# Tue, 07 Sep 2021 19:41:32 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Tue, 09 Nov 2021 00:41:22 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 09 Nov 2021 00:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Tue, 09 Nov 2021 00:41:25 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 09 Nov 2021 00:41:26 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 09 Nov 2021 00:41:26 GMT
ENV XDG_DATA_HOME=/data
# Tue, 09 Nov 2021 00:41:26 GMT
VOLUME [/config]
# Tue, 09 Nov 2021 00:41:26 GMT
VOLUME [/data]
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Nov 2021 00:41:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Nov 2021 00:41:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Nov 2021 00:41:27 GMT
EXPOSE 80
# Tue, 09 Nov 2021 00:41:27 GMT
EXPOSE 443
# Tue, 09 Nov 2021 00:41:27 GMT
EXPOSE 2019
# Tue, 09 Nov 2021 00:41:27 GMT
WORKDIR /srv
# Tue, 09 Nov 2021 00:41:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9c7d5d2c4319fc2386cc1a009e57751b8d7a7d807ae0e867e4d6273e06731d`  
		Last Modified: Tue, 07 Sep 2021 19:42:43 GMT  
		Size: 301.5 KB (301462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c7b669e195c7cce7cf6d957130645125c1171c464622ceaa01378d18f24e37`  
		Last Modified: Tue, 07 Sep 2021 19:42:43 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931bdaaeb048d3dff8468154aa9eceea8e363d63dc61208df60553535bfe8f85`  
		Last Modified: Tue, 09 Nov 2021 00:42:20 GMT  
		Size: 11.3 MB (11323714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f913866909777fce146b3d1c6a81b811018e4bd5ba8ecd4d29168eb9dcced`  
		Last Modified: Tue, 09 Nov 2021 00:42:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.2300; amd64

```console
$ docker pull caddy@sha256:4a8d9dccf760a0249237dfcf9726c0eb1b06e0b19f5ff67cf8718f8da29507c5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718934999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea4590fabf41404b64c9e90299fd322ac88350fd817d631f26264b5915ed362`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:12:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Nov 2021 20:12:21 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:13:18 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Nov 2021 20:13:19 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Nov 2021 20:13:20 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Nov 2021 20:13:21 GMT
VOLUME [c:/config]
# Wed, 10 Nov 2021 20:13:22 GMT
VOLUME [c:/data]
# Wed, 10 Nov 2021 20:13:23 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 10 Nov 2021 20:13:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Nov 2021 20:13:25 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Nov 2021 20:13:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Nov 2021 20:13:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Nov 2021 20:13:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Nov 2021 20:13:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Nov 2021 20:13:30 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Nov 2021 20:13:31 GMT
EXPOSE 80
# Wed, 10 Nov 2021 20:13:32 GMT
EXPOSE 443
# Wed, 10 Nov 2021 20:13:33 GMT
EXPOSE 2019
# Wed, 10 Nov 2021 20:14:19 GMT
RUN caddy version
# Wed, 10 Nov 2021 20:14:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b6e8b6a9caee6f47bdb32f6ec53fd2836fc02cddea3324c72caf380622fc31`  
		Last Modified: Wed, 10 Nov 2021 20:20:37 GMT  
		Size: 370.6 KB (370576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0308f92ecf7a222e22b826cf5c198551ffc380b76ee3e8de67da904b4b02f873`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05df7693285564a1ff855781db06d1dab2fa702b5492fd55461fc675cefb47b6`  
		Last Modified: Wed, 10 Nov 2021 20:20:50 GMT  
		Size: 12.1 MB (12127869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a1d26d8d7789115491377813de4a8a0c15aa4772e3b22b229a4a061f4994d5`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766e31d6b0534ea731f651ccd59e3397360e7878802aaf90257635b0edd37086`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b6f52680a8e584e06bb957343f7acef41f8863af076fed0c94c583f6a6a8ea`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3be75f11ed2b624d7b0d85454d91e6ba425c4b11d179b44611f0353c75976a5`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bb0fed8a1d238828c7b967ddc9453e83dc38e811f50de90a87ca4a79677e3e`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3343adb9cf1bed7b331007eea1fb0bfdcdcc2a11c2c295d513a73d451d338298`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655ad263ab440756e44a5b758408a577f4ba4e960ae9daec72945afc3047553f`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09b8e61a4bbdc190857116fd8fc09cd71a5409e0bf984c7a033272b2ef5f5bb`  
		Last Modified: Wed, 10 Nov 2021 20:20:32 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9723996732fa25ff5ef95b4bd85c9ddf6dfd27408fe9e220bf0156031ade487d`  
		Last Modified: Wed, 10 Nov 2021 20:20:32 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d58c78cd1d1a8562bd34f68b10ada8622f98bf19ad87174e2a3810657e48e70`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67885c8112bf51b21d408141b4bf3b2e13f08f96cdcd873dc6ca1310bdf08f65`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77274081e32b6ce8f84a136cb45008f07cd542a8f2fa0cb8a355331280e27248`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acafd6faed9e989da5b7ca4bcf5d704b15d86d0b5076b645224a578b5453eb61`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109d2337e42e4f8cfc28c01475b5d1ab49d1e776006c622915ec2166c8fead72`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ee8d0bd71b0b4f05c46aa89f1434f50b4685f23ab7e0e092ae5f46e1d150ad`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd8ebab410bbbe5d576ac2f9ec8f4f2b9d251ae4a307bc8c11bb47165553f63`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 290.2 KB (290194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a550a1217bcfc790088e7a6d4f32ebdea15bae25f297c4683cb3dfc3e6c72e4d`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.14393.4770; amd64

```console
$ docker pull caddy@sha256:2c091f3638b3d3948ffa8c2d95a9be662e858768ffc52e366872371a68d003a1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6285957464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fb2d13bfaf3ee5703b28aa6d939cbfac5b14658e1e3e91bbae594e1c4b22a2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:15:34 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Nov 2021 20:15:35 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:16:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Nov 2021 20:16:39 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Nov 2021 20:16:40 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Nov 2021 20:16:41 GMT
VOLUME [c:/config]
# Wed, 10 Nov 2021 20:16:42 GMT
VOLUME [c:/data]
# Wed, 10 Nov 2021 20:16:43 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 10 Nov 2021 20:16:44 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Nov 2021 20:16:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Nov 2021 20:16:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Nov 2021 20:16:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Nov 2021 20:16:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Nov 2021 20:16:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Nov 2021 20:16:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Nov 2021 20:16:50 GMT
EXPOSE 80
# Wed, 10 Nov 2021 20:16:51 GMT
EXPOSE 443
# Wed, 10 Nov 2021 20:16:52 GMT
EXPOSE 2019
# Wed, 10 Nov 2021 20:17:30 GMT
RUN caddy version
# Wed, 10 Nov 2021 20:17:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224cfcc2d1317d73465188f71867febbba9a64bbfcdf83b35bccd662bdb25748`  
		Last Modified: Wed, 10 Nov 2021 20:21:11 GMT  
		Size: 366.8 KB (366836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98f673e7fe75a29f4060341dab79e20ad059162395f10fb1fc2504379d12f22`  
		Last Modified: Wed, 10 Nov 2021 20:21:10 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6dc3d9f8e8e85985894d372a912cae2cbc64cc10540262498597bbe8cad8c31`  
		Last Modified: Wed, 10 Nov 2021 20:21:24 GMT  
		Size: 12.2 MB (12158174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197a3f340985e5e76e3ae77fcbb9e208f521abbad0cfb8921d27d4afe569f280`  
		Last Modified: Wed, 10 Nov 2021 20:21:13 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1443a981044b58af1bae85624fffe4dde7c1759e6a5f930ddaf2eb70bc3185dd`  
		Last Modified: Wed, 10 Nov 2021 20:21:10 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1b023614dd84860e7a4fdd1855131b5478b9b747a40fc9383467934e48e310`  
		Last Modified: Wed, 10 Nov 2021 20:21:09 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daca4ab6367b318ae3a2df27bbe0c53c12ee1a0196fc4f43a43ec47acd74c7c`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a288866cea4075f0f825973ce9d3369dd9411f73c325ed870a5233b383476dbc`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea1c63b1b4cb8f39b59025d926f384679d17bb660eceafe7f7c9418dcdfad61`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b25f60f98964a2d03947e1dac0b01388ad6c9c65497e546f8efe7f2fdcd35e`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d10f21fe32d5dd37a74db003c1119b2aaba639690b10ad4c46d22e2699140fc`  
		Last Modified: Wed, 10 Nov 2021 20:21:06 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4bd5845100c889806835753480fb0016610fbfab35d197c6aa641d73c114ed`  
		Last Modified: Wed, 10 Nov 2021 20:21:06 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190767770423c20b77f963553559cfa26d18b490228ad11c4f9fcf62e6dcefd7`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab0412df33f87a4e77ce1ef8afc68a04cd9a9a56ce9a21e3494f4e4f7c1083a`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80edcc113a751c789aee343b18fdb12c9099cd642cf099ab6a962c7cb0bce8b`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d513b74afabeb0e8050ca955cdf8b72040cabc21350ab394862808bd4382649`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc99c5e78f676bc2fed853c2d43f71dedcbf29fe3a6f69f5d0bc1eabca7f8e98`  
		Last Modified: Wed, 10 Nov 2021 20:21:04 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1532dfe2f3d7f9a4d2eed5ac842a7b54e160fb4d856388e1153d0c6488bab749`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c6594f3623b09c0359fe4347b1981678cebb55cebad4bd683d4bc059e0a201`  
		Last Modified: Wed, 10 Nov 2021 20:21:04 GMT  
		Size: 316.3 KB (316295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c07c5e836014edc4e052889ecbe945aa470b434f2563726bd4f9684da37bfc1`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:3864aebe0cb9d8ec8b0707762c6637cf9ad27a88bde3be6f9d0842eb01a19666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `caddy:windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull caddy@sha256:4a8d9dccf760a0249237dfcf9726c0eb1b06e0b19f5ff67cf8718f8da29507c5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718934999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea4590fabf41404b64c9e90299fd322ac88350fd817d631f26264b5915ed362`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:12:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Nov 2021 20:12:21 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:13:18 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Nov 2021 20:13:19 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Nov 2021 20:13:20 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Nov 2021 20:13:21 GMT
VOLUME [c:/config]
# Wed, 10 Nov 2021 20:13:22 GMT
VOLUME [c:/data]
# Wed, 10 Nov 2021 20:13:23 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 10 Nov 2021 20:13:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Nov 2021 20:13:25 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Nov 2021 20:13:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Nov 2021 20:13:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Nov 2021 20:13:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Nov 2021 20:13:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Nov 2021 20:13:30 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Nov 2021 20:13:31 GMT
EXPOSE 80
# Wed, 10 Nov 2021 20:13:32 GMT
EXPOSE 443
# Wed, 10 Nov 2021 20:13:33 GMT
EXPOSE 2019
# Wed, 10 Nov 2021 20:14:19 GMT
RUN caddy version
# Wed, 10 Nov 2021 20:14:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b6e8b6a9caee6f47bdb32f6ec53fd2836fc02cddea3324c72caf380622fc31`  
		Last Modified: Wed, 10 Nov 2021 20:20:37 GMT  
		Size: 370.6 KB (370576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0308f92ecf7a222e22b826cf5c198551ffc380b76ee3e8de67da904b4b02f873`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05df7693285564a1ff855781db06d1dab2fa702b5492fd55461fc675cefb47b6`  
		Last Modified: Wed, 10 Nov 2021 20:20:50 GMT  
		Size: 12.1 MB (12127869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a1d26d8d7789115491377813de4a8a0c15aa4772e3b22b229a4a061f4994d5`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766e31d6b0534ea731f651ccd59e3397360e7878802aaf90257635b0edd37086`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b6f52680a8e584e06bb957343f7acef41f8863af076fed0c94c583f6a6a8ea`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3be75f11ed2b624d7b0d85454d91e6ba425c4b11d179b44611f0353c75976a5`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bb0fed8a1d238828c7b967ddc9453e83dc38e811f50de90a87ca4a79677e3e`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3343adb9cf1bed7b331007eea1fb0bfdcdcc2a11c2c295d513a73d451d338298`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655ad263ab440756e44a5b758408a577f4ba4e960ae9daec72945afc3047553f`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09b8e61a4bbdc190857116fd8fc09cd71a5409e0bf984c7a033272b2ef5f5bb`  
		Last Modified: Wed, 10 Nov 2021 20:20:32 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9723996732fa25ff5ef95b4bd85c9ddf6dfd27408fe9e220bf0156031ade487d`  
		Last Modified: Wed, 10 Nov 2021 20:20:32 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d58c78cd1d1a8562bd34f68b10ada8622f98bf19ad87174e2a3810657e48e70`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67885c8112bf51b21d408141b4bf3b2e13f08f96cdcd873dc6ca1310bdf08f65`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77274081e32b6ce8f84a136cb45008f07cd542a8f2fa0cb8a355331280e27248`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acafd6faed9e989da5b7ca4bcf5d704b15d86d0b5076b645224a578b5453eb61`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109d2337e42e4f8cfc28c01475b5d1ab49d1e776006c622915ec2166c8fead72`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ee8d0bd71b0b4f05c46aa89f1434f50b4685f23ab7e0e092ae5f46e1d150ad`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd8ebab410bbbe5d576ac2f9ec8f4f2b9d251ae4a307bc8c11bb47165553f63`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 290.2 KB (290194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a550a1217bcfc790088e7a6d4f32ebdea15bae25f297c4683cb3dfc3e6c72e4d`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.14393.4770; amd64

```console
$ docker pull caddy@sha256:2c091f3638b3d3948ffa8c2d95a9be662e858768ffc52e366872371a68d003a1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6285957464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fb2d13bfaf3ee5703b28aa6d939cbfac5b14658e1e3e91bbae594e1c4b22a2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:15:34 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Nov 2021 20:15:35 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:16:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Nov 2021 20:16:39 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Nov 2021 20:16:40 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Nov 2021 20:16:41 GMT
VOLUME [c:/config]
# Wed, 10 Nov 2021 20:16:42 GMT
VOLUME [c:/data]
# Wed, 10 Nov 2021 20:16:43 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 10 Nov 2021 20:16:44 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Nov 2021 20:16:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Nov 2021 20:16:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Nov 2021 20:16:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Nov 2021 20:16:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Nov 2021 20:16:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Nov 2021 20:16:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Nov 2021 20:16:50 GMT
EXPOSE 80
# Wed, 10 Nov 2021 20:16:51 GMT
EXPOSE 443
# Wed, 10 Nov 2021 20:16:52 GMT
EXPOSE 2019
# Wed, 10 Nov 2021 20:17:30 GMT
RUN caddy version
# Wed, 10 Nov 2021 20:17:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224cfcc2d1317d73465188f71867febbba9a64bbfcdf83b35bccd662bdb25748`  
		Last Modified: Wed, 10 Nov 2021 20:21:11 GMT  
		Size: 366.8 KB (366836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98f673e7fe75a29f4060341dab79e20ad059162395f10fb1fc2504379d12f22`  
		Last Modified: Wed, 10 Nov 2021 20:21:10 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6dc3d9f8e8e85985894d372a912cae2cbc64cc10540262498597bbe8cad8c31`  
		Last Modified: Wed, 10 Nov 2021 20:21:24 GMT  
		Size: 12.2 MB (12158174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197a3f340985e5e76e3ae77fcbb9e208f521abbad0cfb8921d27d4afe569f280`  
		Last Modified: Wed, 10 Nov 2021 20:21:13 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1443a981044b58af1bae85624fffe4dde7c1759e6a5f930ddaf2eb70bc3185dd`  
		Last Modified: Wed, 10 Nov 2021 20:21:10 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1b023614dd84860e7a4fdd1855131b5478b9b747a40fc9383467934e48e310`  
		Last Modified: Wed, 10 Nov 2021 20:21:09 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daca4ab6367b318ae3a2df27bbe0c53c12ee1a0196fc4f43a43ec47acd74c7c`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a288866cea4075f0f825973ce9d3369dd9411f73c325ed870a5233b383476dbc`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea1c63b1b4cb8f39b59025d926f384679d17bb660eceafe7f7c9418dcdfad61`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b25f60f98964a2d03947e1dac0b01388ad6c9c65497e546f8efe7f2fdcd35e`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d10f21fe32d5dd37a74db003c1119b2aaba639690b10ad4c46d22e2699140fc`  
		Last Modified: Wed, 10 Nov 2021 20:21:06 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4bd5845100c889806835753480fb0016610fbfab35d197c6aa641d73c114ed`  
		Last Modified: Wed, 10 Nov 2021 20:21:06 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190767770423c20b77f963553559cfa26d18b490228ad11c4f9fcf62e6dcefd7`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab0412df33f87a4e77ce1ef8afc68a04cd9a9a56ce9a21e3494f4e4f7c1083a`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80edcc113a751c789aee343b18fdb12c9099cd642cf099ab6a962c7cb0bce8b`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d513b74afabeb0e8050ca955cdf8b72040cabc21350ab394862808bd4382649`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc99c5e78f676bc2fed853c2d43f71dedcbf29fe3a6f69f5d0bc1eabca7f8e98`  
		Last Modified: Wed, 10 Nov 2021 20:21:04 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1532dfe2f3d7f9a4d2eed5ac842a7b54e160fb4d856388e1153d0c6488bab749`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c6594f3623b09c0359fe4347b1981678cebb55cebad4bd683d4bc059e0a201`  
		Last Modified: Wed, 10 Nov 2021 20:21:04 GMT  
		Size: 316.3 KB (316295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c07c5e836014edc4e052889ecbe945aa470b434f2563726bd4f9684da37bfc1`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:4d8f28e3fbdc28a6ebdf57a867626560f0651157d3cf1cddaa279a9f57c34c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull caddy@sha256:4a8d9dccf760a0249237dfcf9726c0eb1b06e0b19f5ff67cf8718f8da29507c5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2718934999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea4590fabf41404b64c9e90299fd322ac88350fd817d631f26264b5915ed362`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:12:20 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Nov 2021 20:12:21 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:13:18 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Nov 2021 20:13:19 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Nov 2021 20:13:20 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Nov 2021 20:13:21 GMT
VOLUME [c:/config]
# Wed, 10 Nov 2021 20:13:22 GMT
VOLUME [c:/data]
# Wed, 10 Nov 2021 20:13:23 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 10 Nov 2021 20:13:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Nov 2021 20:13:25 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Nov 2021 20:13:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Nov 2021 20:13:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Nov 2021 20:13:28 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Nov 2021 20:13:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Nov 2021 20:13:30 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Nov 2021 20:13:31 GMT
EXPOSE 80
# Wed, 10 Nov 2021 20:13:32 GMT
EXPOSE 443
# Wed, 10 Nov 2021 20:13:33 GMT
EXPOSE 2019
# Wed, 10 Nov 2021 20:14:19 GMT
RUN caddy version
# Wed, 10 Nov 2021 20:14:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b6e8b6a9caee6f47bdb32f6ec53fd2836fc02cddea3324c72caf380622fc31`  
		Last Modified: Wed, 10 Nov 2021 20:20:37 GMT  
		Size: 370.6 KB (370576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0308f92ecf7a222e22b826cf5c198551ffc380b76ee3e8de67da904b4b02f873`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05df7693285564a1ff855781db06d1dab2fa702b5492fd55461fc675cefb47b6`  
		Last Modified: Wed, 10 Nov 2021 20:20:50 GMT  
		Size: 12.1 MB (12127869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a1d26d8d7789115491377813de4a8a0c15aa4772e3b22b229a4a061f4994d5`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766e31d6b0534ea731f651ccd59e3397360e7878802aaf90257635b0edd37086`  
		Last Modified: Wed, 10 Nov 2021 20:20:36 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b6f52680a8e584e06bb957343f7acef41f8863af076fed0c94c583f6a6a8ea`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3be75f11ed2b624d7b0d85454d91e6ba425c4b11d179b44611f0353c75976a5`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bb0fed8a1d238828c7b967ddc9453e83dc38e811f50de90a87ca4a79677e3e`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3343adb9cf1bed7b331007eea1fb0bfdcdcc2a11c2c295d513a73d451d338298`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655ad263ab440756e44a5b758408a577f4ba4e960ae9daec72945afc3047553f`  
		Last Modified: Wed, 10 Nov 2021 20:20:34 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09b8e61a4bbdc190857116fd8fc09cd71a5409e0bf984c7a033272b2ef5f5bb`  
		Last Modified: Wed, 10 Nov 2021 20:20:32 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9723996732fa25ff5ef95b4bd85c9ddf6dfd27408fe9e220bf0156031ade487d`  
		Last Modified: Wed, 10 Nov 2021 20:20:32 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d58c78cd1d1a8562bd34f68b10ada8622f98bf19ad87174e2a3810657e48e70`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67885c8112bf51b21d408141b4bf3b2e13f08f96cdcd873dc6ca1310bdf08f65`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77274081e32b6ce8f84a136cb45008f07cd542a8f2fa0cb8a355331280e27248`  
		Last Modified: Wed, 10 Nov 2021 20:20:31 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acafd6faed9e989da5b7ca4bcf5d704b15d86d0b5076b645224a578b5453eb61`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109d2337e42e4f8cfc28c01475b5d1ab49d1e776006c622915ec2166c8fead72`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ee8d0bd71b0b4f05c46aa89f1434f50b4685f23ab7e0e092ae5f46e1d150ad`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd8ebab410bbbe5d576ac2f9ec8f4f2b9d251ae4a307bc8c11bb47165553f63`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 290.2 KB (290194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a550a1217bcfc790088e7a6d4f32ebdea15bae25f297c4683cb3dfc3e6c72e4d`  
		Last Modified: Wed, 10 Nov 2021 20:20:29 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:b399e4134eac2ed1e68a9f6d12fa6c2f89351edd4b13f45e687d84ee2c8c7891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `caddy:windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull caddy@sha256:2c091f3638b3d3948ffa8c2d95a9be662e858768ffc52e366872371a68d003a1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6285957464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fb2d13bfaf3ee5703b28aa6d939cbfac5b14658e1e3e91bbae594e1c4b22a2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:15:34 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Nov 2021 20:15:35 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:16:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Nov 2021 20:16:39 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Nov 2021 20:16:40 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Nov 2021 20:16:41 GMT
VOLUME [c:/config]
# Wed, 10 Nov 2021 20:16:42 GMT
VOLUME [c:/data]
# Wed, 10 Nov 2021 20:16:43 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 10 Nov 2021 20:16:44 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Nov 2021 20:16:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Nov 2021 20:16:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Nov 2021 20:16:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Nov 2021 20:16:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Nov 2021 20:16:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Nov 2021 20:16:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Nov 2021 20:16:50 GMT
EXPOSE 80
# Wed, 10 Nov 2021 20:16:51 GMT
EXPOSE 443
# Wed, 10 Nov 2021 20:16:52 GMT
EXPOSE 2019
# Wed, 10 Nov 2021 20:17:30 GMT
RUN caddy version
# Wed, 10 Nov 2021 20:17:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224cfcc2d1317d73465188f71867febbba9a64bbfcdf83b35bccd662bdb25748`  
		Last Modified: Wed, 10 Nov 2021 20:21:11 GMT  
		Size: 366.8 KB (366836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98f673e7fe75a29f4060341dab79e20ad059162395f10fb1fc2504379d12f22`  
		Last Modified: Wed, 10 Nov 2021 20:21:10 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6dc3d9f8e8e85985894d372a912cae2cbc64cc10540262498597bbe8cad8c31`  
		Last Modified: Wed, 10 Nov 2021 20:21:24 GMT  
		Size: 12.2 MB (12158174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197a3f340985e5e76e3ae77fcbb9e208f521abbad0cfb8921d27d4afe569f280`  
		Last Modified: Wed, 10 Nov 2021 20:21:13 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1443a981044b58af1bae85624fffe4dde7c1759e6a5f930ddaf2eb70bc3185dd`  
		Last Modified: Wed, 10 Nov 2021 20:21:10 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1b023614dd84860e7a4fdd1855131b5478b9b747a40fc9383467934e48e310`  
		Last Modified: Wed, 10 Nov 2021 20:21:09 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daca4ab6367b318ae3a2df27bbe0c53c12ee1a0196fc4f43a43ec47acd74c7c`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a288866cea4075f0f825973ce9d3369dd9411f73c325ed870a5233b383476dbc`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea1c63b1b4cb8f39b59025d926f384679d17bb660eceafe7f7c9418dcdfad61`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b25f60f98964a2d03947e1dac0b01388ad6c9c65497e546f8efe7f2fdcd35e`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d10f21fe32d5dd37a74db003c1119b2aaba639690b10ad4c46d22e2699140fc`  
		Last Modified: Wed, 10 Nov 2021 20:21:06 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4bd5845100c889806835753480fb0016610fbfab35d197c6aa641d73c114ed`  
		Last Modified: Wed, 10 Nov 2021 20:21:06 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190767770423c20b77f963553559cfa26d18b490228ad11c4f9fcf62e6dcefd7`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab0412df33f87a4e77ce1ef8afc68a04cd9a9a56ce9a21e3494f4e4f7c1083a`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80edcc113a751c789aee343b18fdb12c9099cd642cf099ab6a962c7cb0bce8b`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d513b74afabeb0e8050ca955cdf8b72040cabc21350ab394862808bd4382649`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc99c5e78f676bc2fed853c2d43f71dedcbf29fe3a6f69f5d0bc1eabca7f8e98`  
		Last Modified: Wed, 10 Nov 2021 20:21:04 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1532dfe2f3d7f9a4d2eed5ac842a7b54e160fb4d856388e1153d0c6488bab749`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c6594f3623b09c0359fe4347b1981678cebb55cebad4bd683d4bc059e0a201`  
		Last Modified: Wed, 10 Nov 2021 20:21:04 GMT  
		Size: 316.3 KB (316295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c07c5e836014edc4e052889ecbe945aa470b434f2563726bd4f9684da37bfc1`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
