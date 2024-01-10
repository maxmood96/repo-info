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
$ docker pull caddy@sha256:2f148ddb6662b4245ef4ced637e928eaf67a8a1941572d69627652253e779366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5206; amd64
	-	windows version 10.0.20348.2159; amd64

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

### `caddy:2` - windows version 10.0.17763.5206; amd64

```console
$ docker pull caddy@sha256:23906c96e8647871d54638ee95201b15a6780bd5c5a55e1910f1cce47f51327a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075748892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd668c1e74ca31419de6a4894168996b6be13d2cfb6dda297f76f1f0e82af65`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 12 Dec 2023 23:38:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 02:30:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Dec 2023 02:30:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Dec 2023 02:32:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Dec 2023 02:32:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Dec 2023 02:32:03 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Dec 2023 02:32:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Dec 2023 02:32:05 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Dec 2023 02:32:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Dec 2023 02:32:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Dec 2023 02:32:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Dec 2023 02:32:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Dec 2023 02:32:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Dec 2023 02:32:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Dec 2023 02:32:11 GMT
EXPOSE 80
# Wed, 13 Dec 2023 02:32:12 GMT
EXPOSE 443
# Wed, 13 Dec 2023 02:32:13 GMT
EXPOSE 443/udp
# Wed, 13 Dec 2023 02:32:13 GMT
EXPOSE 2019
# Wed, 13 Dec 2023 02:33:19 GMT
RUN caddy version
# Wed, 13 Dec 2023 02:33:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767e95390edb4050b2c57e1d564c9e4722c5ae776ebfb8907a539571a2609f7c`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc953d49171296238d791f543a2a026383540af60c9b10cc72446745ea9e517`  
		Last Modified: Wed, 13 Dec 2023 02:38:55 GMT  
		Size: 466.4 KB (466376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5091a1fcf41a799b6b5325321d36e20072d566027eeecc072788a9a3c3afbf0b`  
		Last Modified: Wed, 13 Dec 2023 02:38:54 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d0c21ea3d396314641058b6087c719f00acf6e81a122d0308c76705b454c5a`  
		Last Modified: Wed, 13 Dec 2023 02:38:58 GMT  
		Size: 15.3 MB (15282292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7c1ffefa6eaf8ceb9b6964a75043f3440c260e5ef8a7757a4902bbd87b5a11`  
		Last Modified: Wed, 13 Dec 2023 02:38:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209a9db6a8a0e20f16c07fa90f84ff5f0fbcf8896b719c5282405503804e4975`  
		Last Modified: Wed, 13 Dec 2023 02:38:53 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e6508c4f7300255ca275dc9fa4b8ff9f4e4ff4e6c552afee4d03305e571f8`  
		Last Modified: Wed, 13 Dec 2023 02:38:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571a096f7d34249fda9c90244912f35e632dc8c3c50a830c1d3dc6d5d2234264`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee679db41077812368c0ee8780348a81cc00878e2848106d2b022cfa25222615`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61da3eb55b53d10c6d39556e06adcd87b1e813dbf6e7c0c09a4a1fcd3c1a02af`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67d27f68c7ff3cf8ec13fd0ae72ac89b781c819f1959e16c22101faa49884a1`  
		Last Modified: Wed, 13 Dec 2023 02:38:51 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b0c532fc98f8438a57e314863455c2812c5f8273718a387893d58b1eae45a7`  
		Last Modified: Wed, 13 Dec 2023 02:38:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb76494edec3148a22e8826aa2cceb75046d74559b7fe31713da82a5504d187`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621db1494746176522163d644f8f6d572003928346b37dfea1118539767375bf`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e621e03d954adf248bd9ddcdfe28108be9204a2f010bc44cd49534bc26d10c`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb96c188ceb57176f56af8649f49ebde260394730cc2ee6bd5a10634d6676bc`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e2237c5f2e48a944f2cdc493acec61ca707749a0d33362f62a1162e6967f7f`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b904a8ec5a95b1df9b634285424830763de3a36377f8f97be9383346cd82022`  
		Last Modified: Wed, 13 Dec 2023 02:38:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ae7bbabfc6a290ea47a42a976c34545f19465895a8dee1bd94b9f6351d9ae`  
		Last Modified: Wed, 13 Dec 2023 02:38:49 GMT  
		Size: 269.0 KB (268985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4235be6cdbcf40a5350abf8550ae54349cd6889349bacb2c4c6fcdabb02fcb`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.20348.2159; amd64

```console
$ docker pull caddy@sha256:8b2e9ac9b72c8b2c90bc15116cedbb8044d599e4f86ffcbb48cebdfdf97d19f7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1905326657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7092fad7c71072036e6f6e418de96b9a293b2a5fa6c1f533192cee80981c2fdf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Tue, 12 Dec 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 02:33:55 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Dec 2023 02:33:56 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Dec 2023 02:35:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Dec 2023 02:35:11 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Dec 2023 02:35:12 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Dec 2023 02:35:12 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Dec 2023 02:35:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Dec 2023 02:35:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Dec 2023 02:35:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Dec 2023 02:35:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Dec 2023 02:35:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Dec 2023 02:35:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Dec 2023 02:35:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Dec 2023 02:35:19 GMT
EXPOSE 80
# Wed, 13 Dec 2023 02:35:20 GMT
EXPOSE 443
# Wed, 13 Dec 2023 02:35:21 GMT
EXPOSE 443/udp
# Wed, 13 Dec 2023 02:35:23 GMT
EXPOSE 2019
# Wed, 13 Dec 2023 02:35:42 GMT
RUN caddy version
# Wed, 13 Dec 2023 02:35:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d0c853ded9068434b9128a8016b3ae5e18f748f62801c7bb6e6092495300ec`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d3c17fb1ca1499edf5a0a7fe2ed357de61bc5478580af8c193d8c59e8139`  
		Last Modified: Wed, 13 Dec 2023 02:39:22 GMT  
		Size: 468.6 KB (468557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0205b9bfc982e2d76e931acf88ef85dfe1c943d4412d8e0abc82f7f0837e3ffe`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be685bdfb2389b99d51da84fb605d5905240fb7fbb82779d90949871c42c3a01`  
		Last Modified: Wed, 13 Dec 2023 02:39:24 GMT  
		Size: 15.3 MB (15270636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9935999a24844b91a4364fda0be1e1ffa280fb0c3c3c51157ffee05dc396bc2`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bd056752e2fad4d5b1e26bda93daeb2e2b89b03fc440f547e8e8e57b56ec54`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bff69c07007af0ff21680f637729be4b8d66a9b114305a47b54b631e499932`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8602ee7f30c15eb312beb9be91c2987f09264a3ec61fab2a25f7388c80361e65`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d98bd6b64e0a8382fcdef83a12bb138867f39b06a481c87d92f5e8b6bd637db`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab994312751dbeec291009c1153b38cf3621f929570200eefc6f838922099b`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb56c650abb1c98df5455b6b8c1864695f45548b82de29e570ce3f46299e574d`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b69a6fa036380dd82a0f067f8e97178a8da04f68a9c4a9eb4c10f5c432c7ad`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148841d4329f6dd8e152b2fc00676a9c4becd06e9c761400458c7b2d46438314`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8f8b0320cdf29c8f5349e14ec28542bd3c57d39b3d69d580de8ec462540d01`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b20c979eb5abf12332bf27e4b1aa8d06c7b7d6253b88d67681f13191b2ed1f5`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48a3dce4dbfd8b7dec08593b9d5c29404f49689161151ee3dda24b973f91dbe`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbc07c2849a4af7257c854c4fbd200cea57e1d10b82012dfcbe9a675b6fdcc0`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6842cf61f849c09c274f395d1e08b1196c674d9a59c34ddc4a9eb69e190b9d`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6823cd563e14b3750718450028cc7815abe14745863b57adc3e7524f3cdbfcb`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 290.0 KB (289982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae3d36b08abac2ea5a039a22621cc239126e2c32070f73be4efaacfc3c81c91`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1422 bytes)  
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
$ docker pull caddy@sha256:e4e6def23b2b2ddd4fc962e9e8871d2e1049909f09428e7d3455f3e9fe937126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5206; amd64
	-	windows version 10.0.20348.2159; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:40fb52ba04a15d7b79c65ccf594655c93ef84951d4b5f3636dd741c6f7117c82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77049039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec8a77457f35f87a6c0e163b4b9ca06831e9597838815cdfafd6924007b2053`
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
# Tue, 09 Jan 2024 22:20:46 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:20:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:20:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:20:57 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:20:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:20:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:20:58 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:13:01 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:13:01 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:13:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:13:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:13:03 GMT
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
	-	`sha256:2786abec99e189a4a116c45771654dd1220a5a78deb32430974d369c08fa4bd0`  
		Last Modified: Tue, 09 Jan 2024 22:27:13 GMT  
		Size: 67.1 MB (67086665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ece744550870593fb66b630e5fa62ae11cf9c89547275dd4450952b0fc9460`  
		Last Modified: Tue, 09 Jan 2024 22:27:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3a3a5ccc6f4610e4fd60832b6c63eed6366cfe0b0f37e3e6125f54aef9f135`  
		Last Modified: Tue, 09 Jan 2024 23:13:20 GMT  
		Size: 5.0 MB (4972463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe0d8e469393bc3c86e3dc711c99a557728a8c0e8a67a85f65d7fdc195034cd`  
		Last Modified: Tue, 09 Jan 2024 23:13:19 GMT  
		Size: 1.3 MB (1302233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761ef04b7c1f8fcec7e6f8b1f4995bdf8f34100b19140a0faef407b758829e8d`  
		Last Modified: Tue, 09 Jan 2024 23:13:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:83a8b023f6fa4c601dca30abe334e1243463e92f8e84e33dac925e8d6f7a601f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75411881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a0ab3fe89b994d3ff35471a8b1709d10e3ca724eb9a2e14bac7221211877bb`
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
# Wed, 20 Dec 2023 21:34:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Wed, 20 Dec 2023 21:34:12 GMT
ENV GOTOOLCHAIN=local
# Wed, 20 Dec 2023 21:34:12 GMT
ENV GOPATH=/go
# Wed, 20 Dec 2023 21:34:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 21:34:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 20 Dec 2023 21:34:13 GMT
WORKDIR /go
# Wed, 20 Dec 2023 21:51:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 20 Dec 2023 21:51:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_SETCAP=1
# Wed, 20 Dec 2023 21:51:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 20 Dec 2023 21:51:43 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 20 Dec 2023 21:51:43 GMT
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
	-	`sha256:29bee9d75e3ae91d44ddf09cf0fa198b556654c8073aa50d8b630e52a5d203be`  
		Last Modified: Wed, 20 Dec 2023 21:36:17 GMT  
		Size: 65.8 MB (65764273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a485eddce12cbac59d4532427a2f3bc7f475a18f1b6ddc05d3631682cde4be3e`  
		Last Modified: Wed, 20 Dec 2023 21:36:00 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460d4992c24f213c1a4f97d850c33f2a32be4f0763f60ae881dfb36929edbeb8`  
		Last Modified: Wed, 20 Dec 2023 21:52:07 GMT  
		Size: 5.0 MB (4966637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf270d0f9df22c9f4d54cc419be9b59b79eec2ef2f2c70fa2545347b5db6a1de`  
		Last Modified: Wed, 20 Dec 2023 21:52:07 GMT  
		Size: 1.2 MB (1248658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29559d6667b029d9d030a6d020a049a1c7df7a5d84b925b75e0b37d63be04d25`  
		Last Modified: Wed, 20 Dec 2023 21:52:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:286339d083a589ff4ee17f2a98eabb1011f13f93e40c79bba2af0748f9bf2c8c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74795731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08540a67a8309258e1b934ca527574a28d9cd09a153f09e55635d67a11e5572d`
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
# Tue, 09 Jan 2024 22:59:02 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:59:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:59:24 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:59:24 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:59:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:59:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:59:27 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:59:28 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:59:29 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:59:29 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:59:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:59:30 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:59:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:59:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:59:33 GMT
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
	-	`sha256:f975e362e12b206661ef3e8661f8ddef5b3886db6695858a6ee13107cfb406cd`  
		Last Modified: Tue, 09 Jan 2024 23:10:25 GMT  
		Size: 65.8 MB (65849716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d88a6cd0c6e987e9c7854e8091bc0d3da0f5215dc272d31db2a10463a597eb`  
		Last Modified: Tue, 09 Jan 2024 23:10:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ccd85286302c0f7692dc9bf9e673cc831252fa3892db98d4a388f8e3a40229`  
		Last Modified: Tue, 09 Jan 2024 23:59:54 GMT  
		Size: 4.5 MB (4514276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c77c0eb7e54b1d25489fbedb6607137e9123f25be63514940cec48f5afbcbb`  
		Last Modified: Tue, 09 Jan 2024 23:59:53 GMT  
		Size: 1.2 MB (1246091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe6c53215469f1e0efd2612e28e7bc3d644b7460fdac4ed2217adcfcbb01ff`  
		Last Modified: Tue, 09 Jan 2024 23:59:53 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:29c1d8e221c7025b5fa2bd564d67b2cbe54abf6ed141469ee753714d4b86de8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74062596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751a7ab9b4f36aa69472a02e61896bae0e9f5d4d8751e6a7791c550f914532f6`
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
# Tue, 09 Jan 2024 22:40:13 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:40:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:40:23 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:40:23 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:40:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:40:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:40:24 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:34:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:34:50 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:34:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:34:51 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:34:51 GMT
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
	-	`sha256:f784b2816c0487ec6a1efb9635a001a738ce6794c6f60cef8dd8fc658663da9f`  
		Last Modified: Tue, 09 Jan 2024 22:45:17 GMT  
		Size: 64.2 MB (64173642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2878d57b8185e91fa6aee756ccda964266f809fac11f9dce2ed4fbfd8912f1a9`  
		Last Modified: Tue, 09 Jan 2024 22:45:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab371eb8298e2716c51ac9c58092131a438b00268b67ae458e1ace0ff2b0b5a`  
		Last Modified: Tue, 09 Jan 2024 23:35:05 GMT  
		Size: 5.1 MB (5070606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797b9a67275bffa5caa99271d04d6986b812b4aa84192f9ba3f1ff7b1dfed362`  
		Last Modified: Tue, 09 Jan 2024 23:35:05 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13428147a58f4a789fd5d1f01d54bef643a726131dd40b35c267f16843158a6c`  
		Last Modified: Tue, 09 Jan 2024 23:35:04 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:745364722abfeb88309b8c87aaea59721a3b9ce6770ef2ece3727cd89c4ecdb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74295245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ca8de75928fb38f0a93327b23d822645315bee4c8d32dbc96b28ffbf4f513b`
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
# Tue, 09 Jan 2024 22:18:29 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:18:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:18:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:18:54 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:18:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:18:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:18:58 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:31:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:31:34 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:31:34 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:31:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:31:36 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:31:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:31:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:31:39 GMT
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
	-	`sha256:08676902305ce1488e47f2c6cf37c156f8adf34592d23cb6c0adda7f8e20bbec`  
		Last Modified: Tue, 09 Jan 2024 22:27:11 GMT  
		Size: 64.2 MB (64202869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007761f68f098a06788d8a4f5b63c5c25fa52e8f613da754d12a9c8005b2ad44`  
		Last Modified: Tue, 09 Jan 2024 22:26:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28beac3397f3e144b5cbb889b20e5c6450f5a635fd5679a9ddb77b34420a9512`  
		Last Modified: Tue, 09 Jan 2024 23:31:57 GMT  
		Size: 5.3 MB (5270658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee35c838a10edf1f76e27c99108010f65e1cb2d9cbad31ebe0480cdcc17a15d`  
		Last Modified: Tue, 09 Jan 2024 23:31:56 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce2a624f1055a6b34babd0b44d093aa23653397f4289c89018b0396bebcf038`  
		Last Modified: Tue, 09 Jan 2024 23:31:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:9eb20c4013227f7a3b0435a6f5346ec30763958b3f54f7ad0e7a02a7dd369f5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76184930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c9ebcb7eda5bc7753c6ac25b3a1ea2cbdce628c002973e9ad47ffb0d3ba97e`
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
# Tue, 09 Jan 2024 22:43:43 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:43:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:44:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:44:00 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:44:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:44:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:44:01 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:08:20 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:08:21 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:08:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:08:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:08:22 GMT
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
	-	`sha256:8d670b96a401a5cfb61ad27940492a2027ad1b61a1fa46000d705a1d8d159201`  
		Last Modified: Tue, 09 Jan 2024 22:51:10 GMT  
		Size: 66.3 MB (66302457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da6e3a038c3bd2afee0afab16ad35ea548d1966b1df80e55d9dcee9b280b371`  
		Last Modified: Tue, 09 Jan 2024 22:50:59 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08206a39be152f3861e70f6c3448542421f3249680b9274fd278f6015cc11aa5`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 5.1 MB (5116980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a1075ed747212d8e9506ed70d4cccab2b94dd685aa98e25a32f43575e21839`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 1.3 MB (1262390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76b6771ab88a9777236c173bb24bbc313a76da44e25c4c9ce07f8ff003338ee`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.5206; amd64

```console
$ docker pull caddy@sha256:76e18d17fe903d45f1f88f9ba76237a5fdb8392b670b3d2b0b581a9a8a4067de
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2156673231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267688b3ce7bd013fc2b9407cba404926536c40d42366eedebe5680d607fa176`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 12 Dec 2023 23:38:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Dec 2023 23:38:53 GMT
ENV GIT_VERSION=2.23.0
# Tue, 12 Dec 2023 23:38:53 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 12 Dec 2023 23:38:54 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 12 Dec 2023 23:38:55 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 12 Dec 2023 23:40:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 12 Dec 2023 23:40:27 GMT
ENV GOPATH=C:\go
# Tue, 12 Dec 2023 23:41:35 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jan 2024 22:18:47 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:22:02 GMT
RUN $url = 'https://dl.google.com/go/go1.21.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27ac9dd6e66fb3fd0acfa6792ff053c86e7d2c055b022f4b5d53bfddec9e3301'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Jan 2024 22:22:04 GMT
WORKDIR C:\go
# Tue, 09 Jan 2024 23:00:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jan 2024 23:00:16 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:00:17 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:00:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:01:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 09 Jan 2024 23:01:37 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767e95390edb4050b2c57e1d564c9e4722c5ae776ebfb8907a539571a2609f7c`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c57683b4a629f3325c8517d99f497d4ffbcd0e70354e70a95d983a275bfe398`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95bef40c25d2abc3a12986675189e7152f6197fdc5a17343bdee3f0bc2e95a8`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043d50fbb4f0d8961fe3a95130f520d57cfe7e6e85b15cd4f9f14a01364f7ee`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55867ab446b5d5e34f9e6d414898b9a0b31051afc81b28ace1ce47e27d9e24ee`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10285db29cf842d22a49b00cb66fbbfe20e7d4e72a0d3e393d58824190f6835b`  
		Last Modified: Wed, 13 Dec 2023 00:04:19 GMT  
		Size: 25.6 MB (25558777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3037ad7a881ee540014f48a43aa3a857c479d9cefb413ce61a914c943901890b`  
		Last Modified: Wed, 13 Dec 2023 00:04:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788faab53b378465ec447dde1961338c1349487d1152856c0524e2f6a503ec70`  
		Last Modified: Wed, 13 Dec 2023 00:04:12 GMT  
		Size: 282.5 KB (282534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca23066a92625cdc8de9b99f08faf5c3e756534401f72ec8aff465b29c481ee`  
		Last Modified: Tue, 09 Jan 2024 22:39:56 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b92d2b727a3677f7df423fdb871102a4f49e8ab3c3f27447b46a8bb9d6315c5`  
		Last Modified: Tue, 09 Jan 2024 22:40:17 GMT  
		Size: 69.4 MB (69428911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c07e208b8230a3cf4f0d09d8d2e0964843388a9334a811e7537778242b4610`  
		Last Modified: Tue, 09 Jan 2024 22:39:56 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0002a397ba0f92a6b352156052f4a5f9bf5bd0b854e9e066dc85b8231b8d23`  
		Last Modified: Tue, 09 Jan 2024 23:03:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221d1a0d3e162f0c5064835e1683a547fb68ce0fe6ddbc15547e97547f4a815f`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9d6843b6bad3862684d5eade7e7816b48ce845effe90d8c1d5d5250151dd55`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173a315f398d136fd23d058d13fa18b082575f9732c3cc17a733570a15d53606`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e288abae7098c76d0379b4bb3808523310f24e5aa535a62ff1405875e5723c`  
		Last Modified: Tue, 09 Jan 2024 23:03:11 GMT  
		Size: 1.7 MB (1676147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5e67ad5abb1499f08dbb66b77e1f22ffafb79eeacef131b3863ce4f042fcf2`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.20348.2159; amd64

```console
$ docker pull caddy@sha256:b5c196359cb78d80f0c4bb97d3ffbf13a84eb3003c9f238f72cec005c9475105
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1986234916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3131c915e036b0f95ea6c698ffaf9974f6dbce70dc8d2cd1600175d4155dde16`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Tue, 12 Dec 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Dec 2023 23:35:08 GMT
ENV GIT_VERSION=2.23.0
# Tue, 12 Dec 2023 23:35:08 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 12 Dec 2023 23:35:09 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 12 Dec 2023 23:35:10 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 12 Dec 2023 23:35:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 12 Dec 2023 23:35:47 GMT
ENV GOPATH=C:\go
# Tue, 12 Dec 2023 23:36:11 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jan 2024 22:16:03 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:18:27 GMT
RUN $url = 'https://dl.google.com/go/go1.21.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27ac9dd6e66fb3fd0acfa6792ff053c86e7d2c055b022f4b5d53bfddec9e3301'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Jan 2024 22:18:28 GMT
WORKDIR C:\go
# Tue, 09 Jan 2024 23:02:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jan 2024 23:02:03 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:02:04 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:02:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:02:30 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 09 Jan 2024 23:02:31 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d0c853ded9068434b9128a8016b3ae5e18f748f62801c7bb6e6092495300ec`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf365c1e9d59a58fc8cee2522db9139b36cf02ecabe7302489a9a3667b62cea`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69dbeb610a3fa1c3f2962202c58796ff120ea20cc3ba1f2fce807cbbe2c37ab0`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a3be8233329999132fa6e504f39c44abd589439a96846e31508037334d6d11`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755721e8166183821011ca0acdb563f67887cfe33da36997710b182f049fbede`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4700bd9f606505ec47d78dc66a509ca78ea2a8269a8e2b9bcf28ec33c5cbea74`  
		Last Modified: Wed, 13 Dec 2023 00:02:42 GMT  
		Size: 25.6 MB (25554973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777ab971ccee32e15de39ed82eceeb004d2d6f94af7c43ab3d6cfc1baf0abd07`  
		Last Modified: Wed, 13 Dec 2023 00:02:35 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958aa1458398ceb3a543d13279579cc48507080df3b269a5aa1a09da23b03ccf`  
		Last Modified: Wed, 13 Dec 2023 00:02:35 GMT  
		Size: 284.9 KB (284874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ed7a59b16104881efb9e3ac02b81f631cff124b04d7494d955a2c697b7c4ce`  
		Last Modified: Tue, 09 Jan 2024 22:39:21 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b1d528d83cdc1c6fb3f551b955643ffa64d14478df3d1b2aa1faf3cf95d454`  
		Last Modified: Tue, 09 Jan 2024 22:39:41 GMT  
		Size: 69.4 MB (69432029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8730c2425648e897784c3ff628a5fd72bb913811c924412142d22ce7f7d36c`  
		Last Modified: Tue, 09 Jan 2024 22:39:21 GMT  
		Size: 1.5 KB (1539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea60c3b2caff00ee0011a9148cabb96e3a1cde3a81a8ee5b7ca60f5513aff78`  
		Last Modified: Tue, 09 Jan 2024 23:03:30 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f939916b2a0c9fde832abafdf561e4515fc15d11979c5fa3e0bf8165cb4b3a`  
		Last Modified: Tue, 09 Jan 2024 23:03:28 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12cb1ee578e943a57f3c817517ac6b636e4d08c82aaacf57d4002b9732d98b0`  
		Last Modified: Tue, 09 Jan 2024 23:03:27 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c98bc1e6119b0ada6f9e06e3c88634debef4de96ad9906ac1d7065774a50a4f`  
		Last Modified: Tue, 09 Jan 2024 23:03:28 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc678bb3572a4a425d6d29f6ab5a6cbb6fb1e1cf427c0ed3982f9e451901c69`  
		Last Modified: Tue, 09 Jan 2024 23:03:28 GMT  
		Size: 1.7 MB (1671314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8151c697df9e9b88184cda0002778dff9d013f6ebd7c46924622bcb222243585`  
		Last Modified: Tue, 09 Jan 2024 23:03:27 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:88ea79d5d4c27d14e88147a8ee7880afdd51b939d2fc2b455146a10fbc326986
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
$ docker pull caddy@sha256:40fb52ba04a15d7b79c65ccf594655c93ef84951d4b5f3636dd741c6f7117c82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77049039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec8a77457f35f87a6c0e163b4b9ca06831e9597838815cdfafd6924007b2053`
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
# Tue, 09 Jan 2024 22:20:46 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:20:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:20:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:20:57 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:20:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:20:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:20:58 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:13:01 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:13:01 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:13:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:13:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:13:03 GMT
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
	-	`sha256:2786abec99e189a4a116c45771654dd1220a5a78deb32430974d369c08fa4bd0`  
		Last Modified: Tue, 09 Jan 2024 22:27:13 GMT  
		Size: 67.1 MB (67086665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ece744550870593fb66b630e5fa62ae11cf9c89547275dd4450952b0fc9460`  
		Last Modified: Tue, 09 Jan 2024 22:27:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3a3a5ccc6f4610e4fd60832b6c63eed6366cfe0b0f37e3e6125f54aef9f135`  
		Last Modified: Tue, 09 Jan 2024 23:13:20 GMT  
		Size: 5.0 MB (4972463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe0d8e469393bc3c86e3dc711c99a557728a8c0e8a67a85f65d7fdc195034cd`  
		Last Modified: Tue, 09 Jan 2024 23:13:19 GMT  
		Size: 1.3 MB (1302233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761ef04b7c1f8fcec7e6f8b1f4995bdf8f34100b19140a0faef407b758829e8d`  
		Last Modified: Tue, 09 Jan 2024 23:13:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:83a8b023f6fa4c601dca30abe334e1243463e92f8e84e33dac925e8d6f7a601f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75411881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a0ab3fe89b994d3ff35471a8b1709d10e3ca724eb9a2e14bac7221211877bb`
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
# Wed, 20 Dec 2023 21:34:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Wed, 20 Dec 2023 21:34:12 GMT
ENV GOTOOLCHAIN=local
# Wed, 20 Dec 2023 21:34:12 GMT
ENV GOPATH=/go
# Wed, 20 Dec 2023 21:34:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 21:34:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 20 Dec 2023 21:34:13 GMT
WORKDIR /go
# Wed, 20 Dec 2023 21:51:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 20 Dec 2023 21:51:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_SETCAP=1
# Wed, 20 Dec 2023 21:51:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 20 Dec 2023 21:51:43 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 20 Dec 2023 21:51:43 GMT
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
	-	`sha256:29bee9d75e3ae91d44ddf09cf0fa198b556654c8073aa50d8b630e52a5d203be`  
		Last Modified: Wed, 20 Dec 2023 21:36:17 GMT  
		Size: 65.8 MB (65764273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a485eddce12cbac59d4532427a2f3bc7f475a18f1b6ddc05d3631682cde4be3e`  
		Last Modified: Wed, 20 Dec 2023 21:36:00 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460d4992c24f213c1a4f97d850c33f2a32be4f0763f60ae881dfb36929edbeb8`  
		Last Modified: Wed, 20 Dec 2023 21:52:07 GMT  
		Size: 5.0 MB (4966637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf270d0f9df22c9f4d54cc419be9b59b79eec2ef2f2c70fa2545347b5db6a1de`  
		Last Modified: Wed, 20 Dec 2023 21:52:07 GMT  
		Size: 1.2 MB (1248658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29559d6667b029d9d030a6d020a049a1c7df7a5d84b925b75e0b37d63be04d25`  
		Last Modified: Wed, 20 Dec 2023 21:52:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:286339d083a589ff4ee17f2a98eabb1011f13f93e40c79bba2af0748f9bf2c8c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74795731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08540a67a8309258e1b934ca527574a28d9cd09a153f09e55635d67a11e5572d`
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
# Tue, 09 Jan 2024 22:59:02 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:59:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:59:24 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:59:24 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:59:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:59:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:59:27 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:59:28 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:59:29 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:59:29 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:59:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:59:30 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:59:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:59:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:59:33 GMT
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
	-	`sha256:f975e362e12b206661ef3e8661f8ddef5b3886db6695858a6ee13107cfb406cd`  
		Last Modified: Tue, 09 Jan 2024 23:10:25 GMT  
		Size: 65.8 MB (65849716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d88a6cd0c6e987e9c7854e8091bc0d3da0f5215dc272d31db2a10463a597eb`  
		Last Modified: Tue, 09 Jan 2024 23:10:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ccd85286302c0f7692dc9bf9e673cc831252fa3892db98d4a388f8e3a40229`  
		Last Modified: Tue, 09 Jan 2024 23:59:54 GMT  
		Size: 4.5 MB (4514276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c77c0eb7e54b1d25489fbedb6607137e9123f25be63514940cec48f5afbcbb`  
		Last Modified: Tue, 09 Jan 2024 23:59:53 GMT  
		Size: 1.2 MB (1246091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe6c53215469f1e0efd2612e28e7bc3d644b7460fdac4ed2217adcfcbb01ff`  
		Last Modified: Tue, 09 Jan 2024 23:59:53 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:29c1d8e221c7025b5fa2bd564d67b2cbe54abf6ed141469ee753714d4b86de8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74062596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751a7ab9b4f36aa69472a02e61896bae0e9f5d4d8751e6a7791c550f914532f6`
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
# Tue, 09 Jan 2024 22:40:13 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:40:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:40:23 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:40:23 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:40:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:40:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:40:24 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:34:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:34:50 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:34:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:34:51 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:34:51 GMT
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
	-	`sha256:f784b2816c0487ec6a1efb9635a001a738ce6794c6f60cef8dd8fc658663da9f`  
		Last Modified: Tue, 09 Jan 2024 22:45:17 GMT  
		Size: 64.2 MB (64173642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2878d57b8185e91fa6aee756ccda964266f809fac11f9dce2ed4fbfd8912f1a9`  
		Last Modified: Tue, 09 Jan 2024 22:45:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab371eb8298e2716c51ac9c58092131a438b00268b67ae458e1ace0ff2b0b5a`  
		Last Modified: Tue, 09 Jan 2024 23:35:05 GMT  
		Size: 5.1 MB (5070606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797b9a67275bffa5caa99271d04d6986b812b4aa84192f9ba3f1ff7b1dfed362`  
		Last Modified: Tue, 09 Jan 2024 23:35:05 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13428147a58f4a789fd5d1f01d54bef643a726131dd40b35c267f16843158a6c`  
		Last Modified: Tue, 09 Jan 2024 23:35:04 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:745364722abfeb88309b8c87aaea59721a3b9ce6770ef2ece3727cd89c4ecdb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74295245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ca8de75928fb38f0a93327b23d822645315bee4c8d32dbc96b28ffbf4f513b`
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
# Tue, 09 Jan 2024 22:18:29 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:18:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:18:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:18:54 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:18:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:18:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:18:58 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:31:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:31:34 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:31:34 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:31:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:31:36 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:31:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:31:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:31:39 GMT
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
	-	`sha256:08676902305ce1488e47f2c6cf37c156f8adf34592d23cb6c0adda7f8e20bbec`  
		Last Modified: Tue, 09 Jan 2024 22:27:11 GMT  
		Size: 64.2 MB (64202869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007761f68f098a06788d8a4f5b63c5c25fa52e8f613da754d12a9c8005b2ad44`  
		Last Modified: Tue, 09 Jan 2024 22:26:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28beac3397f3e144b5cbb889b20e5c6450f5a635fd5679a9ddb77b34420a9512`  
		Last Modified: Tue, 09 Jan 2024 23:31:57 GMT  
		Size: 5.3 MB (5270658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee35c838a10edf1f76e27c99108010f65e1cb2d9cbad31ebe0480cdcc17a15d`  
		Last Modified: Tue, 09 Jan 2024 23:31:56 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce2a624f1055a6b34babd0b44d093aa23653397f4289c89018b0396bebcf038`  
		Last Modified: Tue, 09 Jan 2024 23:31:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:9eb20c4013227f7a3b0435a6f5346ec30763958b3f54f7ad0e7a02a7dd369f5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76184930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c9ebcb7eda5bc7753c6ac25b3a1ea2cbdce628c002973e9ad47ffb0d3ba97e`
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
# Tue, 09 Jan 2024 22:43:43 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:43:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:44:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:44:00 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:44:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:44:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:44:01 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:08:20 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:08:21 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:08:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:08:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:08:22 GMT
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
	-	`sha256:8d670b96a401a5cfb61ad27940492a2027ad1b61a1fa46000d705a1d8d159201`  
		Last Modified: Tue, 09 Jan 2024 22:51:10 GMT  
		Size: 66.3 MB (66302457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da6e3a038c3bd2afee0afab16ad35ea548d1966b1df80e55d9dcee9b280b371`  
		Last Modified: Tue, 09 Jan 2024 22:50:59 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08206a39be152f3861e70f6c3448542421f3249680b9274fd278f6015cc11aa5`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 5.1 MB (5116980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a1075ed747212d8e9506ed70d4cccab2b94dd685aa98e25a32f43575e21839`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 1.3 MB (1262390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76b6771ab88a9777236c173bb24bbc313a76da44e25c4c9ce07f8ff003338ee`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:ee4395a3f6f47c0262fc9b8b002b6f27c88ea7f60afa086af1976dbc4aac28b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull caddy@sha256:76e18d17fe903d45f1f88f9ba76237a5fdb8392b670b3d2b0b581a9a8a4067de
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2156673231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267688b3ce7bd013fc2b9407cba404926536c40d42366eedebe5680d607fa176`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 12 Dec 2023 23:38:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Dec 2023 23:38:53 GMT
ENV GIT_VERSION=2.23.0
# Tue, 12 Dec 2023 23:38:53 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 12 Dec 2023 23:38:54 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 12 Dec 2023 23:38:55 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 12 Dec 2023 23:40:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 12 Dec 2023 23:40:27 GMT
ENV GOPATH=C:\go
# Tue, 12 Dec 2023 23:41:35 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jan 2024 22:18:47 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:22:02 GMT
RUN $url = 'https://dl.google.com/go/go1.21.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27ac9dd6e66fb3fd0acfa6792ff053c86e7d2c055b022f4b5d53bfddec9e3301'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Jan 2024 22:22:04 GMT
WORKDIR C:\go
# Tue, 09 Jan 2024 23:00:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jan 2024 23:00:16 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:00:17 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:00:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:01:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 09 Jan 2024 23:01:37 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767e95390edb4050b2c57e1d564c9e4722c5ae776ebfb8907a539571a2609f7c`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c57683b4a629f3325c8517d99f497d4ffbcd0e70354e70a95d983a275bfe398`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95bef40c25d2abc3a12986675189e7152f6197fdc5a17343bdee3f0bc2e95a8`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043d50fbb4f0d8961fe3a95130f520d57cfe7e6e85b15cd4f9f14a01364f7ee`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55867ab446b5d5e34f9e6d414898b9a0b31051afc81b28ace1ce47e27d9e24ee`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10285db29cf842d22a49b00cb66fbbfe20e7d4e72a0d3e393d58824190f6835b`  
		Last Modified: Wed, 13 Dec 2023 00:04:19 GMT  
		Size: 25.6 MB (25558777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3037ad7a881ee540014f48a43aa3a857c479d9cefb413ce61a914c943901890b`  
		Last Modified: Wed, 13 Dec 2023 00:04:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788faab53b378465ec447dde1961338c1349487d1152856c0524e2f6a503ec70`  
		Last Modified: Wed, 13 Dec 2023 00:04:12 GMT  
		Size: 282.5 KB (282534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca23066a92625cdc8de9b99f08faf5c3e756534401f72ec8aff465b29c481ee`  
		Last Modified: Tue, 09 Jan 2024 22:39:56 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b92d2b727a3677f7df423fdb871102a4f49e8ab3c3f27447b46a8bb9d6315c5`  
		Last Modified: Tue, 09 Jan 2024 22:40:17 GMT  
		Size: 69.4 MB (69428911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c07e208b8230a3cf4f0d09d8d2e0964843388a9334a811e7537778242b4610`  
		Last Modified: Tue, 09 Jan 2024 22:39:56 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0002a397ba0f92a6b352156052f4a5f9bf5bd0b854e9e066dc85b8231b8d23`  
		Last Modified: Tue, 09 Jan 2024 23:03:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221d1a0d3e162f0c5064835e1683a547fb68ce0fe6ddbc15547e97547f4a815f`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9d6843b6bad3862684d5eade7e7816b48ce845effe90d8c1d5d5250151dd55`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173a315f398d136fd23d058d13fa18b082575f9732c3cc17a733570a15d53606`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e288abae7098c76d0379b4bb3808523310f24e5aa535a62ff1405875e5723c`  
		Last Modified: Tue, 09 Jan 2024 23:03:11 GMT  
		Size: 1.7 MB (1676147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5e67ad5abb1499f08dbb66b77e1f22ffafb79eeacef131b3863ce4f042fcf2`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:3d08e6c2e2cef96a5a8f6ddb7531801ad745003ddac2d632d9679e2c30f95e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2159; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2159; amd64

```console
$ docker pull caddy@sha256:b5c196359cb78d80f0c4bb97d3ffbf13a84eb3003c9f238f72cec005c9475105
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1986234916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3131c915e036b0f95ea6c698ffaf9974f6dbce70dc8d2cd1600175d4155dde16`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Tue, 12 Dec 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Dec 2023 23:35:08 GMT
ENV GIT_VERSION=2.23.0
# Tue, 12 Dec 2023 23:35:08 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 12 Dec 2023 23:35:09 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 12 Dec 2023 23:35:10 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 12 Dec 2023 23:35:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 12 Dec 2023 23:35:47 GMT
ENV GOPATH=C:\go
# Tue, 12 Dec 2023 23:36:11 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jan 2024 22:16:03 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:18:27 GMT
RUN $url = 'https://dl.google.com/go/go1.21.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27ac9dd6e66fb3fd0acfa6792ff053c86e7d2c055b022f4b5d53bfddec9e3301'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Jan 2024 22:18:28 GMT
WORKDIR C:\go
# Tue, 09 Jan 2024 23:02:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jan 2024 23:02:03 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:02:04 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:02:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:02:30 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 09 Jan 2024 23:02:31 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d0c853ded9068434b9128a8016b3ae5e18f748f62801c7bb6e6092495300ec`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf365c1e9d59a58fc8cee2522db9139b36cf02ecabe7302489a9a3667b62cea`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69dbeb610a3fa1c3f2962202c58796ff120ea20cc3ba1f2fce807cbbe2c37ab0`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a3be8233329999132fa6e504f39c44abd589439a96846e31508037334d6d11`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755721e8166183821011ca0acdb563f67887cfe33da36997710b182f049fbede`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4700bd9f606505ec47d78dc66a509ca78ea2a8269a8e2b9bcf28ec33c5cbea74`  
		Last Modified: Wed, 13 Dec 2023 00:02:42 GMT  
		Size: 25.6 MB (25554973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777ab971ccee32e15de39ed82eceeb004d2d6f94af7c43ab3d6cfc1baf0abd07`  
		Last Modified: Wed, 13 Dec 2023 00:02:35 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958aa1458398ceb3a543d13279579cc48507080df3b269a5aa1a09da23b03ccf`  
		Last Modified: Wed, 13 Dec 2023 00:02:35 GMT  
		Size: 284.9 KB (284874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ed7a59b16104881efb9e3ac02b81f631cff124b04d7494d955a2c697b7c4ce`  
		Last Modified: Tue, 09 Jan 2024 22:39:21 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b1d528d83cdc1c6fb3f551b955643ffa64d14478df3d1b2aa1faf3cf95d454`  
		Last Modified: Tue, 09 Jan 2024 22:39:41 GMT  
		Size: 69.4 MB (69432029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8730c2425648e897784c3ff628a5fd72bb913811c924412142d22ce7f7d36c`  
		Last Modified: Tue, 09 Jan 2024 22:39:21 GMT  
		Size: 1.5 KB (1539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea60c3b2caff00ee0011a9148cabb96e3a1cde3a81a8ee5b7ca60f5513aff78`  
		Last Modified: Tue, 09 Jan 2024 23:03:30 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f939916b2a0c9fde832abafdf561e4515fc15d11979c5fa3e0bf8165cb4b3a`  
		Last Modified: Tue, 09 Jan 2024 23:03:28 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12cb1ee578e943a57f3c817517ac6b636e4d08c82aaacf57d4002b9732d98b0`  
		Last Modified: Tue, 09 Jan 2024 23:03:27 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c98bc1e6119b0ada6f9e06e3c88634debef4de96ad9906ac1d7065774a50a4f`  
		Last Modified: Tue, 09 Jan 2024 23:03:28 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc678bb3572a4a425d6d29f6ab5a6cbb6fb1e1cf427c0ed3982f9e451901c69`  
		Last Modified: Tue, 09 Jan 2024 23:03:28 GMT  
		Size: 1.7 MB (1671314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8151c697df9e9b88184cda0002778dff9d013f6ebd7c46924622bcb222243585`  
		Last Modified: Tue, 09 Jan 2024 23:03:27 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:972db88b238031234d870fded48029f384e208fa23012db80dd8de6adc65d559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.5206; amd64
	-	windows version 10.0.20348.2159; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.5206; amd64

```console
$ docker pull caddy@sha256:23906c96e8647871d54638ee95201b15a6780bd5c5a55e1910f1cce47f51327a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075748892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd668c1e74ca31419de6a4894168996b6be13d2cfb6dda297f76f1f0e82af65`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 12 Dec 2023 23:38:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 02:30:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Dec 2023 02:30:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Dec 2023 02:32:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Dec 2023 02:32:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Dec 2023 02:32:03 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Dec 2023 02:32:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Dec 2023 02:32:05 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Dec 2023 02:32:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Dec 2023 02:32:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Dec 2023 02:32:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Dec 2023 02:32:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Dec 2023 02:32:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Dec 2023 02:32:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Dec 2023 02:32:11 GMT
EXPOSE 80
# Wed, 13 Dec 2023 02:32:12 GMT
EXPOSE 443
# Wed, 13 Dec 2023 02:32:13 GMT
EXPOSE 443/udp
# Wed, 13 Dec 2023 02:32:13 GMT
EXPOSE 2019
# Wed, 13 Dec 2023 02:33:19 GMT
RUN caddy version
# Wed, 13 Dec 2023 02:33:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767e95390edb4050b2c57e1d564c9e4722c5ae776ebfb8907a539571a2609f7c`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc953d49171296238d791f543a2a026383540af60c9b10cc72446745ea9e517`  
		Last Modified: Wed, 13 Dec 2023 02:38:55 GMT  
		Size: 466.4 KB (466376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5091a1fcf41a799b6b5325321d36e20072d566027eeecc072788a9a3c3afbf0b`  
		Last Modified: Wed, 13 Dec 2023 02:38:54 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d0c21ea3d396314641058b6087c719f00acf6e81a122d0308c76705b454c5a`  
		Last Modified: Wed, 13 Dec 2023 02:38:58 GMT  
		Size: 15.3 MB (15282292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7c1ffefa6eaf8ceb9b6964a75043f3440c260e5ef8a7757a4902bbd87b5a11`  
		Last Modified: Wed, 13 Dec 2023 02:38:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209a9db6a8a0e20f16c07fa90f84ff5f0fbcf8896b719c5282405503804e4975`  
		Last Modified: Wed, 13 Dec 2023 02:38:53 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e6508c4f7300255ca275dc9fa4b8ff9f4e4ff4e6c552afee4d03305e571f8`  
		Last Modified: Wed, 13 Dec 2023 02:38:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571a096f7d34249fda9c90244912f35e632dc8c3c50a830c1d3dc6d5d2234264`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee679db41077812368c0ee8780348a81cc00878e2848106d2b022cfa25222615`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61da3eb55b53d10c6d39556e06adcd87b1e813dbf6e7c0c09a4a1fcd3c1a02af`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67d27f68c7ff3cf8ec13fd0ae72ac89b781c819f1959e16c22101faa49884a1`  
		Last Modified: Wed, 13 Dec 2023 02:38:51 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b0c532fc98f8438a57e314863455c2812c5f8273718a387893d58b1eae45a7`  
		Last Modified: Wed, 13 Dec 2023 02:38:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb76494edec3148a22e8826aa2cceb75046d74559b7fe31713da82a5504d187`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621db1494746176522163d644f8f6d572003928346b37dfea1118539767375bf`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e621e03d954adf248bd9ddcdfe28108be9204a2f010bc44cd49534bc26d10c`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb96c188ceb57176f56af8649f49ebde260394730cc2ee6bd5a10634d6676bc`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e2237c5f2e48a944f2cdc493acec61ca707749a0d33362f62a1162e6967f7f`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b904a8ec5a95b1df9b634285424830763de3a36377f8f97be9383346cd82022`  
		Last Modified: Wed, 13 Dec 2023 02:38:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ae7bbabfc6a290ea47a42a976c34545f19465895a8dee1bd94b9f6351d9ae`  
		Last Modified: Wed, 13 Dec 2023 02:38:49 GMT  
		Size: 269.0 KB (268985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4235be6cdbcf40a5350abf8550ae54349cd6889349bacb2c4c6fcdabb02fcb`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.20348.2159; amd64

```console
$ docker pull caddy@sha256:8b2e9ac9b72c8b2c90bc15116cedbb8044d599e4f86ffcbb48cebdfdf97d19f7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1905326657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7092fad7c71072036e6f6e418de96b9a293b2a5fa6c1f533192cee80981c2fdf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Tue, 12 Dec 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 02:33:55 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Dec 2023 02:33:56 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Dec 2023 02:35:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Dec 2023 02:35:11 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Dec 2023 02:35:12 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Dec 2023 02:35:12 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Dec 2023 02:35:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Dec 2023 02:35:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Dec 2023 02:35:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Dec 2023 02:35:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Dec 2023 02:35:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Dec 2023 02:35:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Dec 2023 02:35:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Dec 2023 02:35:19 GMT
EXPOSE 80
# Wed, 13 Dec 2023 02:35:20 GMT
EXPOSE 443
# Wed, 13 Dec 2023 02:35:21 GMT
EXPOSE 443/udp
# Wed, 13 Dec 2023 02:35:23 GMT
EXPOSE 2019
# Wed, 13 Dec 2023 02:35:42 GMT
RUN caddy version
# Wed, 13 Dec 2023 02:35:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d0c853ded9068434b9128a8016b3ae5e18f748f62801c7bb6e6092495300ec`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d3c17fb1ca1499edf5a0a7fe2ed357de61bc5478580af8c193d8c59e8139`  
		Last Modified: Wed, 13 Dec 2023 02:39:22 GMT  
		Size: 468.6 KB (468557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0205b9bfc982e2d76e931acf88ef85dfe1c943d4412d8e0abc82f7f0837e3ffe`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be685bdfb2389b99d51da84fb605d5905240fb7fbb82779d90949871c42c3a01`  
		Last Modified: Wed, 13 Dec 2023 02:39:24 GMT  
		Size: 15.3 MB (15270636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9935999a24844b91a4364fda0be1e1ffa280fb0c3c3c51157ffee05dc396bc2`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bd056752e2fad4d5b1e26bda93daeb2e2b89b03fc440f547e8e8e57b56ec54`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bff69c07007af0ff21680f637729be4b8d66a9b114305a47b54b631e499932`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8602ee7f30c15eb312beb9be91c2987f09264a3ec61fab2a25f7388c80361e65`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d98bd6b64e0a8382fcdef83a12bb138867f39b06a481c87d92f5e8b6bd637db`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab994312751dbeec291009c1153b38cf3621f929570200eefc6f838922099b`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb56c650abb1c98df5455b6b8c1864695f45548b82de29e570ce3f46299e574d`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b69a6fa036380dd82a0f067f8e97178a8da04f68a9c4a9eb4c10f5c432c7ad`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148841d4329f6dd8e152b2fc00676a9c4becd06e9c761400458c7b2d46438314`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8f8b0320cdf29c8f5349e14ec28542bd3c57d39b3d69d580de8ec462540d01`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b20c979eb5abf12332bf27e4b1aa8d06c7b7d6253b88d67681f13191b2ed1f5`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48a3dce4dbfd8b7dec08593b9d5c29404f49689161151ee3dda24b973f91dbe`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbc07c2849a4af7257c854c4fbd200cea57e1d10b82012dfcbe9a675b6fdcc0`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6842cf61f849c09c274f395d1e08b1196c674d9a59c34ddc4a9eb69e190b9d`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6823cd563e14b3750718450028cc7815abe14745863b57adc3e7524f3cdbfcb`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 290.0 KB (289982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae3d36b08abac2ea5a039a22621cc239126e2c32070f73be4efaacfc3c81c91`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:7c8910562b78f49c3a2f608132f963d70e34352d7b1eba277e11d71c4aadd90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull caddy@sha256:23906c96e8647871d54638ee95201b15a6780bd5c5a55e1910f1cce47f51327a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075748892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd668c1e74ca31419de6a4894168996b6be13d2cfb6dda297f76f1f0e82af65`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 12 Dec 2023 23:38:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 02:30:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Dec 2023 02:30:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Dec 2023 02:32:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Dec 2023 02:32:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Dec 2023 02:32:03 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Dec 2023 02:32:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Dec 2023 02:32:05 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Dec 2023 02:32:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Dec 2023 02:32:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Dec 2023 02:32:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Dec 2023 02:32:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Dec 2023 02:32:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Dec 2023 02:32:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Dec 2023 02:32:11 GMT
EXPOSE 80
# Wed, 13 Dec 2023 02:32:12 GMT
EXPOSE 443
# Wed, 13 Dec 2023 02:32:13 GMT
EXPOSE 443/udp
# Wed, 13 Dec 2023 02:32:13 GMT
EXPOSE 2019
# Wed, 13 Dec 2023 02:33:19 GMT
RUN caddy version
# Wed, 13 Dec 2023 02:33:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767e95390edb4050b2c57e1d564c9e4722c5ae776ebfb8907a539571a2609f7c`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc953d49171296238d791f543a2a026383540af60c9b10cc72446745ea9e517`  
		Last Modified: Wed, 13 Dec 2023 02:38:55 GMT  
		Size: 466.4 KB (466376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5091a1fcf41a799b6b5325321d36e20072d566027eeecc072788a9a3c3afbf0b`  
		Last Modified: Wed, 13 Dec 2023 02:38:54 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d0c21ea3d396314641058b6087c719f00acf6e81a122d0308c76705b454c5a`  
		Last Modified: Wed, 13 Dec 2023 02:38:58 GMT  
		Size: 15.3 MB (15282292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7c1ffefa6eaf8ceb9b6964a75043f3440c260e5ef8a7757a4902bbd87b5a11`  
		Last Modified: Wed, 13 Dec 2023 02:38:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209a9db6a8a0e20f16c07fa90f84ff5f0fbcf8896b719c5282405503804e4975`  
		Last Modified: Wed, 13 Dec 2023 02:38:53 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e6508c4f7300255ca275dc9fa4b8ff9f4e4ff4e6c552afee4d03305e571f8`  
		Last Modified: Wed, 13 Dec 2023 02:38:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571a096f7d34249fda9c90244912f35e632dc8c3c50a830c1d3dc6d5d2234264`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee679db41077812368c0ee8780348a81cc00878e2848106d2b022cfa25222615`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61da3eb55b53d10c6d39556e06adcd87b1e813dbf6e7c0c09a4a1fcd3c1a02af`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67d27f68c7ff3cf8ec13fd0ae72ac89b781c819f1959e16c22101faa49884a1`  
		Last Modified: Wed, 13 Dec 2023 02:38:51 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b0c532fc98f8438a57e314863455c2812c5f8273718a387893d58b1eae45a7`  
		Last Modified: Wed, 13 Dec 2023 02:38:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb76494edec3148a22e8826aa2cceb75046d74559b7fe31713da82a5504d187`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621db1494746176522163d644f8f6d572003928346b37dfea1118539767375bf`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e621e03d954adf248bd9ddcdfe28108be9204a2f010bc44cd49534bc26d10c`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb96c188ceb57176f56af8649f49ebde260394730cc2ee6bd5a10634d6676bc`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e2237c5f2e48a944f2cdc493acec61ca707749a0d33362f62a1162e6967f7f`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b904a8ec5a95b1df9b634285424830763de3a36377f8f97be9383346cd82022`  
		Last Modified: Wed, 13 Dec 2023 02:38:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ae7bbabfc6a290ea47a42a976c34545f19465895a8dee1bd94b9f6351d9ae`  
		Last Modified: Wed, 13 Dec 2023 02:38:49 GMT  
		Size: 269.0 KB (268985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4235be6cdbcf40a5350abf8550ae54349cd6889349bacb2c4c6fcdabb02fcb`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:05ced206e45b045bc5cd525d92a16ed5dc3db97b7917edef04152739d06b712b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2159; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.2159; amd64

```console
$ docker pull caddy@sha256:8b2e9ac9b72c8b2c90bc15116cedbb8044d599e4f86ffcbb48cebdfdf97d19f7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1905326657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7092fad7c71072036e6f6e418de96b9a293b2a5fa6c1f533192cee80981c2fdf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Tue, 12 Dec 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 02:33:55 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Dec 2023 02:33:56 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Dec 2023 02:35:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Dec 2023 02:35:11 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Dec 2023 02:35:12 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Dec 2023 02:35:12 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Dec 2023 02:35:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Dec 2023 02:35:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Dec 2023 02:35:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Dec 2023 02:35:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Dec 2023 02:35:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Dec 2023 02:35:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Dec 2023 02:35:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Dec 2023 02:35:19 GMT
EXPOSE 80
# Wed, 13 Dec 2023 02:35:20 GMT
EXPOSE 443
# Wed, 13 Dec 2023 02:35:21 GMT
EXPOSE 443/udp
# Wed, 13 Dec 2023 02:35:23 GMT
EXPOSE 2019
# Wed, 13 Dec 2023 02:35:42 GMT
RUN caddy version
# Wed, 13 Dec 2023 02:35:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d0c853ded9068434b9128a8016b3ae5e18f748f62801c7bb6e6092495300ec`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d3c17fb1ca1499edf5a0a7fe2ed357de61bc5478580af8c193d8c59e8139`  
		Last Modified: Wed, 13 Dec 2023 02:39:22 GMT  
		Size: 468.6 KB (468557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0205b9bfc982e2d76e931acf88ef85dfe1c943d4412d8e0abc82f7f0837e3ffe`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be685bdfb2389b99d51da84fb605d5905240fb7fbb82779d90949871c42c3a01`  
		Last Modified: Wed, 13 Dec 2023 02:39:24 GMT  
		Size: 15.3 MB (15270636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9935999a24844b91a4364fda0be1e1ffa280fb0c3c3c51157ffee05dc396bc2`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bd056752e2fad4d5b1e26bda93daeb2e2b89b03fc440f547e8e8e57b56ec54`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bff69c07007af0ff21680f637729be4b8d66a9b114305a47b54b631e499932`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8602ee7f30c15eb312beb9be91c2987f09264a3ec61fab2a25f7388c80361e65`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d98bd6b64e0a8382fcdef83a12bb138867f39b06a481c87d92f5e8b6bd637db`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab994312751dbeec291009c1153b38cf3621f929570200eefc6f838922099b`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb56c650abb1c98df5455b6b8c1864695f45548b82de29e570ce3f46299e574d`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b69a6fa036380dd82a0f067f8e97178a8da04f68a9c4a9eb4c10f5c432c7ad`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148841d4329f6dd8e152b2fc00676a9c4becd06e9c761400458c7b2d46438314`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8f8b0320cdf29c8f5349e14ec28542bd3c57d39b3d69d580de8ec462540d01`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b20c979eb5abf12332bf27e4b1aa8d06c7b7d6253b88d67681f13191b2ed1f5`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48a3dce4dbfd8b7dec08593b9d5c29404f49689161151ee3dda24b973f91dbe`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbc07c2849a4af7257c854c4fbd200cea57e1d10b82012dfcbe9a675b6fdcc0`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6842cf61f849c09c274f395d1e08b1196c674d9a59c34ddc4a9eb69e190b9d`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6823cd563e14b3750718450028cc7815abe14745863b57adc3e7524f3cdbfcb`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 290.0 KB (289982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae3d36b08abac2ea5a039a22621cc239126e2c32070f73be4efaacfc3c81c91`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7`

```console
$ docker pull caddy@sha256:2f148ddb6662b4245ef4ced637e928eaf67a8a1941572d69627652253e779366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5206; amd64
	-	windows version 10.0.20348.2159; amd64

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

### `caddy:2.7` - windows version 10.0.17763.5206; amd64

```console
$ docker pull caddy@sha256:23906c96e8647871d54638ee95201b15a6780bd5c5a55e1910f1cce47f51327a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075748892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd668c1e74ca31419de6a4894168996b6be13d2cfb6dda297f76f1f0e82af65`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 12 Dec 2023 23:38:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 02:30:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Dec 2023 02:30:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Dec 2023 02:32:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Dec 2023 02:32:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Dec 2023 02:32:03 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Dec 2023 02:32:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Dec 2023 02:32:05 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Dec 2023 02:32:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Dec 2023 02:32:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Dec 2023 02:32:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Dec 2023 02:32:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Dec 2023 02:32:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Dec 2023 02:32:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Dec 2023 02:32:11 GMT
EXPOSE 80
# Wed, 13 Dec 2023 02:32:12 GMT
EXPOSE 443
# Wed, 13 Dec 2023 02:32:13 GMT
EXPOSE 443/udp
# Wed, 13 Dec 2023 02:32:13 GMT
EXPOSE 2019
# Wed, 13 Dec 2023 02:33:19 GMT
RUN caddy version
# Wed, 13 Dec 2023 02:33:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767e95390edb4050b2c57e1d564c9e4722c5ae776ebfb8907a539571a2609f7c`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc953d49171296238d791f543a2a026383540af60c9b10cc72446745ea9e517`  
		Last Modified: Wed, 13 Dec 2023 02:38:55 GMT  
		Size: 466.4 KB (466376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5091a1fcf41a799b6b5325321d36e20072d566027eeecc072788a9a3c3afbf0b`  
		Last Modified: Wed, 13 Dec 2023 02:38:54 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d0c21ea3d396314641058b6087c719f00acf6e81a122d0308c76705b454c5a`  
		Last Modified: Wed, 13 Dec 2023 02:38:58 GMT  
		Size: 15.3 MB (15282292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7c1ffefa6eaf8ceb9b6964a75043f3440c260e5ef8a7757a4902bbd87b5a11`  
		Last Modified: Wed, 13 Dec 2023 02:38:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209a9db6a8a0e20f16c07fa90f84ff5f0fbcf8896b719c5282405503804e4975`  
		Last Modified: Wed, 13 Dec 2023 02:38:53 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e6508c4f7300255ca275dc9fa4b8ff9f4e4ff4e6c552afee4d03305e571f8`  
		Last Modified: Wed, 13 Dec 2023 02:38:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571a096f7d34249fda9c90244912f35e632dc8c3c50a830c1d3dc6d5d2234264`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee679db41077812368c0ee8780348a81cc00878e2848106d2b022cfa25222615`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61da3eb55b53d10c6d39556e06adcd87b1e813dbf6e7c0c09a4a1fcd3c1a02af`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67d27f68c7ff3cf8ec13fd0ae72ac89b781c819f1959e16c22101faa49884a1`  
		Last Modified: Wed, 13 Dec 2023 02:38:51 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b0c532fc98f8438a57e314863455c2812c5f8273718a387893d58b1eae45a7`  
		Last Modified: Wed, 13 Dec 2023 02:38:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb76494edec3148a22e8826aa2cceb75046d74559b7fe31713da82a5504d187`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621db1494746176522163d644f8f6d572003928346b37dfea1118539767375bf`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e621e03d954adf248bd9ddcdfe28108be9204a2f010bc44cd49534bc26d10c`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb96c188ceb57176f56af8649f49ebde260394730cc2ee6bd5a10634d6676bc`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e2237c5f2e48a944f2cdc493acec61ca707749a0d33362f62a1162e6967f7f`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b904a8ec5a95b1df9b634285424830763de3a36377f8f97be9383346cd82022`  
		Last Modified: Wed, 13 Dec 2023 02:38:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ae7bbabfc6a290ea47a42a976c34545f19465895a8dee1bd94b9f6351d9ae`  
		Last Modified: Wed, 13 Dec 2023 02:38:49 GMT  
		Size: 269.0 KB (268985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4235be6cdbcf40a5350abf8550ae54349cd6889349bacb2c4c6fcdabb02fcb`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - windows version 10.0.20348.2159; amd64

```console
$ docker pull caddy@sha256:8b2e9ac9b72c8b2c90bc15116cedbb8044d599e4f86ffcbb48cebdfdf97d19f7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1905326657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7092fad7c71072036e6f6e418de96b9a293b2a5fa6c1f533192cee80981c2fdf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Tue, 12 Dec 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 02:33:55 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Dec 2023 02:33:56 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Dec 2023 02:35:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Dec 2023 02:35:11 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Dec 2023 02:35:12 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Dec 2023 02:35:12 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Dec 2023 02:35:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Dec 2023 02:35:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Dec 2023 02:35:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Dec 2023 02:35:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Dec 2023 02:35:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Dec 2023 02:35:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Dec 2023 02:35:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Dec 2023 02:35:19 GMT
EXPOSE 80
# Wed, 13 Dec 2023 02:35:20 GMT
EXPOSE 443
# Wed, 13 Dec 2023 02:35:21 GMT
EXPOSE 443/udp
# Wed, 13 Dec 2023 02:35:23 GMT
EXPOSE 2019
# Wed, 13 Dec 2023 02:35:42 GMT
RUN caddy version
# Wed, 13 Dec 2023 02:35:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d0c853ded9068434b9128a8016b3ae5e18f748f62801c7bb6e6092495300ec`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d3c17fb1ca1499edf5a0a7fe2ed357de61bc5478580af8c193d8c59e8139`  
		Last Modified: Wed, 13 Dec 2023 02:39:22 GMT  
		Size: 468.6 KB (468557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0205b9bfc982e2d76e931acf88ef85dfe1c943d4412d8e0abc82f7f0837e3ffe`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be685bdfb2389b99d51da84fb605d5905240fb7fbb82779d90949871c42c3a01`  
		Last Modified: Wed, 13 Dec 2023 02:39:24 GMT  
		Size: 15.3 MB (15270636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9935999a24844b91a4364fda0be1e1ffa280fb0c3c3c51157ffee05dc396bc2`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bd056752e2fad4d5b1e26bda93daeb2e2b89b03fc440f547e8e8e57b56ec54`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bff69c07007af0ff21680f637729be4b8d66a9b114305a47b54b631e499932`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8602ee7f30c15eb312beb9be91c2987f09264a3ec61fab2a25f7388c80361e65`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d98bd6b64e0a8382fcdef83a12bb138867f39b06a481c87d92f5e8b6bd637db`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab994312751dbeec291009c1153b38cf3621f929570200eefc6f838922099b`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb56c650abb1c98df5455b6b8c1864695f45548b82de29e570ce3f46299e574d`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b69a6fa036380dd82a0f067f8e97178a8da04f68a9c4a9eb4c10f5c432c7ad`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148841d4329f6dd8e152b2fc00676a9c4becd06e9c761400458c7b2d46438314`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8f8b0320cdf29c8f5349e14ec28542bd3c57d39b3d69d580de8ec462540d01`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b20c979eb5abf12332bf27e4b1aa8d06c7b7d6253b88d67681f13191b2ed1f5`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48a3dce4dbfd8b7dec08593b9d5c29404f49689161151ee3dda24b973f91dbe`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbc07c2849a4af7257c854c4fbd200cea57e1d10b82012dfcbe9a675b6fdcc0`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6842cf61f849c09c274f395d1e08b1196c674d9a59c34ddc4a9eb69e190b9d`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6823cd563e14b3750718450028cc7815abe14745863b57adc3e7524f3cdbfcb`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 290.0 KB (289982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae3d36b08abac2ea5a039a22621cc239126e2c32070f73be4efaacfc3c81c91`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1422 bytes)  
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
$ docker pull caddy@sha256:e4e6def23b2b2ddd4fc962e9e8871d2e1049909f09428e7d3455f3e9fe937126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5206; amd64
	-	windows version 10.0.20348.2159; amd64

### `caddy:2.7-builder` - linux; amd64

```console
$ docker pull caddy@sha256:40fb52ba04a15d7b79c65ccf594655c93ef84951d4b5f3636dd741c6f7117c82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77049039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec8a77457f35f87a6c0e163b4b9ca06831e9597838815cdfafd6924007b2053`
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
# Tue, 09 Jan 2024 22:20:46 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:20:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:20:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:20:57 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:20:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:20:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:20:58 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:13:01 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:13:01 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:13:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:13:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:13:03 GMT
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
	-	`sha256:2786abec99e189a4a116c45771654dd1220a5a78deb32430974d369c08fa4bd0`  
		Last Modified: Tue, 09 Jan 2024 22:27:13 GMT  
		Size: 67.1 MB (67086665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ece744550870593fb66b630e5fa62ae11cf9c89547275dd4450952b0fc9460`  
		Last Modified: Tue, 09 Jan 2024 22:27:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3a3a5ccc6f4610e4fd60832b6c63eed6366cfe0b0f37e3e6125f54aef9f135`  
		Last Modified: Tue, 09 Jan 2024 23:13:20 GMT  
		Size: 5.0 MB (4972463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe0d8e469393bc3c86e3dc711c99a557728a8c0e8a67a85f65d7fdc195034cd`  
		Last Modified: Tue, 09 Jan 2024 23:13:19 GMT  
		Size: 1.3 MB (1302233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761ef04b7c1f8fcec7e6f8b1f4995bdf8f34100b19140a0faef407b758829e8d`  
		Last Modified: Tue, 09 Jan 2024 23:13:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:83a8b023f6fa4c601dca30abe334e1243463e92f8e84e33dac925e8d6f7a601f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75411881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a0ab3fe89b994d3ff35471a8b1709d10e3ca724eb9a2e14bac7221211877bb`
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
# Wed, 20 Dec 2023 21:34:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Wed, 20 Dec 2023 21:34:12 GMT
ENV GOTOOLCHAIN=local
# Wed, 20 Dec 2023 21:34:12 GMT
ENV GOPATH=/go
# Wed, 20 Dec 2023 21:34:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 21:34:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 20 Dec 2023 21:34:13 GMT
WORKDIR /go
# Wed, 20 Dec 2023 21:51:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 20 Dec 2023 21:51:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_SETCAP=1
# Wed, 20 Dec 2023 21:51:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 20 Dec 2023 21:51:43 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 20 Dec 2023 21:51:43 GMT
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
	-	`sha256:29bee9d75e3ae91d44ddf09cf0fa198b556654c8073aa50d8b630e52a5d203be`  
		Last Modified: Wed, 20 Dec 2023 21:36:17 GMT  
		Size: 65.8 MB (65764273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a485eddce12cbac59d4532427a2f3bc7f475a18f1b6ddc05d3631682cde4be3e`  
		Last Modified: Wed, 20 Dec 2023 21:36:00 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460d4992c24f213c1a4f97d850c33f2a32be4f0763f60ae881dfb36929edbeb8`  
		Last Modified: Wed, 20 Dec 2023 21:52:07 GMT  
		Size: 5.0 MB (4966637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf270d0f9df22c9f4d54cc419be9b59b79eec2ef2f2c70fa2545347b5db6a1de`  
		Last Modified: Wed, 20 Dec 2023 21:52:07 GMT  
		Size: 1.2 MB (1248658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29559d6667b029d9d030a6d020a049a1c7df7a5d84b925b75e0b37d63be04d25`  
		Last Modified: Wed, 20 Dec 2023 21:52:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:286339d083a589ff4ee17f2a98eabb1011f13f93e40c79bba2af0748f9bf2c8c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74795731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08540a67a8309258e1b934ca527574a28d9cd09a153f09e55635d67a11e5572d`
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
# Tue, 09 Jan 2024 22:59:02 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:59:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:59:24 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:59:24 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:59:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:59:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:59:27 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:59:28 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:59:29 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:59:29 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:59:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:59:30 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:59:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:59:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:59:33 GMT
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
	-	`sha256:f975e362e12b206661ef3e8661f8ddef5b3886db6695858a6ee13107cfb406cd`  
		Last Modified: Tue, 09 Jan 2024 23:10:25 GMT  
		Size: 65.8 MB (65849716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d88a6cd0c6e987e9c7854e8091bc0d3da0f5215dc272d31db2a10463a597eb`  
		Last Modified: Tue, 09 Jan 2024 23:10:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ccd85286302c0f7692dc9bf9e673cc831252fa3892db98d4a388f8e3a40229`  
		Last Modified: Tue, 09 Jan 2024 23:59:54 GMT  
		Size: 4.5 MB (4514276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c77c0eb7e54b1d25489fbedb6607137e9123f25be63514940cec48f5afbcbb`  
		Last Modified: Tue, 09 Jan 2024 23:59:53 GMT  
		Size: 1.2 MB (1246091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe6c53215469f1e0efd2612e28e7bc3d644b7460fdac4ed2217adcfcbb01ff`  
		Last Modified: Tue, 09 Jan 2024 23:59:53 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:29c1d8e221c7025b5fa2bd564d67b2cbe54abf6ed141469ee753714d4b86de8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74062596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751a7ab9b4f36aa69472a02e61896bae0e9f5d4d8751e6a7791c550f914532f6`
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
# Tue, 09 Jan 2024 22:40:13 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:40:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:40:23 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:40:23 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:40:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:40:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:40:24 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:34:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:34:50 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:34:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:34:51 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:34:51 GMT
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
	-	`sha256:f784b2816c0487ec6a1efb9635a001a738ce6794c6f60cef8dd8fc658663da9f`  
		Last Modified: Tue, 09 Jan 2024 22:45:17 GMT  
		Size: 64.2 MB (64173642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2878d57b8185e91fa6aee756ccda964266f809fac11f9dce2ed4fbfd8912f1a9`  
		Last Modified: Tue, 09 Jan 2024 22:45:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab371eb8298e2716c51ac9c58092131a438b00268b67ae458e1ace0ff2b0b5a`  
		Last Modified: Tue, 09 Jan 2024 23:35:05 GMT  
		Size: 5.1 MB (5070606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797b9a67275bffa5caa99271d04d6986b812b4aa84192f9ba3f1ff7b1dfed362`  
		Last Modified: Tue, 09 Jan 2024 23:35:05 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13428147a58f4a789fd5d1f01d54bef643a726131dd40b35c267f16843158a6c`  
		Last Modified: Tue, 09 Jan 2024 23:35:04 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:745364722abfeb88309b8c87aaea59721a3b9ce6770ef2ece3727cd89c4ecdb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74295245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ca8de75928fb38f0a93327b23d822645315bee4c8d32dbc96b28ffbf4f513b`
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
# Tue, 09 Jan 2024 22:18:29 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:18:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:18:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:18:54 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:18:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:18:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:18:58 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:31:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:31:34 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:31:34 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:31:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:31:36 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:31:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:31:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:31:39 GMT
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
	-	`sha256:08676902305ce1488e47f2c6cf37c156f8adf34592d23cb6c0adda7f8e20bbec`  
		Last Modified: Tue, 09 Jan 2024 22:27:11 GMT  
		Size: 64.2 MB (64202869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007761f68f098a06788d8a4f5b63c5c25fa52e8f613da754d12a9c8005b2ad44`  
		Last Modified: Tue, 09 Jan 2024 22:26:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28beac3397f3e144b5cbb889b20e5c6450f5a635fd5679a9ddb77b34420a9512`  
		Last Modified: Tue, 09 Jan 2024 23:31:57 GMT  
		Size: 5.3 MB (5270658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee35c838a10edf1f76e27c99108010f65e1cb2d9cbad31ebe0480cdcc17a15d`  
		Last Modified: Tue, 09 Jan 2024 23:31:56 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce2a624f1055a6b34babd0b44d093aa23653397f4289c89018b0396bebcf038`  
		Last Modified: Tue, 09 Jan 2024 23:31:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; s390x

```console
$ docker pull caddy@sha256:9eb20c4013227f7a3b0435a6f5346ec30763958b3f54f7ad0e7a02a7dd369f5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76184930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c9ebcb7eda5bc7753c6ac25b3a1ea2cbdce628c002973e9ad47ffb0d3ba97e`
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
# Tue, 09 Jan 2024 22:43:43 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:43:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:44:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:44:00 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:44:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:44:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:44:01 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:08:20 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:08:21 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:08:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:08:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:08:22 GMT
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
	-	`sha256:8d670b96a401a5cfb61ad27940492a2027ad1b61a1fa46000d705a1d8d159201`  
		Last Modified: Tue, 09 Jan 2024 22:51:10 GMT  
		Size: 66.3 MB (66302457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da6e3a038c3bd2afee0afab16ad35ea548d1966b1df80e55d9dcee9b280b371`  
		Last Modified: Tue, 09 Jan 2024 22:50:59 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08206a39be152f3861e70f6c3448542421f3249680b9274fd278f6015cc11aa5`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 5.1 MB (5116980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a1075ed747212d8e9506ed70d4cccab2b94dd685aa98e25a32f43575e21839`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 1.3 MB (1262390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76b6771ab88a9777236c173bb24bbc313a76da44e25c4c9ce07f8ff003338ee`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - windows version 10.0.17763.5206; amd64

```console
$ docker pull caddy@sha256:76e18d17fe903d45f1f88f9ba76237a5fdb8392b670b3d2b0b581a9a8a4067de
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2156673231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267688b3ce7bd013fc2b9407cba404926536c40d42366eedebe5680d607fa176`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 12 Dec 2023 23:38:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Dec 2023 23:38:53 GMT
ENV GIT_VERSION=2.23.0
# Tue, 12 Dec 2023 23:38:53 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 12 Dec 2023 23:38:54 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 12 Dec 2023 23:38:55 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 12 Dec 2023 23:40:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 12 Dec 2023 23:40:27 GMT
ENV GOPATH=C:\go
# Tue, 12 Dec 2023 23:41:35 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jan 2024 22:18:47 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:22:02 GMT
RUN $url = 'https://dl.google.com/go/go1.21.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27ac9dd6e66fb3fd0acfa6792ff053c86e7d2c055b022f4b5d53bfddec9e3301'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Jan 2024 22:22:04 GMT
WORKDIR C:\go
# Tue, 09 Jan 2024 23:00:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jan 2024 23:00:16 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:00:17 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:00:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:01:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 09 Jan 2024 23:01:37 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767e95390edb4050b2c57e1d564c9e4722c5ae776ebfb8907a539571a2609f7c`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c57683b4a629f3325c8517d99f497d4ffbcd0e70354e70a95d983a275bfe398`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95bef40c25d2abc3a12986675189e7152f6197fdc5a17343bdee3f0bc2e95a8`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043d50fbb4f0d8961fe3a95130f520d57cfe7e6e85b15cd4f9f14a01364f7ee`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55867ab446b5d5e34f9e6d414898b9a0b31051afc81b28ace1ce47e27d9e24ee`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10285db29cf842d22a49b00cb66fbbfe20e7d4e72a0d3e393d58824190f6835b`  
		Last Modified: Wed, 13 Dec 2023 00:04:19 GMT  
		Size: 25.6 MB (25558777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3037ad7a881ee540014f48a43aa3a857c479d9cefb413ce61a914c943901890b`  
		Last Modified: Wed, 13 Dec 2023 00:04:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788faab53b378465ec447dde1961338c1349487d1152856c0524e2f6a503ec70`  
		Last Modified: Wed, 13 Dec 2023 00:04:12 GMT  
		Size: 282.5 KB (282534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca23066a92625cdc8de9b99f08faf5c3e756534401f72ec8aff465b29c481ee`  
		Last Modified: Tue, 09 Jan 2024 22:39:56 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b92d2b727a3677f7df423fdb871102a4f49e8ab3c3f27447b46a8bb9d6315c5`  
		Last Modified: Tue, 09 Jan 2024 22:40:17 GMT  
		Size: 69.4 MB (69428911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c07e208b8230a3cf4f0d09d8d2e0964843388a9334a811e7537778242b4610`  
		Last Modified: Tue, 09 Jan 2024 22:39:56 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0002a397ba0f92a6b352156052f4a5f9bf5bd0b854e9e066dc85b8231b8d23`  
		Last Modified: Tue, 09 Jan 2024 23:03:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221d1a0d3e162f0c5064835e1683a547fb68ce0fe6ddbc15547e97547f4a815f`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9d6843b6bad3862684d5eade7e7816b48ce845effe90d8c1d5d5250151dd55`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173a315f398d136fd23d058d13fa18b082575f9732c3cc17a733570a15d53606`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e288abae7098c76d0379b4bb3808523310f24e5aa535a62ff1405875e5723c`  
		Last Modified: Tue, 09 Jan 2024 23:03:11 GMT  
		Size: 1.7 MB (1676147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5e67ad5abb1499f08dbb66b77e1f22ffafb79eeacef131b3863ce4f042fcf2`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - windows version 10.0.20348.2159; amd64

```console
$ docker pull caddy@sha256:b5c196359cb78d80f0c4bb97d3ffbf13a84eb3003c9f238f72cec005c9475105
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1986234916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3131c915e036b0f95ea6c698ffaf9974f6dbce70dc8d2cd1600175d4155dde16`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Tue, 12 Dec 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Dec 2023 23:35:08 GMT
ENV GIT_VERSION=2.23.0
# Tue, 12 Dec 2023 23:35:08 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 12 Dec 2023 23:35:09 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 12 Dec 2023 23:35:10 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 12 Dec 2023 23:35:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 12 Dec 2023 23:35:47 GMT
ENV GOPATH=C:\go
# Tue, 12 Dec 2023 23:36:11 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jan 2024 22:16:03 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:18:27 GMT
RUN $url = 'https://dl.google.com/go/go1.21.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27ac9dd6e66fb3fd0acfa6792ff053c86e7d2c055b022f4b5d53bfddec9e3301'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Jan 2024 22:18:28 GMT
WORKDIR C:\go
# Tue, 09 Jan 2024 23:02:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jan 2024 23:02:03 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:02:04 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:02:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:02:30 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 09 Jan 2024 23:02:31 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d0c853ded9068434b9128a8016b3ae5e18f748f62801c7bb6e6092495300ec`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf365c1e9d59a58fc8cee2522db9139b36cf02ecabe7302489a9a3667b62cea`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69dbeb610a3fa1c3f2962202c58796ff120ea20cc3ba1f2fce807cbbe2c37ab0`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a3be8233329999132fa6e504f39c44abd589439a96846e31508037334d6d11`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755721e8166183821011ca0acdb563f67887cfe33da36997710b182f049fbede`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4700bd9f606505ec47d78dc66a509ca78ea2a8269a8e2b9bcf28ec33c5cbea74`  
		Last Modified: Wed, 13 Dec 2023 00:02:42 GMT  
		Size: 25.6 MB (25554973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777ab971ccee32e15de39ed82eceeb004d2d6f94af7c43ab3d6cfc1baf0abd07`  
		Last Modified: Wed, 13 Dec 2023 00:02:35 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958aa1458398ceb3a543d13279579cc48507080df3b269a5aa1a09da23b03ccf`  
		Last Modified: Wed, 13 Dec 2023 00:02:35 GMT  
		Size: 284.9 KB (284874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ed7a59b16104881efb9e3ac02b81f631cff124b04d7494d955a2c697b7c4ce`  
		Last Modified: Tue, 09 Jan 2024 22:39:21 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b1d528d83cdc1c6fb3f551b955643ffa64d14478df3d1b2aa1faf3cf95d454`  
		Last Modified: Tue, 09 Jan 2024 22:39:41 GMT  
		Size: 69.4 MB (69432029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8730c2425648e897784c3ff628a5fd72bb913811c924412142d22ce7f7d36c`  
		Last Modified: Tue, 09 Jan 2024 22:39:21 GMT  
		Size: 1.5 KB (1539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea60c3b2caff00ee0011a9148cabb96e3a1cde3a81a8ee5b7ca60f5513aff78`  
		Last Modified: Tue, 09 Jan 2024 23:03:30 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f939916b2a0c9fde832abafdf561e4515fc15d11979c5fa3e0bf8165cb4b3a`  
		Last Modified: Tue, 09 Jan 2024 23:03:28 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12cb1ee578e943a57f3c817517ac6b636e4d08c82aaacf57d4002b9732d98b0`  
		Last Modified: Tue, 09 Jan 2024 23:03:27 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c98bc1e6119b0ada6f9e06e3c88634debef4de96ad9906ac1d7065774a50a4f`  
		Last Modified: Tue, 09 Jan 2024 23:03:28 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc678bb3572a4a425d6d29f6ab5a6cbb6fb1e1cf427c0ed3982f9e451901c69`  
		Last Modified: Tue, 09 Jan 2024 23:03:28 GMT  
		Size: 1.7 MB (1671314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8151c697df9e9b88184cda0002778dff9d013f6ebd7c46924622bcb222243585`  
		Last Modified: Tue, 09 Jan 2024 23:03:27 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-alpine`

```console
$ docker pull caddy@sha256:88ea79d5d4c27d14e88147a8ee7880afdd51b939d2fc2b455146a10fbc326986
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
$ docker pull caddy@sha256:40fb52ba04a15d7b79c65ccf594655c93ef84951d4b5f3636dd741c6f7117c82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77049039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec8a77457f35f87a6c0e163b4b9ca06831e9597838815cdfafd6924007b2053`
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
# Tue, 09 Jan 2024 22:20:46 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:20:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:20:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:20:57 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:20:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:20:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:20:58 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:13:01 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:13:01 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:13:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:13:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:13:03 GMT
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
	-	`sha256:2786abec99e189a4a116c45771654dd1220a5a78deb32430974d369c08fa4bd0`  
		Last Modified: Tue, 09 Jan 2024 22:27:13 GMT  
		Size: 67.1 MB (67086665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ece744550870593fb66b630e5fa62ae11cf9c89547275dd4450952b0fc9460`  
		Last Modified: Tue, 09 Jan 2024 22:27:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3a3a5ccc6f4610e4fd60832b6c63eed6366cfe0b0f37e3e6125f54aef9f135`  
		Last Modified: Tue, 09 Jan 2024 23:13:20 GMT  
		Size: 5.0 MB (4972463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe0d8e469393bc3c86e3dc711c99a557728a8c0e8a67a85f65d7fdc195034cd`  
		Last Modified: Tue, 09 Jan 2024 23:13:19 GMT  
		Size: 1.3 MB (1302233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761ef04b7c1f8fcec7e6f8b1f4995bdf8f34100b19140a0faef407b758829e8d`  
		Last Modified: Tue, 09 Jan 2024 23:13:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:83a8b023f6fa4c601dca30abe334e1243463e92f8e84e33dac925e8d6f7a601f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75411881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a0ab3fe89b994d3ff35471a8b1709d10e3ca724eb9a2e14bac7221211877bb`
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
# Wed, 20 Dec 2023 21:34:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Wed, 20 Dec 2023 21:34:12 GMT
ENV GOTOOLCHAIN=local
# Wed, 20 Dec 2023 21:34:12 GMT
ENV GOPATH=/go
# Wed, 20 Dec 2023 21:34:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 21:34:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 20 Dec 2023 21:34:13 GMT
WORKDIR /go
# Wed, 20 Dec 2023 21:51:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 20 Dec 2023 21:51:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_SETCAP=1
# Wed, 20 Dec 2023 21:51:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 20 Dec 2023 21:51:43 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 20 Dec 2023 21:51:43 GMT
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
	-	`sha256:29bee9d75e3ae91d44ddf09cf0fa198b556654c8073aa50d8b630e52a5d203be`  
		Last Modified: Wed, 20 Dec 2023 21:36:17 GMT  
		Size: 65.8 MB (65764273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a485eddce12cbac59d4532427a2f3bc7f475a18f1b6ddc05d3631682cde4be3e`  
		Last Modified: Wed, 20 Dec 2023 21:36:00 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460d4992c24f213c1a4f97d850c33f2a32be4f0763f60ae881dfb36929edbeb8`  
		Last Modified: Wed, 20 Dec 2023 21:52:07 GMT  
		Size: 5.0 MB (4966637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf270d0f9df22c9f4d54cc419be9b59b79eec2ef2f2c70fa2545347b5db6a1de`  
		Last Modified: Wed, 20 Dec 2023 21:52:07 GMT  
		Size: 1.2 MB (1248658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29559d6667b029d9d030a6d020a049a1c7df7a5d84b925b75e0b37d63be04d25`  
		Last Modified: Wed, 20 Dec 2023 21:52:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:286339d083a589ff4ee17f2a98eabb1011f13f93e40c79bba2af0748f9bf2c8c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74795731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08540a67a8309258e1b934ca527574a28d9cd09a153f09e55635d67a11e5572d`
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
# Tue, 09 Jan 2024 22:59:02 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:59:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:59:24 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:59:24 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:59:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:59:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:59:27 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:59:28 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:59:29 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:59:29 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:59:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:59:30 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:59:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:59:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:59:33 GMT
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
	-	`sha256:f975e362e12b206661ef3e8661f8ddef5b3886db6695858a6ee13107cfb406cd`  
		Last Modified: Tue, 09 Jan 2024 23:10:25 GMT  
		Size: 65.8 MB (65849716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d88a6cd0c6e987e9c7854e8091bc0d3da0f5215dc272d31db2a10463a597eb`  
		Last Modified: Tue, 09 Jan 2024 23:10:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ccd85286302c0f7692dc9bf9e673cc831252fa3892db98d4a388f8e3a40229`  
		Last Modified: Tue, 09 Jan 2024 23:59:54 GMT  
		Size: 4.5 MB (4514276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c77c0eb7e54b1d25489fbedb6607137e9123f25be63514940cec48f5afbcbb`  
		Last Modified: Tue, 09 Jan 2024 23:59:53 GMT  
		Size: 1.2 MB (1246091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe6c53215469f1e0efd2612e28e7bc3d644b7460fdac4ed2217adcfcbb01ff`  
		Last Modified: Tue, 09 Jan 2024 23:59:53 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:29c1d8e221c7025b5fa2bd564d67b2cbe54abf6ed141469ee753714d4b86de8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74062596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751a7ab9b4f36aa69472a02e61896bae0e9f5d4d8751e6a7791c550f914532f6`
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
# Tue, 09 Jan 2024 22:40:13 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:40:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:40:23 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:40:23 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:40:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:40:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:40:24 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:34:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:34:50 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:34:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:34:51 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:34:51 GMT
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
	-	`sha256:f784b2816c0487ec6a1efb9635a001a738ce6794c6f60cef8dd8fc658663da9f`  
		Last Modified: Tue, 09 Jan 2024 22:45:17 GMT  
		Size: 64.2 MB (64173642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2878d57b8185e91fa6aee756ccda964266f809fac11f9dce2ed4fbfd8912f1a9`  
		Last Modified: Tue, 09 Jan 2024 22:45:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab371eb8298e2716c51ac9c58092131a438b00268b67ae458e1ace0ff2b0b5a`  
		Last Modified: Tue, 09 Jan 2024 23:35:05 GMT  
		Size: 5.1 MB (5070606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797b9a67275bffa5caa99271d04d6986b812b4aa84192f9ba3f1ff7b1dfed362`  
		Last Modified: Tue, 09 Jan 2024 23:35:05 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13428147a58f4a789fd5d1f01d54bef643a726131dd40b35c267f16843158a6c`  
		Last Modified: Tue, 09 Jan 2024 23:35:04 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:745364722abfeb88309b8c87aaea59721a3b9ce6770ef2ece3727cd89c4ecdb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74295245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ca8de75928fb38f0a93327b23d822645315bee4c8d32dbc96b28ffbf4f513b`
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
# Tue, 09 Jan 2024 22:18:29 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:18:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:18:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:18:54 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:18:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:18:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:18:58 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:31:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:31:34 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:31:34 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:31:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:31:36 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:31:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:31:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:31:39 GMT
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
	-	`sha256:08676902305ce1488e47f2c6cf37c156f8adf34592d23cb6c0adda7f8e20bbec`  
		Last Modified: Tue, 09 Jan 2024 22:27:11 GMT  
		Size: 64.2 MB (64202869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007761f68f098a06788d8a4f5b63c5c25fa52e8f613da754d12a9c8005b2ad44`  
		Last Modified: Tue, 09 Jan 2024 22:26:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28beac3397f3e144b5cbb889b20e5c6450f5a635fd5679a9ddb77b34420a9512`  
		Last Modified: Tue, 09 Jan 2024 23:31:57 GMT  
		Size: 5.3 MB (5270658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee35c838a10edf1f76e27c99108010f65e1cb2d9cbad31ebe0480cdcc17a15d`  
		Last Modified: Tue, 09 Jan 2024 23:31:56 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce2a624f1055a6b34babd0b44d093aa23653397f4289c89018b0396bebcf038`  
		Last Modified: Tue, 09 Jan 2024 23:31:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:9eb20c4013227f7a3b0435a6f5346ec30763958b3f54f7ad0e7a02a7dd369f5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76184930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c9ebcb7eda5bc7753c6ac25b3a1ea2cbdce628c002973e9ad47ffb0d3ba97e`
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
# Tue, 09 Jan 2024 22:43:43 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:43:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:44:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:44:00 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:44:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:44:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:44:01 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:08:20 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:08:21 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:08:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:08:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:08:22 GMT
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
	-	`sha256:8d670b96a401a5cfb61ad27940492a2027ad1b61a1fa46000d705a1d8d159201`  
		Last Modified: Tue, 09 Jan 2024 22:51:10 GMT  
		Size: 66.3 MB (66302457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da6e3a038c3bd2afee0afab16ad35ea548d1966b1df80e55d9dcee9b280b371`  
		Last Modified: Tue, 09 Jan 2024 22:50:59 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08206a39be152f3861e70f6c3448542421f3249680b9274fd278f6015cc11aa5`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 5.1 MB (5116980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a1075ed747212d8e9506ed70d4cccab2b94dd685aa98e25a32f43575e21839`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 1.3 MB (1262390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76b6771ab88a9777236c173bb24bbc313a76da44e25c4c9ce07f8ff003338ee`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:ee4395a3f6f47c0262fc9b8b002b6f27c88ea7f60afa086af1976dbc4aac28b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `caddy:2.7-builder-windowsservercore-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull caddy@sha256:76e18d17fe903d45f1f88f9ba76237a5fdb8392b670b3d2b0b581a9a8a4067de
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2156673231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267688b3ce7bd013fc2b9407cba404926536c40d42366eedebe5680d607fa176`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 12 Dec 2023 23:38:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Dec 2023 23:38:53 GMT
ENV GIT_VERSION=2.23.0
# Tue, 12 Dec 2023 23:38:53 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 12 Dec 2023 23:38:54 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 12 Dec 2023 23:38:55 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 12 Dec 2023 23:40:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 12 Dec 2023 23:40:27 GMT
ENV GOPATH=C:\go
# Tue, 12 Dec 2023 23:41:35 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jan 2024 22:18:47 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:22:02 GMT
RUN $url = 'https://dl.google.com/go/go1.21.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27ac9dd6e66fb3fd0acfa6792ff053c86e7d2c055b022f4b5d53bfddec9e3301'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Jan 2024 22:22:04 GMT
WORKDIR C:\go
# Tue, 09 Jan 2024 23:00:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jan 2024 23:00:16 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:00:17 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:00:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:01:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 09 Jan 2024 23:01:37 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767e95390edb4050b2c57e1d564c9e4722c5ae776ebfb8907a539571a2609f7c`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c57683b4a629f3325c8517d99f497d4ffbcd0e70354e70a95d983a275bfe398`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95bef40c25d2abc3a12986675189e7152f6197fdc5a17343bdee3f0bc2e95a8`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043d50fbb4f0d8961fe3a95130f520d57cfe7e6e85b15cd4f9f14a01364f7ee`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55867ab446b5d5e34f9e6d414898b9a0b31051afc81b28ace1ce47e27d9e24ee`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10285db29cf842d22a49b00cb66fbbfe20e7d4e72a0d3e393d58824190f6835b`  
		Last Modified: Wed, 13 Dec 2023 00:04:19 GMT  
		Size: 25.6 MB (25558777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3037ad7a881ee540014f48a43aa3a857c479d9cefb413ce61a914c943901890b`  
		Last Modified: Wed, 13 Dec 2023 00:04:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788faab53b378465ec447dde1961338c1349487d1152856c0524e2f6a503ec70`  
		Last Modified: Wed, 13 Dec 2023 00:04:12 GMT  
		Size: 282.5 KB (282534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca23066a92625cdc8de9b99f08faf5c3e756534401f72ec8aff465b29c481ee`  
		Last Modified: Tue, 09 Jan 2024 22:39:56 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b92d2b727a3677f7df423fdb871102a4f49e8ab3c3f27447b46a8bb9d6315c5`  
		Last Modified: Tue, 09 Jan 2024 22:40:17 GMT  
		Size: 69.4 MB (69428911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c07e208b8230a3cf4f0d09d8d2e0964843388a9334a811e7537778242b4610`  
		Last Modified: Tue, 09 Jan 2024 22:39:56 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0002a397ba0f92a6b352156052f4a5f9bf5bd0b854e9e066dc85b8231b8d23`  
		Last Modified: Tue, 09 Jan 2024 23:03:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221d1a0d3e162f0c5064835e1683a547fb68ce0fe6ddbc15547e97547f4a815f`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9d6843b6bad3862684d5eade7e7816b48ce845effe90d8c1d5d5250151dd55`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173a315f398d136fd23d058d13fa18b082575f9732c3cc17a733570a15d53606`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e288abae7098c76d0379b4bb3808523310f24e5aa535a62ff1405875e5723c`  
		Last Modified: Tue, 09 Jan 2024 23:03:11 GMT  
		Size: 1.7 MB (1676147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5e67ad5abb1499f08dbb66b77e1f22ffafb79eeacef131b3863ce4f042fcf2`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:3d08e6c2e2cef96a5a8f6ddb7531801ad745003ddac2d632d9679e2c30f95e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2159; amd64

### `caddy:2.7-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2159; amd64

```console
$ docker pull caddy@sha256:b5c196359cb78d80f0c4bb97d3ffbf13a84eb3003c9f238f72cec005c9475105
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1986234916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3131c915e036b0f95ea6c698ffaf9974f6dbce70dc8d2cd1600175d4155dde16`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Tue, 12 Dec 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Dec 2023 23:35:08 GMT
ENV GIT_VERSION=2.23.0
# Tue, 12 Dec 2023 23:35:08 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 12 Dec 2023 23:35:09 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 12 Dec 2023 23:35:10 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 12 Dec 2023 23:35:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 12 Dec 2023 23:35:47 GMT
ENV GOPATH=C:\go
# Tue, 12 Dec 2023 23:36:11 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jan 2024 22:16:03 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:18:27 GMT
RUN $url = 'https://dl.google.com/go/go1.21.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27ac9dd6e66fb3fd0acfa6792ff053c86e7d2c055b022f4b5d53bfddec9e3301'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Jan 2024 22:18:28 GMT
WORKDIR C:\go
# Tue, 09 Jan 2024 23:02:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jan 2024 23:02:03 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:02:04 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:02:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:02:30 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 09 Jan 2024 23:02:31 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d0c853ded9068434b9128a8016b3ae5e18f748f62801c7bb6e6092495300ec`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf365c1e9d59a58fc8cee2522db9139b36cf02ecabe7302489a9a3667b62cea`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69dbeb610a3fa1c3f2962202c58796ff120ea20cc3ba1f2fce807cbbe2c37ab0`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a3be8233329999132fa6e504f39c44abd589439a96846e31508037334d6d11`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755721e8166183821011ca0acdb563f67887cfe33da36997710b182f049fbede`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4700bd9f606505ec47d78dc66a509ca78ea2a8269a8e2b9bcf28ec33c5cbea74`  
		Last Modified: Wed, 13 Dec 2023 00:02:42 GMT  
		Size: 25.6 MB (25554973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777ab971ccee32e15de39ed82eceeb004d2d6f94af7c43ab3d6cfc1baf0abd07`  
		Last Modified: Wed, 13 Dec 2023 00:02:35 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958aa1458398ceb3a543d13279579cc48507080df3b269a5aa1a09da23b03ccf`  
		Last Modified: Wed, 13 Dec 2023 00:02:35 GMT  
		Size: 284.9 KB (284874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ed7a59b16104881efb9e3ac02b81f631cff124b04d7494d955a2c697b7c4ce`  
		Last Modified: Tue, 09 Jan 2024 22:39:21 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b1d528d83cdc1c6fb3f551b955643ffa64d14478df3d1b2aa1faf3cf95d454`  
		Last Modified: Tue, 09 Jan 2024 22:39:41 GMT  
		Size: 69.4 MB (69432029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8730c2425648e897784c3ff628a5fd72bb913811c924412142d22ce7f7d36c`  
		Last Modified: Tue, 09 Jan 2024 22:39:21 GMT  
		Size: 1.5 KB (1539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea60c3b2caff00ee0011a9148cabb96e3a1cde3a81a8ee5b7ca60f5513aff78`  
		Last Modified: Tue, 09 Jan 2024 23:03:30 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f939916b2a0c9fde832abafdf561e4515fc15d11979c5fa3e0bf8165cb4b3a`  
		Last Modified: Tue, 09 Jan 2024 23:03:28 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12cb1ee578e943a57f3c817517ac6b636e4d08c82aaacf57d4002b9732d98b0`  
		Last Modified: Tue, 09 Jan 2024 23:03:27 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c98bc1e6119b0ada6f9e06e3c88634debef4de96ad9906ac1d7065774a50a4f`  
		Last Modified: Tue, 09 Jan 2024 23:03:28 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc678bb3572a4a425d6d29f6ab5a6cbb6fb1e1cf427c0ed3982f9e451901c69`  
		Last Modified: Tue, 09 Jan 2024 23:03:28 GMT  
		Size: 1.7 MB (1671314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8151c697df9e9b88184cda0002778dff9d013f6ebd7c46924622bcb222243585`  
		Last Modified: Tue, 09 Jan 2024 23:03:27 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-windowsservercore`

```console
$ docker pull caddy@sha256:972db88b238031234d870fded48029f384e208fa23012db80dd8de6adc65d559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.5206; amd64
	-	windows version 10.0.20348.2159; amd64

### `caddy:2.7-windowsservercore` - windows version 10.0.17763.5206; amd64

```console
$ docker pull caddy@sha256:23906c96e8647871d54638ee95201b15a6780bd5c5a55e1910f1cce47f51327a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075748892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd668c1e74ca31419de6a4894168996b6be13d2cfb6dda297f76f1f0e82af65`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 12 Dec 2023 23:38:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 02:30:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Dec 2023 02:30:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Dec 2023 02:32:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Dec 2023 02:32:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Dec 2023 02:32:03 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Dec 2023 02:32:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Dec 2023 02:32:05 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Dec 2023 02:32:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Dec 2023 02:32:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Dec 2023 02:32:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Dec 2023 02:32:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Dec 2023 02:32:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Dec 2023 02:32:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Dec 2023 02:32:11 GMT
EXPOSE 80
# Wed, 13 Dec 2023 02:32:12 GMT
EXPOSE 443
# Wed, 13 Dec 2023 02:32:13 GMT
EXPOSE 443/udp
# Wed, 13 Dec 2023 02:32:13 GMT
EXPOSE 2019
# Wed, 13 Dec 2023 02:33:19 GMT
RUN caddy version
# Wed, 13 Dec 2023 02:33:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767e95390edb4050b2c57e1d564c9e4722c5ae776ebfb8907a539571a2609f7c`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc953d49171296238d791f543a2a026383540af60c9b10cc72446745ea9e517`  
		Last Modified: Wed, 13 Dec 2023 02:38:55 GMT  
		Size: 466.4 KB (466376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5091a1fcf41a799b6b5325321d36e20072d566027eeecc072788a9a3c3afbf0b`  
		Last Modified: Wed, 13 Dec 2023 02:38:54 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d0c21ea3d396314641058b6087c719f00acf6e81a122d0308c76705b454c5a`  
		Last Modified: Wed, 13 Dec 2023 02:38:58 GMT  
		Size: 15.3 MB (15282292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7c1ffefa6eaf8ceb9b6964a75043f3440c260e5ef8a7757a4902bbd87b5a11`  
		Last Modified: Wed, 13 Dec 2023 02:38:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209a9db6a8a0e20f16c07fa90f84ff5f0fbcf8896b719c5282405503804e4975`  
		Last Modified: Wed, 13 Dec 2023 02:38:53 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e6508c4f7300255ca275dc9fa4b8ff9f4e4ff4e6c552afee4d03305e571f8`  
		Last Modified: Wed, 13 Dec 2023 02:38:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571a096f7d34249fda9c90244912f35e632dc8c3c50a830c1d3dc6d5d2234264`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee679db41077812368c0ee8780348a81cc00878e2848106d2b022cfa25222615`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61da3eb55b53d10c6d39556e06adcd87b1e813dbf6e7c0c09a4a1fcd3c1a02af`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67d27f68c7ff3cf8ec13fd0ae72ac89b781c819f1959e16c22101faa49884a1`  
		Last Modified: Wed, 13 Dec 2023 02:38:51 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b0c532fc98f8438a57e314863455c2812c5f8273718a387893d58b1eae45a7`  
		Last Modified: Wed, 13 Dec 2023 02:38:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb76494edec3148a22e8826aa2cceb75046d74559b7fe31713da82a5504d187`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621db1494746176522163d644f8f6d572003928346b37dfea1118539767375bf`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e621e03d954adf248bd9ddcdfe28108be9204a2f010bc44cd49534bc26d10c`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb96c188ceb57176f56af8649f49ebde260394730cc2ee6bd5a10634d6676bc`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e2237c5f2e48a944f2cdc493acec61ca707749a0d33362f62a1162e6967f7f`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b904a8ec5a95b1df9b634285424830763de3a36377f8f97be9383346cd82022`  
		Last Modified: Wed, 13 Dec 2023 02:38:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ae7bbabfc6a290ea47a42a976c34545f19465895a8dee1bd94b9f6351d9ae`  
		Last Modified: Wed, 13 Dec 2023 02:38:49 GMT  
		Size: 269.0 KB (268985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4235be6cdbcf40a5350abf8550ae54349cd6889349bacb2c4c6fcdabb02fcb`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-windowsservercore` - windows version 10.0.20348.2159; amd64

```console
$ docker pull caddy@sha256:8b2e9ac9b72c8b2c90bc15116cedbb8044d599e4f86ffcbb48cebdfdf97d19f7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1905326657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7092fad7c71072036e6f6e418de96b9a293b2a5fa6c1f533192cee80981c2fdf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Tue, 12 Dec 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 02:33:55 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Dec 2023 02:33:56 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Dec 2023 02:35:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Dec 2023 02:35:11 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Dec 2023 02:35:12 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Dec 2023 02:35:12 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Dec 2023 02:35:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Dec 2023 02:35:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Dec 2023 02:35:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Dec 2023 02:35:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Dec 2023 02:35:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Dec 2023 02:35:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Dec 2023 02:35:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Dec 2023 02:35:19 GMT
EXPOSE 80
# Wed, 13 Dec 2023 02:35:20 GMT
EXPOSE 443
# Wed, 13 Dec 2023 02:35:21 GMT
EXPOSE 443/udp
# Wed, 13 Dec 2023 02:35:23 GMT
EXPOSE 2019
# Wed, 13 Dec 2023 02:35:42 GMT
RUN caddy version
# Wed, 13 Dec 2023 02:35:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d0c853ded9068434b9128a8016b3ae5e18f748f62801c7bb6e6092495300ec`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d3c17fb1ca1499edf5a0a7fe2ed357de61bc5478580af8c193d8c59e8139`  
		Last Modified: Wed, 13 Dec 2023 02:39:22 GMT  
		Size: 468.6 KB (468557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0205b9bfc982e2d76e931acf88ef85dfe1c943d4412d8e0abc82f7f0837e3ffe`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be685bdfb2389b99d51da84fb605d5905240fb7fbb82779d90949871c42c3a01`  
		Last Modified: Wed, 13 Dec 2023 02:39:24 GMT  
		Size: 15.3 MB (15270636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9935999a24844b91a4364fda0be1e1ffa280fb0c3c3c51157ffee05dc396bc2`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bd056752e2fad4d5b1e26bda93daeb2e2b89b03fc440f547e8e8e57b56ec54`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bff69c07007af0ff21680f637729be4b8d66a9b114305a47b54b631e499932`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8602ee7f30c15eb312beb9be91c2987f09264a3ec61fab2a25f7388c80361e65`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d98bd6b64e0a8382fcdef83a12bb138867f39b06a481c87d92f5e8b6bd637db`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab994312751dbeec291009c1153b38cf3621f929570200eefc6f838922099b`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb56c650abb1c98df5455b6b8c1864695f45548b82de29e570ce3f46299e574d`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b69a6fa036380dd82a0f067f8e97178a8da04f68a9c4a9eb4c10f5c432c7ad`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148841d4329f6dd8e152b2fc00676a9c4becd06e9c761400458c7b2d46438314`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8f8b0320cdf29c8f5349e14ec28542bd3c57d39b3d69d580de8ec462540d01`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b20c979eb5abf12332bf27e4b1aa8d06c7b7d6253b88d67681f13191b2ed1f5`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48a3dce4dbfd8b7dec08593b9d5c29404f49689161151ee3dda24b973f91dbe`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbc07c2849a4af7257c854c4fbd200cea57e1d10b82012dfcbe9a675b6fdcc0`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6842cf61f849c09c274f395d1e08b1196c674d9a59c34ddc4a9eb69e190b9d`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6823cd563e14b3750718450028cc7815abe14745863b57adc3e7524f3cdbfcb`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 290.0 KB (289982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae3d36b08abac2ea5a039a22621cc239126e2c32070f73be4efaacfc3c81c91`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-windowsservercore-1809`

```console
$ docker pull caddy@sha256:7c8910562b78f49c3a2f608132f963d70e34352d7b1eba277e11d71c4aadd90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `caddy:2.7-windowsservercore-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull caddy@sha256:23906c96e8647871d54638ee95201b15a6780bd5c5a55e1910f1cce47f51327a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075748892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd668c1e74ca31419de6a4894168996b6be13d2cfb6dda297f76f1f0e82af65`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 12 Dec 2023 23:38:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 02:30:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Dec 2023 02:30:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Dec 2023 02:32:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Dec 2023 02:32:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Dec 2023 02:32:03 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Dec 2023 02:32:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Dec 2023 02:32:05 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Dec 2023 02:32:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Dec 2023 02:32:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Dec 2023 02:32:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Dec 2023 02:32:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Dec 2023 02:32:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Dec 2023 02:32:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Dec 2023 02:32:11 GMT
EXPOSE 80
# Wed, 13 Dec 2023 02:32:12 GMT
EXPOSE 443
# Wed, 13 Dec 2023 02:32:13 GMT
EXPOSE 443/udp
# Wed, 13 Dec 2023 02:32:13 GMT
EXPOSE 2019
# Wed, 13 Dec 2023 02:33:19 GMT
RUN caddy version
# Wed, 13 Dec 2023 02:33:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767e95390edb4050b2c57e1d564c9e4722c5ae776ebfb8907a539571a2609f7c`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc953d49171296238d791f543a2a026383540af60c9b10cc72446745ea9e517`  
		Last Modified: Wed, 13 Dec 2023 02:38:55 GMT  
		Size: 466.4 KB (466376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5091a1fcf41a799b6b5325321d36e20072d566027eeecc072788a9a3c3afbf0b`  
		Last Modified: Wed, 13 Dec 2023 02:38:54 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d0c21ea3d396314641058b6087c719f00acf6e81a122d0308c76705b454c5a`  
		Last Modified: Wed, 13 Dec 2023 02:38:58 GMT  
		Size: 15.3 MB (15282292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7c1ffefa6eaf8ceb9b6964a75043f3440c260e5ef8a7757a4902bbd87b5a11`  
		Last Modified: Wed, 13 Dec 2023 02:38:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209a9db6a8a0e20f16c07fa90f84ff5f0fbcf8896b719c5282405503804e4975`  
		Last Modified: Wed, 13 Dec 2023 02:38:53 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e6508c4f7300255ca275dc9fa4b8ff9f4e4ff4e6c552afee4d03305e571f8`  
		Last Modified: Wed, 13 Dec 2023 02:38:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571a096f7d34249fda9c90244912f35e632dc8c3c50a830c1d3dc6d5d2234264`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee679db41077812368c0ee8780348a81cc00878e2848106d2b022cfa25222615`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61da3eb55b53d10c6d39556e06adcd87b1e813dbf6e7c0c09a4a1fcd3c1a02af`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67d27f68c7ff3cf8ec13fd0ae72ac89b781c819f1959e16c22101faa49884a1`  
		Last Modified: Wed, 13 Dec 2023 02:38:51 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b0c532fc98f8438a57e314863455c2812c5f8273718a387893d58b1eae45a7`  
		Last Modified: Wed, 13 Dec 2023 02:38:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb76494edec3148a22e8826aa2cceb75046d74559b7fe31713da82a5504d187`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621db1494746176522163d644f8f6d572003928346b37dfea1118539767375bf`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e621e03d954adf248bd9ddcdfe28108be9204a2f010bc44cd49534bc26d10c`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb96c188ceb57176f56af8649f49ebde260394730cc2ee6bd5a10634d6676bc`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e2237c5f2e48a944f2cdc493acec61ca707749a0d33362f62a1162e6967f7f`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b904a8ec5a95b1df9b634285424830763de3a36377f8f97be9383346cd82022`  
		Last Modified: Wed, 13 Dec 2023 02:38:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ae7bbabfc6a290ea47a42a976c34545f19465895a8dee1bd94b9f6351d9ae`  
		Last Modified: Wed, 13 Dec 2023 02:38:49 GMT  
		Size: 269.0 KB (268985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4235be6cdbcf40a5350abf8550ae54349cd6889349bacb2c4c6fcdabb02fcb`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:05ced206e45b045bc5cd525d92a16ed5dc3db97b7917edef04152739d06b712b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2159; amd64

### `caddy:2.7-windowsservercore-ltsc2022` - windows version 10.0.20348.2159; amd64

```console
$ docker pull caddy@sha256:8b2e9ac9b72c8b2c90bc15116cedbb8044d599e4f86ffcbb48cebdfdf97d19f7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1905326657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7092fad7c71072036e6f6e418de96b9a293b2a5fa6c1f533192cee80981c2fdf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Tue, 12 Dec 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 02:33:55 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Dec 2023 02:33:56 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Dec 2023 02:35:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Dec 2023 02:35:11 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Dec 2023 02:35:12 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Dec 2023 02:35:12 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Dec 2023 02:35:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Dec 2023 02:35:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Dec 2023 02:35:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Dec 2023 02:35:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Dec 2023 02:35:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Dec 2023 02:35:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Dec 2023 02:35:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Dec 2023 02:35:19 GMT
EXPOSE 80
# Wed, 13 Dec 2023 02:35:20 GMT
EXPOSE 443
# Wed, 13 Dec 2023 02:35:21 GMT
EXPOSE 443/udp
# Wed, 13 Dec 2023 02:35:23 GMT
EXPOSE 2019
# Wed, 13 Dec 2023 02:35:42 GMT
RUN caddy version
# Wed, 13 Dec 2023 02:35:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d0c853ded9068434b9128a8016b3ae5e18f748f62801c7bb6e6092495300ec`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d3c17fb1ca1499edf5a0a7fe2ed357de61bc5478580af8c193d8c59e8139`  
		Last Modified: Wed, 13 Dec 2023 02:39:22 GMT  
		Size: 468.6 KB (468557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0205b9bfc982e2d76e931acf88ef85dfe1c943d4412d8e0abc82f7f0837e3ffe`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be685bdfb2389b99d51da84fb605d5905240fb7fbb82779d90949871c42c3a01`  
		Last Modified: Wed, 13 Dec 2023 02:39:24 GMT  
		Size: 15.3 MB (15270636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9935999a24844b91a4364fda0be1e1ffa280fb0c3c3c51157ffee05dc396bc2`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bd056752e2fad4d5b1e26bda93daeb2e2b89b03fc440f547e8e8e57b56ec54`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bff69c07007af0ff21680f637729be4b8d66a9b114305a47b54b631e499932`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8602ee7f30c15eb312beb9be91c2987f09264a3ec61fab2a25f7388c80361e65`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d98bd6b64e0a8382fcdef83a12bb138867f39b06a481c87d92f5e8b6bd637db`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab994312751dbeec291009c1153b38cf3621f929570200eefc6f838922099b`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb56c650abb1c98df5455b6b8c1864695f45548b82de29e570ce3f46299e574d`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b69a6fa036380dd82a0f067f8e97178a8da04f68a9c4a9eb4c10f5c432c7ad`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148841d4329f6dd8e152b2fc00676a9c4becd06e9c761400458c7b2d46438314`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8f8b0320cdf29c8f5349e14ec28542bd3c57d39b3d69d580de8ec462540d01`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b20c979eb5abf12332bf27e4b1aa8d06c7b7d6253b88d67681f13191b2ed1f5`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48a3dce4dbfd8b7dec08593b9d5c29404f49689161151ee3dda24b973f91dbe`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbc07c2849a4af7257c854c4fbd200cea57e1d10b82012dfcbe9a675b6fdcc0`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6842cf61f849c09c274f395d1e08b1196c674d9a59c34ddc4a9eb69e190b9d`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6823cd563e14b3750718450028cc7815abe14745863b57adc3e7524f3cdbfcb`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 290.0 KB (289982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae3d36b08abac2ea5a039a22621cc239126e2c32070f73be4efaacfc3c81c91`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6`

```console
$ docker pull caddy@sha256:2f148ddb6662b4245ef4ced637e928eaf67a8a1941572d69627652253e779366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5206; amd64
	-	windows version 10.0.20348.2159; amd64

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

### `caddy:2.7.6` - windows version 10.0.17763.5206; amd64

```console
$ docker pull caddy@sha256:23906c96e8647871d54638ee95201b15a6780bd5c5a55e1910f1cce47f51327a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075748892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd668c1e74ca31419de6a4894168996b6be13d2cfb6dda297f76f1f0e82af65`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 12 Dec 2023 23:38:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 02:30:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Dec 2023 02:30:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Dec 2023 02:32:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Dec 2023 02:32:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Dec 2023 02:32:03 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Dec 2023 02:32:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Dec 2023 02:32:05 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Dec 2023 02:32:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Dec 2023 02:32:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Dec 2023 02:32:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Dec 2023 02:32:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Dec 2023 02:32:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Dec 2023 02:32:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Dec 2023 02:32:11 GMT
EXPOSE 80
# Wed, 13 Dec 2023 02:32:12 GMT
EXPOSE 443
# Wed, 13 Dec 2023 02:32:13 GMT
EXPOSE 443/udp
# Wed, 13 Dec 2023 02:32:13 GMT
EXPOSE 2019
# Wed, 13 Dec 2023 02:33:19 GMT
RUN caddy version
# Wed, 13 Dec 2023 02:33:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767e95390edb4050b2c57e1d564c9e4722c5ae776ebfb8907a539571a2609f7c`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc953d49171296238d791f543a2a026383540af60c9b10cc72446745ea9e517`  
		Last Modified: Wed, 13 Dec 2023 02:38:55 GMT  
		Size: 466.4 KB (466376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5091a1fcf41a799b6b5325321d36e20072d566027eeecc072788a9a3c3afbf0b`  
		Last Modified: Wed, 13 Dec 2023 02:38:54 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d0c21ea3d396314641058b6087c719f00acf6e81a122d0308c76705b454c5a`  
		Last Modified: Wed, 13 Dec 2023 02:38:58 GMT  
		Size: 15.3 MB (15282292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7c1ffefa6eaf8ceb9b6964a75043f3440c260e5ef8a7757a4902bbd87b5a11`  
		Last Modified: Wed, 13 Dec 2023 02:38:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209a9db6a8a0e20f16c07fa90f84ff5f0fbcf8896b719c5282405503804e4975`  
		Last Modified: Wed, 13 Dec 2023 02:38:53 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e6508c4f7300255ca275dc9fa4b8ff9f4e4ff4e6c552afee4d03305e571f8`  
		Last Modified: Wed, 13 Dec 2023 02:38:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571a096f7d34249fda9c90244912f35e632dc8c3c50a830c1d3dc6d5d2234264`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee679db41077812368c0ee8780348a81cc00878e2848106d2b022cfa25222615`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61da3eb55b53d10c6d39556e06adcd87b1e813dbf6e7c0c09a4a1fcd3c1a02af`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67d27f68c7ff3cf8ec13fd0ae72ac89b781c819f1959e16c22101faa49884a1`  
		Last Modified: Wed, 13 Dec 2023 02:38:51 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b0c532fc98f8438a57e314863455c2812c5f8273718a387893d58b1eae45a7`  
		Last Modified: Wed, 13 Dec 2023 02:38:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb76494edec3148a22e8826aa2cceb75046d74559b7fe31713da82a5504d187`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621db1494746176522163d644f8f6d572003928346b37dfea1118539767375bf`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e621e03d954adf248bd9ddcdfe28108be9204a2f010bc44cd49534bc26d10c`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb96c188ceb57176f56af8649f49ebde260394730cc2ee6bd5a10634d6676bc`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e2237c5f2e48a944f2cdc493acec61ca707749a0d33362f62a1162e6967f7f`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b904a8ec5a95b1df9b634285424830763de3a36377f8f97be9383346cd82022`  
		Last Modified: Wed, 13 Dec 2023 02:38:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ae7bbabfc6a290ea47a42a976c34545f19465895a8dee1bd94b9f6351d9ae`  
		Last Modified: Wed, 13 Dec 2023 02:38:49 GMT  
		Size: 269.0 KB (268985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4235be6cdbcf40a5350abf8550ae54349cd6889349bacb2c4c6fcdabb02fcb`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6` - windows version 10.0.20348.2159; amd64

```console
$ docker pull caddy@sha256:8b2e9ac9b72c8b2c90bc15116cedbb8044d599e4f86ffcbb48cebdfdf97d19f7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1905326657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7092fad7c71072036e6f6e418de96b9a293b2a5fa6c1f533192cee80981c2fdf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Tue, 12 Dec 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 02:33:55 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Dec 2023 02:33:56 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Dec 2023 02:35:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Dec 2023 02:35:11 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Dec 2023 02:35:12 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Dec 2023 02:35:12 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Dec 2023 02:35:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Dec 2023 02:35:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Dec 2023 02:35:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Dec 2023 02:35:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Dec 2023 02:35:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Dec 2023 02:35:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Dec 2023 02:35:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Dec 2023 02:35:19 GMT
EXPOSE 80
# Wed, 13 Dec 2023 02:35:20 GMT
EXPOSE 443
# Wed, 13 Dec 2023 02:35:21 GMT
EXPOSE 443/udp
# Wed, 13 Dec 2023 02:35:23 GMT
EXPOSE 2019
# Wed, 13 Dec 2023 02:35:42 GMT
RUN caddy version
# Wed, 13 Dec 2023 02:35:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d0c853ded9068434b9128a8016b3ae5e18f748f62801c7bb6e6092495300ec`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d3c17fb1ca1499edf5a0a7fe2ed357de61bc5478580af8c193d8c59e8139`  
		Last Modified: Wed, 13 Dec 2023 02:39:22 GMT  
		Size: 468.6 KB (468557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0205b9bfc982e2d76e931acf88ef85dfe1c943d4412d8e0abc82f7f0837e3ffe`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be685bdfb2389b99d51da84fb605d5905240fb7fbb82779d90949871c42c3a01`  
		Last Modified: Wed, 13 Dec 2023 02:39:24 GMT  
		Size: 15.3 MB (15270636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9935999a24844b91a4364fda0be1e1ffa280fb0c3c3c51157ffee05dc396bc2`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bd056752e2fad4d5b1e26bda93daeb2e2b89b03fc440f547e8e8e57b56ec54`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bff69c07007af0ff21680f637729be4b8d66a9b114305a47b54b631e499932`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8602ee7f30c15eb312beb9be91c2987f09264a3ec61fab2a25f7388c80361e65`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d98bd6b64e0a8382fcdef83a12bb138867f39b06a481c87d92f5e8b6bd637db`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab994312751dbeec291009c1153b38cf3621f929570200eefc6f838922099b`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb56c650abb1c98df5455b6b8c1864695f45548b82de29e570ce3f46299e574d`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b69a6fa036380dd82a0f067f8e97178a8da04f68a9c4a9eb4c10f5c432c7ad`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148841d4329f6dd8e152b2fc00676a9c4becd06e9c761400458c7b2d46438314`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8f8b0320cdf29c8f5349e14ec28542bd3c57d39b3d69d580de8ec462540d01`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b20c979eb5abf12332bf27e4b1aa8d06c7b7d6253b88d67681f13191b2ed1f5`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48a3dce4dbfd8b7dec08593b9d5c29404f49689161151ee3dda24b973f91dbe`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbc07c2849a4af7257c854c4fbd200cea57e1d10b82012dfcbe9a675b6fdcc0`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6842cf61f849c09c274f395d1e08b1196c674d9a59c34ddc4a9eb69e190b9d`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6823cd563e14b3750718450028cc7815abe14745863b57adc3e7524f3cdbfcb`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 290.0 KB (289982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae3d36b08abac2ea5a039a22621cc239126e2c32070f73be4efaacfc3c81c91`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1422 bytes)  
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
$ docker pull caddy@sha256:e4e6def23b2b2ddd4fc962e9e8871d2e1049909f09428e7d3455f3e9fe937126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5206; amd64
	-	windows version 10.0.20348.2159; amd64

### `caddy:2.7.6-builder` - linux; amd64

```console
$ docker pull caddy@sha256:40fb52ba04a15d7b79c65ccf594655c93ef84951d4b5f3636dd741c6f7117c82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77049039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec8a77457f35f87a6c0e163b4b9ca06831e9597838815cdfafd6924007b2053`
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
# Tue, 09 Jan 2024 22:20:46 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:20:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:20:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:20:57 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:20:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:20:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:20:58 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:13:01 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:13:01 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:13:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:13:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:13:03 GMT
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
	-	`sha256:2786abec99e189a4a116c45771654dd1220a5a78deb32430974d369c08fa4bd0`  
		Last Modified: Tue, 09 Jan 2024 22:27:13 GMT  
		Size: 67.1 MB (67086665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ece744550870593fb66b630e5fa62ae11cf9c89547275dd4450952b0fc9460`  
		Last Modified: Tue, 09 Jan 2024 22:27:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3a3a5ccc6f4610e4fd60832b6c63eed6366cfe0b0f37e3e6125f54aef9f135`  
		Last Modified: Tue, 09 Jan 2024 23:13:20 GMT  
		Size: 5.0 MB (4972463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe0d8e469393bc3c86e3dc711c99a557728a8c0e8a67a85f65d7fdc195034cd`  
		Last Modified: Tue, 09 Jan 2024 23:13:19 GMT  
		Size: 1.3 MB (1302233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761ef04b7c1f8fcec7e6f8b1f4995bdf8f34100b19140a0faef407b758829e8d`  
		Last Modified: Tue, 09 Jan 2024 23:13:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:83a8b023f6fa4c601dca30abe334e1243463e92f8e84e33dac925e8d6f7a601f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75411881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a0ab3fe89b994d3ff35471a8b1709d10e3ca724eb9a2e14bac7221211877bb`
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
# Wed, 20 Dec 2023 21:34:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Wed, 20 Dec 2023 21:34:12 GMT
ENV GOTOOLCHAIN=local
# Wed, 20 Dec 2023 21:34:12 GMT
ENV GOPATH=/go
# Wed, 20 Dec 2023 21:34:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 21:34:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 20 Dec 2023 21:34:13 GMT
WORKDIR /go
# Wed, 20 Dec 2023 21:51:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 20 Dec 2023 21:51:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_SETCAP=1
# Wed, 20 Dec 2023 21:51:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 20 Dec 2023 21:51:43 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 20 Dec 2023 21:51:43 GMT
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
	-	`sha256:29bee9d75e3ae91d44ddf09cf0fa198b556654c8073aa50d8b630e52a5d203be`  
		Last Modified: Wed, 20 Dec 2023 21:36:17 GMT  
		Size: 65.8 MB (65764273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a485eddce12cbac59d4532427a2f3bc7f475a18f1b6ddc05d3631682cde4be3e`  
		Last Modified: Wed, 20 Dec 2023 21:36:00 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460d4992c24f213c1a4f97d850c33f2a32be4f0763f60ae881dfb36929edbeb8`  
		Last Modified: Wed, 20 Dec 2023 21:52:07 GMT  
		Size: 5.0 MB (4966637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf270d0f9df22c9f4d54cc419be9b59b79eec2ef2f2c70fa2545347b5db6a1de`  
		Last Modified: Wed, 20 Dec 2023 21:52:07 GMT  
		Size: 1.2 MB (1248658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29559d6667b029d9d030a6d020a049a1c7df7a5d84b925b75e0b37d63be04d25`  
		Last Modified: Wed, 20 Dec 2023 21:52:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:286339d083a589ff4ee17f2a98eabb1011f13f93e40c79bba2af0748f9bf2c8c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74795731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08540a67a8309258e1b934ca527574a28d9cd09a153f09e55635d67a11e5572d`
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
# Tue, 09 Jan 2024 22:59:02 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:59:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:59:24 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:59:24 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:59:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:59:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:59:27 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:59:28 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:59:29 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:59:29 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:59:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:59:30 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:59:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:59:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:59:33 GMT
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
	-	`sha256:f975e362e12b206661ef3e8661f8ddef5b3886db6695858a6ee13107cfb406cd`  
		Last Modified: Tue, 09 Jan 2024 23:10:25 GMT  
		Size: 65.8 MB (65849716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d88a6cd0c6e987e9c7854e8091bc0d3da0f5215dc272d31db2a10463a597eb`  
		Last Modified: Tue, 09 Jan 2024 23:10:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ccd85286302c0f7692dc9bf9e673cc831252fa3892db98d4a388f8e3a40229`  
		Last Modified: Tue, 09 Jan 2024 23:59:54 GMT  
		Size: 4.5 MB (4514276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c77c0eb7e54b1d25489fbedb6607137e9123f25be63514940cec48f5afbcbb`  
		Last Modified: Tue, 09 Jan 2024 23:59:53 GMT  
		Size: 1.2 MB (1246091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe6c53215469f1e0efd2612e28e7bc3d644b7460fdac4ed2217adcfcbb01ff`  
		Last Modified: Tue, 09 Jan 2024 23:59:53 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:29c1d8e221c7025b5fa2bd564d67b2cbe54abf6ed141469ee753714d4b86de8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74062596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751a7ab9b4f36aa69472a02e61896bae0e9f5d4d8751e6a7791c550f914532f6`
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
# Tue, 09 Jan 2024 22:40:13 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:40:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:40:23 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:40:23 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:40:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:40:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:40:24 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:34:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:34:50 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:34:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:34:51 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:34:51 GMT
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
	-	`sha256:f784b2816c0487ec6a1efb9635a001a738ce6794c6f60cef8dd8fc658663da9f`  
		Last Modified: Tue, 09 Jan 2024 22:45:17 GMT  
		Size: 64.2 MB (64173642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2878d57b8185e91fa6aee756ccda964266f809fac11f9dce2ed4fbfd8912f1a9`  
		Last Modified: Tue, 09 Jan 2024 22:45:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab371eb8298e2716c51ac9c58092131a438b00268b67ae458e1ace0ff2b0b5a`  
		Last Modified: Tue, 09 Jan 2024 23:35:05 GMT  
		Size: 5.1 MB (5070606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797b9a67275bffa5caa99271d04d6986b812b4aa84192f9ba3f1ff7b1dfed362`  
		Last Modified: Tue, 09 Jan 2024 23:35:05 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13428147a58f4a789fd5d1f01d54bef643a726131dd40b35c267f16843158a6c`  
		Last Modified: Tue, 09 Jan 2024 23:35:04 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:745364722abfeb88309b8c87aaea59721a3b9ce6770ef2ece3727cd89c4ecdb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74295245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ca8de75928fb38f0a93327b23d822645315bee4c8d32dbc96b28ffbf4f513b`
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
# Tue, 09 Jan 2024 22:18:29 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:18:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:18:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:18:54 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:18:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:18:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:18:58 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:31:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:31:34 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:31:34 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:31:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:31:36 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:31:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:31:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:31:39 GMT
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
	-	`sha256:08676902305ce1488e47f2c6cf37c156f8adf34592d23cb6c0adda7f8e20bbec`  
		Last Modified: Tue, 09 Jan 2024 22:27:11 GMT  
		Size: 64.2 MB (64202869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007761f68f098a06788d8a4f5b63c5c25fa52e8f613da754d12a9c8005b2ad44`  
		Last Modified: Tue, 09 Jan 2024 22:26:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28beac3397f3e144b5cbb889b20e5c6450f5a635fd5679a9ddb77b34420a9512`  
		Last Modified: Tue, 09 Jan 2024 23:31:57 GMT  
		Size: 5.3 MB (5270658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee35c838a10edf1f76e27c99108010f65e1cb2d9cbad31ebe0480cdcc17a15d`  
		Last Modified: Tue, 09 Jan 2024 23:31:56 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce2a624f1055a6b34babd0b44d093aa23653397f4289c89018b0396bebcf038`  
		Last Modified: Tue, 09 Jan 2024 23:31:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; s390x

```console
$ docker pull caddy@sha256:9eb20c4013227f7a3b0435a6f5346ec30763958b3f54f7ad0e7a02a7dd369f5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76184930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c9ebcb7eda5bc7753c6ac25b3a1ea2cbdce628c002973e9ad47ffb0d3ba97e`
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
# Tue, 09 Jan 2024 22:43:43 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:43:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:44:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:44:00 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:44:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:44:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:44:01 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:08:20 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:08:21 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:08:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:08:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:08:22 GMT
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
	-	`sha256:8d670b96a401a5cfb61ad27940492a2027ad1b61a1fa46000d705a1d8d159201`  
		Last Modified: Tue, 09 Jan 2024 22:51:10 GMT  
		Size: 66.3 MB (66302457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da6e3a038c3bd2afee0afab16ad35ea548d1966b1df80e55d9dcee9b280b371`  
		Last Modified: Tue, 09 Jan 2024 22:50:59 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08206a39be152f3861e70f6c3448542421f3249680b9274fd278f6015cc11aa5`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 5.1 MB (5116980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a1075ed747212d8e9506ed70d4cccab2b94dd685aa98e25a32f43575e21839`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 1.3 MB (1262390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76b6771ab88a9777236c173bb24bbc313a76da44e25c4c9ce07f8ff003338ee`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - windows version 10.0.17763.5206; amd64

```console
$ docker pull caddy@sha256:76e18d17fe903d45f1f88f9ba76237a5fdb8392b670b3d2b0b581a9a8a4067de
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2156673231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267688b3ce7bd013fc2b9407cba404926536c40d42366eedebe5680d607fa176`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 12 Dec 2023 23:38:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Dec 2023 23:38:53 GMT
ENV GIT_VERSION=2.23.0
# Tue, 12 Dec 2023 23:38:53 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 12 Dec 2023 23:38:54 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 12 Dec 2023 23:38:55 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 12 Dec 2023 23:40:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 12 Dec 2023 23:40:27 GMT
ENV GOPATH=C:\go
# Tue, 12 Dec 2023 23:41:35 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jan 2024 22:18:47 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:22:02 GMT
RUN $url = 'https://dl.google.com/go/go1.21.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27ac9dd6e66fb3fd0acfa6792ff053c86e7d2c055b022f4b5d53bfddec9e3301'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Jan 2024 22:22:04 GMT
WORKDIR C:\go
# Tue, 09 Jan 2024 23:00:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jan 2024 23:00:16 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:00:17 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:00:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:01:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 09 Jan 2024 23:01:37 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767e95390edb4050b2c57e1d564c9e4722c5ae776ebfb8907a539571a2609f7c`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c57683b4a629f3325c8517d99f497d4ffbcd0e70354e70a95d983a275bfe398`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95bef40c25d2abc3a12986675189e7152f6197fdc5a17343bdee3f0bc2e95a8`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043d50fbb4f0d8961fe3a95130f520d57cfe7e6e85b15cd4f9f14a01364f7ee`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55867ab446b5d5e34f9e6d414898b9a0b31051afc81b28ace1ce47e27d9e24ee`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10285db29cf842d22a49b00cb66fbbfe20e7d4e72a0d3e393d58824190f6835b`  
		Last Modified: Wed, 13 Dec 2023 00:04:19 GMT  
		Size: 25.6 MB (25558777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3037ad7a881ee540014f48a43aa3a857c479d9cefb413ce61a914c943901890b`  
		Last Modified: Wed, 13 Dec 2023 00:04:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788faab53b378465ec447dde1961338c1349487d1152856c0524e2f6a503ec70`  
		Last Modified: Wed, 13 Dec 2023 00:04:12 GMT  
		Size: 282.5 KB (282534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca23066a92625cdc8de9b99f08faf5c3e756534401f72ec8aff465b29c481ee`  
		Last Modified: Tue, 09 Jan 2024 22:39:56 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b92d2b727a3677f7df423fdb871102a4f49e8ab3c3f27447b46a8bb9d6315c5`  
		Last Modified: Tue, 09 Jan 2024 22:40:17 GMT  
		Size: 69.4 MB (69428911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c07e208b8230a3cf4f0d09d8d2e0964843388a9334a811e7537778242b4610`  
		Last Modified: Tue, 09 Jan 2024 22:39:56 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0002a397ba0f92a6b352156052f4a5f9bf5bd0b854e9e066dc85b8231b8d23`  
		Last Modified: Tue, 09 Jan 2024 23:03:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221d1a0d3e162f0c5064835e1683a547fb68ce0fe6ddbc15547e97547f4a815f`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9d6843b6bad3862684d5eade7e7816b48ce845effe90d8c1d5d5250151dd55`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173a315f398d136fd23d058d13fa18b082575f9732c3cc17a733570a15d53606`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e288abae7098c76d0379b4bb3808523310f24e5aa535a62ff1405875e5723c`  
		Last Modified: Tue, 09 Jan 2024 23:03:11 GMT  
		Size: 1.7 MB (1676147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5e67ad5abb1499f08dbb66b77e1f22ffafb79eeacef131b3863ce4f042fcf2`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - windows version 10.0.20348.2159; amd64

```console
$ docker pull caddy@sha256:b5c196359cb78d80f0c4bb97d3ffbf13a84eb3003c9f238f72cec005c9475105
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1986234916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3131c915e036b0f95ea6c698ffaf9974f6dbce70dc8d2cd1600175d4155dde16`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Tue, 12 Dec 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Dec 2023 23:35:08 GMT
ENV GIT_VERSION=2.23.0
# Tue, 12 Dec 2023 23:35:08 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 12 Dec 2023 23:35:09 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 12 Dec 2023 23:35:10 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 12 Dec 2023 23:35:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 12 Dec 2023 23:35:47 GMT
ENV GOPATH=C:\go
# Tue, 12 Dec 2023 23:36:11 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jan 2024 22:16:03 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:18:27 GMT
RUN $url = 'https://dl.google.com/go/go1.21.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27ac9dd6e66fb3fd0acfa6792ff053c86e7d2c055b022f4b5d53bfddec9e3301'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Jan 2024 22:18:28 GMT
WORKDIR C:\go
# Tue, 09 Jan 2024 23:02:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jan 2024 23:02:03 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:02:04 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:02:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:02:30 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 09 Jan 2024 23:02:31 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d0c853ded9068434b9128a8016b3ae5e18f748f62801c7bb6e6092495300ec`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf365c1e9d59a58fc8cee2522db9139b36cf02ecabe7302489a9a3667b62cea`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69dbeb610a3fa1c3f2962202c58796ff120ea20cc3ba1f2fce807cbbe2c37ab0`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a3be8233329999132fa6e504f39c44abd589439a96846e31508037334d6d11`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755721e8166183821011ca0acdb563f67887cfe33da36997710b182f049fbede`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4700bd9f606505ec47d78dc66a509ca78ea2a8269a8e2b9bcf28ec33c5cbea74`  
		Last Modified: Wed, 13 Dec 2023 00:02:42 GMT  
		Size: 25.6 MB (25554973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777ab971ccee32e15de39ed82eceeb004d2d6f94af7c43ab3d6cfc1baf0abd07`  
		Last Modified: Wed, 13 Dec 2023 00:02:35 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958aa1458398ceb3a543d13279579cc48507080df3b269a5aa1a09da23b03ccf`  
		Last Modified: Wed, 13 Dec 2023 00:02:35 GMT  
		Size: 284.9 KB (284874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ed7a59b16104881efb9e3ac02b81f631cff124b04d7494d955a2c697b7c4ce`  
		Last Modified: Tue, 09 Jan 2024 22:39:21 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b1d528d83cdc1c6fb3f551b955643ffa64d14478df3d1b2aa1faf3cf95d454`  
		Last Modified: Tue, 09 Jan 2024 22:39:41 GMT  
		Size: 69.4 MB (69432029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8730c2425648e897784c3ff628a5fd72bb913811c924412142d22ce7f7d36c`  
		Last Modified: Tue, 09 Jan 2024 22:39:21 GMT  
		Size: 1.5 KB (1539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea60c3b2caff00ee0011a9148cabb96e3a1cde3a81a8ee5b7ca60f5513aff78`  
		Last Modified: Tue, 09 Jan 2024 23:03:30 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f939916b2a0c9fde832abafdf561e4515fc15d11979c5fa3e0bf8165cb4b3a`  
		Last Modified: Tue, 09 Jan 2024 23:03:28 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12cb1ee578e943a57f3c817517ac6b636e4d08c82aaacf57d4002b9732d98b0`  
		Last Modified: Tue, 09 Jan 2024 23:03:27 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c98bc1e6119b0ada6f9e06e3c88634debef4de96ad9906ac1d7065774a50a4f`  
		Last Modified: Tue, 09 Jan 2024 23:03:28 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc678bb3572a4a425d6d29f6ab5a6cbb6fb1e1cf427c0ed3982f9e451901c69`  
		Last Modified: Tue, 09 Jan 2024 23:03:28 GMT  
		Size: 1.7 MB (1671314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8151c697df9e9b88184cda0002778dff9d013f6ebd7c46924622bcb222243585`  
		Last Modified: Tue, 09 Jan 2024 23:03:27 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder-alpine`

```console
$ docker pull caddy@sha256:88ea79d5d4c27d14e88147a8ee7880afdd51b939d2fc2b455146a10fbc326986
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
$ docker pull caddy@sha256:40fb52ba04a15d7b79c65ccf594655c93ef84951d4b5f3636dd741c6f7117c82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77049039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec8a77457f35f87a6c0e163b4b9ca06831e9597838815cdfafd6924007b2053`
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
# Tue, 09 Jan 2024 22:20:46 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:20:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:20:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:20:57 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:20:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:20:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:20:58 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:13:01 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:13:01 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:13:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:13:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:13:03 GMT
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
	-	`sha256:2786abec99e189a4a116c45771654dd1220a5a78deb32430974d369c08fa4bd0`  
		Last Modified: Tue, 09 Jan 2024 22:27:13 GMT  
		Size: 67.1 MB (67086665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ece744550870593fb66b630e5fa62ae11cf9c89547275dd4450952b0fc9460`  
		Last Modified: Tue, 09 Jan 2024 22:27:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3a3a5ccc6f4610e4fd60832b6c63eed6366cfe0b0f37e3e6125f54aef9f135`  
		Last Modified: Tue, 09 Jan 2024 23:13:20 GMT  
		Size: 5.0 MB (4972463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe0d8e469393bc3c86e3dc711c99a557728a8c0e8a67a85f65d7fdc195034cd`  
		Last Modified: Tue, 09 Jan 2024 23:13:19 GMT  
		Size: 1.3 MB (1302233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761ef04b7c1f8fcec7e6f8b1f4995bdf8f34100b19140a0faef407b758829e8d`  
		Last Modified: Tue, 09 Jan 2024 23:13:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:83a8b023f6fa4c601dca30abe334e1243463e92f8e84e33dac925e8d6f7a601f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75411881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a0ab3fe89b994d3ff35471a8b1709d10e3ca724eb9a2e14bac7221211877bb`
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
# Wed, 20 Dec 2023 21:34:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Wed, 20 Dec 2023 21:34:12 GMT
ENV GOTOOLCHAIN=local
# Wed, 20 Dec 2023 21:34:12 GMT
ENV GOPATH=/go
# Wed, 20 Dec 2023 21:34:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 21:34:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 20 Dec 2023 21:34:13 GMT
WORKDIR /go
# Wed, 20 Dec 2023 21:51:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 20 Dec 2023 21:51:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_SETCAP=1
# Wed, 20 Dec 2023 21:51:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 20 Dec 2023 21:51:43 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 20 Dec 2023 21:51:43 GMT
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
	-	`sha256:29bee9d75e3ae91d44ddf09cf0fa198b556654c8073aa50d8b630e52a5d203be`  
		Last Modified: Wed, 20 Dec 2023 21:36:17 GMT  
		Size: 65.8 MB (65764273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a485eddce12cbac59d4532427a2f3bc7f475a18f1b6ddc05d3631682cde4be3e`  
		Last Modified: Wed, 20 Dec 2023 21:36:00 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460d4992c24f213c1a4f97d850c33f2a32be4f0763f60ae881dfb36929edbeb8`  
		Last Modified: Wed, 20 Dec 2023 21:52:07 GMT  
		Size: 5.0 MB (4966637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf270d0f9df22c9f4d54cc419be9b59b79eec2ef2f2c70fa2545347b5db6a1de`  
		Last Modified: Wed, 20 Dec 2023 21:52:07 GMT  
		Size: 1.2 MB (1248658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29559d6667b029d9d030a6d020a049a1c7df7a5d84b925b75e0b37d63be04d25`  
		Last Modified: Wed, 20 Dec 2023 21:52:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:286339d083a589ff4ee17f2a98eabb1011f13f93e40c79bba2af0748f9bf2c8c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74795731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08540a67a8309258e1b934ca527574a28d9cd09a153f09e55635d67a11e5572d`
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
# Tue, 09 Jan 2024 22:59:02 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:59:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:59:24 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:59:24 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:59:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:59:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:59:27 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:59:28 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:59:29 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:59:29 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:59:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:59:30 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:59:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:59:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:59:33 GMT
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
	-	`sha256:f975e362e12b206661ef3e8661f8ddef5b3886db6695858a6ee13107cfb406cd`  
		Last Modified: Tue, 09 Jan 2024 23:10:25 GMT  
		Size: 65.8 MB (65849716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d88a6cd0c6e987e9c7854e8091bc0d3da0f5215dc272d31db2a10463a597eb`  
		Last Modified: Tue, 09 Jan 2024 23:10:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ccd85286302c0f7692dc9bf9e673cc831252fa3892db98d4a388f8e3a40229`  
		Last Modified: Tue, 09 Jan 2024 23:59:54 GMT  
		Size: 4.5 MB (4514276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c77c0eb7e54b1d25489fbedb6607137e9123f25be63514940cec48f5afbcbb`  
		Last Modified: Tue, 09 Jan 2024 23:59:53 GMT  
		Size: 1.2 MB (1246091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe6c53215469f1e0efd2612e28e7bc3d644b7460fdac4ed2217adcfcbb01ff`  
		Last Modified: Tue, 09 Jan 2024 23:59:53 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:29c1d8e221c7025b5fa2bd564d67b2cbe54abf6ed141469ee753714d4b86de8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74062596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751a7ab9b4f36aa69472a02e61896bae0e9f5d4d8751e6a7791c550f914532f6`
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
# Tue, 09 Jan 2024 22:40:13 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:40:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:40:23 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:40:23 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:40:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:40:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:40:24 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:34:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:34:50 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:34:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:34:51 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:34:51 GMT
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
	-	`sha256:f784b2816c0487ec6a1efb9635a001a738ce6794c6f60cef8dd8fc658663da9f`  
		Last Modified: Tue, 09 Jan 2024 22:45:17 GMT  
		Size: 64.2 MB (64173642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2878d57b8185e91fa6aee756ccda964266f809fac11f9dce2ed4fbfd8912f1a9`  
		Last Modified: Tue, 09 Jan 2024 22:45:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab371eb8298e2716c51ac9c58092131a438b00268b67ae458e1ace0ff2b0b5a`  
		Last Modified: Tue, 09 Jan 2024 23:35:05 GMT  
		Size: 5.1 MB (5070606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797b9a67275bffa5caa99271d04d6986b812b4aa84192f9ba3f1ff7b1dfed362`  
		Last Modified: Tue, 09 Jan 2024 23:35:05 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13428147a58f4a789fd5d1f01d54bef643a726131dd40b35c267f16843158a6c`  
		Last Modified: Tue, 09 Jan 2024 23:35:04 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:745364722abfeb88309b8c87aaea59721a3b9ce6770ef2ece3727cd89c4ecdb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74295245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ca8de75928fb38f0a93327b23d822645315bee4c8d32dbc96b28ffbf4f513b`
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
# Tue, 09 Jan 2024 22:18:29 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:18:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:18:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:18:54 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:18:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:18:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:18:58 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:31:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:31:34 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:31:34 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:31:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:31:36 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:31:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:31:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:31:39 GMT
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
	-	`sha256:08676902305ce1488e47f2c6cf37c156f8adf34592d23cb6c0adda7f8e20bbec`  
		Last Modified: Tue, 09 Jan 2024 22:27:11 GMT  
		Size: 64.2 MB (64202869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007761f68f098a06788d8a4f5b63c5c25fa52e8f613da754d12a9c8005b2ad44`  
		Last Modified: Tue, 09 Jan 2024 22:26:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28beac3397f3e144b5cbb889b20e5c6450f5a635fd5679a9ddb77b34420a9512`  
		Last Modified: Tue, 09 Jan 2024 23:31:57 GMT  
		Size: 5.3 MB (5270658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee35c838a10edf1f76e27c99108010f65e1cb2d9cbad31ebe0480cdcc17a15d`  
		Last Modified: Tue, 09 Jan 2024 23:31:56 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce2a624f1055a6b34babd0b44d093aa23653397f4289c89018b0396bebcf038`  
		Last Modified: Tue, 09 Jan 2024 23:31:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:9eb20c4013227f7a3b0435a6f5346ec30763958b3f54f7ad0e7a02a7dd369f5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76184930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c9ebcb7eda5bc7753c6ac25b3a1ea2cbdce628c002973e9ad47ffb0d3ba97e`
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
# Tue, 09 Jan 2024 22:43:43 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:43:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:44:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:44:00 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:44:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:44:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:44:01 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:08:20 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:08:21 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:08:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:08:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:08:22 GMT
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
	-	`sha256:8d670b96a401a5cfb61ad27940492a2027ad1b61a1fa46000d705a1d8d159201`  
		Last Modified: Tue, 09 Jan 2024 22:51:10 GMT  
		Size: 66.3 MB (66302457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da6e3a038c3bd2afee0afab16ad35ea548d1966b1df80e55d9dcee9b280b371`  
		Last Modified: Tue, 09 Jan 2024 22:50:59 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08206a39be152f3861e70f6c3448542421f3249680b9274fd278f6015cc11aa5`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 5.1 MB (5116980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a1075ed747212d8e9506ed70d4cccab2b94dd685aa98e25a32f43575e21839`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 1.3 MB (1262390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76b6771ab88a9777236c173bb24bbc313a76da44e25c4c9ce07f8ff003338ee`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:ee4395a3f6f47c0262fc9b8b002b6f27c88ea7f60afa086af1976dbc4aac28b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `caddy:2.7.6-builder-windowsservercore-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull caddy@sha256:76e18d17fe903d45f1f88f9ba76237a5fdb8392b670b3d2b0b581a9a8a4067de
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2156673231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267688b3ce7bd013fc2b9407cba404926536c40d42366eedebe5680d607fa176`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 12 Dec 2023 23:38:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Dec 2023 23:38:53 GMT
ENV GIT_VERSION=2.23.0
# Tue, 12 Dec 2023 23:38:53 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 12 Dec 2023 23:38:54 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 12 Dec 2023 23:38:55 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 12 Dec 2023 23:40:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 12 Dec 2023 23:40:27 GMT
ENV GOPATH=C:\go
# Tue, 12 Dec 2023 23:41:35 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jan 2024 22:18:47 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:22:02 GMT
RUN $url = 'https://dl.google.com/go/go1.21.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27ac9dd6e66fb3fd0acfa6792ff053c86e7d2c055b022f4b5d53bfddec9e3301'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Jan 2024 22:22:04 GMT
WORKDIR C:\go
# Tue, 09 Jan 2024 23:00:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jan 2024 23:00:16 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:00:17 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:00:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:01:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 09 Jan 2024 23:01:37 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767e95390edb4050b2c57e1d564c9e4722c5ae776ebfb8907a539571a2609f7c`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c57683b4a629f3325c8517d99f497d4ffbcd0e70354e70a95d983a275bfe398`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95bef40c25d2abc3a12986675189e7152f6197fdc5a17343bdee3f0bc2e95a8`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043d50fbb4f0d8961fe3a95130f520d57cfe7e6e85b15cd4f9f14a01364f7ee`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55867ab446b5d5e34f9e6d414898b9a0b31051afc81b28ace1ce47e27d9e24ee`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10285db29cf842d22a49b00cb66fbbfe20e7d4e72a0d3e393d58824190f6835b`  
		Last Modified: Wed, 13 Dec 2023 00:04:19 GMT  
		Size: 25.6 MB (25558777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3037ad7a881ee540014f48a43aa3a857c479d9cefb413ce61a914c943901890b`  
		Last Modified: Wed, 13 Dec 2023 00:04:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788faab53b378465ec447dde1961338c1349487d1152856c0524e2f6a503ec70`  
		Last Modified: Wed, 13 Dec 2023 00:04:12 GMT  
		Size: 282.5 KB (282534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca23066a92625cdc8de9b99f08faf5c3e756534401f72ec8aff465b29c481ee`  
		Last Modified: Tue, 09 Jan 2024 22:39:56 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b92d2b727a3677f7df423fdb871102a4f49e8ab3c3f27447b46a8bb9d6315c5`  
		Last Modified: Tue, 09 Jan 2024 22:40:17 GMT  
		Size: 69.4 MB (69428911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c07e208b8230a3cf4f0d09d8d2e0964843388a9334a811e7537778242b4610`  
		Last Modified: Tue, 09 Jan 2024 22:39:56 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0002a397ba0f92a6b352156052f4a5f9bf5bd0b854e9e066dc85b8231b8d23`  
		Last Modified: Tue, 09 Jan 2024 23:03:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221d1a0d3e162f0c5064835e1683a547fb68ce0fe6ddbc15547e97547f4a815f`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9d6843b6bad3862684d5eade7e7816b48ce845effe90d8c1d5d5250151dd55`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173a315f398d136fd23d058d13fa18b082575f9732c3cc17a733570a15d53606`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e288abae7098c76d0379b4bb3808523310f24e5aa535a62ff1405875e5723c`  
		Last Modified: Tue, 09 Jan 2024 23:03:11 GMT  
		Size: 1.7 MB (1676147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5e67ad5abb1499f08dbb66b77e1f22ffafb79eeacef131b3863ce4f042fcf2`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:3d08e6c2e2cef96a5a8f6ddb7531801ad745003ddac2d632d9679e2c30f95e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2159; amd64

### `caddy:2.7.6-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2159; amd64

```console
$ docker pull caddy@sha256:b5c196359cb78d80f0c4bb97d3ffbf13a84eb3003c9f238f72cec005c9475105
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1986234916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3131c915e036b0f95ea6c698ffaf9974f6dbce70dc8d2cd1600175d4155dde16`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Tue, 12 Dec 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Dec 2023 23:35:08 GMT
ENV GIT_VERSION=2.23.0
# Tue, 12 Dec 2023 23:35:08 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 12 Dec 2023 23:35:09 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 12 Dec 2023 23:35:10 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 12 Dec 2023 23:35:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 12 Dec 2023 23:35:47 GMT
ENV GOPATH=C:\go
# Tue, 12 Dec 2023 23:36:11 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jan 2024 22:16:03 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:18:27 GMT
RUN $url = 'https://dl.google.com/go/go1.21.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27ac9dd6e66fb3fd0acfa6792ff053c86e7d2c055b022f4b5d53bfddec9e3301'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Jan 2024 22:18:28 GMT
WORKDIR C:\go
# Tue, 09 Jan 2024 23:02:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jan 2024 23:02:03 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:02:04 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:02:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:02:30 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 09 Jan 2024 23:02:31 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d0c853ded9068434b9128a8016b3ae5e18f748f62801c7bb6e6092495300ec`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf365c1e9d59a58fc8cee2522db9139b36cf02ecabe7302489a9a3667b62cea`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69dbeb610a3fa1c3f2962202c58796ff120ea20cc3ba1f2fce807cbbe2c37ab0`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a3be8233329999132fa6e504f39c44abd589439a96846e31508037334d6d11`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755721e8166183821011ca0acdb563f67887cfe33da36997710b182f049fbede`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4700bd9f606505ec47d78dc66a509ca78ea2a8269a8e2b9bcf28ec33c5cbea74`  
		Last Modified: Wed, 13 Dec 2023 00:02:42 GMT  
		Size: 25.6 MB (25554973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777ab971ccee32e15de39ed82eceeb004d2d6f94af7c43ab3d6cfc1baf0abd07`  
		Last Modified: Wed, 13 Dec 2023 00:02:35 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958aa1458398ceb3a543d13279579cc48507080df3b269a5aa1a09da23b03ccf`  
		Last Modified: Wed, 13 Dec 2023 00:02:35 GMT  
		Size: 284.9 KB (284874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ed7a59b16104881efb9e3ac02b81f631cff124b04d7494d955a2c697b7c4ce`  
		Last Modified: Tue, 09 Jan 2024 22:39:21 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b1d528d83cdc1c6fb3f551b955643ffa64d14478df3d1b2aa1faf3cf95d454`  
		Last Modified: Tue, 09 Jan 2024 22:39:41 GMT  
		Size: 69.4 MB (69432029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8730c2425648e897784c3ff628a5fd72bb913811c924412142d22ce7f7d36c`  
		Last Modified: Tue, 09 Jan 2024 22:39:21 GMT  
		Size: 1.5 KB (1539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea60c3b2caff00ee0011a9148cabb96e3a1cde3a81a8ee5b7ca60f5513aff78`  
		Last Modified: Tue, 09 Jan 2024 23:03:30 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f939916b2a0c9fde832abafdf561e4515fc15d11979c5fa3e0bf8165cb4b3a`  
		Last Modified: Tue, 09 Jan 2024 23:03:28 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12cb1ee578e943a57f3c817517ac6b636e4d08c82aaacf57d4002b9732d98b0`  
		Last Modified: Tue, 09 Jan 2024 23:03:27 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c98bc1e6119b0ada6f9e06e3c88634debef4de96ad9906ac1d7065774a50a4f`  
		Last Modified: Tue, 09 Jan 2024 23:03:28 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc678bb3572a4a425d6d29f6ab5a6cbb6fb1e1cf427c0ed3982f9e451901c69`  
		Last Modified: Tue, 09 Jan 2024 23:03:28 GMT  
		Size: 1.7 MB (1671314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8151c697df9e9b88184cda0002778dff9d013f6ebd7c46924622bcb222243585`  
		Last Modified: Tue, 09 Jan 2024 23:03:27 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-windowsservercore`

```console
$ docker pull caddy@sha256:972db88b238031234d870fded48029f384e208fa23012db80dd8de6adc65d559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.5206; amd64
	-	windows version 10.0.20348.2159; amd64

### `caddy:2.7.6-windowsservercore` - windows version 10.0.17763.5206; amd64

```console
$ docker pull caddy@sha256:23906c96e8647871d54638ee95201b15a6780bd5c5a55e1910f1cce47f51327a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075748892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd668c1e74ca31419de6a4894168996b6be13d2cfb6dda297f76f1f0e82af65`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 12 Dec 2023 23:38:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 02:30:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Dec 2023 02:30:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Dec 2023 02:32:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Dec 2023 02:32:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Dec 2023 02:32:03 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Dec 2023 02:32:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Dec 2023 02:32:05 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Dec 2023 02:32:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Dec 2023 02:32:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Dec 2023 02:32:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Dec 2023 02:32:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Dec 2023 02:32:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Dec 2023 02:32:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Dec 2023 02:32:11 GMT
EXPOSE 80
# Wed, 13 Dec 2023 02:32:12 GMT
EXPOSE 443
# Wed, 13 Dec 2023 02:32:13 GMT
EXPOSE 443/udp
# Wed, 13 Dec 2023 02:32:13 GMT
EXPOSE 2019
# Wed, 13 Dec 2023 02:33:19 GMT
RUN caddy version
# Wed, 13 Dec 2023 02:33:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767e95390edb4050b2c57e1d564c9e4722c5ae776ebfb8907a539571a2609f7c`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc953d49171296238d791f543a2a026383540af60c9b10cc72446745ea9e517`  
		Last Modified: Wed, 13 Dec 2023 02:38:55 GMT  
		Size: 466.4 KB (466376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5091a1fcf41a799b6b5325321d36e20072d566027eeecc072788a9a3c3afbf0b`  
		Last Modified: Wed, 13 Dec 2023 02:38:54 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d0c21ea3d396314641058b6087c719f00acf6e81a122d0308c76705b454c5a`  
		Last Modified: Wed, 13 Dec 2023 02:38:58 GMT  
		Size: 15.3 MB (15282292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7c1ffefa6eaf8ceb9b6964a75043f3440c260e5ef8a7757a4902bbd87b5a11`  
		Last Modified: Wed, 13 Dec 2023 02:38:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209a9db6a8a0e20f16c07fa90f84ff5f0fbcf8896b719c5282405503804e4975`  
		Last Modified: Wed, 13 Dec 2023 02:38:53 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e6508c4f7300255ca275dc9fa4b8ff9f4e4ff4e6c552afee4d03305e571f8`  
		Last Modified: Wed, 13 Dec 2023 02:38:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571a096f7d34249fda9c90244912f35e632dc8c3c50a830c1d3dc6d5d2234264`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee679db41077812368c0ee8780348a81cc00878e2848106d2b022cfa25222615`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61da3eb55b53d10c6d39556e06adcd87b1e813dbf6e7c0c09a4a1fcd3c1a02af`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67d27f68c7ff3cf8ec13fd0ae72ac89b781c819f1959e16c22101faa49884a1`  
		Last Modified: Wed, 13 Dec 2023 02:38:51 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b0c532fc98f8438a57e314863455c2812c5f8273718a387893d58b1eae45a7`  
		Last Modified: Wed, 13 Dec 2023 02:38:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb76494edec3148a22e8826aa2cceb75046d74559b7fe31713da82a5504d187`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621db1494746176522163d644f8f6d572003928346b37dfea1118539767375bf`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e621e03d954adf248bd9ddcdfe28108be9204a2f010bc44cd49534bc26d10c`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb96c188ceb57176f56af8649f49ebde260394730cc2ee6bd5a10634d6676bc`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e2237c5f2e48a944f2cdc493acec61ca707749a0d33362f62a1162e6967f7f`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b904a8ec5a95b1df9b634285424830763de3a36377f8f97be9383346cd82022`  
		Last Modified: Wed, 13 Dec 2023 02:38:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ae7bbabfc6a290ea47a42a976c34545f19465895a8dee1bd94b9f6351d9ae`  
		Last Modified: Wed, 13 Dec 2023 02:38:49 GMT  
		Size: 269.0 KB (268985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4235be6cdbcf40a5350abf8550ae54349cd6889349bacb2c4c6fcdabb02fcb`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-windowsservercore` - windows version 10.0.20348.2159; amd64

```console
$ docker pull caddy@sha256:8b2e9ac9b72c8b2c90bc15116cedbb8044d599e4f86ffcbb48cebdfdf97d19f7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1905326657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7092fad7c71072036e6f6e418de96b9a293b2a5fa6c1f533192cee80981c2fdf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Tue, 12 Dec 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 02:33:55 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Dec 2023 02:33:56 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Dec 2023 02:35:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Dec 2023 02:35:11 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Dec 2023 02:35:12 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Dec 2023 02:35:12 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Dec 2023 02:35:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Dec 2023 02:35:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Dec 2023 02:35:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Dec 2023 02:35:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Dec 2023 02:35:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Dec 2023 02:35:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Dec 2023 02:35:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Dec 2023 02:35:19 GMT
EXPOSE 80
# Wed, 13 Dec 2023 02:35:20 GMT
EXPOSE 443
# Wed, 13 Dec 2023 02:35:21 GMT
EXPOSE 443/udp
# Wed, 13 Dec 2023 02:35:23 GMT
EXPOSE 2019
# Wed, 13 Dec 2023 02:35:42 GMT
RUN caddy version
# Wed, 13 Dec 2023 02:35:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d0c853ded9068434b9128a8016b3ae5e18f748f62801c7bb6e6092495300ec`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d3c17fb1ca1499edf5a0a7fe2ed357de61bc5478580af8c193d8c59e8139`  
		Last Modified: Wed, 13 Dec 2023 02:39:22 GMT  
		Size: 468.6 KB (468557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0205b9bfc982e2d76e931acf88ef85dfe1c943d4412d8e0abc82f7f0837e3ffe`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be685bdfb2389b99d51da84fb605d5905240fb7fbb82779d90949871c42c3a01`  
		Last Modified: Wed, 13 Dec 2023 02:39:24 GMT  
		Size: 15.3 MB (15270636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9935999a24844b91a4364fda0be1e1ffa280fb0c3c3c51157ffee05dc396bc2`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bd056752e2fad4d5b1e26bda93daeb2e2b89b03fc440f547e8e8e57b56ec54`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bff69c07007af0ff21680f637729be4b8d66a9b114305a47b54b631e499932`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8602ee7f30c15eb312beb9be91c2987f09264a3ec61fab2a25f7388c80361e65`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d98bd6b64e0a8382fcdef83a12bb138867f39b06a481c87d92f5e8b6bd637db`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab994312751dbeec291009c1153b38cf3621f929570200eefc6f838922099b`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb56c650abb1c98df5455b6b8c1864695f45548b82de29e570ce3f46299e574d`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b69a6fa036380dd82a0f067f8e97178a8da04f68a9c4a9eb4c10f5c432c7ad`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148841d4329f6dd8e152b2fc00676a9c4becd06e9c761400458c7b2d46438314`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8f8b0320cdf29c8f5349e14ec28542bd3c57d39b3d69d580de8ec462540d01`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b20c979eb5abf12332bf27e4b1aa8d06c7b7d6253b88d67681f13191b2ed1f5`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48a3dce4dbfd8b7dec08593b9d5c29404f49689161151ee3dda24b973f91dbe`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbc07c2849a4af7257c854c4fbd200cea57e1d10b82012dfcbe9a675b6fdcc0`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6842cf61f849c09c274f395d1e08b1196c674d9a59c34ddc4a9eb69e190b9d`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6823cd563e14b3750718450028cc7815abe14745863b57adc3e7524f3cdbfcb`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 290.0 KB (289982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae3d36b08abac2ea5a039a22621cc239126e2c32070f73be4efaacfc3c81c91`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-windowsservercore-1809`

```console
$ docker pull caddy@sha256:7c8910562b78f49c3a2f608132f963d70e34352d7b1eba277e11d71c4aadd90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `caddy:2.7.6-windowsservercore-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull caddy@sha256:23906c96e8647871d54638ee95201b15a6780bd5c5a55e1910f1cce47f51327a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075748892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd668c1e74ca31419de6a4894168996b6be13d2cfb6dda297f76f1f0e82af65`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 12 Dec 2023 23:38:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 02:30:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Dec 2023 02:30:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Dec 2023 02:32:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Dec 2023 02:32:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Dec 2023 02:32:03 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Dec 2023 02:32:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Dec 2023 02:32:05 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Dec 2023 02:32:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Dec 2023 02:32:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Dec 2023 02:32:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Dec 2023 02:32:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Dec 2023 02:32:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Dec 2023 02:32:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Dec 2023 02:32:11 GMT
EXPOSE 80
# Wed, 13 Dec 2023 02:32:12 GMT
EXPOSE 443
# Wed, 13 Dec 2023 02:32:13 GMT
EXPOSE 443/udp
# Wed, 13 Dec 2023 02:32:13 GMT
EXPOSE 2019
# Wed, 13 Dec 2023 02:33:19 GMT
RUN caddy version
# Wed, 13 Dec 2023 02:33:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767e95390edb4050b2c57e1d564c9e4722c5ae776ebfb8907a539571a2609f7c`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc953d49171296238d791f543a2a026383540af60c9b10cc72446745ea9e517`  
		Last Modified: Wed, 13 Dec 2023 02:38:55 GMT  
		Size: 466.4 KB (466376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5091a1fcf41a799b6b5325321d36e20072d566027eeecc072788a9a3c3afbf0b`  
		Last Modified: Wed, 13 Dec 2023 02:38:54 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d0c21ea3d396314641058b6087c719f00acf6e81a122d0308c76705b454c5a`  
		Last Modified: Wed, 13 Dec 2023 02:38:58 GMT  
		Size: 15.3 MB (15282292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7c1ffefa6eaf8ceb9b6964a75043f3440c260e5ef8a7757a4902bbd87b5a11`  
		Last Modified: Wed, 13 Dec 2023 02:38:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209a9db6a8a0e20f16c07fa90f84ff5f0fbcf8896b719c5282405503804e4975`  
		Last Modified: Wed, 13 Dec 2023 02:38:53 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e6508c4f7300255ca275dc9fa4b8ff9f4e4ff4e6c552afee4d03305e571f8`  
		Last Modified: Wed, 13 Dec 2023 02:38:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571a096f7d34249fda9c90244912f35e632dc8c3c50a830c1d3dc6d5d2234264`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee679db41077812368c0ee8780348a81cc00878e2848106d2b022cfa25222615`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61da3eb55b53d10c6d39556e06adcd87b1e813dbf6e7c0c09a4a1fcd3c1a02af`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67d27f68c7ff3cf8ec13fd0ae72ac89b781c819f1959e16c22101faa49884a1`  
		Last Modified: Wed, 13 Dec 2023 02:38:51 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b0c532fc98f8438a57e314863455c2812c5f8273718a387893d58b1eae45a7`  
		Last Modified: Wed, 13 Dec 2023 02:38:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb76494edec3148a22e8826aa2cceb75046d74559b7fe31713da82a5504d187`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621db1494746176522163d644f8f6d572003928346b37dfea1118539767375bf`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e621e03d954adf248bd9ddcdfe28108be9204a2f010bc44cd49534bc26d10c`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb96c188ceb57176f56af8649f49ebde260394730cc2ee6bd5a10634d6676bc`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e2237c5f2e48a944f2cdc493acec61ca707749a0d33362f62a1162e6967f7f`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b904a8ec5a95b1df9b634285424830763de3a36377f8f97be9383346cd82022`  
		Last Modified: Wed, 13 Dec 2023 02:38:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ae7bbabfc6a290ea47a42a976c34545f19465895a8dee1bd94b9f6351d9ae`  
		Last Modified: Wed, 13 Dec 2023 02:38:49 GMT  
		Size: 269.0 KB (268985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4235be6cdbcf40a5350abf8550ae54349cd6889349bacb2c4c6fcdabb02fcb`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:05ced206e45b045bc5cd525d92a16ed5dc3db97b7917edef04152739d06b712b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2159; amd64

### `caddy:2.7.6-windowsservercore-ltsc2022` - windows version 10.0.20348.2159; amd64

```console
$ docker pull caddy@sha256:8b2e9ac9b72c8b2c90bc15116cedbb8044d599e4f86ffcbb48cebdfdf97d19f7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1905326657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7092fad7c71072036e6f6e418de96b9a293b2a5fa6c1f533192cee80981c2fdf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Tue, 12 Dec 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 02:33:55 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Dec 2023 02:33:56 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Dec 2023 02:35:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Dec 2023 02:35:11 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Dec 2023 02:35:12 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Dec 2023 02:35:12 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Dec 2023 02:35:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Dec 2023 02:35:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Dec 2023 02:35:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Dec 2023 02:35:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Dec 2023 02:35:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Dec 2023 02:35:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Dec 2023 02:35:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Dec 2023 02:35:19 GMT
EXPOSE 80
# Wed, 13 Dec 2023 02:35:20 GMT
EXPOSE 443
# Wed, 13 Dec 2023 02:35:21 GMT
EXPOSE 443/udp
# Wed, 13 Dec 2023 02:35:23 GMT
EXPOSE 2019
# Wed, 13 Dec 2023 02:35:42 GMT
RUN caddy version
# Wed, 13 Dec 2023 02:35:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d0c853ded9068434b9128a8016b3ae5e18f748f62801c7bb6e6092495300ec`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d3c17fb1ca1499edf5a0a7fe2ed357de61bc5478580af8c193d8c59e8139`  
		Last Modified: Wed, 13 Dec 2023 02:39:22 GMT  
		Size: 468.6 KB (468557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0205b9bfc982e2d76e931acf88ef85dfe1c943d4412d8e0abc82f7f0837e3ffe`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be685bdfb2389b99d51da84fb605d5905240fb7fbb82779d90949871c42c3a01`  
		Last Modified: Wed, 13 Dec 2023 02:39:24 GMT  
		Size: 15.3 MB (15270636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9935999a24844b91a4364fda0be1e1ffa280fb0c3c3c51157ffee05dc396bc2`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bd056752e2fad4d5b1e26bda93daeb2e2b89b03fc440f547e8e8e57b56ec54`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bff69c07007af0ff21680f637729be4b8d66a9b114305a47b54b631e499932`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8602ee7f30c15eb312beb9be91c2987f09264a3ec61fab2a25f7388c80361e65`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d98bd6b64e0a8382fcdef83a12bb138867f39b06a481c87d92f5e8b6bd637db`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab994312751dbeec291009c1153b38cf3621f929570200eefc6f838922099b`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb56c650abb1c98df5455b6b8c1864695f45548b82de29e570ce3f46299e574d`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b69a6fa036380dd82a0f067f8e97178a8da04f68a9c4a9eb4c10f5c432c7ad`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148841d4329f6dd8e152b2fc00676a9c4becd06e9c761400458c7b2d46438314`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8f8b0320cdf29c8f5349e14ec28542bd3c57d39b3d69d580de8ec462540d01`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b20c979eb5abf12332bf27e4b1aa8d06c7b7d6253b88d67681f13191b2ed1f5`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48a3dce4dbfd8b7dec08593b9d5c29404f49689161151ee3dda24b973f91dbe`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbc07c2849a4af7257c854c4fbd200cea57e1d10b82012dfcbe9a675b6fdcc0`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6842cf61f849c09c274f395d1e08b1196c674d9a59c34ddc4a9eb69e190b9d`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6823cd563e14b3750718450028cc7815abe14745863b57adc3e7524f3cdbfcb`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 290.0 KB (289982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae3d36b08abac2ea5a039a22621cc239126e2c32070f73be4efaacfc3c81c91`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1422 bytes)  
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
$ docker pull caddy@sha256:e4e6def23b2b2ddd4fc962e9e8871d2e1049909f09428e7d3455f3e9fe937126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5206; amd64
	-	windows version 10.0.20348.2159; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:40fb52ba04a15d7b79c65ccf594655c93ef84951d4b5f3636dd741c6f7117c82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77049039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec8a77457f35f87a6c0e163b4b9ca06831e9597838815cdfafd6924007b2053`
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
# Tue, 09 Jan 2024 22:20:46 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:20:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:20:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:20:57 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:20:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:20:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:20:58 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:13:01 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:13:01 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:13:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:13:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:13:03 GMT
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
	-	`sha256:2786abec99e189a4a116c45771654dd1220a5a78deb32430974d369c08fa4bd0`  
		Last Modified: Tue, 09 Jan 2024 22:27:13 GMT  
		Size: 67.1 MB (67086665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ece744550870593fb66b630e5fa62ae11cf9c89547275dd4450952b0fc9460`  
		Last Modified: Tue, 09 Jan 2024 22:27:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3a3a5ccc6f4610e4fd60832b6c63eed6366cfe0b0f37e3e6125f54aef9f135`  
		Last Modified: Tue, 09 Jan 2024 23:13:20 GMT  
		Size: 5.0 MB (4972463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe0d8e469393bc3c86e3dc711c99a557728a8c0e8a67a85f65d7fdc195034cd`  
		Last Modified: Tue, 09 Jan 2024 23:13:19 GMT  
		Size: 1.3 MB (1302233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761ef04b7c1f8fcec7e6f8b1f4995bdf8f34100b19140a0faef407b758829e8d`  
		Last Modified: Tue, 09 Jan 2024 23:13:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:83a8b023f6fa4c601dca30abe334e1243463e92f8e84e33dac925e8d6f7a601f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75411881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a0ab3fe89b994d3ff35471a8b1709d10e3ca724eb9a2e14bac7221211877bb`
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
# Wed, 20 Dec 2023 21:34:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Wed, 20 Dec 2023 21:34:12 GMT
ENV GOTOOLCHAIN=local
# Wed, 20 Dec 2023 21:34:12 GMT
ENV GOPATH=/go
# Wed, 20 Dec 2023 21:34:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 21:34:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 20 Dec 2023 21:34:13 GMT
WORKDIR /go
# Wed, 20 Dec 2023 21:51:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 20 Dec 2023 21:51:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_SETCAP=1
# Wed, 20 Dec 2023 21:51:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 20 Dec 2023 21:51:43 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 20 Dec 2023 21:51:43 GMT
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
	-	`sha256:29bee9d75e3ae91d44ddf09cf0fa198b556654c8073aa50d8b630e52a5d203be`  
		Last Modified: Wed, 20 Dec 2023 21:36:17 GMT  
		Size: 65.8 MB (65764273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a485eddce12cbac59d4532427a2f3bc7f475a18f1b6ddc05d3631682cde4be3e`  
		Last Modified: Wed, 20 Dec 2023 21:36:00 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460d4992c24f213c1a4f97d850c33f2a32be4f0763f60ae881dfb36929edbeb8`  
		Last Modified: Wed, 20 Dec 2023 21:52:07 GMT  
		Size: 5.0 MB (4966637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf270d0f9df22c9f4d54cc419be9b59b79eec2ef2f2c70fa2545347b5db6a1de`  
		Last Modified: Wed, 20 Dec 2023 21:52:07 GMT  
		Size: 1.2 MB (1248658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29559d6667b029d9d030a6d020a049a1c7df7a5d84b925b75e0b37d63be04d25`  
		Last Modified: Wed, 20 Dec 2023 21:52:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:286339d083a589ff4ee17f2a98eabb1011f13f93e40c79bba2af0748f9bf2c8c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74795731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08540a67a8309258e1b934ca527574a28d9cd09a153f09e55635d67a11e5572d`
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
# Tue, 09 Jan 2024 22:59:02 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:59:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:59:24 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:59:24 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:59:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:59:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:59:27 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:59:28 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:59:29 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:59:29 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:59:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:59:30 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:59:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:59:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:59:33 GMT
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
	-	`sha256:f975e362e12b206661ef3e8661f8ddef5b3886db6695858a6ee13107cfb406cd`  
		Last Modified: Tue, 09 Jan 2024 23:10:25 GMT  
		Size: 65.8 MB (65849716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d88a6cd0c6e987e9c7854e8091bc0d3da0f5215dc272d31db2a10463a597eb`  
		Last Modified: Tue, 09 Jan 2024 23:10:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ccd85286302c0f7692dc9bf9e673cc831252fa3892db98d4a388f8e3a40229`  
		Last Modified: Tue, 09 Jan 2024 23:59:54 GMT  
		Size: 4.5 MB (4514276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c77c0eb7e54b1d25489fbedb6607137e9123f25be63514940cec48f5afbcbb`  
		Last Modified: Tue, 09 Jan 2024 23:59:53 GMT  
		Size: 1.2 MB (1246091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe6c53215469f1e0efd2612e28e7bc3d644b7460fdac4ed2217adcfcbb01ff`  
		Last Modified: Tue, 09 Jan 2024 23:59:53 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:29c1d8e221c7025b5fa2bd564d67b2cbe54abf6ed141469ee753714d4b86de8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74062596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751a7ab9b4f36aa69472a02e61896bae0e9f5d4d8751e6a7791c550f914532f6`
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
# Tue, 09 Jan 2024 22:40:13 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:40:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:40:23 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:40:23 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:40:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:40:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:40:24 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:34:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:34:50 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:34:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:34:51 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:34:51 GMT
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
	-	`sha256:f784b2816c0487ec6a1efb9635a001a738ce6794c6f60cef8dd8fc658663da9f`  
		Last Modified: Tue, 09 Jan 2024 22:45:17 GMT  
		Size: 64.2 MB (64173642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2878d57b8185e91fa6aee756ccda964266f809fac11f9dce2ed4fbfd8912f1a9`  
		Last Modified: Tue, 09 Jan 2024 22:45:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab371eb8298e2716c51ac9c58092131a438b00268b67ae458e1ace0ff2b0b5a`  
		Last Modified: Tue, 09 Jan 2024 23:35:05 GMT  
		Size: 5.1 MB (5070606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797b9a67275bffa5caa99271d04d6986b812b4aa84192f9ba3f1ff7b1dfed362`  
		Last Modified: Tue, 09 Jan 2024 23:35:05 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13428147a58f4a789fd5d1f01d54bef643a726131dd40b35c267f16843158a6c`  
		Last Modified: Tue, 09 Jan 2024 23:35:04 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:745364722abfeb88309b8c87aaea59721a3b9ce6770ef2ece3727cd89c4ecdb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74295245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ca8de75928fb38f0a93327b23d822645315bee4c8d32dbc96b28ffbf4f513b`
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
# Tue, 09 Jan 2024 22:18:29 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:18:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:18:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:18:54 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:18:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:18:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:18:58 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:31:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:31:34 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:31:34 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:31:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:31:36 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:31:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:31:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:31:39 GMT
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
	-	`sha256:08676902305ce1488e47f2c6cf37c156f8adf34592d23cb6c0adda7f8e20bbec`  
		Last Modified: Tue, 09 Jan 2024 22:27:11 GMT  
		Size: 64.2 MB (64202869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007761f68f098a06788d8a4f5b63c5c25fa52e8f613da754d12a9c8005b2ad44`  
		Last Modified: Tue, 09 Jan 2024 22:26:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28beac3397f3e144b5cbb889b20e5c6450f5a635fd5679a9ddb77b34420a9512`  
		Last Modified: Tue, 09 Jan 2024 23:31:57 GMT  
		Size: 5.3 MB (5270658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee35c838a10edf1f76e27c99108010f65e1cb2d9cbad31ebe0480cdcc17a15d`  
		Last Modified: Tue, 09 Jan 2024 23:31:56 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce2a624f1055a6b34babd0b44d093aa23653397f4289c89018b0396bebcf038`  
		Last Modified: Tue, 09 Jan 2024 23:31:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:9eb20c4013227f7a3b0435a6f5346ec30763958b3f54f7ad0e7a02a7dd369f5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76184930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c9ebcb7eda5bc7753c6ac25b3a1ea2cbdce628c002973e9ad47ffb0d3ba97e`
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
# Tue, 09 Jan 2024 22:43:43 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:43:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:44:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:44:00 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:44:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:44:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:44:01 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:08:20 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:08:21 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:08:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:08:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:08:22 GMT
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
	-	`sha256:8d670b96a401a5cfb61ad27940492a2027ad1b61a1fa46000d705a1d8d159201`  
		Last Modified: Tue, 09 Jan 2024 22:51:10 GMT  
		Size: 66.3 MB (66302457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da6e3a038c3bd2afee0afab16ad35ea548d1966b1df80e55d9dcee9b280b371`  
		Last Modified: Tue, 09 Jan 2024 22:50:59 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08206a39be152f3861e70f6c3448542421f3249680b9274fd278f6015cc11aa5`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 5.1 MB (5116980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a1075ed747212d8e9506ed70d4cccab2b94dd685aa98e25a32f43575e21839`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 1.3 MB (1262390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76b6771ab88a9777236c173bb24bbc313a76da44e25c4c9ce07f8ff003338ee`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.5206; amd64

```console
$ docker pull caddy@sha256:76e18d17fe903d45f1f88f9ba76237a5fdb8392b670b3d2b0b581a9a8a4067de
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2156673231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267688b3ce7bd013fc2b9407cba404926536c40d42366eedebe5680d607fa176`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 12 Dec 2023 23:38:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Dec 2023 23:38:53 GMT
ENV GIT_VERSION=2.23.0
# Tue, 12 Dec 2023 23:38:53 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 12 Dec 2023 23:38:54 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 12 Dec 2023 23:38:55 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 12 Dec 2023 23:40:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 12 Dec 2023 23:40:27 GMT
ENV GOPATH=C:\go
# Tue, 12 Dec 2023 23:41:35 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jan 2024 22:18:47 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:22:02 GMT
RUN $url = 'https://dl.google.com/go/go1.21.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27ac9dd6e66fb3fd0acfa6792ff053c86e7d2c055b022f4b5d53bfddec9e3301'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Jan 2024 22:22:04 GMT
WORKDIR C:\go
# Tue, 09 Jan 2024 23:00:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jan 2024 23:00:16 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:00:17 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:00:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:01:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 09 Jan 2024 23:01:37 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767e95390edb4050b2c57e1d564c9e4722c5ae776ebfb8907a539571a2609f7c`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c57683b4a629f3325c8517d99f497d4ffbcd0e70354e70a95d983a275bfe398`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95bef40c25d2abc3a12986675189e7152f6197fdc5a17343bdee3f0bc2e95a8`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043d50fbb4f0d8961fe3a95130f520d57cfe7e6e85b15cd4f9f14a01364f7ee`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55867ab446b5d5e34f9e6d414898b9a0b31051afc81b28ace1ce47e27d9e24ee`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10285db29cf842d22a49b00cb66fbbfe20e7d4e72a0d3e393d58824190f6835b`  
		Last Modified: Wed, 13 Dec 2023 00:04:19 GMT  
		Size: 25.6 MB (25558777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3037ad7a881ee540014f48a43aa3a857c479d9cefb413ce61a914c943901890b`  
		Last Modified: Wed, 13 Dec 2023 00:04:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788faab53b378465ec447dde1961338c1349487d1152856c0524e2f6a503ec70`  
		Last Modified: Wed, 13 Dec 2023 00:04:12 GMT  
		Size: 282.5 KB (282534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca23066a92625cdc8de9b99f08faf5c3e756534401f72ec8aff465b29c481ee`  
		Last Modified: Tue, 09 Jan 2024 22:39:56 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b92d2b727a3677f7df423fdb871102a4f49e8ab3c3f27447b46a8bb9d6315c5`  
		Last Modified: Tue, 09 Jan 2024 22:40:17 GMT  
		Size: 69.4 MB (69428911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c07e208b8230a3cf4f0d09d8d2e0964843388a9334a811e7537778242b4610`  
		Last Modified: Tue, 09 Jan 2024 22:39:56 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0002a397ba0f92a6b352156052f4a5f9bf5bd0b854e9e066dc85b8231b8d23`  
		Last Modified: Tue, 09 Jan 2024 23:03:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221d1a0d3e162f0c5064835e1683a547fb68ce0fe6ddbc15547e97547f4a815f`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9d6843b6bad3862684d5eade7e7816b48ce845effe90d8c1d5d5250151dd55`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173a315f398d136fd23d058d13fa18b082575f9732c3cc17a733570a15d53606`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e288abae7098c76d0379b4bb3808523310f24e5aa535a62ff1405875e5723c`  
		Last Modified: Tue, 09 Jan 2024 23:03:11 GMT  
		Size: 1.7 MB (1676147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5e67ad5abb1499f08dbb66b77e1f22ffafb79eeacef131b3863ce4f042fcf2`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.20348.2159; amd64

```console
$ docker pull caddy@sha256:b5c196359cb78d80f0c4bb97d3ffbf13a84eb3003c9f238f72cec005c9475105
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1986234916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3131c915e036b0f95ea6c698ffaf9974f6dbce70dc8d2cd1600175d4155dde16`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Tue, 12 Dec 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Dec 2023 23:35:08 GMT
ENV GIT_VERSION=2.23.0
# Tue, 12 Dec 2023 23:35:08 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 12 Dec 2023 23:35:09 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 12 Dec 2023 23:35:10 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 12 Dec 2023 23:35:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 12 Dec 2023 23:35:47 GMT
ENV GOPATH=C:\go
# Tue, 12 Dec 2023 23:36:11 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jan 2024 22:16:03 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:18:27 GMT
RUN $url = 'https://dl.google.com/go/go1.21.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27ac9dd6e66fb3fd0acfa6792ff053c86e7d2c055b022f4b5d53bfddec9e3301'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Jan 2024 22:18:28 GMT
WORKDIR C:\go
# Tue, 09 Jan 2024 23:02:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jan 2024 23:02:03 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:02:04 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:02:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:02:30 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 09 Jan 2024 23:02:31 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d0c853ded9068434b9128a8016b3ae5e18f748f62801c7bb6e6092495300ec`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf365c1e9d59a58fc8cee2522db9139b36cf02ecabe7302489a9a3667b62cea`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69dbeb610a3fa1c3f2962202c58796ff120ea20cc3ba1f2fce807cbbe2c37ab0`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a3be8233329999132fa6e504f39c44abd589439a96846e31508037334d6d11`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755721e8166183821011ca0acdb563f67887cfe33da36997710b182f049fbede`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4700bd9f606505ec47d78dc66a509ca78ea2a8269a8e2b9bcf28ec33c5cbea74`  
		Last Modified: Wed, 13 Dec 2023 00:02:42 GMT  
		Size: 25.6 MB (25554973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777ab971ccee32e15de39ed82eceeb004d2d6f94af7c43ab3d6cfc1baf0abd07`  
		Last Modified: Wed, 13 Dec 2023 00:02:35 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958aa1458398ceb3a543d13279579cc48507080df3b269a5aa1a09da23b03ccf`  
		Last Modified: Wed, 13 Dec 2023 00:02:35 GMT  
		Size: 284.9 KB (284874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ed7a59b16104881efb9e3ac02b81f631cff124b04d7494d955a2c697b7c4ce`  
		Last Modified: Tue, 09 Jan 2024 22:39:21 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b1d528d83cdc1c6fb3f551b955643ffa64d14478df3d1b2aa1faf3cf95d454`  
		Last Modified: Tue, 09 Jan 2024 22:39:41 GMT  
		Size: 69.4 MB (69432029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8730c2425648e897784c3ff628a5fd72bb913811c924412142d22ce7f7d36c`  
		Last Modified: Tue, 09 Jan 2024 22:39:21 GMT  
		Size: 1.5 KB (1539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea60c3b2caff00ee0011a9148cabb96e3a1cde3a81a8ee5b7ca60f5513aff78`  
		Last Modified: Tue, 09 Jan 2024 23:03:30 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f939916b2a0c9fde832abafdf561e4515fc15d11979c5fa3e0bf8165cb4b3a`  
		Last Modified: Tue, 09 Jan 2024 23:03:28 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12cb1ee578e943a57f3c817517ac6b636e4d08c82aaacf57d4002b9732d98b0`  
		Last Modified: Tue, 09 Jan 2024 23:03:27 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c98bc1e6119b0ada6f9e06e3c88634debef4de96ad9906ac1d7065774a50a4f`  
		Last Modified: Tue, 09 Jan 2024 23:03:28 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc678bb3572a4a425d6d29f6ab5a6cbb6fb1e1cf427c0ed3982f9e451901c69`  
		Last Modified: Tue, 09 Jan 2024 23:03:28 GMT  
		Size: 1.7 MB (1671314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8151c697df9e9b88184cda0002778dff9d013f6ebd7c46924622bcb222243585`  
		Last Modified: Tue, 09 Jan 2024 23:03:27 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:88ea79d5d4c27d14e88147a8ee7880afdd51b939d2fc2b455146a10fbc326986
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
$ docker pull caddy@sha256:40fb52ba04a15d7b79c65ccf594655c93ef84951d4b5f3636dd741c6f7117c82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77049039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec8a77457f35f87a6c0e163b4b9ca06831e9597838815cdfafd6924007b2053`
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
# Tue, 09 Jan 2024 22:20:46 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:20:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:20:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:20:57 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:20:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:20:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:20:58 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:13:01 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:13:01 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:13:01 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:13:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:13:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:13:03 GMT
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
	-	`sha256:2786abec99e189a4a116c45771654dd1220a5a78deb32430974d369c08fa4bd0`  
		Last Modified: Tue, 09 Jan 2024 22:27:13 GMT  
		Size: 67.1 MB (67086665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ece744550870593fb66b630e5fa62ae11cf9c89547275dd4450952b0fc9460`  
		Last Modified: Tue, 09 Jan 2024 22:27:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3a3a5ccc6f4610e4fd60832b6c63eed6366cfe0b0f37e3e6125f54aef9f135`  
		Last Modified: Tue, 09 Jan 2024 23:13:20 GMT  
		Size: 5.0 MB (4972463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe0d8e469393bc3c86e3dc711c99a557728a8c0e8a67a85f65d7fdc195034cd`  
		Last Modified: Tue, 09 Jan 2024 23:13:19 GMT  
		Size: 1.3 MB (1302233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761ef04b7c1f8fcec7e6f8b1f4995bdf8f34100b19140a0faef407b758829e8d`  
		Last Modified: Tue, 09 Jan 2024 23:13:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:83a8b023f6fa4c601dca30abe334e1243463e92f8e84e33dac925e8d6f7a601f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75411881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a0ab3fe89b994d3ff35471a8b1709d10e3ca724eb9a2e14bac7221211877bb`
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
# Wed, 20 Dec 2023 21:34:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.5.linux-amd64.tar.gz'; 			sha256='e2bc0b3e4b64111ec117295c088bde5f00eeed1567999ff77bc859d7df70078e'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.5.linux-armv6l.tar.gz'; 			sha256='837f4bf4e22fcdf920ffeaa4abf3d02d1314e03725431065f4d44c46a01b42fe'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.5.linux-arm64.tar.gz'; 			sha256='841cced7ecda9b2014f139f5bab5ae31785f35399f236b8b3e75dff2a2978d96'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.5.linux-386.tar.gz'; 			sha256='8f4dba9cf5c61757bbd7e9ebdb93b6a30a1b03f4a636a1ba0cc2f27b907ab8e1'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.5.linux-ppc64le.tar.gz'; 			sha256='907b8c6ec4be9b184952e5d3493be66b1746442394a8bc78556c56834cd7c38b'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.5.linux-riscv64.tar.gz'; 			sha256='984d8f999f5019d15527a1a0e6b0c3ef879833e26dcd422ab0ef4d81ac486b96'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.5.linux-s390x.tar.gz'; 			sha256='9c4a81b72ebe44368813cd03684e1080a818bf915d84163abae2ed325a1b2dc0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Wed, 20 Dec 2023 21:34:12 GMT
ENV GOTOOLCHAIN=local
# Wed, 20 Dec 2023 21:34:12 GMT
ENV GOPATH=/go
# Wed, 20 Dec 2023 21:34:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Dec 2023 21:34:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 20 Dec 2023 21:34:13 GMT
WORKDIR /go
# Wed, 20 Dec 2023 21:51:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 20 Dec 2023 21:51:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 20 Dec 2023 21:51:41 GMT
ENV XCADDY_SETCAP=1
# Wed, 20 Dec 2023 21:51:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 20 Dec 2023 21:51:43 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 20 Dec 2023 21:51:43 GMT
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
	-	`sha256:29bee9d75e3ae91d44ddf09cf0fa198b556654c8073aa50d8b630e52a5d203be`  
		Last Modified: Wed, 20 Dec 2023 21:36:17 GMT  
		Size: 65.8 MB (65764273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a485eddce12cbac59d4532427a2f3bc7f475a18f1b6ddc05d3631682cde4be3e`  
		Last Modified: Wed, 20 Dec 2023 21:36:00 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460d4992c24f213c1a4f97d850c33f2a32be4f0763f60ae881dfb36929edbeb8`  
		Last Modified: Wed, 20 Dec 2023 21:52:07 GMT  
		Size: 5.0 MB (4966637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf270d0f9df22c9f4d54cc419be9b59b79eec2ef2f2c70fa2545347b5db6a1de`  
		Last Modified: Wed, 20 Dec 2023 21:52:07 GMT  
		Size: 1.2 MB (1248658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29559d6667b029d9d030a6d020a049a1c7df7a5d84b925b75e0b37d63be04d25`  
		Last Modified: Wed, 20 Dec 2023 21:52:06 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:286339d083a589ff4ee17f2a98eabb1011f13f93e40c79bba2af0748f9bf2c8c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74795731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08540a67a8309258e1b934ca527574a28d9cd09a153f09e55635d67a11e5572d`
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
# Tue, 09 Jan 2024 22:59:02 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:59:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:59:24 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:59:24 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:59:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:59:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:59:27 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:59:28 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:59:29 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:59:29 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:59:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:59:30 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:59:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:59:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:59:33 GMT
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
	-	`sha256:f975e362e12b206661ef3e8661f8ddef5b3886db6695858a6ee13107cfb406cd`  
		Last Modified: Tue, 09 Jan 2024 23:10:25 GMT  
		Size: 65.8 MB (65849716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d88a6cd0c6e987e9c7854e8091bc0d3da0f5215dc272d31db2a10463a597eb`  
		Last Modified: Tue, 09 Jan 2024 23:10:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ccd85286302c0f7692dc9bf9e673cc831252fa3892db98d4a388f8e3a40229`  
		Last Modified: Tue, 09 Jan 2024 23:59:54 GMT  
		Size: 4.5 MB (4514276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c77c0eb7e54b1d25489fbedb6607137e9123f25be63514940cec48f5afbcbb`  
		Last Modified: Tue, 09 Jan 2024 23:59:53 GMT  
		Size: 1.2 MB (1246091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe6c53215469f1e0efd2612e28e7bc3d644b7460fdac4ed2217adcfcbb01ff`  
		Last Modified: Tue, 09 Jan 2024 23:59:53 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:29c1d8e221c7025b5fa2bd564d67b2cbe54abf6ed141469ee753714d4b86de8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74062596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751a7ab9b4f36aa69472a02e61896bae0e9f5d4d8751e6a7791c550f914532f6`
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
# Tue, 09 Jan 2024 22:40:13 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:40:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:40:23 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:40:23 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:40:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:40:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:40:24 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:34:49 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:34:50 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:34:50 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:34:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:34:51 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:34:51 GMT
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
	-	`sha256:f784b2816c0487ec6a1efb9635a001a738ce6794c6f60cef8dd8fc658663da9f`  
		Last Modified: Tue, 09 Jan 2024 22:45:17 GMT  
		Size: 64.2 MB (64173642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2878d57b8185e91fa6aee756ccda964266f809fac11f9dce2ed4fbfd8912f1a9`  
		Last Modified: Tue, 09 Jan 2024 22:45:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab371eb8298e2716c51ac9c58092131a438b00268b67ae458e1ace0ff2b0b5a`  
		Last Modified: Tue, 09 Jan 2024 23:35:05 GMT  
		Size: 5.1 MB (5070606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797b9a67275bffa5caa99271d04d6986b812b4aa84192f9ba3f1ff7b1dfed362`  
		Last Modified: Tue, 09 Jan 2024 23:35:05 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13428147a58f4a789fd5d1f01d54bef643a726131dd40b35c267f16843158a6c`  
		Last Modified: Tue, 09 Jan 2024 23:35:04 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:745364722abfeb88309b8c87aaea59721a3b9ce6770ef2ece3727cd89c4ecdb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74295245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ca8de75928fb38f0a93327b23d822645315bee4c8d32dbc96b28ffbf4f513b`
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
# Tue, 09 Jan 2024 22:18:29 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:18:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:18:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:18:54 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:18:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:18:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:18:58 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:31:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:31:34 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:31:34 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:31:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:31:36 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:31:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:31:39 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:31:39 GMT
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
	-	`sha256:08676902305ce1488e47f2c6cf37c156f8adf34592d23cb6c0adda7f8e20bbec`  
		Last Modified: Tue, 09 Jan 2024 22:27:11 GMT  
		Size: 64.2 MB (64202869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007761f68f098a06788d8a4f5b63c5c25fa52e8f613da754d12a9c8005b2ad44`  
		Last Modified: Tue, 09 Jan 2024 22:26:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28beac3397f3e144b5cbb889b20e5c6450f5a635fd5679a9ddb77b34420a9512`  
		Last Modified: Tue, 09 Jan 2024 23:31:57 GMT  
		Size: 5.3 MB (5270658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee35c838a10edf1f76e27c99108010f65e1cb2d9cbad31ebe0480cdcc17a15d`  
		Last Modified: Tue, 09 Jan 2024 23:31:56 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce2a624f1055a6b34babd0b44d093aa23653397f4289c89018b0396bebcf038`  
		Last Modified: Tue, 09 Jan 2024 23:31:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:9eb20c4013227f7a3b0435a6f5346ec30763958b3f54f7ad0e7a02a7dd369f5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76184930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c9ebcb7eda5bc7753c6ac25b3a1ea2cbdce628c002973e9ad47ffb0d3ba97e`
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
# Tue, 09 Jan 2024 22:43:43 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:43:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			url='https://dl.google.com/go/go1.21.6.linux-amd64.tar.gz'; 			sha256='3f934f40ac360b9c01f616a9aa1796d227d8b0328bf64cb045c7b8c4ee9caea4'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'armv7') 			url='https://dl.google.com/go/go1.21.6.linux-armv6l.tar.gz'; 			sha256='6a8eda6cc6a799ff25e74ce0c13fdc1a76c0983a0bb07c789a2a3454bf6ec9b2'; 			;; 		'aarch64') 			url='https://dl.google.com/go/go1.21.6.linux-arm64.tar.gz'; 			sha256='e2e8aa88e1b5170a0d495d7d9c766af2b2b6c6925a8f8956d834ad6b4cacbd9a'; 			;; 		'x86') 			url='https://dl.google.com/go/go1.21.6.linux-386.tar.gz'; 			sha256='05d09041b5a1193c14e4b2db3f7fcc649b236c567f5eb93305c537851b72dd95'; 			;; 		'ppc64le') 			url='https://dl.google.com/go/go1.21.6.linux-ppc64le.tar.gz'; 			sha256='e872b1e9a3f2f08fd4554615a32ca9123a4ba877ab6d19d36abc3424f86bc07f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.6.linux-riscv64.tar.gz'; 			sha256='86a2fe6597af4b37d98bca632f109034b624786a8d9c1504d340661355ed31f7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.6.linux-s390x.tar.gz'; 			sha256='92894d0f732d3379bc414ffdd617eaadad47e1d72610e10d69a1156db03fc052'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		apk del --no-network .fetch-deps; 		go version
# Tue, 09 Jan 2024 22:44:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jan 2024 22:44:00 GMT
ENV GOPATH=/go
# Tue, 09 Jan 2024 22:44:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jan 2024 22:44:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 09 Jan 2024 22:44:01 GMT
WORKDIR /go
# Tue, 09 Jan 2024 23:08:20 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:08:21 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:08:21 GMT
ENV XCADDY_SETCAP=1
# Tue, 09 Jan 2024 23:08:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 09 Jan 2024 23:08:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 09 Jan 2024 23:08:22 GMT
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
	-	`sha256:8d670b96a401a5cfb61ad27940492a2027ad1b61a1fa46000d705a1d8d159201`  
		Last Modified: Tue, 09 Jan 2024 22:51:10 GMT  
		Size: 66.3 MB (66302457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da6e3a038c3bd2afee0afab16ad35ea548d1966b1df80e55d9dcee9b280b371`  
		Last Modified: Tue, 09 Jan 2024 22:50:59 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08206a39be152f3861e70f6c3448542421f3249680b9274fd278f6015cc11aa5`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 5.1 MB (5116980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a1075ed747212d8e9506ed70d4cccab2b94dd685aa98e25a32f43575e21839`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 1.3 MB (1262390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76b6771ab88a9777236c173bb24bbc313a76da44e25c4c9ce07f8ff003338ee`  
		Last Modified: Tue, 09 Jan 2024 23:08:42 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:ee4395a3f6f47c0262fc9b8b002b6f27c88ea7f60afa086af1976dbc4aac28b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull caddy@sha256:76e18d17fe903d45f1f88f9ba76237a5fdb8392b670b3d2b0b581a9a8a4067de
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2156673231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267688b3ce7bd013fc2b9407cba404926536c40d42366eedebe5680d607fa176`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 12 Dec 2023 23:38:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Dec 2023 23:38:53 GMT
ENV GIT_VERSION=2.23.0
# Tue, 12 Dec 2023 23:38:53 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 12 Dec 2023 23:38:54 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 12 Dec 2023 23:38:55 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 12 Dec 2023 23:40:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 12 Dec 2023 23:40:27 GMT
ENV GOPATH=C:\go
# Tue, 12 Dec 2023 23:41:35 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jan 2024 22:18:47 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:22:02 GMT
RUN $url = 'https://dl.google.com/go/go1.21.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27ac9dd6e66fb3fd0acfa6792ff053c86e7d2c055b022f4b5d53bfddec9e3301'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Jan 2024 22:22:04 GMT
WORKDIR C:\go
# Tue, 09 Jan 2024 23:00:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jan 2024 23:00:16 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:00:17 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:00:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:01:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 09 Jan 2024 23:01:37 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767e95390edb4050b2c57e1d564c9e4722c5ae776ebfb8907a539571a2609f7c`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c57683b4a629f3325c8517d99f497d4ffbcd0e70354e70a95d983a275bfe398`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95bef40c25d2abc3a12986675189e7152f6197fdc5a17343bdee3f0bc2e95a8`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b043d50fbb4f0d8961fe3a95130f520d57cfe7e6e85b15cd4f9f14a01364f7ee`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55867ab446b5d5e34f9e6d414898b9a0b31051afc81b28ace1ce47e27d9e24ee`  
		Last Modified: Wed, 13 Dec 2023 00:04:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10285db29cf842d22a49b00cb66fbbfe20e7d4e72a0d3e393d58824190f6835b`  
		Last Modified: Wed, 13 Dec 2023 00:04:19 GMT  
		Size: 25.6 MB (25558777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3037ad7a881ee540014f48a43aa3a857c479d9cefb413ce61a914c943901890b`  
		Last Modified: Wed, 13 Dec 2023 00:04:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788faab53b378465ec447dde1961338c1349487d1152856c0524e2f6a503ec70`  
		Last Modified: Wed, 13 Dec 2023 00:04:12 GMT  
		Size: 282.5 KB (282534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca23066a92625cdc8de9b99f08faf5c3e756534401f72ec8aff465b29c481ee`  
		Last Modified: Tue, 09 Jan 2024 22:39:56 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b92d2b727a3677f7df423fdb871102a4f49e8ab3c3f27447b46a8bb9d6315c5`  
		Last Modified: Tue, 09 Jan 2024 22:40:17 GMT  
		Size: 69.4 MB (69428911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c07e208b8230a3cf4f0d09d8d2e0964843388a9334a811e7537778242b4610`  
		Last Modified: Tue, 09 Jan 2024 22:39:56 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0002a397ba0f92a6b352156052f4a5f9bf5bd0b854e9e066dc85b8231b8d23`  
		Last Modified: Tue, 09 Jan 2024 23:03:12 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221d1a0d3e162f0c5064835e1683a547fb68ce0fe6ddbc15547e97547f4a815f`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9d6843b6bad3862684d5eade7e7816b48ce845effe90d8c1d5d5250151dd55`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173a315f398d136fd23d058d13fa18b082575f9732c3cc17a733570a15d53606`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e288abae7098c76d0379b4bb3808523310f24e5aa535a62ff1405875e5723c`  
		Last Modified: Tue, 09 Jan 2024 23:03:11 GMT  
		Size: 1.7 MB (1676147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5e67ad5abb1499f08dbb66b77e1f22ffafb79eeacef131b3863ce4f042fcf2`  
		Last Modified: Tue, 09 Jan 2024 23:03:10 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:3d08e6c2e2cef96a5a8f6ddb7531801ad745003ddac2d632d9679e2c30f95e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2159; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2159; amd64

```console
$ docker pull caddy@sha256:b5c196359cb78d80f0c4bb97d3ffbf13a84eb3003c9f238f72cec005c9475105
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1986234916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3131c915e036b0f95ea6c698ffaf9974f6dbce70dc8d2cd1600175d4155dde16`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Tue, 12 Dec 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Dec 2023 23:35:08 GMT
ENV GIT_VERSION=2.23.0
# Tue, 12 Dec 2023 23:35:08 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 12 Dec 2023 23:35:09 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 12 Dec 2023 23:35:10 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 12 Dec 2023 23:35:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 12 Dec 2023 23:35:47 GMT
ENV GOPATH=C:\go
# Tue, 12 Dec 2023 23:36:11 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jan 2024 22:16:03 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 09 Jan 2024 22:18:27 GMT
RUN $url = 'https://dl.google.com/go/go1.21.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '27ac9dd6e66fb3fd0acfa6792ff053c86e7d2c055b022f4b5d53bfddec9e3301'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 09 Jan 2024 22:18:28 GMT
WORKDIR C:\go
# Tue, 09 Jan 2024 23:02:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jan 2024 23:02:03 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 09 Jan 2024 23:02:04 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 09 Jan 2024 23:02:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 09 Jan 2024 23:02:30 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 09 Jan 2024 23:02:31 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d0c853ded9068434b9128a8016b3ae5e18f748f62801c7bb6e6092495300ec`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf365c1e9d59a58fc8cee2522db9139b36cf02ecabe7302489a9a3667b62cea`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69dbeb610a3fa1c3f2962202c58796ff120ea20cc3ba1f2fce807cbbe2c37ab0`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a3be8233329999132fa6e504f39c44abd589439a96846e31508037334d6d11`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755721e8166183821011ca0acdb563f67887cfe33da36997710b182f049fbede`  
		Last Modified: Wed, 13 Dec 2023 00:02:37 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4700bd9f606505ec47d78dc66a509ca78ea2a8269a8e2b9bcf28ec33c5cbea74`  
		Last Modified: Wed, 13 Dec 2023 00:02:42 GMT  
		Size: 25.6 MB (25554973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777ab971ccee32e15de39ed82eceeb004d2d6f94af7c43ab3d6cfc1baf0abd07`  
		Last Modified: Wed, 13 Dec 2023 00:02:35 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958aa1458398ceb3a543d13279579cc48507080df3b269a5aa1a09da23b03ccf`  
		Last Modified: Wed, 13 Dec 2023 00:02:35 GMT  
		Size: 284.9 KB (284874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ed7a59b16104881efb9e3ac02b81f631cff124b04d7494d955a2c697b7c4ce`  
		Last Modified: Tue, 09 Jan 2024 22:39:21 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b1d528d83cdc1c6fb3f551b955643ffa64d14478df3d1b2aa1faf3cf95d454`  
		Last Modified: Tue, 09 Jan 2024 22:39:41 GMT  
		Size: 69.4 MB (69432029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8730c2425648e897784c3ff628a5fd72bb913811c924412142d22ce7f7d36c`  
		Last Modified: Tue, 09 Jan 2024 22:39:21 GMT  
		Size: 1.5 KB (1539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea60c3b2caff00ee0011a9148cabb96e3a1cde3a81a8ee5b7ca60f5513aff78`  
		Last Modified: Tue, 09 Jan 2024 23:03:30 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f939916b2a0c9fde832abafdf561e4515fc15d11979c5fa3e0bf8165cb4b3a`  
		Last Modified: Tue, 09 Jan 2024 23:03:28 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12cb1ee578e943a57f3c817517ac6b636e4d08c82aaacf57d4002b9732d98b0`  
		Last Modified: Tue, 09 Jan 2024 23:03:27 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c98bc1e6119b0ada6f9e06e3c88634debef4de96ad9906ac1d7065774a50a4f`  
		Last Modified: Tue, 09 Jan 2024 23:03:28 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc678bb3572a4a425d6d29f6ab5a6cbb6fb1e1cf427c0ed3982f9e451901c69`  
		Last Modified: Tue, 09 Jan 2024 23:03:28 GMT  
		Size: 1.7 MB (1671314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8151c697df9e9b88184cda0002778dff9d013f6ebd7c46924622bcb222243585`  
		Last Modified: Tue, 09 Jan 2024 23:03:27 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:2f148ddb6662b4245ef4ced637e928eaf67a8a1941572d69627652253e779366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5206; amd64
	-	windows version 10.0.20348.2159; amd64

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

### `caddy:latest` - windows version 10.0.17763.5206; amd64

```console
$ docker pull caddy@sha256:23906c96e8647871d54638ee95201b15a6780bd5c5a55e1910f1cce47f51327a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075748892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd668c1e74ca31419de6a4894168996b6be13d2cfb6dda297f76f1f0e82af65`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 12 Dec 2023 23:38:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 02:30:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Dec 2023 02:30:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Dec 2023 02:32:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Dec 2023 02:32:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Dec 2023 02:32:03 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Dec 2023 02:32:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Dec 2023 02:32:05 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Dec 2023 02:32:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Dec 2023 02:32:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Dec 2023 02:32:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Dec 2023 02:32:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Dec 2023 02:32:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Dec 2023 02:32:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Dec 2023 02:32:11 GMT
EXPOSE 80
# Wed, 13 Dec 2023 02:32:12 GMT
EXPOSE 443
# Wed, 13 Dec 2023 02:32:13 GMT
EXPOSE 443/udp
# Wed, 13 Dec 2023 02:32:13 GMT
EXPOSE 2019
# Wed, 13 Dec 2023 02:33:19 GMT
RUN caddy version
# Wed, 13 Dec 2023 02:33:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767e95390edb4050b2c57e1d564c9e4722c5ae776ebfb8907a539571a2609f7c`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc953d49171296238d791f543a2a026383540af60c9b10cc72446745ea9e517`  
		Last Modified: Wed, 13 Dec 2023 02:38:55 GMT  
		Size: 466.4 KB (466376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5091a1fcf41a799b6b5325321d36e20072d566027eeecc072788a9a3c3afbf0b`  
		Last Modified: Wed, 13 Dec 2023 02:38:54 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d0c21ea3d396314641058b6087c719f00acf6e81a122d0308c76705b454c5a`  
		Last Modified: Wed, 13 Dec 2023 02:38:58 GMT  
		Size: 15.3 MB (15282292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7c1ffefa6eaf8ceb9b6964a75043f3440c260e5ef8a7757a4902bbd87b5a11`  
		Last Modified: Wed, 13 Dec 2023 02:38:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209a9db6a8a0e20f16c07fa90f84ff5f0fbcf8896b719c5282405503804e4975`  
		Last Modified: Wed, 13 Dec 2023 02:38:53 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e6508c4f7300255ca275dc9fa4b8ff9f4e4ff4e6c552afee4d03305e571f8`  
		Last Modified: Wed, 13 Dec 2023 02:38:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571a096f7d34249fda9c90244912f35e632dc8c3c50a830c1d3dc6d5d2234264`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee679db41077812368c0ee8780348a81cc00878e2848106d2b022cfa25222615`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61da3eb55b53d10c6d39556e06adcd87b1e813dbf6e7c0c09a4a1fcd3c1a02af`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67d27f68c7ff3cf8ec13fd0ae72ac89b781c819f1959e16c22101faa49884a1`  
		Last Modified: Wed, 13 Dec 2023 02:38:51 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b0c532fc98f8438a57e314863455c2812c5f8273718a387893d58b1eae45a7`  
		Last Modified: Wed, 13 Dec 2023 02:38:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb76494edec3148a22e8826aa2cceb75046d74559b7fe31713da82a5504d187`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621db1494746176522163d644f8f6d572003928346b37dfea1118539767375bf`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e621e03d954adf248bd9ddcdfe28108be9204a2f010bc44cd49534bc26d10c`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb96c188ceb57176f56af8649f49ebde260394730cc2ee6bd5a10634d6676bc`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e2237c5f2e48a944f2cdc493acec61ca707749a0d33362f62a1162e6967f7f`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b904a8ec5a95b1df9b634285424830763de3a36377f8f97be9383346cd82022`  
		Last Modified: Wed, 13 Dec 2023 02:38:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ae7bbabfc6a290ea47a42a976c34545f19465895a8dee1bd94b9f6351d9ae`  
		Last Modified: Wed, 13 Dec 2023 02:38:49 GMT  
		Size: 269.0 KB (268985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4235be6cdbcf40a5350abf8550ae54349cd6889349bacb2c4c6fcdabb02fcb`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.20348.2159; amd64

```console
$ docker pull caddy@sha256:8b2e9ac9b72c8b2c90bc15116cedbb8044d599e4f86ffcbb48cebdfdf97d19f7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1905326657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7092fad7c71072036e6f6e418de96b9a293b2a5fa6c1f533192cee80981c2fdf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Tue, 12 Dec 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 02:33:55 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Dec 2023 02:33:56 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Dec 2023 02:35:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Dec 2023 02:35:11 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Dec 2023 02:35:12 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Dec 2023 02:35:12 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Dec 2023 02:35:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Dec 2023 02:35:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Dec 2023 02:35:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Dec 2023 02:35:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Dec 2023 02:35:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Dec 2023 02:35:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Dec 2023 02:35:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Dec 2023 02:35:19 GMT
EXPOSE 80
# Wed, 13 Dec 2023 02:35:20 GMT
EXPOSE 443
# Wed, 13 Dec 2023 02:35:21 GMT
EXPOSE 443/udp
# Wed, 13 Dec 2023 02:35:23 GMT
EXPOSE 2019
# Wed, 13 Dec 2023 02:35:42 GMT
RUN caddy version
# Wed, 13 Dec 2023 02:35:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d0c853ded9068434b9128a8016b3ae5e18f748f62801c7bb6e6092495300ec`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d3c17fb1ca1499edf5a0a7fe2ed357de61bc5478580af8c193d8c59e8139`  
		Last Modified: Wed, 13 Dec 2023 02:39:22 GMT  
		Size: 468.6 KB (468557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0205b9bfc982e2d76e931acf88ef85dfe1c943d4412d8e0abc82f7f0837e3ffe`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be685bdfb2389b99d51da84fb605d5905240fb7fbb82779d90949871c42c3a01`  
		Last Modified: Wed, 13 Dec 2023 02:39:24 GMT  
		Size: 15.3 MB (15270636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9935999a24844b91a4364fda0be1e1ffa280fb0c3c3c51157ffee05dc396bc2`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bd056752e2fad4d5b1e26bda93daeb2e2b89b03fc440f547e8e8e57b56ec54`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bff69c07007af0ff21680f637729be4b8d66a9b114305a47b54b631e499932`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8602ee7f30c15eb312beb9be91c2987f09264a3ec61fab2a25f7388c80361e65`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d98bd6b64e0a8382fcdef83a12bb138867f39b06a481c87d92f5e8b6bd637db`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab994312751dbeec291009c1153b38cf3621f929570200eefc6f838922099b`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb56c650abb1c98df5455b6b8c1864695f45548b82de29e570ce3f46299e574d`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b69a6fa036380dd82a0f067f8e97178a8da04f68a9c4a9eb4c10f5c432c7ad`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148841d4329f6dd8e152b2fc00676a9c4becd06e9c761400458c7b2d46438314`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8f8b0320cdf29c8f5349e14ec28542bd3c57d39b3d69d580de8ec462540d01`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b20c979eb5abf12332bf27e4b1aa8d06c7b7d6253b88d67681f13191b2ed1f5`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48a3dce4dbfd8b7dec08593b9d5c29404f49689161151ee3dda24b973f91dbe`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbc07c2849a4af7257c854c4fbd200cea57e1d10b82012dfcbe9a675b6fdcc0`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6842cf61f849c09c274f395d1e08b1196c674d9a59c34ddc4a9eb69e190b9d`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6823cd563e14b3750718450028cc7815abe14745863b57adc3e7524f3cdbfcb`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 290.0 KB (289982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae3d36b08abac2ea5a039a22621cc239126e2c32070f73be4efaacfc3c81c91`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:972db88b238031234d870fded48029f384e208fa23012db80dd8de6adc65d559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.5206; amd64
	-	windows version 10.0.20348.2159; amd64

### `caddy:windowsservercore` - windows version 10.0.17763.5206; amd64

```console
$ docker pull caddy@sha256:23906c96e8647871d54638ee95201b15a6780bd5c5a55e1910f1cce47f51327a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075748892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd668c1e74ca31419de6a4894168996b6be13d2cfb6dda297f76f1f0e82af65`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 12 Dec 2023 23:38:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 02:30:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Dec 2023 02:30:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Dec 2023 02:32:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Dec 2023 02:32:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Dec 2023 02:32:03 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Dec 2023 02:32:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Dec 2023 02:32:05 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Dec 2023 02:32:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Dec 2023 02:32:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Dec 2023 02:32:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Dec 2023 02:32:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Dec 2023 02:32:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Dec 2023 02:32:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Dec 2023 02:32:11 GMT
EXPOSE 80
# Wed, 13 Dec 2023 02:32:12 GMT
EXPOSE 443
# Wed, 13 Dec 2023 02:32:13 GMT
EXPOSE 443/udp
# Wed, 13 Dec 2023 02:32:13 GMT
EXPOSE 2019
# Wed, 13 Dec 2023 02:33:19 GMT
RUN caddy version
# Wed, 13 Dec 2023 02:33:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767e95390edb4050b2c57e1d564c9e4722c5ae776ebfb8907a539571a2609f7c`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc953d49171296238d791f543a2a026383540af60c9b10cc72446745ea9e517`  
		Last Modified: Wed, 13 Dec 2023 02:38:55 GMT  
		Size: 466.4 KB (466376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5091a1fcf41a799b6b5325321d36e20072d566027eeecc072788a9a3c3afbf0b`  
		Last Modified: Wed, 13 Dec 2023 02:38:54 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d0c21ea3d396314641058b6087c719f00acf6e81a122d0308c76705b454c5a`  
		Last Modified: Wed, 13 Dec 2023 02:38:58 GMT  
		Size: 15.3 MB (15282292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7c1ffefa6eaf8ceb9b6964a75043f3440c260e5ef8a7757a4902bbd87b5a11`  
		Last Modified: Wed, 13 Dec 2023 02:38:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209a9db6a8a0e20f16c07fa90f84ff5f0fbcf8896b719c5282405503804e4975`  
		Last Modified: Wed, 13 Dec 2023 02:38:53 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e6508c4f7300255ca275dc9fa4b8ff9f4e4ff4e6c552afee4d03305e571f8`  
		Last Modified: Wed, 13 Dec 2023 02:38:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571a096f7d34249fda9c90244912f35e632dc8c3c50a830c1d3dc6d5d2234264`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee679db41077812368c0ee8780348a81cc00878e2848106d2b022cfa25222615`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61da3eb55b53d10c6d39556e06adcd87b1e813dbf6e7c0c09a4a1fcd3c1a02af`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67d27f68c7ff3cf8ec13fd0ae72ac89b781c819f1959e16c22101faa49884a1`  
		Last Modified: Wed, 13 Dec 2023 02:38:51 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b0c532fc98f8438a57e314863455c2812c5f8273718a387893d58b1eae45a7`  
		Last Modified: Wed, 13 Dec 2023 02:38:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb76494edec3148a22e8826aa2cceb75046d74559b7fe31713da82a5504d187`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621db1494746176522163d644f8f6d572003928346b37dfea1118539767375bf`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e621e03d954adf248bd9ddcdfe28108be9204a2f010bc44cd49534bc26d10c`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb96c188ceb57176f56af8649f49ebde260394730cc2ee6bd5a10634d6676bc`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e2237c5f2e48a944f2cdc493acec61ca707749a0d33362f62a1162e6967f7f`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b904a8ec5a95b1df9b634285424830763de3a36377f8f97be9383346cd82022`  
		Last Modified: Wed, 13 Dec 2023 02:38:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ae7bbabfc6a290ea47a42a976c34545f19465895a8dee1bd94b9f6351d9ae`  
		Last Modified: Wed, 13 Dec 2023 02:38:49 GMT  
		Size: 269.0 KB (268985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4235be6cdbcf40a5350abf8550ae54349cd6889349bacb2c4c6fcdabb02fcb`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.20348.2159; amd64

```console
$ docker pull caddy@sha256:8b2e9ac9b72c8b2c90bc15116cedbb8044d599e4f86ffcbb48cebdfdf97d19f7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1905326657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7092fad7c71072036e6f6e418de96b9a293b2a5fa6c1f533192cee80981c2fdf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Tue, 12 Dec 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 02:33:55 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Dec 2023 02:33:56 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Dec 2023 02:35:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Dec 2023 02:35:11 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Dec 2023 02:35:12 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Dec 2023 02:35:12 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Dec 2023 02:35:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Dec 2023 02:35:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Dec 2023 02:35:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Dec 2023 02:35:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Dec 2023 02:35:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Dec 2023 02:35:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Dec 2023 02:35:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Dec 2023 02:35:19 GMT
EXPOSE 80
# Wed, 13 Dec 2023 02:35:20 GMT
EXPOSE 443
# Wed, 13 Dec 2023 02:35:21 GMT
EXPOSE 443/udp
# Wed, 13 Dec 2023 02:35:23 GMT
EXPOSE 2019
# Wed, 13 Dec 2023 02:35:42 GMT
RUN caddy version
# Wed, 13 Dec 2023 02:35:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d0c853ded9068434b9128a8016b3ae5e18f748f62801c7bb6e6092495300ec`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d3c17fb1ca1499edf5a0a7fe2ed357de61bc5478580af8c193d8c59e8139`  
		Last Modified: Wed, 13 Dec 2023 02:39:22 GMT  
		Size: 468.6 KB (468557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0205b9bfc982e2d76e931acf88ef85dfe1c943d4412d8e0abc82f7f0837e3ffe`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be685bdfb2389b99d51da84fb605d5905240fb7fbb82779d90949871c42c3a01`  
		Last Modified: Wed, 13 Dec 2023 02:39:24 GMT  
		Size: 15.3 MB (15270636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9935999a24844b91a4364fda0be1e1ffa280fb0c3c3c51157ffee05dc396bc2`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bd056752e2fad4d5b1e26bda93daeb2e2b89b03fc440f547e8e8e57b56ec54`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bff69c07007af0ff21680f637729be4b8d66a9b114305a47b54b631e499932`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8602ee7f30c15eb312beb9be91c2987f09264a3ec61fab2a25f7388c80361e65`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d98bd6b64e0a8382fcdef83a12bb138867f39b06a481c87d92f5e8b6bd637db`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab994312751dbeec291009c1153b38cf3621f929570200eefc6f838922099b`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb56c650abb1c98df5455b6b8c1864695f45548b82de29e570ce3f46299e574d`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b69a6fa036380dd82a0f067f8e97178a8da04f68a9c4a9eb4c10f5c432c7ad`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148841d4329f6dd8e152b2fc00676a9c4becd06e9c761400458c7b2d46438314`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8f8b0320cdf29c8f5349e14ec28542bd3c57d39b3d69d580de8ec462540d01`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b20c979eb5abf12332bf27e4b1aa8d06c7b7d6253b88d67681f13191b2ed1f5`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48a3dce4dbfd8b7dec08593b9d5c29404f49689161151ee3dda24b973f91dbe`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbc07c2849a4af7257c854c4fbd200cea57e1d10b82012dfcbe9a675b6fdcc0`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6842cf61f849c09c274f395d1e08b1196c674d9a59c34ddc4a9eb69e190b9d`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6823cd563e14b3750718450028cc7815abe14745863b57adc3e7524f3cdbfcb`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 290.0 KB (289982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae3d36b08abac2ea5a039a22621cc239126e2c32070f73be4efaacfc3c81c91`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:7c8910562b78f49c3a2f608132f963d70e34352d7b1eba277e11d71c4aadd90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull caddy@sha256:23906c96e8647871d54638ee95201b15a6780bd5c5a55e1910f1cce47f51327a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2075748892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd668c1e74ca31419de6a4894168996b6be13d2cfb6dda297f76f1f0e82af65`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Tue, 12 Dec 2023 23:38:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 02:30:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Dec 2023 02:30:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Dec 2023 02:32:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Dec 2023 02:32:02 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Dec 2023 02:32:03 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Dec 2023 02:32:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Dec 2023 02:32:05 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Dec 2023 02:32:06 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Dec 2023 02:32:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Dec 2023 02:32:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Dec 2023 02:32:08 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Dec 2023 02:32:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Dec 2023 02:32:10 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Dec 2023 02:32:11 GMT
EXPOSE 80
# Wed, 13 Dec 2023 02:32:12 GMT
EXPOSE 443
# Wed, 13 Dec 2023 02:32:13 GMT
EXPOSE 443/udp
# Wed, 13 Dec 2023 02:32:13 GMT
EXPOSE 2019
# Wed, 13 Dec 2023 02:33:19 GMT
RUN caddy version
# Wed, 13 Dec 2023 02:33:20 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767e95390edb4050b2c57e1d564c9e4722c5ae776ebfb8907a539571a2609f7c`  
		Last Modified: Wed, 13 Dec 2023 00:04:16 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc953d49171296238d791f543a2a026383540af60c9b10cc72446745ea9e517`  
		Last Modified: Wed, 13 Dec 2023 02:38:55 GMT  
		Size: 466.4 KB (466376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5091a1fcf41a799b6b5325321d36e20072d566027eeecc072788a9a3c3afbf0b`  
		Last Modified: Wed, 13 Dec 2023 02:38:54 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d0c21ea3d396314641058b6087c719f00acf6e81a122d0308c76705b454c5a`  
		Last Modified: Wed, 13 Dec 2023 02:38:58 GMT  
		Size: 15.3 MB (15282292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7c1ffefa6eaf8ceb9b6964a75043f3440c260e5ef8a7757a4902bbd87b5a11`  
		Last Modified: Wed, 13 Dec 2023 02:38:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209a9db6a8a0e20f16c07fa90f84ff5f0fbcf8896b719c5282405503804e4975`  
		Last Modified: Wed, 13 Dec 2023 02:38:53 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3e6508c4f7300255ca275dc9fa4b8ff9f4e4ff4e6c552afee4d03305e571f8`  
		Last Modified: Wed, 13 Dec 2023 02:38:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571a096f7d34249fda9c90244912f35e632dc8c3c50a830c1d3dc6d5d2234264`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee679db41077812368c0ee8780348a81cc00878e2848106d2b022cfa25222615`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61da3eb55b53d10c6d39556e06adcd87b1e813dbf6e7c0c09a4a1fcd3c1a02af`  
		Last Modified: Wed, 13 Dec 2023 02:38:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67d27f68c7ff3cf8ec13fd0ae72ac89b781c819f1959e16c22101faa49884a1`  
		Last Modified: Wed, 13 Dec 2023 02:38:51 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b0c532fc98f8438a57e314863455c2812c5f8273718a387893d58b1eae45a7`  
		Last Modified: Wed, 13 Dec 2023 02:38:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb76494edec3148a22e8826aa2cceb75046d74559b7fe31713da82a5504d187`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621db1494746176522163d644f8f6d572003928346b37dfea1118539767375bf`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e621e03d954adf248bd9ddcdfe28108be9204a2f010bc44cd49534bc26d10c`  
		Last Modified: Wed, 13 Dec 2023 02:38:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb96c188ceb57176f56af8649f49ebde260394730cc2ee6bd5a10634d6676bc`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e2237c5f2e48a944f2cdc493acec61ca707749a0d33362f62a1162e6967f7f`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b904a8ec5a95b1df9b634285424830763de3a36377f8f97be9383346cd82022`  
		Last Modified: Wed, 13 Dec 2023 02:38:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720ae7bbabfc6a290ea47a42a976c34545f19465895a8dee1bd94b9f6351d9ae`  
		Last Modified: Wed, 13 Dec 2023 02:38:49 GMT  
		Size: 269.0 KB (268985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4235be6cdbcf40a5350abf8550ae54349cd6889349bacb2c4c6fcdabb02fcb`  
		Last Modified: Wed, 13 Dec 2023 02:38:48 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:05ced206e45b045bc5cd525d92a16ed5dc3db97b7917edef04152739d06b712b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2159; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.2159; amd64

```console
$ docker pull caddy@sha256:8b2e9ac9b72c8b2c90bc15116cedbb8044d599e4f86ffcbb48cebdfdf97d19f7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1905326657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7092fad7c71072036e6f6e418de96b9a293b2a5fa6c1f533192cee80981c2fdf`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Tue, 12 Dec 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 02:33:55 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Dec 2023 02:33:56 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Dec 2023 02:35:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Dec 2023 02:35:11 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Dec 2023 02:35:12 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Dec 2023 02:35:12 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Dec 2023 02:35:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Dec 2023 02:35:14 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Dec 2023 02:35:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Dec 2023 02:35:16 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Dec 2023 02:35:17 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Dec 2023 02:35:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Dec 2023 02:35:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Dec 2023 02:35:19 GMT
EXPOSE 80
# Wed, 13 Dec 2023 02:35:20 GMT
EXPOSE 443
# Wed, 13 Dec 2023 02:35:21 GMT
EXPOSE 443/udp
# Wed, 13 Dec 2023 02:35:23 GMT
EXPOSE 2019
# Wed, 13 Dec 2023 02:35:42 GMT
RUN caddy version
# Wed, 13 Dec 2023 02:35:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d0c853ded9068434b9128a8016b3ae5e18f748f62801c7bb6e6092495300ec`  
		Last Modified: Wed, 13 Dec 2023 00:02:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d3c17fb1ca1499edf5a0a7fe2ed357de61bc5478580af8c193d8c59e8139`  
		Last Modified: Wed, 13 Dec 2023 02:39:22 GMT  
		Size: 468.6 KB (468557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0205b9bfc982e2d76e931acf88ef85dfe1c943d4412d8e0abc82f7f0837e3ffe`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be685bdfb2389b99d51da84fb605d5905240fb7fbb82779d90949871c42c3a01`  
		Last Modified: Wed, 13 Dec 2023 02:39:24 GMT  
		Size: 15.3 MB (15270636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9935999a24844b91a4364fda0be1e1ffa280fb0c3c3c51157ffee05dc396bc2`  
		Last Modified: Wed, 13 Dec 2023 02:39:21 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bd056752e2fad4d5b1e26bda93daeb2e2b89b03fc440f547e8e8e57b56ec54`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bff69c07007af0ff21680f637729be4b8d66a9b114305a47b54b631e499932`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8602ee7f30c15eb312beb9be91c2987f09264a3ec61fab2a25f7388c80361e65`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d98bd6b64e0a8382fcdef83a12bb138867f39b06a481c87d92f5e8b6bd637db`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab994312751dbeec291009c1153b38cf3621f929570200eefc6f838922099b`  
		Last Modified: Wed, 13 Dec 2023 02:39:19 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb56c650abb1c98df5455b6b8c1864695f45548b82de29e570ce3f46299e574d`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b69a6fa036380dd82a0f067f8e97178a8da04f68a9c4a9eb4c10f5c432c7ad`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148841d4329f6dd8e152b2fc00676a9c4becd06e9c761400458c7b2d46438314`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8f8b0320cdf29c8f5349e14ec28542bd3c57d39b3d69d580de8ec462540d01`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b20c979eb5abf12332bf27e4b1aa8d06c7b7d6253b88d67681f13191b2ed1f5`  
		Last Modified: Wed, 13 Dec 2023 02:39:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48a3dce4dbfd8b7dec08593b9d5c29404f49689161151ee3dda24b973f91dbe`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbc07c2849a4af7257c854c4fbd200cea57e1d10b82012dfcbe9a675b6fdcc0`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6842cf61f849c09c274f395d1e08b1196c674d9a59c34ddc4a9eb69e190b9d`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6823cd563e14b3750718450028cc7815abe14745863b57adc3e7524f3cdbfcb`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 290.0 KB (289982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae3d36b08abac2ea5a039a22621cc239126e2c32070f73be4efaacfc3c81c91`  
		Last Modified: Wed, 13 Dec 2023 02:39:15 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
