## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:b5a59725783bab0d65803f87028c68dd6611ca6184040bd98b18797cbe26bdd9
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
$ docker pull caddy@sha256:e9451e07cc2803c7a90963bf251e0b81abcc9967ca49fb7a87c3301fad5e60dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14839844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735d6b37a42653d291d2a89384895976357b1437fb674a07614cbd3fb35f00e0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 00:02:43 GMT
RUN apk add --no-cache ca-certificates mailcap
# Sat, 19 Mar 2022 00:02:45 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Sat, 19 Mar 2022 00:02:45 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 19 Mar 2022 00:02:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 19 Mar 2022 00:02:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 19 Mar 2022 00:02:49 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 19 Mar 2022 00:02:49 GMT
ENV XDG_DATA_HOME=/data
# Sat, 19 Mar 2022 00:02:49 GMT
VOLUME [/config]
# Sat, 19 Mar 2022 00:02:50 GMT
VOLUME [/data]
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 19 Mar 2022 00:02:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 19 Mar 2022 00:02:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 19 Mar 2022 00:02:52 GMT
EXPOSE 80
# Sat, 19 Mar 2022 00:02:52 GMT
EXPOSE 443
# Sat, 19 Mar 2022 00:02:52 GMT
EXPOSE 2019
# Sat, 19 Mar 2022 00:02:52 GMT
WORKDIR /srv
# Sat, 19 Mar 2022 00:02:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c225d4ce3a38a8a3e6febdc9bbb81aa1faff22dfdccfc44d557d61621d8c3b3`  
		Last Modified: Sat, 19 Mar 2022 00:03:30 GMT  
		Size: 291.2 KB (291236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b48903a98ce96620ab34d505f9fd3337e46ef729e6b93f4c31442a01c031958`  
		Last Modified: Sat, 19 Mar 2022 00:03:29 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9a49498837c179e70172feedd8b5b1684fda96fc85932d533d15fb395d2d25`  
		Last Modified: Sat, 19 Mar 2022 00:03:32 GMT  
		Size: 11.7 MB (11726453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f986cb0c37bc3e0802acdfcb21bfebfdfadce1af2753530be51de31642dc8db5`  
		Last Modified: Sat, 19 Mar 2022 00:03:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:5f09a9314e7bcb6c997fafb0c72623e4fe1333f5ffacf717901b8d71992a6314
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14052796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23651bcdf82f31f580af8bb2a691742988178ec24273cc7d427790fc899b70d2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:33 GMT
ADD file:8f1611b9334907a82945fdb21e17ee41541ab95050fc199c60fca662759171a5 in / 
# Thu, 17 Mar 2022 14:32:33 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 14:58:04 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 14:58:06 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 14:58:07 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 14:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 14:58:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 14:58:13 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 14:58:14 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 14:58:14 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 14:58:15 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 14:58:15 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 14:58:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 14:58:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 14:58:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 14:58:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 14:58:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 14:58:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 14:58:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 14:58:19 GMT
EXPOSE 80
# Thu, 17 Mar 2022 14:58:19 GMT
EXPOSE 443
# Thu, 17 Mar 2022 14:58:20 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 14:58:20 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 14:58:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4025825e6ef43541c3a3e1ecb0092bc1b098e792051c7e338d6da54f66b19661`  
		Last Modified: Thu, 17 Mar 2022 14:34:09 GMT  
		Size: 2.6 MB (2629364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe387c61070bfe1fbf52bdf2f034ca39f369605473616ebfc4b89287058a395d`  
		Last Modified: Thu, 17 Mar 2022 15:00:12 GMT  
		Size: 291.6 KB (291648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bc40a5454d774d40dfddbe6f85673f34aed00cd8e9a3035963763b18376639`  
		Last Modified: Thu, 17 Mar 2022 15:00:12 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81988b3231106e730dc6c7d0b24ebc84826809dd090bff899495129990559e78`  
		Last Modified: Thu, 17 Mar 2022 15:00:19 GMT  
		Size: 11.1 MB (11125802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd1a3665abdbac555066d2695c45980beba49a104e3a55b2d2cf31f8da4c2da`  
		Last Modified: Thu, 17 Mar 2022 15:00:12 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:5d40c99ca31d7c7cc087a8c0059966c8b9e43f0bafbf525cf4fb1494a45da5b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13833799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde5bec726177426cb4d320b0f016f0a8e4569182c6de303c9c9d042446b6197`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 17:21:06 GMT
ADD file:c25fcf153ea349f64e08a1bd0756ce550f2a081ad56cc40c89027d85d1bc26da in / 
# Thu, 17 Mar 2022 17:21:06 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 18:17:08 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 18:17:11 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 18:17:12 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 18:17:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 18:17:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 18:17:19 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 18:17:19 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 18:17:20 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 18:17:20 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 18:17:21 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 18:17:21 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 18:17:22 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 18:17:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 18:17:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 18:17:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 18:17:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 18:17:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 18:17:25 GMT
EXPOSE 80
# Thu, 17 Mar 2022 18:17:25 GMT
EXPOSE 443
# Thu, 17 Mar 2022 18:17:26 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 18:17:26 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 18:17:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c3a1157c36d8d156f7664fa098212ab2149a64bcb59767cdf4595a86617c17fd`  
		Last Modified: Thu, 17 Mar 2022 17:22:45 GMT  
		Size: 2.4 MB (2430456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376a93fbfdd661b6ba92aa7097c65e646f83c50d150e4227f42141e158b7928b`  
		Last Modified: Thu, 17 Mar 2022 18:19:35 GMT  
		Size: 290.6 KB (290632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3bd6226dffa9763d44b0e5688ab7b844b744846e3cc0fa7d8ab6d3c068e466`  
		Last Modified: Thu, 17 Mar 2022 18:19:35 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9ffbfdd3e888d3f9a94270e0b47ca758645b21ec38f6a203223475052b2802`  
		Last Modified: Thu, 17 Mar 2022 18:19:42 GMT  
		Size: 11.1 MB (11106727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb6dc1be2f2389fa78d2d0002c63575d8d14197e59e0347dbca9ae951a38d4f`  
		Last Modified: Thu, 17 Mar 2022 18:19:35 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:a4e7a7a9d505b716122bbfb9b41e25b8189dafc8115284279687c2021de7aca1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13751720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a574b32ce3c98bd1848efe2e07ad86e55789b4da7fe02909566fa06a0fdbe6a1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 07:13:27 GMT
RUN apk add --no-cache ca-certificates mailcap
# Fri, 18 Mar 2022 07:13:29 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Fri, 18 Mar 2022 07:13:30 GMT
ENV CADDY_VERSION=v2.4.6
# Fri, 18 Mar 2022 07:13:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 18 Mar 2022 07:13:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 18 Mar 2022 07:13:34 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 18 Mar 2022 07:13:35 GMT
ENV XDG_DATA_HOME=/data
# Fri, 18 Mar 2022 07:13:36 GMT
VOLUME [/config]
# Fri, 18 Mar 2022 07:13:37 GMT
VOLUME [/data]
# Fri, 18 Mar 2022 07:13:38 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Fri, 18 Mar 2022 07:13:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 18 Mar 2022 07:13:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 18 Mar 2022 07:13:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 18 Mar 2022 07:13:42 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 18 Mar 2022 07:13:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 18 Mar 2022 07:13:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 18 Mar 2022 07:13:45 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 18 Mar 2022 07:13:46 GMT
EXPOSE 80
# Fri, 18 Mar 2022 07:13:47 GMT
EXPOSE 443
# Fri, 18 Mar 2022 07:13:48 GMT
EXPOSE 2019
# Fri, 18 Mar 2022 07:13:49 GMT
WORKDIR /srv
# Fri, 18 Mar 2022 07:13:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649e3e65430e0077032ab20dedb081c00e1be3a1f4660b94275f242d1dcd295d`  
		Last Modified: Fri, 18 Mar 2022 07:14:57 GMT  
		Size: 291.3 KB (291292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048be0a2d569af2daf2b6cd4728a72f8fecd26611069441023a70b360d3850a0`  
		Last Modified: Fri, 18 Mar 2022 07:14:57 GMT  
		Size: 5.8 KB (5751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e382adfd8256a09e2e4bed4c90c8755fc3ee3c58e0679734cd85e4da6ac486`  
		Last Modified: Fri, 18 Mar 2022 07:14:59 GMT  
		Size: 10.7 MB (10738636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d589a4f582ad58b1be3ac310f968793927b5d1629ae84b5c78100265bd825d`  
		Last Modified: Fri, 18 Mar 2022 07:14:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:b91b55c6bdcfe17f047217339ace7c264f76e9011d077d7f84cb4852667273e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13419279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0272ad9824009f684ca3ecddd7e61583b5994b0c08a6db63295222a0dbf8a2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 18:18:43 GMT
ADD file:bf9c99d8209e0bed9fd3b62cbe691ebf3829d5a35e63e2b066f1f842577a6d24 in / 
# Thu, 17 Mar 2022 18:18:48 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:30:55 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 21:31:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 21:31:03 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 21:31:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 21:31:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 21:31:20 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 21:31:22 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 21:31:24 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 21:31:27 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 21:31:29 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 21:31:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 21:31:34 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 21:31:36 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 21:31:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 21:31:42 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 21:31:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 21:31:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 21:31:49 GMT
EXPOSE 80
# Thu, 17 Mar 2022 21:31:55 GMT
EXPOSE 443
# Thu, 17 Mar 2022 21:31:58 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 21:32:01 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 21:32:03 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8b7e8363a93630a772b70e3cf72231f43c62addae0ee8e507c61d43e3781c4e7`  
		Last Modified: Thu, 17 Mar 2022 18:20:01 GMT  
		Size: 2.8 MB (2817281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e91dcc90eb989323abf507cb545731e08fdb7ae99452318650960f3b2bc29b8`  
		Last Modified: Thu, 17 Mar 2022 21:34:38 GMT  
		Size: 293.7 KB (293720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8763c1a56f6f74d41630bbb545d52602505e99c0e311f1ccfc50c001aa5c705c`  
		Last Modified: Thu, 17 Mar 2022 21:34:37 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e19db97ec3aacb5588ff43135ffccf7eef8281b28c0f3e95f8fa4a4c6e9f554`  
		Last Modified: Thu, 17 Mar 2022 21:34:40 GMT  
		Size: 10.3 MB (10302291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5f036cbadaf9e63bb1584d58115f79a3f4f9fdbce665e25642178129efa74b`  
		Last Modified: Thu, 17 Mar 2022 21:34:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:f710373b7c95e8c39a1e57b06884bac2548574d182889812998295c8b120c1ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14226716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced9b4438f1c256b9508d7d3dbf5048aed06c31b8a05cfbda638e5292d0dee83`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 17 Mar 2022 14:35:54 GMT
ADD file:cd4f7409c75ce2e40b46bbdeca277e2c4500aab51e1a7b6fa518c60e371f0a33 in / 
# Thu, 17 Mar 2022 14:35:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:00:36 GMT
RUN apk add --no-cache ca-certificates mailcap
# Thu, 17 Mar 2022 21:00:37 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"
# Thu, 17 Mar 2022 21:00:37 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 17 Mar 2022 21:00:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='ecdcf8ecf6ba92032b27bc935e3ca18b192b25ff54ecfc26bc685ac71c6fe66a6d387cfd085d786533e20f3df3db86e18709a9556d86f1745e9358cc0984973e' ;; 		armhf)   binArch='armv6'; checksum='7d14b1a14a632fff0d82c6e8621c729319befa36b9be9ed2d0309170818e484b8280df4c78538460697afdec59f9781365cc89ac9183310bf15370d56d37ec28' ;; 		armv7)   binArch='armv7'; checksum='c5bc52232ce5cd8f4d91e03996cce9404568804fe6f0e97e79a2d595cadc21918b45fc9c7bc5b4da50a8e02f865391de39ececdeda30dfc592d8f3a5bda6e289' ;; 		aarch64) binArch='arm64'; checksum='c521f56e6332bb51fb5b9df9c6b790d3a1dc64731ac71bca8d798681b40d912ca54b70f64438efd7e7c926a7a3f7f4daf674080b5be9bfb6bb648238aaba09db' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='22b20f463c0b5963165fa26c29d3cd30518b85ab3ed1a2f3104c708abc0690b18bacb0ba3f0468ad58bee41472f01d2f9a37fa67a23b422b0070f76c38f3c667' ;; 		s390x)   binArch='s390x'; checksum='949f31cd4a9117c5ac23f195f5d50968ac3cd0cfa6ac3d7040c662a4a39679642f36cb42d9185f502e9887b147628e2c5dc402a06d01f00552a5ba9dfe774f09' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	chmod +x /usr/bin/caddy; 	caddy version
# Thu, 17 Mar 2022 21:00:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 21:00:40 GMT
ENV XDG_CONFIG_HOME=/config
# Thu, 17 Mar 2022 21:00:40 GMT
ENV XDG_DATA_HOME=/data
# Thu, 17 Mar 2022 21:00:40 GMT
VOLUME [/config]
# Thu, 17 Mar 2022 21:00:41 GMT
VOLUME [/data]
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 17 Mar 2022 21:00:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 17 Mar 2022 21:00:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 17 Mar 2022 21:00:42 GMT
EXPOSE 80
# Thu, 17 Mar 2022 21:00:42 GMT
EXPOSE 443
# Thu, 17 Mar 2022 21:00:42 GMT
EXPOSE 2019
# Thu, 17 Mar 2022 21:00:42 GMT
WORKDIR /srv
# Thu, 17 Mar 2022 21:00:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:1a9a9eea18bd912112f7ed42a3730393bafbb84387ab6790fe9358d09100f3a3`  
		Last Modified: Thu, 17 Mar 2022 14:36:47 GMT  
		Size: 2.6 MB (2605208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c5df2f20a519a7f78f07f63378f86b2481339dccb5001000518f146e1ef5c0`  
		Last Modified: Thu, 17 Mar 2022 21:01:48 GMT  
		Size: 291.8 KB (291797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6179022673cadc5a23974fa435eaa88fbe3c46ae7f0e61e3a80fa34f7cb6c846`  
		Last Modified: Thu, 17 Mar 2022 21:01:47 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a36f8de1aad1bf91018c94013e0cf58d27a1e6c141c8c11cb4beae1b0aaa78`  
		Last Modified: Thu, 17 Mar 2022 21:01:49 GMT  
		Size: 11.3 MB (11323729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f17a5362f8b342e5c3ac44e83b09ad5a9c93dabbea07012c1a32399962536e`  
		Last Modified: Thu, 17 Mar 2022 21:01:48 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
