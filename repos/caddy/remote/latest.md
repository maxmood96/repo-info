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
