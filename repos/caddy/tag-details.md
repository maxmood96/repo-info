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
-	[`caddy:2.7`](#caddy27)
-	[`caddy:2.7-alpine`](#caddy27-alpine)
-	[`caddy:2.7-builder`](#caddy27-builder)
-	[`caddy:2.7-builder-alpine`](#caddy27-builder-alpine)
-	[`caddy:2.7-builder-windowsservercore-1809`](#caddy27-builder-windowsservercore-1809)
-	[`caddy:2.7-builder-windowsservercore-ltsc2022`](#caddy27-builder-windowsservercore-ltsc2022)
-	[`caddy:2.7-windowsservercore`](#caddy27-windowsservercore)
-	[`caddy:2.7-windowsservercore-1809`](#caddy27-windowsservercore-1809)
-	[`caddy:2.7-windowsservercore-ltsc2022`](#caddy27-windowsservercore-ltsc2022)
-	[`caddy:2.7.6`](#caddy276)
-	[`caddy:2.7.6-alpine`](#caddy276-alpine)
-	[`caddy:2.7.6-builder`](#caddy276-builder)
-	[`caddy:2.7.6-builder-alpine`](#caddy276-builder-alpine)
-	[`caddy:2.7.6-builder-windowsservercore-1809`](#caddy276-builder-windowsservercore-1809)
-	[`caddy:2.7.6-builder-windowsservercore-ltsc2022`](#caddy276-builder-windowsservercore-ltsc2022)
-	[`caddy:2.7.6-windowsservercore`](#caddy276-windowsservercore)
-	[`caddy:2.7.6-windowsservercore-1809`](#caddy276-windowsservercore-1809)
-	[`caddy:2.7.6-windowsservercore-ltsc2022`](#caddy276-windowsservercore-ltsc2022)
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
$ docker pull caddy@sha256:e523a9bc9e19fb96a082b4d83ebae2ce6267f56f2b7b4ac462135ebc51f68e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5122; amd64
	-	windows version 10.0.20348.2113; amd64

### `caddy:2` - linux; amd64

```console
$ docker pull caddy@sha256:7b8b4b0a4784433bd53271ff8f27d0940f96b1e633bb69b27d2c9ac5a293536a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18467236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657b947906e764d7ff65a638b958cb7f84b3754e49ede071620658385e743168`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:32:06 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:39:38 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:39:38 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:39:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:39:41 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:39:41 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:39:41 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:39:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:39:42 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:39:42 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:39:42 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:39:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08886dfc0722c4ed2cb6a70c285a33fe35aec069435868488356dde320b4d21c`  
		Last Modified: Fri, 01 Dec 2023 06:32:30 GMT  
		Size: 350.8 KB (350845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd2155878b9ec9d659128d039d90b8a50369fe85c88f64a597b6a9cd9441c1b`  
		Last Modified: Fri, 08 Dec 2023 20:40:01 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7343593237d1bd5fb218804e360a7a8c4d94d7af8da4eb1a72fbaf48fab9ce2`  
		Last Modified: Fri, 08 Dec 2023 20:40:03 GMT  
		Size: 14.7 MB (14706441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:fe42da7df688686dab79fb02be7f13aae32c9a9f84eec3b28b634cc48d5a7346
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17423030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f95b690a9e892f56dbf3fd455d714c2d22ebd35967fdc770fb704c870eeffc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:39:01 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:07:47 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:07:47 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:07:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:07:50 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:07:50 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:07:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:07:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:07:51 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:07:51 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc24e4ccf558b6e992efaaa7a735322be11fe99ce19e722eee6ae70bb76515d`  
		Last Modified: Fri, 01 Dec 2023 00:39:21 GMT  
		Size: 347.6 KB (347632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775b4c8558ad1bf8d7568fc741be39ee2a28ecdd33f84ed7597b6192873a81a`  
		Last Modified: Fri, 08 Dec 2023 20:08:10 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbf57a0db316ab6b42386b0221d652cc4f9d9d597206ce1d4e9bfd5ba0f7777`  
		Last Modified: Fri, 08 Dec 2023 20:08:12 GMT  
		Size: 13.9 MB (13920999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:cf486c3cc2b7d7cc0bdfc8db52605e6a533c0528e717b2ccd6e9779713d72229
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17146731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68a807660343335d38b999c8c1b687f5ec5c882c6f5180e13281152b030f103`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:19:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:16:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:16:22 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:16:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:16:25 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:16:26 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:16:27 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:16:27 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:16:28 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:16:28 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:16:28 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:16:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803b34e1f84b29ca968d2fbf85c278608566c34dfd1742e088c6483685957029`  
		Last Modified: Fri, 01 Dec 2023 03:19:48 GMT  
		Size: 344.5 KB (344464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de504bcc2429a4454910b605f8bb2f6eec4cad953044e48d02a7d51542b7266f`  
		Last Modified: Fri, 08 Dec 2023 20:16:53 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73099274a85e30e93cb0e71106c443fd9a5b923ef43adabf808db6a58db9ad8b`  
		Last Modified: Fri, 08 Dec 2023 20:16:56 GMT  
		Size: 13.9 MB (13893732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:71069b6f75345cd8b5e4841d92dcaebb4fa2acf454074eeb2c571517ac3671cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae18940ab920c723e970d89fde606b552e5b39f5fa33535cb6c7be09b6cff763`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:11:08 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 19:55:15 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 19:55:16 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 19:55:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 19:55:17 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 19:55:17 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 19:55:17 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 80
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 443
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 19:55:18 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 19:55:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e383270d6915b6b427f49a75d657d5a0403fcd47a5f89cd30e85143ca54c22`  
		Last Modified: Fri, 01 Dec 2023 03:11:28 GMT  
		Size: 360.7 KB (360655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f87e6bdbafc6710a3ed7bfbb4bb134e8d93bea992ab895c653cac0779389396`  
		Last Modified: Fri, 08 Dec 2023 19:55:35 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874486d3ac5891d4df17819e02e1cdd3775748effa24bc53645cd2db841a0837`  
		Last Modified: Fri, 08 Dec 2023 19:55:36 GMT  
		Size: 13.6 MB (13568967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; ppc64le

```console
$ docker pull caddy@sha256:9991e527a64c1d20422e24e141a57efec5365c7bcd68662808b0ea23da815b3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17051913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274840ad1c2fe6344d298e9d6242bde6e602b3444a071cfe45d3db4360d193b4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:42:19 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:22:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:22:14 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:22:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:22:19 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:22:19 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:22:19 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:22:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:22:20 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:22:22 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:22:22 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:22:23 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:22:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:22:24 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:22:24 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:22:25 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:22:25 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:22:26 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:22:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce4bc2907f69809c3086f118895d7e5c8683349557239c0ce79dfbda0ce3768`  
		Last Modified: Fri, 01 Dec 2023 05:44:17 GMT  
		Size: 362.2 KB (362185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3c2787bdbaa50fce90e65038b2dbc9850d2fff68d5e731bcdb83c71ede912b`  
		Last Modified: Fri, 08 Dec 2023 20:22:53 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ce50c6341ede9fe5f61cc3a75eb534b7dd1172b7e88c015862cb9351c91ca1`  
		Last Modified: Fri, 08 Dec 2023 20:22:55 GMT  
		Size: 13.3 MB (13333877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; s390x

```console
$ docker pull caddy@sha256:f8db25c8783258ee73a7ab061dbcb53f5229be2510ab4c72cbb6fe5292fdd1a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17818230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4782f6a3e2f343e87b335a56846d9ae67a4a5aded358a8501a4fb5a076e92cef`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:22:31 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 19:57:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 19:57:07 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 19:57:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 19:57:11 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 19:57:11 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 19:57:13 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 19:57:13 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 19:57:13 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 19:57:13 GMT
EXPOSE 80
# Fri, 08 Dec 2023 19:57:13 GMT
EXPOSE 443
# Fri, 08 Dec 2023 19:57:14 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 19:57:14 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 19:57:14 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 19:57:14 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20bbe0abb0a3f63718aa78742832077ad86b8ae86d70ce3ebcece342ec022c6`  
		Last Modified: Fri, 01 Dec 2023 08:23:07 GMT  
		Size: 354.9 KB (354948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa042ad4816c33e4f907bbf008abef2397efe2b3fc378430b2b925663a088370`  
		Last Modified: Fri, 08 Dec 2023 19:57:43 GMT  
		Size: 7.5 KB (7526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ceec9a3d819911fec4d039d31e2e3e38214fa45cb8384e8f047b5588724355`  
		Last Modified: Fri, 08 Dec 2023 19:57:45 GMT  
		Size: 14.2 MB (14238302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.17763.5122; amd64

```console
$ docker pull caddy@sha256:3d281f8c1d34b38abb3b5ca4ff98d70312daad9b0654a470374d0447a69a3ccf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073448315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e423604e6f05b59d8afa51e2d09a8fc11e1ac3353a126e3ce73b1c2bc65872b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:16:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:16:25 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:17:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:17:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:17:34 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:17:35 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:17:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:17:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:17:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:17:41 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:17:43 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:18:34 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:18:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09e9b6b38c0082853f1d6caa4d3536344a04da2aa5b674837aba8781b265e0d`  
		Last Modified: Fri, 08 Dec 2023 20:22:45 GMT  
		Size: 462.7 KB (462693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb778801cf9547a5b9021d3090bd8e4fc05f09e3aed56b6950dcbd044211d3f`  
		Last Modified: Fri, 08 Dec 2023 20:22:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ec815279848293cd980ed43a496bf4d3e8f8035f8d46dd1a3278e02c4558a8`  
		Last Modified: Fri, 08 Dec 2023 20:22:46 GMT  
		Size: 15.3 MB (15274633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9671feff108f8e0d8be270b64952394b3eaf7d16a7e9163cffc500ad3a42bd17`  
		Last Modified: Fri, 08 Dec 2023 20:22:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44f97706c45d8ebb4578d93d6c1cb5ecc4625f2f78fa40f25f9e72af014449a`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7b5732d0f0e4f61cac2e09f77054657b1bfc21c56b5b4b842e96ee7de3d45d`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348bbb9a26a300473cbb347ce3e405736e7a71ef7d2e67068452760fe4a1a67e`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4dc80dd8b7091a5cb553a95c06fa14380bf94a6f80467e3d7a36cb649fce8c`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6e2ab9cd2c6c903f643bcab22655dc93ec72fcc2f748a47375e2209580eed8`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a498a93a315d79030214cb59d847ede547dfc1159616120a3b48f2b1585bccfc`  
		Last Modified: Fri, 08 Dec 2023 20:22:40 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a7d0f8e26a8dd06b83bb38bfecf51f24ec1456947f459528e71b2544d13f5`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0da3c95480c1f76c862487e0683bed75c660c5cce3e3864677b8c956228e64`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1712e0793bc7067adabbb602cf9eaf0e6ab60f33be0b2b10282325884270ab07`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26aa77bbc553e8bf9318552da7ffe35258b387e04151dd211a006f50cb57a6`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e384f6873d9619640183b8c67671c94c80eb3725ac52c312de84b314b2cd4c53`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7ecef2ca51e4738a30164e40d773f9bfcc9a55bda13a00745349db1618fbf0`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29866626f3b37691b2e593b7ad8a6d3f6e916d9ca428c22e1b3834e568c605c9`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dff7ab50f452876c91da33fe48a0e1409de6cbb0ffca4e1aefa68caa5722d01`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 256.7 KB (256705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55865895b10a6247b60406c70eaa3584e7904512f0092bd7d9013bd9fe64c740`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.20348.2113; amd64

```console
$ docker pull caddy@sha256:cca2801fca8e41625ec6c3c42ee17cc76b64320f93ec2c37999b29b5f9ff0747
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1902845713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ad0d44150328d8253edf3d339d33f508e3a25395c8fd773d2d2fe5966eb244`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:19:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:19:10 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:19:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:19:34 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:19:35 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:19:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:19:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:19:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:19:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:19:43 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:19:44 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:19:58 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:19:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9e496904b6bbc7ce10b08f4c5c00b922d19bb8ebfca4735ba504c9ca77dd2b`  
		Last Modified: Fri, 08 Dec 2023 20:23:12 GMT  
		Size: 474.4 KB (474429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d370d88e3c2ee411f6f86dd892eba2c381cf5706823fcf82fec94a47d7d3bb4`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1861a873425170bdbe2b563cd2b9584401a7be0e3d9a6ceac998eef4eab482ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:13 GMT  
		Size: 15.3 MB (15274241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e17c8887831a9d0a255eb44daaaedffc1bb98b51fc0177786dd130c85034006`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2595203a1e7cbe5c30c3a77633ff7b832c6f07580e688e7c2bc89b5442e72ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b5a75922e76c5c96d069952df83b51d1243d2d6955db5b45dd7b63aea2b3a1`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bbe845ab80dc71320eea94c3d56888074ea930dc6fbe934c60e6c801e9cee3`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74052a6ffee1242926db0907e5406b7e5d81e181d3c9c266d381aaf221bf0252`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbd2ebe3b760156655b6475d7ff52b549e20b5115cf815016c902f834bf3f14`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5945b936f7903435999bc26916fd896f5c645c5b70834243317e66b14d7c2d97`  
		Last Modified: Fri, 08 Dec 2023 20:23:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4345b37fb7af089771ba8cf5542de3045ebb0f1d247ea038535504b320c4ac2c`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12593e8f188e5024af21891d9f3141bc5b85d9e2e9e2b61d7c2634f9f491b9a4`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3632692d5118ec05512cfb67c4aa09a8dfdfe1e40467dfc5ee8e5d2e9a349b2a`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e694808297bceaf6299316f20be2a78e4d2eef8a2ca455dd79ce544cf0a00e66`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258e53ea4c6d9b42de13f722ade5338a5393993985f05ca5b438982dde948654`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20692d7b4da06a40fca6c59bffc5e13dc0a0ffc429f70ed8701dc1d5d8c087fd`  
		Last Modified: Fri, 08 Dec 2023 20:23:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f686dbb1484378b8f73bbbfac32eb04d8f9a6b2b3f4db7d17c1f997941475a7f`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84003630e1340399082b07e0df6cb438545136bc3f0c134d52e8fe9d878e7239`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 292.2 KB (292197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9991bbf8fb125121b7478726325dcb657bfbeb24af279019b7b2f7ac0c404f7`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:eabac2898cf9fc7dc94d3fb03ac84c9c923aa6cc6f04874937d2f525e0d2f006
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
$ docker pull caddy@sha256:7b8b4b0a4784433bd53271ff8f27d0940f96b1e633bb69b27d2c9ac5a293536a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18467236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657b947906e764d7ff65a638b958cb7f84b3754e49ede071620658385e743168`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:32:06 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:39:38 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:39:38 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:39:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:39:41 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:39:41 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:39:41 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:39:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:39:42 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:39:42 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:39:42 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:39:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08886dfc0722c4ed2cb6a70c285a33fe35aec069435868488356dde320b4d21c`  
		Last Modified: Fri, 01 Dec 2023 06:32:30 GMT  
		Size: 350.8 KB (350845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd2155878b9ec9d659128d039d90b8a50369fe85c88f64a597b6a9cd9441c1b`  
		Last Modified: Fri, 08 Dec 2023 20:40:01 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7343593237d1bd5fb218804e360a7a8c4d94d7af8da4eb1a72fbaf48fab9ce2`  
		Last Modified: Fri, 08 Dec 2023 20:40:03 GMT  
		Size: 14.7 MB (14706441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:fe42da7df688686dab79fb02be7f13aae32c9a9f84eec3b28b634cc48d5a7346
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17423030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f95b690a9e892f56dbf3fd455d714c2d22ebd35967fdc770fb704c870eeffc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:39:01 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:07:47 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:07:47 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:07:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:07:50 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:07:50 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:07:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:07:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:07:51 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:07:51 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc24e4ccf558b6e992efaaa7a735322be11fe99ce19e722eee6ae70bb76515d`  
		Last Modified: Fri, 01 Dec 2023 00:39:21 GMT  
		Size: 347.6 KB (347632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775b4c8558ad1bf8d7568fc741be39ee2a28ecdd33f84ed7597b6192873a81a`  
		Last Modified: Fri, 08 Dec 2023 20:08:10 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbf57a0db316ab6b42386b0221d652cc4f9d9d597206ce1d4e9bfd5ba0f7777`  
		Last Modified: Fri, 08 Dec 2023 20:08:12 GMT  
		Size: 13.9 MB (13920999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:cf486c3cc2b7d7cc0bdfc8db52605e6a533c0528e717b2ccd6e9779713d72229
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17146731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68a807660343335d38b999c8c1b687f5ec5c882c6f5180e13281152b030f103`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:19:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:16:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:16:22 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:16:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:16:25 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:16:26 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:16:27 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:16:27 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:16:28 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:16:28 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:16:28 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:16:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803b34e1f84b29ca968d2fbf85c278608566c34dfd1742e088c6483685957029`  
		Last Modified: Fri, 01 Dec 2023 03:19:48 GMT  
		Size: 344.5 KB (344464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de504bcc2429a4454910b605f8bb2f6eec4cad953044e48d02a7d51542b7266f`  
		Last Modified: Fri, 08 Dec 2023 20:16:53 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73099274a85e30e93cb0e71106c443fd9a5b923ef43adabf808db6a58db9ad8b`  
		Last Modified: Fri, 08 Dec 2023 20:16:56 GMT  
		Size: 13.9 MB (13893732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:71069b6f75345cd8b5e4841d92dcaebb4fa2acf454074eeb2c571517ac3671cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae18940ab920c723e970d89fde606b552e5b39f5fa33535cb6c7be09b6cff763`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:11:08 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 19:55:15 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 19:55:16 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 19:55:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 19:55:17 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 19:55:17 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 19:55:17 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 80
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 443
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 19:55:18 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 19:55:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e383270d6915b6b427f49a75d657d5a0403fcd47a5f89cd30e85143ca54c22`  
		Last Modified: Fri, 01 Dec 2023 03:11:28 GMT  
		Size: 360.7 KB (360655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f87e6bdbafc6710a3ed7bfbb4bb134e8d93bea992ab895c653cac0779389396`  
		Last Modified: Fri, 08 Dec 2023 19:55:35 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874486d3ac5891d4df17819e02e1cdd3775748effa24bc53645cd2db841a0837`  
		Last Modified: Fri, 08 Dec 2023 19:55:36 GMT  
		Size: 13.6 MB (13568967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:9991e527a64c1d20422e24e141a57efec5365c7bcd68662808b0ea23da815b3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17051913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274840ad1c2fe6344d298e9d6242bde6e602b3444a071cfe45d3db4360d193b4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:42:19 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:22:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:22:14 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:22:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:22:19 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:22:19 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:22:19 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:22:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:22:20 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:22:22 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:22:22 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:22:23 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:22:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:22:24 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:22:24 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:22:25 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:22:25 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:22:26 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:22:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce4bc2907f69809c3086f118895d7e5c8683349557239c0ce79dfbda0ce3768`  
		Last Modified: Fri, 01 Dec 2023 05:44:17 GMT  
		Size: 362.2 KB (362185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3c2787bdbaa50fce90e65038b2dbc9850d2fff68d5e731bcdb83c71ede912b`  
		Last Modified: Fri, 08 Dec 2023 20:22:53 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ce50c6341ede9fe5f61cc3a75eb534b7dd1172b7e88c015862cb9351c91ca1`  
		Last Modified: Fri, 08 Dec 2023 20:22:55 GMT  
		Size: 13.3 MB (13333877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:f8db25c8783258ee73a7ab061dbcb53f5229be2510ab4c72cbb6fe5292fdd1a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17818230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4782f6a3e2f343e87b335a56846d9ae67a4a5aded358a8501a4fb5a076e92cef`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:22:31 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 19:57:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 19:57:07 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 19:57:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 19:57:11 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 19:57:11 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 19:57:13 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 19:57:13 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 19:57:13 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 19:57:13 GMT
EXPOSE 80
# Fri, 08 Dec 2023 19:57:13 GMT
EXPOSE 443
# Fri, 08 Dec 2023 19:57:14 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 19:57:14 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 19:57:14 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 19:57:14 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20bbe0abb0a3f63718aa78742832077ad86b8ae86d70ce3ebcece342ec022c6`  
		Last Modified: Fri, 01 Dec 2023 08:23:07 GMT  
		Size: 354.9 KB (354948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa042ad4816c33e4f907bbf008abef2397efe2b3fc378430b2b925663a088370`  
		Last Modified: Fri, 08 Dec 2023 19:57:43 GMT  
		Size: 7.5 KB (7526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ceec9a3d819911fec4d039d31e2e3e38214fa45cb8384e8f047b5588724355`  
		Last Modified: Fri, 08 Dec 2023 19:57:45 GMT  
		Size: 14.2 MB (14238302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:1bad661ef08b648af7c9c79e708965d3a69434285f24de76111124fdf5d339d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5122; amd64
	-	windows version 10.0.20348.2113; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:64cc92d77653c256c9cde397fb221c57907a57b0fe04f4e83ab2f7123f7f9147
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76963251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccce7adcc2b72b984adc9e5dd37663d1e6e512e39657c41bed43c55b38f9bad9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:46:23 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 03:46:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:25:52 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:26:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:26:02 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:26:02 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:26:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:26:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:26:03 GMT
WORKDIR /go
# Tue, 05 Dec 2023 20:48:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 20:48:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:39:46 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:39:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:39:46 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 20:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 20:39:47 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 20:39:47 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5501dced60f86be38cc73d3c038f7db4afeee65726f7e422aacf09244539ebf1`  
		Last Modified: Fri, 01 Dec 2023 03:50:39 GMT  
		Size: 284.7 KB (284697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63d189496f5f03c835c9c85df2db6920546d36a1701f6b5ad15f800c671605d`  
		Last Modified: Tue, 05 Dec 2023 20:31:27 GMT  
		Size: 67.0 MB (67003308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aeb88dd0f3e06a57abc08c781b85c89d138194918c469aea9a1bed9753d2ed0`  
		Last Modified: Tue, 05 Dec 2023 20:31:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40ff2505fd8d96e76bddb63b05c2d42815db1dabe0093ec8f8f53be403b0d01`  
		Last Modified: Tue, 05 Dec 2023 20:49:17 GMT  
		Size: 5.0 MB (4970029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ba23d637be879f93c12d4e6d077eb636688fa34e5d637f1f9a2f0a28509f0d`  
		Last Modified: Fri, 08 Dec 2023 20:40:19 GMT  
		Size: 1.3 MB (1302232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57ad5b5be9e26b4f05c8402814544f231f87d6a736a05320421e0ce2e623f04`  
		Last Modified: Fri, 08 Dec 2023 20:40:19 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:cd2d4a5ddcdef2492b7b440240d2e3beffa1695c0a1273227efdbc97a0fddc86
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75411895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed519bbe9039d7d32e60f9e1c959613953c4508dc6dd1506a355f0e0fd39bbe7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:53:48 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 00:53:48 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:49:18 GMT
ENV GOLANG_VERSION=1.21.5
# Sat, 09 Dec 2023 01:49:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	elif [ "$arch" = 'armv7' ]; then 		[ -s /usr/local/go/go.env ]; 		before="$(go env GOARM)"; [ "$before" != '7' ]; 		{ 			echo; 			echo '# https://github.com/docker-library/golang/issues/494'; 			echo 'GOARM=7'; 		} >> /usr/local/go/go.env; 		after="$(go env GOARM)"; [ "$after" = '7' ]; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Sat, 09 Dec 2023 01:49:51 GMT
ENV GOTOOLCHAIN=local
# Sat, 09 Dec 2023 01:49:51 GMT
ENV GOPATH=/go
# Sat, 09 Dec 2023 01:49:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 01:49:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Sat, 09 Dec 2023 01:49:52 GMT
WORKDIR /go
# Sat, 09 Dec 2023 02:08:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 09 Dec 2023 02:08:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 09 Dec 2023 02:08:59 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 09 Dec 2023 02:08:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 09 Dec 2023 02:08:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 09 Dec 2023 02:09:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 09 Dec 2023 02:09:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 09 Dec 2023 02:09:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e7ba0492eb25e7f21078441d7cdc65088836bc1984bc4a14cd3e9cd75cbf32`  
		Last Modified: Fri, 01 Dec 2023 01:00:23 GMT  
		Size: 284.9 KB (284884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbf3e566edb99ecb0ecb757d0f571633d7d822bf31896dd76a40ff9d89e98c0`  
		Last Modified: Sat, 09 Dec 2023 01:53:04 GMT  
		Size: 65.8 MB (65764277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e170d213450f3f3c66f85329ded2a75a6b38e5b51cfe01f2ad9d2cc2aab61079`  
		Last Modified: Sat, 09 Dec 2023 01:52:51 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612473e16b229d3c58615a469f9ca073ec9dc483d79cd7bb87479eea58ee5454`  
		Last Modified: Sat, 09 Dec 2023 02:09:20 GMT  
		Size: 5.0 MB (4966653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ed572067dfce272b021aee6f0cd14272e2a1157f0cf11ad00004a5c9354bc0`  
		Last Modified: Sat, 09 Dec 2023 02:09:19 GMT  
		Size: 1.2 MB (1248652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7608cc7cd78c6c2f18a53621dbd0b1746b9274ce1b35a8279b261816e41718ef`  
		Last Modified: Sat, 09 Dec 2023 02:09:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:7b8943fed6d62476c9dea44a16caea83fb6d540be101271d0974e0f2ed5a1567
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74707178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e459d7afebbd1af456db2bc6e8849445ca45f2586a9bbd0337ba314f570a177`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:44:57 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 08:44:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:58:01 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:58:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:58:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:58:16 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:58:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:58:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:58:17 GMT
WORKDIR /go
# Tue, 05 Dec 2023 21:22:31 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 21:22:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:16:31 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:16:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:16:32 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 20:16:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 20:16:34 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 20:16:34 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a824ff289f1a3c765a444079137b8b7f1cee80348faa53e1ba4c960b73ed2a`  
		Last Modified: Fri, 01 Dec 2023 08:49:42 GMT  
		Size: 284.1 KB (284079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4989177b4ed66b7e9f9e8c4bfce82720b582e24b735d6628effa75d81c5718fc`  
		Last Modified: Tue, 05 Dec 2023 21:04:43 GMT  
		Size: 65.8 MB (65764197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f9b58eae167c54d3faa3eeffd480cdae7e8b4841eb816a86cfdd01f8ae29ef`  
		Last Modified: Tue, 05 Dec 2023 21:04:29 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4cd1a3aab8fc02791b1e19f81b7de1bd691c10a7c942acc7e733221bf12888`  
		Last Modified: Tue, 05 Dec 2023 21:22:47 GMT  
		Size: 4.5 MB (4511237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c6a5bcaed596afac229d37cd822ea4770b06d4d3580d14a71d26e32136f1aa`  
		Last Modified: Fri, 08 Dec 2023 20:17:09 GMT  
		Size: 1.2 MB (1246093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c59154934645e7c4d44eda6d3d5ea9d4b32e23fbf7ccb7009cc54413ae815d`  
		Last Modified: Fri, 08 Dec 2023 20:17:09 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:3fce35ec600b6e48bb63c1b2d390b6d515a6f0e7355b582fcb347092222bdc37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73981648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3475cc52d42bfd049fb20d388ecf6c8482841b98a265b9fc09b60bc815011df9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:43:53 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 03:18:30 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:16:18 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:16:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:16:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:16:28 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:16:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:16:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:16:28 GMT
WORKDIR /go
# Tue, 05 Dec 2023 20:38:16 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 20:38:16 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 19:55:21 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 19:55:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 19:55:21 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 19:55:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 19:55:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 19:55:22 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a63ed24dc22a348b35d99b5ec9dc67ff66563b539875e5c8ab2d870b3991ac`  
		Last Modified: Fri, 01 Dec 2023 02:44:03 GMT  
		Size: 286.3 KB (286307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f00641dffc5c2a149049ee9046bb24cfc7de534b7495a0f27784a4fff0fadc`  
		Last Modified: Tue, 05 Dec 2023 20:21:00 GMT  
		Size: 64.1 MB (64094844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452682ba77e89fc55be3a168358f5f43bccad93ecdd3d53b4dec7fff6915128b`  
		Last Modified: Tue, 05 Dec 2023 20:20:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3fe1e12507f8c4a2731393eebfc5ab973aa344b0daceec525560b812b26f60`  
		Last Modified: Tue, 05 Dec 2023 20:38:33 GMT  
		Size: 5.1 MB (5068450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1568fb18f5eae3df776dd2fee8d447615d0f62601f82ebdb1bf2af5155bb83`  
		Last Modified: Fri, 08 Dec 2023 19:55:49 GMT  
		Size: 1.2 MB (1198450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15988851efd259492be8e7583025cb2b00f7477442c7be3e2d3dd97adbc39e76`  
		Last Modified: Fri, 08 Dec 2023 19:55:48 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:e21739ed4cecc54ebd496b12fa757f5901f3c0b45d211c0c5fa2ef551543c2d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74206507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed778e73218e8613cd2044f7eb703ec05bf43271d444ca5ffe77e053baa719c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:37:34 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 06:37:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:38:14 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:38:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:38:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:38:38 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:38:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:38:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:38:41 GMT
WORKDIR /go
# Tue, 05 Dec 2023 21:04:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 21:04:34 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:22:32 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:22:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:22:33 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 20:22:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 20:22:35 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 20:22:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692dbecd5e141c462ab06ef113ec964b525e7564d734890cc1d5b1dbf33ee34e`  
		Last Modified: Fri, 01 Dec 2023 06:43:30 GMT  
		Size: 286.7 KB (286661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc89a0f2d97ecfd4d20235e72227fc24aa79a64509fe9ea64702db658f2ad26d`  
		Last Modified: Tue, 05 Dec 2023 20:46:23 GMT  
		Size: 64.1 MB (64115804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d76f2c2e2bbb4190b1865ddafdc8cb88adee4c79d7d5ba23e69696e9610889`  
		Last Modified: Tue, 05 Dec 2023 20:46:11 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e0ec0f713ee657d6aa159fab65c05939480b5ca50a8e3dc4b1a9a6578160f7`  
		Last Modified: Tue, 05 Dec 2023 21:04:57 GMT  
		Size: 5.3 MB (5268970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbd7401349780157d6d930ec942f00b1d5404d31ae60bff5c7b41238cf8e3b1`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 1.2 MB (1186185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67206b5e4434d3211a98a71837832baed45e4fb0c03ff8dc204bc7762a8ab559`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:bf201fa7da491e4decf9c0a638b9fbcb4b459d5b13bcc9a2f4c0fb4c583c609b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76101050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e2b3cda7ff391c43b985fdbd1c3515e69b6fbe94f8ea6c9a09749c147e491c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:14:49 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 08:14:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:44:16 GMT
ENV GOLANG_VERSION=1.21.5
# Sat, 09 Dec 2023 01:50:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	elif [ "$arch" = 'armv7' ]; then 		[ -s /usr/local/go/go.env ]; 		before="$(go env GOARM)"; [ "$before" != '7' ]; 		{ 			echo; 			echo '# https://github.com/docker-library/golang/issues/494'; 			echo 'GOARM=7'; 		} >> /usr/local/go/go.env; 		after="$(go env GOARM)"; [ "$after" = '7' ]; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Sat, 09 Dec 2023 01:50:41 GMT
ENV GOTOOLCHAIN=local
# Sat, 09 Dec 2023 01:50:41 GMT
ENV GOPATH=/go
# Sat, 09 Dec 2023 01:50:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 01:50:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Sat, 09 Dec 2023 01:50:42 GMT
WORKDIR /go
# Sat, 09 Dec 2023 02:12:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 09 Dec 2023 02:12:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 09 Dec 2023 02:12:31 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 09 Dec 2023 02:12:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 09 Dec 2023 02:12:31 GMT
ENV XCADDY_SETCAP=1
# Sat, 09 Dec 2023 02:12:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 09 Dec 2023 02:12:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 09 Dec 2023 02:12:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab563e8d41683e124df048aa9b564b0e8e1021e85213666971a015df51d5e48`  
		Last Modified: Fri, 01 Dec 2023 08:20:46 GMT  
		Size: 285.1 KB (285090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c541c9463bd8d06e97aa1b14ce0792cf2caf6ef8ddc7b046b21032b3390bee`  
		Last Modified: Sat, 09 Dec 2023 01:54:50 GMT  
		Size: 66.2 MB (66218593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236faa4ca6aed551be037e8e0a2312e72dedf504cdffa8d2015882df02c5b87e`  
		Last Modified: Sat, 09 Dec 2023 01:54:39 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee294f5771410ee01c59c398d0270a28f5ae4caff9abfa5339f1c54b1dc1ab5a`  
		Last Modified: Sat, 09 Dec 2023 02:12:56 GMT  
		Size: 5.1 MB (5116966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cbd016bf9fbfd249882a217530ca94dcac095e46620a64badd9bbfa6ae9ebe`  
		Last Modified: Sat, 09 Dec 2023 02:12:55 GMT  
		Size: 1.3 MB (1262386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b36774ae94aa93a3beb6e355ee08897437b53c870bc56fdc3047ce591cfa2ac`  
		Last Modified: Sat, 09 Dec 2023 02:12:55 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.5122; amd64

```console
$ docker pull caddy@sha256:cdab1fd140455df0674bfedde2f4948b5289720efd10ff1301ce39bb60cd8daf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154297412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39391f7d87fac7b43f0ed0b59b1981b263a30d3397f5f5244adf81cb7627ba5a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 02:47:03 GMT
ENV GIT_VERSION=2.23.0
# Thu, 16 Nov 2023 02:47:04 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 16 Nov 2023 02:47:05 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 16 Nov 2023 02:47:06 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 16 Nov 2023 02:48:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 02:48:31 GMT
ENV GOPATH=C:\go
# Thu, 16 Nov 2023 02:49:41 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Dec 2023 20:18:04 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:21:11 GMT
RUN $url = 'https://dl.google.com/go/go1.21.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bbe603cde7c9dee658f45164b4d06de1eff6e6e6b800100824e7c00d56a9a92f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Dec 2023 20:21:13 GMT
WORKDIR C:\go
# Tue, 05 Dec 2023 20:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Dec 2023 20:59:30 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:20:06 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:20:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:21:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 08 Dec 2023 20:21:15 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e901367fac1450f509d3118ada9e004e3613844ebdf91861147a093483930a4`  
		Last Modified: Thu, 16 Nov 2023 03:11:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e08004205bd077d8f22b013c70dc2f10796c64fced1eb9927e0055daff2d05d`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebc5048afc68ef48e2f2136545e2cccf26bb29eb4926bf4259b370ad55b4e7a`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f50fe5c7ef21648f3eaa4304932877a116fcb910b8e9095c779a2fbe6d57f7e`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76fe0e37750041d4ede2a0ca3b5245cfe075c3eb2ee27d7ce72ee8c3d7b20cc`  
		Last Modified: Thu, 16 Nov 2023 03:12:00 GMT  
		Size: 25.5 MB (25537512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8097bb9b8778d15dbf89d899653bf1634ec17554e5d84ef1ccfcac8ebf86afe2`  
		Last Modified: Thu, 16 Nov 2023 03:11:53 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b542d31e914d67da86cc5701cdc282ab664dc1170507e3802e22ab3026436a90`  
		Last Modified: Thu, 16 Nov 2023 03:11:53 GMT  
		Size: 263.2 KB (263200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86acdf7d3955fb44136bac433a30ccbbb97863120f270af32659dd65446666c7`  
		Last Modified: Tue, 05 Dec 2023 20:39:22 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1abe126c354944b7db8aa724d8f757167f7c3b36d39f976ef3b1b0d1b1b65ab`  
		Last Modified: Tue, 05 Dec 2023 20:39:41 GMT  
		Size: 69.4 MB (69361283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6338af096e09067ad482a0f4a6df1d1eee5b5595a64ca5f367b94ce27903e284`  
		Last Modified: Tue, 05 Dec 2023 20:39:22 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0adc218b27ef5639384c060fb663de3bd74374279d3fd525aa281f63a754779`  
		Last Modified: Tue, 05 Dec 2023 21:02:06 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c21053b248805df7ad888734f5cd1df5a6b426111512d5a6b7530060e7f30b2`  
		Last Modified: Tue, 05 Dec 2023 21:02:03 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034eb8f336a0d8e998c3eef6834d07c072c0679ccd4fde02cc8787ed46c80b19`  
		Last Modified: Fri, 08 Dec 2023 20:23:31 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af9b0b53a037a76c1c2e0e3afbe4fad733bc634a5ca02d53055360d9b7e33b9`  
		Last Modified: Fri, 08 Dec 2023 20:23:31 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f653ab9a896e2a3cfaf147a9ebb6e2d23f453cc3f953ee19b27333ebbc66460b`  
		Last Modified: Fri, 08 Dec 2023 20:23:32 GMT  
		Size: 1.7 MB (1685700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed98b1069776f09873a216052d2bf114c714b8269e4235d0aee375a2b0b7962`  
		Last Modified: Fri, 08 Dec 2023 20:23:31 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.20348.2113; amd64

```console
$ docker pull caddy@sha256:b1d94a17104c4814aa7672316e4c713aefcdfa6ffd19043f4111784c09931cda
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1983623336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61ba19fe8fdfa90a532d1f355b356c651a2921264135f6417c72193a5f37396`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 02:43:34 GMT
ENV GIT_VERSION=2.23.0
# Thu, 16 Nov 2023 02:43:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 16 Nov 2023 02:43:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 16 Nov 2023 02:43:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 16 Nov 2023 02:44:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 02:44:11 GMT
ENV GOPATH=C:\go
# Thu, 16 Nov 2023 02:44:30 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Dec 2023 20:15:35 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:17:49 GMT
RUN $url = 'https://dl.google.com/go/go1.21.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bbe603cde7c9dee658f45164b4d06de1eff6e6e6b800100824e7c00d56a9a92f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Dec 2023 20:17:50 GMT
WORKDIR C:\go
# Tue, 05 Dec 2023 21:00:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Dec 2023 21:00:58 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:21:33 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:21:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:21:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 08 Dec 2023 20:21:57 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b1d4a557f047b695f94452d9707061981d7fae4239c674b332282b8291963c`  
		Last Modified: Thu, 16 Nov 2023 03:11:20 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45549c207f14d769cba7c36b66157ec213bbc32ce57d685d8e2c407cf3987bb`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c674717e06bf8cb25d5887393ef9568ee0ab6390966b9666808e836e9bd471d`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2227badcd9f5f2b70b3d2ffd1c18887498f413c07802bfb334e8dc7b2d2acc`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9f3b5e90a2e6028cf194e870b24a7158f875f18b81f4f9137a5db3ea1f79ac`  
		Last Modified: Thu, 16 Nov 2023 03:11:23 GMT  
		Size: 25.5 MB (25536225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7811a5416dcd19193a5b3ab9327607bf845f7ff77f95d3e20abdfb7435c32ae0`  
		Last Modified: Thu, 16 Nov 2023 03:11:16 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5931209e960a94616639ea72e4d3ad9dc9cb554790ce930152c73bdc1449c034`  
		Last Modified: Thu, 16 Nov 2023 03:11:16 GMT  
		Size: 266.6 KB (266600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a70f603a2fb4e76edd3165b62a179fb8f6410e265f5ae4a3732ee68e610034b`  
		Last Modified: Tue, 05 Dec 2023 20:38:48 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e37840dec3a6665ce48520be8b2c51b654359765bee5ab0780ee74746f0eb2`  
		Last Modified: Tue, 05 Dec 2023 20:39:08 GMT  
		Size: 69.3 MB (69342960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d16ae54757acda093616d24735d4c92d4676649bec49807fc35de90d15e15c`  
		Last Modified: Tue, 05 Dec 2023 20:38:48 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5744d01eddd2ef9d9673fdb0f0e48203fad1b01f2b14899a3ec6393c4548e75`  
		Last Modified: Tue, 05 Dec 2023 21:02:23 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35bb848667aa413b6ce6c309a4c2169635b0740dc335b9b39413a00627c01ab`  
		Last Modified: Tue, 05 Dec 2023 21:02:21 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54630e9807bbb8995ce52459e6e3c8d818351c481e0ce29280570e90d0138d33`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f15ec018ec91e33ee96d4f0e6b66d9edb40b185a13f91d16f12d0bf682ab08b`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79cc8b934303f209cd48271252cb46966445a1099aac277ae4caf120af718ab`  
		Last Modified: Fri, 08 Dec 2023 20:23:49 GMT  
		Size: 1.7 MB (1677815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224f75043e75fb7c85d3daec88a29069c6ff40b8feeaa26bac868d524758955`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:a6d9bf50074feba4597d504f2c617c7d3e772c19b67d0ca788dcf2dcb421bd08
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
$ docker pull caddy@sha256:64cc92d77653c256c9cde397fb221c57907a57b0fe04f4e83ab2f7123f7f9147
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76963251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccce7adcc2b72b984adc9e5dd37663d1e6e512e39657c41bed43c55b38f9bad9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:46:23 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 03:46:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:25:52 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:26:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:26:02 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:26:02 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:26:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:26:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:26:03 GMT
WORKDIR /go
# Tue, 05 Dec 2023 20:48:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 20:48:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:39:46 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:39:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:39:46 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 20:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 20:39:47 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 20:39:47 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5501dced60f86be38cc73d3c038f7db4afeee65726f7e422aacf09244539ebf1`  
		Last Modified: Fri, 01 Dec 2023 03:50:39 GMT  
		Size: 284.7 KB (284697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63d189496f5f03c835c9c85df2db6920546d36a1701f6b5ad15f800c671605d`  
		Last Modified: Tue, 05 Dec 2023 20:31:27 GMT  
		Size: 67.0 MB (67003308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aeb88dd0f3e06a57abc08c781b85c89d138194918c469aea9a1bed9753d2ed0`  
		Last Modified: Tue, 05 Dec 2023 20:31:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40ff2505fd8d96e76bddb63b05c2d42815db1dabe0093ec8f8f53be403b0d01`  
		Last Modified: Tue, 05 Dec 2023 20:49:17 GMT  
		Size: 5.0 MB (4970029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ba23d637be879f93c12d4e6d077eb636688fa34e5d637f1f9a2f0a28509f0d`  
		Last Modified: Fri, 08 Dec 2023 20:40:19 GMT  
		Size: 1.3 MB (1302232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57ad5b5be9e26b4f05c8402814544f231f87d6a736a05320421e0ce2e623f04`  
		Last Modified: Fri, 08 Dec 2023 20:40:19 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:cd2d4a5ddcdef2492b7b440240d2e3beffa1695c0a1273227efdbc97a0fddc86
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75411895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed519bbe9039d7d32e60f9e1c959613953c4508dc6dd1506a355f0e0fd39bbe7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:53:48 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 00:53:48 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:49:18 GMT
ENV GOLANG_VERSION=1.21.5
# Sat, 09 Dec 2023 01:49:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	elif [ "$arch" = 'armv7' ]; then 		[ -s /usr/local/go/go.env ]; 		before="$(go env GOARM)"; [ "$before" != '7' ]; 		{ 			echo; 			echo '# https://github.com/docker-library/golang/issues/494'; 			echo 'GOARM=7'; 		} >> /usr/local/go/go.env; 		after="$(go env GOARM)"; [ "$after" = '7' ]; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Sat, 09 Dec 2023 01:49:51 GMT
ENV GOTOOLCHAIN=local
# Sat, 09 Dec 2023 01:49:51 GMT
ENV GOPATH=/go
# Sat, 09 Dec 2023 01:49:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 01:49:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Sat, 09 Dec 2023 01:49:52 GMT
WORKDIR /go
# Sat, 09 Dec 2023 02:08:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 09 Dec 2023 02:08:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 09 Dec 2023 02:08:59 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 09 Dec 2023 02:08:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 09 Dec 2023 02:08:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 09 Dec 2023 02:09:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 09 Dec 2023 02:09:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 09 Dec 2023 02:09:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e7ba0492eb25e7f21078441d7cdc65088836bc1984bc4a14cd3e9cd75cbf32`  
		Last Modified: Fri, 01 Dec 2023 01:00:23 GMT  
		Size: 284.9 KB (284884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbf3e566edb99ecb0ecb757d0f571633d7d822bf31896dd76a40ff9d89e98c0`  
		Last Modified: Sat, 09 Dec 2023 01:53:04 GMT  
		Size: 65.8 MB (65764277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e170d213450f3f3c66f85329ded2a75a6b38e5b51cfe01f2ad9d2cc2aab61079`  
		Last Modified: Sat, 09 Dec 2023 01:52:51 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612473e16b229d3c58615a469f9ca073ec9dc483d79cd7bb87479eea58ee5454`  
		Last Modified: Sat, 09 Dec 2023 02:09:20 GMT  
		Size: 5.0 MB (4966653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ed572067dfce272b021aee6f0cd14272e2a1157f0cf11ad00004a5c9354bc0`  
		Last Modified: Sat, 09 Dec 2023 02:09:19 GMT  
		Size: 1.2 MB (1248652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7608cc7cd78c6c2f18a53621dbd0b1746b9274ce1b35a8279b261816e41718ef`  
		Last Modified: Sat, 09 Dec 2023 02:09:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:7b8943fed6d62476c9dea44a16caea83fb6d540be101271d0974e0f2ed5a1567
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74707178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e459d7afebbd1af456db2bc6e8849445ca45f2586a9bbd0337ba314f570a177`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:44:57 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 08:44:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:58:01 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:58:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:58:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:58:16 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:58:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:58:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:58:17 GMT
WORKDIR /go
# Tue, 05 Dec 2023 21:22:31 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 21:22:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:16:31 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:16:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:16:32 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 20:16:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 20:16:34 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 20:16:34 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a824ff289f1a3c765a444079137b8b7f1cee80348faa53e1ba4c960b73ed2a`  
		Last Modified: Fri, 01 Dec 2023 08:49:42 GMT  
		Size: 284.1 KB (284079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4989177b4ed66b7e9f9e8c4bfce82720b582e24b735d6628effa75d81c5718fc`  
		Last Modified: Tue, 05 Dec 2023 21:04:43 GMT  
		Size: 65.8 MB (65764197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f9b58eae167c54d3faa3eeffd480cdae7e8b4841eb816a86cfdd01f8ae29ef`  
		Last Modified: Tue, 05 Dec 2023 21:04:29 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4cd1a3aab8fc02791b1e19f81b7de1bd691c10a7c942acc7e733221bf12888`  
		Last Modified: Tue, 05 Dec 2023 21:22:47 GMT  
		Size: 4.5 MB (4511237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c6a5bcaed596afac229d37cd822ea4770b06d4d3580d14a71d26e32136f1aa`  
		Last Modified: Fri, 08 Dec 2023 20:17:09 GMT  
		Size: 1.2 MB (1246093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c59154934645e7c4d44eda6d3d5ea9d4b32e23fbf7ccb7009cc54413ae815d`  
		Last Modified: Fri, 08 Dec 2023 20:17:09 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:3fce35ec600b6e48bb63c1b2d390b6d515a6f0e7355b582fcb347092222bdc37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73981648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3475cc52d42bfd049fb20d388ecf6c8482841b98a265b9fc09b60bc815011df9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:43:53 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 03:18:30 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:16:18 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:16:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:16:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:16:28 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:16:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:16:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:16:28 GMT
WORKDIR /go
# Tue, 05 Dec 2023 20:38:16 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 20:38:16 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 19:55:21 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 19:55:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 19:55:21 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 19:55:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 19:55:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 19:55:22 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a63ed24dc22a348b35d99b5ec9dc67ff66563b539875e5c8ab2d870b3991ac`  
		Last Modified: Fri, 01 Dec 2023 02:44:03 GMT  
		Size: 286.3 KB (286307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f00641dffc5c2a149049ee9046bb24cfc7de534b7495a0f27784a4fff0fadc`  
		Last Modified: Tue, 05 Dec 2023 20:21:00 GMT  
		Size: 64.1 MB (64094844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452682ba77e89fc55be3a168358f5f43bccad93ecdd3d53b4dec7fff6915128b`  
		Last Modified: Tue, 05 Dec 2023 20:20:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3fe1e12507f8c4a2731393eebfc5ab973aa344b0daceec525560b812b26f60`  
		Last Modified: Tue, 05 Dec 2023 20:38:33 GMT  
		Size: 5.1 MB (5068450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1568fb18f5eae3df776dd2fee8d447615d0f62601f82ebdb1bf2af5155bb83`  
		Last Modified: Fri, 08 Dec 2023 19:55:49 GMT  
		Size: 1.2 MB (1198450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15988851efd259492be8e7583025cb2b00f7477442c7be3e2d3dd97adbc39e76`  
		Last Modified: Fri, 08 Dec 2023 19:55:48 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:e21739ed4cecc54ebd496b12fa757f5901f3c0b45d211c0c5fa2ef551543c2d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74206507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed778e73218e8613cd2044f7eb703ec05bf43271d444ca5ffe77e053baa719c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:37:34 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 06:37:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:38:14 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:38:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:38:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:38:38 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:38:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:38:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:38:41 GMT
WORKDIR /go
# Tue, 05 Dec 2023 21:04:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 21:04:34 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:22:32 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:22:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:22:33 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 20:22:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 20:22:35 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 20:22:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692dbecd5e141c462ab06ef113ec964b525e7564d734890cc1d5b1dbf33ee34e`  
		Last Modified: Fri, 01 Dec 2023 06:43:30 GMT  
		Size: 286.7 KB (286661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc89a0f2d97ecfd4d20235e72227fc24aa79a64509fe9ea64702db658f2ad26d`  
		Last Modified: Tue, 05 Dec 2023 20:46:23 GMT  
		Size: 64.1 MB (64115804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d76f2c2e2bbb4190b1865ddafdc8cb88adee4c79d7d5ba23e69696e9610889`  
		Last Modified: Tue, 05 Dec 2023 20:46:11 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e0ec0f713ee657d6aa159fab65c05939480b5ca50a8e3dc4b1a9a6578160f7`  
		Last Modified: Tue, 05 Dec 2023 21:04:57 GMT  
		Size: 5.3 MB (5268970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbd7401349780157d6d930ec942f00b1d5404d31ae60bff5c7b41238cf8e3b1`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 1.2 MB (1186185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67206b5e4434d3211a98a71837832baed45e4fb0c03ff8dc204bc7762a8ab559`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:bf201fa7da491e4decf9c0a638b9fbcb4b459d5b13bcc9a2f4c0fb4c583c609b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76101050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e2b3cda7ff391c43b985fdbd1c3515e69b6fbe94f8ea6c9a09749c147e491c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:14:49 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 08:14:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:44:16 GMT
ENV GOLANG_VERSION=1.21.5
# Sat, 09 Dec 2023 01:50:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	elif [ "$arch" = 'armv7' ]; then 		[ -s /usr/local/go/go.env ]; 		before="$(go env GOARM)"; [ "$before" != '7' ]; 		{ 			echo; 			echo '# https://github.com/docker-library/golang/issues/494'; 			echo 'GOARM=7'; 		} >> /usr/local/go/go.env; 		after="$(go env GOARM)"; [ "$after" = '7' ]; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Sat, 09 Dec 2023 01:50:41 GMT
ENV GOTOOLCHAIN=local
# Sat, 09 Dec 2023 01:50:41 GMT
ENV GOPATH=/go
# Sat, 09 Dec 2023 01:50:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 01:50:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Sat, 09 Dec 2023 01:50:42 GMT
WORKDIR /go
# Sat, 09 Dec 2023 02:12:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 09 Dec 2023 02:12:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 09 Dec 2023 02:12:31 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 09 Dec 2023 02:12:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 09 Dec 2023 02:12:31 GMT
ENV XCADDY_SETCAP=1
# Sat, 09 Dec 2023 02:12:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 09 Dec 2023 02:12:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 09 Dec 2023 02:12:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab563e8d41683e124df048aa9b564b0e8e1021e85213666971a015df51d5e48`  
		Last Modified: Fri, 01 Dec 2023 08:20:46 GMT  
		Size: 285.1 KB (285090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c541c9463bd8d06e97aa1b14ce0792cf2caf6ef8ddc7b046b21032b3390bee`  
		Last Modified: Sat, 09 Dec 2023 01:54:50 GMT  
		Size: 66.2 MB (66218593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236faa4ca6aed551be037e8e0a2312e72dedf504cdffa8d2015882df02c5b87e`  
		Last Modified: Sat, 09 Dec 2023 01:54:39 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee294f5771410ee01c59c398d0270a28f5ae4caff9abfa5339f1c54b1dc1ab5a`  
		Last Modified: Sat, 09 Dec 2023 02:12:56 GMT  
		Size: 5.1 MB (5116966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cbd016bf9fbfd249882a217530ca94dcac095e46620a64badd9bbfa6ae9ebe`  
		Last Modified: Sat, 09 Dec 2023 02:12:55 GMT  
		Size: 1.3 MB (1262386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b36774ae94aa93a3beb6e355ee08897437b53c870bc56fdc3047ce591cfa2ac`  
		Last Modified: Sat, 09 Dec 2023 02:12:55 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:8bf37ab9a085a9916fcfb4a921ebbfe2d29d2893fac56672655cc8ccd5fa3c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull caddy@sha256:cdab1fd140455df0674bfedde2f4948b5289720efd10ff1301ce39bb60cd8daf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154297412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39391f7d87fac7b43f0ed0b59b1981b263a30d3397f5f5244adf81cb7627ba5a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 02:47:03 GMT
ENV GIT_VERSION=2.23.0
# Thu, 16 Nov 2023 02:47:04 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 16 Nov 2023 02:47:05 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 16 Nov 2023 02:47:06 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 16 Nov 2023 02:48:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 02:48:31 GMT
ENV GOPATH=C:\go
# Thu, 16 Nov 2023 02:49:41 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Dec 2023 20:18:04 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:21:11 GMT
RUN $url = 'https://dl.google.com/go/go1.21.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bbe603cde7c9dee658f45164b4d06de1eff6e6e6b800100824e7c00d56a9a92f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Dec 2023 20:21:13 GMT
WORKDIR C:\go
# Tue, 05 Dec 2023 20:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Dec 2023 20:59:30 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:20:06 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:20:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:21:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 08 Dec 2023 20:21:15 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e901367fac1450f509d3118ada9e004e3613844ebdf91861147a093483930a4`  
		Last Modified: Thu, 16 Nov 2023 03:11:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e08004205bd077d8f22b013c70dc2f10796c64fced1eb9927e0055daff2d05d`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebc5048afc68ef48e2f2136545e2cccf26bb29eb4926bf4259b370ad55b4e7a`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f50fe5c7ef21648f3eaa4304932877a116fcb910b8e9095c779a2fbe6d57f7e`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76fe0e37750041d4ede2a0ca3b5245cfe075c3eb2ee27d7ce72ee8c3d7b20cc`  
		Last Modified: Thu, 16 Nov 2023 03:12:00 GMT  
		Size: 25.5 MB (25537512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8097bb9b8778d15dbf89d899653bf1634ec17554e5d84ef1ccfcac8ebf86afe2`  
		Last Modified: Thu, 16 Nov 2023 03:11:53 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b542d31e914d67da86cc5701cdc282ab664dc1170507e3802e22ab3026436a90`  
		Last Modified: Thu, 16 Nov 2023 03:11:53 GMT  
		Size: 263.2 KB (263200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86acdf7d3955fb44136bac433a30ccbbb97863120f270af32659dd65446666c7`  
		Last Modified: Tue, 05 Dec 2023 20:39:22 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1abe126c354944b7db8aa724d8f757167f7c3b36d39f976ef3b1b0d1b1b65ab`  
		Last Modified: Tue, 05 Dec 2023 20:39:41 GMT  
		Size: 69.4 MB (69361283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6338af096e09067ad482a0f4a6df1d1eee5b5595a64ca5f367b94ce27903e284`  
		Last Modified: Tue, 05 Dec 2023 20:39:22 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0adc218b27ef5639384c060fb663de3bd74374279d3fd525aa281f63a754779`  
		Last Modified: Tue, 05 Dec 2023 21:02:06 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c21053b248805df7ad888734f5cd1df5a6b426111512d5a6b7530060e7f30b2`  
		Last Modified: Tue, 05 Dec 2023 21:02:03 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034eb8f336a0d8e998c3eef6834d07c072c0679ccd4fde02cc8787ed46c80b19`  
		Last Modified: Fri, 08 Dec 2023 20:23:31 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af9b0b53a037a76c1c2e0e3afbe4fad733bc634a5ca02d53055360d9b7e33b9`  
		Last Modified: Fri, 08 Dec 2023 20:23:31 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f653ab9a896e2a3cfaf147a9ebb6e2d23f453cc3f953ee19b27333ebbc66460b`  
		Last Modified: Fri, 08 Dec 2023 20:23:32 GMT  
		Size: 1.7 MB (1685700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed98b1069776f09873a216052d2bf114c714b8269e4235d0aee375a2b0b7962`  
		Last Modified: Fri, 08 Dec 2023 20:23:31 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:b944570c2f667cfb312913d3478de80037fe9967f6fd20a1358e3f1b87467164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull caddy@sha256:b1d94a17104c4814aa7672316e4c713aefcdfa6ffd19043f4111784c09931cda
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1983623336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61ba19fe8fdfa90a532d1f355b356c651a2921264135f6417c72193a5f37396`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 02:43:34 GMT
ENV GIT_VERSION=2.23.0
# Thu, 16 Nov 2023 02:43:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 16 Nov 2023 02:43:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 16 Nov 2023 02:43:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 16 Nov 2023 02:44:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 02:44:11 GMT
ENV GOPATH=C:\go
# Thu, 16 Nov 2023 02:44:30 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Dec 2023 20:15:35 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:17:49 GMT
RUN $url = 'https://dl.google.com/go/go1.21.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bbe603cde7c9dee658f45164b4d06de1eff6e6e6b800100824e7c00d56a9a92f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Dec 2023 20:17:50 GMT
WORKDIR C:\go
# Tue, 05 Dec 2023 21:00:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Dec 2023 21:00:58 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:21:33 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:21:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:21:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 08 Dec 2023 20:21:57 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b1d4a557f047b695f94452d9707061981d7fae4239c674b332282b8291963c`  
		Last Modified: Thu, 16 Nov 2023 03:11:20 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45549c207f14d769cba7c36b66157ec213bbc32ce57d685d8e2c407cf3987bb`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c674717e06bf8cb25d5887393ef9568ee0ab6390966b9666808e836e9bd471d`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2227badcd9f5f2b70b3d2ffd1c18887498f413c07802bfb334e8dc7b2d2acc`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9f3b5e90a2e6028cf194e870b24a7158f875f18b81f4f9137a5db3ea1f79ac`  
		Last Modified: Thu, 16 Nov 2023 03:11:23 GMT  
		Size: 25.5 MB (25536225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7811a5416dcd19193a5b3ab9327607bf845f7ff77f95d3e20abdfb7435c32ae0`  
		Last Modified: Thu, 16 Nov 2023 03:11:16 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5931209e960a94616639ea72e4d3ad9dc9cb554790ce930152c73bdc1449c034`  
		Last Modified: Thu, 16 Nov 2023 03:11:16 GMT  
		Size: 266.6 KB (266600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a70f603a2fb4e76edd3165b62a179fb8f6410e265f5ae4a3732ee68e610034b`  
		Last Modified: Tue, 05 Dec 2023 20:38:48 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e37840dec3a6665ce48520be8b2c51b654359765bee5ab0780ee74746f0eb2`  
		Last Modified: Tue, 05 Dec 2023 20:39:08 GMT  
		Size: 69.3 MB (69342960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d16ae54757acda093616d24735d4c92d4676649bec49807fc35de90d15e15c`  
		Last Modified: Tue, 05 Dec 2023 20:38:48 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5744d01eddd2ef9d9673fdb0f0e48203fad1b01f2b14899a3ec6393c4548e75`  
		Last Modified: Tue, 05 Dec 2023 21:02:23 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35bb848667aa413b6ce6c309a4c2169635b0740dc335b9b39413a00627c01ab`  
		Last Modified: Tue, 05 Dec 2023 21:02:21 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54630e9807bbb8995ce52459e6e3c8d818351c481e0ce29280570e90d0138d33`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f15ec018ec91e33ee96d4f0e6b66d9edb40b185a13f91d16f12d0bf682ab08b`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79cc8b934303f209cd48271252cb46966445a1099aac277ae4caf120af718ab`  
		Last Modified: Fri, 08 Dec 2023 20:23:49 GMT  
		Size: 1.7 MB (1677815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224f75043e75fb7c85d3daec88a29069c6ff40b8feeaa26bac868d524758955`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:23526c514f90e81e3b94593ed41182252a81ba946c70cf1d2638381f84849d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.5122; amd64
	-	windows version 10.0.20348.2113; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.5122; amd64

```console
$ docker pull caddy@sha256:3d281f8c1d34b38abb3b5ca4ff98d70312daad9b0654a470374d0447a69a3ccf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073448315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e423604e6f05b59d8afa51e2d09a8fc11e1ac3353a126e3ce73b1c2bc65872b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:16:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:16:25 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:17:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:17:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:17:34 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:17:35 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:17:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:17:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:17:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:17:41 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:17:43 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:18:34 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:18:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09e9b6b38c0082853f1d6caa4d3536344a04da2aa5b674837aba8781b265e0d`  
		Last Modified: Fri, 08 Dec 2023 20:22:45 GMT  
		Size: 462.7 KB (462693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb778801cf9547a5b9021d3090bd8e4fc05f09e3aed56b6950dcbd044211d3f`  
		Last Modified: Fri, 08 Dec 2023 20:22:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ec815279848293cd980ed43a496bf4d3e8f8035f8d46dd1a3278e02c4558a8`  
		Last Modified: Fri, 08 Dec 2023 20:22:46 GMT  
		Size: 15.3 MB (15274633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9671feff108f8e0d8be270b64952394b3eaf7d16a7e9163cffc500ad3a42bd17`  
		Last Modified: Fri, 08 Dec 2023 20:22:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44f97706c45d8ebb4578d93d6c1cb5ecc4625f2f78fa40f25f9e72af014449a`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7b5732d0f0e4f61cac2e09f77054657b1bfc21c56b5b4b842e96ee7de3d45d`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348bbb9a26a300473cbb347ce3e405736e7a71ef7d2e67068452760fe4a1a67e`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4dc80dd8b7091a5cb553a95c06fa14380bf94a6f80467e3d7a36cb649fce8c`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6e2ab9cd2c6c903f643bcab22655dc93ec72fcc2f748a47375e2209580eed8`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a498a93a315d79030214cb59d847ede547dfc1159616120a3b48f2b1585bccfc`  
		Last Modified: Fri, 08 Dec 2023 20:22:40 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a7d0f8e26a8dd06b83bb38bfecf51f24ec1456947f459528e71b2544d13f5`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0da3c95480c1f76c862487e0683bed75c660c5cce3e3864677b8c956228e64`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1712e0793bc7067adabbb602cf9eaf0e6ab60f33be0b2b10282325884270ab07`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26aa77bbc553e8bf9318552da7ffe35258b387e04151dd211a006f50cb57a6`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e384f6873d9619640183b8c67671c94c80eb3725ac52c312de84b314b2cd4c53`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7ecef2ca51e4738a30164e40d773f9bfcc9a55bda13a00745349db1618fbf0`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29866626f3b37691b2e593b7ad8a6d3f6e916d9ca428c22e1b3834e568c605c9`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dff7ab50f452876c91da33fe48a0e1409de6cbb0ffca4e1aefa68caa5722d01`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 256.7 KB (256705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55865895b10a6247b60406c70eaa3584e7904512f0092bd7d9013bd9fe64c740`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.20348.2113; amd64

```console
$ docker pull caddy@sha256:cca2801fca8e41625ec6c3c42ee17cc76b64320f93ec2c37999b29b5f9ff0747
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1902845713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ad0d44150328d8253edf3d339d33f508e3a25395c8fd773d2d2fe5966eb244`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:19:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:19:10 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:19:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:19:34 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:19:35 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:19:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:19:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:19:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:19:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:19:43 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:19:44 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:19:58 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:19:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9e496904b6bbc7ce10b08f4c5c00b922d19bb8ebfca4735ba504c9ca77dd2b`  
		Last Modified: Fri, 08 Dec 2023 20:23:12 GMT  
		Size: 474.4 KB (474429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d370d88e3c2ee411f6f86dd892eba2c381cf5706823fcf82fec94a47d7d3bb4`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1861a873425170bdbe2b563cd2b9584401a7be0e3d9a6ceac998eef4eab482ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:13 GMT  
		Size: 15.3 MB (15274241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e17c8887831a9d0a255eb44daaaedffc1bb98b51fc0177786dd130c85034006`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2595203a1e7cbe5c30c3a77633ff7b832c6f07580e688e7c2bc89b5442e72ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b5a75922e76c5c96d069952df83b51d1243d2d6955db5b45dd7b63aea2b3a1`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bbe845ab80dc71320eea94c3d56888074ea930dc6fbe934c60e6c801e9cee3`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74052a6ffee1242926db0907e5406b7e5d81e181d3c9c266d381aaf221bf0252`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbd2ebe3b760156655b6475d7ff52b549e20b5115cf815016c902f834bf3f14`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5945b936f7903435999bc26916fd896f5c645c5b70834243317e66b14d7c2d97`  
		Last Modified: Fri, 08 Dec 2023 20:23:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4345b37fb7af089771ba8cf5542de3045ebb0f1d247ea038535504b320c4ac2c`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12593e8f188e5024af21891d9f3141bc5b85d9e2e9e2b61d7c2634f9f491b9a4`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3632692d5118ec05512cfb67c4aa09a8dfdfe1e40467dfc5ee8e5d2e9a349b2a`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e694808297bceaf6299316f20be2a78e4d2eef8a2ca455dd79ce544cf0a00e66`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258e53ea4c6d9b42de13f722ade5338a5393993985f05ca5b438982dde948654`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20692d7b4da06a40fca6c59bffc5e13dc0a0ffc429f70ed8701dc1d5d8c087fd`  
		Last Modified: Fri, 08 Dec 2023 20:23:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f686dbb1484378b8f73bbbfac32eb04d8f9a6b2b3f4db7d17c1f997941475a7f`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84003630e1340399082b07e0df6cb438545136bc3f0c134d52e8fe9d878e7239`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 292.2 KB (292197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9991bbf8fb125121b7478726325dcb657bfbeb24af279019b7b2f7ac0c404f7`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:67a59b537826dfa0019b55a7c113d5bdd826062754543ae24cccdcf2a558d407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull caddy@sha256:3d281f8c1d34b38abb3b5ca4ff98d70312daad9b0654a470374d0447a69a3ccf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073448315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e423604e6f05b59d8afa51e2d09a8fc11e1ac3353a126e3ce73b1c2bc65872b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:16:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:16:25 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:17:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:17:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:17:34 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:17:35 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:17:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:17:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:17:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:17:41 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:17:43 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:18:34 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:18:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09e9b6b38c0082853f1d6caa4d3536344a04da2aa5b674837aba8781b265e0d`  
		Last Modified: Fri, 08 Dec 2023 20:22:45 GMT  
		Size: 462.7 KB (462693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb778801cf9547a5b9021d3090bd8e4fc05f09e3aed56b6950dcbd044211d3f`  
		Last Modified: Fri, 08 Dec 2023 20:22:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ec815279848293cd980ed43a496bf4d3e8f8035f8d46dd1a3278e02c4558a8`  
		Last Modified: Fri, 08 Dec 2023 20:22:46 GMT  
		Size: 15.3 MB (15274633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9671feff108f8e0d8be270b64952394b3eaf7d16a7e9163cffc500ad3a42bd17`  
		Last Modified: Fri, 08 Dec 2023 20:22:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44f97706c45d8ebb4578d93d6c1cb5ecc4625f2f78fa40f25f9e72af014449a`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7b5732d0f0e4f61cac2e09f77054657b1bfc21c56b5b4b842e96ee7de3d45d`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348bbb9a26a300473cbb347ce3e405736e7a71ef7d2e67068452760fe4a1a67e`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4dc80dd8b7091a5cb553a95c06fa14380bf94a6f80467e3d7a36cb649fce8c`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6e2ab9cd2c6c903f643bcab22655dc93ec72fcc2f748a47375e2209580eed8`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a498a93a315d79030214cb59d847ede547dfc1159616120a3b48f2b1585bccfc`  
		Last Modified: Fri, 08 Dec 2023 20:22:40 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a7d0f8e26a8dd06b83bb38bfecf51f24ec1456947f459528e71b2544d13f5`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0da3c95480c1f76c862487e0683bed75c660c5cce3e3864677b8c956228e64`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1712e0793bc7067adabbb602cf9eaf0e6ab60f33be0b2b10282325884270ab07`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26aa77bbc553e8bf9318552da7ffe35258b387e04151dd211a006f50cb57a6`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e384f6873d9619640183b8c67671c94c80eb3725ac52c312de84b314b2cd4c53`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7ecef2ca51e4738a30164e40d773f9bfcc9a55bda13a00745349db1618fbf0`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29866626f3b37691b2e593b7ad8a6d3f6e916d9ca428c22e1b3834e568c605c9`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dff7ab50f452876c91da33fe48a0e1409de6cbb0ffca4e1aefa68caa5722d01`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 256.7 KB (256705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55865895b10a6247b60406c70eaa3584e7904512f0092bd7d9013bd9fe64c740`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:0726791503ced6bf9bdc5b322a8082762fb4ca97438a2c8fb49d0e80f06838ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull caddy@sha256:cca2801fca8e41625ec6c3c42ee17cc76b64320f93ec2c37999b29b5f9ff0747
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1902845713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ad0d44150328d8253edf3d339d33f508e3a25395c8fd773d2d2fe5966eb244`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:19:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:19:10 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:19:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:19:34 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:19:35 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:19:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:19:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:19:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:19:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:19:43 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:19:44 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:19:58 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:19:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9e496904b6bbc7ce10b08f4c5c00b922d19bb8ebfca4735ba504c9ca77dd2b`  
		Last Modified: Fri, 08 Dec 2023 20:23:12 GMT  
		Size: 474.4 KB (474429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d370d88e3c2ee411f6f86dd892eba2c381cf5706823fcf82fec94a47d7d3bb4`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1861a873425170bdbe2b563cd2b9584401a7be0e3d9a6ceac998eef4eab482ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:13 GMT  
		Size: 15.3 MB (15274241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e17c8887831a9d0a255eb44daaaedffc1bb98b51fc0177786dd130c85034006`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2595203a1e7cbe5c30c3a77633ff7b832c6f07580e688e7c2bc89b5442e72ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b5a75922e76c5c96d069952df83b51d1243d2d6955db5b45dd7b63aea2b3a1`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bbe845ab80dc71320eea94c3d56888074ea930dc6fbe934c60e6c801e9cee3`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74052a6ffee1242926db0907e5406b7e5d81e181d3c9c266d381aaf221bf0252`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbd2ebe3b760156655b6475d7ff52b549e20b5115cf815016c902f834bf3f14`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5945b936f7903435999bc26916fd896f5c645c5b70834243317e66b14d7c2d97`  
		Last Modified: Fri, 08 Dec 2023 20:23:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4345b37fb7af089771ba8cf5542de3045ebb0f1d247ea038535504b320c4ac2c`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12593e8f188e5024af21891d9f3141bc5b85d9e2e9e2b61d7c2634f9f491b9a4`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3632692d5118ec05512cfb67c4aa09a8dfdfe1e40467dfc5ee8e5d2e9a349b2a`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e694808297bceaf6299316f20be2a78e4d2eef8a2ca455dd79ce544cf0a00e66`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258e53ea4c6d9b42de13f722ade5338a5393993985f05ca5b438982dde948654`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20692d7b4da06a40fca6c59bffc5e13dc0a0ffc429f70ed8701dc1d5d8c087fd`  
		Last Modified: Fri, 08 Dec 2023 20:23:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f686dbb1484378b8f73bbbfac32eb04d8f9a6b2b3f4db7d17c1f997941475a7f`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84003630e1340399082b07e0df6cb438545136bc3f0c134d52e8fe9d878e7239`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 292.2 KB (292197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9991bbf8fb125121b7478726325dcb657bfbeb24af279019b7b2f7ac0c404f7`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7`

```console
$ docker pull caddy@sha256:e523a9bc9e19fb96a082b4d83ebae2ce6267f56f2b7b4ac462135ebc51f68e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5122; amd64
	-	windows version 10.0.20348.2113; amd64

### `caddy:2.7` - linux; amd64

```console
$ docker pull caddy@sha256:7b8b4b0a4784433bd53271ff8f27d0940f96b1e633bb69b27d2c9ac5a293536a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18467236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657b947906e764d7ff65a638b958cb7f84b3754e49ede071620658385e743168`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:32:06 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:39:38 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:39:38 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:39:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:39:41 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:39:41 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:39:41 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:39:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:39:42 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:39:42 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:39:42 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:39:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08886dfc0722c4ed2cb6a70c285a33fe35aec069435868488356dde320b4d21c`  
		Last Modified: Fri, 01 Dec 2023 06:32:30 GMT  
		Size: 350.8 KB (350845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd2155878b9ec9d659128d039d90b8a50369fe85c88f64a597b6a9cd9441c1b`  
		Last Modified: Fri, 08 Dec 2023 20:40:01 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7343593237d1bd5fb218804e360a7a8c4d94d7af8da4eb1a72fbaf48fab9ce2`  
		Last Modified: Fri, 08 Dec 2023 20:40:03 GMT  
		Size: 14.7 MB (14706441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - linux; arm variant v6

```console
$ docker pull caddy@sha256:fe42da7df688686dab79fb02be7f13aae32c9a9f84eec3b28b634cc48d5a7346
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17423030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f95b690a9e892f56dbf3fd455d714c2d22ebd35967fdc770fb704c870eeffc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:39:01 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:07:47 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:07:47 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:07:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:07:50 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:07:50 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:07:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:07:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:07:51 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:07:51 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc24e4ccf558b6e992efaaa7a735322be11fe99ce19e722eee6ae70bb76515d`  
		Last Modified: Fri, 01 Dec 2023 00:39:21 GMT  
		Size: 347.6 KB (347632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775b4c8558ad1bf8d7568fc741be39ee2a28ecdd33f84ed7597b6192873a81a`  
		Last Modified: Fri, 08 Dec 2023 20:08:10 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbf57a0db316ab6b42386b0221d652cc4f9d9d597206ce1d4e9bfd5ba0f7777`  
		Last Modified: Fri, 08 Dec 2023 20:08:12 GMT  
		Size: 13.9 MB (13920999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - linux; arm variant v7

```console
$ docker pull caddy@sha256:cf486c3cc2b7d7cc0bdfc8db52605e6a533c0528e717b2ccd6e9779713d72229
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17146731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68a807660343335d38b999c8c1b687f5ec5c882c6f5180e13281152b030f103`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:19:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:16:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:16:22 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:16:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:16:25 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:16:26 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:16:27 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:16:27 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:16:28 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:16:28 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:16:28 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:16:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803b34e1f84b29ca968d2fbf85c278608566c34dfd1742e088c6483685957029`  
		Last Modified: Fri, 01 Dec 2023 03:19:48 GMT  
		Size: 344.5 KB (344464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de504bcc2429a4454910b605f8bb2f6eec4cad953044e48d02a7d51542b7266f`  
		Last Modified: Fri, 08 Dec 2023 20:16:53 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73099274a85e30e93cb0e71106c443fd9a5b923ef43adabf808db6a58db9ad8b`  
		Last Modified: Fri, 08 Dec 2023 20:16:56 GMT  
		Size: 13.9 MB (13893732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:71069b6f75345cd8b5e4841d92dcaebb4fa2acf454074eeb2c571517ac3671cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae18940ab920c723e970d89fde606b552e5b39f5fa33535cb6c7be09b6cff763`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:11:08 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 19:55:15 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 19:55:16 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 19:55:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 19:55:17 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 19:55:17 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 19:55:17 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 80
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 443
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 19:55:18 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 19:55:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e383270d6915b6b427f49a75d657d5a0403fcd47a5f89cd30e85143ca54c22`  
		Last Modified: Fri, 01 Dec 2023 03:11:28 GMT  
		Size: 360.7 KB (360655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f87e6bdbafc6710a3ed7bfbb4bb134e8d93bea992ab895c653cac0779389396`  
		Last Modified: Fri, 08 Dec 2023 19:55:35 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874486d3ac5891d4df17819e02e1cdd3775748effa24bc53645cd2db841a0837`  
		Last Modified: Fri, 08 Dec 2023 19:55:36 GMT  
		Size: 13.6 MB (13568967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - linux; ppc64le

```console
$ docker pull caddy@sha256:9991e527a64c1d20422e24e141a57efec5365c7bcd68662808b0ea23da815b3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17051913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274840ad1c2fe6344d298e9d6242bde6e602b3444a071cfe45d3db4360d193b4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:42:19 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:22:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:22:14 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:22:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:22:19 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:22:19 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:22:19 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:22:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:22:20 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:22:22 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:22:22 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:22:23 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:22:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:22:24 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:22:24 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:22:25 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:22:25 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:22:26 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:22:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce4bc2907f69809c3086f118895d7e5c8683349557239c0ce79dfbda0ce3768`  
		Last Modified: Fri, 01 Dec 2023 05:44:17 GMT  
		Size: 362.2 KB (362185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3c2787bdbaa50fce90e65038b2dbc9850d2fff68d5e731bcdb83c71ede912b`  
		Last Modified: Fri, 08 Dec 2023 20:22:53 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ce50c6341ede9fe5f61cc3a75eb534b7dd1172b7e88c015862cb9351c91ca1`  
		Last Modified: Fri, 08 Dec 2023 20:22:55 GMT  
		Size: 13.3 MB (13333877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - linux; s390x

```console
$ docker pull caddy@sha256:f8db25c8783258ee73a7ab061dbcb53f5229be2510ab4c72cbb6fe5292fdd1a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17818230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4782f6a3e2f343e87b335a56846d9ae67a4a5aded358a8501a4fb5a076e92cef`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:22:31 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 19:57:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 19:57:07 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 19:57:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 19:57:11 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 19:57:11 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 19:57:13 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 19:57:13 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 19:57:13 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 19:57:13 GMT
EXPOSE 80
# Fri, 08 Dec 2023 19:57:13 GMT
EXPOSE 443
# Fri, 08 Dec 2023 19:57:14 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 19:57:14 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 19:57:14 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 19:57:14 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20bbe0abb0a3f63718aa78742832077ad86b8ae86d70ce3ebcece342ec022c6`  
		Last Modified: Fri, 01 Dec 2023 08:23:07 GMT  
		Size: 354.9 KB (354948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa042ad4816c33e4f907bbf008abef2397efe2b3fc378430b2b925663a088370`  
		Last Modified: Fri, 08 Dec 2023 19:57:43 GMT  
		Size: 7.5 KB (7526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ceec9a3d819911fec4d039d31e2e3e38214fa45cb8384e8f047b5588724355`  
		Last Modified: Fri, 08 Dec 2023 19:57:45 GMT  
		Size: 14.2 MB (14238302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - windows version 10.0.17763.5122; amd64

```console
$ docker pull caddy@sha256:3d281f8c1d34b38abb3b5ca4ff98d70312daad9b0654a470374d0447a69a3ccf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073448315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e423604e6f05b59d8afa51e2d09a8fc11e1ac3353a126e3ce73b1c2bc65872b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:16:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:16:25 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:17:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:17:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:17:34 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:17:35 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:17:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:17:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:17:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:17:41 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:17:43 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:18:34 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:18:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09e9b6b38c0082853f1d6caa4d3536344a04da2aa5b674837aba8781b265e0d`  
		Last Modified: Fri, 08 Dec 2023 20:22:45 GMT  
		Size: 462.7 KB (462693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb778801cf9547a5b9021d3090bd8e4fc05f09e3aed56b6950dcbd044211d3f`  
		Last Modified: Fri, 08 Dec 2023 20:22:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ec815279848293cd980ed43a496bf4d3e8f8035f8d46dd1a3278e02c4558a8`  
		Last Modified: Fri, 08 Dec 2023 20:22:46 GMT  
		Size: 15.3 MB (15274633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9671feff108f8e0d8be270b64952394b3eaf7d16a7e9163cffc500ad3a42bd17`  
		Last Modified: Fri, 08 Dec 2023 20:22:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44f97706c45d8ebb4578d93d6c1cb5ecc4625f2f78fa40f25f9e72af014449a`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7b5732d0f0e4f61cac2e09f77054657b1bfc21c56b5b4b842e96ee7de3d45d`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348bbb9a26a300473cbb347ce3e405736e7a71ef7d2e67068452760fe4a1a67e`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4dc80dd8b7091a5cb553a95c06fa14380bf94a6f80467e3d7a36cb649fce8c`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6e2ab9cd2c6c903f643bcab22655dc93ec72fcc2f748a47375e2209580eed8`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a498a93a315d79030214cb59d847ede547dfc1159616120a3b48f2b1585bccfc`  
		Last Modified: Fri, 08 Dec 2023 20:22:40 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a7d0f8e26a8dd06b83bb38bfecf51f24ec1456947f459528e71b2544d13f5`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0da3c95480c1f76c862487e0683bed75c660c5cce3e3864677b8c956228e64`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1712e0793bc7067adabbb602cf9eaf0e6ab60f33be0b2b10282325884270ab07`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26aa77bbc553e8bf9318552da7ffe35258b387e04151dd211a006f50cb57a6`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e384f6873d9619640183b8c67671c94c80eb3725ac52c312de84b314b2cd4c53`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7ecef2ca51e4738a30164e40d773f9bfcc9a55bda13a00745349db1618fbf0`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29866626f3b37691b2e593b7ad8a6d3f6e916d9ca428c22e1b3834e568c605c9`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dff7ab50f452876c91da33fe48a0e1409de6cbb0ffca4e1aefa68caa5722d01`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 256.7 KB (256705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55865895b10a6247b60406c70eaa3584e7904512f0092bd7d9013bd9fe64c740`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - windows version 10.0.20348.2113; amd64

```console
$ docker pull caddy@sha256:cca2801fca8e41625ec6c3c42ee17cc76b64320f93ec2c37999b29b5f9ff0747
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1902845713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ad0d44150328d8253edf3d339d33f508e3a25395c8fd773d2d2fe5966eb244`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:19:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:19:10 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:19:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:19:34 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:19:35 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:19:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:19:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:19:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:19:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:19:43 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:19:44 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:19:58 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:19:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9e496904b6bbc7ce10b08f4c5c00b922d19bb8ebfca4735ba504c9ca77dd2b`  
		Last Modified: Fri, 08 Dec 2023 20:23:12 GMT  
		Size: 474.4 KB (474429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d370d88e3c2ee411f6f86dd892eba2c381cf5706823fcf82fec94a47d7d3bb4`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1861a873425170bdbe2b563cd2b9584401a7be0e3d9a6ceac998eef4eab482ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:13 GMT  
		Size: 15.3 MB (15274241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e17c8887831a9d0a255eb44daaaedffc1bb98b51fc0177786dd130c85034006`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2595203a1e7cbe5c30c3a77633ff7b832c6f07580e688e7c2bc89b5442e72ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b5a75922e76c5c96d069952df83b51d1243d2d6955db5b45dd7b63aea2b3a1`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bbe845ab80dc71320eea94c3d56888074ea930dc6fbe934c60e6c801e9cee3`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74052a6ffee1242926db0907e5406b7e5d81e181d3c9c266d381aaf221bf0252`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbd2ebe3b760156655b6475d7ff52b549e20b5115cf815016c902f834bf3f14`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5945b936f7903435999bc26916fd896f5c645c5b70834243317e66b14d7c2d97`  
		Last Modified: Fri, 08 Dec 2023 20:23:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4345b37fb7af089771ba8cf5542de3045ebb0f1d247ea038535504b320c4ac2c`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12593e8f188e5024af21891d9f3141bc5b85d9e2e9e2b61d7c2634f9f491b9a4`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3632692d5118ec05512cfb67c4aa09a8dfdfe1e40467dfc5ee8e5d2e9a349b2a`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e694808297bceaf6299316f20be2a78e4d2eef8a2ca455dd79ce544cf0a00e66`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258e53ea4c6d9b42de13f722ade5338a5393993985f05ca5b438982dde948654`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20692d7b4da06a40fca6c59bffc5e13dc0a0ffc429f70ed8701dc1d5d8c087fd`  
		Last Modified: Fri, 08 Dec 2023 20:23:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f686dbb1484378b8f73bbbfac32eb04d8f9a6b2b3f4db7d17c1f997941475a7f`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84003630e1340399082b07e0df6cb438545136bc3f0c134d52e8fe9d878e7239`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 292.2 KB (292197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9991bbf8fb125121b7478726325dcb657bfbeb24af279019b7b2f7ac0c404f7`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-alpine`

```console
$ docker pull caddy@sha256:eabac2898cf9fc7dc94d3fb03ac84c9c923aa6cc6f04874937d2f525e0d2f006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.7-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:7b8b4b0a4784433bd53271ff8f27d0940f96b1e633bb69b27d2c9ac5a293536a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18467236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657b947906e764d7ff65a638b958cb7f84b3754e49ede071620658385e743168`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:32:06 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:39:38 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:39:38 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:39:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:39:41 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:39:41 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:39:41 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:39:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:39:42 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:39:42 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:39:42 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:39:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08886dfc0722c4ed2cb6a70c285a33fe35aec069435868488356dde320b4d21c`  
		Last Modified: Fri, 01 Dec 2023 06:32:30 GMT  
		Size: 350.8 KB (350845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd2155878b9ec9d659128d039d90b8a50369fe85c88f64a597b6a9cd9441c1b`  
		Last Modified: Fri, 08 Dec 2023 20:40:01 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7343593237d1bd5fb218804e360a7a8c4d94d7af8da4eb1a72fbaf48fab9ce2`  
		Last Modified: Fri, 08 Dec 2023 20:40:03 GMT  
		Size: 14.7 MB (14706441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:fe42da7df688686dab79fb02be7f13aae32c9a9f84eec3b28b634cc48d5a7346
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17423030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f95b690a9e892f56dbf3fd455d714c2d22ebd35967fdc770fb704c870eeffc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:39:01 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:07:47 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:07:47 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:07:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:07:50 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:07:50 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:07:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:07:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:07:51 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:07:51 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc24e4ccf558b6e992efaaa7a735322be11fe99ce19e722eee6ae70bb76515d`  
		Last Modified: Fri, 01 Dec 2023 00:39:21 GMT  
		Size: 347.6 KB (347632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775b4c8558ad1bf8d7568fc741be39ee2a28ecdd33f84ed7597b6192873a81a`  
		Last Modified: Fri, 08 Dec 2023 20:08:10 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbf57a0db316ab6b42386b0221d652cc4f9d9d597206ce1d4e9bfd5ba0f7777`  
		Last Modified: Fri, 08 Dec 2023 20:08:12 GMT  
		Size: 13.9 MB (13920999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:cf486c3cc2b7d7cc0bdfc8db52605e6a533c0528e717b2ccd6e9779713d72229
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17146731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68a807660343335d38b999c8c1b687f5ec5c882c6f5180e13281152b030f103`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:19:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:16:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:16:22 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:16:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:16:25 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:16:26 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:16:27 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:16:27 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:16:28 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:16:28 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:16:28 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:16:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803b34e1f84b29ca968d2fbf85c278608566c34dfd1742e088c6483685957029`  
		Last Modified: Fri, 01 Dec 2023 03:19:48 GMT  
		Size: 344.5 KB (344464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de504bcc2429a4454910b605f8bb2f6eec4cad953044e48d02a7d51542b7266f`  
		Last Modified: Fri, 08 Dec 2023 20:16:53 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73099274a85e30e93cb0e71106c443fd9a5b923ef43adabf808db6a58db9ad8b`  
		Last Modified: Fri, 08 Dec 2023 20:16:56 GMT  
		Size: 13.9 MB (13893732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:71069b6f75345cd8b5e4841d92dcaebb4fa2acf454074eeb2c571517ac3671cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae18940ab920c723e970d89fde606b552e5b39f5fa33535cb6c7be09b6cff763`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:11:08 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 19:55:15 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 19:55:16 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 19:55:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 19:55:17 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 19:55:17 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 19:55:17 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 80
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 443
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 19:55:18 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 19:55:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e383270d6915b6b427f49a75d657d5a0403fcd47a5f89cd30e85143ca54c22`  
		Last Modified: Fri, 01 Dec 2023 03:11:28 GMT  
		Size: 360.7 KB (360655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f87e6bdbafc6710a3ed7bfbb4bb134e8d93bea992ab895c653cac0779389396`  
		Last Modified: Fri, 08 Dec 2023 19:55:35 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874486d3ac5891d4df17819e02e1cdd3775748effa24bc53645cd2db841a0837`  
		Last Modified: Fri, 08 Dec 2023 19:55:36 GMT  
		Size: 13.6 MB (13568967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:9991e527a64c1d20422e24e141a57efec5365c7bcd68662808b0ea23da815b3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17051913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274840ad1c2fe6344d298e9d6242bde6e602b3444a071cfe45d3db4360d193b4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:42:19 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:22:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:22:14 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:22:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:22:19 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:22:19 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:22:19 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:22:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:22:20 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:22:22 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:22:22 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:22:23 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:22:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:22:24 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:22:24 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:22:25 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:22:25 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:22:26 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:22:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce4bc2907f69809c3086f118895d7e5c8683349557239c0ce79dfbda0ce3768`  
		Last Modified: Fri, 01 Dec 2023 05:44:17 GMT  
		Size: 362.2 KB (362185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3c2787bdbaa50fce90e65038b2dbc9850d2fff68d5e731bcdb83c71ede912b`  
		Last Modified: Fri, 08 Dec 2023 20:22:53 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ce50c6341ede9fe5f61cc3a75eb534b7dd1172b7e88c015862cb9351c91ca1`  
		Last Modified: Fri, 08 Dec 2023 20:22:55 GMT  
		Size: 13.3 MB (13333877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:f8db25c8783258ee73a7ab061dbcb53f5229be2510ab4c72cbb6fe5292fdd1a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17818230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4782f6a3e2f343e87b335a56846d9ae67a4a5aded358a8501a4fb5a076e92cef`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:22:31 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 19:57:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 19:57:07 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 19:57:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 19:57:11 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 19:57:11 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 19:57:13 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 19:57:13 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 19:57:13 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 19:57:13 GMT
EXPOSE 80
# Fri, 08 Dec 2023 19:57:13 GMT
EXPOSE 443
# Fri, 08 Dec 2023 19:57:14 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 19:57:14 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 19:57:14 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 19:57:14 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20bbe0abb0a3f63718aa78742832077ad86b8ae86d70ce3ebcece342ec022c6`  
		Last Modified: Fri, 01 Dec 2023 08:23:07 GMT  
		Size: 354.9 KB (354948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa042ad4816c33e4f907bbf008abef2397efe2b3fc378430b2b925663a088370`  
		Last Modified: Fri, 08 Dec 2023 19:57:43 GMT  
		Size: 7.5 KB (7526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ceec9a3d819911fec4d039d31e2e3e38214fa45cb8384e8f047b5588724355`  
		Last Modified: Fri, 08 Dec 2023 19:57:45 GMT  
		Size: 14.2 MB (14238302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder`

```console
$ docker pull caddy@sha256:1bad661ef08b648af7c9c79e708965d3a69434285f24de76111124fdf5d339d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5122; amd64
	-	windows version 10.0.20348.2113; amd64

### `caddy:2.7-builder` - linux; amd64

```console
$ docker pull caddy@sha256:64cc92d77653c256c9cde397fb221c57907a57b0fe04f4e83ab2f7123f7f9147
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76963251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccce7adcc2b72b984adc9e5dd37663d1e6e512e39657c41bed43c55b38f9bad9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:46:23 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 03:46:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:25:52 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:26:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:26:02 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:26:02 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:26:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:26:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:26:03 GMT
WORKDIR /go
# Tue, 05 Dec 2023 20:48:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 20:48:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:39:46 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:39:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:39:46 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 20:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 20:39:47 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 20:39:47 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5501dced60f86be38cc73d3c038f7db4afeee65726f7e422aacf09244539ebf1`  
		Last Modified: Fri, 01 Dec 2023 03:50:39 GMT  
		Size: 284.7 KB (284697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63d189496f5f03c835c9c85df2db6920546d36a1701f6b5ad15f800c671605d`  
		Last Modified: Tue, 05 Dec 2023 20:31:27 GMT  
		Size: 67.0 MB (67003308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aeb88dd0f3e06a57abc08c781b85c89d138194918c469aea9a1bed9753d2ed0`  
		Last Modified: Tue, 05 Dec 2023 20:31:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40ff2505fd8d96e76bddb63b05c2d42815db1dabe0093ec8f8f53be403b0d01`  
		Last Modified: Tue, 05 Dec 2023 20:49:17 GMT  
		Size: 5.0 MB (4970029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ba23d637be879f93c12d4e6d077eb636688fa34e5d637f1f9a2f0a28509f0d`  
		Last Modified: Fri, 08 Dec 2023 20:40:19 GMT  
		Size: 1.3 MB (1302232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57ad5b5be9e26b4f05c8402814544f231f87d6a736a05320421e0ce2e623f04`  
		Last Modified: Fri, 08 Dec 2023 20:40:19 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:cd2d4a5ddcdef2492b7b440240d2e3beffa1695c0a1273227efdbc97a0fddc86
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75411895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed519bbe9039d7d32e60f9e1c959613953c4508dc6dd1506a355f0e0fd39bbe7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:53:48 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 00:53:48 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:49:18 GMT
ENV GOLANG_VERSION=1.21.5
# Sat, 09 Dec 2023 01:49:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	elif [ "$arch" = 'armv7' ]; then 		[ -s /usr/local/go/go.env ]; 		before="$(go env GOARM)"; [ "$before" != '7' ]; 		{ 			echo; 			echo '# https://github.com/docker-library/golang/issues/494'; 			echo 'GOARM=7'; 		} >> /usr/local/go/go.env; 		after="$(go env GOARM)"; [ "$after" = '7' ]; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Sat, 09 Dec 2023 01:49:51 GMT
ENV GOTOOLCHAIN=local
# Sat, 09 Dec 2023 01:49:51 GMT
ENV GOPATH=/go
# Sat, 09 Dec 2023 01:49:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 01:49:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Sat, 09 Dec 2023 01:49:52 GMT
WORKDIR /go
# Sat, 09 Dec 2023 02:08:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 09 Dec 2023 02:08:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 09 Dec 2023 02:08:59 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 09 Dec 2023 02:08:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 09 Dec 2023 02:08:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 09 Dec 2023 02:09:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 09 Dec 2023 02:09:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 09 Dec 2023 02:09:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e7ba0492eb25e7f21078441d7cdc65088836bc1984bc4a14cd3e9cd75cbf32`  
		Last Modified: Fri, 01 Dec 2023 01:00:23 GMT  
		Size: 284.9 KB (284884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbf3e566edb99ecb0ecb757d0f571633d7d822bf31896dd76a40ff9d89e98c0`  
		Last Modified: Sat, 09 Dec 2023 01:53:04 GMT  
		Size: 65.8 MB (65764277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e170d213450f3f3c66f85329ded2a75a6b38e5b51cfe01f2ad9d2cc2aab61079`  
		Last Modified: Sat, 09 Dec 2023 01:52:51 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612473e16b229d3c58615a469f9ca073ec9dc483d79cd7bb87479eea58ee5454`  
		Last Modified: Sat, 09 Dec 2023 02:09:20 GMT  
		Size: 5.0 MB (4966653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ed572067dfce272b021aee6f0cd14272e2a1157f0cf11ad00004a5c9354bc0`  
		Last Modified: Sat, 09 Dec 2023 02:09:19 GMT  
		Size: 1.2 MB (1248652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7608cc7cd78c6c2f18a53621dbd0b1746b9274ce1b35a8279b261816e41718ef`  
		Last Modified: Sat, 09 Dec 2023 02:09:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:7b8943fed6d62476c9dea44a16caea83fb6d540be101271d0974e0f2ed5a1567
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74707178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e459d7afebbd1af456db2bc6e8849445ca45f2586a9bbd0337ba314f570a177`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:44:57 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 08:44:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:58:01 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:58:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:58:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:58:16 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:58:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:58:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:58:17 GMT
WORKDIR /go
# Tue, 05 Dec 2023 21:22:31 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 21:22:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:16:31 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:16:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:16:32 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 20:16:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 20:16:34 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 20:16:34 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a824ff289f1a3c765a444079137b8b7f1cee80348faa53e1ba4c960b73ed2a`  
		Last Modified: Fri, 01 Dec 2023 08:49:42 GMT  
		Size: 284.1 KB (284079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4989177b4ed66b7e9f9e8c4bfce82720b582e24b735d6628effa75d81c5718fc`  
		Last Modified: Tue, 05 Dec 2023 21:04:43 GMT  
		Size: 65.8 MB (65764197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f9b58eae167c54d3faa3eeffd480cdae7e8b4841eb816a86cfdd01f8ae29ef`  
		Last Modified: Tue, 05 Dec 2023 21:04:29 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4cd1a3aab8fc02791b1e19f81b7de1bd691c10a7c942acc7e733221bf12888`  
		Last Modified: Tue, 05 Dec 2023 21:22:47 GMT  
		Size: 4.5 MB (4511237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c6a5bcaed596afac229d37cd822ea4770b06d4d3580d14a71d26e32136f1aa`  
		Last Modified: Fri, 08 Dec 2023 20:17:09 GMT  
		Size: 1.2 MB (1246093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c59154934645e7c4d44eda6d3d5ea9d4b32e23fbf7ccb7009cc54413ae815d`  
		Last Modified: Fri, 08 Dec 2023 20:17:09 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:3fce35ec600b6e48bb63c1b2d390b6d515a6f0e7355b582fcb347092222bdc37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73981648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3475cc52d42bfd049fb20d388ecf6c8482841b98a265b9fc09b60bc815011df9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:43:53 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 03:18:30 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:16:18 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:16:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:16:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:16:28 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:16:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:16:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:16:28 GMT
WORKDIR /go
# Tue, 05 Dec 2023 20:38:16 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 20:38:16 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 19:55:21 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 19:55:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 19:55:21 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 19:55:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 19:55:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 19:55:22 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a63ed24dc22a348b35d99b5ec9dc67ff66563b539875e5c8ab2d870b3991ac`  
		Last Modified: Fri, 01 Dec 2023 02:44:03 GMT  
		Size: 286.3 KB (286307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f00641dffc5c2a149049ee9046bb24cfc7de534b7495a0f27784a4fff0fadc`  
		Last Modified: Tue, 05 Dec 2023 20:21:00 GMT  
		Size: 64.1 MB (64094844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452682ba77e89fc55be3a168358f5f43bccad93ecdd3d53b4dec7fff6915128b`  
		Last Modified: Tue, 05 Dec 2023 20:20:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3fe1e12507f8c4a2731393eebfc5ab973aa344b0daceec525560b812b26f60`  
		Last Modified: Tue, 05 Dec 2023 20:38:33 GMT  
		Size: 5.1 MB (5068450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1568fb18f5eae3df776dd2fee8d447615d0f62601f82ebdb1bf2af5155bb83`  
		Last Modified: Fri, 08 Dec 2023 19:55:49 GMT  
		Size: 1.2 MB (1198450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15988851efd259492be8e7583025cb2b00f7477442c7be3e2d3dd97adbc39e76`  
		Last Modified: Fri, 08 Dec 2023 19:55:48 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:e21739ed4cecc54ebd496b12fa757f5901f3c0b45d211c0c5fa2ef551543c2d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74206507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed778e73218e8613cd2044f7eb703ec05bf43271d444ca5ffe77e053baa719c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:37:34 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 06:37:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:38:14 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:38:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:38:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:38:38 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:38:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:38:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:38:41 GMT
WORKDIR /go
# Tue, 05 Dec 2023 21:04:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 21:04:34 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:22:32 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:22:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:22:33 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 20:22:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 20:22:35 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 20:22:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692dbecd5e141c462ab06ef113ec964b525e7564d734890cc1d5b1dbf33ee34e`  
		Last Modified: Fri, 01 Dec 2023 06:43:30 GMT  
		Size: 286.7 KB (286661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc89a0f2d97ecfd4d20235e72227fc24aa79a64509fe9ea64702db658f2ad26d`  
		Last Modified: Tue, 05 Dec 2023 20:46:23 GMT  
		Size: 64.1 MB (64115804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d76f2c2e2bbb4190b1865ddafdc8cb88adee4c79d7d5ba23e69696e9610889`  
		Last Modified: Tue, 05 Dec 2023 20:46:11 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e0ec0f713ee657d6aa159fab65c05939480b5ca50a8e3dc4b1a9a6578160f7`  
		Last Modified: Tue, 05 Dec 2023 21:04:57 GMT  
		Size: 5.3 MB (5268970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbd7401349780157d6d930ec942f00b1d5404d31ae60bff5c7b41238cf8e3b1`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 1.2 MB (1186185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67206b5e4434d3211a98a71837832baed45e4fb0c03ff8dc204bc7762a8ab559`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; s390x

```console
$ docker pull caddy@sha256:bf201fa7da491e4decf9c0a638b9fbcb4b459d5b13bcc9a2f4c0fb4c583c609b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76101050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e2b3cda7ff391c43b985fdbd1c3515e69b6fbe94f8ea6c9a09749c147e491c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:14:49 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 08:14:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:44:16 GMT
ENV GOLANG_VERSION=1.21.5
# Sat, 09 Dec 2023 01:50:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	elif [ "$arch" = 'armv7' ]; then 		[ -s /usr/local/go/go.env ]; 		before="$(go env GOARM)"; [ "$before" != '7' ]; 		{ 			echo; 			echo '# https://github.com/docker-library/golang/issues/494'; 			echo 'GOARM=7'; 		} >> /usr/local/go/go.env; 		after="$(go env GOARM)"; [ "$after" = '7' ]; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Sat, 09 Dec 2023 01:50:41 GMT
ENV GOTOOLCHAIN=local
# Sat, 09 Dec 2023 01:50:41 GMT
ENV GOPATH=/go
# Sat, 09 Dec 2023 01:50:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 01:50:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Sat, 09 Dec 2023 01:50:42 GMT
WORKDIR /go
# Sat, 09 Dec 2023 02:12:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 09 Dec 2023 02:12:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 09 Dec 2023 02:12:31 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 09 Dec 2023 02:12:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 09 Dec 2023 02:12:31 GMT
ENV XCADDY_SETCAP=1
# Sat, 09 Dec 2023 02:12:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 09 Dec 2023 02:12:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 09 Dec 2023 02:12:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab563e8d41683e124df048aa9b564b0e8e1021e85213666971a015df51d5e48`  
		Last Modified: Fri, 01 Dec 2023 08:20:46 GMT  
		Size: 285.1 KB (285090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c541c9463bd8d06e97aa1b14ce0792cf2caf6ef8ddc7b046b21032b3390bee`  
		Last Modified: Sat, 09 Dec 2023 01:54:50 GMT  
		Size: 66.2 MB (66218593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236faa4ca6aed551be037e8e0a2312e72dedf504cdffa8d2015882df02c5b87e`  
		Last Modified: Sat, 09 Dec 2023 01:54:39 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee294f5771410ee01c59c398d0270a28f5ae4caff9abfa5339f1c54b1dc1ab5a`  
		Last Modified: Sat, 09 Dec 2023 02:12:56 GMT  
		Size: 5.1 MB (5116966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cbd016bf9fbfd249882a217530ca94dcac095e46620a64badd9bbfa6ae9ebe`  
		Last Modified: Sat, 09 Dec 2023 02:12:55 GMT  
		Size: 1.3 MB (1262386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b36774ae94aa93a3beb6e355ee08897437b53c870bc56fdc3047ce591cfa2ac`  
		Last Modified: Sat, 09 Dec 2023 02:12:55 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - windows version 10.0.17763.5122; amd64

```console
$ docker pull caddy@sha256:cdab1fd140455df0674bfedde2f4948b5289720efd10ff1301ce39bb60cd8daf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154297412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39391f7d87fac7b43f0ed0b59b1981b263a30d3397f5f5244adf81cb7627ba5a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 02:47:03 GMT
ENV GIT_VERSION=2.23.0
# Thu, 16 Nov 2023 02:47:04 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 16 Nov 2023 02:47:05 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 16 Nov 2023 02:47:06 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 16 Nov 2023 02:48:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 02:48:31 GMT
ENV GOPATH=C:\go
# Thu, 16 Nov 2023 02:49:41 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Dec 2023 20:18:04 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:21:11 GMT
RUN $url = 'https://dl.google.com/go/go1.21.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bbe603cde7c9dee658f45164b4d06de1eff6e6e6b800100824e7c00d56a9a92f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Dec 2023 20:21:13 GMT
WORKDIR C:\go
# Tue, 05 Dec 2023 20:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Dec 2023 20:59:30 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:20:06 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:20:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:21:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 08 Dec 2023 20:21:15 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e901367fac1450f509d3118ada9e004e3613844ebdf91861147a093483930a4`  
		Last Modified: Thu, 16 Nov 2023 03:11:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e08004205bd077d8f22b013c70dc2f10796c64fced1eb9927e0055daff2d05d`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebc5048afc68ef48e2f2136545e2cccf26bb29eb4926bf4259b370ad55b4e7a`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f50fe5c7ef21648f3eaa4304932877a116fcb910b8e9095c779a2fbe6d57f7e`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76fe0e37750041d4ede2a0ca3b5245cfe075c3eb2ee27d7ce72ee8c3d7b20cc`  
		Last Modified: Thu, 16 Nov 2023 03:12:00 GMT  
		Size: 25.5 MB (25537512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8097bb9b8778d15dbf89d899653bf1634ec17554e5d84ef1ccfcac8ebf86afe2`  
		Last Modified: Thu, 16 Nov 2023 03:11:53 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b542d31e914d67da86cc5701cdc282ab664dc1170507e3802e22ab3026436a90`  
		Last Modified: Thu, 16 Nov 2023 03:11:53 GMT  
		Size: 263.2 KB (263200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86acdf7d3955fb44136bac433a30ccbbb97863120f270af32659dd65446666c7`  
		Last Modified: Tue, 05 Dec 2023 20:39:22 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1abe126c354944b7db8aa724d8f757167f7c3b36d39f976ef3b1b0d1b1b65ab`  
		Last Modified: Tue, 05 Dec 2023 20:39:41 GMT  
		Size: 69.4 MB (69361283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6338af096e09067ad482a0f4a6df1d1eee5b5595a64ca5f367b94ce27903e284`  
		Last Modified: Tue, 05 Dec 2023 20:39:22 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0adc218b27ef5639384c060fb663de3bd74374279d3fd525aa281f63a754779`  
		Last Modified: Tue, 05 Dec 2023 21:02:06 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c21053b248805df7ad888734f5cd1df5a6b426111512d5a6b7530060e7f30b2`  
		Last Modified: Tue, 05 Dec 2023 21:02:03 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034eb8f336a0d8e998c3eef6834d07c072c0679ccd4fde02cc8787ed46c80b19`  
		Last Modified: Fri, 08 Dec 2023 20:23:31 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af9b0b53a037a76c1c2e0e3afbe4fad733bc634a5ca02d53055360d9b7e33b9`  
		Last Modified: Fri, 08 Dec 2023 20:23:31 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f653ab9a896e2a3cfaf147a9ebb6e2d23f453cc3f953ee19b27333ebbc66460b`  
		Last Modified: Fri, 08 Dec 2023 20:23:32 GMT  
		Size: 1.7 MB (1685700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed98b1069776f09873a216052d2bf114c714b8269e4235d0aee375a2b0b7962`  
		Last Modified: Fri, 08 Dec 2023 20:23:31 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - windows version 10.0.20348.2113; amd64

```console
$ docker pull caddy@sha256:b1d94a17104c4814aa7672316e4c713aefcdfa6ffd19043f4111784c09931cda
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1983623336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61ba19fe8fdfa90a532d1f355b356c651a2921264135f6417c72193a5f37396`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 02:43:34 GMT
ENV GIT_VERSION=2.23.0
# Thu, 16 Nov 2023 02:43:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 16 Nov 2023 02:43:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 16 Nov 2023 02:43:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 16 Nov 2023 02:44:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 02:44:11 GMT
ENV GOPATH=C:\go
# Thu, 16 Nov 2023 02:44:30 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Dec 2023 20:15:35 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:17:49 GMT
RUN $url = 'https://dl.google.com/go/go1.21.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bbe603cde7c9dee658f45164b4d06de1eff6e6e6b800100824e7c00d56a9a92f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Dec 2023 20:17:50 GMT
WORKDIR C:\go
# Tue, 05 Dec 2023 21:00:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Dec 2023 21:00:58 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:21:33 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:21:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:21:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 08 Dec 2023 20:21:57 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b1d4a557f047b695f94452d9707061981d7fae4239c674b332282b8291963c`  
		Last Modified: Thu, 16 Nov 2023 03:11:20 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45549c207f14d769cba7c36b66157ec213bbc32ce57d685d8e2c407cf3987bb`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c674717e06bf8cb25d5887393ef9568ee0ab6390966b9666808e836e9bd471d`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2227badcd9f5f2b70b3d2ffd1c18887498f413c07802bfb334e8dc7b2d2acc`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9f3b5e90a2e6028cf194e870b24a7158f875f18b81f4f9137a5db3ea1f79ac`  
		Last Modified: Thu, 16 Nov 2023 03:11:23 GMT  
		Size: 25.5 MB (25536225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7811a5416dcd19193a5b3ab9327607bf845f7ff77f95d3e20abdfb7435c32ae0`  
		Last Modified: Thu, 16 Nov 2023 03:11:16 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5931209e960a94616639ea72e4d3ad9dc9cb554790ce930152c73bdc1449c034`  
		Last Modified: Thu, 16 Nov 2023 03:11:16 GMT  
		Size: 266.6 KB (266600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a70f603a2fb4e76edd3165b62a179fb8f6410e265f5ae4a3732ee68e610034b`  
		Last Modified: Tue, 05 Dec 2023 20:38:48 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e37840dec3a6665ce48520be8b2c51b654359765bee5ab0780ee74746f0eb2`  
		Last Modified: Tue, 05 Dec 2023 20:39:08 GMT  
		Size: 69.3 MB (69342960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d16ae54757acda093616d24735d4c92d4676649bec49807fc35de90d15e15c`  
		Last Modified: Tue, 05 Dec 2023 20:38:48 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5744d01eddd2ef9d9673fdb0f0e48203fad1b01f2b14899a3ec6393c4548e75`  
		Last Modified: Tue, 05 Dec 2023 21:02:23 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35bb848667aa413b6ce6c309a4c2169635b0740dc335b9b39413a00627c01ab`  
		Last Modified: Tue, 05 Dec 2023 21:02:21 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54630e9807bbb8995ce52459e6e3c8d818351c481e0ce29280570e90d0138d33`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f15ec018ec91e33ee96d4f0e6b66d9edb40b185a13f91d16f12d0bf682ab08b`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79cc8b934303f209cd48271252cb46966445a1099aac277ae4caf120af718ab`  
		Last Modified: Fri, 08 Dec 2023 20:23:49 GMT  
		Size: 1.7 MB (1677815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224f75043e75fb7c85d3daec88a29069c6ff40b8feeaa26bac868d524758955`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-alpine`

```console
$ docker pull caddy@sha256:a6d9bf50074feba4597d504f2c617c7d3e772c19b67d0ca788dcf2dcb421bd08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.7-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:64cc92d77653c256c9cde397fb221c57907a57b0fe04f4e83ab2f7123f7f9147
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76963251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccce7adcc2b72b984adc9e5dd37663d1e6e512e39657c41bed43c55b38f9bad9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:46:23 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 03:46:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:25:52 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:26:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:26:02 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:26:02 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:26:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:26:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:26:03 GMT
WORKDIR /go
# Tue, 05 Dec 2023 20:48:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 20:48:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:39:46 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:39:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:39:46 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 20:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 20:39:47 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 20:39:47 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5501dced60f86be38cc73d3c038f7db4afeee65726f7e422aacf09244539ebf1`  
		Last Modified: Fri, 01 Dec 2023 03:50:39 GMT  
		Size: 284.7 KB (284697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63d189496f5f03c835c9c85df2db6920546d36a1701f6b5ad15f800c671605d`  
		Last Modified: Tue, 05 Dec 2023 20:31:27 GMT  
		Size: 67.0 MB (67003308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aeb88dd0f3e06a57abc08c781b85c89d138194918c469aea9a1bed9753d2ed0`  
		Last Modified: Tue, 05 Dec 2023 20:31:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40ff2505fd8d96e76bddb63b05c2d42815db1dabe0093ec8f8f53be403b0d01`  
		Last Modified: Tue, 05 Dec 2023 20:49:17 GMT  
		Size: 5.0 MB (4970029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ba23d637be879f93c12d4e6d077eb636688fa34e5d637f1f9a2f0a28509f0d`  
		Last Modified: Fri, 08 Dec 2023 20:40:19 GMT  
		Size: 1.3 MB (1302232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57ad5b5be9e26b4f05c8402814544f231f87d6a736a05320421e0ce2e623f04`  
		Last Modified: Fri, 08 Dec 2023 20:40:19 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:cd2d4a5ddcdef2492b7b440240d2e3beffa1695c0a1273227efdbc97a0fddc86
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75411895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed519bbe9039d7d32e60f9e1c959613953c4508dc6dd1506a355f0e0fd39bbe7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:53:48 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 00:53:48 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:49:18 GMT
ENV GOLANG_VERSION=1.21.5
# Sat, 09 Dec 2023 01:49:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	elif [ "$arch" = 'armv7' ]; then 		[ -s /usr/local/go/go.env ]; 		before="$(go env GOARM)"; [ "$before" != '7' ]; 		{ 			echo; 			echo '# https://github.com/docker-library/golang/issues/494'; 			echo 'GOARM=7'; 		} >> /usr/local/go/go.env; 		after="$(go env GOARM)"; [ "$after" = '7' ]; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Sat, 09 Dec 2023 01:49:51 GMT
ENV GOTOOLCHAIN=local
# Sat, 09 Dec 2023 01:49:51 GMT
ENV GOPATH=/go
# Sat, 09 Dec 2023 01:49:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 01:49:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Sat, 09 Dec 2023 01:49:52 GMT
WORKDIR /go
# Sat, 09 Dec 2023 02:08:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 09 Dec 2023 02:08:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 09 Dec 2023 02:08:59 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 09 Dec 2023 02:08:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 09 Dec 2023 02:08:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 09 Dec 2023 02:09:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 09 Dec 2023 02:09:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 09 Dec 2023 02:09:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e7ba0492eb25e7f21078441d7cdc65088836bc1984bc4a14cd3e9cd75cbf32`  
		Last Modified: Fri, 01 Dec 2023 01:00:23 GMT  
		Size: 284.9 KB (284884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbf3e566edb99ecb0ecb757d0f571633d7d822bf31896dd76a40ff9d89e98c0`  
		Last Modified: Sat, 09 Dec 2023 01:53:04 GMT  
		Size: 65.8 MB (65764277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e170d213450f3f3c66f85329ded2a75a6b38e5b51cfe01f2ad9d2cc2aab61079`  
		Last Modified: Sat, 09 Dec 2023 01:52:51 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612473e16b229d3c58615a469f9ca073ec9dc483d79cd7bb87479eea58ee5454`  
		Last Modified: Sat, 09 Dec 2023 02:09:20 GMT  
		Size: 5.0 MB (4966653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ed572067dfce272b021aee6f0cd14272e2a1157f0cf11ad00004a5c9354bc0`  
		Last Modified: Sat, 09 Dec 2023 02:09:19 GMT  
		Size: 1.2 MB (1248652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7608cc7cd78c6c2f18a53621dbd0b1746b9274ce1b35a8279b261816e41718ef`  
		Last Modified: Sat, 09 Dec 2023 02:09:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:7b8943fed6d62476c9dea44a16caea83fb6d540be101271d0974e0f2ed5a1567
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74707178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e459d7afebbd1af456db2bc6e8849445ca45f2586a9bbd0337ba314f570a177`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:44:57 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 08:44:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:58:01 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:58:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:58:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:58:16 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:58:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:58:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:58:17 GMT
WORKDIR /go
# Tue, 05 Dec 2023 21:22:31 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 21:22:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:16:31 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:16:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:16:32 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 20:16:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 20:16:34 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 20:16:34 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a824ff289f1a3c765a444079137b8b7f1cee80348faa53e1ba4c960b73ed2a`  
		Last Modified: Fri, 01 Dec 2023 08:49:42 GMT  
		Size: 284.1 KB (284079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4989177b4ed66b7e9f9e8c4bfce82720b582e24b735d6628effa75d81c5718fc`  
		Last Modified: Tue, 05 Dec 2023 21:04:43 GMT  
		Size: 65.8 MB (65764197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f9b58eae167c54d3faa3eeffd480cdae7e8b4841eb816a86cfdd01f8ae29ef`  
		Last Modified: Tue, 05 Dec 2023 21:04:29 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4cd1a3aab8fc02791b1e19f81b7de1bd691c10a7c942acc7e733221bf12888`  
		Last Modified: Tue, 05 Dec 2023 21:22:47 GMT  
		Size: 4.5 MB (4511237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c6a5bcaed596afac229d37cd822ea4770b06d4d3580d14a71d26e32136f1aa`  
		Last Modified: Fri, 08 Dec 2023 20:17:09 GMT  
		Size: 1.2 MB (1246093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c59154934645e7c4d44eda6d3d5ea9d4b32e23fbf7ccb7009cc54413ae815d`  
		Last Modified: Fri, 08 Dec 2023 20:17:09 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:3fce35ec600b6e48bb63c1b2d390b6d515a6f0e7355b582fcb347092222bdc37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73981648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3475cc52d42bfd049fb20d388ecf6c8482841b98a265b9fc09b60bc815011df9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:43:53 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 03:18:30 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:16:18 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:16:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:16:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:16:28 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:16:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:16:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:16:28 GMT
WORKDIR /go
# Tue, 05 Dec 2023 20:38:16 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 20:38:16 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 19:55:21 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 19:55:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 19:55:21 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 19:55:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 19:55:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 19:55:22 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a63ed24dc22a348b35d99b5ec9dc67ff66563b539875e5c8ab2d870b3991ac`  
		Last Modified: Fri, 01 Dec 2023 02:44:03 GMT  
		Size: 286.3 KB (286307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f00641dffc5c2a149049ee9046bb24cfc7de534b7495a0f27784a4fff0fadc`  
		Last Modified: Tue, 05 Dec 2023 20:21:00 GMT  
		Size: 64.1 MB (64094844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452682ba77e89fc55be3a168358f5f43bccad93ecdd3d53b4dec7fff6915128b`  
		Last Modified: Tue, 05 Dec 2023 20:20:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3fe1e12507f8c4a2731393eebfc5ab973aa344b0daceec525560b812b26f60`  
		Last Modified: Tue, 05 Dec 2023 20:38:33 GMT  
		Size: 5.1 MB (5068450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1568fb18f5eae3df776dd2fee8d447615d0f62601f82ebdb1bf2af5155bb83`  
		Last Modified: Fri, 08 Dec 2023 19:55:49 GMT  
		Size: 1.2 MB (1198450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15988851efd259492be8e7583025cb2b00f7477442c7be3e2d3dd97adbc39e76`  
		Last Modified: Fri, 08 Dec 2023 19:55:48 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:e21739ed4cecc54ebd496b12fa757f5901f3c0b45d211c0c5fa2ef551543c2d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74206507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed778e73218e8613cd2044f7eb703ec05bf43271d444ca5ffe77e053baa719c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:37:34 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 06:37:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:38:14 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:38:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:38:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:38:38 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:38:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:38:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:38:41 GMT
WORKDIR /go
# Tue, 05 Dec 2023 21:04:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 21:04:34 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:22:32 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:22:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:22:33 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 20:22:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 20:22:35 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 20:22:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692dbecd5e141c462ab06ef113ec964b525e7564d734890cc1d5b1dbf33ee34e`  
		Last Modified: Fri, 01 Dec 2023 06:43:30 GMT  
		Size: 286.7 KB (286661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc89a0f2d97ecfd4d20235e72227fc24aa79a64509fe9ea64702db658f2ad26d`  
		Last Modified: Tue, 05 Dec 2023 20:46:23 GMT  
		Size: 64.1 MB (64115804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d76f2c2e2bbb4190b1865ddafdc8cb88adee4c79d7d5ba23e69696e9610889`  
		Last Modified: Tue, 05 Dec 2023 20:46:11 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e0ec0f713ee657d6aa159fab65c05939480b5ca50a8e3dc4b1a9a6578160f7`  
		Last Modified: Tue, 05 Dec 2023 21:04:57 GMT  
		Size: 5.3 MB (5268970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbd7401349780157d6d930ec942f00b1d5404d31ae60bff5c7b41238cf8e3b1`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 1.2 MB (1186185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67206b5e4434d3211a98a71837832baed45e4fb0c03ff8dc204bc7762a8ab559`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:bf201fa7da491e4decf9c0a638b9fbcb4b459d5b13bcc9a2f4c0fb4c583c609b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76101050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e2b3cda7ff391c43b985fdbd1c3515e69b6fbe94f8ea6c9a09749c147e491c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:14:49 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 08:14:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:44:16 GMT
ENV GOLANG_VERSION=1.21.5
# Sat, 09 Dec 2023 01:50:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	elif [ "$arch" = 'armv7' ]; then 		[ -s /usr/local/go/go.env ]; 		before="$(go env GOARM)"; [ "$before" != '7' ]; 		{ 			echo; 			echo '# https://github.com/docker-library/golang/issues/494'; 			echo 'GOARM=7'; 		} >> /usr/local/go/go.env; 		after="$(go env GOARM)"; [ "$after" = '7' ]; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Sat, 09 Dec 2023 01:50:41 GMT
ENV GOTOOLCHAIN=local
# Sat, 09 Dec 2023 01:50:41 GMT
ENV GOPATH=/go
# Sat, 09 Dec 2023 01:50:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 01:50:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Sat, 09 Dec 2023 01:50:42 GMT
WORKDIR /go
# Sat, 09 Dec 2023 02:12:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 09 Dec 2023 02:12:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 09 Dec 2023 02:12:31 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 09 Dec 2023 02:12:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 09 Dec 2023 02:12:31 GMT
ENV XCADDY_SETCAP=1
# Sat, 09 Dec 2023 02:12:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 09 Dec 2023 02:12:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 09 Dec 2023 02:12:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab563e8d41683e124df048aa9b564b0e8e1021e85213666971a015df51d5e48`  
		Last Modified: Fri, 01 Dec 2023 08:20:46 GMT  
		Size: 285.1 KB (285090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c541c9463bd8d06e97aa1b14ce0792cf2caf6ef8ddc7b046b21032b3390bee`  
		Last Modified: Sat, 09 Dec 2023 01:54:50 GMT  
		Size: 66.2 MB (66218593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236faa4ca6aed551be037e8e0a2312e72dedf504cdffa8d2015882df02c5b87e`  
		Last Modified: Sat, 09 Dec 2023 01:54:39 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee294f5771410ee01c59c398d0270a28f5ae4caff9abfa5339f1c54b1dc1ab5a`  
		Last Modified: Sat, 09 Dec 2023 02:12:56 GMT  
		Size: 5.1 MB (5116966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cbd016bf9fbfd249882a217530ca94dcac095e46620a64badd9bbfa6ae9ebe`  
		Last Modified: Sat, 09 Dec 2023 02:12:55 GMT  
		Size: 1.3 MB (1262386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b36774ae94aa93a3beb6e355ee08897437b53c870bc56fdc3047ce591cfa2ac`  
		Last Modified: Sat, 09 Dec 2023 02:12:55 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:8bf37ab9a085a9916fcfb4a921ebbfe2d29d2893fac56672655cc8ccd5fa3c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `caddy:2.7-builder-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull caddy@sha256:cdab1fd140455df0674bfedde2f4948b5289720efd10ff1301ce39bb60cd8daf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154297412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39391f7d87fac7b43f0ed0b59b1981b263a30d3397f5f5244adf81cb7627ba5a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 02:47:03 GMT
ENV GIT_VERSION=2.23.0
# Thu, 16 Nov 2023 02:47:04 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 16 Nov 2023 02:47:05 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 16 Nov 2023 02:47:06 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 16 Nov 2023 02:48:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 02:48:31 GMT
ENV GOPATH=C:\go
# Thu, 16 Nov 2023 02:49:41 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Dec 2023 20:18:04 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:21:11 GMT
RUN $url = 'https://dl.google.com/go/go1.21.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bbe603cde7c9dee658f45164b4d06de1eff6e6e6b800100824e7c00d56a9a92f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Dec 2023 20:21:13 GMT
WORKDIR C:\go
# Tue, 05 Dec 2023 20:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Dec 2023 20:59:30 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:20:06 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:20:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:21:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 08 Dec 2023 20:21:15 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e901367fac1450f509d3118ada9e004e3613844ebdf91861147a093483930a4`  
		Last Modified: Thu, 16 Nov 2023 03:11:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e08004205bd077d8f22b013c70dc2f10796c64fced1eb9927e0055daff2d05d`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebc5048afc68ef48e2f2136545e2cccf26bb29eb4926bf4259b370ad55b4e7a`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f50fe5c7ef21648f3eaa4304932877a116fcb910b8e9095c779a2fbe6d57f7e`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76fe0e37750041d4ede2a0ca3b5245cfe075c3eb2ee27d7ce72ee8c3d7b20cc`  
		Last Modified: Thu, 16 Nov 2023 03:12:00 GMT  
		Size: 25.5 MB (25537512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8097bb9b8778d15dbf89d899653bf1634ec17554e5d84ef1ccfcac8ebf86afe2`  
		Last Modified: Thu, 16 Nov 2023 03:11:53 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b542d31e914d67da86cc5701cdc282ab664dc1170507e3802e22ab3026436a90`  
		Last Modified: Thu, 16 Nov 2023 03:11:53 GMT  
		Size: 263.2 KB (263200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86acdf7d3955fb44136bac433a30ccbbb97863120f270af32659dd65446666c7`  
		Last Modified: Tue, 05 Dec 2023 20:39:22 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1abe126c354944b7db8aa724d8f757167f7c3b36d39f976ef3b1b0d1b1b65ab`  
		Last Modified: Tue, 05 Dec 2023 20:39:41 GMT  
		Size: 69.4 MB (69361283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6338af096e09067ad482a0f4a6df1d1eee5b5595a64ca5f367b94ce27903e284`  
		Last Modified: Tue, 05 Dec 2023 20:39:22 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0adc218b27ef5639384c060fb663de3bd74374279d3fd525aa281f63a754779`  
		Last Modified: Tue, 05 Dec 2023 21:02:06 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c21053b248805df7ad888734f5cd1df5a6b426111512d5a6b7530060e7f30b2`  
		Last Modified: Tue, 05 Dec 2023 21:02:03 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034eb8f336a0d8e998c3eef6834d07c072c0679ccd4fde02cc8787ed46c80b19`  
		Last Modified: Fri, 08 Dec 2023 20:23:31 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af9b0b53a037a76c1c2e0e3afbe4fad733bc634a5ca02d53055360d9b7e33b9`  
		Last Modified: Fri, 08 Dec 2023 20:23:31 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f653ab9a896e2a3cfaf147a9ebb6e2d23f453cc3f953ee19b27333ebbc66460b`  
		Last Modified: Fri, 08 Dec 2023 20:23:32 GMT  
		Size: 1.7 MB (1685700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed98b1069776f09873a216052d2bf114c714b8269e4235d0aee375a2b0b7962`  
		Last Modified: Fri, 08 Dec 2023 20:23:31 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:b944570c2f667cfb312913d3478de80037fe9967f6fd20a1358e3f1b87467164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `caddy:2.7-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull caddy@sha256:b1d94a17104c4814aa7672316e4c713aefcdfa6ffd19043f4111784c09931cda
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1983623336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61ba19fe8fdfa90a532d1f355b356c651a2921264135f6417c72193a5f37396`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 02:43:34 GMT
ENV GIT_VERSION=2.23.0
# Thu, 16 Nov 2023 02:43:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 16 Nov 2023 02:43:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 16 Nov 2023 02:43:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 16 Nov 2023 02:44:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 02:44:11 GMT
ENV GOPATH=C:\go
# Thu, 16 Nov 2023 02:44:30 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Dec 2023 20:15:35 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:17:49 GMT
RUN $url = 'https://dl.google.com/go/go1.21.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bbe603cde7c9dee658f45164b4d06de1eff6e6e6b800100824e7c00d56a9a92f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Dec 2023 20:17:50 GMT
WORKDIR C:\go
# Tue, 05 Dec 2023 21:00:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Dec 2023 21:00:58 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:21:33 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:21:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:21:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 08 Dec 2023 20:21:57 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b1d4a557f047b695f94452d9707061981d7fae4239c674b332282b8291963c`  
		Last Modified: Thu, 16 Nov 2023 03:11:20 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45549c207f14d769cba7c36b66157ec213bbc32ce57d685d8e2c407cf3987bb`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c674717e06bf8cb25d5887393ef9568ee0ab6390966b9666808e836e9bd471d`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2227badcd9f5f2b70b3d2ffd1c18887498f413c07802bfb334e8dc7b2d2acc`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9f3b5e90a2e6028cf194e870b24a7158f875f18b81f4f9137a5db3ea1f79ac`  
		Last Modified: Thu, 16 Nov 2023 03:11:23 GMT  
		Size: 25.5 MB (25536225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7811a5416dcd19193a5b3ab9327607bf845f7ff77f95d3e20abdfb7435c32ae0`  
		Last Modified: Thu, 16 Nov 2023 03:11:16 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5931209e960a94616639ea72e4d3ad9dc9cb554790ce930152c73bdc1449c034`  
		Last Modified: Thu, 16 Nov 2023 03:11:16 GMT  
		Size: 266.6 KB (266600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a70f603a2fb4e76edd3165b62a179fb8f6410e265f5ae4a3732ee68e610034b`  
		Last Modified: Tue, 05 Dec 2023 20:38:48 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e37840dec3a6665ce48520be8b2c51b654359765bee5ab0780ee74746f0eb2`  
		Last Modified: Tue, 05 Dec 2023 20:39:08 GMT  
		Size: 69.3 MB (69342960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d16ae54757acda093616d24735d4c92d4676649bec49807fc35de90d15e15c`  
		Last Modified: Tue, 05 Dec 2023 20:38:48 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5744d01eddd2ef9d9673fdb0f0e48203fad1b01f2b14899a3ec6393c4548e75`  
		Last Modified: Tue, 05 Dec 2023 21:02:23 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35bb848667aa413b6ce6c309a4c2169635b0740dc335b9b39413a00627c01ab`  
		Last Modified: Tue, 05 Dec 2023 21:02:21 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54630e9807bbb8995ce52459e6e3c8d818351c481e0ce29280570e90d0138d33`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f15ec018ec91e33ee96d4f0e6b66d9edb40b185a13f91d16f12d0bf682ab08b`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79cc8b934303f209cd48271252cb46966445a1099aac277ae4caf120af718ab`  
		Last Modified: Fri, 08 Dec 2023 20:23:49 GMT  
		Size: 1.7 MB (1677815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224f75043e75fb7c85d3daec88a29069c6ff40b8feeaa26bac868d524758955`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-windowsservercore`

```console
$ docker pull caddy@sha256:23526c514f90e81e3b94593ed41182252a81ba946c70cf1d2638381f84849d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.5122; amd64
	-	windows version 10.0.20348.2113; amd64

### `caddy:2.7-windowsservercore` - windows version 10.0.17763.5122; amd64

```console
$ docker pull caddy@sha256:3d281f8c1d34b38abb3b5ca4ff98d70312daad9b0654a470374d0447a69a3ccf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073448315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e423604e6f05b59d8afa51e2d09a8fc11e1ac3353a126e3ce73b1c2bc65872b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:16:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:16:25 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:17:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:17:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:17:34 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:17:35 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:17:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:17:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:17:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:17:41 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:17:43 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:18:34 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:18:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09e9b6b38c0082853f1d6caa4d3536344a04da2aa5b674837aba8781b265e0d`  
		Last Modified: Fri, 08 Dec 2023 20:22:45 GMT  
		Size: 462.7 KB (462693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb778801cf9547a5b9021d3090bd8e4fc05f09e3aed56b6950dcbd044211d3f`  
		Last Modified: Fri, 08 Dec 2023 20:22:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ec815279848293cd980ed43a496bf4d3e8f8035f8d46dd1a3278e02c4558a8`  
		Last Modified: Fri, 08 Dec 2023 20:22:46 GMT  
		Size: 15.3 MB (15274633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9671feff108f8e0d8be270b64952394b3eaf7d16a7e9163cffc500ad3a42bd17`  
		Last Modified: Fri, 08 Dec 2023 20:22:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44f97706c45d8ebb4578d93d6c1cb5ecc4625f2f78fa40f25f9e72af014449a`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7b5732d0f0e4f61cac2e09f77054657b1bfc21c56b5b4b842e96ee7de3d45d`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348bbb9a26a300473cbb347ce3e405736e7a71ef7d2e67068452760fe4a1a67e`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4dc80dd8b7091a5cb553a95c06fa14380bf94a6f80467e3d7a36cb649fce8c`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6e2ab9cd2c6c903f643bcab22655dc93ec72fcc2f748a47375e2209580eed8`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a498a93a315d79030214cb59d847ede547dfc1159616120a3b48f2b1585bccfc`  
		Last Modified: Fri, 08 Dec 2023 20:22:40 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a7d0f8e26a8dd06b83bb38bfecf51f24ec1456947f459528e71b2544d13f5`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0da3c95480c1f76c862487e0683bed75c660c5cce3e3864677b8c956228e64`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1712e0793bc7067adabbb602cf9eaf0e6ab60f33be0b2b10282325884270ab07`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26aa77bbc553e8bf9318552da7ffe35258b387e04151dd211a006f50cb57a6`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e384f6873d9619640183b8c67671c94c80eb3725ac52c312de84b314b2cd4c53`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7ecef2ca51e4738a30164e40d773f9bfcc9a55bda13a00745349db1618fbf0`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29866626f3b37691b2e593b7ad8a6d3f6e916d9ca428c22e1b3834e568c605c9`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dff7ab50f452876c91da33fe48a0e1409de6cbb0ffca4e1aefa68caa5722d01`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 256.7 KB (256705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55865895b10a6247b60406c70eaa3584e7904512f0092bd7d9013bd9fe64c740`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-windowsservercore` - windows version 10.0.20348.2113; amd64

```console
$ docker pull caddy@sha256:cca2801fca8e41625ec6c3c42ee17cc76b64320f93ec2c37999b29b5f9ff0747
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1902845713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ad0d44150328d8253edf3d339d33f508e3a25395c8fd773d2d2fe5966eb244`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:19:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:19:10 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:19:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:19:34 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:19:35 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:19:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:19:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:19:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:19:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:19:43 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:19:44 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:19:58 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:19:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9e496904b6bbc7ce10b08f4c5c00b922d19bb8ebfca4735ba504c9ca77dd2b`  
		Last Modified: Fri, 08 Dec 2023 20:23:12 GMT  
		Size: 474.4 KB (474429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d370d88e3c2ee411f6f86dd892eba2c381cf5706823fcf82fec94a47d7d3bb4`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1861a873425170bdbe2b563cd2b9584401a7be0e3d9a6ceac998eef4eab482ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:13 GMT  
		Size: 15.3 MB (15274241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e17c8887831a9d0a255eb44daaaedffc1bb98b51fc0177786dd130c85034006`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2595203a1e7cbe5c30c3a77633ff7b832c6f07580e688e7c2bc89b5442e72ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b5a75922e76c5c96d069952df83b51d1243d2d6955db5b45dd7b63aea2b3a1`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bbe845ab80dc71320eea94c3d56888074ea930dc6fbe934c60e6c801e9cee3`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74052a6ffee1242926db0907e5406b7e5d81e181d3c9c266d381aaf221bf0252`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbd2ebe3b760156655b6475d7ff52b549e20b5115cf815016c902f834bf3f14`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5945b936f7903435999bc26916fd896f5c645c5b70834243317e66b14d7c2d97`  
		Last Modified: Fri, 08 Dec 2023 20:23:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4345b37fb7af089771ba8cf5542de3045ebb0f1d247ea038535504b320c4ac2c`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12593e8f188e5024af21891d9f3141bc5b85d9e2e9e2b61d7c2634f9f491b9a4`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3632692d5118ec05512cfb67c4aa09a8dfdfe1e40467dfc5ee8e5d2e9a349b2a`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e694808297bceaf6299316f20be2a78e4d2eef8a2ca455dd79ce544cf0a00e66`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258e53ea4c6d9b42de13f722ade5338a5393993985f05ca5b438982dde948654`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20692d7b4da06a40fca6c59bffc5e13dc0a0ffc429f70ed8701dc1d5d8c087fd`  
		Last Modified: Fri, 08 Dec 2023 20:23:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f686dbb1484378b8f73bbbfac32eb04d8f9a6b2b3f4db7d17c1f997941475a7f`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84003630e1340399082b07e0df6cb438545136bc3f0c134d52e8fe9d878e7239`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 292.2 KB (292197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9991bbf8fb125121b7478726325dcb657bfbeb24af279019b7b2f7ac0c404f7`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-windowsservercore-1809`

```console
$ docker pull caddy@sha256:67a59b537826dfa0019b55a7c113d5bdd826062754543ae24cccdcf2a558d407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `caddy:2.7-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull caddy@sha256:3d281f8c1d34b38abb3b5ca4ff98d70312daad9b0654a470374d0447a69a3ccf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073448315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e423604e6f05b59d8afa51e2d09a8fc11e1ac3353a126e3ce73b1c2bc65872b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:16:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:16:25 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:17:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:17:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:17:34 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:17:35 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:17:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:17:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:17:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:17:41 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:17:43 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:18:34 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:18:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09e9b6b38c0082853f1d6caa4d3536344a04da2aa5b674837aba8781b265e0d`  
		Last Modified: Fri, 08 Dec 2023 20:22:45 GMT  
		Size: 462.7 KB (462693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb778801cf9547a5b9021d3090bd8e4fc05f09e3aed56b6950dcbd044211d3f`  
		Last Modified: Fri, 08 Dec 2023 20:22:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ec815279848293cd980ed43a496bf4d3e8f8035f8d46dd1a3278e02c4558a8`  
		Last Modified: Fri, 08 Dec 2023 20:22:46 GMT  
		Size: 15.3 MB (15274633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9671feff108f8e0d8be270b64952394b3eaf7d16a7e9163cffc500ad3a42bd17`  
		Last Modified: Fri, 08 Dec 2023 20:22:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44f97706c45d8ebb4578d93d6c1cb5ecc4625f2f78fa40f25f9e72af014449a`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7b5732d0f0e4f61cac2e09f77054657b1bfc21c56b5b4b842e96ee7de3d45d`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348bbb9a26a300473cbb347ce3e405736e7a71ef7d2e67068452760fe4a1a67e`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4dc80dd8b7091a5cb553a95c06fa14380bf94a6f80467e3d7a36cb649fce8c`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6e2ab9cd2c6c903f643bcab22655dc93ec72fcc2f748a47375e2209580eed8`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a498a93a315d79030214cb59d847ede547dfc1159616120a3b48f2b1585bccfc`  
		Last Modified: Fri, 08 Dec 2023 20:22:40 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a7d0f8e26a8dd06b83bb38bfecf51f24ec1456947f459528e71b2544d13f5`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0da3c95480c1f76c862487e0683bed75c660c5cce3e3864677b8c956228e64`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1712e0793bc7067adabbb602cf9eaf0e6ab60f33be0b2b10282325884270ab07`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26aa77bbc553e8bf9318552da7ffe35258b387e04151dd211a006f50cb57a6`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e384f6873d9619640183b8c67671c94c80eb3725ac52c312de84b314b2cd4c53`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7ecef2ca51e4738a30164e40d773f9bfcc9a55bda13a00745349db1618fbf0`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29866626f3b37691b2e593b7ad8a6d3f6e916d9ca428c22e1b3834e568c605c9`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dff7ab50f452876c91da33fe48a0e1409de6cbb0ffca4e1aefa68caa5722d01`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 256.7 KB (256705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55865895b10a6247b60406c70eaa3584e7904512f0092bd7d9013bd9fe64c740`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:0726791503ced6bf9bdc5b322a8082762fb4ca97438a2c8fb49d0e80f06838ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `caddy:2.7-windowsservercore-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull caddy@sha256:cca2801fca8e41625ec6c3c42ee17cc76b64320f93ec2c37999b29b5f9ff0747
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1902845713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ad0d44150328d8253edf3d339d33f508e3a25395c8fd773d2d2fe5966eb244`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:19:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:19:10 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:19:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:19:34 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:19:35 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:19:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:19:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:19:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:19:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:19:43 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:19:44 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:19:58 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:19:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9e496904b6bbc7ce10b08f4c5c00b922d19bb8ebfca4735ba504c9ca77dd2b`  
		Last Modified: Fri, 08 Dec 2023 20:23:12 GMT  
		Size: 474.4 KB (474429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d370d88e3c2ee411f6f86dd892eba2c381cf5706823fcf82fec94a47d7d3bb4`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1861a873425170bdbe2b563cd2b9584401a7be0e3d9a6ceac998eef4eab482ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:13 GMT  
		Size: 15.3 MB (15274241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e17c8887831a9d0a255eb44daaaedffc1bb98b51fc0177786dd130c85034006`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2595203a1e7cbe5c30c3a77633ff7b832c6f07580e688e7c2bc89b5442e72ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b5a75922e76c5c96d069952df83b51d1243d2d6955db5b45dd7b63aea2b3a1`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bbe845ab80dc71320eea94c3d56888074ea930dc6fbe934c60e6c801e9cee3`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74052a6ffee1242926db0907e5406b7e5d81e181d3c9c266d381aaf221bf0252`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbd2ebe3b760156655b6475d7ff52b549e20b5115cf815016c902f834bf3f14`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5945b936f7903435999bc26916fd896f5c645c5b70834243317e66b14d7c2d97`  
		Last Modified: Fri, 08 Dec 2023 20:23:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4345b37fb7af089771ba8cf5542de3045ebb0f1d247ea038535504b320c4ac2c`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12593e8f188e5024af21891d9f3141bc5b85d9e2e9e2b61d7c2634f9f491b9a4`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3632692d5118ec05512cfb67c4aa09a8dfdfe1e40467dfc5ee8e5d2e9a349b2a`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e694808297bceaf6299316f20be2a78e4d2eef8a2ca455dd79ce544cf0a00e66`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258e53ea4c6d9b42de13f722ade5338a5393993985f05ca5b438982dde948654`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20692d7b4da06a40fca6c59bffc5e13dc0a0ffc429f70ed8701dc1d5d8c087fd`  
		Last Modified: Fri, 08 Dec 2023 20:23:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f686dbb1484378b8f73bbbfac32eb04d8f9a6b2b3f4db7d17c1f997941475a7f`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84003630e1340399082b07e0df6cb438545136bc3f0c134d52e8fe9d878e7239`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 292.2 KB (292197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9991bbf8fb125121b7478726325dcb657bfbeb24af279019b7b2f7ac0c404f7`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6`

```console
$ docker pull caddy@sha256:e523a9bc9e19fb96a082b4d83ebae2ce6267f56f2b7b4ac462135ebc51f68e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5122; amd64
	-	windows version 10.0.20348.2113; amd64

### `caddy:2.7.6` - linux; amd64

```console
$ docker pull caddy@sha256:7b8b4b0a4784433bd53271ff8f27d0940f96b1e633bb69b27d2c9ac5a293536a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18467236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657b947906e764d7ff65a638b958cb7f84b3754e49ede071620658385e743168`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:32:06 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:39:38 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:39:38 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:39:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:39:41 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:39:41 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:39:41 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:39:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:39:42 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:39:42 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:39:42 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:39:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08886dfc0722c4ed2cb6a70c285a33fe35aec069435868488356dde320b4d21c`  
		Last Modified: Fri, 01 Dec 2023 06:32:30 GMT  
		Size: 350.8 KB (350845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd2155878b9ec9d659128d039d90b8a50369fe85c88f64a597b6a9cd9441c1b`  
		Last Modified: Fri, 08 Dec 2023 20:40:01 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7343593237d1bd5fb218804e360a7a8c4d94d7af8da4eb1a72fbaf48fab9ce2`  
		Last Modified: Fri, 08 Dec 2023 20:40:03 GMT  
		Size: 14.7 MB (14706441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6` - linux; arm variant v6

```console
$ docker pull caddy@sha256:fe42da7df688686dab79fb02be7f13aae32c9a9f84eec3b28b634cc48d5a7346
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17423030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f95b690a9e892f56dbf3fd455d714c2d22ebd35967fdc770fb704c870eeffc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:39:01 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:07:47 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:07:47 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:07:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:07:50 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:07:50 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:07:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:07:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:07:51 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:07:51 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc24e4ccf558b6e992efaaa7a735322be11fe99ce19e722eee6ae70bb76515d`  
		Last Modified: Fri, 01 Dec 2023 00:39:21 GMT  
		Size: 347.6 KB (347632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775b4c8558ad1bf8d7568fc741be39ee2a28ecdd33f84ed7597b6192873a81a`  
		Last Modified: Fri, 08 Dec 2023 20:08:10 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbf57a0db316ab6b42386b0221d652cc4f9d9d597206ce1d4e9bfd5ba0f7777`  
		Last Modified: Fri, 08 Dec 2023 20:08:12 GMT  
		Size: 13.9 MB (13920999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6` - linux; arm variant v7

```console
$ docker pull caddy@sha256:cf486c3cc2b7d7cc0bdfc8db52605e6a533c0528e717b2ccd6e9779713d72229
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17146731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68a807660343335d38b999c8c1b687f5ec5c882c6f5180e13281152b030f103`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:19:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:16:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:16:22 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:16:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:16:25 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:16:26 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:16:27 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:16:27 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:16:28 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:16:28 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:16:28 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:16:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803b34e1f84b29ca968d2fbf85c278608566c34dfd1742e088c6483685957029`  
		Last Modified: Fri, 01 Dec 2023 03:19:48 GMT  
		Size: 344.5 KB (344464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de504bcc2429a4454910b605f8bb2f6eec4cad953044e48d02a7d51542b7266f`  
		Last Modified: Fri, 08 Dec 2023 20:16:53 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73099274a85e30e93cb0e71106c443fd9a5b923ef43adabf808db6a58db9ad8b`  
		Last Modified: Fri, 08 Dec 2023 20:16:56 GMT  
		Size: 13.9 MB (13893732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:71069b6f75345cd8b5e4841d92dcaebb4fa2acf454074eeb2c571517ac3671cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae18940ab920c723e970d89fde606b552e5b39f5fa33535cb6c7be09b6cff763`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:11:08 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 19:55:15 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 19:55:16 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 19:55:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 19:55:17 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 19:55:17 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 19:55:17 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 80
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 443
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 19:55:18 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 19:55:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e383270d6915b6b427f49a75d657d5a0403fcd47a5f89cd30e85143ca54c22`  
		Last Modified: Fri, 01 Dec 2023 03:11:28 GMT  
		Size: 360.7 KB (360655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f87e6bdbafc6710a3ed7bfbb4bb134e8d93bea992ab895c653cac0779389396`  
		Last Modified: Fri, 08 Dec 2023 19:55:35 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874486d3ac5891d4df17819e02e1cdd3775748effa24bc53645cd2db841a0837`  
		Last Modified: Fri, 08 Dec 2023 19:55:36 GMT  
		Size: 13.6 MB (13568967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6` - linux; ppc64le

```console
$ docker pull caddy@sha256:9991e527a64c1d20422e24e141a57efec5365c7bcd68662808b0ea23da815b3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17051913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274840ad1c2fe6344d298e9d6242bde6e602b3444a071cfe45d3db4360d193b4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:42:19 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:22:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:22:14 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:22:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:22:19 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:22:19 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:22:19 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:22:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:22:20 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:22:22 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:22:22 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:22:23 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:22:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:22:24 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:22:24 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:22:25 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:22:25 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:22:26 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:22:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce4bc2907f69809c3086f118895d7e5c8683349557239c0ce79dfbda0ce3768`  
		Last Modified: Fri, 01 Dec 2023 05:44:17 GMT  
		Size: 362.2 KB (362185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3c2787bdbaa50fce90e65038b2dbc9850d2fff68d5e731bcdb83c71ede912b`  
		Last Modified: Fri, 08 Dec 2023 20:22:53 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ce50c6341ede9fe5f61cc3a75eb534b7dd1172b7e88c015862cb9351c91ca1`  
		Last Modified: Fri, 08 Dec 2023 20:22:55 GMT  
		Size: 13.3 MB (13333877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6` - linux; s390x

```console
$ docker pull caddy@sha256:f8db25c8783258ee73a7ab061dbcb53f5229be2510ab4c72cbb6fe5292fdd1a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17818230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4782f6a3e2f343e87b335a56846d9ae67a4a5aded358a8501a4fb5a076e92cef`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:22:31 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 19:57:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 19:57:07 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 19:57:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 19:57:11 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 19:57:11 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 19:57:13 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 19:57:13 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 19:57:13 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 19:57:13 GMT
EXPOSE 80
# Fri, 08 Dec 2023 19:57:13 GMT
EXPOSE 443
# Fri, 08 Dec 2023 19:57:14 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 19:57:14 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 19:57:14 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 19:57:14 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20bbe0abb0a3f63718aa78742832077ad86b8ae86d70ce3ebcece342ec022c6`  
		Last Modified: Fri, 01 Dec 2023 08:23:07 GMT  
		Size: 354.9 KB (354948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa042ad4816c33e4f907bbf008abef2397efe2b3fc378430b2b925663a088370`  
		Last Modified: Fri, 08 Dec 2023 19:57:43 GMT  
		Size: 7.5 KB (7526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ceec9a3d819911fec4d039d31e2e3e38214fa45cb8384e8f047b5588724355`  
		Last Modified: Fri, 08 Dec 2023 19:57:45 GMT  
		Size: 14.2 MB (14238302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6` - windows version 10.0.17763.5122; amd64

```console
$ docker pull caddy@sha256:3d281f8c1d34b38abb3b5ca4ff98d70312daad9b0654a470374d0447a69a3ccf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073448315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e423604e6f05b59d8afa51e2d09a8fc11e1ac3353a126e3ce73b1c2bc65872b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:16:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:16:25 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:17:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:17:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:17:34 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:17:35 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:17:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:17:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:17:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:17:41 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:17:43 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:18:34 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:18:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09e9b6b38c0082853f1d6caa4d3536344a04da2aa5b674837aba8781b265e0d`  
		Last Modified: Fri, 08 Dec 2023 20:22:45 GMT  
		Size: 462.7 KB (462693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb778801cf9547a5b9021d3090bd8e4fc05f09e3aed56b6950dcbd044211d3f`  
		Last Modified: Fri, 08 Dec 2023 20:22:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ec815279848293cd980ed43a496bf4d3e8f8035f8d46dd1a3278e02c4558a8`  
		Last Modified: Fri, 08 Dec 2023 20:22:46 GMT  
		Size: 15.3 MB (15274633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9671feff108f8e0d8be270b64952394b3eaf7d16a7e9163cffc500ad3a42bd17`  
		Last Modified: Fri, 08 Dec 2023 20:22:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44f97706c45d8ebb4578d93d6c1cb5ecc4625f2f78fa40f25f9e72af014449a`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7b5732d0f0e4f61cac2e09f77054657b1bfc21c56b5b4b842e96ee7de3d45d`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348bbb9a26a300473cbb347ce3e405736e7a71ef7d2e67068452760fe4a1a67e`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4dc80dd8b7091a5cb553a95c06fa14380bf94a6f80467e3d7a36cb649fce8c`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6e2ab9cd2c6c903f643bcab22655dc93ec72fcc2f748a47375e2209580eed8`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a498a93a315d79030214cb59d847ede547dfc1159616120a3b48f2b1585bccfc`  
		Last Modified: Fri, 08 Dec 2023 20:22:40 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a7d0f8e26a8dd06b83bb38bfecf51f24ec1456947f459528e71b2544d13f5`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0da3c95480c1f76c862487e0683bed75c660c5cce3e3864677b8c956228e64`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1712e0793bc7067adabbb602cf9eaf0e6ab60f33be0b2b10282325884270ab07`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26aa77bbc553e8bf9318552da7ffe35258b387e04151dd211a006f50cb57a6`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e384f6873d9619640183b8c67671c94c80eb3725ac52c312de84b314b2cd4c53`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7ecef2ca51e4738a30164e40d773f9bfcc9a55bda13a00745349db1618fbf0`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29866626f3b37691b2e593b7ad8a6d3f6e916d9ca428c22e1b3834e568c605c9`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dff7ab50f452876c91da33fe48a0e1409de6cbb0ffca4e1aefa68caa5722d01`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 256.7 KB (256705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55865895b10a6247b60406c70eaa3584e7904512f0092bd7d9013bd9fe64c740`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6` - windows version 10.0.20348.2113; amd64

```console
$ docker pull caddy@sha256:cca2801fca8e41625ec6c3c42ee17cc76b64320f93ec2c37999b29b5f9ff0747
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1902845713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ad0d44150328d8253edf3d339d33f508e3a25395c8fd773d2d2fe5966eb244`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:19:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:19:10 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:19:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:19:34 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:19:35 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:19:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:19:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:19:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:19:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:19:43 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:19:44 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:19:58 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:19:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9e496904b6bbc7ce10b08f4c5c00b922d19bb8ebfca4735ba504c9ca77dd2b`  
		Last Modified: Fri, 08 Dec 2023 20:23:12 GMT  
		Size: 474.4 KB (474429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d370d88e3c2ee411f6f86dd892eba2c381cf5706823fcf82fec94a47d7d3bb4`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1861a873425170bdbe2b563cd2b9584401a7be0e3d9a6ceac998eef4eab482ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:13 GMT  
		Size: 15.3 MB (15274241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e17c8887831a9d0a255eb44daaaedffc1bb98b51fc0177786dd130c85034006`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2595203a1e7cbe5c30c3a77633ff7b832c6f07580e688e7c2bc89b5442e72ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b5a75922e76c5c96d069952df83b51d1243d2d6955db5b45dd7b63aea2b3a1`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bbe845ab80dc71320eea94c3d56888074ea930dc6fbe934c60e6c801e9cee3`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74052a6ffee1242926db0907e5406b7e5d81e181d3c9c266d381aaf221bf0252`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbd2ebe3b760156655b6475d7ff52b549e20b5115cf815016c902f834bf3f14`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5945b936f7903435999bc26916fd896f5c645c5b70834243317e66b14d7c2d97`  
		Last Modified: Fri, 08 Dec 2023 20:23:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4345b37fb7af089771ba8cf5542de3045ebb0f1d247ea038535504b320c4ac2c`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12593e8f188e5024af21891d9f3141bc5b85d9e2e9e2b61d7c2634f9f491b9a4`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3632692d5118ec05512cfb67c4aa09a8dfdfe1e40467dfc5ee8e5d2e9a349b2a`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e694808297bceaf6299316f20be2a78e4d2eef8a2ca455dd79ce544cf0a00e66`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258e53ea4c6d9b42de13f722ade5338a5393993985f05ca5b438982dde948654`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20692d7b4da06a40fca6c59bffc5e13dc0a0ffc429f70ed8701dc1d5d8c087fd`  
		Last Modified: Fri, 08 Dec 2023 20:23:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f686dbb1484378b8f73bbbfac32eb04d8f9a6b2b3f4db7d17c1f997941475a7f`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84003630e1340399082b07e0df6cb438545136bc3f0c134d52e8fe9d878e7239`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 292.2 KB (292197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9991bbf8fb125121b7478726325dcb657bfbeb24af279019b7b2f7ac0c404f7`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-alpine`

```console
$ docker pull caddy@sha256:eabac2898cf9fc7dc94d3fb03ac84c9c923aa6cc6f04874937d2f525e0d2f006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.7.6-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:7b8b4b0a4784433bd53271ff8f27d0940f96b1e633bb69b27d2c9ac5a293536a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18467236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657b947906e764d7ff65a638b958cb7f84b3754e49ede071620658385e743168`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:32:06 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:39:38 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:39:38 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:39:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:39:41 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:39:41 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:39:41 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:39:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:39:42 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:39:42 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:39:42 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:39:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08886dfc0722c4ed2cb6a70c285a33fe35aec069435868488356dde320b4d21c`  
		Last Modified: Fri, 01 Dec 2023 06:32:30 GMT  
		Size: 350.8 KB (350845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd2155878b9ec9d659128d039d90b8a50369fe85c88f64a597b6a9cd9441c1b`  
		Last Modified: Fri, 08 Dec 2023 20:40:01 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7343593237d1bd5fb218804e360a7a8c4d94d7af8da4eb1a72fbaf48fab9ce2`  
		Last Modified: Fri, 08 Dec 2023 20:40:03 GMT  
		Size: 14.7 MB (14706441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:fe42da7df688686dab79fb02be7f13aae32c9a9f84eec3b28b634cc48d5a7346
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17423030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f95b690a9e892f56dbf3fd455d714c2d22ebd35967fdc770fb704c870eeffc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:39:01 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:07:47 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:07:47 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:07:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:07:50 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:07:50 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:07:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:07:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:07:51 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:07:51 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc24e4ccf558b6e992efaaa7a735322be11fe99ce19e722eee6ae70bb76515d`  
		Last Modified: Fri, 01 Dec 2023 00:39:21 GMT  
		Size: 347.6 KB (347632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775b4c8558ad1bf8d7568fc741be39ee2a28ecdd33f84ed7597b6192873a81a`  
		Last Modified: Fri, 08 Dec 2023 20:08:10 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbf57a0db316ab6b42386b0221d652cc4f9d9d597206ce1d4e9bfd5ba0f7777`  
		Last Modified: Fri, 08 Dec 2023 20:08:12 GMT  
		Size: 13.9 MB (13920999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:cf486c3cc2b7d7cc0bdfc8db52605e6a533c0528e717b2ccd6e9779713d72229
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17146731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68a807660343335d38b999c8c1b687f5ec5c882c6f5180e13281152b030f103`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:19:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:16:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:16:22 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:16:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:16:25 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:16:26 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:16:27 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:16:27 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:16:28 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:16:28 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:16:28 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:16:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803b34e1f84b29ca968d2fbf85c278608566c34dfd1742e088c6483685957029`  
		Last Modified: Fri, 01 Dec 2023 03:19:48 GMT  
		Size: 344.5 KB (344464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de504bcc2429a4454910b605f8bb2f6eec4cad953044e48d02a7d51542b7266f`  
		Last Modified: Fri, 08 Dec 2023 20:16:53 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73099274a85e30e93cb0e71106c443fd9a5b923ef43adabf808db6a58db9ad8b`  
		Last Modified: Fri, 08 Dec 2023 20:16:56 GMT  
		Size: 13.9 MB (13893732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:71069b6f75345cd8b5e4841d92dcaebb4fa2acf454074eeb2c571517ac3671cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae18940ab920c723e970d89fde606b552e5b39f5fa33535cb6c7be09b6cff763`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:11:08 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 19:55:15 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 19:55:16 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 19:55:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 19:55:17 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 19:55:17 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 19:55:17 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 80
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 443
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 19:55:18 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 19:55:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e383270d6915b6b427f49a75d657d5a0403fcd47a5f89cd30e85143ca54c22`  
		Last Modified: Fri, 01 Dec 2023 03:11:28 GMT  
		Size: 360.7 KB (360655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f87e6bdbafc6710a3ed7bfbb4bb134e8d93bea992ab895c653cac0779389396`  
		Last Modified: Fri, 08 Dec 2023 19:55:35 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874486d3ac5891d4df17819e02e1cdd3775748effa24bc53645cd2db841a0837`  
		Last Modified: Fri, 08 Dec 2023 19:55:36 GMT  
		Size: 13.6 MB (13568967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:9991e527a64c1d20422e24e141a57efec5365c7bcd68662808b0ea23da815b3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17051913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274840ad1c2fe6344d298e9d6242bde6e602b3444a071cfe45d3db4360d193b4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:42:19 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:22:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:22:14 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:22:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:22:19 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:22:19 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:22:19 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:22:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:22:20 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:22:22 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:22:22 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:22:23 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:22:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:22:24 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:22:24 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:22:25 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:22:25 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:22:26 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:22:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce4bc2907f69809c3086f118895d7e5c8683349557239c0ce79dfbda0ce3768`  
		Last Modified: Fri, 01 Dec 2023 05:44:17 GMT  
		Size: 362.2 KB (362185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3c2787bdbaa50fce90e65038b2dbc9850d2fff68d5e731bcdb83c71ede912b`  
		Last Modified: Fri, 08 Dec 2023 20:22:53 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ce50c6341ede9fe5f61cc3a75eb534b7dd1172b7e88c015862cb9351c91ca1`  
		Last Modified: Fri, 08 Dec 2023 20:22:55 GMT  
		Size: 13.3 MB (13333877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:f8db25c8783258ee73a7ab061dbcb53f5229be2510ab4c72cbb6fe5292fdd1a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17818230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4782f6a3e2f343e87b335a56846d9ae67a4a5aded358a8501a4fb5a076e92cef`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:22:31 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 19:57:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 19:57:07 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 19:57:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 19:57:11 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 19:57:11 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 19:57:13 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 19:57:13 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 19:57:13 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 19:57:13 GMT
EXPOSE 80
# Fri, 08 Dec 2023 19:57:13 GMT
EXPOSE 443
# Fri, 08 Dec 2023 19:57:14 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 19:57:14 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 19:57:14 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 19:57:14 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20bbe0abb0a3f63718aa78742832077ad86b8ae86d70ce3ebcece342ec022c6`  
		Last Modified: Fri, 01 Dec 2023 08:23:07 GMT  
		Size: 354.9 KB (354948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa042ad4816c33e4f907bbf008abef2397efe2b3fc378430b2b925663a088370`  
		Last Modified: Fri, 08 Dec 2023 19:57:43 GMT  
		Size: 7.5 KB (7526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ceec9a3d819911fec4d039d31e2e3e38214fa45cb8384e8f047b5588724355`  
		Last Modified: Fri, 08 Dec 2023 19:57:45 GMT  
		Size: 14.2 MB (14238302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder`

```console
$ docker pull caddy@sha256:1bad661ef08b648af7c9c79e708965d3a69434285f24de76111124fdf5d339d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5122; amd64
	-	windows version 10.0.20348.2113; amd64

### `caddy:2.7.6-builder` - linux; amd64

```console
$ docker pull caddy@sha256:64cc92d77653c256c9cde397fb221c57907a57b0fe04f4e83ab2f7123f7f9147
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76963251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccce7adcc2b72b984adc9e5dd37663d1e6e512e39657c41bed43c55b38f9bad9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:46:23 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 03:46:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:25:52 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:26:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:26:02 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:26:02 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:26:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:26:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:26:03 GMT
WORKDIR /go
# Tue, 05 Dec 2023 20:48:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 20:48:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:39:46 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:39:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:39:46 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 20:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 20:39:47 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 20:39:47 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5501dced60f86be38cc73d3c038f7db4afeee65726f7e422aacf09244539ebf1`  
		Last Modified: Fri, 01 Dec 2023 03:50:39 GMT  
		Size: 284.7 KB (284697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63d189496f5f03c835c9c85df2db6920546d36a1701f6b5ad15f800c671605d`  
		Last Modified: Tue, 05 Dec 2023 20:31:27 GMT  
		Size: 67.0 MB (67003308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aeb88dd0f3e06a57abc08c781b85c89d138194918c469aea9a1bed9753d2ed0`  
		Last Modified: Tue, 05 Dec 2023 20:31:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40ff2505fd8d96e76bddb63b05c2d42815db1dabe0093ec8f8f53be403b0d01`  
		Last Modified: Tue, 05 Dec 2023 20:49:17 GMT  
		Size: 5.0 MB (4970029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ba23d637be879f93c12d4e6d077eb636688fa34e5d637f1f9a2f0a28509f0d`  
		Last Modified: Fri, 08 Dec 2023 20:40:19 GMT  
		Size: 1.3 MB (1302232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57ad5b5be9e26b4f05c8402814544f231f87d6a736a05320421e0ce2e623f04`  
		Last Modified: Fri, 08 Dec 2023 20:40:19 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:cd2d4a5ddcdef2492b7b440240d2e3beffa1695c0a1273227efdbc97a0fddc86
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75411895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed519bbe9039d7d32e60f9e1c959613953c4508dc6dd1506a355f0e0fd39bbe7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:53:48 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 00:53:48 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:49:18 GMT
ENV GOLANG_VERSION=1.21.5
# Sat, 09 Dec 2023 01:49:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	elif [ "$arch" = 'armv7' ]; then 		[ -s /usr/local/go/go.env ]; 		before="$(go env GOARM)"; [ "$before" != '7' ]; 		{ 			echo; 			echo '# https://github.com/docker-library/golang/issues/494'; 			echo 'GOARM=7'; 		} >> /usr/local/go/go.env; 		after="$(go env GOARM)"; [ "$after" = '7' ]; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Sat, 09 Dec 2023 01:49:51 GMT
ENV GOTOOLCHAIN=local
# Sat, 09 Dec 2023 01:49:51 GMT
ENV GOPATH=/go
# Sat, 09 Dec 2023 01:49:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 01:49:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Sat, 09 Dec 2023 01:49:52 GMT
WORKDIR /go
# Sat, 09 Dec 2023 02:08:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 09 Dec 2023 02:08:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 09 Dec 2023 02:08:59 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 09 Dec 2023 02:08:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 09 Dec 2023 02:08:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 09 Dec 2023 02:09:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 09 Dec 2023 02:09:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 09 Dec 2023 02:09:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e7ba0492eb25e7f21078441d7cdc65088836bc1984bc4a14cd3e9cd75cbf32`  
		Last Modified: Fri, 01 Dec 2023 01:00:23 GMT  
		Size: 284.9 KB (284884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbf3e566edb99ecb0ecb757d0f571633d7d822bf31896dd76a40ff9d89e98c0`  
		Last Modified: Sat, 09 Dec 2023 01:53:04 GMT  
		Size: 65.8 MB (65764277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e170d213450f3f3c66f85329ded2a75a6b38e5b51cfe01f2ad9d2cc2aab61079`  
		Last Modified: Sat, 09 Dec 2023 01:52:51 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612473e16b229d3c58615a469f9ca073ec9dc483d79cd7bb87479eea58ee5454`  
		Last Modified: Sat, 09 Dec 2023 02:09:20 GMT  
		Size: 5.0 MB (4966653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ed572067dfce272b021aee6f0cd14272e2a1157f0cf11ad00004a5c9354bc0`  
		Last Modified: Sat, 09 Dec 2023 02:09:19 GMT  
		Size: 1.2 MB (1248652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7608cc7cd78c6c2f18a53621dbd0b1746b9274ce1b35a8279b261816e41718ef`  
		Last Modified: Sat, 09 Dec 2023 02:09:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:7b8943fed6d62476c9dea44a16caea83fb6d540be101271d0974e0f2ed5a1567
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74707178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e459d7afebbd1af456db2bc6e8849445ca45f2586a9bbd0337ba314f570a177`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:44:57 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 08:44:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:58:01 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:58:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:58:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:58:16 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:58:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:58:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:58:17 GMT
WORKDIR /go
# Tue, 05 Dec 2023 21:22:31 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 21:22:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:16:31 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:16:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:16:32 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 20:16:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 20:16:34 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 20:16:34 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a824ff289f1a3c765a444079137b8b7f1cee80348faa53e1ba4c960b73ed2a`  
		Last Modified: Fri, 01 Dec 2023 08:49:42 GMT  
		Size: 284.1 KB (284079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4989177b4ed66b7e9f9e8c4bfce82720b582e24b735d6628effa75d81c5718fc`  
		Last Modified: Tue, 05 Dec 2023 21:04:43 GMT  
		Size: 65.8 MB (65764197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f9b58eae167c54d3faa3eeffd480cdae7e8b4841eb816a86cfdd01f8ae29ef`  
		Last Modified: Tue, 05 Dec 2023 21:04:29 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4cd1a3aab8fc02791b1e19f81b7de1bd691c10a7c942acc7e733221bf12888`  
		Last Modified: Tue, 05 Dec 2023 21:22:47 GMT  
		Size: 4.5 MB (4511237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c6a5bcaed596afac229d37cd822ea4770b06d4d3580d14a71d26e32136f1aa`  
		Last Modified: Fri, 08 Dec 2023 20:17:09 GMT  
		Size: 1.2 MB (1246093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c59154934645e7c4d44eda6d3d5ea9d4b32e23fbf7ccb7009cc54413ae815d`  
		Last Modified: Fri, 08 Dec 2023 20:17:09 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:3fce35ec600b6e48bb63c1b2d390b6d515a6f0e7355b582fcb347092222bdc37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73981648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3475cc52d42bfd049fb20d388ecf6c8482841b98a265b9fc09b60bc815011df9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:43:53 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 03:18:30 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:16:18 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:16:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:16:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:16:28 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:16:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:16:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:16:28 GMT
WORKDIR /go
# Tue, 05 Dec 2023 20:38:16 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 20:38:16 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 19:55:21 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 19:55:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 19:55:21 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 19:55:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 19:55:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 19:55:22 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a63ed24dc22a348b35d99b5ec9dc67ff66563b539875e5c8ab2d870b3991ac`  
		Last Modified: Fri, 01 Dec 2023 02:44:03 GMT  
		Size: 286.3 KB (286307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f00641dffc5c2a149049ee9046bb24cfc7de534b7495a0f27784a4fff0fadc`  
		Last Modified: Tue, 05 Dec 2023 20:21:00 GMT  
		Size: 64.1 MB (64094844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452682ba77e89fc55be3a168358f5f43bccad93ecdd3d53b4dec7fff6915128b`  
		Last Modified: Tue, 05 Dec 2023 20:20:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3fe1e12507f8c4a2731393eebfc5ab973aa344b0daceec525560b812b26f60`  
		Last Modified: Tue, 05 Dec 2023 20:38:33 GMT  
		Size: 5.1 MB (5068450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1568fb18f5eae3df776dd2fee8d447615d0f62601f82ebdb1bf2af5155bb83`  
		Last Modified: Fri, 08 Dec 2023 19:55:49 GMT  
		Size: 1.2 MB (1198450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15988851efd259492be8e7583025cb2b00f7477442c7be3e2d3dd97adbc39e76`  
		Last Modified: Fri, 08 Dec 2023 19:55:48 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:e21739ed4cecc54ebd496b12fa757f5901f3c0b45d211c0c5fa2ef551543c2d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74206507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed778e73218e8613cd2044f7eb703ec05bf43271d444ca5ffe77e053baa719c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:37:34 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 06:37:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:38:14 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:38:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:38:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:38:38 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:38:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:38:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:38:41 GMT
WORKDIR /go
# Tue, 05 Dec 2023 21:04:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 21:04:34 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:22:32 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:22:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:22:33 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 20:22:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 20:22:35 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 20:22:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692dbecd5e141c462ab06ef113ec964b525e7564d734890cc1d5b1dbf33ee34e`  
		Last Modified: Fri, 01 Dec 2023 06:43:30 GMT  
		Size: 286.7 KB (286661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc89a0f2d97ecfd4d20235e72227fc24aa79a64509fe9ea64702db658f2ad26d`  
		Last Modified: Tue, 05 Dec 2023 20:46:23 GMT  
		Size: 64.1 MB (64115804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d76f2c2e2bbb4190b1865ddafdc8cb88adee4c79d7d5ba23e69696e9610889`  
		Last Modified: Tue, 05 Dec 2023 20:46:11 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e0ec0f713ee657d6aa159fab65c05939480b5ca50a8e3dc4b1a9a6578160f7`  
		Last Modified: Tue, 05 Dec 2023 21:04:57 GMT  
		Size: 5.3 MB (5268970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbd7401349780157d6d930ec942f00b1d5404d31ae60bff5c7b41238cf8e3b1`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 1.2 MB (1186185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67206b5e4434d3211a98a71837832baed45e4fb0c03ff8dc204bc7762a8ab559`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; s390x

```console
$ docker pull caddy@sha256:bf201fa7da491e4decf9c0a638b9fbcb4b459d5b13bcc9a2f4c0fb4c583c609b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76101050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e2b3cda7ff391c43b985fdbd1c3515e69b6fbe94f8ea6c9a09749c147e491c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:14:49 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 08:14:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:44:16 GMT
ENV GOLANG_VERSION=1.21.5
# Sat, 09 Dec 2023 01:50:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	elif [ "$arch" = 'armv7' ]; then 		[ -s /usr/local/go/go.env ]; 		before="$(go env GOARM)"; [ "$before" != '7' ]; 		{ 			echo; 			echo '# https://github.com/docker-library/golang/issues/494'; 			echo 'GOARM=7'; 		} >> /usr/local/go/go.env; 		after="$(go env GOARM)"; [ "$after" = '7' ]; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Sat, 09 Dec 2023 01:50:41 GMT
ENV GOTOOLCHAIN=local
# Sat, 09 Dec 2023 01:50:41 GMT
ENV GOPATH=/go
# Sat, 09 Dec 2023 01:50:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 01:50:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Sat, 09 Dec 2023 01:50:42 GMT
WORKDIR /go
# Sat, 09 Dec 2023 02:12:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 09 Dec 2023 02:12:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 09 Dec 2023 02:12:31 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 09 Dec 2023 02:12:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 09 Dec 2023 02:12:31 GMT
ENV XCADDY_SETCAP=1
# Sat, 09 Dec 2023 02:12:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 09 Dec 2023 02:12:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 09 Dec 2023 02:12:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab563e8d41683e124df048aa9b564b0e8e1021e85213666971a015df51d5e48`  
		Last Modified: Fri, 01 Dec 2023 08:20:46 GMT  
		Size: 285.1 KB (285090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c541c9463bd8d06e97aa1b14ce0792cf2caf6ef8ddc7b046b21032b3390bee`  
		Last Modified: Sat, 09 Dec 2023 01:54:50 GMT  
		Size: 66.2 MB (66218593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236faa4ca6aed551be037e8e0a2312e72dedf504cdffa8d2015882df02c5b87e`  
		Last Modified: Sat, 09 Dec 2023 01:54:39 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee294f5771410ee01c59c398d0270a28f5ae4caff9abfa5339f1c54b1dc1ab5a`  
		Last Modified: Sat, 09 Dec 2023 02:12:56 GMT  
		Size: 5.1 MB (5116966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cbd016bf9fbfd249882a217530ca94dcac095e46620a64badd9bbfa6ae9ebe`  
		Last Modified: Sat, 09 Dec 2023 02:12:55 GMT  
		Size: 1.3 MB (1262386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b36774ae94aa93a3beb6e355ee08897437b53c870bc56fdc3047ce591cfa2ac`  
		Last Modified: Sat, 09 Dec 2023 02:12:55 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - windows version 10.0.17763.5122; amd64

```console
$ docker pull caddy@sha256:cdab1fd140455df0674bfedde2f4948b5289720efd10ff1301ce39bb60cd8daf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154297412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39391f7d87fac7b43f0ed0b59b1981b263a30d3397f5f5244adf81cb7627ba5a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 02:47:03 GMT
ENV GIT_VERSION=2.23.0
# Thu, 16 Nov 2023 02:47:04 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 16 Nov 2023 02:47:05 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 16 Nov 2023 02:47:06 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 16 Nov 2023 02:48:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 02:48:31 GMT
ENV GOPATH=C:\go
# Thu, 16 Nov 2023 02:49:41 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Dec 2023 20:18:04 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:21:11 GMT
RUN $url = 'https://dl.google.com/go/go1.21.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bbe603cde7c9dee658f45164b4d06de1eff6e6e6b800100824e7c00d56a9a92f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Dec 2023 20:21:13 GMT
WORKDIR C:\go
# Tue, 05 Dec 2023 20:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Dec 2023 20:59:30 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:20:06 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:20:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:21:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 08 Dec 2023 20:21:15 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e901367fac1450f509d3118ada9e004e3613844ebdf91861147a093483930a4`  
		Last Modified: Thu, 16 Nov 2023 03:11:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e08004205bd077d8f22b013c70dc2f10796c64fced1eb9927e0055daff2d05d`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebc5048afc68ef48e2f2136545e2cccf26bb29eb4926bf4259b370ad55b4e7a`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f50fe5c7ef21648f3eaa4304932877a116fcb910b8e9095c779a2fbe6d57f7e`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76fe0e37750041d4ede2a0ca3b5245cfe075c3eb2ee27d7ce72ee8c3d7b20cc`  
		Last Modified: Thu, 16 Nov 2023 03:12:00 GMT  
		Size: 25.5 MB (25537512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8097bb9b8778d15dbf89d899653bf1634ec17554e5d84ef1ccfcac8ebf86afe2`  
		Last Modified: Thu, 16 Nov 2023 03:11:53 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b542d31e914d67da86cc5701cdc282ab664dc1170507e3802e22ab3026436a90`  
		Last Modified: Thu, 16 Nov 2023 03:11:53 GMT  
		Size: 263.2 KB (263200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86acdf7d3955fb44136bac433a30ccbbb97863120f270af32659dd65446666c7`  
		Last Modified: Tue, 05 Dec 2023 20:39:22 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1abe126c354944b7db8aa724d8f757167f7c3b36d39f976ef3b1b0d1b1b65ab`  
		Last Modified: Tue, 05 Dec 2023 20:39:41 GMT  
		Size: 69.4 MB (69361283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6338af096e09067ad482a0f4a6df1d1eee5b5595a64ca5f367b94ce27903e284`  
		Last Modified: Tue, 05 Dec 2023 20:39:22 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0adc218b27ef5639384c060fb663de3bd74374279d3fd525aa281f63a754779`  
		Last Modified: Tue, 05 Dec 2023 21:02:06 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c21053b248805df7ad888734f5cd1df5a6b426111512d5a6b7530060e7f30b2`  
		Last Modified: Tue, 05 Dec 2023 21:02:03 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034eb8f336a0d8e998c3eef6834d07c072c0679ccd4fde02cc8787ed46c80b19`  
		Last Modified: Fri, 08 Dec 2023 20:23:31 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af9b0b53a037a76c1c2e0e3afbe4fad733bc634a5ca02d53055360d9b7e33b9`  
		Last Modified: Fri, 08 Dec 2023 20:23:31 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f653ab9a896e2a3cfaf147a9ebb6e2d23f453cc3f953ee19b27333ebbc66460b`  
		Last Modified: Fri, 08 Dec 2023 20:23:32 GMT  
		Size: 1.7 MB (1685700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed98b1069776f09873a216052d2bf114c714b8269e4235d0aee375a2b0b7962`  
		Last Modified: Fri, 08 Dec 2023 20:23:31 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - windows version 10.0.20348.2113; amd64

```console
$ docker pull caddy@sha256:b1d94a17104c4814aa7672316e4c713aefcdfa6ffd19043f4111784c09931cda
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1983623336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61ba19fe8fdfa90a532d1f355b356c651a2921264135f6417c72193a5f37396`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 02:43:34 GMT
ENV GIT_VERSION=2.23.0
# Thu, 16 Nov 2023 02:43:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 16 Nov 2023 02:43:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 16 Nov 2023 02:43:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 16 Nov 2023 02:44:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 02:44:11 GMT
ENV GOPATH=C:\go
# Thu, 16 Nov 2023 02:44:30 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Dec 2023 20:15:35 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:17:49 GMT
RUN $url = 'https://dl.google.com/go/go1.21.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bbe603cde7c9dee658f45164b4d06de1eff6e6e6b800100824e7c00d56a9a92f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Dec 2023 20:17:50 GMT
WORKDIR C:\go
# Tue, 05 Dec 2023 21:00:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Dec 2023 21:00:58 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:21:33 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:21:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:21:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 08 Dec 2023 20:21:57 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b1d4a557f047b695f94452d9707061981d7fae4239c674b332282b8291963c`  
		Last Modified: Thu, 16 Nov 2023 03:11:20 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45549c207f14d769cba7c36b66157ec213bbc32ce57d685d8e2c407cf3987bb`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c674717e06bf8cb25d5887393ef9568ee0ab6390966b9666808e836e9bd471d`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2227badcd9f5f2b70b3d2ffd1c18887498f413c07802bfb334e8dc7b2d2acc`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9f3b5e90a2e6028cf194e870b24a7158f875f18b81f4f9137a5db3ea1f79ac`  
		Last Modified: Thu, 16 Nov 2023 03:11:23 GMT  
		Size: 25.5 MB (25536225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7811a5416dcd19193a5b3ab9327607bf845f7ff77f95d3e20abdfb7435c32ae0`  
		Last Modified: Thu, 16 Nov 2023 03:11:16 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5931209e960a94616639ea72e4d3ad9dc9cb554790ce930152c73bdc1449c034`  
		Last Modified: Thu, 16 Nov 2023 03:11:16 GMT  
		Size: 266.6 KB (266600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a70f603a2fb4e76edd3165b62a179fb8f6410e265f5ae4a3732ee68e610034b`  
		Last Modified: Tue, 05 Dec 2023 20:38:48 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e37840dec3a6665ce48520be8b2c51b654359765bee5ab0780ee74746f0eb2`  
		Last Modified: Tue, 05 Dec 2023 20:39:08 GMT  
		Size: 69.3 MB (69342960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d16ae54757acda093616d24735d4c92d4676649bec49807fc35de90d15e15c`  
		Last Modified: Tue, 05 Dec 2023 20:38:48 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5744d01eddd2ef9d9673fdb0f0e48203fad1b01f2b14899a3ec6393c4548e75`  
		Last Modified: Tue, 05 Dec 2023 21:02:23 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35bb848667aa413b6ce6c309a4c2169635b0740dc335b9b39413a00627c01ab`  
		Last Modified: Tue, 05 Dec 2023 21:02:21 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54630e9807bbb8995ce52459e6e3c8d818351c481e0ce29280570e90d0138d33`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f15ec018ec91e33ee96d4f0e6b66d9edb40b185a13f91d16f12d0bf682ab08b`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79cc8b934303f209cd48271252cb46966445a1099aac277ae4caf120af718ab`  
		Last Modified: Fri, 08 Dec 2023 20:23:49 GMT  
		Size: 1.7 MB (1677815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224f75043e75fb7c85d3daec88a29069c6ff40b8feeaa26bac868d524758955`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder-alpine`

```console
$ docker pull caddy@sha256:a6d9bf50074feba4597d504f2c617c7d3e772c19b67d0ca788dcf2dcb421bd08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2.7.6-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:64cc92d77653c256c9cde397fb221c57907a57b0fe04f4e83ab2f7123f7f9147
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76963251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccce7adcc2b72b984adc9e5dd37663d1e6e512e39657c41bed43c55b38f9bad9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:46:23 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 03:46:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:25:52 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:26:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:26:02 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:26:02 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:26:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:26:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:26:03 GMT
WORKDIR /go
# Tue, 05 Dec 2023 20:48:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 20:48:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:39:46 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:39:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:39:46 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 20:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 20:39:47 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 20:39:47 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5501dced60f86be38cc73d3c038f7db4afeee65726f7e422aacf09244539ebf1`  
		Last Modified: Fri, 01 Dec 2023 03:50:39 GMT  
		Size: 284.7 KB (284697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63d189496f5f03c835c9c85df2db6920546d36a1701f6b5ad15f800c671605d`  
		Last Modified: Tue, 05 Dec 2023 20:31:27 GMT  
		Size: 67.0 MB (67003308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aeb88dd0f3e06a57abc08c781b85c89d138194918c469aea9a1bed9753d2ed0`  
		Last Modified: Tue, 05 Dec 2023 20:31:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40ff2505fd8d96e76bddb63b05c2d42815db1dabe0093ec8f8f53be403b0d01`  
		Last Modified: Tue, 05 Dec 2023 20:49:17 GMT  
		Size: 5.0 MB (4970029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ba23d637be879f93c12d4e6d077eb636688fa34e5d637f1f9a2f0a28509f0d`  
		Last Modified: Fri, 08 Dec 2023 20:40:19 GMT  
		Size: 1.3 MB (1302232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57ad5b5be9e26b4f05c8402814544f231f87d6a736a05320421e0ce2e623f04`  
		Last Modified: Fri, 08 Dec 2023 20:40:19 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:cd2d4a5ddcdef2492b7b440240d2e3beffa1695c0a1273227efdbc97a0fddc86
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75411895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed519bbe9039d7d32e60f9e1c959613953c4508dc6dd1506a355f0e0fd39bbe7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:53:48 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 00:53:48 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:49:18 GMT
ENV GOLANG_VERSION=1.21.5
# Sat, 09 Dec 2023 01:49:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	elif [ "$arch" = 'armv7' ]; then 		[ -s /usr/local/go/go.env ]; 		before="$(go env GOARM)"; [ "$before" != '7' ]; 		{ 			echo; 			echo '# https://github.com/docker-library/golang/issues/494'; 			echo 'GOARM=7'; 		} >> /usr/local/go/go.env; 		after="$(go env GOARM)"; [ "$after" = '7' ]; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Sat, 09 Dec 2023 01:49:51 GMT
ENV GOTOOLCHAIN=local
# Sat, 09 Dec 2023 01:49:51 GMT
ENV GOPATH=/go
# Sat, 09 Dec 2023 01:49:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 01:49:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Sat, 09 Dec 2023 01:49:52 GMT
WORKDIR /go
# Sat, 09 Dec 2023 02:08:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 09 Dec 2023 02:08:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 09 Dec 2023 02:08:59 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 09 Dec 2023 02:08:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 09 Dec 2023 02:08:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 09 Dec 2023 02:09:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 09 Dec 2023 02:09:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 09 Dec 2023 02:09:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e7ba0492eb25e7f21078441d7cdc65088836bc1984bc4a14cd3e9cd75cbf32`  
		Last Modified: Fri, 01 Dec 2023 01:00:23 GMT  
		Size: 284.9 KB (284884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbf3e566edb99ecb0ecb757d0f571633d7d822bf31896dd76a40ff9d89e98c0`  
		Last Modified: Sat, 09 Dec 2023 01:53:04 GMT  
		Size: 65.8 MB (65764277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e170d213450f3f3c66f85329ded2a75a6b38e5b51cfe01f2ad9d2cc2aab61079`  
		Last Modified: Sat, 09 Dec 2023 01:52:51 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612473e16b229d3c58615a469f9ca073ec9dc483d79cd7bb87479eea58ee5454`  
		Last Modified: Sat, 09 Dec 2023 02:09:20 GMT  
		Size: 5.0 MB (4966653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ed572067dfce272b021aee6f0cd14272e2a1157f0cf11ad00004a5c9354bc0`  
		Last Modified: Sat, 09 Dec 2023 02:09:19 GMT  
		Size: 1.2 MB (1248652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7608cc7cd78c6c2f18a53621dbd0b1746b9274ce1b35a8279b261816e41718ef`  
		Last Modified: Sat, 09 Dec 2023 02:09:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:7b8943fed6d62476c9dea44a16caea83fb6d540be101271d0974e0f2ed5a1567
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74707178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e459d7afebbd1af456db2bc6e8849445ca45f2586a9bbd0337ba314f570a177`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:44:57 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 08:44:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:58:01 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:58:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:58:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:58:16 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:58:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:58:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:58:17 GMT
WORKDIR /go
# Tue, 05 Dec 2023 21:22:31 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 21:22:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:16:31 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:16:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:16:32 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 20:16:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 20:16:34 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 20:16:34 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a824ff289f1a3c765a444079137b8b7f1cee80348faa53e1ba4c960b73ed2a`  
		Last Modified: Fri, 01 Dec 2023 08:49:42 GMT  
		Size: 284.1 KB (284079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4989177b4ed66b7e9f9e8c4bfce82720b582e24b735d6628effa75d81c5718fc`  
		Last Modified: Tue, 05 Dec 2023 21:04:43 GMT  
		Size: 65.8 MB (65764197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f9b58eae167c54d3faa3eeffd480cdae7e8b4841eb816a86cfdd01f8ae29ef`  
		Last Modified: Tue, 05 Dec 2023 21:04:29 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4cd1a3aab8fc02791b1e19f81b7de1bd691c10a7c942acc7e733221bf12888`  
		Last Modified: Tue, 05 Dec 2023 21:22:47 GMT  
		Size: 4.5 MB (4511237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c6a5bcaed596afac229d37cd822ea4770b06d4d3580d14a71d26e32136f1aa`  
		Last Modified: Fri, 08 Dec 2023 20:17:09 GMT  
		Size: 1.2 MB (1246093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c59154934645e7c4d44eda6d3d5ea9d4b32e23fbf7ccb7009cc54413ae815d`  
		Last Modified: Fri, 08 Dec 2023 20:17:09 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:3fce35ec600b6e48bb63c1b2d390b6d515a6f0e7355b582fcb347092222bdc37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73981648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3475cc52d42bfd049fb20d388ecf6c8482841b98a265b9fc09b60bc815011df9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:43:53 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 03:18:30 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:16:18 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:16:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:16:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:16:28 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:16:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:16:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:16:28 GMT
WORKDIR /go
# Tue, 05 Dec 2023 20:38:16 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 20:38:16 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 19:55:21 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 19:55:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 19:55:21 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 19:55:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 19:55:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 19:55:22 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a63ed24dc22a348b35d99b5ec9dc67ff66563b539875e5c8ab2d870b3991ac`  
		Last Modified: Fri, 01 Dec 2023 02:44:03 GMT  
		Size: 286.3 KB (286307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f00641dffc5c2a149049ee9046bb24cfc7de534b7495a0f27784a4fff0fadc`  
		Last Modified: Tue, 05 Dec 2023 20:21:00 GMT  
		Size: 64.1 MB (64094844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452682ba77e89fc55be3a168358f5f43bccad93ecdd3d53b4dec7fff6915128b`  
		Last Modified: Tue, 05 Dec 2023 20:20:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3fe1e12507f8c4a2731393eebfc5ab973aa344b0daceec525560b812b26f60`  
		Last Modified: Tue, 05 Dec 2023 20:38:33 GMT  
		Size: 5.1 MB (5068450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1568fb18f5eae3df776dd2fee8d447615d0f62601f82ebdb1bf2af5155bb83`  
		Last Modified: Fri, 08 Dec 2023 19:55:49 GMT  
		Size: 1.2 MB (1198450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15988851efd259492be8e7583025cb2b00f7477442c7be3e2d3dd97adbc39e76`  
		Last Modified: Fri, 08 Dec 2023 19:55:48 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:e21739ed4cecc54ebd496b12fa757f5901f3c0b45d211c0c5fa2ef551543c2d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74206507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed778e73218e8613cd2044f7eb703ec05bf43271d444ca5ffe77e053baa719c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:37:34 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 06:37:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:38:14 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:38:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:38:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:38:38 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:38:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:38:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:38:41 GMT
WORKDIR /go
# Tue, 05 Dec 2023 21:04:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 21:04:34 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:22:32 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:22:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:22:33 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 20:22:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 20:22:35 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 20:22:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692dbecd5e141c462ab06ef113ec964b525e7564d734890cc1d5b1dbf33ee34e`  
		Last Modified: Fri, 01 Dec 2023 06:43:30 GMT  
		Size: 286.7 KB (286661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc89a0f2d97ecfd4d20235e72227fc24aa79a64509fe9ea64702db658f2ad26d`  
		Last Modified: Tue, 05 Dec 2023 20:46:23 GMT  
		Size: 64.1 MB (64115804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d76f2c2e2bbb4190b1865ddafdc8cb88adee4c79d7d5ba23e69696e9610889`  
		Last Modified: Tue, 05 Dec 2023 20:46:11 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e0ec0f713ee657d6aa159fab65c05939480b5ca50a8e3dc4b1a9a6578160f7`  
		Last Modified: Tue, 05 Dec 2023 21:04:57 GMT  
		Size: 5.3 MB (5268970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbd7401349780157d6d930ec942f00b1d5404d31ae60bff5c7b41238cf8e3b1`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 1.2 MB (1186185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67206b5e4434d3211a98a71837832baed45e4fb0c03ff8dc204bc7762a8ab559`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:bf201fa7da491e4decf9c0a638b9fbcb4b459d5b13bcc9a2f4c0fb4c583c609b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76101050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e2b3cda7ff391c43b985fdbd1c3515e69b6fbe94f8ea6c9a09749c147e491c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:14:49 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 08:14:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:44:16 GMT
ENV GOLANG_VERSION=1.21.5
# Sat, 09 Dec 2023 01:50:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	elif [ "$arch" = 'armv7' ]; then 		[ -s /usr/local/go/go.env ]; 		before="$(go env GOARM)"; [ "$before" != '7' ]; 		{ 			echo; 			echo '# https://github.com/docker-library/golang/issues/494'; 			echo 'GOARM=7'; 		} >> /usr/local/go/go.env; 		after="$(go env GOARM)"; [ "$after" = '7' ]; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Sat, 09 Dec 2023 01:50:41 GMT
ENV GOTOOLCHAIN=local
# Sat, 09 Dec 2023 01:50:41 GMT
ENV GOPATH=/go
# Sat, 09 Dec 2023 01:50:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 01:50:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Sat, 09 Dec 2023 01:50:42 GMT
WORKDIR /go
# Sat, 09 Dec 2023 02:12:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 09 Dec 2023 02:12:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 09 Dec 2023 02:12:31 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 09 Dec 2023 02:12:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 09 Dec 2023 02:12:31 GMT
ENV XCADDY_SETCAP=1
# Sat, 09 Dec 2023 02:12:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 09 Dec 2023 02:12:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 09 Dec 2023 02:12:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab563e8d41683e124df048aa9b564b0e8e1021e85213666971a015df51d5e48`  
		Last Modified: Fri, 01 Dec 2023 08:20:46 GMT  
		Size: 285.1 KB (285090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c541c9463bd8d06e97aa1b14ce0792cf2caf6ef8ddc7b046b21032b3390bee`  
		Last Modified: Sat, 09 Dec 2023 01:54:50 GMT  
		Size: 66.2 MB (66218593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236faa4ca6aed551be037e8e0a2312e72dedf504cdffa8d2015882df02c5b87e`  
		Last Modified: Sat, 09 Dec 2023 01:54:39 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee294f5771410ee01c59c398d0270a28f5ae4caff9abfa5339f1c54b1dc1ab5a`  
		Last Modified: Sat, 09 Dec 2023 02:12:56 GMT  
		Size: 5.1 MB (5116966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cbd016bf9fbfd249882a217530ca94dcac095e46620a64badd9bbfa6ae9ebe`  
		Last Modified: Sat, 09 Dec 2023 02:12:55 GMT  
		Size: 1.3 MB (1262386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b36774ae94aa93a3beb6e355ee08897437b53c870bc56fdc3047ce591cfa2ac`  
		Last Modified: Sat, 09 Dec 2023 02:12:55 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:8bf37ab9a085a9916fcfb4a921ebbfe2d29d2893fac56672655cc8ccd5fa3c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `caddy:2.7.6-builder-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull caddy@sha256:cdab1fd140455df0674bfedde2f4948b5289720efd10ff1301ce39bb60cd8daf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154297412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39391f7d87fac7b43f0ed0b59b1981b263a30d3397f5f5244adf81cb7627ba5a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 02:47:03 GMT
ENV GIT_VERSION=2.23.0
# Thu, 16 Nov 2023 02:47:04 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 16 Nov 2023 02:47:05 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 16 Nov 2023 02:47:06 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 16 Nov 2023 02:48:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 02:48:31 GMT
ENV GOPATH=C:\go
# Thu, 16 Nov 2023 02:49:41 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Dec 2023 20:18:04 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:21:11 GMT
RUN $url = 'https://dl.google.com/go/go1.21.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bbe603cde7c9dee658f45164b4d06de1eff6e6e6b800100824e7c00d56a9a92f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Dec 2023 20:21:13 GMT
WORKDIR C:\go
# Tue, 05 Dec 2023 20:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Dec 2023 20:59:30 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:20:06 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:20:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:21:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 08 Dec 2023 20:21:15 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e901367fac1450f509d3118ada9e004e3613844ebdf91861147a093483930a4`  
		Last Modified: Thu, 16 Nov 2023 03:11:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e08004205bd077d8f22b013c70dc2f10796c64fced1eb9927e0055daff2d05d`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebc5048afc68ef48e2f2136545e2cccf26bb29eb4926bf4259b370ad55b4e7a`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f50fe5c7ef21648f3eaa4304932877a116fcb910b8e9095c779a2fbe6d57f7e`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76fe0e37750041d4ede2a0ca3b5245cfe075c3eb2ee27d7ce72ee8c3d7b20cc`  
		Last Modified: Thu, 16 Nov 2023 03:12:00 GMT  
		Size: 25.5 MB (25537512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8097bb9b8778d15dbf89d899653bf1634ec17554e5d84ef1ccfcac8ebf86afe2`  
		Last Modified: Thu, 16 Nov 2023 03:11:53 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b542d31e914d67da86cc5701cdc282ab664dc1170507e3802e22ab3026436a90`  
		Last Modified: Thu, 16 Nov 2023 03:11:53 GMT  
		Size: 263.2 KB (263200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86acdf7d3955fb44136bac433a30ccbbb97863120f270af32659dd65446666c7`  
		Last Modified: Tue, 05 Dec 2023 20:39:22 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1abe126c354944b7db8aa724d8f757167f7c3b36d39f976ef3b1b0d1b1b65ab`  
		Last Modified: Tue, 05 Dec 2023 20:39:41 GMT  
		Size: 69.4 MB (69361283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6338af096e09067ad482a0f4a6df1d1eee5b5595a64ca5f367b94ce27903e284`  
		Last Modified: Tue, 05 Dec 2023 20:39:22 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0adc218b27ef5639384c060fb663de3bd74374279d3fd525aa281f63a754779`  
		Last Modified: Tue, 05 Dec 2023 21:02:06 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c21053b248805df7ad888734f5cd1df5a6b426111512d5a6b7530060e7f30b2`  
		Last Modified: Tue, 05 Dec 2023 21:02:03 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034eb8f336a0d8e998c3eef6834d07c072c0679ccd4fde02cc8787ed46c80b19`  
		Last Modified: Fri, 08 Dec 2023 20:23:31 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af9b0b53a037a76c1c2e0e3afbe4fad733bc634a5ca02d53055360d9b7e33b9`  
		Last Modified: Fri, 08 Dec 2023 20:23:31 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f653ab9a896e2a3cfaf147a9ebb6e2d23f453cc3f953ee19b27333ebbc66460b`  
		Last Modified: Fri, 08 Dec 2023 20:23:32 GMT  
		Size: 1.7 MB (1685700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed98b1069776f09873a216052d2bf114c714b8269e4235d0aee375a2b0b7962`  
		Last Modified: Fri, 08 Dec 2023 20:23:31 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:b944570c2f667cfb312913d3478de80037fe9967f6fd20a1358e3f1b87467164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `caddy:2.7.6-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull caddy@sha256:b1d94a17104c4814aa7672316e4c713aefcdfa6ffd19043f4111784c09931cda
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1983623336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61ba19fe8fdfa90a532d1f355b356c651a2921264135f6417c72193a5f37396`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 02:43:34 GMT
ENV GIT_VERSION=2.23.0
# Thu, 16 Nov 2023 02:43:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 16 Nov 2023 02:43:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 16 Nov 2023 02:43:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 16 Nov 2023 02:44:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 02:44:11 GMT
ENV GOPATH=C:\go
# Thu, 16 Nov 2023 02:44:30 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Dec 2023 20:15:35 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:17:49 GMT
RUN $url = 'https://dl.google.com/go/go1.21.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bbe603cde7c9dee658f45164b4d06de1eff6e6e6b800100824e7c00d56a9a92f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Dec 2023 20:17:50 GMT
WORKDIR C:\go
# Tue, 05 Dec 2023 21:00:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Dec 2023 21:00:58 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:21:33 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:21:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:21:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 08 Dec 2023 20:21:57 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b1d4a557f047b695f94452d9707061981d7fae4239c674b332282b8291963c`  
		Last Modified: Thu, 16 Nov 2023 03:11:20 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45549c207f14d769cba7c36b66157ec213bbc32ce57d685d8e2c407cf3987bb`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c674717e06bf8cb25d5887393ef9568ee0ab6390966b9666808e836e9bd471d`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2227badcd9f5f2b70b3d2ffd1c18887498f413c07802bfb334e8dc7b2d2acc`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9f3b5e90a2e6028cf194e870b24a7158f875f18b81f4f9137a5db3ea1f79ac`  
		Last Modified: Thu, 16 Nov 2023 03:11:23 GMT  
		Size: 25.5 MB (25536225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7811a5416dcd19193a5b3ab9327607bf845f7ff77f95d3e20abdfb7435c32ae0`  
		Last Modified: Thu, 16 Nov 2023 03:11:16 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5931209e960a94616639ea72e4d3ad9dc9cb554790ce930152c73bdc1449c034`  
		Last Modified: Thu, 16 Nov 2023 03:11:16 GMT  
		Size: 266.6 KB (266600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a70f603a2fb4e76edd3165b62a179fb8f6410e265f5ae4a3732ee68e610034b`  
		Last Modified: Tue, 05 Dec 2023 20:38:48 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e37840dec3a6665ce48520be8b2c51b654359765bee5ab0780ee74746f0eb2`  
		Last Modified: Tue, 05 Dec 2023 20:39:08 GMT  
		Size: 69.3 MB (69342960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d16ae54757acda093616d24735d4c92d4676649bec49807fc35de90d15e15c`  
		Last Modified: Tue, 05 Dec 2023 20:38:48 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5744d01eddd2ef9d9673fdb0f0e48203fad1b01f2b14899a3ec6393c4548e75`  
		Last Modified: Tue, 05 Dec 2023 21:02:23 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35bb848667aa413b6ce6c309a4c2169635b0740dc335b9b39413a00627c01ab`  
		Last Modified: Tue, 05 Dec 2023 21:02:21 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54630e9807bbb8995ce52459e6e3c8d818351c481e0ce29280570e90d0138d33`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f15ec018ec91e33ee96d4f0e6b66d9edb40b185a13f91d16f12d0bf682ab08b`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79cc8b934303f209cd48271252cb46966445a1099aac277ae4caf120af718ab`  
		Last Modified: Fri, 08 Dec 2023 20:23:49 GMT  
		Size: 1.7 MB (1677815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224f75043e75fb7c85d3daec88a29069c6ff40b8feeaa26bac868d524758955`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-windowsservercore`

```console
$ docker pull caddy@sha256:23526c514f90e81e3b94593ed41182252a81ba946c70cf1d2638381f84849d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.5122; amd64
	-	windows version 10.0.20348.2113; amd64

### `caddy:2.7.6-windowsservercore` - windows version 10.0.17763.5122; amd64

```console
$ docker pull caddy@sha256:3d281f8c1d34b38abb3b5ca4ff98d70312daad9b0654a470374d0447a69a3ccf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073448315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e423604e6f05b59d8afa51e2d09a8fc11e1ac3353a126e3ce73b1c2bc65872b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:16:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:16:25 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:17:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:17:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:17:34 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:17:35 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:17:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:17:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:17:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:17:41 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:17:43 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:18:34 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:18:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09e9b6b38c0082853f1d6caa4d3536344a04da2aa5b674837aba8781b265e0d`  
		Last Modified: Fri, 08 Dec 2023 20:22:45 GMT  
		Size: 462.7 KB (462693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb778801cf9547a5b9021d3090bd8e4fc05f09e3aed56b6950dcbd044211d3f`  
		Last Modified: Fri, 08 Dec 2023 20:22:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ec815279848293cd980ed43a496bf4d3e8f8035f8d46dd1a3278e02c4558a8`  
		Last Modified: Fri, 08 Dec 2023 20:22:46 GMT  
		Size: 15.3 MB (15274633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9671feff108f8e0d8be270b64952394b3eaf7d16a7e9163cffc500ad3a42bd17`  
		Last Modified: Fri, 08 Dec 2023 20:22:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44f97706c45d8ebb4578d93d6c1cb5ecc4625f2f78fa40f25f9e72af014449a`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7b5732d0f0e4f61cac2e09f77054657b1bfc21c56b5b4b842e96ee7de3d45d`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348bbb9a26a300473cbb347ce3e405736e7a71ef7d2e67068452760fe4a1a67e`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4dc80dd8b7091a5cb553a95c06fa14380bf94a6f80467e3d7a36cb649fce8c`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6e2ab9cd2c6c903f643bcab22655dc93ec72fcc2f748a47375e2209580eed8`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a498a93a315d79030214cb59d847ede547dfc1159616120a3b48f2b1585bccfc`  
		Last Modified: Fri, 08 Dec 2023 20:22:40 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a7d0f8e26a8dd06b83bb38bfecf51f24ec1456947f459528e71b2544d13f5`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0da3c95480c1f76c862487e0683bed75c660c5cce3e3864677b8c956228e64`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1712e0793bc7067adabbb602cf9eaf0e6ab60f33be0b2b10282325884270ab07`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26aa77bbc553e8bf9318552da7ffe35258b387e04151dd211a006f50cb57a6`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e384f6873d9619640183b8c67671c94c80eb3725ac52c312de84b314b2cd4c53`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7ecef2ca51e4738a30164e40d773f9bfcc9a55bda13a00745349db1618fbf0`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29866626f3b37691b2e593b7ad8a6d3f6e916d9ca428c22e1b3834e568c605c9`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dff7ab50f452876c91da33fe48a0e1409de6cbb0ffca4e1aefa68caa5722d01`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 256.7 KB (256705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55865895b10a6247b60406c70eaa3584e7904512f0092bd7d9013bd9fe64c740`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-windowsservercore` - windows version 10.0.20348.2113; amd64

```console
$ docker pull caddy@sha256:cca2801fca8e41625ec6c3c42ee17cc76b64320f93ec2c37999b29b5f9ff0747
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1902845713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ad0d44150328d8253edf3d339d33f508e3a25395c8fd773d2d2fe5966eb244`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:19:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:19:10 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:19:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:19:34 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:19:35 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:19:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:19:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:19:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:19:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:19:43 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:19:44 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:19:58 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:19:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9e496904b6bbc7ce10b08f4c5c00b922d19bb8ebfca4735ba504c9ca77dd2b`  
		Last Modified: Fri, 08 Dec 2023 20:23:12 GMT  
		Size: 474.4 KB (474429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d370d88e3c2ee411f6f86dd892eba2c381cf5706823fcf82fec94a47d7d3bb4`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1861a873425170bdbe2b563cd2b9584401a7be0e3d9a6ceac998eef4eab482ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:13 GMT  
		Size: 15.3 MB (15274241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e17c8887831a9d0a255eb44daaaedffc1bb98b51fc0177786dd130c85034006`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2595203a1e7cbe5c30c3a77633ff7b832c6f07580e688e7c2bc89b5442e72ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b5a75922e76c5c96d069952df83b51d1243d2d6955db5b45dd7b63aea2b3a1`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bbe845ab80dc71320eea94c3d56888074ea930dc6fbe934c60e6c801e9cee3`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74052a6ffee1242926db0907e5406b7e5d81e181d3c9c266d381aaf221bf0252`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbd2ebe3b760156655b6475d7ff52b549e20b5115cf815016c902f834bf3f14`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5945b936f7903435999bc26916fd896f5c645c5b70834243317e66b14d7c2d97`  
		Last Modified: Fri, 08 Dec 2023 20:23:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4345b37fb7af089771ba8cf5542de3045ebb0f1d247ea038535504b320c4ac2c`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12593e8f188e5024af21891d9f3141bc5b85d9e2e9e2b61d7c2634f9f491b9a4`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3632692d5118ec05512cfb67c4aa09a8dfdfe1e40467dfc5ee8e5d2e9a349b2a`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e694808297bceaf6299316f20be2a78e4d2eef8a2ca455dd79ce544cf0a00e66`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258e53ea4c6d9b42de13f722ade5338a5393993985f05ca5b438982dde948654`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20692d7b4da06a40fca6c59bffc5e13dc0a0ffc429f70ed8701dc1d5d8c087fd`  
		Last Modified: Fri, 08 Dec 2023 20:23:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f686dbb1484378b8f73bbbfac32eb04d8f9a6b2b3f4db7d17c1f997941475a7f`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84003630e1340399082b07e0df6cb438545136bc3f0c134d52e8fe9d878e7239`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 292.2 KB (292197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9991bbf8fb125121b7478726325dcb657bfbeb24af279019b7b2f7ac0c404f7`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-windowsservercore-1809`

```console
$ docker pull caddy@sha256:67a59b537826dfa0019b55a7c113d5bdd826062754543ae24cccdcf2a558d407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `caddy:2.7.6-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull caddy@sha256:3d281f8c1d34b38abb3b5ca4ff98d70312daad9b0654a470374d0447a69a3ccf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073448315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e423604e6f05b59d8afa51e2d09a8fc11e1ac3353a126e3ce73b1c2bc65872b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:16:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:16:25 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:17:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:17:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:17:34 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:17:35 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:17:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:17:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:17:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:17:41 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:17:43 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:18:34 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:18:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09e9b6b38c0082853f1d6caa4d3536344a04da2aa5b674837aba8781b265e0d`  
		Last Modified: Fri, 08 Dec 2023 20:22:45 GMT  
		Size: 462.7 KB (462693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb778801cf9547a5b9021d3090bd8e4fc05f09e3aed56b6950dcbd044211d3f`  
		Last Modified: Fri, 08 Dec 2023 20:22:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ec815279848293cd980ed43a496bf4d3e8f8035f8d46dd1a3278e02c4558a8`  
		Last Modified: Fri, 08 Dec 2023 20:22:46 GMT  
		Size: 15.3 MB (15274633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9671feff108f8e0d8be270b64952394b3eaf7d16a7e9163cffc500ad3a42bd17`  
		Last Modified: Fri, 08 Dec 2023 20:22:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44f97706c45d8ebb4578d93d6c1cb5ecc4625f2f78fa40f25f9e72af014449a`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7b5732d0f0e4f61cac2e09f77054657b1bfc21c56b5b4b842e96ee7de3d45d`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348bbb9a26a300473cbb347ce3e405736e7a71ef7d2e67068452760fe4a1a67e`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4dc80dd8b7091a5cb553a95c06fa14380bf94a6f80467e3d7a36cb649fce8c`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6e2ab9cd2c6c903f643bcab22655dc93ec72fcc2f748a47375e2209580eed8`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a498a93a315d79030214cb59d847ede547dfc1159616120a3b48f2b1585bccfc`  
		Last Modified: Fri, 08 Dec 2023 20:22:40 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a7d0f8e26a8dd06b83bb38bfecf51f24ec1456947f459528e71b2544d13f5`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0da3c95480c1f76c862487e0683bed75c660c5cce3e3864677b8c956228e64`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1712e0793bc7067adabbb602cf9eaf0e6ab60f33be0b2b10282325884270ab07`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26aa77bbc553e8bf9318552da7ffe35258b387e04151dd211a006f50cb57a6`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e384f6873d9619640183b8c67671c94c80eb3725ac52c312de84b314b2cd4c53`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7ecef2ca51e4738a30164e40d773f9bfcc9a55bda13a00745349db1618fbf0`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29866626f3b37691b2e593b7ad8a6d3f6e916d9ca428c22e1b3834e568c605c9`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dff7ab50f452876c91da33fe48a0e1409de6cbb0ffca4e1aefa68caa5722d01`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 256.7 KB (256705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55865895b10a6247b60406c70eaa3584e7904512f0092bd7d9013bd9fe64c740`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:0726791503ced6bf9bdc5b322a8082762fb4ca97438a2c8fb49d0e80f06838ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `caddy:2.7.6-windowsservercore-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull caddy@sha256:cca2801fca8e41625ec6c3c42ee17cc76b64320f93ec2c37999b29b5f9ff0747
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1902845713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ad0d44150328d8253edf3d339d33f508e3a25395c8fd773d2d2fe5966eb244`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:19:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:19:10 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:19:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:19:34 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:19:35 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:19:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:19:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:19:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:19:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:19:43 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:19:44 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:19:58 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:19:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9e496904b6bbc7ce10b08f4c5c00b922d19bb8ebfca4735ba504c9ca77dd2b`  
		Last Modified: Fri, 08 Dec 2023 20:23:12 GMT  
		Size: 474.4 KB (474429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d370d88e3c2ee411f6f86dd892eba2c381cf5706823fcf82fec94a47d7d3bb4`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1861a873425170bdbe2b563cd2b9584401a7be0e3d9a6ceac998eef4eab482ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:13 GMT  
		Size: 15.3 MB (15274241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e17c8887831a9d0a255eb44daaaedffc1bb98b51fc0177786dd130c85034006`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2595203a1e7cbe5c30c3a77633ff7b832c6f07580e688e7c2bc89b5442e72ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b5a75922e76c5c96d069952df83b51d1243d2d6955db5b45dd7b63aea2b3a1`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bbe845ab80dc71320eea94c3d56888074ea930dc6fbe934c60e6c801e9cee3`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74052a6ffee1242926db0907e5406b7e5d81e181d3c9c266d381aaf221bf0252`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbd2ebe3b760156655b6475d7ff52b549e20b5115cf815016c902f834bf3f14`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5945b936f7903435999bc26916fd896f5c645c5b70834243317e66b14d7c2d97`  
		Last Modified: Fri, 08 Dec 2023 20:23:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4345b37fb7af089771ba8cf5542de3045ebb0f1d247ea038535504b320c4ac2c`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12593e8f188e5024af21891d9f3141bc5b85d9e2e9e2b61d7c2634f9f491b9a4`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3632692d5118ec05512cfb67c4aa09a8dfdfe1e40467dfc5ee8e5d2e9a349b2a`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e694808297bceaf6299316f20be2a78e4d2eef8a2ca455dd79ce544cf0a00e66`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258e53ea4c6d9b42de13f722ade5338a5393993985f05ca5b438982dde948654`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20692d7b4da06a40fca6c59bffc5e13dc0a0ffc429f70ed8701dc1d5d8c087fd`  
		Last Modified: Fri, 08 Dec 2023 20:23:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f686dbb1484378b8f73bbbfac32eb04d8f9a6b2b3f4db7d17c1f997941475a7f`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84003630e1340399082b07e0df6cb438545136bc3f0c134d52e8fe9d878e7239`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 292.2 KB (292197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9991bbf8fb125121b7478726325dcb657bfbeb24af279019b7b2f7ac0c404f7`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:alpine`

```console
$ docker pull caddy@sha256:eabac2898cf9fc7dc94d3fb03ac84c9c923aa6cc6f04874937d2f525e0d2f006
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
$ docker pull caddy@sha256:7b8b4b0a4784433bd53271ff8f27d0940f96b1e633bb69b27d2c9ac5a293536a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18467236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657b947906e764d7ff65a638b958cb7f84b3754e49ede071620658385e743168`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:32:06 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:39:38 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:39:38 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:39:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:39:41 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:39:41 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:39:41 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:39:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:39:42 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:39:42 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:39:42 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:39:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08886dfc0722c4ed2cb6a70c285a33fe35aec069435868488356dde320b4d21c`  
		Last Modified: Fri, 01 Dec 2023 06:32:30 GMT  
		Size: 350.8 KB (350845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd2155878b9ec9d659128d039d90b8a50369fe85c88f64a597b6a9cd9441c1b`  
		Last Modified: Fri, 08 Dec 2023 20:40:01 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7343593237d1bd5fb218804e360a7a8c4d94d7af8da4eb1a72fbaf48fab9ce2`  
		Last Modified: Fri, 08 Dec 2023 20:40:03 GMT  
		Size: 14.7 MB (14706441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:fe42da7df688686dab79fb02be7f13aae32c9a9f84eec3b28b634cc48d5a7346
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17423030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f95b690a9e892f56dbf3fd455d714c2d22ebd35967fdc770fb704c870eeffc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:39:01 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:07:47 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:07:47 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:07:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:07:50 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:07:50 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:07:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:07:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:07:51 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:07:51 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc24e4ccf558b6e992efaaa7a735322be11fe99ce19e722eee6ae70bb76515d`  
		Last Modified: Fri, 01 Dec 2023 00:39:21 GMT  
		Size: 347.6 KB (347632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775b4c8558ad1bf8d7568fc741be39ee2a28ecdd33f84ed7597b6192873a81a`  
		Last Modified: Fri, 08 Dec 2023 20:08:10 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbf57a0db316ab6b42386b0221d652cc4f9d9d597206ce1d4e9bfd5ba0f7777`  
		Last Modified: Fri, 08 Dec 2023 20:08:12 GMT  
		Size: 13.9 MB (13920999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:cf486c3cc2b7d7cc0bdfc8db52605e6a533c0528e717b2ccd6e9779713d72229
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17146731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68a807660343335d38b999c8c1b687f5ec5c882c6f5180e13281152b030f103`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:19:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:16:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:16:22 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:16:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:16:25 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:16:26 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:16:27 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:16:27 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:16:28 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:16:28 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:16:28 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:16:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803b34e1f84b29ca968d2fbf85c278608566c34dfd1742e088c6483685957029`  
		Last Modified: Fri, 01 Dec 2023 03:19:48 GMT  
		Size: 344.5 KB (344464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de504bcc2429a4454910b605f8bb2f6eec4cad953044e48d02a7d51542b7266f`  
		Last Modified: Fri, 08 Dec 2023 20:16:53 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73099274a85e30e93cb0e71106c443fd9a5b923ef43adabf808db6a58db9ad8b`  
		Last Modified: Fri, 08 Dec 2023 20:16:56 GMT  
		Size: 13.9 MB (13893732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:71069b6f75345cd8b5e4841d92dcaebb4fa2acf454074eeb2c571517ac3671cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae18940ab920c723e970d89fde606b552e5b39f5fa33535cb6c7be09b6cff763`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:11:08 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 19:55:15 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 19:55:16 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 19:55:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 19:55:17 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 19:55:17 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 19:55:17 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 80
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 443
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 19:55:18 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 19:55:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e383270d6915b6b427f49a75d657d5a0403fcd47a5f89cd30e85143ca54c22`  
		Last Modified: Fri, 01 Dec 2023 03:11:28 GMT  
		Size: 360.7 KB (360655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f87e6bdbafc6710a3ed7bfbb4bb134e8d93bea992ab895c653cac0779389396`  
		Last Modified: Fri, 08 Dec 2023 19:55:35 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874486d3ac5891d4df17819e02e1cdd3775748effa24bc53645cd2db841a0837`  
		Last Modified: Fri, 08 Dec 2023 19:55:36 GMT  
		Size: 13.6 MB (13568967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:9991e527a64c1d20422e24e141a57efec5365c7bcd68662808b0ea23da815b3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17051913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274840ad1c2fe6344d298e9d6242bde6e602b3444a071cfe45d3db4360d193b4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:42:19 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:22:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:22:14 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:22:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:22:19 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:22:19 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:22:19 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:22:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:22:20 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:22:22 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:22:22 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:22:23 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:22:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:22:24 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:22:24 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:22:25 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:22:25 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:22:26 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:22:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce4bc2907f69809c3086f118895d7e5c8683349557239c0ce79dfbda0ce3768`  
		Last Modified: Fri, 01 Dec 2023 05:44:17 GMT  
		Size: 362.2 KB (362185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3c2787bdbaa50fce90e65038b2dbc9850d2fff68d5e731bcdb83c71ede912b`  
		Last Modified: Fri, 08 Dec 2023 20:22:53 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ce50c6341ede9fe5f61cc3a75eb534b7dd1172b7e88c015862cb9351c91ca1`  
		Last Modified: Fri, 08 Dec 2023 20:22:55 GMT  
		Size: 13.3 MB (13333877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:f8db25c8783258ee73a7ab061dbcb53f5229be2510ab4c72cbb6fe5292fdd1a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17818230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4782f6a3e2f343e87b335a56846d9ae67a4a5aded358a8501a4fb5a076e92cef`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:22:31 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 19:57:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 19:57:07 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 19:57:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 19:57:11 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 19:57:11 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 19:57:13 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 19:57:13 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 19:57:13 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 19:57:13 GMT
EXPOSE 80
# Fri, 08 Dec 2023 19:57:13 GMT
EXPOSE 443
# Fri, 08 Dec 2023 19:57:14 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 19:57:14 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 19:57:14 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 19:57:14 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20bbe0abb0a3f63718aa78742832077ad86b8ae86d70ce3ebcece342ec022c6`  
		Last Modified: Fri, 01 Dec 2023 08:23:07 GMT  
		Size: 354.9 KB (354948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa042ad4816c33e4f907bbf008abef2397efe2b3fc378430b2b925663a088370`  
		Last Modified: Fri, 08 Dec 2023 19:57:43 GMT  
		Size: 7.5 KB (7526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ceec9a3d819911fec4d039d31e2e3e38214fa45cb8384e8f047b5588724355`  
		Last Modified: Fri, 08 Dec 2023 19:57:45 GMT  
		Size: 14.2 MB (14238302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder`

```console
$ docker pull caddy@sha256:1bad661ef08b648af7c9c79e708965d3a69434285f24de76111124fdf5d339d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5122; amd64
	-	windows version 10.0.20348.2113; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:64cc92d77653c256c9cde397fb221c57907a57b0fe04f4e83ab2f7123f7f9147
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76963251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccce7adcc2b72b984adc9e5dd37663d1e6e512e39657c41bed43c55b38f9bad9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:46:23 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 03:46:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:25:52 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:26:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:26:02 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:26:02 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:26:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:26:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:26:03 GMT
WORKDIR /go
# Tue, 05 Dec 2023 20:48:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 20:48:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:39:46 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:39:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:39:46 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 20:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 20:39:47 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 20:39:47 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5501dced60f86be38cc73d3c038f7db4afeee65726f7e422aacf09244539ebf1`  
		Last Modified: Fri, 01 Dec 2023 03:50:39 GMT  
		Size: 284.7 KB (284697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63d189496f5f03c835c9c85df2db6920546d36a1701f6b5ad15f800c671605d`  
		Last Modified: Tue, 05 Dec 2023 20:31:27 GMT  
		Size: 67.0 MB (67003308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aeb88dd0f3e06a57abc08c781b85c89d138194918c469aea9a1bed9753d2ed0`  
		Last Modified: Tue, 05 Dec 2023 20:31:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40ff2505fd8d96e76bddb63b05c2d42815db1dabe0093ec8f8f53be403b0d01`  
		Last Modified: Tue, 05 Dec 2023 20:49:17 GMT  
		Size: 5.0 MB (4970029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ba23d637be879f93c12d4e6d077eb636688fa34e5d637f1f9a2f0a28509f0d`  
		Last Modified: Fri, 08 Dec 2023 20:40:19 GMT  
		Size: 1.3 MB (1302232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57ad5b5be9e26b4f05c8402814544f231f87d6a736a05320421e0ce2e623f04`  
		Last Modified: Fri, 08 Dec 2023 20:40:19 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:cd2d4a5ddcdef2492b7b440240d2e3beffa1695c0a1273227efdbc97a0fddc86
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75411895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed519bbe9039d7d32e60f9e1c959613953c4508dc6dd1506a355f0e0fd39bbe7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:53:48 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 00:53:48 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:49:18 GMT
ENV GOLANG_VERSION=1.21.5
# Sat, 09 Dec 2023 01:49:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	elif [ "$arch" = 'armv7' ]; then 		[ -s /usr/local/go/go.env ]; 		before="$(go env GOARM)"; [ "$before" != '7' ]; 		{ 			echo; 			echo '# https://github.com/docker-library/golang/issues/494'; 			echo 'GOARM=7'; 		} >> /usr/local/go/go.env; 		after="$(go env GOARM)"; [ "$after" = '7' ]; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Sat, 09 Dec 2023 01:49:51 GMT
ENV GOTOOLCHAIN=local
# Sat, 09 Dec 2023 01:49:51 GMT
ENV GOPATH=/go
# Sat, 09 Dec 2023 01:49:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 01:49:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Sat, 09 Dec 2023 01:49:52 GMT
WORKDIR /go
# Sat, 09 Dec 2023 02:08:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 09 Dec 2023 02:08:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 09 Dec 2023 02:08:59 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 09 Dec 2023 02:08:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 09 Dec 2023 02:08:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 09 Dec 2023 02:09:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 09 Dec 2023 02:09:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 09 Dec 2023 02:09:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e7ba0492eb25e7f21078441d7cdc65088836bc1984bc4a14cd3e9cd75cbf32`  
		Last Modified: Fri, 01 Dec 2023 01:00:23 GMT  
		Size: 284.9 KB (284884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbf3e566edb99ecb0ecb757d0f571633d7d822bf31896dd76a40ff9d89e98c0`  
		Last Modified: Sat, 09 Dec 2023 01:53:04 GMT  
		Size: 65.8 MB (65764277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e170d213450f3f3c66f85329ded2a75a6b38e5b51cfe01f2ad9d2cc2aab61079`  
		Last Modified: Sat, 09 Dec 2023 01:52:51 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612473e16b229d3c58615a469f9ca073ec9dc483d79cd7bb87479eea58ee5454`  
		Last Modified: Sat, 09 Dec 2023 02:09:20 GMT  
		Size: 5.0 MB (4966653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ed572067dfce272b021aee6f0cd14272e2a1157f0cf11ad00004a5c9354bc0`  
		Last Modified: Sat, 09 Dec 2023 02:09:19 GMT  
		Size: 1.2 MB (1248652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7608cc7cd78c6c2f18a53621dbd0b1746b9274ce1b35a8279b261816e41718ef`  
		Last Modified: Sat, 09 Dec 2023 02:09:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:7b8943fed6d62476c9dea44a16caea83fb6d540be101271d0974e0f2ed5a1567
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74707178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e459d7afebbd1af456db2bc6e8849445ca45f2586a9bbd0337ba314f570a177`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:44:57 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 08:44:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:58:01 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:58:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:58:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:58:16 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:58:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:58:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:58:17 GMT
WORKDIR /go
# Tue, 05 Dec 2023 21:22:31 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 21:22:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:16:31 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:16:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:16:32 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 20:16:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 20:16:34 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 20:16:34 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a824ff289f1a3c765a444079137b8b7f1cee80348faa53e1ba4c960b73ed2a`  
		Last Modified: Fri, 01 Dec 2023 08:49:42 GMT  
		Size: 284.1 KB (284079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4989177b4ed66b7e9f9e8c4bfce82720b582e24b735d6628effa75d81c5718fc`  
		Last Modified: Tue, 05 Dec 2023 21:04:43 GMT  
		Size: 65.8 MB (65764197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f9b58eae167c54d3faa3eeffd480cdae7e8b4841eb816a86cfdd01f8ae29ef`  
		Last Modified: Tue, 05 Dec 2023 21:04:29 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4cd1a3aab8fc02791b1e19f81b7de1bd691c10a7c942acc7e733221bf12888`  
		Last Modified: Tue, 05 Dec 2023 21:22:47 GMT  
		Size: 4.5 MB (4511237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c6a5bcaed596afac229d37cd822ea4770b06d4d3580d14a71d26e32136f1aa`  
		Last Modified: Fri, 08 Dec 2023 20:17:09 GMT  
		Size: 1.2 MB (1246093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c59154934645e7c4d44eda6d3d5ea9d4b32e23fbf7ccb7009cc54413ae815d`  
		Last Modified: Fri, 08 Dec 2023 20:17:09 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:3fce35ec600b6e48bb63c1b2d390b6d515a6f0e7355b582fcb347092222bdc37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73981648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3475cc52d42bfd049fb20d388ecf6c8482841b98a265b9fc09b60bc815011df9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:43:53 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 03:18:30 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:16:18 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:16:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:16:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:16:28 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:16:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:16:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:16:28 GMT
WORKDIR /go
# Tue, 05 Dec 2023 20:38:16 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 20:38:16 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 19:55:21 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 19:55:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 19:55:21 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 19:55:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 19:55:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 19:55:22 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a63ed24dc22a348b35d99b5ec9dc67ff66563b539875e5c8ab2d870b3991ac`  
		Last Modified: Fri, 01 Dec 2023 02:44:03 GMT  
		Size: 286.3 KB (286307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f00641dffc5c2a149049ee9046bb24cfc7de534b7495a0f27784a4fff0fadc`  
		Last Modified: Tue, 05 Dec 2023 20:21:00 GMT  
		Size: 64.1 MB (64094844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452682ba77e89fc55be3a168358f5f43bccad93ecdd3d53b4dec7fff6915128b`  
		Last Modified: Tue, 05 Dec 2023 20:20:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3fe1e12507f8c4a2731393eebfc5ab973aa344b0daceec525560b812b26f60`  
		Last Modified: Tue, 05 Dec 2023 20:38:33 GMT  
		Size: 5.1 MB (5068450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1568fb18f5eae3df776dd2fee8d447615d0f62601f82ebdb1bf2af5155bb83`  
		Last Modified: Fri, 08 Dec 2023 19:55:49 GMT  
		Size: 1.2 MB (1198450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15988851efd259492be8e7583025cb2b00f7477442c7be3e2d3dd97adbc39e76`  
		Last Modified: Fri, 08 Dec 2023 19:55:48 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:e21739ed4cecc54ebd496b12fa757f5901f3c0b45d211c0c5fa2ef551543c2d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74206507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed778e73218e8613cd2044f7eb703ec05bf43271d444ca5ffe77e053baa719c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:37:34 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 06:37:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:38:14 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:38:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:38:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:38:38 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:38:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:38:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:38:41 GMT
WORKDIR /go
# Tue, 05 Dec 2023 21:04:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 21:04:34 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:22:32 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:22:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:22:33 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 20:22:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 20:22:35 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 20:22:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692dbecd5e141c462ab06ef113ec964b525e7564d734890cc1d5b1dbf33ee34e`  
		Last Modified: Fri, 01 Dec 2023 06:43:30 GMT  
		Size: 286.7 KB (286661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc89a0f2d97ecfd4d20235e72227fc24aa79a64509fe9ea64702db658f2ad26d`  
		Last Modified: Tue, 05 Dec 2023 20:46:23 GMT  
		Size: 64.1 MB (64115804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d76f2c2e2bbb4190b1865ddafdc8cb88adee4c79d7d5ba23e69696e9610889`  
		Last Modified: Tue, 05 Dec 2023 20:46:11 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e0ec0f713ee657d6aa159fab65c05939480b5ca50a8e3dc4b1a9a6578160f7`  
		Last Modified: Tue, 05 Dec 2023 21:04:57 GMT  
		Size: 5.3 MB (5268970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbd7401349780157d6d930ec942f00b1d5404d31ae60bff5c7b41238cf8e3b1`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 1.2 MB (1186185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67206b5e4434d3211a98a71837832baed45e4fb0c03ff8dc204bc7762a8ab559`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:bf201fa7da491e4decf9c0a638b9fbcb4b459d5b13bcc9a2f4c0fb4c583c609b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76101050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e2b3cda7ff391c43b985fdbd1c3515e69b6fbe94f8ea6c9a09749c147e491c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:14:49 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 08:14:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:44:16 GMT
ENV GOLANG_VERSION=1.21.5
# Sat, 09 Dec 2023 01:50:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	elif [ "$arch" = 'armv7' ]; then 		[ -s /usr/local/go/go.env ]; 		before="$(go env GOARM)"; [ "$before" != '7' ]; 		{ 			echo; 			echo '# https://github.com/docker-library/golang/issues/494'; 			echo 'GOARM=7'; 		} >> /usr/local/go/go.env; 		after="$(go env GOARM)"; [ "$after" = '7' ]; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Sat, 09 Dec 2023 01:50:41 GMT
ENV GOTOOLCHAIN=local
# Sat, 09 Dec 2023 01:50:41 GMT
ENV GOPATH=/go
# Sat, 09 Dec 2023 01:50:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 01:50:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Sat, 09 Dec 2023 01:50:42 GMT
WORKDIR /go
# Sat, 09 Dec 2023 02:12:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 09 Dec 2023 02:12:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 09 Dec 2023 02:12:31 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 09 Dec 2023 02:12:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 09 Dec 2023 02:12:31 GMT
ENV XCADDY_SETCAP=1
# Sat, 09 Dec 2023 02:12:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 09 Dec 2023 02:12:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 09 Dec 2023 02:12:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab563e8d41683e124df048aa9b564b0e8e1021e85213666971a015df51d5e48`  
		Last Modified: Fri, 01 Dec 2023 08:20:46 GMT  
		Size: 285.1 KB (285090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c541c9463bd8d06e97aa1b14ce0792cf2caf6ef8ddc7b046b21032b3390bee`  
		Last Modified: Sat, 09 Dec 2023 01:54:50 GMT  
		Size: 66.2 MB (66218593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236faa4ca6aed551be037e8e0a2312e72dedf504cdffa8d2015882df02c5b87e`  
		Last Modified: Sat, 09 Dec 2023 01:54:39 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee294f5771410ee01c59c398d0270a28f5ae4caff9abfa5339f1c54b1dc1ab5a`  
		Last Modified: Sat, 09 Dec 2023 02:12:56 GMT  
		Size: 5.1 MB (5116966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cbd016bf9fbfd249882a217530ca94dcac095e46620a64badd9bbfa6ae9ebe`  
		Last Modified: Sat, 09 Dec 2023 02:12:55 GMT  
		Size: 1.3 MB (1262386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b36774ae94aa93a3beb6e355ee08897437b53c870bc56fdc3047ce591cfa2ac`  
		Last Modified: Sat, 09 Dec 2023 02:12:55 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.5122; amd64

```console
$ docker pull caddy@sha256:cdab1fd140455df0674bfedde2f4948b5289720efd10ff1301ce39bb60cd8daf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154297412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39391f7d87fac7b43f0ed0b59b1981b263a30d3397f5f5244adf81cb7627ba5a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 02:47:03 GMT
ENV GIT_VERSION=2.23.0
# Thu, 16 Nov 2023 02:47:04 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 16 Nov 2023 02:47:05 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 16 Nov 2023 02:47:06 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 16 Nov 2023 02:48:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 02:48:31 GMT
ENV GOPATH=C:\go
# Thu, 16 Nov 2023 02:49:41 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Dec 2023 20:18:04 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:21:11 GMT
RUN $url = 'https://dl.google.com/go/go1.21.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bbe603cde7c9dee658f45164b4d06de1eff6e6e6b800100824e7c00d56a9a92f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Dec 2023 20:21:13 GMT
WORKDIR C:\go
# Tue, 05 Dec 2023 20:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Dec 2023 20:59:30 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:20:06 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:20:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:21:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 08 Dec 2023 20:21:15 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e901367fac1450f509d3118ada9e004e3613844ebdf91861147a093483930a4`  
		Last Modified: Thu, 16 Nov 2023 03:11:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e08004205bd077d8f22b013c70dc2f10796c64fced1eb9927e0055daff2d05d`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebc5048afc68ef48e2f2136545e2cccf26bb29eb4926bf4259b370ad55b4e7a`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f50fe5c7ef21648f3eaa4304932877a116fcb910b8e9095c779a2fbe6d57f7e`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76fe0e37750041d4ede2a0ca3b5245cfe075c3eb2ee27d7ce72ee8c3d7b20cc`  
		Last Modified: Thu, 16 Nov 2023 03:12:00 GMT  
		Size: 25.5 MB (25537512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8097bb9b8778d15dbf89d899653bf1634ec17554e5d84ef1ccfcac8ebf86afe2`  
		Last Modified: Thu, 16 Nov 2023 03:11:53 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b542d31e914d67da86cc5701cdc282ab664dc1170507e3802e22ab3026436a90`  
		Last Modified: Thu, 16 Nov 2023 03:11:53 GMT  
		Size: 263.2 KB (263200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86acdf7d3955fb44136bac433a30ccbbb97863120f270af32659dd65446666c7`  
		Last Modified: Tue, 05 Dec 2023 20:39:22 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1abe126c354944b7db8aa724d8f757167f7c3b36d39f976ef3b1b0d1b1b65ab`  
		Last Modified: Tue, 05 Dec 2023 20:39:41 GMT  
		Size: 69.4 MB (69361283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6338af096e09067ad482a0f4a6df1d1eee5b5595a64ca5f367b94ce27903e284`  
		Last Modified: Tue, 05 Dec 2023 20:39:22 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0adc218b27ef5639384c060fb663de3bd74374279d3fd525aa281f63a754779`  
		Last Modified: Tue, 05 Dec 2023 21:02:06 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c21053b248805df7ad888734f5cd1df5a6b426111512d5a6b7530060e7f30b2`  
		Last Modified: Tue, 05 Dec 2023 21:02:03 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034eb8f336a0d8e998c3eef6834d07c072c0679ccd4fde02cc8787ed46c80b19`  
		Last Modified: Fri, 08 Dec 2023 20:23:31 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af9b0b53a037a76c1c2e0e3afbe4fad733bc634a5ca02d53055360d9b7e33b9`  
		Last Modified: Fri, 08 Dec 2023 20:23:31 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f653ab9a896e2a3cfaf147a9ebb6e2d23f453cc3f953ee19b27333ebbc66460b`  
		Last Modified: Fri, 08 Dec 2023 20:23:32 GMT  
		Size: 1.7 MB (1685700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed98b1069776f09873a216052d2bf114c714b8269e4235d0aee375a2b0b7962`  
		Last Modified: Fri, 08 Dec 2023 20:23:31 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.20348.2113; amd64

```console
$ docker pull caddy@sha256:b1d94a17104c4814aa7672316e4c713aefcdfa6ffd19043f4111784c09931cda
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1983623336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61ba19fe8fdfa90a532d1f355b356c651a2921264135f6417c72193a5f37396`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 02:43:34 GMT
ENV GIT_VERSION=2.23.0
# Thu, 16 Nov 2023 02:43:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 16 Nov 2023 02:43:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 16 Nov 2023 02:43:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 16 Nov 2023 02:44:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 02:44:11 GMT
ENV GOPATH=C:\go
# Thu, 16 Nov 2023 02:44:30 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Dec 2023 20:15:35 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:17:49 GMT
RUN $url = 'https://dl.google.com/go/go1.21.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bbe603cde7c9dee658f45164b4d06de1eff6e6e6b800100824e7c00d56a9a92f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Dec 2023 20:17:50 GMT
WORKDIR C:\go
# Tue, 05 Dec 2023 21:00:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Dec 2023 21:00:58 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:21:33 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:21:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:21:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 08 Dec 2023 20:21:57 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b1d4a557f047b695f94452d9707061981d7fae4239c674b332282b8291963c`  
		Last Modified: Thu, 16 Nov 2023 03:11:20 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45549c207f14d769cba7c36b66157ec213bbc32ce57d685d8e2c407cf3987bb`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c674717e06bf8cb25d5887393ef9568ee0ab6390966b9666808e836e9bd471d`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2227badcd9f5f2b70b3d2ffd1c18887498f413c07802bfb334e8dc7b2d2acc`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9f3b5e90a2e6028cf194e870b24a7158f875f18b81f4f9137a5db3ea1f79ac`  
		Last Modified: Thu, 16 Nov 2023 03:11:23 GMT  
		Size: 25.5 MB (25536225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7811a5416dcd19193a5b3ab9327607bf845f7ff77f95d3e20abdfb7435c32ae0`  
		Last Modified: Thu, 16 Nov 2023 03:11:16 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5931209e960a94616639ea72e4d3ad9dc9cb554790ce930152c73bdc1449c034`  
		Last Modified: Thu, 16 Nov 2023 03:11:16 GMT  
		Size: 266.6 KB (266600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a70f603a2fb4e76edd3165b62a179fb8f6410e265f5ae4a3732ee68e610034b`  
		Last Modified: Tue, 05 Dec 2023 20:38:48 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e37840dec3a6665ce48520be8b2c51b654359765bee5ab0780ee74746f0eb2`  
		Last Modified: Tue, 05 Dec 2023 20:39:08 GMT  
		Size: 69.3 MB (69342960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d16ae54757acda093616d24735d4c92d4676649bec49807fc35de90d15e15c`  
		Last Modified: Tue, 05 Dec 2023 20:38:48 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5744d01eddd2ef9d9673fdb0f0e48203fad1b01f2b14899a3ec6393c4548e75`  
		Last Modified: Tue, 05 Dec 2023 21:02:23 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35bb848667aa413b6ce6c309a4c2169635b0740dc335b9b39413a00627c01ab`  
		Last Modified: Tue, 05 Dec 2023 21:02:21 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54630e9807bbb8995ce52459e6e3c8d818351c481e0ce29280570e90d0138d33`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f15ec018ec91e33ee96d4f0e6b66d9edb40b185a13f91d16f12d0bf682ab08b`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79cc8b934303f209cd48271252cb46966445a1099aac277ae4caf120af718ab`  
		Last Modified: Fri, 08 Dec 2023 20:23:49 GMT  
		Size: 1.7 MB (1677815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224f75043e75fb7c85d3daec88a29069c6ff40b8feeaa26bac868d524758955`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:a6d9bf50074feba4597d504f2c617c7d3e772c19b67d0ca788dcf2dcb421bd08
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
$ docker pull caddy@sha256:64cc92d77653c256c9cde397fb221c57907a57b0fe04f4e83ab2f7123f7f9147
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76963251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccce7adcc2b72b984adc9e5dd37663d1e6e512e39657c41bed43c55b38f9bad9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:46:23 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 03:46:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:25:52 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:26:01 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:26:02 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:26:02 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:26:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:26:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:26:03 GMT
WORKDIR /go
# Tue, 05 Dec 2023 20:48:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 20:48:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:39:46 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:39:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:39:46 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 20:39:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 20:39:47 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 20:39:47 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5501dced60f86be38cc73d3c038f7db4afeee65726f7e422aacf09244539ebf1`  
		Last Modified: Fri, 01 Dec 2023 03:50:39 GMT  
		Size: 284.7 KB (284697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63d189496f5f03c835c9c85df2db6920546d36a1701f6b5ad15f800c671605d`  
		Last Modified: Tue, 05 Dec 2023 20:31:27 GMT  
		Size: 67.0 MB (67003308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aeb88dd0f3e06a57abc08c781b85c89d138194918c469aea9a1bed9753d2ed0`  
		Last Modified: Tue, 05 Dec 2023 20:31:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40ff2505fd8d96e76bddb63b05c2d42815db1dabe0093ec8f8f53be403b0d01`  
		Last Modified: Tue, 05 Dec 2023 20:49:17 GMT  
		Size: 5.0 MB (4970029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ba23d637be879f93c12d4e6d077eb636688fa34e5d637f1f9a2f0a28509f0d`  
		Last Modified: Fri, 08 Dec 2023 20:40:19 GMT  
		Size: 1.3 MB (1302232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57ad5b5be9e26b4f05c8402814544f231f87d6a736a05320421e0ce2e623f04`  
		Last Modified: Fri, 08 Dec 2023 20:40:19 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:cd2d4a5ddcdef2492b7b440240d2e3beffa1695c0a1273227efdbc97a0fddc86
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75411895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed519bbe9039d7d32e60f9e1c959613953c4508dc6dd1506a355f0e0fd39bbe7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:53:48 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 00:53:48 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:49:18 GMT
ENV GOLANG_VERSION=1.21.5
# Sat, 09 Dec 2023 01:49:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	elif [ "$arch" = 'armv7' ]; then 		[ -s /usr/local/go/go.env ]; 		before="$(go env GOARM)"; [ "$before" != '7' ]; 		{ 			echo; 			echo '# https://github.com/docker-library/golang/issues/494'; 			echo 'GOARM=7'; 		} >> /usr/local/go/go.env; 		after="$(go env GOARM)"; [ "$after" = '7' ]; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Sat, 09 Dec 2023 01:49:51 GMT
ENV GOTOOLCHAIN=local
# Sat, 09 Dec 2023 01:49:51 GMT
ENV GOPATH=/go
# Sat, 09 Dec 2023 01:49:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 01:49:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Sat, 09 Dec 2023 01:49:52 GMT
WORKDIR /go
# Sat, 09 Dec 2023 02:08:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 09 Dec 2023 02:08:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 09 Dec 2023 02:08:59 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 09 Dec 2023 02:08:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 09 Dec 2023 02:08:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 09 Dec 2023 02:09:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 09 Dec 2023 02:09:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 09 Dec 2023 02:09:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e7ba0492eb25e7f21078441d7cdc65088836bc1984bc4a14cd3e9cd75cbf32`  
		Last Modified: Fri, 01 Dec 2023 01:00:23 GMT  
		Size: 284.9 KB (284884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbf3e566edb99ecb0ecb757d0f571633d7d822bf31896dd76a40ff9d89e98c0`  
		Last Modified: Sat, 09 Dec 2023 01:53:04 GMT  
		Size: 65.8 MB (65764277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e170d213450f3f3c66f85329ded2a75a6b38e5b51cfe01f2ad9d2cc2aab61079`  
		Last Modified: Sat, 09 Dec 2023 01:52:51 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612473e16b229d3c58615a469f9ca073ec9dc483d79cd7bb87479eea58ee5454`  
		Last Modified: Sat, 09 Dec 2023 02:09:20 GMT  
		Size: 5.0 MB (4966653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ed572067dfce272b021aee6f0cd14272e2a1157f0cf11ad00004a5c9354bc0`  
		Last Modified: Sat, 09 Dec 2023 02:09:19 GMT  
		Size: 1.2 MB (1248652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7608cc7cd78c6c2f18a53621dbd0b1746b9274ce1b35a8279b261816e41718ef`  
		Last Modified: Sat, 09 Dec 2023 02:09:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:7b8943fed6d62476c9dea44a16caea83fb6d540be101271d0974e0f2ed5a1567
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74707178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e459d7afebbd1af456db2bc6e8849445ca45f2586a9bbd0337ba314f570a177`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:44:57 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 08:44:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:58:01 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:58:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:58:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:58:16 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:58:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:58:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:58:17 GMT
WORKDIR /go
# Tue, 05 Dec 2023 21:22:31 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 21:22:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:16:31 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:16:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:16:32 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 20:16:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 20:16:34 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 20:16:34 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a824ff289f1a3c765a444079137b8b7f1cee80348faa53e1ba4c960b73ed2a`  
		Last Modified: Fri, 01 Dec 2023 08:49:42 GMT  
		Size: 284.1 KB (284079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4989177b4ed66b7e9f9e8c4bfce82720b582e24b735d6628effa75d81c5718fc`  
		Last Modified: Tue, 05 Dec 2023 21:04:43 GMT  
		Size: 65.8 MB (65764197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f9b58eae167c54d3faa3eeffd480cdae7e8b4841eb816a86cfdd01f8ae29ef`  
		Last Modified: Tue, 05 Dec 2023 21:04:29 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4cd1a3aab8fc02791b1e19f81b7de1bd691c10a7c942acc7e733221bf12888`  
		Last Modified: Tue, 05 Dec 2023 21:22:47 GMT  
		Size: 4.5 MB (4511237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c6a5bcaed596afac229d37cd822ea4770b06d4d3580d14a71d26e32136f1aa`  
		Last Modified: Fri, 08 Dec 2023 20:17:09 GMT  
		Size: 1.2 MB (1246093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c59154934645e7c4d44eda6d3d5ea9d4b32e23fbf7ccb7009cc54413ae815d`  
		Last Modified: Fri, 08 Dec 2023 20:17:09 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:3fce35ec600b6e48bb63c1b2d390b6d515a6f0e7355b582fcb347092222bdc37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73981648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3475cc52d42bfd049fb20d388ecf6c8482841b98a265b9fc09b60bc815011df9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:43:53 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 03:18:30 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:16:18 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:16:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:16:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:16:28 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:16:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:16:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:16:28 GMT
WORKDIR /go
# Tue, 05 Dec 2023 20:38:16 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 20:38:16 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 19:55:21 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 19:55:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 19:55:21 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 19:55:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 19:55:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 19:55:22 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a63ed24dc22a348b35d99b5ec9dc67ff66563b539875e5c8ab2d870b3991ac`  
		Last Modified: Fri, 01 Dec 2023 02:44:03 GMT  
		Size: 286.3 KB (286307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f00641dffc5c2a149049ee9046bb24cfc7de534b7495a0f27784a4fff0fadc`  
		Last Modified: Tue, 05 Dec 2023 20:21:00 GMT  
		Size: 64.1 MB (64094844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452682ba77e89fc55be3a168358f5f43bccad93ecdd3d53b4dec7fff6915128b`  
		Last Modified: Tue, 05 Dec 2023 20:20:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3fe1e12507f8c4a2731393eebfc5ab973aa344b0daceec525560b812b26f60`  
		Last Modified: Tue, 05 Dec 2023 20:38:33 GMT  
		Size: 5.1 MB (5068450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1568fb18f5eae3df776dd2fee8d447615d0f62601f82ebdb1bf2af5155bb83`  
		Last Modified: Fri, 08 Dec 2023 19:55:49 GMT  
		Size: 1.2 MB (1198450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15988851efd259492be8e7583025cb2b00f7477442c7be3e2d3dd97adbc39e76`  
		Last Modified: Fri, 08 Dec 2023 19:55:48 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:e21739ed4cecc54ebd496b12fa757f5901f3c0b45d211c0c5fa2ef551543c2d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74206507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed778e73218e8613cd2044f7eb703ec05bf43271d444ca5ffe77e053baa719c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:37:34 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 06:37:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:38:14 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:38:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Dec 2023 20:38:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Dec 2023 20:38:38 GMT
ENV GOPATH=/go
# Tue, 05 Dec 2023 20:38:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:38:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 05 Dec 2023 20:38:41 GMT
WORKDIR /go
# Tue, 05 Dec 2023 21:04:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Dec 2023 21:04:34 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:22:32 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:22:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:22:33 GMT
ENV XCADDY_SETCAP=1
# Fri, 08 Dec 2023 20:22:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Fri, 08 Dec 2023 20:22:35 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Fri, 08 Dec 2023 20:22:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692dbecd5e141c462ab06ef113ec964b525e7564d734890cc1d5b1dbf33ee34e`  
		Last Modified: Fri, 01 Dec 2023 06:43:30 GMT  
		Size: 286.7 KB (286661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc89a0f2d97ecfd4d20235e72227fc24aa79a64509fe9ea64702db658f2ad26d`  
		Last Modified: Tue, 05 Dec 2023 20:46:23 GMT  
		Size: 64.1 MB (64115804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d76f2c2e2bbb4190b1865ddafdc8cb88adee4c79d7d5ba23e69696e9610889`  
		Last Modified: Tue, 05 Dec 2023 20:46:11 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e0ec0f713ee657d6aa159fab65c05939480b5ca50a8e3dc4b1a9a6578160f7`  
		Last Modified: Tue, 05 Dec 2023 21:04:57 GMT  
		Size: 5.3 MB (5268970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbd7401349780157d6d930ec942f00b1d5404d31ae60bff5c7b41238cf8e3b1`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 1.2 MB (1186185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67206b5e4434d3211a98a71837832baed45e4fb0c03ff8dc204bc7762a8ab559`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:bf201fa7da491e4decf9c0a638b9fbcb4b459d5b13bcc9a2f4c0fb4c583c609b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76101050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e2b3cda7ff391c43b985fdbd1c3515e69b6fbe94f8ea6c9a09749c147e491c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:14:49 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 08:14:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 20:44:16 GMT
ENV GOLANG_VERSION=1.21.5
# Sat, 09 Dec 2023 01:50:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.5.src.tar.gz'; 		sha256='285cbbdf4b6e6e62ed58f370f3f6d8c30825d6e56c5853c66d3c23bcdb09db19'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	elif [ "$arch" = 'armv7' ]; then 		[ -s /usr/local/go/go.env ]; 		before="$(go env GOARM)"; [ "$before" != '7' ]; 		{ 			echo; 			echo '# https://github.com/docker-library/golang/issues/494'; 			echo 'GOARM=7'; 		} >> /usr/local/go/go.env; 		after="$(go env GOARM)"; [ "$after" = '7' ]; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Sat, 09 Dec 2023 01:50:41 GMT
ENV GOTOOLCHAIN=local
# Sat, 09 Dec 2023 01:50:41 GMT
ENV GOPATH=/go
# Sat, 09 Dec 2023 01:50:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 01:50:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Sat, 09 Dec 2023 01:50:42 GMT
WORKDIR /go
# Sat, 09 Dec 2023 02:12:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 09 Dec 2023 02:12:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 09 Dec 2023 02:12:31 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 09 Dec 2023 02:12:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 09 Dec 2023 02:12:31 GMT
ENV XCADDY_SETCAP=1
# Sat, 09 Dec 2023 02:12:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 09 Dec 2023 02:12:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 09 Dec 2023 02:12:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab563e8d41683e124df048aa9b564b0e8e1021e85213666971a015df51d5e48`  
		Last Modified: Fri, 01 Dec 2023 08:20:46 GMT  
		Size: 285.1 KB (285090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c541c9463bd8d06e97aa1b14ce0792cf2caf6ef8ddc7b046b21032b3390bee`  
		Last Modified: Sat, 09 Dec 2023 01:54:50 GMT  
		Size: 66.2 MB (66218593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236faa4ca6aed551be037e8e0a2312e72dedf504cdffa8d2015882df02c5b87e`  
		Last Modified: Sat, 09 Dec 2023 01:54:39 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee294f5771410ee01c59c398d0270a28f5ae4caff9abfa5339f1c54b1dc1ab5a`  
		Last Modified: Sat, 09 Dec 2023 02:12:56 GMT  
		Size: 5.1 MB (5116966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cbd016bf9fbfd249882a217530ca94dcac095e46620a64badd9bbfa6ae9ebe`  
		Last Modified: Sat, 09 Dec 2023 02:12:55 GMT  
		Size: 1.3 MB (1262386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b36774ae94aa93a3beb6e355ee08897437b53c870bc56fdc3047ce591cfa2ac`  
		Last Modified: Sat, 09 Dec 2023 02:12:55 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:8bf37ab9a085a9916fcfb4a921ebbfe2d29d2893fac56672655cc8ccd5fa3c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull caddy@sha256:cdab1fd140455df0674bfedde2f4948b5289720efd10ff1301ce39bb60cd8daf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154297412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39391f7d87fac7b43f0ed0b59b1981b263a30d3397f5f5244adf81cb7627ba5a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 02:47:03 GMT
ENV GIT_VERSION=2.23.0
# Thu, 16 Nov 2023 02:47:04 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 16 Nov 2023 02:47:05 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 16 Nov 2023 02:47:06 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 16 Nov 2023 02:48:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 02:48:31 GMT
ENV GOPATH=C:\go
# Thu, 16 Nov 2023 02:49:41 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Dec 2023 20:18:04 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:21:11 GMT
RUN $url = 'https://dl.google.com/go/go1.21.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bbe603cde7c9dee658f45164b4d06de1eff6e6e6b800100824e7c00d56a9a92f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Dec 2023 20:21:13 GMT
WORKDIR C:\go
# Tue, 05 Dec 2023 20:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Dec 2023 20:59:30 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:20:06 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:20:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:21:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 08 Dec 2023 20:21:15 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e901367fac1450f509d3118ada9e004e3613844ebdf91861147a093483930a4`  
		Last Modified: Thu, 16 Nov 2023 03:11:57 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e08004205bd077d8f22b013c70dc2f10796c64fced1eb9927e0055daff2d05d`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebc5048afc68ef48e2f2136545e2cccf26bb29eb4926bf4259b370ad55b4e7a`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f50fe5c7ef21648f3eaa4304932877a116fcb910b8e9095c779a2fbe6d57f7e`  
		Last Modified: Thu, 16 Nov 2023 03:11:55 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76fe0e37750041d4ede2a0ca3b5245cfe075c3eb2ee27d7ce72ee8c3d7b20cc`  
		Last Modified: Thu, 16 Nov 2023 03:12:00 GMT  
		Size: 25.5 MB (25537512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8097bb9b8778d15dbf89d899653bf1634ec17554e5d84ef1ccfcac8ebf86afe2`  
		Last Modified: Thu, 16 Nov 2023 03:11:53 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b542d31e914d67da86cc5701cdc282ab664dc1170507e3802e22ab3026436a90`  
		Last Modified: Thu, 16 Nov 2023 03:11:53 GMT  
		Size: 263.2 KB (263200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86acdf7d3955fb44136bac433a30ccbbb97863120f270af32659dd65446666c7`  
		Last Modified: Tue, 05 Dec 2023 20:39:22 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1abe126c354944b7db8aa724d8f757167f7c3b36d39f976ef3b1b0d1b1b65ab`  
		Last Modified: Tue, 05 Dec 2023 20:39:41 GMT  
		Size: 69.4 MB (69361283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6338af096e09067ad482a0f4a6df1d1eee5b5595a64ca5f367b94ce27903e284`  
		Last Modified: Tue, 05 Dec 2023 20:39:22 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0adc218b27ef5639384c060fb663de3bd74374279d3fd525aa281f63a754779`  
		Last Modified: Tue, 05 Dec 2023 21:02:06 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c21053b248805df7ad888734f5cd1df5a6b426111512d5a6b7530060e7f30b2`  
		Last Modified: Tue, 05 Dec 2023 21:02:03 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034eb8f336a0d8e998c3eef6834d07c072c0679ccd4fde02cc8787ed46c80b19`  
		Last Modified: Fri, 08 Dec 2023 20:23:31 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af9b0b53a037a76c1c2e0e3afbe4fad733bc634a5ca02d53055360d9b7e33b9`  
		Last Modified: Fri, 08 Dec 2023 20:23:31 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f653ab9a896e2a3cfaf147a9ebb6e2d23f453cc3f953ee19b27333ebbc66460b`  
		Last Modified: Fri, 08 Dec 2023 20:23:32 GMT  
		Size: 1.7 MB (1685700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed98b1069776f09873a216052d2bf114c714b8269e4235d0aee375a2b0b7962`  
		Last Modified: Fri, 08 Dec 2023 20:23:31 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:b944570c2f667cfb312913d3478de80037fe9967f6fd20a1358e3f1b87467164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull caddy@sha256:b1d94a17104c4814aa7672316e4c713aefcdfa6ffd19043f4111784c09931cda
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1983623336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61ba19fe8fdfa90a532d1f355b356c651a2921264135f6417c72193a5f37396`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 02:43:34 GMT
ENV GIT_VERSION=2.23.0
# Thu, 16 Nov 2023 02:43:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 16 Nov 2023 02:43:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 16 Nov 2023 02:43:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 16 Nov 2023 02:44:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 02:44:11 GMT
ENV GOPATH=C:\go
# Thu, 16 Nov 2023 02:44:30 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Dec 2023 20:15:35 GMT
ENV GOLANG_VERSION=1.21.5
# Tue, 05 Dec 2023 20:17:49 GMT
RUN $url = 'https://dl.google.com/go/go1.21.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bbe603cde7c9dee658f45164b4d06de1eff6e6e6b800100824e7c00d56a9a92f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Dec 2023 20:17:50 GMT
WORKDIR C:\go
# Tue, 05 Dec 2023 21:00:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Dec 2023 21:00:58 GMT
ENV XCADDY_VERSION=v0.3.5
# Fri, 08 Dec 2023 20:21:33 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:21:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 08 Dec 2023 20:21:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Fri, 08 Dec 2023 20:21:57 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b1d4a557f047b695f94452d9707061981d7fae4239c674b332282b8291963c`  
		Last Modified: Thu, 16 Nov 2023 03:11:20 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45549c207f14d769cba7c36b66157ec213bbc32ce57d685d8e2c407cf3987bb`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c674717e06bf8cb25d5887393ef9568ee0ab6390966b9666808e836e9bd471d`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2227badcd9f5f2b70b3d2ffd1c18887498f413c07802bfb334e8dc7b2d2acc`  
		Last Modified: Thu, 16 Nov 2023 03:11:18 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9f3b5e90a2e6028cf194e870b24a7158f875f18b81f4f9137a5db3ea1f79ac`  
		Last Modified: Thu, 16 Nov 2023 03:11:23 GMT  
		Size: 25.5 MB (25536225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7811a5416dcd19193a5b3ab9327607bf845f7ff77f95d3e20abdfb7435c32ae0`  
		Last Modified: Thu, 16 Nov 2023 03:11:16 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5931209e960a94616639ea72e4d3ad9dc9cb554790ce930152c73bdc1449c034`  
		Last Modified: Thu, 16 Nov 2023 03:11:16 GMT  
		Size: 266.6 KB (266600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a70f603a2fb4e76edd3165b62a179fb8f6410e265f5ae4a3732ee68e610034b`  
		Last Modified: Tue, 05 Dec 2023 20:38:48 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e37840dec3a6665ce48520be8b2c51b654359765bee5ab0780ee74746f0eb2`  
		Last Modified: Tue, 05 Dec 2023 20:39:08 GMT  
		Size: 69.3 MB (69342960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d16ae54757acda093616d24735d4c92d4676649bec49807fc35de90d15e15c`  
		Last Modified: Tue, 05 Dec 2023 20:38:48 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5744d01eddd2ef9d9673fdb0f0e48203fad1b01f2b14899a3ec6393c4548e75`  
		Last Modified: Tue, 05 Dec 2023 21:02:23 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35bb848667aa413b6ce6c309a4c2169635b0740dc335b9b39413a00627c01ab`  
		Last Modified: Tue, 05 Dec 2023 21:02:21 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54630e9807bbb8995ce52459e6e3c8d818351c481e0ce29280570e90d0138d33`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f15ec018ec91e33ee96d4f0e6b66d9edb40b185a13f91d16f12d0bf682ab08b`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79cc8b934303f209cd48271252cb46966445a1099aac277ae4caf120af718ab`  
		Last Modified: Fri, 08 Dec 2023 20:23:49 GMT  
		Size: 1.7 MB (1677815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224f75043e75fb7c85d3daec88a29069c6ff40b8feeaa26bac868d524758955`  
		Last Modified: Fri, 08 Dec 2023 20:23:48 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:e523a9bc9e19fb96a082b4d83ebae2ce6267f56f2b7b4ac462135ebc51f68e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5122; amd64
	-	windows version 10.0.20348.2113; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:7b8b4b0a4784433bd53271ff8f27d0940f96b1e633bb69b27d2c9ac5a293536a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18467236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657b947906e764d7ff65a638b958cb7f84b3754e49ede071620658385e743168`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:32:06 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:39:38 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:39:38 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:39:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:39:41 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:39:41 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:39:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:39:41 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:39:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:39:42 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:39:42 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:39:42 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:39:42 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08886dfc0722c4ed2cb6a70c285a33fe35aec069435868488356dde320b4d21c`  
		Last Modified: Fri, 01 Dec 2023 06:32:30 GMT  
		Size: 350.8 KB (350845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd2155878b9ec9d659128d039d90b8a50369fe85c88f64a597b6a9cd9441c1b`  
		Last Modified: Fri, 08 Dec 2023 20:40:01 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7343593237d1bd5fb218804e360a7a8c4d94d7af8da4eb1a72fbaf48fab9ce2`  
		Last Modified: Fri, 08 Dec 2023 20:40:03 GMT  
		Size: 14.7 MB (14706441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:fe42da7df688686dab79fb02be7f13aae32c9a9f84eec3b28b634cc48d5a7346
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17423030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f95b690a9e892f56dbf3fd455d714c2d22ebd35967fdc770fb704c870eeffc`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:39:01 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:07:47 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:07:47 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:07:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:07:50 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:07:50 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:07:50 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:07:51 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:07:51 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:07:51 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:07:51 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:07:51 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc24e4ccf558b6e992efaaa7a735322be11fe99ce19e722eee6ae70bb76515d`  
		Last Modified: Fri, 01 Dec 2023 00:39:21 GMT  
		Size: 347.6 KB (347632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1775b4c8558ad1bf8d7568fc741be39ee2a28ecdd33f84ed7597b6192873a81a`  
		Last Modified: Fri, 08 Dec 2023 20:08:10 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbf57a0db316ab6b42386b0221d652cc4f9d9d597206ce1d4e9bfd5ba0f7777`  
		Last Modified: Fri, 08 Dec 2023 20:08:12 GMT  
		Size: 13.9 MB (13920999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:cf486c3cc2b7d7cc0bdfc8db52605e6a533c0528e717b2ccd6e9779713d72229
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17146731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68a807660343335d38b999c8c1b687f5ec5c882c6f5180e13281152b030f103`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:19:12 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:16:22 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:16:22 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:16:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:16:25 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:16:26 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:16:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:16:27 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:16:27 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:16:27 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:16:28 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:16:28 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:16:28 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:16:28 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803b34e1f84b29ca968d2fbf85c278608566c34dfd1742e088c6483685957029`  
		Last Modified: Fri, 01 Dec 2023 03:19:48 GMT  
		Size: 344.5 KB (344464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de504bcc2429a4454910b605f8bb2f6eec4cad953044e48d02a7d51542b7266f`  
		Last Modified: Fri, 08 Dec 2023 20:16:53 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73099274a85e30e93cb0e71106c443fd9a5b923ef43adabf808db6a58db9ad8b`  
		Last Modified: Fri, 08 Dec 2023 20:16:56 GMT  
		Size: 13.9 MB (13893732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:71069b6f75345cd8b5e4841d92dcaebb4fa2acf454074eeb2c571517ac3671cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae18940ab920c723e970d89fde606b552e5b39f5fa33535cb6c7be09b6cff763`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:11:08 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 19:55:15 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 19:55:16 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 19:55:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 19:55:17 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 19:55:17 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 19:55:17 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 19:55:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 80
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 443
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 19:55:18 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 19:55:18 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 19:55:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e383270d6915b6b427f49a75d657d5a0403fcd47a5f89cd30e85143ca54c22`  
		Last Modified: Fri, 01 Dec 2023 03:11:28 GMT  
		Size: 360.7 KB (360655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f87e6bdbafc6710a3ed7bfbb4bb134e8d93bea992ab895c653cac0779389396`  
		Last Modified: Fri, 08 Dec 2023 19:55:35 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874486d3ac5891d4df17819e02e1cdd3775748effa24bc53645cd2db841a0837`  
		Last Modified: Fri, 08 Dec 2023 19:55:36 GMT  
		Size: 13.6 MB (13568967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:9991e527a64c1d20422e24e141a57efec5365c7bcd68662808b0ea23da815b3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17051913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274840ad1c2fe6344d298e9d6242bde6e602b3444a071cfe45d3db4360d193b4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:42:19 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 20:22:14 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 20:22:14 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:22:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 20:22:19 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 20:22:19 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 20:22:19 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:22:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:22:20 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:22:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:22:22 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:22:22 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:22:23 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:22:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:22:24 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:22:24 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:22:25 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:22:25 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:22:26 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 20:22:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce4bc2907f69809c3086f118895d7e5c8683349557239c0ce79dfbda0ce3768`  
		Last Modified: Fri, 01 Dec 2023 05:44:17 GMT  
		Size: 362.2 KB (362185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3c2787bdbaa50fce90e65038b2dbc9850d2fff68d5e731bcdb83c71ede912b`  
		Last Modified: Fri, 08 Dec 2023 20:22:53 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ce50c6341ede9fe5f61cc3a75eb534b7dd1172b7e88c015862cb9351c91ca1`  
		Last Modified: Fri, 08 Dec 2023 20:22:55 GMT  
		Size: 13.3 MB (13333877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:f8db25c8783258ee73a7ab061dbcb53f5229be2510ab4c72cbb6fe5292fdd1a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17818230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4782f6a3e2f343e87b335a56846d9ae67a4a5aded358a8501a4fb5a076e92cef`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:22:31 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 08 Dec 2023 19:57:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 08 Dec 2023 19:57:07 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 19:57:10 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 08 Dec 2023 19:57:11 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 19:57:11 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 19:57:12 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 19:57:13 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 19:57:13 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 19:57:13 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 19:57:13 GMT
EXPOSE 80
# Fri, 08 Dec 2023 19:57:13 GMT
EXPOSE 443
# Fri, 08 Dec 2023 19:57:14 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 19:57:14 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 19:57:14 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 19:57:14 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20bbe0abb0a3f63718aa78742832077ad86b8ae86d70ce3ebcece342ec022c6`  
		Last Modified: Fri, 01 Dec 2023 08:23:07 GMT  
		Size: 354.9 KB (354948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa042ad4816c33e4f907bbf008abef2397efe2b3fc378430b2b925663a088370`  
		Last Modified: Fri, 08 Dec 2023 19:57:43 GMT  
		Size: 7.5 KB (7526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ceec9a3d819911fec4d039d31e2e3e38214fa45cb8384e8f047b5588724355`  
		Last Modified: Fri, 08 Dec 2023 19:57:45 GMT  
		Size: 14.2 MB (14238302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.5122; amd64

```console
$ docker pull caddy@sha256:3d281f8c1d34b38abb3b5ca4ff98d70312daad9b0654a470374d0447a69a3ccf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073448315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e423604e6f05b59d8afa51e2d09a8fc11e1ac3353a126e3ce73b1c2bc65872b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:16:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:16:25 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:17:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:17:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:17:34 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:17:35 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:17:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:17:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:17:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:17:41 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:17:43 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:18:34 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:18:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09e9b6b38c0082853f1d6caa4d3536344a04da2aa5b674837aba8781b265e0d`  
		Last Modified: Fri, 08 Dec 2023 20:22:45 GMT  
		Size: 462.7 KB (462693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb778801cf9547a5b9021d3090bd8e4fc05f09e3aed56b6950dcbd044211d3f`  
		Last Modified: Fri, 08 Dec 2023 20:22:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ec815279848293cd980ed43a496bf4d3e8f8035f8d46dd1a3278e02c4558a8`  
		Last Modified: Fri, 08 Dec 2023 20:22:46 GMT  
		Size: 15.3 MB (15274633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9671feff108f8e0d8be270b64952394b3eaf7d16a7e9163cffc500ad3a42bd17`  
		Last Modified: Fri, 08 Dec 2023 20:22:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44f97706c45d8ebb4578d93d6c1cb5ecc4625f2f78fa40f25f9e72af014449a`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7b5732d0f0e4f61cac2e09f77054657b1bfc21c56b5b4b842e96ee7de3d45d`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348bbb9a26a300473cbb347ce3e405736e7a71ef7d2e67068452760fe4a1a67e`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4dc80dd8b7091a5cb553a95c06fa14380bf94a6f80467e3d7a36cb649fce8c`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6e2ab9cd2c6c903f643bcab22655dc93ec72fcc2f748a47375e2209580eed8`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a498a93a315d79030214cb59d847ede547dfc1159616120a3b48f2b1585bccfc`  
		Last Modified: Fri, 08 Dec 2023 20:22:40 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a7d0f8e26a8dd06b83bb38bfecf51f24ec1456947f459528e71b2544d13f5`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0da3c95480c1f76c862487e0683bed75c660c5cce3e3864677b8c956228e64`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1712e0793bc7067adabbb602cf9eaf0e6ab60f33be0b2b10282325884270ab07`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26aa77bbc553e8bf9318552da7ffe35258b387e04151dd211a006f50cb57a6`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e384f6873d9619640183b8c67671c94c80eb3725ac52c312de84b314b2cd4c53`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7ecef2ca51e4738a30164e40d773f9bfcc9a55bda13a00745349db1618fbf0`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29866626f3b37691b2e593b7ad8a6d3f6e916d9ca428c22e1b3834e568c605c9`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dff7ab50f452876c91da33fe48a0e1409de6cbb0ffca4e1aefa68caa5722d01`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 256.7 KB (256705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55865895b10a6247b60406c70eaa3584e7904512f0092bd7d9013bd9fe64c740`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.20348.2113; amd64

```console
$ docker pull caddy@sha256:cca2801fca8e41625ec6c3c42ee17cc76b64320f93ec2c37999b29b5f9ff0747
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1902845713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ad0d44150328d8253edf3d339d33f508e3a25395c8fd773d2d2fe5966eb244`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:19:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:19:10 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:19:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:19:34 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:19:35 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:19:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:19:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:19:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:19:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:19:43 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:19:44 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:19:58 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:19:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9e496904b6bbc7ce10b08f4c5c00b922d19bb8ebfca4735ba504c9ca77dd2b`  
		Last Modified: Fri, 08 Dec 2023 20:23:12 GMT  
		Size: 474.4 KB (474429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d370d88e3c2ee411f6f86dd892eba2c381cf5706823fcf82fec94a47d7d3bb4`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1861a873425170bdbe2b563cd2b9584401a7be0e3d9a6ceac998eef4eab482ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:13 GMT  
		Size: 15.3 MB (15274241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e17c8887831a9d0a255eb44daaaedffc1bb98b51fc0177786dd130c85034006`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2595203a1e7cbe5c30c3a77633ff7b832c6f07580e688e7c2bc89b5442e72ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b5a75922e76c5c96d069952df83b51d1243d2d6955db5b45dd7b63aea2b3a1`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bbe845ab80dc71320eea94c3d56888074ea930dc6fbe934c60e6c801e9cee3`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74052a6ffee1242926db0907e5406b7e5d81e181d3c9c266d381aaf221bf0252`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbd2ebe3b760156655b6475d7ff52b549e20b5115cf815016c902f834bf3f14`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5945b936f7903435999bc26916fd896f5c645c5b70834243317e66b14d7c2d97`  
		Last Modified: Fri, 08 Dec 2023 20:23:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4345b37fb7af089771ba8cf5542de3045ebb0f1d247ea038535504b320c4ac2c`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12593e8f188e5024af21891d9f3141bc5b85d9e2e9e2b61d7c2634f9f491b9a4`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3632692d5118ec05512cfb67c4aa09a8dfdfe1e40467dfc5ee8e5d2e9a349b2a`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e694808297bceaf6299316f20be2a78e4d2eef8a2ca455dd79ce544cf0a00e66`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258e53ea4c6d9b42de13f722ade5338a5393993985f05ca5b438982dde948654`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20692d7b4da06a40fca6c59bffc5e13dc0a0ffc429f70ed8701dc1d5d8c087fd`  
		Last Modified: Fri, 08 Dec 2023 20:23:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f686dbb1484378b8f73bbbfac32eb04d8f9a6b2b3f4db7d17c1f997941475a7f`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84003630e1340399082b07e0df6cb438545136bc3f0c134d52e8fe9d878e7239`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 292.2 KB (292197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9991bbf8fb125121b7478726325dcb657bfbeb24af279019b7b2f7ac0c404f7`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:23526c514f90e81e3b94593ed41182252a81ba946c70cf1d2638381f84849d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.5122; amd64
	-	windows version 10.0.20348.2113; amd64

### `caddy:windowsservercore` - windows version 10.0.17763.5122; amd64

```console
$ docker pull caddy@sha256:3d281f8c1d34b38abb3b5ca4ff98d70312daad9b0654a470374d0447a69a3ccf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073448315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e423604e6f05b59d8afa51e2d09a8fc11e1ac3353a126e3ce73b1c2bc65872b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:16:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:16:25 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:17:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:17:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:17:34 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:17:35 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:17:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:17:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:17:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:17:41 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:17:43 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:18:34 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:18:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09e9b6b38c0082853f1d6caa4d3536344a04da2aa5b674837aba8781b265e0d`  
		Last Modified: Fri, 08 Dec 2023 20:22:45 GMT  
		Size: 462.7 KB (462693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb778801cf9547a5b9021d3090bd8e4fc05f09e3aed56b6950dcbd044211d3f`  
		Last Modified: Fri, 08 Dec 2023 20:22:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ec815279848293cd980ed43a496bf4d3e8f8035f8d46dd1a3278e02c4558a8`  
		Last Modified: Fri, 08 Dec 2023 20:22:46 GMT  
		Size: 15.3 MB (15274633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9671feff108f8e0d8be270b64952394b3eaf7d16a7e9163cffc500ad3a42bd17`  
		Last Modified: Fri, 08 Dec 2023 20:22:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44f97706c45d8ebb4578d93d6c1cb5ecc4625f2f78fa40f25f9e72af014449a`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7b5732d0f0e4f61cac2e09f77054657b1bfc21c56b5b4b842e96ee7de3d45d`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348bbb9a26a300473cbb347ce3e405736e7a71ef7d2e67068452760fe4a1a67e`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4dc80dd8b7091a5cb553a95c06fa14380bf94a6f80467e3d7a36cb649fce8c`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6e2ab9cd2c6c903f643bcab22655dc93ec72fcc2f748a47375e2209580eed8`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a498a93a315d79030214cb59d847ede547dfc1159616120a3b48f2b1585bccfc`  
		Last Modified: Fri, 08 Dec 2023 20:22:40 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a7d0f8e26a8dd06b83bb38bfecf51f24ec1456947f459528e71b2544d13f5`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0da3c95480c1f76c862487e0683bed75c660c5cce3e3864677b8c956228e64`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1712e0793bc7067adabbb602cf9eaf0e6ab60f33be0b2b10282325884270ab07`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26aa77bbc553e8bf9318552da7ffe35258b387e04151dd211a006f50cb57a6`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e384f6873d9619640183b8c67671c94c80eb3725ac52c312de84b314b2cd4c53`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7ecef2ca51e4738a30164e40d773f9bfcc9a55bda13a00745349db1618fbf0`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29866626f3b37691b2e593b7ad8a6d3f6e916d9ca428c22e1b3834e568c605c9`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dff7ab50f452876c91da33fe48a0e1409de6cbb0ffca4e1aefa68caa5722d01`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 256.7 KB (256705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55865895b10a6247b60406c70eaa3584e7904512f0092bd7d9013bd9fe64c740`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.20348.2113; amd64

```console
$ docker pull caddy@sha256:cca2801fca8e41625ec6c3c42ee17cc76b64320f93ec2c37999b29b5f9ff0747
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1902845713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ad0d44150328d8253edf3d339d33f508e3a25395c8fd773d2d2fe5966eb244`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:19:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:19:10 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:19:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:19:34 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:19:35 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:19:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:19:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:19:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:19:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:19:43 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:19:44 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:19:58 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:19:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9e496904b6bbc7ce10b08f4c5c00b922d19bb8ebfca4735ba504c9ca77dd2b`  
		Last Modified: Fri, 08 Dec 2023 20:23:12 GMT  
		Size: 474.4 KB (474429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d370d88e3c2ee411f6f86dd892eba2c381cf5706823fcf82fec94a47d7d3bb4`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1861a873425170bdbe2b563cd2b9584401a7be0e3d9a6ceac998eef4eab482ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:13 GMT  
		Size: 15.3 MB (15274241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e17c8887831a9d0a255eb44daaaedffc1bb98b51fc0177786dd130c85034006`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2595203a1e7cbe5c30c3a77633ff7b832c6f07580e688e7c2bc89b5442e72ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b5a75922e76c5c96d069952df83b51d1243d2d6955db5b45dd7b63aea2b3a1`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bbe845ab80dc71320eea94c3d56888074ea930dc6fbe934c60e6c801e9cee3`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74052a6ffee1242926db0907e5406b7e5d81e181d3c9c266d381aaf221bf0252`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbd2ebe3b760156655b6475d7ff52b549e20b5115cf815016c902f834bf3f14`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5945b936f7903435999bc26916fd896f5c645c5b70834243317e66b14d7c2d97`  
		Last Modified: Fri, 08 Dec 2023 20:23:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4345b37fb7af089771ba8cf5542de3045ebb0f1d247ea038535504b320c4ac2c`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12593e8f188e5024af21891d9f3141bc5b85d9e2e9e2b61d7c2634f9f491b9a4`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3632692d5118ec05512cfb67c4aa09a8dfdfe1e40467dfc5ee8e5d2e9a349b2a`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e694808297bceaf6299316f20be2a78e4d2eef8a2ca455dd79ce544cf0a00e66`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258e53ea4c6d9b42de13f722ade5338a5393993985f05ca5b438982dde948654`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20692d7b4da06a40fca6c59bffc5e13dc0a0ffc429f70ed8701dc1d5d8c087fd`  
		Last Modified: Fri, 08 Dec 2023 20:23:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f686dbb1484378b8f73bbbfac32eb04d8f9a6b2b3f4db7d17c1f997941475a7f`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84003630e1340399082b07e0df6cb438545136bc3f0c134d52e8fe9d878e7239`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 292.2 KB (292197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9991bbf8fb125121b7478726325dcb657bfbeb24af279019b7b2f7ac0c404f7`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:67a59b537826dfa0019b55a7c113d5bdd826062754543ae24cccdcf2a558d407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull caddy@sha256:3d281f8c1d34b38abb3b5ca4ff98d70312daad9b0654a470374d0447a69a3ccf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073448315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e423604e6f05b59d8afa51e2d09a8fc11e1ac3353a126e3ce73b1c2bc65872b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:16:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:16:25 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:17:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:17:33 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:17:34 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:17:35 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:17:36 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:17:37 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:17:38 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:17:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:17:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:17:41 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:17:42 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:17:43 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:18:34 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:18:35 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09e9b6b38c0082853f1d6caa4d3536344a04da2aa5b674837aba8781b265e0d`  
		Last Modified: Fri, 08 Dec 2023 20:22:45 GMT  
		Size: 462.7 KB (462693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb778801cf9547a5b9021d3090bd8e4fc05f09e3aed56b6950dcbd044211d3f`  
		Last Modified: Fri, 08 Dec 2023 20:22:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ec815279848293cd980ed43a496bf4d3e8f8035f8d46dd1a3278e02c4558a8`  
		Last Modified: Fri, 08 Dec 2023 20:22:46 GMT  
		Size: 15.3 MB (15274633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9671feff108f8e0d8be270b64952394b3eaf7d16a7e9163cffc500ad3a42bd17`  
		Last Modified: Fri, 08 Dec 2023 20:22:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44f97706c45d8ebb4578d93d6c1cb5ecc4625f2f78fa40f25f9e72af014449a`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7b5732d0f0e4f61cac2e09f77054657b1bfc21c56b5b4b842e96ee7de3d45d`  
		Last Modified: Fri, 08 Dec 2023 20:22:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348bbb9a26a300473cbb347ce3e405736e7a71ef7d2e67068452760fe4a1a67e`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4dc80dd8b7091a5cb553a95c06fa14380bf94a6f80467e3d7a36cb649fce8c`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6e2ab9cd2c6c903f643bcab22655dc93ec72fcc2f748a47375e2209580eed8`  
		Last Modified: Fri, 08 Dec 2023 20:22:41 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a498a93a315d79030214cb59d847ede547dfc1159616120a3b48f2b1585bccfc`  
		Last Modified: Fri, 08 Dec 2023 20:22:40 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a7d0f8e26a8dd06b83bb38bfecf51f24ec1456947f459528e71b2544d13f5`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0da3c95480c1f76c862487e0683bed75c660c5cce3e3864677b8c956228e64`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1712e0793bc7067adabbb602cf9eaf0e6ab60f33be0b2b10282325884270ab07`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c26aa77bbc553e8bf9318552da7ffe35258b387e04151dd211a006f50cb57a6`  
		Last Modified: Fri, 08 Dec 2023 20:22:39 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e384f6873d9619640183b8c67671c94c80eb3725ac52c312de84b314b2cd4c53`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7ecef2ca51e4738a30164e40d773f9bfcc9a55bda13a00745349db1618fbf0`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29866626f3b37691b2e593b7ad8a6d3f6e916d9ca428c22e1b3834e568c605c9`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dff7ab50f452876c91da33fe48a0e1409de6cbb0ffca4e1aefa68caa5722d01`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 256.7 KB (256705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55865895b10a6247b60406c70eaa3584e7904512f0092bd7d9013bd9fe64c740`  
		Last Modified: Fri, 08 Dec 2023 20:22:37 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:0726791503ced6bf9bdc5b322a8082762fb4ca97438a2c8fb49d0e80f06838ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull caddy@sha256:cca2801fca8e41625ec6c3c42ee17cc76b64320f93ec2c37999b29b5f9ff0747
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1902845713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ad0d44150328d8253edf3d339d33f508e3a25395c8fd773d2d2fe5966eb244`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Dec 2023 20:19:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Fri, 08 Dec 2023 20:19:10 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 20:19:33 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Fri, 08 Dec 2023 20:19:34 GMT
ENV XDG_CONFIG_HOME=c:/config
# Fri, 08 Dec 2023 20:19:35 GMT
ENV XDG_DATA_HOME=c:/data
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 20:19:36 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 20:19:37 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 20:19:38 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 20:19:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 20:19:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 20:19:41 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 80
# Fri, 08 Dec 2023 20:19:42 GMT
EXPOSE 443
# Fri, 08 Dec 2023 20:19:43 GMT
EXPOSE 443/udp
# Fri, 08 Dec 2023 20:19:44 GMT
EXPOSE 2019
# Fri, 08 Dec 2023 20:19:58 GMT
RUN caddy version
# Fri, 08 Dec 2023 20:19:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9e496904b6bbc7ce10b08f4c5c00b922d19bb8ebfca4735ba504c9ca77dd2b`  
		Last Modified: Fri, 08 Dec 2023 20:23:12 GMT  
		Size: 474.4 KB (474429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d370d88e3c2ee411f6f86dd892eba2c381cf5706823fcf82fec94a47d7d3bb4`  
		Last Modified: Fri, 08 Dec 2023 20:23:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1861a873425170bdbe2b563cd2b9584401a7be0e3d9a6ceac998eef4eab482ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:13 GMT  
		Size: 15.3 MB (15274241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e17c8887831a9d0a255eb44daaaedffc1bb98b51fc0177786dd130c85034006`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2595203a1e7cbe5c30c3a77633ff7b832c6f07580e688e7c2bc89b5442e72ae`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b5a75922e76c5c96d069952df83b51d1243d2d6955db5b45dd7b63aea2b3a1`  
		Last Modified: Fri, 08 Dec 2023 20:23:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bbe845ab80dc71320eea94c3d56888074ea930dc6fbe934c60e6c801e9cee3`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74052a6ffee1242926db0907e5406b7e5d81e181d3c9c266d381aaf221bf0252`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbd2ebe3b760156655b6475d7ff52b549e20b5115cf815016c902f834bf3f14`  
		Last Modified: Fri, 08 Dec 2023 20:23:08 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5945b936f7903435999bc26916fd896f5c645c5b70834243317e66b14d7c2d97`  
		Last Modified: Fri, 08 Dec 2023 20:23:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4345b37fb7af089771ba8cf5542de3045ebb0f1d247ea038535504b320c4ac2c`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12593e8f188e5024af21891d9f3141bc5b85d9e2e9e2b61d7c2634f9f491b9a4`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3632692d5118ec05512cfb67c4aa09a8dfdfe1e40467dfc5ee8e5d2e9a349b2a`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e694808297bceaf6299316f20be2a78e4d2eef8a2ca455dd79ce544cf0a00e66`  
		Last Modified: Fri, 08 Dec 2023 20:23:06 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258e53ea4c6d9b42de13f722ade5338a5393993985f05ca5b438982dde948654`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20692d7b4da06a40fca6c59bffc5e13dc0a0ffc429f70ed8701dc1d5d8c087fd`  
		Last Modified: Fri, 08 Dec 2023 20:23:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f686dbb1484378b8f73bbbfac32eb04d8f9a6b2b3f4db7d17c1f997941475a7f`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84003630e1340399082b07e0df6cb438545136bc3f0c134d52e8fe9d878e7239`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 292.2 KB (292197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9991bbf8fb125121b7478726325dcb657bfbeb24af279019b7b2f7ac0c404f7`  
		Last Modified: Fri, 08 Dec 2023 20:23:04 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
