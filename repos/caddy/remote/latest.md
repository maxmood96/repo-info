## `caddy:latest`

```console
$ docker pull caddy@sha256:bcf45332e3ebd42456f5fe63be2175ebfee971d85c2cd1bd837dd0beb422fa1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.5329; amd64
	-	windows version 10.0.20348.2227; amd64

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

### `caddy:latest` - windows version 10.0.17763.5329; amd64

```console
$ docker pull caddy@sha256:45db61c754ddd6e5ec06fd28a8099b51b78e0848a64f1b55a89da26731ef2579
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2085736435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d84e958273e9ab44607135820d1cb0a85c662765ec566b7fdfc82c7f819995`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:24:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 11 Jan 2024 00:24:52 GMT
ENV CADDY_VERSION=v2.7.6
# Thu, 11 Jan 2024 00:26:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 11 Jan 2024 00:26:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 11 Jan 2024 00:26:11 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 11 Jan 2024 00:26:12 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Thu, 11 Jan 2024 00:26:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 11 Jan 2024 00:26:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 11 Jan 2024 00:26:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 11 Jan 2024 00:26:15 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 11 Jan 2024 00:26:16 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 11 Jan 2024 00:26:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 11 Jan 2024 00:26:17 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 11 Jan 2024 00:26:18 GMT
EXPOSE 80
# Thu, 11 Jan 2024 00:26:19 GMT
EXPOSE 443
# Thu, 11 Jan 2024 00:26:20 GMT
EXPOSE 443/udp
# Thu, 11 Jan 2024 00:26:21 GMT
EXPOSE 2019
# Thu, 11 Jan 2024 00:27:18 GMT
RUN caddy version
# Thu, 11 Jan 2024 00:27:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8ac948dab7d4d3a44ab44e27a80115467b2f5fba68a58b377fef3e920bc5eb`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2628b34eba07214b21750eb21215539642fc79460ac44602f68367c8ef8f1876`  
		Last Modified: Thu, 11 Jan 2024 00:31:48 GMT  
		Size: 460.6 KB (460623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bba07c52b418ca922065149b75e4f078732301d850f6c6a857a0396fa758183`  
		Last Modified: Thu, 11 Jan 2024 00:31:47 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d43dbc97e7f70164392cf4e8ba36666c051180f2d9a5fa749c2ebd8f8902da`  
		Last Modified: Thu, 11 Jan 2024 00:31:50 GMT  
		Size: 15.3 MB (15274872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf65f149b526a7db12aa1cc0a82fee2c91e70e14004538422b70bf463f1e6a`  
		Last Modified: Thu, 11 Jan 2024 00:31:47 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0e80605ac50e370132adb19e7fbd35df1083f20a16f102ba838dcd1fbe6ddb`  
		Last Modified: Thu, 11 Jan 2024 00:31:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbf4dbf98c5ef756b92eec802352998cae9a7a53998309f4d23f3a25fe998ab`  
		Last Modified: Thu, 11 Jan 2024 00:31:45 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5289b1119e5b6b3d21ecba38a21af08402723786c6a0d255d9656bab6fb0e45b`  
		Last Modified: Thu, 11 Jan 2024 00:31:45 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4279deef6070878783847e2a97632c9e6c1c1f4ee240c4582cf8ff0f507a1f`  
		Last Modified: Thu, 11 Jan 2024 00:31:45 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baca7c3ac198520fe83b18575029c9d68d6458b37234869602bf5a246f1cae49`  
		Last Modified: Thu, 11 Jan 2024 00:31:45 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc6cdf36ba1ce7eb637a46f998fd84b12e02b76b737244ac8f6a5a61a2f6d65`  
		Last Modified: Thu, 11 Jan 2024 00:31:44 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0870a17942cc9d0cbbffa15ab03f6401c95d37ab9fd965e63cb8267dfb6a4d5`  
		Last Modified: Thu, 11 Jan 2024 00:31:43 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97548b26d83c7392114297bcfdbf85c8fdf5f812fea56a4c355e28a0f063454e`  
		Last Modified: Thu, 11 Jan 2024 00:31:43 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824baecd8144b0da5828335f980e72f9721a3ac35dbda7f8927ef4e1dc4fdf0f`  
		Last Modified: Thu, 11 Jan 2024 00:31:43 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe4e2c9f762e3bacef96b2394563066a0e8f4b62d3dea44e8a8d6c1a661ac86`  
		Last Modified: Thu, 11 Jan 2024 00:31:43 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f434e7a3223202b5c62896b0b513f7ac33068974c4a3a87c2c13dd95dda313`  
		Last Modified: Thu, 11 Jan 2024 00:31:41 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41470b117bd27755279ab256ba0156bf64796a6fcd06cc26ac6d1e617387d4a0`  
		Last Modified: Thu, 11 Jan 2024 00:31:41 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e389ce50002f8ac47cbbe67517402ca31e7fc2e99945faf3cf392848560faaa8`  
		Last Modified: Thu, 11 Jan 2024 00:31:41 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0990eeef88a51462c1b1e6a7044d57c8b6976e099844570344699067f387a3`  
		Last Modified: Thu, 11 Jan 2024 00:31:42 GMT  
		Size: 254.6 KB (254599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b1fd2b9188ec5f76a81bfc4d7aa53b000672e101a91e51a5df9ab4cfcc2a8c`  
		Last Modified: Thu, 11 Jan 2024 00:31:41 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.20348.2227; amd64

```console
$ docker pull caddy@sha256:05a3dbd22c8c2ab815187427fd6c4c93118d8ef0f894a4c8ea63e2f94a614660
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1916234157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33367b5c991e5b0e4f4752a83d92a2427c6e9d98fbfdf37769b0924602a0139c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:27:50 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 11 Jan 2024 00:27:51 GMT
ENV CADDY_VERSION=v2.7.6
# Thu, 11 Jan 2024 00:28:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 11 Jan 2024 00:28:18 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 11 Jan 2024 00:28:18 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 11 Jan 2024 00:28:19 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Thu, 11 Jan 2024 00:28:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 11 Jan 2024 00:28:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 11 Jan 2024 00:28:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 11 Jan 2024 00:28:23 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 11 Jan 2024 00:28:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 11 Jan 2024 00:28:24 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 11 Jan 2024 00:28:25 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 11 Jan 2024 00:28:26 GMT
EXPOSE 80
# Thu, 11 Jan 2024 00:28:27 GMT
EXPOSE 443
# Thu, 11 Jan 2024 00:28:27 GMT
EXPOSE 443/udp
# Thu, 11 Jan 2024 00:28:28 GMT
EXPOSE 2019
# Thu, 11 Jan 2024 00:28:44 GMT
RUN caddy version
# Thu, 11 Jan 2024 00:28:45 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddb0a528ee25f289459dfa0d84bac9a14b9127f771882f0b60425ffaab79933`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320a9722b5187c98507b3945fbc5f2610abcc5d11d2a15edefb980c3890b4e62`  
		Last Modified: Thu, 11 Jan 2024 00:32:14 GMT  
		Size: 453.3 KB (453259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752dd8672cb5e334b293f934bde801e1be65eefc21179ec32a474b467094ac33`  
		Last Modified: Thu, 11 Jan 2024 00:32:13 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a96d6e9a72b624c3ca3d2ef154de09ab3922aeb66434dca1c3ada99bf483f7`  
		Last Modified: Thu, 11 Jan 2024 00:32:17 GMT  
		Size: 15.3 MB (15265727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c07cef1770381d1bd7e459337ce742ee1284a3a4f8aac9a8fa9021d44757d3`  
		Last Modified: Thu, 11 Jan 2024 00:32:13 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82192ad642e7980cf5f189cbec9102a5d27ebe938505fb7f1d3f00f6aed19f7b`  
		Last Modified: Thu, 11 Jan 2024 00:32:12 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4803481e3aae3efca19bc8239515b896f31b9c62936eff5e6b5f1f6e993027f`  
		Last Modified: Thu, 11 Jan 2024 00:32:12 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a2a948dcaeaac0c98b7c989af28731ccb460e44746d30876190f5a9533d4c3`  
		Last Modified: Thu, 11 Jan 2024 00:32:11 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb1fe3167023a8395dfb5d81d67735c3fac4f60265929a599be827819517ac5`  
		Last Modified: Thu, 11 Jan 2024 00:32:11 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe6c398a041f35ff13cb508ddac27bcfebcb67648963fa20c8a1674e0e272c0`  
		Last Modified: Thu, 11 Jan 2024 00:32:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823f94dc7cc6da16f64623b1be06863d7e5fd9537404d44d75bce4c9286d99d7`  
		Last Modified: Thu, 11 Jan 2024 00:32:10 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc6ad89630dde06deaf62bae99287cff6f9527eb0e4c0285b80c4b9f8b3392a`  
		Last Modified: Thu, 11 Jan 2024 00:32:10 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57f987c615a8934b60b413c4fb87f01bc1da99f905a3875ae15c1aa9e27972d`  
		Last Modified: Thu, 11 Jan 2024 00:32:10 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02382ce5c206a96e1663dafb2c888a7f7e97c9ce90d2b4e909e7a9b35b9456b8`  
		Last Modified: Thu, 11 Jan 2024 00:32:09 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60fd2eca8dc0381fd073410f4a3fb823dbd8ace74b7e02c761dbbf3fe531cff`  
		Last Modified: Thu, 11 Jan 2024 00:32:09 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7f66b6ee25ed55a56fb5128546b63989de6134ebbaca4e28b5486e3f64978b`  
		Last Modified: Thu, 11 Jan 2024 00:32:07 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba2deb7a206bc3d9388c2ac7b452b6399c7640b5f133e5ebfecfe63f1b33203`  
		Last Modified: Thu, 11 Jan 2024 00:32:07 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0838841899be257f01da94634e7b567988eaabe9d86f896573bf1cd1115c60`  
		Last Modified: Thu, 11 Jan 2024 00:32:07 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79396b6f9c050e882d6c88bfe39e8289153fe98a4b83c004731ab90e32fb4be`  
		Last Modified: Thu, 11 Jan 2024 00:32:08 GMT  
		Size: 278.6 KB (278612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2225d4cc5c0d44fab26c5a88559b5fb67343364f0ae80e4689ee11674d61a9`  
		Last Modified: Thu, 11 Jan 2024 00:32:07 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
