## `caddy:latest`

```console
$ docker pull caddy@sha256:4916ad44f7563c0dd767d900ffafee75016f01e3c966b3c46e6c2f7bc896b2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2686; amd64

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
