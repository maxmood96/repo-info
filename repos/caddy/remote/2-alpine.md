## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:0157ce2e3977145c950dc562b339351cd37d06abe9ac8bf36b04b1b2f8ce6104
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
$ docker pull caddy@sha256:aaa9d8750860e5b886fab8c4da6842782ec2eb2e963e6d48ad59657fadd9a6aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18474296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0e21ab2b0efc5ac0207c16134ac96b3779212c692cde05a24f73a68fec756a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:43:13 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 22:43:15 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 18:19:15 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:19:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 18:19:17 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 18:19:18 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 18:19:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 80
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 443
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 18:19:18 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 18:19:19 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 18:19:19 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37be51084fb891c6796079e693b73f6f882266a5e66211344173031e2b0c8ffd`  
		Last Modified: Thu, 28 Sep 2023 22:43:35 GMT  
		Size: 350.8 KB (350826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d867aa37ac50364bf4082dc48c7d4e1b88ead3164d47855e1bbc2ef3678cfc`  
		Last Modified: Thu, 28 Sep 2023 22:43:35 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9a4bfabc0b0dc6924b7d8aad02805798c86ada09d9d11861f29ed76915f758`  
		Last Modified: Thu, 12 Oct 2023 18:19:43 GMT  
		Size: 14.7 MB (14713998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:be2cb3ef217d514df988a7fef43bc11cf8267f3c3eea319a82c6c4c2985cd7fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17422254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5375c06eba744fadf74e23a036a6af05a75573760968f9d65a405d7401973be3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 21:59:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 21:59:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 01:39:17 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 01:39:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 01:39:20 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 01:39:20 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 01:39:20 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 01:39:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 01:39:21 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 80
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 443
# Thu, 12 Oct 2023 01:39:21 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 01:39:22 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 01:39:22 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 01:39:22 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1018057a600163b1c1b92c21ade975c631b2f8ccde66d524cfe0ecdac8e1920d`  
		Last Modified: Thu, 28 Sep 2023 21:59:43 GMT  
		Size: 347.6 KB (347613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec54680cbf2cb1a25285c82a7888498ab47d03a68db200a160d7162325a5be19`  
		Last Modified: Thu, 28 Sep 2023 21:59:43 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38012b56d72a4a2c2a42ed660476530218852cf8953587cb803fab0cf7de99c3`  
		Last Modified: Thu, 12 Oct 2023 01:39:46 GMT  
		Size: 13.9 MB (13921845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:cc67ef274e0b09f75c4adf46397b2b796c00d9d014d1312d53bc3e16fa763bbf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17155291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67b853d3cd7e1ec8e5fdb884e061c15e6da29f25d0954bf803f08625dc542bf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:19:18 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 23:19:20 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 18:03:38 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 18:03:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 18:03:41 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 18:03:41 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 18:03:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 18:03:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 80
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 443
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 18:03:42 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 18:03:42 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 18:03:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66901ba48d0ee53cd827f4eb2cfd8b049cebba8c3d307b69760e1be917f69476`  
		Last Modified: Thu, 28 Sep 2023 23:19:46 GMT  
		Size: 344.4 KB (344448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dddeb3f6febb36993d8a51ad919784fd152aab5f6e17fe00d579916f32e42911`  
		Last Modified: Thu, 28 Sep 2023 23:19:46 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00371969ebc6f50beb432e93f29b2658ffdbf2de985784e17b0a8e696970a7d`  
		Last Modified: Thu, 12 Oct 2023 18:04:03 GMT  
		Size: 13.9 MB (13903435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:c5cdeee3505159e6a4ebd367b13f1a6bb32d424327be8ee4a3e09734c5cf63d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17273792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6797cb1033afffac8c55f0ee0f0dd9f60e58dc19ef1edc5852606eced4c793b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 01:16:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 29 Sep 2023 01:16:13 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 12 Oct 2023 19:45:02 GMT
ENV CADDY_VERSION=v2.7.5
# Thu, 12 Oct 2023 19:45:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='4afdf50ccf3a8f32344dbac46006ca2b5d90c2ef656c53e8617f1c3b81c5f9e44bd3a9e0b62975f73c85451c354d3d9b5292f5247d18a62d95ab19c8b0a5dba7' ;; 		armhf)   binArch='armv6'; checksum='5f47b4ff5d290799bba1b9183c6ddfe7fee69c8086375337a7498717ce09fc627845f6cb466840daf539c763979ab60fe229b9ddeaf7f92fad800742d4ad5b3a' ;; 		armv7)   binArch='armv7'; checksum='bdd120779427cf288a383ecf9d63fa6b61e2118f189e02263ad45989bae507ce1db84ced60de3b33653e9729166e4ca436785503558955b9934be69138184055' ;; 		aarch64) binArch='arm64'; checksum='a857cbe25bcc5402e9c4fa2a6c36338f91b7e23962beedccd32e10b3aa34dda084ae742c79085d6e7581acfe33f7c9cf161224b1e56cdb661ebfb6f7424b8d0a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='72c66d44cfc8f8d248e04f08903866d62a0e11c36b51c49c08c73c833a3f4322a780405543e721dcf375b71dee06e90230c64141efb2a9614f551e2134f120a9' ;; 		s390x)   binArch='s390x'; checksum='5fb95fb495da282330f34b7f23fff3e664638397dcde2c33a3c7450e448154425b2514573604be3cac03d30b37444c4866170f232f14a33e50bff0d1e1abf126' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.5/caddy_2.7.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 12 Oct 2023 19:45:04 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 12 Oct 2023 19:45:04 GMT
ENV XDG_DATA_HOME=/data
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.version=v2.7.5
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 12 Oct 2023 19:45:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 12 Oct 2023 19:45:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 80
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 443
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 443/udp
# Thu, 12 Oct 2023 19:45:05 GMT
EXPOSE 2019
# Thu, 12 Oct 2023 19:45:05 GMT
WORKDIR /srv
# Thu, 12 Oct 2023 19:45:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f21cb0286edf1f5fefb4a859b414a446bb81baa9e8901fc8f4eca55a43aeeec`  
		Last Modified: Fri, 29 Sep 2023 01:16:34 GMT  
		Size: 360.6 KB (360643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5444b3f9419d06a4b77a65935a3b1c6e657c607bcfb9e3bd1abebe57eae36e6a`  
		Last Modified: Fri, 29 Sep 2023 01:16:34 GMT  
		Size: 7.5 KB (7507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516e60671cdfd4ec2cb64a788cecf65bb2166ba5bf3e7bba029ccf0c8c0dbeb3`  
		Last Modified: Thu, 12 Oct 2023 19:45:30 GMT  
		Size: 13.6 MB (13573811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:65084a14a1557b92af5b8ba6fcba9a7a710ed5caef1e2310f9622166608c9531
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16945195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ba45deaa04c3feac6474c22204ac6f5ebc380b331ff7d585ecd196284459b3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 21:22:20 GMT
ADD file:a720acb99214334c501363d564d8cae9b90d062ccf8a24a5ba1c831545b783dd in / 
# Thu, 28 Sep 2023 21:22:21 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 02:17:03 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 29 Sep 2023 02:17:06 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Fri, 29 Sep 2023 02:17:06 GMT
ENV CADDY_VERSION=v2.7.4
# Fri, 29 Sep 2023 02:17:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68cc53c79b88da5f1a33f5a1e1da7fbac5ad041380e91e27663b44e0cb2d8e07e08690295e86e9e65a37472b52f7d95f84f383ee0b8f3d5e1bd4b755d3990e6a' ;; 		armhf)   binArch='armv6'; checksum='e6db35a9a2d78a8375d287bb1e4dc37f21eeadd5e41ad0c4adc2e35d3f80e061602d3e9c498ac4a4956754ad7be8c5f0489395db2c9729782906d771e528c898' ;; 		armv7)   binArch='armv7'; checksum='5e94a538e9f9d62da2cdfae04294e943800ced348a66fad13ab6c99aa8184485a1ceba2dbcf13d996f4a4bad1a49e2774b880182b0edcf1a112b1001c552e424' ;; 		aarch64) binArch='arm64'; checksum='eb9be2b3d09351d97843a4e2b73f36a4d36d3cb689dd580b5706b243fb66d0dc8a04460fd4a87dea772442c9fe7a1cddb0022e085be663f3d1e12127e3295d9d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3accb7bbfe23d33057bf023951b3ccddd4cf1708314adad71aa2f298581da293af1bc817ff346248c895499908de7ced661f64a4d115b41657630e14cc8f62a7' ;; 		s390x)   binArch='s390x'; checksum='73c4961582ddc4a0d013c7af85642cf68a7bb0069e04aabba28ff3270f86853b394277d90b7b971695b949087e8d3fb50661da03953e632705e3f63c6e7acdb8' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.4/caddy_2.7.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 29 Sep 2023 02:17:13 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 29 Sep 2023 02:17:14 GMT
ENV XDG_DATA_HOME=/data
# Fri, 29 Sep 2023 02:17:15 GMT
LABEL org.opencontainers.image.version=v2.7.4
# Fri, 29 Sep 2023 02:17:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 29 Sep 2023 02:17:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 29 Sep 2023 02:17:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 29 Sep 2023 02:17:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 29 Sep 2023 02:17:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 29 Sep 2023 02:17:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 29 Sep 2023 02:17:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 29 Sep 2023 02:17:21 GMT
EXPOSE 80
# Fri, 29 Sep 2023 02:17:21 GMT
EXPOSE 443
# Fri, 29 Sep 2023 02:17:22 GMT
EXPOSE 443/udp
# Fri, 29 Sep 2023 02:17:22 GMT
EXPOSE 2019
# Fri, 29 Sep 2023 02:17:24 GMT
WORKDIR /srv
# Fri, 29 Sep 2023 02:17:25 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:cd37f9856024d6685ac0233823aded690551c5872d6a27699a96c6a479d20f6f`  
		Last Modified: Thu, 28 Sep 2023 21:23:43 GMT  
		Size: 3.3 MB (3346508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa65cea7f5d70d1e203b851e43ad676e92f28c930ad32b6691e84ff9b5cda87`  
		Last Modified: Fri, 29 Sep 2023 02:18:03 GMT  
		Size: 362.2 KB (362182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7089a1d537371e29a65d106f43b45f2a0367d4d1db0eb7d6b7099f8ba05645`  
		Last Modified: Fri, 29 Sep 2023 02:18:01 GMT  
		Size: 7.5 KB (7507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b93ab741fa6270144ea59d6a5fa3c4138286a569f246fdccd829b317b051f3a`  
		Last Modified: Fri, 29 Sep 2023 02:18:05 GMT  
		Size: 13.2 MB (13228998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:9e13bd2b56147eecc80f1fe1710e4350ea63d5edfb389fa89e2c6de06c08593a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17721238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f0101e0f893afb763d99b2050dbf4d68a44aae29785af6c05af5a552b0c1a7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 22:19:38 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Thu, 28 Sep 2023 22:19:39 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/0c7fa00a87c65a6ef47ed36d841cd223682a2a2c/welcome/index.html"
# Thu, 28 Sep 2023 22:19:39 GMT
ENV CADDY_VERSION=v2.7.4
# Thu, 28 Sep 2023 22:19:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68cc53c79b88da5f1a33f5a1e1da7fbac5ad041380e91e27663b44e0cb2d8e07e08690295e86e9e65a37472b52f7d95f84f383ee0b8f3d5e1bd4b755d3990e6a' ;; 		armhf)   binArch='armv6'; checksum='e6db35a9a2d78a8375d287bb1e4dc37f21eeadd5e41ad0c4adc2e35d3f80e061602d3e9c498ac4a4956754ad7be8c5f0489395db2c9729782906d771e528c898' ;; 		armv7)   binArch='armv7'; checksum='5e94a538e9f9d62da2cdfae04294e943800ced348a66fad13ab6c99aa8184485a1ceba2dbcf13d996f4a4bad1a49e2774b880182b0edcf1a112b1001c552e424' ;; 		aarch64) binArch='arm64'; checksum='eb9be2b3d09351d97843a4e2b73f36a4d36d3cb689dd580b5706b243fb66d0dc8a04460fd4a87dea772442c9fe7a1cddb0022e085be663f3d1e12127e3295d9d' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='3accb7bbfe23d33057bf023951b3ccddd4cf1708314adad71aa2f298581da293af1bc817ff346248c895499908de7ced661f64a4d115b41657630e14cc8f62a7' ;; 		s390x)   binArch='s390x'; checksum='73c4961582ddc4a0d013c7af85642cf68a7bb0069e04aabba28ff3270f86853b394277d90b7b971695b949087e8d3fb50661da03953e632705e3f63c6e7acdb8' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.4/caddy_2.7.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 28 Sep 2023 22:19:42 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 28 Sep 2023 22:19:42 GMT
ENV XDG_DATA_HOME=/data
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.version=v2.7.4
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 28 Sep 2023 22:19:42 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 28 Sep 2023 22:19:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 80
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 443
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 443/udp
# Thu, 28 Sep 2023 22:19:43 GMT
EXPOSE 2019
# Thu, 28 Sep 2023 22:19:44 GMT
WORKDIR /srv
# Thu, 28 Sep 2023 22:19:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed3df874173df47ad0bd0ef67b8ee598c77921810d84a67fd2984c4f8151c91`  
		Last Modified: Thu, 28 Sep 2023 22:20:14 GMT  
		Size: 354.9 KB (354948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a69c42a5c7fc6d73c00c7f6eb68522f3881aae55db4f85a8400e83b678b181`  
		Last Modified: Thu, 28 Sep 2023 22:20:14 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793016dc78c9794c627c07afcd2fb34af4ee470ee7fef1a1596eff0c59ba6659`  
		Last Modified: Thu, 28 Sep 2023 22:20:16 GMT  
		Size: 14.1 MB (14143684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
