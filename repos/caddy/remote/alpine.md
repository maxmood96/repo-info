## `caddy:alpine`

```console
$ docker pull caddy@sha256:b518403f906c605f5d9deecf2cef6dd107afda1e8cd39336406c88b1f4d95405
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
