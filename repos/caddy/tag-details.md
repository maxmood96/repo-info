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
$ docker pull caddy@sha256:ce43091c481420028215c752115f25e501155b055ae9f4862bae373bda4c1308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `caddy:2` - linux; amd64

```console
$ docker pull caddy@sha256:a6054d207060158cd0f019d6a35907bf47d1f8dacf58cdb63075a930d8ebca38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18467348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da4af4af9d73e970be3df873e00b8e658a7fc56ab982bfffa21d9bae68e3943`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:18:44 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 03:18:46 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 03:18:46 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 03:18:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 03:18:48 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 03:18:48 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 03:18:48 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 03:18:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 03:18:48 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 80
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 443
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 03:18:49 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 03:18:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a167b92bd92ca649523209f279d023d90edd2658f2dbbd5a79cd991b707a1bf4`  
		Last Modified: Sat, 16 Mar 2024 03:19:12 GMT  
		Size: 350.8 KB (350841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa65d2923419d52c79891c5c107216c8efc7534f740cafcddcb57fcd915fd61`  
		Last Modified: Sat, 16 Mar 2024 03:19:12 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832dc3f423aedf5c58d59571f7e5eebd543b4c31f0a0bacc36b509313473765e`  
		Last Modified: Sat, 16 Mar 2024 03:19:15 GMT  
		Size: 14.7 MB (14706436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:d5b956705aa5cb2d80a34b0da959c62f6e1b85d3b6af5d39bdd43a5ebad79732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17423235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637ed474101820123d027bf07c3bacd795eec60a114ec44aa0ab7c081f03fcdd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:36:00 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 06:36:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 06:36:01 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 06:36:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 06:36:04 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 06:36:04 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 06:36:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 06:36:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 06:36:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 80
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 443
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 06:36:05 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 06:36:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7e837cfa426b2a8d095055ea95ecda50deb35a29395410997280bf4efa14be`  
		Last Modified: Sat, 16 Mar 2024 06:36:25 GMT  
		Size: 347.6 KB (347629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aac6695e2937791ffb389edf1aee134b4e2e7c879173c70c5b0851017f402f5`  
		Last Modified: Sat, 16 Mar 2024 06:36:24 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a5dfabcee2609d8f2199b85fef83d4b0fa6612faa5a74b40f2809ccef87a5d`  
		Last Modified: Sat, 16 Mar 2024 06:36:27 GMT  
		Size: 13.9 MB (13921018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:d193bf8cf22c67a72ca3f4bc784363a0964ee0bc6481457a375beff0c515bb7b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17147117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c56baf0ceba318c0b5f456a51c90a5291492d8586689fa76bc097b01b50d670`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:36:34 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 08:36:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 08:36:35 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 08:36:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 08:36:38 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 08:36:38 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 08:36:38 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 08:36:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 08:36:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 80
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 443
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 08:36:39 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 08:36:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ad552b06977a907a460096cd3aa8d4cad657ae3a90be3bc63eba494b31a255`  
		Last Modified: Sat, 16 Mar 2024 08:36:59 GMT  
		Size: 344.5 KB (344462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7eb11427d968ddc8915316bd59544b644278fd1c3960927ab066c8cc916a8b`  
		Last Modified: Sat, 16 Mar 2024 08:36:58 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a13a58310f383c1986a52280e47b5d9a59f7ef7f02bf39ff3b494af779dab9`  
		Last Modified: Sat, 16 Mar 2024 08:37:02 GMT  
		Size: 13.9 MB (13893734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:aaf3497a43eee2656c636b04c5ac7dd7f81e15e6911be1c0509fcc51df3e6dbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f62720e336d430f97f77dea70bb3ceacea271cb1d7f6a246eb3c366e509827`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:55:39 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 02:55:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 02:55:41 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 02:55:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 02:55:43 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 02:55:43 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 02:55:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 80
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 443
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 02:55:44 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 02:55:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef488aa53de475202749fc28d385b1e4e59841fe4085a7edee2eb5026d11b95c`  
		Last Modified: Sat, 16 Mar 2024 02:56:01 GMT  
		Size: 360.7 KB (360666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322174feb81fda6e9c1e8e8ac7e49b8e77de2dca870243af972ee7545d4b7916`  
		Last Modified: Sat, 16 Mar 2024 02:56:01 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3360e007ed3153df2f6fbc7ef89943b1fc701d62c811d8855293b7df0f352d`  
		Last Modified: Sat, 16 Mar 2024 02:56:02 GMT  
		Size: 13.6 MB (13568947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; ppc64le

```console
$ docker pull caddy@sha256:00e289b4657ffa0aec2c98f544cf7890e6cf6e4bd9dd1adfc01697d5fbb436a6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17052079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717f7ea5ec28ca8fed34729b1466cd1f5f96309057a0ec85b2e903833000f9ac`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:55:44 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 15 Mar 2024 23:55:46 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 15 Mar 2024 23:55:47 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 15 Mar 2024 23:55:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 15 Mar 2024 23:55:51 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 15 Mar 2024 23:55:51 GMT
ENV XDG_DATA_HOME=/data
# Fri, 15 Mar 2024 23:55:52 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 15 Mar 2024 23:55:52 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 15 Mar 2024 23:55:52 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 15 Mar 2024 23:55:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 15 Mar 2024 23:55:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 15 Mar 2024 23:55:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 15 Mar 2024 23:55:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 15 Mar 2024 23:55:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 15 Mar 2024 23:55:54 GMT
EXPOSE 80
# Fri, 15 Mar 2024 23:55:55 GMT
EXPOSE 443
# Fri, 15 Mar 2024 23:55:55 GMT
EXPOSE 443/udp
# Fri, 15 Mar 2024 23:55:55 GMT
EXPOSE 2019
# Fri, 15 Mar 2024 23:55:56 GMT
WORKDIR /srv
# Fri, 15 Mar 2024 23:55:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d58b091eab1c134ec71c79ecd145766a6b85840017d1e2223575349179f742c`  
		Last Modified: Fri, 15 Mar 2024 23:56:22 GMT  
		Size: 362.2 KB (362200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cfe42e2461424bcaa647db536a9454b1c48bf3410add89e0ec0367328cff78`  
		Last Modified: Fri, 15 Mar 2024 23:56:22 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103d176f7ec2158a797ee8c4909124a9a7cc2b8cff9b8c59e7368d8730563728`  
		Last Modified: Fri, 15 Mar 2024 23:56:24 GMT  
		Size: 13.3 MB (13333863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; s390x

```console
$ docker pull caddy@sha256:aabd334d2f437365b8585670694b9cbe711132d5937a3d7f14b5840ff92fbf55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17818312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dd63d90fd552a57206bdfb4bb41bc51fd60b881c3ffe41f0852c6bac9ef68e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:48:00 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 04:48:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 04:48:01 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 04:48:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 04:48:04 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 04:48:04 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 04:48:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 04:48:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 04:48:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 04:48:05 GMT
EXPOSE 80
# Sat, 27 Jan 2024 04:48:05 GMT
EXPOSE 443
# Sat, 27 Jan 2024 04:48:05 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 04:48:06 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 04:48:06 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 04:48:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e608a3e3404a06a0444cc06a7949f9a4a2c56e2983aced16d2d32f009f2dbc17`  
		Last Modified: Sat, 27 Jan 2024 04:50:42 GMT  
		Size: 354.9 KB (354944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addd52ad78c14ade7e55ee491d32b0e51556e0c0a8b84d1fd1abc3a1430cc057`  
		Last Modified: Sat, 27 Jan 2024 04:50:42 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e597a1de66b259ef54ca1d052f65d662a6ea3ebf545513d9c91e80c67aa1f3`  
		Last Modified: Sat, 27 Jan 2024 04:50:44 GMT  
		Size: 14.2 MB (14238310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:e92a98f9befbcc685cba6014745c4c4e5573d524f98646666afae41fe635a647
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1973514153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c02263e4345786d822a7cbe2109be66b8bbc405dad0088432e203c583cdb8c4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:37:25 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:37:26 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:37:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:37:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:37:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:37:54 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:37:55 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:37:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:37:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:37:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:38:00 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:38:01 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:38:03 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:38:21 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:38:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3433f0cddf0bf50f831ae26d44034fb9ccdaea63173630b59cbe9dc33860a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:45 GMT  
		Size: 471.5 KB (471467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39aa89107a4c1ac15acc37ba98faa00f98774062e839984cd569c84acccbefa`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903c57abacc03a4132d1914d83b140d91cad6d3f72113588dbb0449668e5459e`  
		Last Modified: Wed, 13 Mar 2024 02:41:47 GMT  
		Size: 15.3 MB (15272331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c505d8db5c54f9f5b13a230f310c78e1daa9f0fa5baa7db6bb4b6f9b2824c64`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02c7783ff4e4ea0351aa496f9316d007b5d39dd7ac091772a53c788cc850835`  
		Last Modified: Wed, 13 Mar 2024 02:41:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2f6f475cd8b631685eb3441f13c0418b595dc3f64fc43f4de103cd270bd07a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c099338186092d8e8a9ee4e1aef2ac6bac6e0e37d05b00acc2519d4828eebc1a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66be30fd26f10adf7753fc7287726b290417f432503173cc8cfcc37c5970eed5`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdecded462eba57ac719ddeaf73027953397d9470c8d9ce91486b650688448d1`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b196924a8268e867bced4e92552ad7a24d5079dd5d3a5f2d32e98acf5b94ec`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83e0533daa0143428320795f95f747a318ce9dfaec9c1918dc09ddabff7ce6`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d6f7d580438b0f330c60e990071ee0a7fd2cb8e861b5b3673229aae5f40a97`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3043316cf0d3543d7ad8c2cf29b9f42217a7ff7ee358b9ccf49ec1c2742b40dc`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9d07b35dd72d9c89f56d604b5b5ff1096607de0b699a7845b4d4eef4542999`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7138f2320f3eb26befb56422d151646fa73d61b45b1fd7ba1a97e97b12b1794`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dd6eb25db87e92a30fe3a646b0ca820c3a8a855af39f49e9c1239e9e7e8fa8`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff49c00e60e2791dac19058d6bba6e562c80b90859f8e91ae70b474a582042`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c28453d92f8177a5ca4103ba031b5f02ceb70269930e8642e8bda358f1eef11`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 289.3 KB (289264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5958cc3ab872a13ea8011a1ae0a2290cefbfb5721bf58c5c16e2a1dfa216aa`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:2a10673838e2beefb539398925457319c1e7800b242f5c261bc40ddd7f16aa33
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2141123401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001b000d65334996d09969a3e79ce6304b5ea6811c67eb7add59f0c78b73ba5c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:34:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:34:08 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:35:29 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:35:30 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:35:31 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:35:31 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:35:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:35:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:35:35 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:35:36 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:35:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:35:39 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:35:40 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:36:47 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:36:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bb323765ff7b405cedec6f88daa8a1c8470f45c358d637c0062cf4c63d7e07`  
		Last Modified: Wed, 13 Mar 2024 02:41:21 GMT  
		Size: 465.6 KB (465620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b3f11ec4ee425a6a0b9f5ad200c9193592181f59520c9a80372e647787163a`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ffe491a522455b1d95c1d0d3384188ea361064259fffcadd657bebae4fa934`  
		Last Modified: Wed, 13 Mar 2024 02:41:24 GMT  
		Size: 15.3 MB (15277213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b62af40926c0d1a37e6126f41f63533166809b5b54434cf3b53ab5734357e59`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a9b1639ec2e8588ca4fd94f87b31b4e30adef3c0ac45ea4ac0e4cdce643d6`  
		Last Modified: Wed, 13 Mar 2024 02:41:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7a48958fcb11d52bb7a65f60d6f322d3326d4f2916e0547b764cbe4fe0eae8`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9eb36d28260e8ba5549b16a87d121a4d7b0d38f46e1127ee1fd95f2e31e6f2c`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d221a46e4e966da289289be19ac425d0199540bef1d6d7c890ba45ec255e79`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feeda3213337ce81d383bcb08c0b241e763185b91a2e180f35c59395e3c0290f`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d7bf5ae3a283a09c7a385afa5160b2d0f1d275fc23e0a1711bf734511fe0b1`  
		Last Modified: Wed, 13 Mar 2024 02:41:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f309d19b55289fe422d64dd24736be59a52f6eba872d8fb1054416f8b5d9c553`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4ac1a4021eeee54512dde50b437001408fd1dda9d896f68d38728f7dba8c6c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e117655b528b6e8f7ce8d4d2cb69d41a1735fec0e31e10dc40cddcf0d012be`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5524c6d618843e710fa22d77e57a844c7cdfd68676c809d2d1ecde656c16a81c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879784be55be2c5d212302ae42232de9bfeaccea0b1398ec0101ef36d542930c`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f8aadcc42505eea344cf0504c7312d01033f159e88d6eadab5abb9eefc98a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41580c6cc25a82ee1a4de9315ec98ce6e89bd73461a941248648d04292e9ff52`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1261dc2b6b686493c5c3989f8efdd404b912398f6a38933aba80fe65d5d6240c`  
		Last Modified: Wed, 13 Mar 2024 02:41:15 GMT  
		Size: 258.2 KB (258159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8856855cc09ca543e8712766ea12d12556af369305babcaf786f620c89c3450d`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:dda81a416214d4dbdd978810efa19643e39b626fe0f979558fbb116758784c89
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
$ docker pull caddy@sha256:a6054d207060158cd0f019d6a35907bf47d1f8dacf58cdb63075a930d8ebca38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18467348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da4af4af9d73e970be3df873e00b8e658a7fc56ab982bfffa21d9bae68e3943`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:18:44 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 03:18:46 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 03:18:46 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 03:18:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 03:18:48 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 03:18:48 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 03:18:48 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 03:18:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 03:18:48 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 80
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 443
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 03:18:49 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 03:18:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a167b92bd92ca649523209f279d023d90edd2658f2dbbd5a79cd991b707a1bf4`  
		Last Modified: Sat, 16 Mar 2024 03:19:12 GMT  
		Size: 350.8 KB (350841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa65d2923419d52c79891c5c107216c8efc7534f740cafcddcb57fcd915fd61`  
		Last Modified: Sat, 16 Mar 2024 03:19:12 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832dc3f423aedf5c58d59571f7e5eebd543b4c31f0a0bacc36b509313473765e`  
		Last Modified: Sat, 16 Mar 2024 03:19:15 GMT  
		Size: 14.7 MB (14706436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:d5b956705aa5cb2d80a34b0da959c62f6e1b85d3b6af5d39bdd43a5ebad79732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17423235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637ed474101820123d027bf07c3bacd795eec60a114ec44aa0ab7c081f03fcdd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:36:00 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 06:36:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 06:36:01 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 06:36:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 06:36:04 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 06:36:04 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 06:36:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 06:36:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 06:36:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 80
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 443
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 06:36:05 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 06:36:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7e837cfa426b2a8d095055ea95ecda50deb35a29395410997280bf4efa14be`  
		Last Modified: Sat, 16 Mar 2024 06:36:25 GMT  
		Size: 347.6 KB (347629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aac6695e2937791ffb389edf1aee134b4e2e7c879173c70c5b0851017f402f5`  
		Last Modified: Sat, 16 Mar 2024 06:36:24 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a5dfabcee2609d8f2199b85fef83d4b0fa6612faa5a74b40f2809ccef87a5d`  
		Last Modified: Sat, 16 Mar 2024 06:36:27 GMT  
		Size: 13.9 MB (13921018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:d193bf8cf22c67a72ca3f4bc784363a0964ee0bc6481457a375beff0c515bb7b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17147117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c56baf0ceba318c0b5f456a51c90a5291492d8586689fa76bc097b01b50d670`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:36:34 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 08:36:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 08:36:35 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 08:36:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 08:36:38 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 08:36:38 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 08:36:38 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 08:36:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 08:36:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 80
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 443
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 08:36:39 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 08:36:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ad552b06977a907a460096cd3aa8d4cad657ae3a90be3bc63eba494b31a255`  
		Last Modified: Sat, 16 Mar 2024 08:36:59 GMT  
		Size: 344.5 KB (344462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7eb11427d968ddc8915316bd59544b644278fd1c3960927ab066c8cc916a8b`  
		Last Modified: Sat, 16 Mar 2024 08:36:58 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a13a58310f383c1986a52280e47b5d9a59f7ef7f02bf39ff3b494af779dab9`  
		Last Modified: Sat, 16 Mar 2024 08:37:02 GMT  
		Size: 13.9 MB (13893734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:aaf3497a43eee2656c636b04c5ac7dd7f81e15e6911be1c0509fcc51df3e6dbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f62720e336d430f97f77dea70bb3ceacea271cb1d7f6a246eb3c366e509827`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:55:39 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 02:55:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 02:55:41 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 02:55:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 02:55:43 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 02:55:43 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 02:55:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 80
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 443
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 02:55:44 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 02:55:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef488aa53de475202749fc28d385b1e4e59841fe4085a7edee2eb5026d11b95c`  
		Last Modified: Sat, 16 Mar 2024 02:56:01 GMT  
		Size: 360.7 KB (360666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322174feb81fda6e9c1e8e8ac7e49b8e77de2dca870243af972ee7545d4b7916`  
		Last Modified: Sat, 16 Mar 2024 02:56:01 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3360e007ed3153df2f6fbc7ef89943b1fc701d62c811d8855293b7df0f352d`  
		Last Modified: Sat, 16 Mar 2024 02:56:02 GMT  
		Size: 13.6 MB (13568947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:00e289b4657ffa0aec2c98f544cf7890e6cf6e4bd9dd1adfc01697d5fbb436a6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17052079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717f7ea5ec28ca8fed34729b1466cd1f5f96309057a0ec85b2e903833000f9ac`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:55:44 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 15 Mar 2024 23:55:46 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 15 Mar 2024 23:55:47 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 15 Mar 2024 23:55:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 15 Mar 2024 23:55:51 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 15 Mar 2024 23:55:51 GMT
ENV XDG_DATA_HOME=/data
# Fri, 15 Mar 2024 23:55:52 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 15 Mar 2024 23:55:52 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 15 Mar 2024 23:55:52 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 15 Mar 2024 23:55:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 15 Mar 2024 23:55:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 15 Mar 2024 23:55:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 15 Mar 2024 23:55:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 15 Mar 2024 23:55:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 15 Mar 2024 23:55:54 GMT
EXPOSE 80
# Fri, 15 Mar 2024 23:55:55 GMT
EXPOSE 443
# Fri, 15 Mar 2024 23:55:55 GMT
EXPOSE 443/udp
# Fri, 15 Mar 2024 23:55:55 GMT
EXPOSE 2019
# Fri, 15 Mar 2024 23:55:56 GMT
WORKDIR /srv
# Fri, 15 Mar 2024 23:55:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d58b091eab1c134ec71c79ecd145766a6b85840017d1e2223575349179f742c`  
		Last Modified: Fri, 15 Mar 2024 23:56:22 GMT  
		Size: 362.2 KB (362200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cfe42e2461424bcaa647db536a9454b1c48bf3410add89e0ec0367328cff78`  
		Last Modified: Fri, 15 Mar 2024 23:56:22 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103d176f7ec2158a797ee8c4909124a9a7cc2b8cff9b8c59e7368d8730563728`  
		Last Modified: Fri, 15 Mar 2024 23:56:24 GMT  
		Size: 13.3 MB (13333863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:aabd334d2f437365b8585670694b9cbe711132d5937a3d7f14b5840ff92fbf55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17818312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dd63d90fd552a57206bdfb4bb41bc51fd60b881c3ffe41f0852c6bac9ef68e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:48:00 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 04:48:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 04:48:01 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 04:48:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 04:48:04 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 04:48:04 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 04:48:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 04:48:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 04:48:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 04:48:05 GMT
EXPOSE 80
# Sat, 27 Jan 2024 04:48:05 GMT
EXPOSE 443
# Sat, 27 Jan 2024 04:48:05 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 04:48:06 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 04:48:06 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 04:48:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e608a3e3404a06a0444cc06a7949f9a4a2c56e2983aced16d2d32f009f2dbc17`  
		Last Modified: Sat, 27 Jan 2024 04:50:42 GMT  
		Size: 354.9 KB (354944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addd52ad78c14ade7e55ee491d32b0e51556e0c0a8b84d1fd1abc3a1430cc057`  
		Last Modified: Sat, 27 Jan 2024 04:50:42 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e597a1de66b259ef54ca1d052f65d662a6ea3ebf545513d9c91e80c67aa1f3`  
		Last Modified: Sat, 27 Jan 2024 04:50:44 GMT  
		Size: 14.2 MB (14238310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:297a97b4f8f3f4467bcf9cfd5a6f5ba5bcfa38be56824c82e2c4f1c029701f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:a37704d2149bb703350b3e63704ecb468ec6f10cdc3784c818988e250484b2ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76973825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a6b943c698684ea914a9d08c8a00d2e573cbc2a95669142bc1b35350317cff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 03:18:55 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 03:18:55 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 03:18:55 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 03:18:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 03:18:55 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 03:18:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 03:18:57 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 03:18:57 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e791cb90c3d0bf08a988f13b405c9947c74b5bc31c7c939197a7175f6c7f0e`  
		Last Modified: Sat, 27 Jan 2024 01:36:33 GMT  
		Size: 284.7 KB (284690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3da9c61ef062502252a549dbc1f90925a8d7b6ef0644ffbfaea77be8b6f058`  
		Last Modified: Tue, 05 Mar 2024 19:25:57 GMT  
		Size: 67.0 MB (67010725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1741a7c0e9ce85801257b76332c08a3abdf5069bf46b0e764a32219d92189dc5`  
		Last Modified: Tue, 05 Mar 2024 19:25:45 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f302d3cc779898a1baa29b9dde46627021754a60a003a8ceb71b73f80af80bb2`  
		Last Modified: Sat, 16 Mar 2024 03:19:27 GMT  
		Size: 5.0 MB (4973021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51954c5f8bcd596606e74156291b16b5d0c2b430bb9f0a49db89dc03278cbd8e`  
		Last Modified: Sat, 16 Mar 2024 03:19:26 GMT  
		Size: 1.3 MB (1302235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351f34f77cd30086783b4d1e7bd91ac224af75f55690527012c4f114a65048b5`  
		Last Modified: Sat, 16 Mar 2024 03:19:26 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:042f6baf4a87f12037bf9a9146e994b03974edfdf6e94ef3a6c8ed9a5b0e01d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75407449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8104ab01bd342cfbbde6ad9a086efdba750ddaaeb6b4ce5acae4072b032808f1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 06:36:10 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 06:36:10 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 06:36:10 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 06:36:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 06:36:10 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 06:36:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 06:36:11 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 06:36:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18595ac3d5791e4d7e7dbcffcbf63e97e29974bd7191f7779889293f06709605`  
		Last Modified: Sat, 16 Mar 2024 01:27:12 GMT  
		Size: 284.9 KB (284879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67b0661c8b928f9ee07193e83a55962dc30ea03b3917d927fbfc6172db763d1`  
		Last Modified: Sat, 16 Mar 2024 01:28:25 GMT  
		Size: 65.8 MB (65767483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e94e3f035a7e84adb42051a6776fb957bb01e4afe261ef52850410749238c3e`  
		Last Modified: Sat, 16 Mar 2024 01:28:09 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90af61f594723149cbf4c52926248b7aa924edce2e71c1146dbfe1c4952d0e85`  
		Last Modified: Sat, 16 Mar 2024 06:36:39 GMT  
		Size: 5.0 MB (4958759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2b089f053b69b50a0ec1b57924c3f1dbab09af5f892a3f3824a1f1d91c4653`  
		Last Modified: Sat, 16 Mar 2024 06:36:39 GMT  
		Size: 1.2 MB (1248659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb3baf5a17563281d926d65bf039e75bafa0be92988b008e142f88f13e48831`  
		Last Modified: Sat, 16 Mar 2024 06:36:39 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:bba85446aa9cf082d96393b37ee2eb8948d32119f9f1b4a7de4264ed6265bc16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d75fc02eccf5b473914195c6b5a7f27a9c7b3af790feb14ca2afa4f0a1e6d2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 08:36:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 08:36:44 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 08:36:44 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 08:36:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 08:36:44 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 08:36:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 08:36:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 08:36:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03de95814623b83a4328b4db2e23b14214f57c18389a27379988469d9b6bbccc`  
		Last Modified: Sat, 16 Mar 2024 00:51:49 GMT  
		Size: 284.1 KB (284082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb316a6d2b1f8b686717aa026be6622630e91b4e2beff72260e41b9c26f5f328`  
		Last Modified: Sat, 16 Mar 2024 00:52:59 GMT  
		Size: 65.8 MB (65767446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3402119434a07f7977a54237330b21abbea9474c729d8bbbe43e79507612156`  
		Last Modified: Sat, 16 Mar 2024 00:52:46 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3e193cf2bcf63192347811ea80a7312b468b42f6341ff8912fb721dcdd07b1`  
		Last Modified: Sat, 16 Mar 2024 08:37:14 GMT  
		Size: 4.5 MB (4514679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302bab84b8a106df7129ce421df27645cf93461c26631a73c4c16dcc48213e33`  
		Last Modified: Sat, 16 Mar 2024 08:37:14 GMT  
		Size: 1.2 MB (1246087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa5da11b54d5792ea909f7bcbe533482069dd4540457779cb629671faadd4eb`  
		Last Modified: Sat, 16 Mar 2024 08:37:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:636495b6181fd6f900cfb1c3fafd4aa67ef8113e127a39c225dcd2b9f28018ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73993764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804083a23a5a42633ad7c22fc0b9908822db952792867afe4852db23de6882c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 02:55:47 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 02:55:48 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 02:55:48 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 02:55:48 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 02:55:48 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 02:55:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 02:55:49 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 02:55:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69c4102457739613c6fcb205a5a8e7dbc8383d57dade0a4502b1bca7b100a4d`  
		Last Modified: Sat, 16 Mar 2024 02:38:03 GMT  
		Size: 286.3 KB (286314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472e8443302a7aa2ee7c60f88cf1c1bff960c6982004fabf4d0b7dbb39552784`  
		Last Modified: Sat, 16 Mar 2024 02:38:55 GMT  
		Size: 64.1 MB (64111127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f3ae01babba08c7331e1311c66fc81f093559e9b48b75c7f09e492835df417`  
		Last Modified: Sat, 16 Mar 2024 02:38:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a47c8e46877caae3d8fa35784305f82b6173865f636c831581e413586174c9f`  
		Last Modified: Sat, 16 Mar 2024 02:56:14 GMT  
		Size: 5.1 MB (5063904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b458a517cc70120b5d5ad7b3624d14288f8fc2bb374503684e47dfb2d81ede41`  
		Last Modified: Sat, 16 Mar 2024 02:56:14 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e927a09144840e6a0520002506a03480353d2bf16acf387e392f67125a232f`  
		Last Modified: Sat, 16 Mar 2024 02:56:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:74036381f9b78d58ddddc74f279042dff06d05ac2b95c3faf063485eac603111
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74219852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afdeb2455afb0545182f73124c3e233abb4a6b803a834f42127d9a1eff4982c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 07:31:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 07:31:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 07:31:22 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 07:31:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 07:31:22 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 07:31:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 07:31:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 07:31:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e315e4c0ee7596e0eb7cc17d622c433e9fc4ef254b722e11e6794265328ea583`  
		Last Modified: Sat, 16 Mar 2024 00:32:12 GMT  
		Size: 286.7 KB (286670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee59a251903fa4e415f22830cd12da95ca1bcf671572b4a701a1d8f75a55d5ee`  
		Last Modified: Sat, 16 Mar 2024 00:33:15 GMT  
		Size: 64.1 MB (64126904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a227c25fca514ad52229d19315a3e0db7f235f9a840f9474237fadee44634bd1`  
		Last Modified: Sat, 16 Mar 2024 00:33:03 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da53f00025342b23cc1c1a712e9f3ff08b05bc0759f58b580a2081c4b925b9e8`  
		Last Modified: Sat, 16 Mar 2024 07:31:42 GMT  
		Size: 5.3 MB (5271003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1eb59d0f562ae579e22be9806e6ea172a7ee0399f354980329dfa3e8e04045`  
		Last Modified: Sat, 16 Mar 2024 07:31:41 GMT  
		Size: 1.2 MB (1186176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f27806532c2006d7f3b98c3ab37d72cf977ec4c488b65e389cb46e6b551627`  
		Last Modified: Sat, 16 Mar 2024 07:31:41 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:179342439e20a0f8308f5b3c8f51063386fb33fb38d9eda738dfd1d4b398280c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76101838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4eddf19e318b73f4fa90802285b549c08b6b015cfc8f36a11adbbf9c593fc2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Tue, 05 Mar 2024 20:58:12 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:58:12 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:58:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:58:13 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:58:13 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1b6899ff00172fd5c809d57028913a3c5aead2c05d0c3c01b15a5249c4ddec`  
		Last Modified: Sat, 27 Jan 2024 05:46:31 GMT  
		Size: 285.1 KB (285091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192deec459dbc25471d5ce96dbf84de90f9e77914e5074081b4aba0516977050`  
		Last Modified: Tue, 05 Mar 2024 20:12:42 GMT  
		Size: 66.2 MB (66218961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e6d46fb71afdd9825fc4397b4949daac74f5a564377560ed3cb3bb910da97f`  
		Last Modified: Tue, 05 Mar 2024 20:12:31 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad42b5ce4497969e7a2ebbdf9ada284081c50ce1744927873987c8075ed117fa`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 5.1 MB (5117256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea105a4685d829ffde13e2d0e06f02ec7f1e1381059eae15941a5aeb36d5f7a7`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 1.3 MB (1262390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1423e2dcf9499ee1179b946513f3194740bf64ee1f24d0a7688bde92f8773874`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:deed166abe77b412a506924346166c58e03f6e35fb2836e7af244be01925eddf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2054342050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7b95fb04081aaf80026e1bb52d4a79df79ea5aac969382123b16607318419f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 01:46:04 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Mar 2024 01:46:05 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Mar 2024 01:46:06 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Mar 2024 01:46:07 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Mar 2024 01:46:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 01:46:43 GMT
ENV GOPATH=C:\go
# Wed, 13 Mar 2024 01:47:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Mar 2024 02:01:45 GMT
ENV GOLANG_VERSION=1.21.8
# Wed, 13 Mar 2024 02:04:07 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 02:04:09 GMT
WORKDIR C:\go
# Wed, 13 Mar 2024 02:40:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:40:13 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 13 Mar 2024 02:40:14 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:40:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 13 Mar 2024 02:40:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 13 Mar 2024 02:40:40 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0a2d972d6c007b69f2c3ea41c1fe5fad6b189bfe40efacdcaf910b884fb6bb`  
		Last Modified: Wed, 13 Mar 2024 02:13:35 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f3068df504cd61566fc5e038c996322e35f58e08e0c6ef6ce589b11de4eb93`  
		Last Modified: Wed, 13 Mar 2024 02:13:34 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98750f7d798b8a0b5199088d4860bce5d51320b2fc07440f211ec692f4bf63b4`  
		Last Modified: Wed, 13 Mar 2024 02:13:33 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e43d1ea980f98746869d1942fc459ed402f307d4de5c435e325d2c9d534e99`  
		Last Modified: Wed, 13 Mar 2024 02:13:33 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fc4a2ae5d19f3b766991bfec5347bd5192c19ede11e7dfbf8b7d698fc1323d`  
		Last Modified: Wed, 13 Mar 2024 02:13:38 GMT  
		Size: 25.6 MB (25551948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251908e7b1f95da24e9f4ec7c727a2662105696c9de2925ab36938572cfb9f79`  
		Last Modified: Wed, 13 Mar 2024 02:13:31 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2927b1ac917c6e3261034f1c0cbb347c73f26593e997c505dfd04da18f966c1a`  
		Last Modified: Wed, 13 Mar 2024 02:13:31 GMT  
		Size: 273.7 KB (273727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5d297a0f5c09416c27b06ff859cb837506ffabdf0faa0cb5112e0a34839aab`  
		Last Modified: Wed, 13 Mar 2024 02:15:44 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1412d17e78321071b9d6a4dbb609e6a24c2e829a90ed9ca7e20a72ede74d04`  
		Last Modified: Wed, 13 Mar 2024 02:16:03 GMT  
		Size: 69.4 MB (69363257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619eb2756fc98681ecf9e1220a72f64f2e3f3fe9e72edd3a6021ad0249b9b2a5`  
		Last Modified: Wed, 13 Mar 2024 02:15:44 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf19d565f6ad05c073e69610b1e850eaf1a6aa6806195ea601c4a47303140d27`  
		Last Modified: Wed, 13 Mar 2024 02:42:22 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279cafbdd3019482f630ef1d502ea930d8ee1cfd8f9977bb52059c87ddff7a55`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e9d1117318fed479ece2fe1c6f9b896efcca03021ea368d722153aca1f8bc9`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d106feccb912e361adb23c8a586aad6b6c8493698e3893f4b1a2cd40bdd03cb4`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e766bc3c556143c937c2d95209a8d6370902ee4f31471f2a35c4d7045d361af6`  
		Last Modified: Wed, 13 Mar 2024 02:42:20 GMT  
		Size: 1.7 MB (1676188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39236cd34ad31ef892f22ac798c76cb384eb17ff72d5881539cbee398708be72`  
		Last Modified: Wed, 13 Mar 2024 02:42:20 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:53d965e8f604060a1c65cdf2a722300b8ff2f7a36494b6c0ba0c315fc7ffd2c2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221957582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0daee73c43fffad7bf7cfb8399d58db63aaa5f6727affb62b8d370b9760df81f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 01:49:48 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Mar 2024 01:49:49 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Mar 2024 01:49:50 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Mar 2024 01:49:51 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Mar 2024 01:51:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 01:51:29 GMT
ENV GOPATH=C:\go
# Wed, 13 Mar 2024 01:52:49 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Mar 2024 02:04:28 GMT
ENV GOLANG_VERSION=1.21.8
# Wed, 13 Mar 2024 02:07:38 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 02:07:39 GMT
WORKDIR C:\go
# Wed, 13 Mar 2024 02:38:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:38:30 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 13 Mar 2024 02:38:31 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:38:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 13 Mar 2024 02:39:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 13 Mar 2024 02:39:54 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc39f00be83bc8d2b0e0f2123fce0278f495e47f8a969bf03ec57df5f98cbda`  
		Last Modified: Wed, 13 Mar 2024 02:14:08 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f8b9e441646ef17118a0d394fa50244ef70c9e053c5b7d33e648796c8df90e`  
		Last Modified: Wed, 13 Mar 2024 02:14:07 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8759cd20778bf436a14e59cb31806b28212fcd510d8de32d44e49a9f39656f3d`  
		Last Modified: Wed, 13 Mar 2024 02:14:06 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d99a22ebabf5f80d07ad166a24eace1c2fa31cef2566a179bfec0d6407513e`  
		Last Modified: Wed, 13 Mar 2024 02:14:06 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfdb963b4125b258828e1fbac783c993a6845ad94973fad173f5dd25be3c34b`  
		Last Modified: Wed, 13 Mar 2024 02:14:12 GMT  
		Size: 25.5 MB (25540238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae89960ac90d33a751006d43faf1cbd1309b448658a447bb19dddabdbee17a9`  
		Last Modified: Wed, 13 Mar 2024 02:14:04 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff0bdcb61a7230b8b00d6e08d739c64fc0342dc675ed99fe6d35885cf1aa369`  
		Last Modified: Wed, 13 Mar 2024 02:14:05 GMT  
		Size: 272.6 KB (272572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c052d4b938689fbc1637386d1e61efa391787bd8128ee6d093464bad09b0231`  
		Last Modified: Wed, 13 Mar 2024 02:16:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e82772a8bffddc9f4a46c65cfa48f47938d84feb3730231762158c98014e47a`  
		Last Modified: Wed, 13 Mar 2024 02:16:31 GMT  
		Size: 69.4 MB (69350702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbffcc4012ecf27a404cc40eb63c43a880ad5104a82ee619fd0669acb2b5a710`  
		Last Modified: Wed, 13 Mar 2024 02:16:12 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fcd0eeed9adb7d9bf391df7f194150cb8ee56a63bc679cf147a14185381c3b`  
		Last Modified: Wed, 13 Mar 2024 02:42:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d74d351932d9ba6c92c9398e69d6736df75938a6ba3b7f1055206a1ed80b48`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db51f1e77d8641618afadb6f8c1ad073c4f72bb79099a00b0cabcbc8f5579248`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43620705f408ca0a7894137080f7947cc45d10badb0c7668ae1d46464494001b`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdaa0771d9c8b704195f821c3a9c23a5d9ff5e7e9b29335b835ce237f9d4dd50`  
		Last Modified: Wed, 13 Mar 2024 02:42:03 GMT  
		Size: 1.7 MB (1676257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010496734b493d0bc1b1a73566306e98777144ff64c5c886cf84de3af4fd971b`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:8308bb619e5ff5bc1842b8fc8480bb1584220a0c241f125727fa844918aac505
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
$ docker pull caddy@sha256:a37704d2149bb703350b3e63704ecb468ec6f10cdc3784c818988e250484b2ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76973825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a6b943c698684ea914a9d08c8a00d2e573cbc2a95669142bc1b35350317cff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 03:18:55 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 03:18:55 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 03:18:55 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 03:18:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 03:18:55 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 03:18:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 03:18:57 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 03:18:57 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e791cb90c3d0bf08a988f13b405c9947c74b5bc31c7c939197a7175f6c7f0e`  
		Last Modified: Sat, 27 Jan 2024 01:36:33 GMT  
		Size: 284.7 KB (284690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3da9c61ef062502252a549dbc1f90925a8d7b6ef0644ffbfaea77be8b6f058`  
		Last Modified: Tue, 05 Mar 2024 19:25:57 GMT  
		Size: 67.0 MB (67010725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1741a7c0e9ce85801257b76332c08a3abdf5069bf46b0e764a32219d92189dc5`  
		Last Modified: Tue, 05 Mar 2024 19:25:45 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f302d3cc779898a1baa29b9dde46627021754a60a003a8ceb71b73f80af80bb2`  
		Last Modified: Sat, 16 Mar 2024 03:19:27 GMT  
		Size: 5.0 MB (4973021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51954c5f8bcd596606e74156291b16b5d0c2b430bb9f0a49db89dc03278cbd8e`  
		Last Modified: Sat, 16 Mar 2024 03:19:26 GMT  
		Size: 1.3 MB (1302235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351f34f77cd30086783b4d1e7bd91ac224af75f55690527012c4f114a65048b5`  
		Last Modified: Sat, 16 Mar 2024 03:19:26 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:042f6baf4a87f12037bf9a9146e994b03974edfdf6e94ef3a6c8ed9a5b0e01d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75407449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8104ab01bd342cfbbde6ad9a086efdba750ddaaeb6b4ce5acae4072b032808f1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 06:36:10 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 06:36:10 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 06:36:10 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 06:36:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 06:36:10 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 06:36:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 06:36:11 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 06:36:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18595ac3d5791e4d7e7dbcffcbf63e97e29974bd7191f7779889293f06709605`  
		Last Modified: Sat, 16 Mar 2024 01:27:12 GMT  
		Size: 284.9 KB (284879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67b0661c8b928f9ee07193e83a55962dc30ea03b3917d927fbfc6172db763d1`  
		Last Modified: Sat, 16 Mar 2024 01:28:25 GMT  
		Size: 65.8 MB (65767483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e94e3f035a7e84adb42051a6776fb957bb01e4afe261ef52850410749238c3e`  
		Last Modified: Sat, 16 Mar 2024 01:28:09 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90af61f594723149cbf4c52926248b7aa924edce2e71c1146dbfe1c4952d0e85`  
		Last Modified: Sat, 16 Mar 2024 06:36:39 GMT  
		Size: 5.0 MB (4958759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2b089f053b69b50a0ec1b57924c3f1dbab09af5f892a3f3824a1f1d91c4653`  
		Last Modified: Sat, 16 Mar 2024 06:36:39 GMT  
		Size: 1.2 MB (1248659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb3baf5a17563281d926d65bf039e75bafa0be92988b008e142f88f13e48831`  
		Last Modified: Sat, 16 Mar 2024 06:36:39 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:bba85446aa9cf082d96393b37ee2eb8948d32119f9f1b4a7de4264ed6265bc16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d75fc02eccf5b473914195c6b5a7f27a9c7b3af790feb14ca2afa4f0a1e6d2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 08:36:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 08:36:44 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 08:36:44 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 08:36:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 08:36:44 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 08:36:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 08:36:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 08:36:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03de95814623b83a4328b4db2e23b14214f57c18389a27379988469d9b6bbccc`  
		Last Modified: Sat, 16 Mar 2024 00:51:49 GMT  
		Size: 284.1 KB (284082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb316a6d2b1f8b686717aa026be6622630e91b4e2beff72260e41b9c26f5f328`  
		Last Modified: Sat, 16 Mar 2024 00:52:59 GMT  
		Size: 65.8 MB (65767446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3402119434a07f7977a54237330b21abbea9474c729d8bbbe43e79507612156`  
		Last Modified: Sat, 16 Mar 2024 00:52:46 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3e193cf2bcf63192347811ea80a7312b468b42f6341ff8912fb721dcdd07b1`  
		Last Modified: Sat, 16 Mar 2024 08:37:14 GMT  
		Size: 4.5 MB (4514679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302bab84b8a106df7129ce421df27645cf93461c26631a73c4c16dcc48213e33`  
		Last Modified: Sat, 16 Mar 2024 08:37:14 GMT  
		Size: 1.2 MB (1246087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa5da11b54d5792ea909f7bcbe533482069dd4540457779cb629671faadd4eb`  
		Last Modified: Sat, 16 Mar 2024 08:37:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:636495b6181fd6f900cfb1c3fafd4aa67ef8113e127a39c225dcd2b9f28018ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73993764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804083a23a5a42633ad7c22fc0b9908822db952792867afe4852db23de6882c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 02:55:47 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 02:55:48 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 02:55:48 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 02:55:48 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 02:55:48 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 02:55:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 02:55:49 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 02:55:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69c4102457739613c6fcb205a5a8e7dbc8383d57dade0a4502b1bca7b100a4d`  
		Last Modified: Sat, 16 Mar 2024 02:38:03 GMT  
		Size: 286.3 KB (286314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472e8443302a7aa2ee7c60f88cf1c1bff960c6982004fabf4d0b7dbb39552784`  
		Last Modified: Sat, 16 Mar 2024 02:38:55 GMT  
		Size: 64.1 MB (64111127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f3ae01babba08c7331e1311c66fc81f093559e9b48b75c7f09e492835df417`  
		Last Modified: Sat, 16 Mar 2024 02:38:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a47c8e46877caae3d8fa35784305f82b6173865f636c831581e413586174c9f`  
		Last Modified: Sat, 16 Mar 2024 02:56:14 GMT  
		Size: 5.1 MB (5063904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b458a517cc70120b5d5ad7b3624d14288f8fc2bb374503684e47dfb2d81ede41`  
		Last Modified: Sat, 16 Mar 2024 02:56:14 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e927a09144840e6a0520002506a03480353d2bf16acf387e392f67125a232f`  
		Last Modified: Sat, 16 Mar 2024 02:56:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:74036381f9b78d58ddddc74f279042dff06d05ac2b95c3faf063485eac603111
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74219852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afdeb2455afb0545182f73124c3e233abb4a6b803a834f42127d9a1eff4982c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 07:31:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 07:31:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 07:31:22 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 07:31:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 07:31:22 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 07:31:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 07:31:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 07:31:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e315e4c0ee7596e0eb7cc17d622c433e9fc4ef254b722e11e6794265328ea583`  
		Last Modified: Sat, 16 Mar 2024 00:32:12 GMT  
		Size: 286.7 KB (286670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee59a251903fa4e415f22830cd12da95ca1bcf671572b4a701a1d8f75a55d5ee`  
		Last Modified: Sat, 16 Mar 2024 00:33:15 GMT  
		Size: 64.1 MB (64126904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a227c25fca514ad52229d19315a3e0db7f235f9a840f9474237fadee44634bd1`  
		Last Modified: Sat, 16 Mar 2024 00:33:03 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da53f00025342b23cc1c1a712e9f3ff08b05bc0759f58b580a2081c4b925b9e8`  
		Last Modified: Sat, 16 Mar 2024 07:31:42 GMT  
		Size: 5.3 MB (5271003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1eb59d0f562ae579e22be9806e6ea172a7ee0399f354980329dfa3e8e04045`  
		Last Modified: Sat, 16 Mar 2024 07:31:41 GMT  
		Size: 1.2 MB (1186176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f27806532c2006d7f3b98c3ab37d72cf977ec4c488b65e389cb46e6b551627`  
		Last Modified: Sat, 16 Mar 2024 07:31:41 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:179342439e20a0f8308f5b3c8f51063386fb33fb38d9eda738dfd1d4b398280c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76101838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4eddf19e318b73f4fa90802285b549c08b6b015cfc8f36a11adbbf9c593fc2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Tue, 05 Mar 2024 20:58:12 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:58:12 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:58:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:58:13 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:58:13 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1b6899ff00172fd5c809d57028913a3c5aead2c05d0c3c01b15a5249c4ddec`  
		Last Modified: Sat, 27 Jan 2024 05:46:31 GMT  
		Size: 285.1 KB (285091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192deec459dbc25471d5ce96dbf84de90f9e77914e5074081b4aba0516977050`  
		Last Modified: Tue, 05 Mar 2024 20:12:42 GMT  
		Size: 66.2 MB (66218961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e6d46fb71afdd9825fc4397b4949daac74f5a564377560ed3cb3bb910da97f`  
		Last Modified: Tue, 05 Mar 2024 20:12:31 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad42b5ce4497969e7a2ebbdf9ada284081c50ce1744927873987c8075ed117fa`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 5.1 MB (5117256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea105a4685d829ffde13e2d0e06f02ec7f1e1381059eae15941a5aeb36d5f7a7`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 1.3 MB (1262390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1423e2dcf9499ee1179b946513f3194740bf64ee1f24d0a7688bde92f8773874`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:88480ae6cc843e1f4d7891d869f95182848a5414c6545cc2662d466a7c8dfdd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:53d965e8f604060a1c65cdf2a722300b8ff2f7a36494b6c0ba0c315fc7ffd2c2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221957582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0daee73c43fffad7bf7cfb8399d58db63aaa5f6727affb62b8d370b9760df81f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 01:49:48 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Mar 2024 01:49:49 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Mar 2024 01:49:50 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Mar 2024 01:49:51 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Mar 2024 01:51:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 01:51:29 GMT
ENV GOPATH=C:\go
# Wed, 13 Mar 2024 01:52:49 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Mar 2024 02:04:28 GMT
ENV GOLANG_VERSION=1.21.8
# Wed, 13 Mar 2024 02:07:38 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 02:07:39 GMT
WORKDIR C:\go
# Wed, 13 Mar 2024 02:38:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:38:30 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 13 Mar 2024 02:38:31 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:38:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 13 Mar 2024 02:39:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 13 Mar 2024 02:39:54 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc39f00be83bc8d2b0e0f2123fce0278f495e47f8a969bf03ec57df5f98cbda`  
		Last Modified: Wed, 13 Mar 2024 02:14:08 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f8b9e441646ef17118a0d394fa50244ef70c9e053c5b7d33e648796c8df90e`  
		Last Modified: Wed, 13 Mar 2024 02:14:07 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8759cd20778bf436a14e59cb31806b28212fcd510d8de32d44e49a9f39656f3d`  
		Last Modified: Wed, 13 Mar 2024 02:14:06 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d99a22ebabf5f80d07ad166a24eace1c2fa31cef2566a179bfec0d6407513e`  
		Last Modified: Wed, 13 Mar 2024 02:14:06 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfdb963b4125b258828e1fbac783c993a6845ad94973fad173f5dd25be3c34b`  
		Last Modified: Wed, 13 Mar 2024 02:14:12 GMT  
		Size: 25.5 MB (25540238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae89960ac90d33a751006d43faf1cbd1309b448658a447bb19dddabdbee17a9`  
		Last Modified: Wed, 13 Mar 2024 02:14:04 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff0bdcb61a7230b8b00d6e08d739c64fc0342dc675ed99fe6d35885cf1aa369`  
		Last Modified: Wed, 13 Mar 2024 02:14:05 GMT  
		Size: 272.6 KB (272572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c052d4b938689fbc1637386d1e61efa391787bd8128ee6d093464bad09b0231`  
		Last Modified: Wed, 13 Mar 2024 02:16:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e82772a8bffddc9f4a46c65cfa48f47938d84feb3730231762158c98014e47a`  
		Last Modified: Wed, 13 Mar 2024 02:16:31 GMT  
		Size: 69.4 MB (69350702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbffcc4012ecf27a404cc40eb63c43a880ad5104a82ee619fd0669acb2b5a710`  
		Last Modified: Wed, 13 Mar 2024 02:16:12 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fcd0eeed9adb7d9bf391df7f194150cb8ee56a63bc679cf147a14185381c3b`  
		Last Modified: Wed, 13 Mar 2024 02:42:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d74d351932d9ba6c92c9398e69d6736df75938a6ba3b7f1055206a1ed80b48`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db51f1e77d8641618afadb6f8c1ad073c4f72bb79099a00b0cabcbc8f5579248`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43620705f408ca0a7894137080f7947cc45d10badb0c7668ae1d46464494001b`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdaa0771d9c8b704195f821c3a9c23a5d9ff5e7e9b29335b835ce237f9d4dd50`  
		Last Modified: Wed, 13 Mar 2024 02:42:03 GMT  
		Size: 1.7 MB (1676257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010496734b493d0bc1b1a73566306e98777144ff64c5c886cf84de3af4fd971b`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:7904ec0c624b28630437b42e793d0e1bc2472c348c79b15b26d065162eafd9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:deed166abe77b412a506924346166c58e03f6e35fb2836e7af244be01925eddf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2054342050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7b95fb04081aaf80026e1bb52d4a79df79ea5aac969382123b16607318419f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 01:46:04 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Mar 2024 01:46:05 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Mar 2024 01:46:06 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Mar 2024 01:46:07 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Mar 2024 01:46:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 01:46:43 GMT
ENV GOPATH=C:\go
# Wed, 13 Mar 2024 01:47:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Mar 2024 02:01:45 GMT
ENV GOLANG_VERSION=1.21.8
# Wed, 13 Mar 2024 02:04:07 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 02:04:09 GMT
WORKDIR C:\go
# Wed, 13 Mar 2024 02:40:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:40:13 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 13 Mar 2024 02:40:14 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:40:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 13 Mar 2024 02:40:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 13 Mar 2024 02:40:40 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0a2d972d6c007b69f2c3ea41c1fe5fad6b189bfe40efacdcaf910b884fb6bb`  
		Last Modified: Wed, 13 Mar 2024 02:13:35 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f3068df504cd61566fc5e038c996322e35f58e08e0c6ef6ce589b11de4eb93`  
		Last Modified: Wed, 13 Mar 2024 02:13:34 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98750f7d798b8a0b5199088d4860bce5d51320b2fc07440f211ec692f4bf63b4`  
		Last Modified: Wed, 13 Mar 2024 02:13:33 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e43d1ea980f98746869d1942fc459ed402f307d4de5c435e325d2c9d534e99`  
		Last Modified: Wed, 13 Mar 2024 02:13:33 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fc4a2ae5d19f3b766991bfec5347bd5192c19ede11e7dfbf8b7d698fc1323d`  
		Last Modified: Wed, 13 Mar 2024 02:13:38 GMT  
		Size: 25.6 MB (25551948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251908e7b1f95da24e9f4ec7c727a2662105696c9de2925ab36938572cfb9f79`  
		Last Modified: Wed, 13 Mar 2024 02:13:31 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2927b1ac917c6e3261034f1c0cbb347c73f26593e997c505dfd04da18f966c1a`  
		Last Modified: Wed, 13 Mar 2024 02:13:31 GMT  
		Size: 273.7 KB (273727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5d297a0f5c09416c27b06ff859cb837506ffabdf0faa0cb5112e0a34839aab`  
		Last Modified: Wed, 13 Mar 2024 02:15:44 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1412d17e78321071b9d6a4dbb609e6a24c2e829a90ed9ca7e20a72ede74d04`  
		Last Modified: Wed, 13 Mar 2024 02:16:03 GMT  
		Size: 69.4 MB (69363257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619eb2756fc98681ecf9e1220a72f64f2e3f3fe9e72edd3a6021ad0249b9b2a5`  
		Last Modified: Wed, 13 Mar 2024 02:15:44 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf19d565f6ad05c073e69610b1e850eaf1a6aa6806195ea601c4a47303140d27`  
		Last Modified: Wed, 13 Mar 2024 02:42:22 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279cafbdd3019482f630ef1d502ea930d8ee1cfd8f9977bb52059c87ddff7a55`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e9d1117318fed479ece2fe1c6f9b896efcca03021ea368d722153aca1f8bc9`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d106feccb912e361adb23c8a586aad6b6c8493698e3893f4b1a2cd40bdd03cb4`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e766bc3c556143c937c2d95209a8d6370902ee4f31471f2a35c4d7045d361af6`  
		Last Modified: Wed, 13 Mar 2024 02:42:20 GMT  
		Size: 1.7 MB (1676188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39236cd34ad31ef892f22ac798c76cb384eb17ff72d5881539cbee398708be72`  
		Last Modified: Wed, 13 Mar 2024 02:42:20 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:02e4ec422a43bbe257c0b6f52bc54f9e391ac2ed078f86fc4d80269ca8ef3533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `caddy:2-windowsservercore` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:e92a98f9befbcc685cba6014745c4c4e5573d524f98646666afae41fe635a647
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1973514153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c02263e4345786d822a7cbe2109be66b8bbc405dad0088432e203c583cdb8c4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:37:25 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:37:26 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:37:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:37:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:37:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:37:54 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:37:55 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:37:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:37:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:37:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:38:00 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:38:01 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:38:03 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:38:21 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:38:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3433f0cddf0bf50f831ae26d44034fb9ccdaea63173630b59cbe9dc33860a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:45 GMT  
		Size: 471.5 KB (471467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39aa89107a4c1ac15acc37ba98faa00f98774062e839984cd569c84acccbefa`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903c57abacc03a4132d1914d83b140d91cad6d3f72113588dbb0449668e5459e`  
		Last Modified: Wed, 13 Mar 2024 02:41:47 GMT  
		Size: 15.3 MB (15272331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c505d8db5c54f9f5b13a230f310c78e1daa9f0fa5baa7db6bb4b6f9b2824c64`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02c7783ff4e4ea0351aa496f9316d007b5d39dd7ac091772a53c788cc850835`  
		Last Modified: Wed, 13 Mar 2024 02:41:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2f6f475cd8b631685eb3441f13c0418b595dc3f64fc43f4de103cd270bd07a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c099338186092d8e8a9ee4e1aef2ac6bac6e0e37d05b00acc2519d4828eebc1a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66be30fd26f10adf7753fc7287726b290417f432503173cc8cfcc37c5970eed5`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdecded462eba57ac719ddeaf73027953397d9470c8d9ce91486b650688448d1`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b196924a8268e867bced4e92552ad7a24d5079dd5d3a5f2d32e98acf5b94ec`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83e0533daa0143428320795f95f747a318ce9dfaec9c1918dc09ddabff7ce6`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d6f7d580438b0f330c60e990071ee0a7fd2cb8e861b5b3673229aae5f40a97`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3043316cf0d3543d7ad8c2cf29b9f42217a7ff7ee358b9ccf49ec1c2742b40dc`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9d07b35dd72d9c89f56d604b5b5ff1096607de0b699a7845b4d4eef4542999`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7138f2320f3eb26befb56422d151646fa73d61b45b1fd7ba1a97e97b12b1794`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dd6eb25db87e92a30fe3a646b0ca820c3a8a855af39f49e9c1239e9e7e8fa8`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff49c00e60e2791dac19058d6bba6e562c80b90859f8e91ae70b474a582042`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c28453d92f8177a5ca4103ba031b5f02ceb70269930e8642e8bda358f1eef11`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 289.3 KB (289264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5958cc3ab872a13ea8011a1ae0a2290cefbfb5721bf58c5c16e2a1dfa216aa`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:2a10673838e2beefb539398925457319c1e7800b242f5c261bc40ddd7f16aa33
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2141123401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001b000d65334996d09969a3e79ce6304b5ea6811c67eb7add59f0c78b73ba5c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:34:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:34:08 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:35:29 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:35:30 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:35:31 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:35:31 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:35:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:35:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:35:35 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:35:36 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:35:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:35:39 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:35:40 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:36:47 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:36:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bb323765ff7b405cedec6f88daa8a1c8470f45c358d637c0062cf4c63d7e07`  
		Last Modified: Wed, 13 Mar 2024 02:41:21 GMT  
		Size: 465.6 KB (465620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b3f11ec4ee425a6a0b9f5ad200c9193592181f59520c9a80372e647787163a`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ffe491a522455b1d95c1d0d3384188ea361064259fffcadd657bebae4fa934`  
		Last Modified: Wed, 13 Mar 2024 02:41:24 GMT  
		Size: 15.3 MB (15277213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b62af40926c0d1a37e6126f41f63533166809b5b54434cf3b53ab5734357e59`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a9b1639ec2e8588ca4fd94f87b31b4e30adef3c0ac45ea4ac0e4cdce643d6`  
		Last Modified: Wed, 13 Mar 2024 02:41:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7a48958fcb11d52bb7a65f60d6f322d3326d4f2916e0547b764cbe4fe0eae8`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9eb36d28260e8ba5549b16a87d121a4d7b0d38f46e1127ee1fd95f2e31e6f2c`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d221a46e4e966da289289be19ac425d0199540bef1d6d7c890ba45ec255e79`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feeda3213337ce81d383bcb08c0b241e763185b91a2e180f35c59395e3c0290f`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d7bf5ae3a283a09c7a385afa5160b2d0f1d275fc23e0a1711bf734511fe0b1`  
		Last Modified: Wed, 13 Mar 2024 02:41:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f309d19b55289fe422d64dd24736be59a52f6eba872d8fb1054416f8b5d9c553`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4ac1a4021eeee54512dde50b437001408fd1dda9d896f68d38728f7dba8c6c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e117655b528b6e8f7ce8d4d2cb69d41a1735fec0e31e10dc40cddcf0d012be`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5524c6d618843e710fa22d77e57a844c7cdfd68676c809d2d1ecde656c16a81c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879784be55be2c5d212302ae42232de9bfeaccea0b1398ec0101ef36d542930c`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f8aadcc42505eea344cf0504c7312d01033f159e88d6eadab5abb9eefc98a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41580c6cc25a82ee1a4de9315ec98ce6e89bd73461a941248648d04292e9ff52`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1261dc2b6b686493c5c3989f8efdd404b912398f6a38933aba80fe65d5d6240c`  
		Last Modified: Wed, 13 Mar 2024 02:41:15 GMT  
		Size: 258.2 KB (258159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8856855cc09ca543e8712766ea12d12556af369305babcaf786f620c89c3450d`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:3e51c662d70a2bcf344a51331fb88b7d223db9cc683b01463633782351400cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:2a10673838e2beefb539398925457319c1e7800b242f5c261bc40ddd7f16aa33
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2141123401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001b000d65334996d09969a3e79ce6304b5ea6811c67eb7add59f0c78b73ba5c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:34:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:34:08 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:35:29 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:35:30 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:35:31 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:35:31 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:35:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:35:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:35:35 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:35:36 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:35:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:35:39 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:35:40 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:36:47 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:36:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bb323765ff7b405cedec6f88daa8a1c8470f45c358d637c0062cf4c63d7e07`  
		Last Modified: Wed, 13 Mar 2024 02:41:21 GMT  
		Size: 465.6 KB (465620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b3f11ec4ee425a6a0b9f5ad200c9193592181f59520c9a80372e647787163a`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ffe491a522455b1d95c1d0d3384188ea361064259fffcadd657bebae4fa934`  
		Last Modified: Wed, 13 Mar 2024 02:41:24 GMT  
		Size: 15.3 MB (15277213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b62af40926c0d1a37e6126f41f63533166809b5b54434cf3b53ab5734357e59`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a9b1639ec2e8588ca4fd94f87b31b4e30adef3c0ac45ea4ac0e4cdce643d6`  
		Last Modified: Wed, 13 Mar 2024 02:41:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7a48958fcb11d52bb7a65f60d6f322d3326d4f2916e0547b764cbe4fe0eae8`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9eb36d28260e8ba5549b16a87d121a4d7b0d38f46e1127ee1fd95f2e31e6f2c`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d221a46e4e966da289289be19ac425d0199540bef1d6d7c890ba45ec255e79`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feeda3213337ce81d383bcb08c0b241e763185b91a2e180f35c59395e3c0290f`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d7bf5ae3a283a09c7a385afa5160b2d0f1d275fc23e0a1711bf734511fe0b1`  
		Last Modified: Wed, 13 Mar 2024 02:41:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f309d19b55289fe422d64dd24736be59a52f6eba872d8fb1054416f8b5d9c553`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4ac1a4021eeee54512dde50b437001408fd1dda9d896f68d38728f7dba8c6c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e117655b528b6e8f7ce8d4d2cb69d41a1735fec0e31e10dc40cddcf0d012be`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5524c6d618843e710fa22d77e57a844c7cdfd68676c809d2d1ecde656c16a81c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879784be55be2c5d212302ae42232de9bfeaccea0b1398ec0101ef36d542930c`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f8aadcc42505eea344cf0504c7312d01033f159e88d6eadab5abb9eefc98a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41580c6cc25a82ee1a4de9315ec98ce6e89bd73461a941248648d04292e9ff52`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1261dc2b6b686493c5c3989f8efdd404b912398f6a38933aba80fe65d5d6240c`  
		Last Modified: Wed, 13 Mar 2024 02:41:15 GMT  
		Size: 258.2 KB (258159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8856855cc09ca543e8712766ea12d12556af369305babcaf786f620c89c3450d`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:e56fe39382d5d420f2ca9e2758ad977fc5a521e371d1658d8f98d8fd55615b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:e92a98f9befbcc685cba6014745c4c4e5573d524f98646666afae41fe635a647
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1973514153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c02263e4345786d822a7cbe2109be66b8bbc405dad0088432e203c583cdb8c4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:37:25 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:37:26 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:37:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:37:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:37:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:37:54 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:37:55 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:37:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:37:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:37:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:38:00 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:38:01 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:38:03 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:38:21 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:38:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3433f0cddf0bf50f831ae26d44034fb9ccdaea63173630b59cbe9dc33860a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:45 GMT  
		Size: 471.5 KB (471467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39aa89107a4c1ac15acc37ba98faa00f98774062e839984cd569c84acccbefa`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903c57abacc03a4132d1914d83b140d91cad6d3f72113588dbb0449668e5459e`  
		Last Modified: Wed, 13 Mar 2024 02:41:47 GMT  
		Size: 15.3 MB (15272331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c505d8db5c54f9f5b13a230f310c78e1daa9f0fa5baa7db6bb4b6f9b2824c64`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02c7783ff4e4ea0351aa496f9316d007b5d39dd7ac091772a53c788cc850835`  
		Last Modified: Wed, 13 Mar 2024 02:41:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2f6f475cd8b631685eb3441f13c0418b595dc3f64fc43f4de103cd270bd07a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c099338186092d8e8a9ee4e1aef2ac6bac6e0e37d05b00acc2519d4828eebc1a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66be30fd26f10adf7753fc7287726b290417f432503173cc8cfcc37c5970eed5`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdecded462eba57ac719ddeaf73027953397d9470c8d9ce91486b650688448d1`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b196924a8268e867bced4e92552ad7a24d5079dd5d3a5f2d32e98acf5b94ec`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83e0533daa0143428320795f95f747a318ce9dfaec9c1918dc09ddabff7ce6`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d6f7d580438b0f330c60e990071ee0a7fd2cb8e861b5b3673229aae5f40a97`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3043316cf0d3543d7ad8c2cf29b9f42217a7ff7ee358b9ccf49ec1c2742b40dc`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9d07b35dd72d9c89f56d604b5b5ff1096607de0b699a7845b4d4eef4542999`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7138f2320f3eb26befb56422d151646fa73d61b45b1fd7ba1a97e97b12b1794`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dd6eb25db87e92a30fe3a646b0ca820c3a8a855af39f49e9c1239e9e7e8fa8`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff49c00e60e2791dac19058d6bba6e562c80b90859f8e91ae70b474a582042`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c28453d92f8177a5ca4103ba031b5f02ceb70269930e8642e8bda358f1eef11`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 289.3 KB (289264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5958cc3ab872a13ea8011a1ae0a2290cefbfb5721bf58c5c16e2a1dfa216aa`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7`

```console
$ docker pull caddy@sha256:ce43091c481420028215c752115f25e501155b055ae9f4862bae373bda4c1308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `caddy:2.7` - linux; amd64

```console
$ docker pull caddy@sha256:a6054d207060158cd0f019d6a35907bf47d1f8dacf58cdb63075a930d8ebca38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18467348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da4af4af9d73e970be3df873e00b8e658a7fc56ab982bfffa21d9bae68e3943`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:18:44 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 03:18:46 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 03:18:46 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 03:18:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 03:18:48 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 03:18:48 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 03:18:48 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 03:18:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 03:18:48 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 80
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 443
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 03:18:49 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 03:18:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a167b92bd92ca649523209f279d023d90edd2658f2dbbd5a79cd991b707a1bf4`  
		Last Modified: Sat, 16 Mar 2024 03:19:12 GMT  
		Size: 350.8 KB (350841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa65d2923419d52c79891c5c107216c8efc7534f740cafcddcb57fcd915fd61`  
		Last Modified: Sat, 16 Mar 2024 03:19:12 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832dc3f423aedf5c58d59571f7e5eebd543b4c31f0a0bacc36b509313473765e`  
		Last Modified: Sat, 16 Mar 2024 03:19:15 GMT  
		Size: 14.7 MB (14706436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - linux; arm variant v6

```console
$ docker pull caddy@sha256:d5b956705aa5cb2d80a34b0da959c62f6e1b85d3b6af5d39bdd43a5ebad79732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17423235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637ed474101820123d027bf07c3bacd795eec60a114ec44aa0ab7c081f03fcdd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:36:00 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 06:36:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 06:36:01 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 06:36:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 06:36:04 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 06:36:04 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 06:36:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 06:36:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 06:36:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 80
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 443
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 06:36:05 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 06:36:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7e837cfa426b2a8d095055ea95ecda50deb35a29395410997280bf4efa14be`  
		Last Modified: Sat, 16 Mar 2024 06:36:25 GMT  
		Size: 347.6 KB (347629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aac6695e2937791ffb389edf1aee134b4e2e7c879173c70c5b0851017f402f5`  
		Last Modified: Sat, 16 Mar 2024 06:36:24 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a5dfabcee2609d8f2199b85fef83d4b0fa6612faa5a74b40f2809ccef87a5d`  
		Last Modified: Sat, 16 Mar 2024 06:36:27 GMT  
		Size: 13.9 MB (13921018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - linux; arm variant v7

```console
$ docker pull caddy@sha256:d193bf8cf22c67a72ca3f4bc784363a0964ee0bc6481457a375beff0c515bb7b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17147117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c56baf0ceba318c0b5f456a51c90a5291492d8586689fa76bc097b01b50d670`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:36:34 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 08:36:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 08:36:35 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 08:36:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 08:36:38 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 08:36:38 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 08:36:38 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 08:36:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 08:36:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 80
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 443
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 08:36:39 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 08:36:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ad552b06977a907a460096cd3aa8d4cad657ae3a90be3bc63eba494b31a255`  
		Last Modified: Sat, 16 Mar 2024 08:36:59 GMT  
		Size: 344.5 KB (344462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7eb11427d968ddc8915316bd59544b644278fd1c3960927ab066c8cc916a8b`  
		Last Modified: Sat, 16 Mar 2024 08:36:58 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a13a58310f383c1986a52280e47b5d9a59f7ef7f02bf39ff3b494af779dab9`  
		Last Modified: Sat, 16 Mar 2024 08:37:02 GMT  
		Size: 13.9 MB (13893734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:aaf3497a43eee2656c636b04c5ac7dd7f81e15e6911be1c0509fcc51df3e6dbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f62720e336d430f97f77dea70bb3ceacea271cb1d7f6a246eb3c366e509827`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:55:39 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 02:55:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 02:55:41 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 02:55:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 02:55:43 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 02:55:43 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 02:55:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 80
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 443
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 02:55:44 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 02:55:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef488aa53de475202749fc28d385b1e4e59841fe4085a7edee2eb5026d11b95c`  
		Last Modified: Sat, 16 Mar 2024 02:56:01 GMT  
		Size: 360.7 KB (360666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322174feb81fda6e9c1e8e8ac7e49b8e77de2dca870243af972ee7545d4b7916`  
		Last Modified: Sat, 16 Mar 2024 02:56:01 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3360e007ed3153df2f6fbc7ef89943b1fc701d62c811d8855293b7df0f352d`  
		Last Modified: Sat, 16 Mar 2024 02:56:02 GMT  
		Size: 13.6 MB (13568947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - linux; ppc64le

```console
$ docker pull caddy@sha256:00e289b4657ffa0aec2c98f544cf7890e6cf6e4bd9dd1adfc01697d5fbb436a6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17052079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717f7ea5ec28ca8fed34729b1466cd1f5f96309057a0ec85b2e903833000f9ac`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:55:44 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 15 Mar 2024 23:55:46 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 15 Mar 2024 23:55:47 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 15 Mar 2024 23:55:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 15 Mar 2024 23:55:51 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 15 Mar 2024 23:55:51 GMT
ENV XDG_DATA_HOME=/data
# Fri, 15 Mar 2024 23:55:52 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 15 Mar 2024 23:55:52 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 15 Mar 2024 23:55:52 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 15 Mar 2024 23:55:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 15 Mar 2024 23:55:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 15 Mar 2024 23:55:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 15 Mar 2024 23:55:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 15 Mar 2024 23:55:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 15 Mar 2024 23:55:54 GMT
EXPOSE 80
# Fri, 15 Mar 2024 23:55:55 GMT
EXPOSE 443
# Fri, 15 Mar 2024 23:55:55 GMT
EXPOSE 443/udp
# Fri, 15 Mar 2024 23:55:55 GMT
EXPOSE 2019
# Fri, 15 Mar 2024 23:55:56 GMT
WORKDIR /srv
# Fri, 15 Mar 2024 23:55:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d58b091eab1c134ec71c79ecd145766a6b85840017d1e2223575349179f742c`  
		Last Modified: Fri, 15 Mar 2024 23:56:22 GMT  
		Size: 362.2 KB (362200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cfe42e2461424bcaa647db536a9454b1c48bf3410add89e0ec0367328cff78`  
		Last Modified: Fri, 15 Mar 2024 23:56:22 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103d176f7ec2158a797ee8c4909124a9a7cc2b8cff9b8c59e7368d8730563728`  
		Last Modified: Fri, 15 Mar 2024 23:56:24 GMT  
		Size: 13.3 MB (13333863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - linux; s390x

```console
$ docker pull caddy@sha256:aabd334d2f437365b8585670694b9cbe711132d5937a3d7f14b5840ff92fbf55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17818312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dd63d90fd552a57206bdfb4bb41bc51fd60b881c3ffe41f0852c6bac9ef68e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:48:00 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 04:48:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 04:48:01 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 04:48:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 04:48:04 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 04:48:04 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 04:48:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 04:48:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 04:48:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 04:48:05 GMT
EXPOSE 80
# Sat, 27 Jan 2024 04:48:05 GMT
EXPOSE 443
# Sat, 27 Jan 2024 04:48:05 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 04:48:06 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 04:48:06 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 04:48:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e608a3e3404a06a0444cc06a7949f9a4a2c56e2983aced16d2d32f009f2dbc17`  
		Last Modified: Sat, 27 Jan 2024 04:50:42 GMT  
		Size: 354.9 KB (354944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addd52ad78c14ade7e55ee491d32b0e51556e0c0a8b84d1fd1abc3a1430cc057`  
		Last Modified: Sat, 27 Jan 2024 04:50:42 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e597a1de66b259ef54ca1d052f65d662a6ea3ebf545513d9c91e80c67aa1f3`  
		Last Modified: Sat, 27 Jan 2024 04:50:44 GMT  
		Size: 14.2 MB (14238310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:e92a98f9befbcc685cba6014745c4c4e5573d524f98646666afae41fe635a647
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1973514153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c02263e4345786d822a7cbe2109be66b8bbc405dad0088432e203c583cdb8c4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:37:25 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:37:26 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:37:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:37:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:37:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:37:54 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:37:55 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:37:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:37:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:37:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:38:00 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:38:01 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:38:03 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:38:21 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:38:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3433f0cddf0bf50f831ae26d44034fb9ccdaea63173630b59cbe9dc33860a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:45 GMT  
		Size: 471.5 KB (471467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39aa89107a4c1ac15acc37ba98faa00f98774062e839984cd569c84acccbefa`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903c57abacc03a4132d1914d83b140d91cad6d3f72113588dbb0449668e5459e`  
		Last Modified: Wed, 13 Mar 2024 02:41:47 GMT  
		Size: 15.3 MB (15272331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c505d8db5c54f9f5b13a230f310c78e1daa9f0fa5baa7db6bb4b6f9b2824c64`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02c7783ff4e4ea0351aa496f9316d007b5d39dd7ac091772a53c788cc850835`  
		Last Modified: Wed, 13 Mar 2024 02:41:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2f6f475cd8b631685eb3441f13c0418b595dc3f64fc43f4de103cd270bd07a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c099338186092d8e8a9ee4e1aef2ac6bac6e0e37d05b00acc2519d4828eebc1a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66be30fd26f10adf7753fc7287726b290417f432503173cc8cfcc37c5970eed5`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdecded462eba57ac719ddeaf73027953397d9470c8d9ce91486b650688448d1`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b196924a8268e867bced4e92552ad7a24d5079dd5d3a5f2d32e98acf5b94ec`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83e0533daa0143428320795f95f747a318ce9dfaec9c1918dc09ddabff7ce6`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d6f7d580438b0f330c60e990071ee0a7fd2cb8e861b5b3673229aae5f40a97`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3043316cf0d3543d7ad8c2cf29b9f42217a7ff7ee358b9ccf49ec1c2742b40dc`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9d07b35dd72d9c89f56d604b5b5ff1096607de0b699a7845b4d4eef4542999`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7138f2320f3eb26befb56422d151646fa73d61b45b1fd7ba1a97e97b12b1794`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dd6eb25db87e92a30fe3a646b0ca820c3a8a855af39f49e9c1239e9e7e8fa8`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff49c00e60e2791dac19058d6bba6e562c80b90859f8e91ae70b474a582042`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c28453d92f8177a5ca4103ba031b5f02ceb70269930e8642e8bda358f1eef11`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 289.3 KB (289264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5958cc3ab872a13ea8011a1ae0a2290cefbfb5721bf58c5c16e2a1dfa216aa`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:2a10673838e2beefb539398925457319c1e7800b242f5c261bc40ddd7f16aa33
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2141123401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001b000d65334996d09969a3e79ce6304b5ea6811c67eb7add59f0c78b73ba5c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:34:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:34:08 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:35:29 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:35:30 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:35:31 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:35:31 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:35:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:35:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:35:35 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:35:36 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:35:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:35:39 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:35:40 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:36:47 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:36:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bb323765ff7b405cedec6f88daa8a1c8470f45c358d637c0062cf4c63d7e07`  
		Last Modified: Wed, 13 Mar 2024 02:41:21 GMT  
		Size: 465.6 KB (465620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b3f11ec4ee425a6a0b9f5ad200c9193592181f59520c9a80372e647787163a`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ffe491a522455b1d95c1d0d3384188ea361064259fffcadd657bebae4fa934`  
		Last Modified: Wed, 13 Mar 2024 02:41:24 GMT  
		Size: 15.3 MB (15277213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b62af40926c0d1a37e6126f41f63533166809b5b54434cf3b53ab5734357e59`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a9b1639ec2e8588ca4fd94f87b31b4e30adef3c0ac45ea4ac0e4cdce643d6`  
		Last Modified: Wed, 13 Mar 2024 02:41:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7a48958fcb11d52bb7a65f60d6f322d3326d4f2916e0547b764cbe4fe0eae8`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9eb36d28260e8ba5549b16a87d121a4d7b0d38f46e1127ee1fd95f2e31e6f2c`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d221a46e4e966da289289be19ac425d0199540bef1d6d7c890ba45ec255e79`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feeda3213337ce81d383bcb08c0b241e763185b91a2e180f35c59395e3c0290f`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d7bf5ae3a283a09c7a385afa5160b2d0f1d275fc23e0a1711bf734511fe0b1`  
		Last Modified: Wed, 13 Mar 2024 02:41:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f309d19b55289fe422d64dd24736be59a52f6eba872d8fb1054416f8b5d9c553`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4ac1a4021eeee54512dde50b437001408fd1dda9d896f68d38728f7dba8c6c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e117655b528b6e8f7ce8d4d2cb69d41a1735fec0e31e10dc40cddcf0d012be`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5524c6d618843e710fa22d77e57a844c7cdfd68676c809d2d1ecde656c16a81c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879784be55be2c5d212302ae42232de9bfeaccea0b1398ec0101ef36d542930c`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f8aadcc42505eea344cf0504c7312d01033f159e88d6eadab5abb9eefc98a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41580c6cc25a82ee1a4de9315ec98ce6e89bd73461a941248648d04292e9ff52`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1261dc2b6b686493c5c3989f8efdd404b912398f6a38933aba80fe65d5d6240c`  
		Last Modified: Wed, 13 Mar 2024 02:41:15 GMT  
		Size: 258.2 KB (258159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8856855cc09ca543e8712766ea12d12556af369305babcaf786f620c89c3450d`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-alpine`

```console
$ docker pull caddy@sha256:dda81a416214d4dbdd978810efa19643e39b626fe0f979558fbb116758784c89
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
$ docker pull caddy@sha256:a6054d207060158cd0f019d6a35907bf47d1f8dacf58cdb63075a930d8ebca38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18467348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da4af4af9d73e970be3df873e00b8e658a7fc56ab982bfffa21d9bae68e3943`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:18:44 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 03:18:46 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 03:18:46 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 03:18:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 03:18:48 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 03:18:48 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 03:18:48 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 03:18:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 03:18:48 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 80
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 443
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 03:18:49 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 03:18:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a167b92bd92ca649523209f279d023d90edd2658f2dbbd5a79cd991b707a1bf4`  
		Last Modified: Sat, 16 Mar 2024 03:19:12 GMT  
		Size: 350.8 KB (350841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa65d2923419d52c79891c5c107216c8efc7534f740cafcddcb57fcd915fd61`  
		Last Modified: Sat, 16 Mar 2024 03:19:12 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832dc3f423aedf5c58d59571f7e5eebd543b4c31f0a0bacc36b509313473765e`  
		Last Modified: Sat, 16 Mar 2024 03:19:15 GMT  
		Size: 14.7 MB (14706436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:d5b956705aa5cb2d80a34b0da959c62f6e1b85d3b6af5d39bdd43a5ebad79732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17423235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637ed474101820123d027bf07c3bacd795eec60a114ec44aa0ab7c081f03fcdd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:36:00 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 06:36:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 06:36:01 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 06:36:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 06:36:04 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 06:36:04 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 06:36:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 06:36:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 06:36:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 80
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 443
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 06:36:05 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 06:36:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7e837cfa426b2a8d095055ea95ecda50deb35a29395410997280bf4efa14be`  
		Last Modified: Sat, 16 Mar 2024 06:36:25 GMT  
		Size: 347.6 KB (347629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aac6695e2937791ffb389edf1aee134b4e2e7c879173c70c5b0851017f402f5`  
		Last Modified: Sat, 16 Mar 2024 06:36:24 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a5dfabcee2609d8f2199b85fef83d4b0fa6612faa5a74b40f2809ccef87a5d`  
		Last Modified: Sat, 16 Mar 2024 06:36:27 GMT  
		Size: 13.9 MB (13921018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:d193bf8cf22c67a72ca3f4bc784363a0964ee0bc6481457a375beff0c515bb7b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17147117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c56baf0ceba318c0b5f456a51c90a5291492d8586689fa76bc097b01b50d670`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:36:34 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 08:36:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 08:36:35 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 08:36:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 08:36:38 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 08:36:38 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 08:36:38 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 08:36:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 08:36:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 80
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 443
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 08:36:39 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 08:36:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ad552b06977a907a460096cd3aa8d4cad657ae3a90be3bc63eba494b31a255`  
		Last Modified: Sat, 16 Mar 2024 08:36:59 GMT  
		Size: 344.5 KB (344462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7eb11427d968ddc8915316bd59544b644278fd1c3960927ab066c8cc916a8b`  
		Last Modified: Sat, 16 Mar 2024 08:36:58 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a13a58310f383c1986a52280e47b5d9a59f7ef7f02bf39ff3b494af779dab9`  
		Last Modified: Sat, 16 Mar 2024 08:37:02 GMT  
		Size: 13.9 MB (13893734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:aaf3497a43eee2656c636b04c5ac7dd7f81e15e6911be1c0509fcc51df3e6dbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f62720e336d430f97f77dea70bb3ceacea271cb1d7f6a246eb3c366e509827`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:55:39 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 02:55:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 02:55:41 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 02:55:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 02:55:43 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 02:55:43 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 02:55:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 80
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 443
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 02:55:44 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 02:55:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef488aa53de475202749fc28d385b1e4e59841fe4085a7edee2eb5026d11b95c`  
		Last Modified: Sat, 16 Mar 2024 02:56:01 GMT  
		Size: 360.7 KB (360666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322174feb81fda6e9c1e8e8ac7e49b8e77de2dca870243af972ee7545d4b7916`  
		Last Modified: Sat, 16 Mar 2024 02:56:01 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3360e007ed3153df2f6fbc7ef89943b1fc701d62c811d8855293b7df0f352d`  
		Last Modified: Sat, 16 Mar 2024 02:56:02 GMT  
		Size: 13.6 MB (13568947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:00e289b4657ffa0aec2c98f544cf7890e6cf6e4bd9dd1adfc01697d5fbb436a6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17052079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717f7ea5ec28ca8fed34729b1466cd1f5f96309057a0ec85b2e903833000f9ac`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:55:44 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 15 Mar 2024 23:55:46 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 15 Mar 2024 23:55:47 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 15 Mar 2024 23:55:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 15 Mar 2024 23:55:51 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 15 Mar 2024 23:55:51 GMT
ENV XDG_DATA_HOME=/data
# Fri, 15 Mar 2024 23:55:52 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 15 Mar 2024 23:55:52 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 15 Mar 2024 23:55:52 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 15 Mar 2024 23:55:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 15 Mar 2024 23:55:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 15 Mar 2024 23:55:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 15 Mar 2024 23:55:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 15 Mar 2024 23:55:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 15 Mar 2024 23:55:54 GMT
EXPOSE 80
# Fri, 15 Mar 2024 23:55:55 GMT
EXPOSE 443
# Fri, 15 Mar 2024 23:55:55 GMT
EXPOSE 443/udp
# Fri, 15 Mar 2024 23:55:55 GMT
EXPOSE 2019
# Fri, 15 Mar 2024 23:55:56 GMT
WORKDIR /srv
# Fri, 15 Mar 2024 23:55:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d58b091eab1c134ec71c79ecd145766a6b85840017d1e2223575349179f742c`  
		Last Modified: Fri, 15 Mar 2024 23:56:22 GMT  
		Size: 362.2 KB (362200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cfe42e2461424bcaa647db536a9454b1c48bf3410add89e0ec0367328cff78`  
		Last Modified: Fri, 15 Mar 2024 23:56:22 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103d176f7ec2158a797ee8c4909124a9a7cc2b8cff9b8c59e7368d8730563728`  
		Last Modified: Fri, 15 Mar 2024 23:56:24 GMT  
		Size: 13.3 MB (13333863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:aabd334d2f437365b8585670694b9cbe711132d5937a3d7f14b5840ff92fbf55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17818312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dd63d90fd552a57206bdfb4bb41bc51fd60b881c3ffe41f0852c6bac9ef68e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:48:00 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 04:48:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 04:48:01 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 04:48:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 04:48:04 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 04:48:04 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 04:48:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 04:48:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 04:48:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 04:48:05 GMT
EXPOSE 80
# Sat, 27 Jan 2024 04:48:05 GMT
EXPOSE 443
# Sat, 27 Jan 2024 04:48:05 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 04:48:06 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 04:48:06 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 04:48:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e608a3e3404a06a0444cc06a7949f9a4a2c56e2983aced16d2d32f009f2dbc17`  
		Last Modified: Sat, 27 Jan 2024 04:50:42 GMT  
		Size: 354.9 KB (354944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addd52ad78c14ade7e55ee491d32b0e51556e0c0a8b84d1fd1abc3a1430cc057`  
		Last Modified: Sat, 27 Jan 2024 04:50:42 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e597a1de66b259ef54ca1d052f65d662a6ea3ebf545513d9c91e80c67aa1f3`  
		Last Modified: Sat, 27 Jan 2024 04:50:44 GMT  
		Size: 14.2 MB (14238310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder`

```console
$ docker pull caddy@sha256:297a97b4f8f3f4467bcf9cfd5a6f5ba5bcfa38be56824c82e2c4f1c029701f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `caddy:2.7-builder` - linux; amd64

```console
$ docker pull caddy@sha256:a37704d2149bb703350b3e63704ecb468ec6f10cdc3784c818988e250484b2ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76973825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a6b943c698684ea914a9d08c8a00d2e573cbc2a95669142bc1b35350317cff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 03:18:55 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 03:18:55 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 03:18:55 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 03:18:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 03:18:55 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 03:18:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 03:18:57 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 03:18:57 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e791cb90c3d0bf08a988f13b405c9947c74b5bc31c7c939197a7175f6c7f0e`  
		Last Modified: Sat, 27 Jan 2024 01:36:33 GMT  
		Size: 284.7 KB (284690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3da9c61ef062502252a549dbc1f90925a8d7b6ef0644ffbfaea77be8b6f058`  
		Last Modified: Tue, 05 Mar 2024 19:25:57 GMT  
		Size: 67.0 MB (67010725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1741a7c0e9ce85801257b76332c08a3abdf5069bf46b0e764a32219d92189dc5`  
		Last Modified: Tue, 05 Mar 2024 19:25:45 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f302d3cc779898a1baa29b9dde46627021754a60a003a8ceb71b73f80af80bb2`  
		Last Modified: Sat, 16 Mar 2024 03:19:27 GMT  
		Size: 5.0 MB (4973021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51954c5f8bcd596606e74156291b16b5d0c2b430bb9f0a49db89dc03278cbd8e`  
		Last Modified: Sat, 16 Mar 2024 03:19:26 GMT  
		Size: 1.3 MB (1302235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351f34f77cd30086783b4d1e7bd91ac224af75f55690527012c4f114a65048b5`  
		Last Modified: Sat, 16 Mar 2024 03:19:26 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:042f6baf4a87f12037bf9a9146e994b03974edfdf6e94ef3a6c8ed9a5b0e01d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75407449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8104ab01bd342cfbbde6ad9a086efdba750ddaaeb6b4ce5acae4072b032808f1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 06:36:10 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 06:36:10 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 06:36:10 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 06:36:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 06:36:10 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 06:36:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 06:36:11 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 06:36:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18595ac3d5791e4d7e7dbcffcbf63e97e29974bd7191f7779889293f06709605`  
		Last Modified: Sat, 16 Mar 2024 01:27:12 GMT  
		Size: 284.9 KB (284879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67b0661c8b928f9ee07193e83a55962dc30ea03b3917d927fbfc6172db763d1`  
		Last Modified: Sat, 16 Mar 2024 01:28:25 GMT  
		Size: 65.8 MB (65767483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e94e3f035a7e84adb42051a6776fb957bb01e4afe261ef52850410749238c3e`  
		Last Modified: Sat, 16 Mar 2024 01:28:09 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90af61f594723149cbf4c52926248b7aa924edce2e71c1146dbfe1c4952d0e85`  
		Last Modified: Sat, 16 Mar 2024 06:36:39 GMT  
		Size: 5.0 MB (4958759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2b089f053b69b50a0ec1b57924c3f1dbab09af5f892a3f3824a1f1d91c4653`  
		Last Modified: Sat, 16 Mar 2024 06:36:39 GMT  
		Size: 1.2 MB (1248659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb3baf5a17563281d926d65bf039e75bafa0be92988b008e142f88f13e48831`  
		Last Modified: Sat, 16 Mar 2024 06:36:39 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:bba85446aa9cf082d96393b37ee2eb8948d32119f9f1b4a7de4264ed6265bc16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d75fc02eccf5b473914195c6b5a7f27a9c7b3af790feb14ca2afa4f0a1e6d2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 08:36:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 08:36:44 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 08:36:44 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 08:36:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 08:36:44 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 08:36:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 08:36:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 08:36:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03de95814623b83a4328b4db2e23b14214f57c18389a27379988469d9b6bbccc`  
		Last Modified: Sat, 16 Mar 2024 00:51:49 GMT  
		Size: 284.1 KB (284082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb316a6d2b1f8b686717aa026be6622630e91b4e2beff72260e41b9c26f5f328`  
		Last Modified: Sat, 16 Mar 2024 00:52:59 GMT  
		Size: 65.8 MB (65767446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3402119434a07f7977a54237330b21abbea9474c729d8bbbe43e79507612156`  
		Last Modified: Sat, 16 Mar 2024 00:52:46 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3e193cf2bcf63192347811ea80a7312b468b42f6341ff8912fb721dcdd07b1`  
		Last Modified: Sat, 16 Mar 2024 08:37:14 GMT  
		Size: 4.5 MB (4514679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302bab84b8a106df7129ce421df27645cf93461c26631a73c4c16dcc48213e33`  
		Last Modified: Sat, 16 Mar 2024 08:37:14 GMT  
		Size: 1.2 MB (1246087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa5da11b54d5792ea909f7bcbe533482069dd4540457779cb629671faadd4eb`  
		Last Modified: Sat, 16 Mar 2024 08:37:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:636495b6181fd6f900cfb1c3fafd4aa67ef8113e127a39c225dcd2b9f28018ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73993764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804083a23a5a42633ad7c22fc0b9908822db952792867afe4852db23de6882c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 02:55:47 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 02:55:48 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 02:55:48 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 02:55:48 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 02:55:48 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 02:55:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 02:55:49 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 02:55:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69c4102457739613c6fcb205a5a8e7dbc8383d57dade0a4502b1bca7b100a4d`  
		Last Modified: Sat, 16 Mar 2024 02:38:03 GMT  
		Size: 286.3 KB (286314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472e8443302a7aa2ee7c60f88cf1c1bff960c6982004fabf4d0b7dbb39552784`  
		Last Modified: Sat, 16 Mar 2024 02:38:55 GMT  
		Size: 64.1 MB (64111127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f3ae01babba08c7331e1311c66fc81f093559e9b48b75c7f09e492835df417`  
		Last Modified: Sat, 16 Mar 2024 02:38:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a47c8e46877caae3d8fa35784305f82b6173865f636c831581e413586174c9f`  
		Last Modified: Sat, 16 Mar 2024 02:56:14 GMT  
		Size: 5.1 MB (5063904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b458a517cc70120b5d5ad7b3624d14288f8fc2bb374503684e47dfb2d81ede41`  
		Last Modified: Sat, 16 Mar 2024 02:56:14 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e927a09144840e6a0520002506a03480353d2bf16acf387e392f67125a232f`  
		Last Modified: Sat, 16 Mar 2024 02:56:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:74036381f9b78d58ddddc74f279042dff06d05ac2b95c3faf063485eac603111
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74219852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afdeb2455afb0545182f73124c3e233abb4a6b803a834f42127d9a1eff4982c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 07:31:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 07:31:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 07:31:22 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 07:31:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 07:31:22 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 07:31:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 07:31:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 07:31:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e315e4c0ee7596e0eb7cc17d622c433e9fc4ef254b722e11e6794265328ea583`  
		Last Modified: Sat, 16 Mar 2024 00:32:12 GMT  
		Size: 286.7 KB (286670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee59a251903fa4e415f22830cd12da95ca1bcf671572b4a701a1d8f75a55d5ee`  
		Last Modified: Sat, 16 Mar 2024 00:33:15 GMT  
		Size: 64.1 MB (64126904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a227c25fca514ad52229d19315a3e0db7f235f9a840f9474237fadee44634bd1`  
		Last Modified: Sat, 16 Mar 2024 00:33:03 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da53f00025342b23cc1c1a712e9f3ff08b05bc0759f58b580a2081c4b925b9e8`  
		Last Modified: Sat, 16 Mar 2024 07:31:42 GMT  
		Size: 5.3 MB (5271003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1eb59d0f562ae579e22be9806e6ea172a7ee0399f354980329dfa3e8e04045`  
		Last Modified: Sat, 16 Mar 2024 07:31:41 GMT  
		Size: 1.2 MB (1186176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f27806532c2006d7f3b98c3ab37d72cf977ec4c488b65e389cb46e6b551627`  
		Last Modified: Sat, 16 Mar 2024 07:31:41 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; s390x

```console
$ docker pull caddy@sha256:179342439e20a0f8308f5b3c8f51063386fb33fb38d9eda738dfd1d4b398280c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76101838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4eddf19e318b73f4fa90802285b549c08b6b015cfc8f36a11adbbf9c593fc2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Tue, 05 Mar 2024 20:58:12 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:58:12 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:58:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:58:13 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:58:13 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1b6899ff00172fd5c809d57028913a3c5aead2c05d0c3c01b15a5249c4ddec`  
		Last Modified: Sat, 27 Jan 2024 05:46:31 GMT  
		Size: 285.1 KB (285091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192deec459dbc25471d5ce96dbf84de90f9e77914e5074081b4aba0516977050`  
		Last Modified: Tue, 05 Mar 2024 20:12:42 GMT  
		Size: 66.2 MB (66218961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e6d46fb71afdd9825fc4397b4949daac74f5a564377560ed3cb3bb910da97f`  
		Last Modified: Tue, 05 Mar 2024 20:12:31 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad42b5ce4497969e7a2ebbdf9ada284081c50ce1744927873987c8075ed117fa`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 5.1 MB (5117256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea105a4685d829ffde13e2d0e06f02ec7f1e1381059eae15941a5aeb36d5f7a7`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 1.3 MB (1262390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1423e2dcf9499ee1179b946513f3194740bf64ee1f24d0a7688bde92f8773874`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:deed166abe77b412a506924346166c58e03f6e35fb2836e7af244be01925eddf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2054342050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7b95fb04081aaf80026e1bb52d4a79df79ea5aac969382123b16607318419f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 01:46:04 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Mar 2024 01:46:05 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Mar 2024 01:46:06 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Mar 2024 01:46:07 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Mar 2024 01:46:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 01:46:43 GMT
ENV GOPATH=C:\go
# Wed, 13 Mar 2024 01:47:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Mar 2024 02:01:45 GMT
ENV GOLANG_VERSION=1.21.8
# Wed, 13 Mar 2024 02:04:07 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 02:04:09 GMT
WORKDIR C:\go
# Wed, 13 Mar 2024 02:40:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:40:13 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 13 Mar 2024 02:40:14 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:40:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 13 Mar 2024 02:40:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 13 Mar 2024 02:40:40 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0a2d972d6c007b69f2c3ea41c1fe5fad6b189bfe40efacdcaf910b884fb6bb`  
		Last Modified: Wed, 13 Mar 2024 02:13:35 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f3068df504cd61566fc5e038c996322e35f58e08e0c6ef6ce589b11de4eb93`  
		Last Modified: Wed, 13 Mar 2024 02:13:34 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98750f7d798b8a0b5199088d4860bce5d51320b2fc07440f211ec692f4bf63b4`  
		Last Modified: Wed, 13 Mar 2024 02:13:33 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e43d1ea980f98746869d1942fc459ed402f307d4de5c435e325d2c9d534e99`  
		Last Modified: Wed, 13 Mar 2024 02:13:33 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fc4a2ae5d19f3b766991bfec5347bd5192c19ede11e7dfbf8b7d698fc1323d`  
		Last Modified: Wed, 13 Mar 2024 02:13:38 GMT  
		Size: 25.6 MB (25551948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251908e7b1f95da24e9f4ec7c727a2662105696c9de2925ab36938572cfb9f79`  
		Last Modified: Wed, 13 Mar 2024 02:13:31 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2927b1ac917c6e3261034f1c0cbb347c73f26593e997c505dfd04da18f966c1a`  
		Last Modified: Wed, 13 Mar 2024 02:13:31 GMT  
		Size: 273.7 KB (273727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5d297a0f5c09416c27b06ff859cb837506ffabdf0faa0cb5112e0a34839aab`  
		Last Modified: Wed, 13 Mar 2024 02:15:44 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1412d17e78321071b9d6a4dbb609e6a24c2e829a90ed9ca7e20a72ede74d04`  
		Last Modified: Wed, 13 Mar 2024 02:16:03 GMT  
		Size: 69.4 MB (69363257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619eb2756fc98681ecf9e1220a72f64f2e3f3fe9e72edd3a6021ad0249b9b2a5`  
		Last Modified: Wed, 13 Mar 2024 02:15:44 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf19d565f6ad05c073e69610b1e850eaf1a6aa6806195ea601c4a47303140d27`  
		Last Modified: Wed, 13 Mar 2024 02:42:22 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279cafbdd3019482f630ef1d502ea930d8ee1cfd8f9977bb52059c87ddff7a55`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e9d1117318fed479ece2fe1c6f9b896efcca03021ea368d722153aca1f8bc9`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d106feccb912e361adb23c8a586aad6b6c8493698e3893f4b1a2cd40bdd03cb4`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e766bc3c556143c937c2d95209a8d6370902ee4f31471f2a35c4d7045d361af6`  
		Last Modified: Wed, 13 Mar 2024 02:42:20 GMT  
		Size: 1.7 MB (1676188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39236cd34ad31ef892f22ac798c76cb384eb17ff72d5881539cbee398708be72`  
		Last Modified: Wed, 13 Mar 2024 02:42:20 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:53d965e8f604060a1c65cdf2a722300b8ff2f7a36494b6c0ba0c315fc7ffd2c2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221957582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0daee73c43fffad7bf7cfb8399d58db63aaa5f6727affb62b8d370b9760df81f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 01:49:48 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Mar 2024 01:49:49 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Mar 2024 01:49:50 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Mar 2024 01:49:51 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Mar 2024 01:51:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 01:51:29 GMT
ENV GOPATH=C:\go
# Wed, 13 Mar 2024 01:52:49 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Mar 2024 02:04:28 GMT
ENV GOLANG_VERSION=1.21.8
# Wed, 13 Mar 2024 02:07:38 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 02:07:39 GMT
WORKDIR C:\go
# Wed, 13 Mar 2024 02:38:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:38:30 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 13 Mar 2024 02:38:31 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:38:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 13 Mar 2024 02:39:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 13 Mar 2024 02:39:54 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc39f00be83bc8d2b0e0f2123fce0278f495e47f8a969bf03ec57df5f98cbda`  
		Last Modified: Wed, 13 Mar 2024 02:14:08 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f8b9e441646ef17118a0d394fa50244ef70c9e053c5b7d33e648796c8df90e`  
		Last Modified: Wed, 13 Mar 2024 02:14:07 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8759cd20778bf436a14e59cb31806b28212fcd510d8de32d44e49a9f39656f3d`  
		Last Modified: Wed, 13 Mar 2024 02:14:06 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d99a22ebabf5f80d07ad166a24eace1c2fa31cef2566a179bfec0d6407513e`  
		Last Modified: Wed, 13 Mar 2024 02:14:06 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfdb963b4125b258828e1fbac783c993a6845ad94973fad173f5dd25be3c34b`  
		Last Modified: Wed, 13 Mar 2024 02:14:12 GMT  
		Size: 25.5 MB (25540238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae89960ac90d33a751006d43faf1cbd1309b448658a447bb19dddabdbee17a9`  
		Last Modified: Wed, 13 Mar 2024 02:14:04 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff0bdcb61a7230b8b00d6e08d739c64fc0342dc675ed99fe6d35885cf1aa369`  
		Last Modified: Wed, 13 Mar 2024 02:14:05 GMT  
		Size: 272.6 KB (272572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c052d4b938689fbc1637386d1e61efa391787bd8128ee6d093464bad09b0231`  
		Last Modified: Wed, 13 Mar 2024 02:16:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e82772a8bffddc9f4a46c65cfa48f47938d84feb3730231762158c98014e47a`  
		Last Modified: Wed, 13 Mar 2024 02:16:31 GMT  
		Size: 69.4 MB (69350702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbffcc4012ecf27a404cc40eb63c43a880ad5104a82ee619fd0669acb2b5a710`  
		Last Modified: Wed, 13 Mar 2024 02:16:12 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fcd0eeed9adb7d9bf391df7f194150cb8ee56a63bc679cf147a14185381c3b`  
		Last Modified: Wed, 13 Mar 2024 02:42:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d74d351932d9ba6c92c9398e69d6736df75938a6ba3b7f1055206a1ed80b48`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db51f1e77d8641618afadb6f8c1ad073c4f72bb79099a00b0cabcbc8f5579248`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43620705f408ca0a7894137080f7947cc45d10badb0c7668ae1d46464494001b`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdaa0771d9c8b704195f821c3a9c23a5d9ff5e7e9b29335b835ce237f9d4dd50`  
		Last Modified: Wed, 13 Mar 2024 02:42:03 GMT  
		Size: 1.7 MB (1676257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010496734b493d0bc1b1a73566306e98777144ff64c5c886cf84de3af4fd971b`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-alpine`

```console
$ docker pull caddy@sha256:8308bb619e5ff5bc1842b8fc8480bb1584220a0c241f125727fa844918aac505
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
$ docker pull caddy@sha256:a37704d2149bb703350b3e63704ecb468ec6f10cdc3784c818988e250484b2ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76973825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a6b943c698684ea914a9d08c8a00d2e573cbc2a95669142bc1b35350317cff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 03:18:55 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 03:18:55 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 03:18:55 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 03:18:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 03:18:55 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 03:18:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 03:18:57 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 03:18:57 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e791cb90c3d0bf08a988f13b405c9947c74b5bc31c7c939197a7175f6c7f0e`  
		Last Modified: Sat, 27 Jan 2024 01:36:33 GMT  
		Size: 284.7 KB (284690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3da9c61ef062502252a549dbc1f90925a8d7b6ef0644ffbfaea77be8b6f058`  
		Last Modified: Tue, 05 Mar 2024 19:25:57 GMT  
		Size: 67.0 MB (67010725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1741a7c0e9ce85801257b76332c08a3abdf5069bf46b0e764a32219d92189dc5`  
		Last Modified: Tue, 05 Mar 2024 19:25:45 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f302d3cc779898a1baa29b9dde46627021754a60a003a8ceb71b73f80af80bb2`  
		Last Modified: Sat, 16 Mar 2024 03:19:27 GMT  
		Size: 5.0 MB (4973021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51954c5f8bcd596606e74156291b16b5d0c2b430bb9f0a49db89dc03278cbd8e`  
		Last Modified: Sat, 16 Mar 2024 03:19:26 GMT  
		Size: 1.3 MB (1302235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351f34f77cd30086783b4d1e7bd91ac224af75f55690527012c4f114a65048b5`  
		Last Modified: Sat, 16 Mar 2024 03:19:26 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:042f6baf4a87f12037bf9a9146e994b03974edfdf6e94ef3a6c8ed9a5b0e01d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75407449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8104ab01bd342cfbbde6ad9a086efdba750ddaaeb6b4ce5acae4072b032808f1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 06:36:10 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 06:36:10 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 06:36:10 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 06:36:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 06:36:10 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 06:36:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 06:36:11 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 06:36:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18595ac3d5791e4d7e7dbcffcbf63e97e29974bd7191f7779889293f06709605`  
		Last Modified: Sat, 16 Mar 2024 01:27:12 GMT  
		Size: 284.9 KB (284879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67b0661c8b928f9ee07193e83a55962dc30ea03b3917d927fbfc6172db763d1`  
		Last Modified: Sat, 16 Mar 2024 01:28:25 GMT  
		Size: 65.8 MB (65767483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e94e3f035a7e84adb42051a6776fb957bb01e4afe261ef52850410749238c3e`  
		Last Modified: Sat, 16 Mar 2024 01:28:09 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90af61f594723149cbf4c52926248b7aa924edce2e71c1146dbfe1c4952d0e85`  
		Last Modified: Sat, 16 Mar 2024 06:36:39 GMT  
		Size: 5.0 MB (4958759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2b089f053b69b50a0ec1b57924c3f1dbab09af5f892a3f3824a1f1d91c4653`  
		Last Modified: Sat, 16 Mar 2024 06:36:39 GMT  
		Size: 1.2 MB (1248659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb3baf5a17563281d926d65bf039e75bafa0be92988b008e142f88f13e48831`  
		Last Modified: Sat, 16 Mar 2024 06:36:39 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:bba85446aa9cf082d96393b37ee2eb8948d32119f9f1b4a7de4264ed6265bc16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d75fc02eccf5b473914195c6b5a7f27a9c7b3af790feb14ca2afa4f0a1e6d2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 08:36:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 08:36:44 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 08:36:44 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 08:36:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 08:36:44 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 08:36:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 08:36:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 08:36:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03de95814623b83a4328b4db2e23b14214f57c18389a27379988469d9b6bbccc`  
		Last Modified: Sat, 16 Mar 2024 00:51:49 GMT  
		Size: 284.1 KB (284082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb316a6d2b1f8b686717aa026be6622630e91b4e2beff72260e41b9c26f5f328`  
		Last Modified: Sat, 16 Mar 2024 00:52:59 GMT  
		Size: 65.8 MB (65767446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3402119434a07f7977a54237330b21abbea9474c729d8bbbe43e79507612156`  
		Last Modified: Sat, 16 Mar 2024 00:52:46 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3e193cf2bcf63192347811ea80a7312b468b42f6341ff8912fb721dcdd07b1`  
		Last Modified: Sat, 16 Mar 2024 08:37:14 GMT  
		Size: 4.5 MB (4514679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302bab84b8a106df7129ce421df27645cf93461c26631a73c4c16dcc48213e33`  
		Last Modified: Sat, 16 Mar 2024 08:37:14 GMT  
		Size: 1.2 MB (1246087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa5da11b54d5792ea909f7bcbe533482069dd4540457779cb629671faadd4eb`  
		Last Modified: Sat, 16 Mar 2024 08:37:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:636495b6181fd6f900cfb1c3fafd4aa67ef8113e127a39c225dcd2b9f28018ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73993764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804083a23a5a42633ad7c22fc0b9908822db952792867afe4852db23de6882c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 02:55:47 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 02:55:48 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 02:55:48 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 02:55:48 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 02:55:48 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 02:55:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 02:55:49 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 02:55:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69c4102457739613c6fcb205a5a8e7dbc8383d57dade0a4502b1bca7b100a4d`  
		Last Modified: Sat, 16 Mar 2024 02:38:03 GMT  
		Size: 286.3 KB (286314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472e8443302a7aa2ee7c60f88cf1c1bff960c6982004fabf4d0b7dbb39552784`  
		Last Modified: Sat, 16 Mar 2024 02:38:55 GMT  
		Size: 64.1 MB (64111127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f3ae01babba08c7331e1311c66fc81f093559e9b48b75c7f09e492835df417`  
		Last Modified: Sat, 16 Mar 2024 02:38:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a47c8e46877caae3d8fa35784305f82b6173865f636c831581e413586174c9f`  
		Last Modified: Sat, 16 Mar 2024 02:56:14 GMT  
		Size: 5.1 MB (5063904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b458a517cc70120b5d5ad7b3624d14288f8fc2bb374503684e47dfb2d81ede41`  
		Last Modified: Sat, 16 Mar 2024 02:56:14 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e927a09144840e6a0520002506a03480353d2bf16acf387e392f67125a232f`  
		Last Modified: Sat, 16 Mar 2024 02:56:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:74036381f9b78d58ddddc74f279042dff06d05ac2b95c3faf063485eac603111
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74219852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afdeb2455afb0545182f73124c3e233abb4a6b803a834f42127d9a1eff4982c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 07:31:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 07:31:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 07:31:22 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 07:31:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 07:31:22 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 07:31:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 07:31:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 07:31:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e315e4c0ee7596e0eb7cc17d622c433e9fc4ef254b722e11e6794265328ea583`  
		Last Modified: Sat, 16 Mar 2024 00:32:12 GMT  
		Size: 286.7 KB (286670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee59a251903fa4e415f22830cd12da95ca1bcf671572b4a701a1d8f75a55d5ee`  
		Last Modified: Sat, 16 Mar 2024 00:33:15 GMT  
		Size: 64.1 MB (64126904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a227c25fca514ad52229d19315a3e0db7f235f9a840f9474237fadee44634bd1`  
		Last Modified: Sat, 16 Mar 2024 00:33:03 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da53f00025342b23cc1c1a712e9f3ff08b05bc0759f58b580a2081c4b925b9e8`  
		Last Modified: Sat, 16 Mar 2024 07:31:42 GMT  
		Size: 5.3 MB (5271003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1eb59d0f562ae579e22be9806e6ea172a7ee0399f354980329dfa3e8e04045`  
		Last Modified: Sat, 16 Mar 2024 07:31:41 GMT  
		Size: 1.2 MB (1186176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f27806532c2006d7f3b98c3ab37d72cf977ec4c488b65e389cb46e6b551627`  
		Last Modified: Sat, 16 Mar 2024 07:31:41 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:179342439e20a0f8308f5b3c8f51063386fb33fb38d9eda738dfd1d4b398280c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76101838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4eddf19e318b73f4fa90802285b549c08b6b015cfc8f36a11adbbf9c593fc2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Tue, 05 Mar 2024 20:58:12 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:58:12 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:58:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:58:13 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:58:13 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1b6899ff00172fd5c809d57028913a3c5aead2c05d0c3c01b15a5249c4ddec`  
		Last Modified: Sat, 27 Jan 2024 05:46:31 GMT  
		Size: 285.1 KB (285091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192deec459dbc25471d5ce96dbf84de90f9e77914e5074081b4aba0516977050`  
		Last Modified: Tue, 05 Mar 2024 20:12:42 GMT  
		Size: 66.2 MB (66218961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e6d46fb71afdd9825fc4397b4949daac74f5a564377560ed3cb3bb910da97f`  
		Last Modified: Tue, 05 Mar 2024 20:12:31 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad42b5ce4497969e7a2ebbdf9ada284081c50ce1744927873987c8075ed117fa`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 5.1 MB (5117256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea105a4685d829ffde13e2d0e06f02ec7f1e1381059eae15941a5aeb36d5f7a7`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 1.3 MB (1262390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1423e2dcf9499ee1179b946513f3194740bf64ee1f24d0a7688bde92f8773874`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:88480ae6cc843e1f4d7891d869f95182848a5414c6545cc2662d466a7c8dfdd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `caddy:2.7-builder-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:53d965e8f604060a1c65cdf2a722300b8ff2f7a36494b6c0ba0c315fc7ffd2c2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221957582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0daee73c43fffad7bf7cfb8399d58db63aaa5f6727affb62b8d370b9760df81f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 01:49:48 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Mar 2024 01:49:49 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Mar 2024 01:49:50 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Mar 2024 01:49:51 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Mar 2024 01:51:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 01:51:29 GMT
ENV GOPATH=C:\go
# Wed, 13 Mar 2024 01:52:49 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Mar 2024 02:04:28 GMT
ENV GOLANG_VERSION=1.21.8
# Wed, 13 Mar 2024 02:07:38 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 02:07:39 GMT
WORKDIR C:\go
# Wed, 13 Mar 2024 02:38:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:38:30 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 13 Mar 2024 02:38:31 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:38:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 13 Mar 2024 02:39:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 13 Mar 2024 02:39:54 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc39f00be83bc8d2b0e0f2123fce0278f495e47f8a969bf03ec57df5f98cbda`  
		Last Modified: Wed, 13 Mar 2024 02:14:08 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f8b9e441646ef17118a0d394fa50244ef70c9e053c5b7d33e648796c8df90e`  
		Last Modified: Wed, 13 Mar 2024 02:14:07 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8759cd20778bf436a14e59cb31806b28212fcd510d8de32d44e49a9f39656f3d`  
		Last Modified: Wed, 13 Mar 2024 02:14:06 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d99a22ebabf5f80d07ad166a24eace1c2fa31cef2566a179bfec0d6407513e`  
		Last Modified: Wed, 13 Mar 2024 02:14:06 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfdb963b4125b258828e1fbac783c993a6845ad94973fad173f5dd25be3c34b`  
		Last Modified: Wed, 13 Mar 2024 02:14:12 GMT  
		Size: 25.5 MB (25540238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae89960ac90d33a751006d43faf1cbd1309b448658a447bb19dddabdbee17a9`  
		Last Modified: Wed, 13 Mar 2024 02:14:04 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff0bdcb61a7230b8b00d6e08d739c64fc0342dc675ed99fe6d35885cf1aa369`  
		Last Modified: Wed, 13 Mar 2024 02:14:05 GMT  
		Size: 272.6 KB (272572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c052d4b938689fbc1637386d1e61efa391787bd8128ee6d093464bad09b0231`  
		Last Modified: Wed, 13 Mar 2024 02:16:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e82772a8bffddc9f4a46c65cfa48f47938d84feb3730231762158c98014e47a`  
		Last Modified: Wed, 13 Mar 2024 02:16:31 GMT  
		Size: 69.4 MB (69350702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbffcc4012ecf27a404cc40eb63c43a880ad5104a82ee619fd0669acb2b5a710`  
		Last Modified: Wed, 13 Mar 2024 02:16:12 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fcd0eeed9adb7d9bf391df7f194150cb8ee56a63bc679cf147a14185381c3b`  
		Last Modified: Wed, 13 Mar 2024 02:42:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d74d351932d9ba6c92c9398e69d6736df75938a6ba3b7f1055206a1ed80b48`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db51f1e77d8641618afadb6f8c1ad073c4f72bb79099a00b0cabcbc8f5579248`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43620705f408ca0a7894137080f7947cc45d10badb0c7668ae1d46464494001b`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdaa0771d9c8b704195f821c3a9c23a5d9ff5e7e9b29335b835ce237f9d4dd50`  
		Last Modified: Wed, 13 Mar 2024 02:42:03 GMT  
		Size: 1.7 MB (1676257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010496734b493d0bc1b1a73566306e98777144ff64c5c886cf84de3af4fd971b`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:7904ec0c624b28630437b42e793d0e1bc2472c348c79b15b26d065162eafd9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `caddy:2.7-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:deed166abe77b412a506924346166c58e03f6e35fb2836e7af244be01925eddf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2054342050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7b95fb04081aaf80026e1bb52d4a79df79ea5aac969382123b16607318419f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 01:46:04 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Mar 2024 01:46:05 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Mar 2024 01:46:06 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Mar 2024 01:46:07 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Mar 2024 01:46:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 01:46:43 GMT
ENV GOPATH=C:\go
# Wed, 13 Mar 2024 01:47:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Mar 2024 02:01:45 GMT
ENV GOLANG_VERSION=1.21.8
# Wed, 13 Mar 2024 02:04:07 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 02:04:09 GMT
WORKDIR C:\go
# Wed, 13 Mar 2024 02:40:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:40:13 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 13 Mar 2024 02:40:14 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:40:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 13 Mar 2024 02:40:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 13 Mar 2024 02:40:40 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0a2d972d6c007b69f2c3ea41c1fe5fad6b189bfe40efacdcaf910b884fb6bb`  
		Last Modified: Wed, 13 Mar 2024 02:13:35 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f3068df504cd61566fc5e038c996322e35f58e08e0c6ef6ce589b11de4eb93`  
		Last Modified: Wed, 13 Mar 2024 02:13:34 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98750f7d798b8a0b5199088d4860bce5d51320b2fc07440f211ec692f4bf63b4`  
		Last Modified: Wed, 13 Mar 2024 02:13:33 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e43d1ea980f98746869d1942fc459ed402f307d4de5c435e325d2c9d534e99`  
		Last Modified: Wed, 13 Mar 2024 02:13:33 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fc4a2ae5d19f3b766991bfec5347bd5192c19ede11e7dfbf8b7d698fc1323d`  
		Last Modified: Wed, 13 Mar 2024 02:13:38 GMT  
		Size: 25.6 MB (25551948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251908e7b1f95da24e9f4ec7c727a2662105696c9de2925ab36938572cfb9f79`  
		Last Modified: Wed, 13 Mar 2024 02:13:31 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2927b1ac917c6e3261034f1c0cbb347c73f26593e997c505dfd04da18f966c1a`  
		Last Modified: Wed, 13 Mar 2024 02:13:31 GMT  
		Size: 273.7 KB (273727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5d297a0f5c09416c27b06ff859cb837506ffabdf0faa0cb5112e0a34839aab`  
		Last Modified: Wed, 13 Mar 2024 02:15:44 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1412d17e78321071b9d6a4dbb609e6a24c2e829a90ed9ca7e20a72ede74d04`  
		Last Modified: Wed, 13 Mar 2024 02:16:03 GMT  
		Size: 69.4 MB (69363257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619eb2756fc98681ecf9e1220a72f64f2e3f3fe9e72edd3a6021ad0249b9b2a5`  
		Last Modified: Wed, 13 Mar 2024 02:15:44 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf19d565f6ad05c073e69610b1e850eaf1a6aa6806195ea601c4a47303140d27`  
		Last Modified: Wed, 13 Mar 2024 02:42:22 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279cafbdd3019482f630ef1d502ea930d8ee1cfd8f9977bb52059c87ddff7a55`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e9d1117318fed479ece2fe1c6f9b896efcca03021ea368d722153aca1f8bc9`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d106feccb912e361adb23c8a586aad6b6c8493698e3893f4b1a2cd40bdd03cb4`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e766bc3c556143c937c2d95209a8d6370902ee4f31471f2a35c4d7045d361af6`  
		Last Modified: Wed, 13 Mar 2024 02:42:20 GMT  
		Size: 1.7 MB (1676188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39236cd34ad31ef892f22ac798c76cb384eb17ff72d5881539cbee398708be72`  
		Last Modified: Wed, 13 Mar 2024 02:42:20 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-windowsservercore`

```console
$ docker pull caddy@sha256:02e4ec422a43bbe257c0b6f52bc54f9e391ac2ed078f86fc4d80269ca8ef3533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `caddy:2.7-windowsservercore` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:e92a98f9befbcc685cba6014745c4c4e5573d524f98646666afae41fe635a647
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1973514153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c02263e4345786d822a7cbe2109be66b8bbc405dad0088432e203c583cdb8c4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:37:25 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:37:26 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:37:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:37:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:37:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:37:54 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:37:55 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:37:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:37:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:37:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:38:00 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:38:01 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:38:03 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:38:21 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:38:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3433f0cddf0bf50f831ae26d44034fb9ccdaea63173630b59cbe9dc33860a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:45 GMT  
		Size: 471.5 KB (471467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39aa89107a4c1ac15acc37ba98faa00f98774062e839984cd569c84acccbefa`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903c57abacc03a4132d1914d83b140d91cad6d3f72113588dbb0449668e5459e`  
		Last Modified: Wed, 13 Mar 2024 02:41:47 GMT  
		Size: 15.3 MB (15272331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c505d8db5c54f9f5b13a230f310c78e1daa9f0fa5baa7db6bb4b6f9b2824c64`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02c7783ff4e4ea0351aa496f9316d007b5d39dd7ac091772a53c788cc850835`  
		Last Modified: Wed, 13 Mar 2024 02:41:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2f6f475cd8b631685eb3441f13c0418b595dc3f64fc43f4de103cd270bd07a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c099338186092d8e8a9ee4e1aef2ac6bac6e0e37d05b00acc2519d4828eebc1a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66be30fd26f10adf7753fc7287726b290417f432503173cc8cfcc37c5970eed5`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdecded462eba57ac719ddeaf73027953397d9470c8d9ce91486b650688448d1`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b196924a8268e867bced4e92552ad7a24d5079dd5d3a5f2d32e98acf5b94ec`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83e0533daa0143428320795f95f747a318ce9dfaec9c1918dc09ddabff7ce6`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d6f7d580438b0f330c60e990071ee0a7fd2cb8e861b5b3673229aae5f40a97`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3043316cf0d3543d7ad8c2cf29b9f42217a7ff7ee358b9ccf49ec1c2742b40dc`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9d07b35dd72d9c89f56d604b5b5ff1096607de0b699a7845b4d4eef4542999`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7138f2320f3eb26befb56422d151646fa73d61b45b1fd7ba1a97e97b12b1794`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dd6eb25db87e92a30fe3a646b0ca820c3a8a855af39f49e9c1239e9e7e8fa8`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff49c00e60e2791dac19058d6bba6e562c80b90859f8e91ae70b474a582042`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c28453d92f8177a5ca4103ba031b5f02ceb70269930e8642e8bda358f1eef11`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 289.3 KB (289264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5958cc3ab872a13ea8011a1ae0a2290cefbfb5721bf58c5c16e2a1dfa216aa`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-windowsservercore` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:2a10673838e2beefb539398925457319c1e7800b242f5c261bc40ddd7f16aa33
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2141123401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001b000d65334996d09969a3e79ce6304b5ea6811c67eb7add59f0c78b73ba5c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:34:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:34:08 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:35:29 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:35:30 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:35:31 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:35:31 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:35:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:35:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:35:35 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:35:36 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:35:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:35:39 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:35:40 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:36:47 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:36:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bb323765ff7b405cedec6f88daa8a1c8470f45c358d637c0062cf4c63d7e07`  
		Last Modified: Wed, 13 Mar 2024 02:41:21 GMT  
		Size: 465.6 KB (465620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b3f11ec4ee425a6a0b9f5ad200c9193592181f59520c9a80372e647787163a`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ffe491a522455b1d95c1d0d3384188ea361064259fffcadd657bebae4fa934`  
		Last Modified: Wed, 13 Mar 2024 02:41:24 GMT  
		Size: 15.3 MB (15277213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b62af40926c0d1a37e6126f41f63533166809b5b54434cf3b53ab5734357e59`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a9b1639ec2e8588ca4fd94f87b31b4e30adef3c0ac45ea4ac0e4cdce643d6`  
		Last Modified: Wed, 13 Mar 2024 02:41:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7a48958fcb11d52bb7a65f60d6f322d3326d4f2916e0547b764cbe4fe0eae8`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9eb36d28260e8ba5549b16a87d121a4d7b0d38f46e1127ee1fd95f2e31e6f2c`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d221a46e4e966da289289be19ac425d0199540bef1d6d7c890ba45ec255e79`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feeda3213337ce81d383bcb08c0b241e763185b91a2e180f35c59395e3c0290f`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d7bf5ae3a283a09c7a385afa5160b2d0f1d275fc23e0a1711bf734511fe0b1`  
		Last Modified: Wed, 13 Mar 2024 02:41:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f309d19b55289fe422d64dd24736be59a52f6eba872d8fb1054416f8b5d9c553`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4ac1a4021eeee54512dde50b437001408fd1dda9d896f68d38728f7dba8c6c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e117655b528b6e8f7ce8d4d2cb69d41a1735fec0e31e10dc40cddcf0d012be`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5524c6d618843e710fa22d77e57a844c7cdfd68676c809d2d1ecde656c16a81c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879784be55be2c5d212302ae42232de9bfeaccea0b1398ec0101ef36d542930c`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f8aadcc42505eea344cf0504c7312d01033f159e88d6eadab5abb9eefc98a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41580c6cc25a82ee1a4de9315ec98ce6e89bd73461a941248648d04292e9ff52`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1261dc2b6b686493c5c3989f8efdd404b912398f6a38933aba80fe65d5d6240c`  
		Last Modified: Wed, 13 Mar 2024 02:41:15 GMT  
		Size: 258.2 KB (258159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8856855cc09ca543e8712766ea12d12556af369305babcaf786f620c89c3450d`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-windowsservercore-1809`

```console
$ docker pull caddy@sha256:3e51c662d70a2bcf344a51331fb88b7d223db9cc683b01463633782351400cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `caddy:2.7-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:2a10673838e2beefb539398925457319c1e7800b242f5c261bc40ddd7f16aa33
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2141123401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001b000d65334996d09969a3e79ce6304b5ea6811c67eb7add59f0c78b73ba5c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:34:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:34:08 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:35:29 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:35:30 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:35:31 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:35:31 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:35:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:35:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:35:35 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:35:36 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:35:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:35:39 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:35:40 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:36:47 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:36:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bb323765ff7b405cedec6f88daa8a1c8470f45c358d637c0062cf4c63d7e07`  
		Last Modified: Wed, 13 Mar 2024 02:41:21 GMT  
		Size: 465.6 KB (465620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b3f11ec4ee425a6a0b9f5ad200c9193592181f59520c9a80372e647787163a`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ffe491a522455b1d95c1d0d3384188ea361064259fffcadd657bebae4fa934`  
		Last Modified: Wed, 13 Mar 2024 02:41:24 GMT  
		Size: 15.3 MB (15277213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b62af40926c0d1a37e6126f41f63533166809b5b54434cf3b53ab5734357e59`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a9b1639ec2e8588ca4fd94f87b31b4e30adef3c0ac45ea4ac0e4cdce643d6`  
		Last Modified: Wed, 13 Mar 2024 02:41:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7a48958fcb11d52bb7a65f60d6f322d3326d4f2916e0547b764cbe4fe0eae8`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9eb36d28260e8ba5549b16a87d121a4d7b0d38f46e1127ee1fd95f2e31e6f2c`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d221a46e4e966da289289be19ac425d0199540bef1d6d7c890ba45ec255e79`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feeda3213337ce81d383bcb08c0b241e763185b91a2e180f35c59395e3c0290f`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d7bf5ae3a283a09c7a385afa5160b2d0f1d275fc23e0a1711bf734511fe0b1`  
		Last Modified: Wed, 13 Mar 2024 02:41:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f309d19b55289fe422d64dd24736be59a52f6eba872d8fb1054416f8b5d9c553`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4ac1a4021eeee54512dde50b437001408fd1dda9d896f68d38728f7dba8c6c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e117655b528b6e8f7ce8d4d2cb69d41a1735fec0e31e10dc40cddcf0d012be`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5524c6d618843e710fa22d77e57a844c7cdfd68676c809d2d1ecde656c16a81c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879784be55be2c5d212302ae42232de9bfeaccea0b1398ec0101ef36d542930c`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f8aadcc42505eea344cf0504c7312d01033f159e88d6eadab5abb9eefc98a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41580c6cc25a82ee1a4de9315ec98ce6e89bd73461a941248648d04292e9ff52`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1261dc2b6b686493c5c3989f8efdd404b912398f6a38933aba80fe65d5d6240c`  
		Last Modified: Wed, 13 Mar 2024 02:41:15 GMT  
		Size: 258.2 KB (258159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8856855cc09ca543e8712766ea12d12556af369305babcaf786f620c89c3450d`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:e56fe39382d5d420f2ca9e2758ad977fc5a521e371d1658d8f98d8fd55615b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `caddy:2.7-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:e92a98f9befbcc685cba6014745c4c4e5573d524f98646666afae41fe635a647
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1973514153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c02263e4345786d822a7cbe2109be66b8bbc405dad0088432e203c583cdb8c4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:37:25 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:37:26 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:37:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:37:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:37:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:37:54 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:37:55 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:37:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:37:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:37:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:38:00 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:38:01 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:38:03 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:38:21 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:38:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3433f0cddf0bf50f831ae26d44034fb9ccdaea63173630b59cbe9dc33860a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:45 GMT  
		Size: 471.5 KB (471467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39aa89107a4c1ac15acc37ba98faa00f98774062e839984cd569c84acccbefa`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903c57abacc03a4132d1914d83b140d91cad6d3f72113588dbb0449668e5459e`  
		Last Modified: Wed, 13 Mar 2024 02:41:47 GMT  
		Size: 15.3 MB (15272331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c505d8db5c54f9f5b13a230f310c78e1daa9f0fa5baa7db6bb4b6f9b2824c64`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02c7783ff4e4ea0351aa496f9316d007b5d39dd7ac091772a53c788cc850835`  
		Last Modified: Wed, 13 Mar 2024 02:41:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2f6f475cd8b631685eb3441f13c0418b595dc3f64fc43f4de103cd270bd07a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c099338186092d8e8a9ee4e1aef2ac6bac6e0e37d05b00acc2519d4828eebc1a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66be30fd26f10adf7753fc7287726b290417f432503173cc8cfcc37c5970eed5`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdecded462eba57ac719ddeaf73027953397d9470c8d9ce91486b650688448d1`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b196924a8268e867bced4e92552ad7a24d5079dd5d3a5f2d32e98acf5b94ec`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83e0533daa0143428320795f95f747a318ce9dfaec9c1918dc09ddabff7ce6`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d6f7d580438b0f330c60e990071ee0a7fd2cb8e861b5b3673229aae5f40a97`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3043316cf0d3543d7ad8c2cf29b9f42217a7ff7ee358b9ccf49ec1c2742b40dc`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9d07b35dd72d9c89f56d604b5b5ff1096607de0b699a7845b4d4eef4542999`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7138f2320f3eb26befb56422d151646fa73d61b45b1fd7ba1a97e97b12b1794`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dd6eb25db87e92a30fe3a646b0ca820c3a8a855af39f49e9c1239e9e7e8fa8`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff49c00e60e2791dac19058d6bba6e562c80b90859f8e91ae70b474a582042`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c28453d92f8177a5ca4103ba031b5f02ceb70269930e8642e8bda358f1eef11`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 289.3 KB (289264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5958cc3ab872a13ea8011a1ae0a2290cefbfb5721bf58c5c16e2a1dfa216aa`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6`

```console
$ docker pull caddy@sha256:ce43091c481420028215c752115f25e501155b055ae9f4862bae373bda4c1308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `caddy:2.7.6` - linux; amd64

```console
$ docker pull caddy@sha256:a6054d207060158cd0f019d6a35907bf47d1f8dacf58cdb63075a930d8ebca38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18467348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da4af4af9d73e970be3df873e00b8e658a7fc56ab982bfffa21d9bae68e3943`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:18:44 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 03:18:46 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 03:18:46 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 03:18:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 03:18:48 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 03:18:48 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 03:18:48 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 03:18:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 03:18:48 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 80
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 443
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 03:18:49 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 03:18:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a167b92bd92ca649523209f279d023d90edd2658f2dbbd5a79cd991b707a1bf4`  
		Last Modified: Sat, 16 Mar 2024 03:19:12 GMT  
		Size: 350.8 KB (350841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa65d2923419d52c79891c5c107216c8efc7534f740cafcddcb57fcd915fd61`  
		Last Modified: Sat, 16 Mar 2024 03:19:12 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832dc3f423aedf5c58d59571f7e5eebd543b4c31f0a0bacc36b509313473765e`  
		Last Modified: Sat, 16 Mar 2024 03:19:15 GMT  
		Size: 14.7 MB (14706436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6` - linux; arm variant v6

```console
$ docker pull caddy@sha256:d5b956705aa5cb2d80a34b0da959c62f6e1b85d3b6af5d39bdd43a5ebad79732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17423235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637ed474101820123d027bf07c3bacd795eec60a114ec44aa0ab7c081f03fcdd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:36:00 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 06:36:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 06:36:01 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 06:36:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 06:36:04 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 06:36:04 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 06:36:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 06:36:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 06:36:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 80
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 443
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 06:36:05 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 06:36:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7e837cfa426b2a8d095055ea95ecda50deb35a29395410997280bf4efa14be`  
		Last Modified: Sat, 16 Mar 2024 06:36:25 GMT  
		Size: 347.6 KB (347629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aac6695e2937791ffb389edf1aee134b4e2e7c879173c70c5b0851017f402f5`  
		Last Modified: Sat, 16 Mar 2024 06:36:24 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a5dfabcee2609d8f2199b85fef83d4b0fa6612faa5a74b40f2809ccef87a5d`  
		Last Modified: Sat, 16 Mar 2024 06:36:27 GMT  
		Size: 13.9 MB (13921018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6` - linux; arm variant v7

```console
$ docker pull caddy@sha256:d193bf8cf22c67a72ca3f4bc784363a0964ee0bc6481457a375beff0c515bb7b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17147117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c56baf0ceba318c0b5f456a51c90a5291492d8586689fa76bc097b01b50d670`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:36:34 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 08:36:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 08:36:35 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 08:36:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 08:36:38 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 08:36:38 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 08:36:38 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 08:36:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 08:36:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 80
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 443
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 08:36:39 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 08:36:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ad552b06977a907a460096cd3aa8d4cad657ae3a90be3bc63eba494b31a255`  
		Last Modified: Sat, 16 Mar 2024 08:36:59 GMT  
		Size: 344.5 KB (344462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7eb11427d968ddc8915316bd59544b644278fd1c3960927ab066c8cc916a8b`  
		Last Modified: Sat, 16 Mar 2024 08:36:58 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a13a58310f383c1986a52280e47b5d9a59f7ef7f02bf39ff3b494af779dab9`  
		Last Modified: Sat, 16 Mar 2024 08:37:02 GMT  
		Size: 13.9 MB (13893734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:aaf3497a43eee2656c636b04c5ac7dd7f81e15e6911be1c0509fcc51df3e6dbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f62720e336d430f97f77dea70bb3ceacea271cb1d7f6a246eb3c366e509827`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:55:39 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 02:55:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 02:55:41 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 02:55:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 02:55:43 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 02:55:43 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 02:55:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 80
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 443
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 02:55:44 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 02:55:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef488aa53de475202749fc28d385b1e4e59841fe4085a7edee2eb5026d11b95c`  
		Last Modified: Sat, 16 Mar 2024 02:56:01 GMT  
		Size: 360.7 KB (360666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322174feb81fda6e9c1e8e8ac7e49b8e77de2dca870243af972ee7545d4b7916`  
		Last Modified: Sat, 16 Mar 2024 02:56:01 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3360e007ed3153df2f6fbc7ef89943b1fc701d62c811d8855293b7df0f352d`  
		Last Modified: Sat, 16 Mar 2024 02:56:02 GMT  
		Size: 13.6 MB (13568947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6` - linux; ppc64le

```console
$ docker pull caddy@sha256:00e289b4657ffa0aec2c98f544cf7890e6cf6e4bd9dd1adfc01697d5fbb436a6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17052079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717f7ea5ec28ca8fed34729b1466cd1f5f96309057a0ec85b2e903833000f9ac`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:55:44 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 15 Mar 2024 23:55:46 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 15 Mar 2024 23:55:47 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 15 Mar 2024 23:55:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 15 Mar 2024 23:55:51 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 15 Mar 2024 23:55:51 GMT
ENV XDG_DATA_HOME=/data
# Fri, 15 Mar 2024 23:55:52 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 15 Mar 2024 23:55:52 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 15 Mar 2024 23:55:52 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 15 Mar 2024 23:55:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 15 Mar 2024 23:55:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 15 Mar 2024 23:55:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 15 Mar 2024 23:55:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 15 Mar 2024 23:55:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 15 Mar 2024 23:55:54 GMT
EXPOSE 80
# Fri, 15 Mar 2024 23:55:55 GMT
EXPOSE 443
# Fri, 15 Mar 2024 23:55:55 GMT
EXPOSE 443/udp
# Fri, 15 Mar 2024 23:55:55 GMT
EXPOSE 2019
# Fri, 15 Mar 2024 23:55:56 GMT
WORKDIR /srv
# Fri, 15 Mar 2024 23:55:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d58b091eab1c134ec71c79ecd145766a6b85840017d1e2223575349179f742c`  
		Last Modified: Fri, 15 Mar 2024 23:56:22 GMT  
		Size: 362.2 KB (362200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cfe42e2461424bcaa647db536a9454b1c48bf3410add89e0ec0367328cff78`  
		Last Modified: Fri, 15 Mar 2024 23:56:22 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103d176f7ec2158a797ee8c4909124a9a7cc2b8cff9b8c59e7368d8730563728`  
		Last Modified: Fri, 15 Mar 2024 23:56:24 GMT  
		Size: 13.3 MB (13333863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6` - linux; s390x

```console
$ docker pull caddy@sha256:aabd334d2f437365b8585670694b9cbe711132d5937a3d7f14b5840ff92fbf55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17818312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dd63d90fd552a57206bdfb4bb41bc51fd60b881c3ffe41f0852c6bac9ef68e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:48:00 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 04:48:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 04:48:01 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 04:48:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 04:48:04 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 04:48:04 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 04:48:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 04:48:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 04:48:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 04:48:05 GMT
EXPOSE 80
# Sat, 27 Jan 2024 04:48:05 GMT
EXPOSE 443
# Sat, 27 Jan 2024 04:48:05 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 04:48:06 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 04:48:06 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 04:48:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e608a3e3404a06a0444cc06a7949f9a4a2c56e2983aced16d2d32f009f2dbc17`  
		Last Modified: Sat, 27 Jan 2024 04:50:42 GMT  
		Size: 354.9 KB (354944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addd52ad78c14ade7e55ee491d32b0e51556e0c0a8b84d1fd1abc3a1430cc057`  
		Last Modified: Sat, 27 Jan 2024 04:50:42 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e597a1de66b259ef54ca1d052f65d662a6ea3ebf545513d9c91e80c67aa1f3`  
		Last Modified: Sat, 27 Jan 2024 04:50:44 GMT  
		Size: 14.2 MB (14238310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:e92a98f9befbcc685cba6014745c4c4e5573d524f98646666afae41fe635a647
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1973514153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c02263e4345786d822a7cbe2109be66b8bbc405dad0088432e203c583cdb8c4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:37:25 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:37:26 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:37:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:37:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:37:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:37:54 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:37:55 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:37:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:37:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:37:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:38:00 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:38:01 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:38:03 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:38:21 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:38:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3433f0cddf0bf50f831ae26d44034fb9ccdaea63173630b59cbe9dc33860a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:45 GMT  
		Size: 471.5 KB (471467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39aa89107a4c1ac15acc37ba98faa00f98774062e839984cd569c84acccbefa`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903c57abacc03a4132d1914d83b140d91cad6d3f72113588dbb0449668e5459e`  
		Last Modified: Wed, 13 Mar 2024 02:41:47 GMT  
		Size: 15.3 MB (15272331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c505d8db5c54f9f5b13a230f310c78e1daa9f0fa5baa7db6bb4b6f9b2824c64`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02c7783ff4e4ea0351aa496f9316d007b5d39dd7ac091772a53c788cc850835`  
		Last Modified: Wed, 13 Mar 2024 02:41:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2f6f475cd8b631685eb3441f13c0418b595dc3f64fc43f4de103cd270bd07a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c099338186092d8e8a9ee4e1aef2ac6bac6e0e37d05b00acc2519d4828eebc1a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66be30fd26f10adf7753fc7287726b290417f432503173cc8cfcc37c5970eed5`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdecded462eba57ac719ddeaf73027953397d9470c8d9ce91486b650688448d1`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b196924a8268e867bced4e92552ad7a24d5079dd5d3a5f2d32e98acf5b94ec`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83e0533daa0143428320795f95f747a318ce9dfaec9c1918dc09ddabff7ce6`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d6f7d580438b0f330c60e990071ee0a7fd2cb8e861b5b3673229aae5f40a97`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3043316cf0d3543d7ad8c2cf29b9f42217a7ff7ee358b9ccf49ec1c2742b40dc`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9d07b35dd72d9c89f56d604b5b5ff1096607de0b699a7845b4d4eef4542999`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7138f2320f3eb26befb56422d151646fa73d61b45b1fd7ba1a97e97b12b1794`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dd6eb25db87e92a30fe3a646b0ca820c3a8a855af39f49e9c1239e9e7e8fa8`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff49c00e60e2791dac19058d6bba6e562c80b90859f8e91ae70b474a582042`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c28453d92f8177a5ca4103ba031b5f02ceb70269930e8642e8bda358f1eef11`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 289.3 KB (289264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5958cc3ab872a13ea8011a1ae0a2290cefbfb5721bf58c5c16e2a1dfa216aa`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:2a10673838e2beefb539398925457319c1e7800b242f5c261bc40ddd7f16aa33
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2141123401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001b000d65334996d09969a3e79ce6304b5ea6811c67eb7add59f0c78b73ba5c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:34:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:34:08 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:35:29 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:35:30 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:35:31 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:35:31 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:35:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:35:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:35:35 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:35:36 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:35:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:35:39 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:35:40 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:36:47 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:36:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bb323765ff7b405cedec6f88daa8a1c8470f45c358d637c0062cf4c63d7e07`  
		Last Modified: Wed, 13 Mar 2024 02:41:21 GMT  
		Size: 465.6 KB (465620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b3f11ec4ee425a6a0b9f5ad200c9193592181f59520c9a80372e647787163a`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ffe491a522455b1d95c1d0d3384188ea361064259fffcadd657bebae4fa934`  
		Last Modified: Wed, 13 Mar 2024 02:41:24 GMT  
		Size: 15.3 MB (15277213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b62af40926c0d1a37e6126f41f63533166809b5b54434cf3b53ab5734357e59`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a9b1639ec2e8588ca4fd94f87b31b4e30adef3c0ac45ea4ac0e4cdce643d6`  
		Last Modified: Wed, 13 Mar 2024 02:41:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7a48958fcb11d52bb7a65f60d6f322d3326d4f2916e0547b764cbe4fe0eae8`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9eb36d28260e8ba5549b16a87d121a4d7b0d38f46e1127ee1fd95f2e31e6f2c`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d221a46e4e966da289289be19ac425d0199540bef1d6d7c890ba45ec255e79`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feeda3213337ce81d383bcb08c0b241e763185b91a2e180f35c59395e3c0290f`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d7bf5ae3a283a09c7a385afa5160b2d0f1d275fc23e0a1711bf734511fe0b1`  
		Last Modified: Wed, 13 Mar 2024 02:41:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f309d19b55289fe422d64dd24736be59a52f6eba872d8fb1054416f8b5d9c553`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4ac1a4021eeee54512dde50b437001408fd1dda9d896f68d38728f7dba8c6c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e117655b528b6e8f7ce8d4d2cb69d41a1735fec0e31e10dc40cddcf0d012be`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5524c6d618843e710fa22d77e57a844c7cdfd68676c809d2d1ecde656c16a81c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879784be55be2c5d212302ae42232de9bfeaccea0b1398ec0101ef36d542930c`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f8aadcc42505eea344cf0504c7312d01033f159e88d6eadab5abb9eefc98a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41580c6cc25a82ee1a4de9315ec98ce6e89bd73461a941248648d04292e9ff52`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1261dc2b6b686493c5c3989f8efdd404b912398f6a38933aba80fe65d5d6240c`  
		Last Modified: Wed, 13 Mar 2024 02:41:15 GMT  
		Size: 258.2 KB (258159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8856855cc09ca543e8712766ea12d12556af369305babcaf786f620c89c3450d`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-alpine`

```console
$ docker pull caddy@sha256:dda81a416214d4dbdd978810efa19643e39b626fe0f979558fbb116758784c89
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
$ docker pull caddy@sha256:a6054d207060158cd0f019d6a35907bf47d1f8dacf58cdb63075a930d8ebca38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18467348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da4af4af9d73e970be3df873e00b8e658a7fc56ab982bfffa21d9bae68e3943`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:18:44 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 03:18:46 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 03:18:46 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 03:18:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 03:18:48 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 03:18:48 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 03:18:48 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 03:18:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 03:18:48 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 80
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 443
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 03:18:49 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 03:18:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a167b92bd92ca649523209f279d023d90edd2658f2dbbd5a79cd991b707a1bf4`  
		Last Modified: Sat, 16 Mar 2024 03:19:12 GMT  
		Size: 350.8 KB (350841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa65d2923419d52c79891c5c107216c8efc7534f740cafcddcb57fcd915fd61`  
		Last Modified: Sat, 16 Mar 2024 03:19:12 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832dc3f423aedf5c58d59571f7e5eebd543b4c31f0a0bacc36b509313473765e`  
		Last Modified: Sat, 16 Mar 2024 03:19:15 GMT  
		Size: 14.7 MB (14706436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:d5b956705aa5cb2d80a34b0da959c62f6e1b85d3b6af5d39bdd43a5ebad79732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17423235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637ed474101820123d027bf07c3bacd795eec60a114ec44aa0ab7c081f03fcdd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:36:00 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 06:36:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 06:36:01 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 06:36:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 06:36:04 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 06:36:04 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 06:36:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 06:36:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 06:36:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 80
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 443
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 06:36:05 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 06:36:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7e837cfa426b2a8d095055ea95ecda50deb35a29395410997280bf4efa14be`  
		Last Modified: Sat, 16 Mar 2024 06:36:25 GMT  
		Size: 347.6 KB (347629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aac6695e2937791ffb389edf1aee134b4e2e7c879173c70c5b0851017f402f5`  
		Last Modified: Sat, 16 Mar 2024 06:36:24 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a5dfabcee2609d8f2199b85fef83d4b0fa6612faa5a74b40f2809ccef87a5d`  
		Last Modified: Sat, 16 Mar 2024 06:36:27 GMT  
		Size: 13.9 MB (13921018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:d193bf8cf22c67a72ca3f4bc784363a0964ee0bc6481457a375beff0c515bb7b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17147117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c56baf0ceba318c0b5f456a51c90a5291492d8586689fa76bc097b01b50d670`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:36:34 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 08:36:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 08:36:35 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 08:36:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 08:36:38 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 08:36:38 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 08:36:38 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 08:36:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 08:36:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 80
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 443
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 08:36:39 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 08:36:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ad552b06977a907a460096cd3aa8d4cad657ae3a90be3bc63eba494b31a255`  
		Last Modified: Sat, 16 Mar 2024 08:36:59 GMT  
		Size: 344.5 KB (344462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7eb11427d968ddc8915316bd59544b644278fd1c3960927ab066c8cc916a8b`  
		Last Modified: Sat, 16 Mar 2024 08:36:58 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a13a58310f383c1986a52280e47b5d9a59f7ef7f02bf39ff3b494af779dab9`  
		Last Modified: Sat, 16 Mar 2024 08:37:02 GMT  
		Size: 13.9 MB (13893734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:aaf3497a43eee2656c636b04c5ac7dd7f81e15e6911be1c0509fcc51df3e6dbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f62720e336d430f97f77dea70bb3ceacea271cb1d7f6a246eb3c366e509827`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:55:39 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 02:55:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 02:55:41 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 02:55:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 02:55:43 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 02:55:43 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 02:55:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 80
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 443
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 02:55:44 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 02:55:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef488aa53de475202749fc28d385b1e4e59841fe4085a7edee2eb5026d11b95c`  
		Last Modified: Sat, 16 Mar 2024 02:56:01 GMT  
		Size: 360.7 KB (360666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322174feb81fda6e9c1e8e8ac7e49b8e77de2dca870243af972ee7545d4b7916`  
		Last Modified: Sat, 16 Mar 2024 02:56:01 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3360e007ed3153df2f6fbc7ef89943b1fc701d62c811d8855293b7df0f352d`  
		Last Modified: Sat, 16 Mar 2024 02:56:02 GMT  
		Size: 13.6 MB (13568947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:00e289b4657ffa0aec2c98f544cf7890e6cf6e4bd9dd1adfc01697d5fbb436a6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17052079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717f7ea5ec28ca8fed34729b1466cd1f5f96309057a0ec85b2e903833000f9ac`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:55:44 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 15 Mar 2024 23:55:46 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 15 Mar 2024 23:55:47 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 15 Mar 2024 23:55:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 15 Mar 2024 23:55:51 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 15 Mar 2024 23:55:51 GMT
ENV XDG_DATA_HOME=/data
# Fri, 15 Mar 2024 23:55:52 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 15 Mar 2024 23:55:52 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 15 Mar 2024 23:55:52 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 15 Mar 2024 23:55:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 15 Mar 2024 23:55:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 15 Mar 2024 23:55:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 15 Mar 2024 23:55:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 15 Mar 2024 23:55:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 15 Mar 2024 23:55:54 GMT
EXPOSE 80
# Fri, 15 Mar 2024 23:55:55 GMT
EXPOSE 443
# Fri, 15 Mar 2024 23:55:55 GMT
EXPOSE 443/udp
# Fri, 15 Mar 2024 23:55:55 GMT
EXPOSE 2019
# Fri, 15 Mar 2024 23:55:56 GMT
WORKDIR /srv
# Fri, 15 Mar 2024 23:55:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d58b091eab1c134ec71c79ecd145766a6b85840017d1e2223575349179f742c`  
		Last Modified: Fri, 15 Mar 2024 23:56:22 GMT  
		Size: 362.2 KB (362200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cfe42e2461424bcaa647db536a9454b1c48bf3410add89e0ec0367328cff78`  
		Last Modified: Fri, 15 Mar 2024 23:56:22 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103d176f7ec2158a797ee8c4909124a9a7cc2b8cff9b8c59e7368d8730563728`  
		Last Modified: Fri, 15 Mar 2024 23:56:24 GMT  
		Size: 13.3 MB (13333863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:aabd334d2f437365b8585670694b9cbe711132d5937a3d7f14b5840ff92fbf55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17818312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dd63d90fd552a57206bdfb4bb41bc51fd60b881c3ffe41f0852c6bac9ef68e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:48:00 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 04:48:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 04:48:01 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 04:48:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 04:48:04 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 04:48:04 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 04:48:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 04:48:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 04:48:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 04:48:05 GMT
EXPOSE 80
# Sat, 27 Jan 2024 04:48:05 GMT
EXPOSE 443
# Sat, 27 Jan 2024 04:48:05 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 04:48:06 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 04:48:06 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 04:48:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e608a3e3404a06a0444cc06a7949f9a4a2c56e2983aced16d2d32f009f2dbc17`  
		Last Modified: Sat, 27 Jan 2024 04:50:42 GMT  
		Size: 354.9 KB (354944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addd52ad78c14ade7e55ee491d32b0e51556e0c0a8b84d1fd1abc3a1430cc057`  
		Last Modified: Sat, 27 Jan 2024 04:50:42 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e597a1de66b259ef54ca1d052f65d662a6ea3ebf545513d9c91e80c67aa1f3`  
		Last Modified: Sat, 27 Jan 2024 04:50:44 GMT  
		Size: 14.2 MB (14238310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder`

```console
$ docker pull caddy@sha256:297a97b4f8f3f4467bcf9cfd5a6f5ba5bcfa38be56824c82e2c4f1c029701f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `caddy:2.7.6-builder` - linux; amd64

```console
$ docker pull caddy@sha256:a37704d2149bb703350b3e63704ecb468ec6f10cdc3784c818988e250484b2ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76973825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a6b943c698684ea914a9d08c8a00d2e573cbc2a95669142bc1b35350317cff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 03:18:55 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 03:18:55 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 03:18:55 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 03:18:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 03:18:55 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 03:18:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 03:18:57 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 03:18:57 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e791cb90c3d0bf08a988f13b405c9947c74b5bc31c7c939197a7175f6c7f0e`  
		Last Modified: Sat, 27 Jan 2024 01:36:33 GMT  
		Size: 284.7 KB (284690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3da9c61ef062502252a549dbc1f90925a8d7b6ef0644ffbfaea77be8b6f058`  
		Last Modified: Tue, 05 Mar 2024 19:25:57 GMT  
		Size: 67.0 MB (67010725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1741a7c0e9ce85801257b76332c08a3abdf5069bf46b0e764a32219d92189dc5`  
		Last Modified: Tue, 05 Mar 2024 19:25:45 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f302d3cc779898a1baa29b9dde46627021754a60a003a8ceb71b73f80af80bb2`  
		Last Modified: Sat, 16 Mar 2024 03:19:27 GMT  
		Size: 5.0 MB (4973021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51954c5f8bcd596606e74156291b16b5d0c2b430bb9f0a49db89dc03278cbd8e`  
		Last Modified: Sat, 16 Mar 2024 03:19:26 GMT  
		Size: 1.3 MB (1302235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351f34f77cd30086783b4d1e7bd91ac224af75f55690527012c4f114a65048b5`  
		Last Modified: Sat, 16 Mar 2024 03:19:26 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:042f6baf4a87f12037bf9a9146e994b03974edfdf6e94ef3a6c8ed9a5b0e01d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75407449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8104ab01bd342cfbbde6ad9a086efdba750ddaaeb6b4ce5acae4072b032808f1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 06:36:10 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 06:36:10 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 06:36:10 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 06:36:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 06:36:10 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 06:36:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 06:36:11 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 06:36:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18595ac3d5791e4d7e7dbcffcbf63e97e29974bd7191f7779889293f06709605`  
		Last Modified: Sat, 16 Mar 2024 01:27:12 GMT  
		Size: 284.9 KB (284879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67b0661c8b928f9ee07193e83a55962dc30ea03b3917d927fbfc6172db763d1`  
		Last Modified: Sat, 16 Mar 2024 01:28:25 GMT  
		Size: 65.8 MB (65767483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e94e3f035a7e84adb42051a6776fb957bb01e4afe261ef52850410749238c3e`  
		Last Modified: Sat, 16 Mar 2024 01:28:09 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90af61f594723149cbf4c52926248b7aa924edce2e71c1146dbfe1c4952d0e85`  
		Last Modified: Sat, 16 Mar 2024 06:36:39 GMT  
		Size: 5.0 MB (4958759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2b089f053b69b50a0ec1b57924c3f1dbab09af5f892a3f3824a1f1d91c4653`  
		Last Modified: Sat, 16 Mar 2024 06:36:39 GMT  
		Size: 1.2 MB (1248659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb3baf5a17563281d926d65bf039e75bafa0be92988b008e142f88f13e48831`  
		Last Modified: Sat, 16 Mar 2024 06:36:39 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:bba85446aa9cf082d96393b37ee2eb8948d32119f9f1b4a7de4264ed6265bc16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d75fc02eccf5b473914195c6b5a7f27a9c7b3af790feb14ca2afa4f0a1e6d2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 08:36:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 08:36:44 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 08:36:44 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 08:36:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 08:36:44 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 08:36:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 08:36:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 08:36:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03de95814623b83a4328b4db2e23b14214f57c18389a27379988469d9b6bbccc`  
		Last Modified: Sat, 16 Mar 2024 00:51:49 GMT  
		Size: 284.1 KB (284082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb316a6d2b1f8b686717aa026be6622630e91b4e2beff72260e41b9c26f5f328`  
		Last Modified: Sat, 16 Mar 2024 00:52:59 GMT  
		Size: 65.8 MB (65767446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3402119434a07f7977a54237330b21abbea9474c729d8bbbe43e79507612156`  
		Last Modified: Sat, 16 Mar 2024 00:52:46 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3e193cf2bcf63192347811ea80a7312b468b42f6341ff8912fb721dcdd07b1`  
		Last Modified: Sat, 16 Mar 2024 08:37:14 GMT  
		Size: 4.5 MB (4514679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302bab84b8a106df7129ce421df27645cf93461c26631a73c4c16dcc48213e33`  
		Last Modified: Sat, 16 Mar 2024 08:37:14 GMT  
		Size: 1.2 MB (1246087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa5da11b54d5792ea909f7bcbe533482069dd4540457779cb629671faadd4eb`  
		Last Modified: Sat, 16 Mar 2024 08:37:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:636495b6181fd6f900cfb1c3fafd4aa67ef8113e127a39c225dcd2b9f28018ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73993764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804083a23a5a42633ad7c22fc0b9908822db952792867afe4852db23de6882c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 02:55:47 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 02:55:48 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 02:55:48 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 02:55:48 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 02:55:48 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 02:55:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 02:55:49 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 02:55:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69c4102457739613c6fcb205a5a8e7dbc8383d57dade0a4502b1bca7b100a4d`  
		Last Modified: Sat, 16 Mar 2024 02:38:03 GMT  
		Size: 286.3 KB (286314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472e8443302a7aa2ee7c60f88cf1c1bff960c6982004fabf4d0b7dbb39552784`  
		Last Modified: Sat, 16 Mar 2024 02:38:55 GMT  
		Size: 64.1 MB (64111127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f3ae01babba08c7331e1311c66fc81f093559e9b48b75c7f09e492835df417`  
		Last Modified: Sat, 16 Mar 2024 02:38:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a47c8e46877caae3d8fa35784305f82b6173865f636c831581e413586174c9f`  
		Last Modified: Sat, 16 Mar 2024 02:56:14 GMT  
		Size: 5.1 MB (5063904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b458a517cc70120b5d5ad7b3624d14288f8fc2bb374503684e47dfb2d81ede41`  
		Last Modified: Sat, 16 Mar 2024 02:56:14 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e927a09144840e6a0520002506a03480353d2bf16acf387e392f67125a232f`  
		Last Modified: Sat, 16 Mar 2024 02:56:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:74036381f9b78d58ddddc74f279042dff06d05ac2b95c3faf063485eac603111
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74219852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afdeb2455afb0545182f73124c3e233abb4a6b803a834f42127d9a1eff4982c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 07:31:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 07:31:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 07:31:22 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 07:31:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 07:31:22 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 07:31:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 07:31:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 07:31:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e315e4c0ee7596e0eb7cc17d622c433e9fc4ef254b722e11e6794265328ea583`  
		Last Modified: Sat, 16 Mar 2024 00:32:12 GMT  
		Size: 286.7 KB (286670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee59a251903fa4e415f22830cd12da95ca1bcf671572b4a701a1d8f75a55d5ee`  
		Last Modified: Sat, 16 Mar 2024 00:33:15 GMT  
		Size: 64.1 MB (64126904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a227c25fca514ad52229d19315a3e0db7f235f9a840f9474237fadee44634bd1`  
		Last Modified: Sat, 16 Mar 2024 00:33:03 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da53f00025342b23cc1c1a712e9f3ff08b05bc0759f58b580a2081c4b925b9e8`  
		Last Modified: Sat, 16 Mar 2024 07:31:42 GMT  
		Size: 5.3 MB (5271003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1eb59d0f562ae579e22be9806e6ea172a7ee0399f354980329dfa3e8e04045`  
		Last Modified: Sat, 16 Mar 2024 07:31:41 GMT  
		Size: 1.2 MB (1186176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f27806532c2006d7f3b98c3ab37d72cf977ec4c488b65e389cb46e6b551627`  
		Last Modified: Sat, 16 Mar 2024 07:31:41 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; s390x

```console
$ docker pull caddy@sha256:179342439e20a0f8308f5b3c8f51063386fb33fb38d9eda738dfd1d4b398280c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76101838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4eddf19e318b73f4fa90802285b549c08b6b015cfc8f36a11adbbf9c593fc2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Tue, 05 Mar 2024 20:58:12 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:58:12 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:58:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:58:13 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:58:13 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1b6899ff00172fd5c809d57028913a3c5aead2c05d0c3c01b15a5249c4ddec`  
		Last Modified: Sat, 27 Jan 2024 05:46:31 GMT  
		Size: 285.1 KB (285091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192deec459dbc25471d5ce96dbf84de90f9e77914e5074081b4aba0516977050`  
		Last Modified: Tue, 05 Mar 2024 20:12:42 GMT  
		Size: 66.2 MB (66218961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e6d46fb71afdd9825fc4397b4949daac74f5a564377560ed3cb3bb910da97f`  
		Last Modified: Tue, 05 Mar 2024 20:12:31 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad42b5ce4497969e7a2ebbdf9ada284081c50ce1744927873987c8075ed117fa`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 5.1 MB (5117256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea105a4685d829ffde13e2d0e06f02ec7f1e1381059eae15941a5aeb36d5f7a7`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 1.3 MB (1262390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1423e2dcf9499ee1179b946513f3194740bf64ee1f24d0a7688bde92f8773874`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:deed166abe77b412a506924346166c58e03f6e35fb2836e7af244be01925eddf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2054342050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7b95fb04081aaf80026e1bb52d4a79df79ea5aac969382123b16607318419f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 01:46:04 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Mar 2024 01:46:05 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Mar 2024 01:46:06 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Mar 2024 01:46:07 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Mar 2024 01:46:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 01:46:43 GMT
ENV GOPATH=C:\go
# Wed, 13 Mar 2024 01:47:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Mar 2024 02:01:45 GMT
ENV GOLANG_VERSION=1.21.8
# Wed, 13 Mar 2024 02:04:07 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 02:04:09 GMT
WORKDIR C:\go
# Wed, 13 Mar 2024 02:40:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:40:13 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 13 Mar 2024 02:40:14 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:40:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 13 Mar 2024 02:40:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 13 Mar 2024 02:40:40 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0a2d972d6c007b69f2c3ea41c1fe5fad6b189bfe40efacdcaf910b884fb6bb`  
		Last Modified: Wed, 13 Mar 2024 02:13:35 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f3068df504cd61566fc5e038c996322e35f58e08e0c6ef6ce589b11de4eb93`  
		Last Modified: Wed, 13 Mar 2024 02:13:34 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98750f7d798b8a0b5199088d4860bce5d51320b2fc07440f211ec692f4bf63b4`  
		Last Modified: Wed, 13 Mar 2024 02:13:33 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e43d1ea980f98746869d1942fc459ed402f307d4de5c435e325d2c9d534e99`  
		Last Modified: Wed, 13 Mar 2024 02:13:33 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fc4a2ae5d19f3b766991bfec5347bd5192c19ede11e7dfbf8b7d698fc1323d`  
		Last Modified: Wed, 13 Mar 2024 02:13:38 GMT  
		Size: 25.6 MB (25551948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251908e7b1f95da24e9f4ec7c727a2662105696c9de2925ab36938572cfb9f79`  
		Last Modified: Wed, 13 Mar 2024 02:13:31 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2927b1ac917c6e3261034f1c0cbb347c73f26593e997c505dfd04da18f966c1a`  
		Last Modified: Wed, 13 Mar 2024 02:13:31 GMT  
		Size: 273.7 KB (273727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5d297a0f5c09416c27b06ff859cb837506ffabdf0faa0cb5112e0a34839aab`  
		Last Modified: Wed, 13 Mar 2024 02:15:44 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1412d17e78321071b9d6a4dbb609e6a24c2e829a90ed9ca7e20a72ede74d04`  
		Last Modified: Wed, 13 Mar 2024 02:16:03 GMT  
		Size: 69.4 MB (69363257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619eb2756fc98681ecf9e1220a72f64f2e3f3fe9e72edd3a6021ad0249b9b2a5`  
		Last Modified: Wed, 13 Mar 2024 02:15:44 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf19d565f6ad05c073e69610b1e850eaf1a6aa6806195ea601c4a47303140d27`  
		Last Modified: Wed, 13 Mar 2024 02:42:22 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279cafbdd3019482f630ef1d502ea930d8ee1cfd8f9977bb52059c87ddff7a55`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e9d1117318fed479ece2fe1c6f9b896efcca03021ea368d722153aca1f8bc9`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d106feccb912e361adb23c8a586aad6b6c8493698e3893f4b1a2cd40bdd03cb4`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e766bc3c556143c937c2d95209a8d6370902ee4f31471f2a35c4d7045d361af6`  
		Last Modified: Wed, 13 Mar 2024 02:42:20 GMT  
		Size: 1.7 MB (1676188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39236cd34ad31ef892f22ac798c76cb384eb17ff72d5881539cbee398708be72`  
		Last Modified: Wed, 13 Mar 2024 02:42:20 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:53d965e8f604060a1c65cdf2a722300b8ff2f7a36494b6c0ba0c315fc7ffd2c2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221957582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0daee73c43fffad7bf7cfb8399d58db63aaa5f6727affb62b8d370b9760df81f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 01:49:48 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Mar 2024 01:49:49 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Mar 2024 01:49:50 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Mar 2024 01:49:51 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Mar 2024 01:51:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 01:51:29 GMT
ENV GOPATH=C:\go
# Wed, 13 Mar 2024 01:52:49 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Mar 2024 02:04:28 GMT
ENV GOLANG_VERSION=1.21.8
# Wed, 13 Mar 2024 02:07:38 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 02:07:39 GMT
WORKDIR C:\go
# Wed, 13 Mar 2024 02:38:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:38:30 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 13 Mar 2024 02:38:31 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:38:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 13 Mar 2024 02:39:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 13 Mar 2024 02:39:54 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc39f00be83bc8d2b0e0f2123fce0278f495e47f8a969bf03ec57df5f98cbda`  
		Last Modified: Wed, 13 Mar 2024 02:14:08 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f8b9e441646ef17118a0d394fa50244ef70c9e053c5b7d33e648796c8df90e`  
		Last Modified: Wed, 13 Mar 2024 02:14:07 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8759cd20778bf436a14e59cb31806b28212fcd510d8de32d44e49a9f39656f3d`  
		Last Modified: Wed, 13 Mar 2024 02:14:06 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d99a22ebabf5f80d07ad166a24eace1c2fa31cef2566a179bfec0d6407513e`  
		Last Modified: Wed, 13 Mar 2024 02:14:06 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfdb963b4125b258828e1fbac783c993a6845ad94973fad173f5dd25be3c34b`  
		Last Modified: Wed, 13 Mar 2024 02:14:12 GMT  
		Size: 25.5 MB (25540238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae89960ac90d33a751006d43faf1cbd1309b448658a447bb19dddabdbee17a9`  
		Last Modified: Wed, 13 Mar 2024 02:14:04 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff0bdcb61a7230b8b00d6e08d739c64fc0342dc675ed99fe6d35885cf1aa369`  
		Last Modified: Wed, 13 Mar 2024 02:14:05 GMT  
		Size: 272.6 KB (272572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c052d4b938689fbc1637386d1e61efa391787bd8128ee6d093464bad09b0231`  
		Last Modified: Wed, 13 Mar 2024 02:16:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e82772a8bffddc9f4a46c65cfa48f47938d84feb3730231762158c98014e47a`  
		Last Modified: Wed, 13 Mar 2024 02:16:31 GMT  
		Size: 69.4 MB (69350702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbffcc4012ecf27a404cc40eb63c43a880ad5104a82ee619fd0669acb2b5a710`  
		Last Modified: Wed, 13 Mar 2024 02:16:12 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fcd0eeed9adb7d9bf391df7f194150cb8ee56a63bc679cf147a14185381c3b`  
		Last Modified: Wed, 13 Mar 2024 02:42:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d74d351932d9ba6c92c9398e69d6736df75938a6ba3b7f1055206a1ed80b48`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db51f1e77d8641618afadb6f8c1ad073c4f72bb79099a00b0cabcbc8f5579248`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43620705f408ca0a7894137080f7947cc45d10badb0c7668ae1d46464494001b`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdaa0771d9c8b704195f821c3a9c23a5d9ff5e7e9b29335b835ce237f9d4dd50`  
		Last Modified: Wed, 13 Mar 2024 02:42:03 GMT  
		Size: 1.7 MB (1676257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010496734b493d0bc1b1a73566306e98777144ff64c5c886cf84de3af4fd971b`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder-alpine`

```console
$ docker pull caddy@sha256:8308bb619e5ff5bc1842b8fc8480bb1584220a0c241f125727fa844918aac505
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
$ docker pull caddy@sha256:a37704d2149bb703350b3e63704ecb468ec6f10cdc3784c818988e250484b2ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76973825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a6b943c698684ea914a9d08c8a00d2e573cbc2a95669142bc1b35350317cff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 03:18:55 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 03:18:55 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 03:18:55 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 03:18:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 03:18:55 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 03:18:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 03:18:57 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 03:18:57 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e791cb90c3d0bf08a988f13b405c9947c74b5bc31c7c939197a7175f6c7f0e`  
		Last Modified: Sat, 27 Jan 2024 01:36:33 GMT  
		Size: 284.7 KB (284690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3da9c61ef062502252a549dbc1f90925a8d7b6ef0644ffbfaea77be8b6f058`  
		Last Modified: Tue, 05 Mar 2024 19:25:57 GMT  
		Size: 67.0 MB (67010725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1741a7c0e9ce85801257b76332c08a3abdf5069bf46b0e764a32219d92189dc5`  
		Last Modified: Tue, 05 Mar 2024 19:25:45 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f302d3cc779898a1baa29b9dde46627021754a60a003a8ceb71b73f80af80bb2`  
		Last Modified: Sat, 16 Mar 2024 03:19:27 GMT  
		Size: 5.0 MB (4973021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51954c5f8bcd596606e74156291b16b5d0c2b430bb9f0a49db89dc03278cbd8e`  
		Last Modified: Sat, 16 Mar 2024 03:19:26 GMT  
		Size: 1.3 MB (1302235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351f34f77cd30086783b4d1e7bd91ac224af75f55690527012c4f114a65048b5`  
		Last Modified: Sat, 16 Mar 2024 03:19:26 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:042f6baf4a87f12037bf9a9146e994b03974edfdf6e94ef3a6c8ed9a5b0e01d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75407449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8104ab01bd342cfbbde6ad9a086efdba750ddaaeb6b4ce5acae4072b032808f1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 06:36:10 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 06:36:10 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 06:36:10 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 06:36:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 06:36:10 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 06:36:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 06:36:11 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 06:36:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18595ac3d5791e4d7e7dbcffcbf63e97e29974bd7191f7779889293f06709605`  
		Last Modified: Sat, 16 Mar 2024 01:27:12 GMT  
		Size: 284.9 KB (284879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67b0661c8b928f9ee07193e83a55962dc30ea03b3917d927fbfc6172db763d1`  
		Last Modified: Sat, 16 Mar 2024 01:28:25 GMT  
		Size: 65.8 MB (65767483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e94e3f035a7e84adb42051a6776fb957bb01e4afe261ef52850410749238c3e`  
		Last Modified: Sat, 16 Mar 2024 01:28:09 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90af61f594723149cbf4c52926248b7aa924edce2e71c1146dbfe1c4952d0e85`  
		Last Modified: Sat, 16 Mar 2024 06:36:39 GMT  
		Size: 5.0 MB (4958759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2b089f053b69b50a0ec1b57924c3f1dbab09af5f892a3f3824a1f1d91c4653`  
		Last Modified: Sat, 16 Mar 2024 06:36:39 GMT  
		Size: 1.2 MB (1248659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb3baf5a17563281d926d65bf039e75bafa0be92988b008e142f88f13e48831`  
		Last Modified: Sat, 16 Mar 2024 06:36:39 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:bba85446aa9cf082d96393b37ee2eb8948d32119f9f1b4a7de4264ed6265bc16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d75fc02eccf5b473914195c6b5a7f27a9c7b3af790feb14ca2afa4f0a1e6d2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 08:36:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 08:36:44 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 08:36:44 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 08:36:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 08:36:44 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 08:36:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 08:36:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 08:36:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03de95814623b83a4328b4db2e23b14214f57c18389a27379988469d9b6bbccc`  
		Last Modified: Sat, 16 Mar 2024 00:51:49 GMT  
		Size: 284.1 KB (284082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb316a6d2b1f8b686717aa026be6622630e91b4e2beff72260e41b9c26f5f328`  
		Last Modified: Sat, 16 Mar 2024 00:52:59 GMT  
		Size: 65.8 MB (65767446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3402119434a07f7977a54237330b21abbea9474c729d8bbbe43e79507612156`  
		Last Modified: Sat, 16 Mar 2024 00:52:46 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3e193cf2bcf63192347811ea80a7312b468b42f6341ff8912fb721dcdd07b1`  
		Last Modified: Sat, 16 Mar 2024 08:37:14 GMT  
		Size: 4.5 MB (4514679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302bab84b8a106df7129ce421df27645cf93461c26631a73c4c16dcc48213e33`  
		Last Modified: Sat, 16 Mar 2024 08:37:14 GMT  
		Size: 1.2 MB (1246087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa5da11b54d5792ea909f7bcbe533482069dd4540457779cb629671faadd4eb`  
		Last Modified: Sat, 16 Mar 2024 08:37:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:636495b6181fd6f900cfb1c3fafd4aa67ef8113e127a39c225dcd2b9f28018ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73993764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804083a23a5a42633ad7c22fc0b9908822db952792867afe4852db23de6882c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 02:55:47 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 02:55:48 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 02:55:48 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 02:55:48 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 02:55:48 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 02:55:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 02:55:49 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 02:55:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69c4102457739613c6fcb205a5a8e7dbc8383d57dade0a4502b1bca7b100a4d`  
		Last Modified: Sat, 16 Mar 2024 02:38:03 GMT  
		Size: 286.3 KB (286314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472e8443302a7aa2ee7c60f88cf1c1bff960c6982004fabf4d0b7dbb39552784`  
		Last Modified: Sat, 16 Mar 2024 02:38:55 GMT  
		Size: 64.1 MB (64111127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f3ae01babba08c7331e1311c66fc81f093559e9b48b75c7f09e492835df417`  
		Last Modified: Sat, 16 Mar 2024 02:38:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a47c8e46877caae3d8fa35784305f82b6173865f636c831581e413586174c9f`  
		Last Modified: Sat, 16 Mar 2024 02:56:14 GMT  
		Size: 5.1 MB (5063904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b458a517cc70120b5d5ad7b3624d14288f8fc2bb374503684e47dfb2d81ede41`  
		Last Modified: Sat, 16 Mar 2024 02:56:14 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e927a09144840e6a0520002506a03480353d2bf16acf387e392f67125a232f`  
		Last Modified: Sat, 16 Mar 2024 02:56:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:74036381f9b78d58ddddc74f279042dff06d05ac2b95c3faf063485eac603111
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74219852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afdeb2455afb0545182f73124c3e233abb4a6b803a834f42127d9a1eff4982c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 07:31:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 07:31:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 07:31:22 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 07:31:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 07:31:22 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 07:31:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 07:31:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 07:31:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e315e4c0ee7596e0eb7cc17d622c433e9fc4ef254b722e11e6794265328ea583`  
		Last Modified: Sat, 16 Mar 2024 00:32:12 GMT  
		Size: 286.7 KB (286670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee59a251903fa4e415f22830cd12da95ca1bcf671572b4a701a1d8f75a55d5ee`  
		Last Modified: Sat, 16 Mar 2024 00:33:15 GMT  
		Size: 64.1 MB (64126904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a227c25fca514ad52229d19315a3e0db7f235f9a840f9474237fadee44634bd1`  
		Last Modified: Sat, 16 Mar 2024 00:33:03 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da53f00025342b23cc1c1a712e9f3ff08b05bc0759f58b580a2081c4b925b9e8`  
		Last Modified: Sat, 16 Mar 2024 07:31:42 GMT  
		Size: 5.3 MB (5271003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1eb59d0f562ae579e22be9806e6ea172a7ee0399f354980329dfa3e8e04045`  
		Last Modified: Sat, 16 Mar 2024 07:31:41 GMT  
		Size: 1.2 MB (1186176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f27806532c2006d7f3b98c3ab37d72cf977ec4c488b65e389cb46e6b551627`  
		Last Modified: Sat, 16 Mar 2024 07:31:41 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:179342439e20a0f8308f5b3c8f51063386fb33fb38d9eda738dfd1d4b398280c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76101838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4eddf19e318b73f4fa90802285b549c08b6b015cfc8f36a11adbbf9c593fc2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Tue, 05 Mar 2024 20:58:12 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:58:12 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:58:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:58:13 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:58:13 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1b6899ff00172fd5c809d57028913a3c5aead2c05d0c3c01b15a5249c4ddec`  
		Last Modified: Sat, 27 Jan 2024 05:46:31 GMT  
		Size: 285.1 KB (285091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192deec459dbc25471d5ce96dbf84de90f9e77914e5074081b4aba0516977050`  
		Last Modified: Tue, 05 Mar 2024 20:12:42 GMT  
		Size: 66.2 MB (66218961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e6d46fb71afdd9825fc4397b4949daac74f5a564377560ed3cb3bb910da97f`  
		Last Modified: Tue, 05 Mar 2024 20:12:31 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad42b5ce4497969e7a2ebbdf9ada284081c50ce1744927873987c8075ed117fa`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 5.1 MB (5117256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea105a4685d829ffde13e2d0e06f02ec7f1e1381059eae15941a5aeb36d5f7a7`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 1.3 MB (1262390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1423e2dcf9499ee1179b946513f3194740bf64ee1f24d0a7688bde92f8773874`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:88480ae6cc843e1f4d7891d869f95182848a5414c6545cc2662d466a7c8dfdd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `caddy:2.7.6-builder-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:53d965e8f604060a1c65cdf2a722300b8ff2f7a36494b6c0ba0c315fc7ffd2c2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221957582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0daee73c43fffad7bf7cfb8399d58db63aaa5f6727affb62b8d370b9760df81f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 01:49:48 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Mar 2024 01:49:49 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Mar 2024 01:49:50 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Mar 2024 01:49:51 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Mar 2024 01:51:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 01:51:29 GMT
ENV GOPATH=C:\go
# Wed, 13 Mar 2024 01:52:49 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Mar 2024 02:04:28 GMT
ENV GOLANG_VERSION=1.21.8
# Wed, 13 Mar 2024 02:07:38 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 02:07:39 GMT
WORKDIR C:\go
# Wed, 13 Mar 2024 02:38:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:38:30 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 13 Mar 2024 02:38:31 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:38:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 13 Mar 2024 02:39:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 13 Mar 2024 02:39:54 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc39f00be83bc8d2b0e0f2123fce0278f495e47f8a969bf03ec57df5f98cbda`  
		Last Modified: Wed, 13 Mar 2024 02:14:08 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f8b9e441646ef17118a0d394fa50244ef70c9e053c5b7d33e648796c8df90e`  
		Last Modified: Wed, 13 Mar 2024 02:14:07 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8759cd20778bf436a14e59cb31806b28212fcd510d8de32d44e49a9f39656f3d`  
		Last Modified: Wed, 13 Mar 2024 02:14:06 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d99a22ebabf5f80d07ad166a24eace1c2fa31cef2566a179bfec0d6407513e`  
		Last Modified: Wed, 13 Mar 2024 02:14:06 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfdb963b4125b258828e1fbac783c993a6845ad94973fad173f5dd25be3c34b`  
		Last Modified: Wed, 13 Mar 2024 02:14:12 GMT  
		Size: 25.5 MB (25540238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae89960ac90d33a751006d43faf1cbd1309b448658a447bb19dddabdbee17a9`  
		Last Modified: Wed, 13 Mar 2024 02:14:04 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff0bdcb61a7230b8b00d6e08d739c64fc0342dc675ed99fe6d35885cf1aa369`  
		Last Modified: Wed, 13 Mar 2024 02:14:05 GMT  
		Size: 272.6 KB (272572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c052d4b938689fbc1637386d1e61efa391787bd8128ee6d093464bad09b0231`  
		Last Modified: Wed, 13 Mar 2024 02:16:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e82772a8bffddc9f4a46c65cfa48f47938d84feb3730231762158c98014e47a`  
		Last Modified: Wed, 13 Mar 2024 02:16:31 GMT  
		Size: 69.4 MB (69350702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbffcc4012ecf27a404cc40eb63c43a880ad5104a82ee619fd0669acb2b5a710`  
		Last Modified: Wed, 13 Mar 2024 02:16:12 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fcd0eeed9adb7d9bf391df7f194150cb8ee56a63bc679cf147a14185381c3b`  
		Last Modified: Wed, 13 Mar 2024 02:42:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d74d351932d9ba6c92c9398e69d6736df75938a6ba3b7f1055206a1ed80b48`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db51f1e77d8641618afadb6f8c1ad073c4f72bb79099a00b0cabcbc8f5579248`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43620705f408ca0a7894137080f7947cc45d10badb0c7668ae1d46464494001b`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdaa0771d9c8b704195f821c3a9c23a5d9ff5e7e9b29335b835ce237f9d4dd50`  
		Last Modified: Wed, 13 Mar 2024 02:42:03 GMT  
		Size: 1.7 MB (1676257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010496734b493d0bc1b1a73566306e98777144ff64c5c886cf84de3af4fd971b`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:7904ec0c624b28630437b42e793d0e1bc2472c348c79b15b26d065162eafd9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `caddy:2.7.6-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:deed166abe77b412a506924346166c58e03f6e35fb2836e7af244be01925eddf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2054342050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7b95fb04081aaf80026e1bb52d4a79df79ea5aac969382123b16607318419f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 01:46:04 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Mar 2024 01:46:05 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Mar 2024 01:46:06 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Mar 2024 01:46:07 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Mar 2024 01:46:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 01:46:43 GMT
ENV GOPATH=C:\go
# Wed, 13 Mar 2024 01:47:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Mar 2024 02:01:45 GMT
ENV GOLANG_VERSION=1.21.8
# Wed, 13 Mar 2024 02:04:07 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 02:04:09 GMT
WORKDIR C:\go
# Wed, 13 Mar 2024 02:40:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:40:13 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 13 Mar 2024 02:40:14 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:40:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 13 Mar 2024 02:40:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 13 Mar 2024 02:40:40 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0a2d972d6c007b69f2c3ea41c1fe5fad6b189bfe40efacdcaf910b884fb6bb`  
		Last Modified: Wed, 13 Mar 2024 02:13:35 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f3068df504cd61566fc5e038c996322e35f58e08e0c6ef6ce589b11de4eb93`  
		Last Modified: Wed, 13 Mar 2024 02:13:34 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98750f7d798b8a0b5199088d4860bce5d51320b2fc07440f211ec692f4bf63b4`  
		Last Modified: Wed, 13 Mar 2024 02:13:33 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e43d1ea980f98746869d1942fc459ed402f307d4de5c435e325d2c9d534e99`  
		Last Modified: Wed, 13 Mar 2024 02:13:33 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fc4a2ae5d19f3b766991bfec5347bd5192c19ede11e7dfbf8b7d698fc1323d`  
		Last Modified: Wed, 13 Mar 2024 02:13:38 GMT  
		Size: 25.6 MB (25551948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251908e7b1f95da24e9f4ec7c727a2662105696c9de2925ab36938572cfb9f79`  
		Last Modified: Wed, 13 Mar 2024 02:13:31 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2927b1ac917c6e3261034f1c0cbb347c73f26593e997c505dfd04da18f966c1a`  
		Last Modified: Wed, 13 Mar 2024 02:13:31 GMT  
		Size: 273.7 KB (273727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5d297a0f5c09416c27b06ff859cb837506ffabdf0faa0cb5112e0a34839aab`  
		Last Modified: Wed, 13 Mar 2024 02:15:44 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1412d17e78321071b9d6a4dbb609e6a24c2e829a90ed9ca7e20a72ede74d04`  
		Last Modified: Wed, 13 Mar 2024 02:16:03 GMT  
		Size: 69.4 MB (69363257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619eb2756fc98681ecf9e1220a72f64f2e3f3fe9e72edd3a6021ad0249b9b2a5`  
		Last Modified: Wed, 13 Mar 2024 02:15:44 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf19d565f6ad05c073e69610b1e850eaf1a6aa6806195ea601c4a47303140d27`  
		Last Modified: Wed, 13 Mar 2024 02:42:22 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279cafbdd3019482f630ef1d502ea930d8ee1cfd8f9977bb52059c87ddff7a55`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e9d1117318fed479ece2fe1c6f9b896efcca03021ea368d722153aca1f8bc9`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d106feccb912e361adb23c8a586aad6b6c8493698e3893f4b1a2cd40bdd03cb4`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e766bc3c556143c937c2d95209a8d6370902ee4f31471f2a35c4d7045d361af6`  
		Last Modified: Wed, 13 Mar 2024 02:42:20 GMT  
		Size: 1.7 MB (1676188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39236cd34ad31ef892f22ac798c76cb384eb17ff72d5881539cbee398708be72`  
		Last Modified: Wed, 13 Mar 2024 02:42:20 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-windowsservercore`

```console
$ docker pull caddy@sha256:02e4ec422a43bbe257c0b6f52bc54f9e391ac2ed078f86fc4d80269ca8ef3533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `caddy:2.7.6-windowsservercore` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:e92a98f9befbcc685cba6014745c4c4e5573d524f98646666afae41fe635a647
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1973514153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c02263e4345786d822a7cbe2109be66b8bbc405dad0088432e203c583cdb8c4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:37:25 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:37:26 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:37:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:37:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:37:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:37:54 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:37:55 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:37:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:37:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:37:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:38:00 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:38:01 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:38:03 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:38:21 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:38:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3433f0cddf0bf50f831ae26d44034fb9ccdaea63173630b59cbe9dc33860a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:45 GMT  
		Size: 471.5 KB (471467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39aa89107a4c1ac15acc37ba98faa00f98774062e839984cd569c84acccbefa`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903c57abacc03a4132d1914d83b140d91cad6d3f72113588dbb0449668e5459e`  
		Last Modified: Wed, 13 Mar 2024 02:41:47 GMT  
		Size: 15.3 MB (15272331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c505d8db5c54f9f5b13a230f310c78e1daa9f0fa5baa7db6bb4b6f9b2824c64`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02c7783ff4e4ea0351aa496f9316d007b5d39dd7ac091772a53c788cc850835`  
		Last Modified: Wed, 13 Mar 2024 02:41:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2f6f475cd8b631685eb3441f13c0418b595dc3f64fc43f4de103cd270bd07a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c099338186092d8e8a9ee4e1aef2ac6bac6e0e37d05b00acc2519d4828eebc1a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66be30fd26f10adf7753fc7287726b290417f432503173cc8cfcc37c5970eed5`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdecded462eba57ac719ddeaf73027953397d9470c8d9ce91486b650688448d1`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b196924a8268e867bced4e92552ad7a24d5079dd5d3a5f2d32e98acf5b94ec`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83e0533daa0143428320795f95f747a318ce9dfaec9c1918dc09ddabff7ce6`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d6f7d580438b0f330c60e990071ee0a7fd2cb8e861b5b3673229aae5f40a97`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3043316cf0d3543d7ad8c2cf29b9f42217a7ff7ee358b9ccf49ec1c2742b40dc`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9d07b35dd72d9c89f56d604b5b5ff1096607de0b699a7845b4d4eef4542999`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7138f2320f3eb26befb56422d151646fa73d61b45b1fd7ba1a97e97b12b1794`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dd6eb25db87e92a30fe3a646b0ca820c3a8a855af39f49e9c1239e9e7e8fa8`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff49c00e60e2791dac19058d6bba6e562c80b90859f8e91ae70b474a582042`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c28453d92f8177a5ca4103ba031b5f02ceb70269930e8642e8bda358f1eef11`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 289.3 KB (289264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5958cc3ab872a13ea8011a1ae0a2290cefbfb5721bf58c5c16e2a1dfa216aa`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-windowsservercore` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:2a10673838e2beefb539398925457319c1e7800b242f5c261bc40ddd7f16aa33
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2141123401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001b000d65334996d09969a3e79ce6304b5ea6811c67eb7add59f0c78b73ba5c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:34:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:34:08 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:35:29 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:35:30 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:35:31 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:35:31 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:35:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:35:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:35:35 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:35:36 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:35:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:35:39 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:35:40 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:36:47 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:36:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bb323765ff7b405cedec6f88daa8a1c8470f45c358d637c0062cf4c63d7e07`  
		Last Modified: Wed, 13 Mar 2024 02:41:21 GMT  
		Size: 465.6 KB (465620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b3f11ec4ee425a6a0b9f5ad200c9193592181f59520c9a80372e647787163a`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ffe491a522455b1d95c1d0d3384188ea361064259fffcadd657bebae4fa934`  
		Last Modified: Wed, 13 Mar 2024 02:41:24 GMT  
		Size: 15.3 MB (15277213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b62af40926c0d1a37e6126f41f63533166809b5b54434cf3b53ab5734357e59`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a9b1639ec2e8588ca4fd94f87b31b4e30adef3c0ac45ea4ac0e4cdce643d6`  
		Last Modified: Wed, 13 Mar 2024 02:41:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7a48958fcb11d52bb7a65f60d6f322d3326d4f2916e0547b764cbe4fe0eae8`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9eb36d28260e8ba5549b16a87d121a4d7b0d38f46e1127ee1fd95f2e31e6f2c`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d221a46e4e966da289289be19ac425d0199540bef1d6d7c890ba45ec255e79`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feeda3213337ce81d383bcb08c0b241e763185b91a2e180f35c59395e3c0290f`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d7bf5ae3a283a09c7a385afa5160b2d0f1d275fc23e0a1711bf734511fe0b1`  
		Last Modified: Wed, 13 Mar 2024 02:41:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f309d19b55289fe422d64dd24736be59a52f6eba872d8fb1054416f8b5d9c553`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4ac1a4021eeee54512dde50b437001408fd1dda9d896f68d38728f7dba8c6c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e117655b528b6e8f7ce8d4d2cb69d41a1735fec0e31e10dc40cddcf0d012be`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5524c6d618843e710fa22d77e57a844c7cdfd68676c809d2d1ecde656c16a81c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879784be55be2c5d212302ae42232de9bfeaccea0b1398ec0101ef36d542930c`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f8aadcc42505eea344cf0504c7312d01033f159e88d6eadab5abb9eefc98a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41580c6cc25a82ee1a4de9315ec98ce6e89bd73461a941248648d04292e9ff52`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1261dc2b6b686493c5c3989f8efdd404b912398f6a38933aba80fe65d5d6240c`  
		Last Modified: Wed, 13 Mar 2024 02:41:15 GMT  
		Size: 258.2 KB (258159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8856855cc09ca543e8712766ea12d12556af369305babcaf786f620c89c3450d`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-windowsservercore-1809`

```console
$ docker pull caddy@sha256:3e51c662d70a2bcf344a51331fb88b7d223db9cc683b01463633782351400cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `caddy:2.7.6-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:2a10673838e2beefb539398925457319c1e7800b242f5c261bc40ddd7f16aa33
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2141123401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001b000d65334996d09969a3e79ce6304b5ea6811c67eb7add59f0c78b73ba5c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:34:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:34:08 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:35:29 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:35:30 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:35:31 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:35:31 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:35:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:35:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:35:35 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:35:36 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:35:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:35:39 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:35:40 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:36:47 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:36:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bb323765ff7b405cedec6f88daa8a1c8470f45c358d637c0062cf4c63d7e07`  
		Last Modified: Wed, 13 Mar 2024 02:41:21 GMT  
		Size: 465.6 KB (465620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b3f11ec4ee425a6a0b9f5ad200c9193592181f59520c9a80372e647787163a`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ffe491a522455b1d95c1d0d3384188ea361064259fffcadd657bebae4fa934`  
		Last Modified: Wed, 13 Mar 2024 02:41:24 GMT  
		Size: 15.3 MB (15277213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b62af40926c0d1a37e6126f41f63533166809b5b54434cf3b53ab5734357e59`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a9b1639ec2e8588ca4fd94f87b31b4e30adef3c0ac45ea4ac0e4cdce643d6`  
		Last Modified: Wed, 13 Mar 2024 02:41:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7a48958fcb11d52bb7a65f60d6f322d3326d4f2916e0547b764cbe4fe0eae8`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9eb36d28260e8ba5549b16a87d121a4d7b0d38f46e1127ee1fd95f2e31e6f2c`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d221a46e4e966da289289be19ac425d0199540bef1d6d7c890ba45ec255e79`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feeda3213337ce81d383bcb08c0b241e763185b91a2e180f35c59395e3c0290f`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d7bf5ae3a283a09c7a385afa5160b2d0f1d275fc23e0a1711bf734511fe0b1`  
		Last Modified: Wed, 13 Mar 2024 02:41:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f309d19b55289fe422d64dd24736be59a52f6eba872d8fb1054416f8b5d9c553`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4ac1a4021eeee54512dde50b437001408fd1dda9d896f68d38728f7dba8c6c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e117655b528b6e8f7ce8d4d2cb69d41a1735fec0e31e10dc40cddcf0d012be`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5524c6d618843e710fa22d77e57a844c7cdfd68676c809d2d1ecde656c16a81c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879784be55be2c5d212302ae42232de9bfeaccea0b1398ec0101ef36d542930c`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f8aadcc42505eea344cf0504c7312d01033f159e88d6eadab5abb9eefc98a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41580c6cc25a82ee1a4de9315ec98ce6e89bd73461a941248648d04292e9ff52`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1261dc2b6b686493c5c3989f8efdd404b912398f6a38933aba80fe65d5d6240c`  
		Last Modified: Wed, 13 Mar 2024 02:41:15 GMT  
		Size: 258.2 KB (258159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8856855cc09ca543e8712766ea12d12556af369305babcaf786f620c89c3450d`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:e56fe39382d5d420f2ca9e2758ad977fc5a521e371d1658d8f98d8fd55615b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `caddy:2.7.6-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:e92a98f9befbcc685cba6014745c4c4e5573d524f98646666afae41fe635a647
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1973514153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c02263e4345786d822a7cbe2109be66b8bbc405dad0088432e203c583cdb8c4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:37:25 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:37:26 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:37:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:37:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:37:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:37:54 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:37:55 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:37:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:37:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:37:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:38:00 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:38:01 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:38:03 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:38:21 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:38:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3433f0cddf0bf50f831ae26d44034fb9ccdaea63173630b59cbe9dc33860a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:45 GMT  
		Size: 471.5 KB (471467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39aa89107a4c1ac15acc37ba98faa00f98774062e839984cd569c84acccbefa`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903c57abacc03a4132d1914d83b140d91cad6d3f72113588dbb0449668e5459e`  
		Last Modified: Wed, 13 Mar 2024 02:41:47 GMT  
		Size: 15.3 MB (15272331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c505d8db5c54f9f5b13a230f310c78e1daa9f0fa5baa7db6bb4b6f9b2824c64`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02c7783ff4e4ea0351aa496f9316d007b5d39dd7ac091772a53c788cc850835`  
		Last Modified: Wed, 13 Mar 2024 02:41:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2f6f475cd8b631685eb3441f13c0418b595dc3f64fc43f4de103cd270bd07a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c099338186092d8e8a9ee4e1aef2ac6bac6e0e37d05b00acc2519d4828eebc1a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66be30fd26f10adf7753fc7287726b290417f432503173cc8cfcc37c5970eed5`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdecded462eba57ac719ddeaf73027953397d9470c8d9ce91486b650688448d1`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b196924a8268e867bced4e92552ad7a24d5079dd5d3a5f2d32e98acf5b94ec`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83e0533daa0143428320795f95f747a318ce9dfaec9c1918dc09ddabff7ce6`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d6f7d580438b0f330c60e990071ee0a7fd2cb8e861b5b3673229aae5f40a97`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3043316cf0d3543d7ad8c2cf29b9f42217a7ff7ee358b9ccf49ec1c2742b40dc`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9d07b35dd72d9c89f56d604b5b5ff1096607de0b699a7845b4d4eef4542999`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7138f2320f3eb26befb56422d151646fa73d61b45b1fd7ba1a97e97b12b1794`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dd6eb25db87e92a30fe3a646b0ca820c3a8a855af39f49e9c1239e9e7e8fa8`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff49c00e60e2791dac19058d6bba6e562c80b90859f8e91ae70b474a582042`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c28453d92f8177a5ca4103ba031b5f02ceb70269930e8642e8bda358f1eef11`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 289.3 KB (289264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5958cc3ab872a13ea8011a1ae0a2290cefbfb5721bf58c5c16e2a1dfa216aa`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:alpine`

```console
$ docker pull caddy@sha256:dda81a416214d4dbdd978810efa19643e39b626fe0f979558fbb116758784c89
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
$ docker pull caddy@sha256:a6054d207060158cd0f019d6a35907bf47d1f8dacf58cdb63075a930d8ebca38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18467348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da4af4af9d73e970be3df873e00b8e658a7fc56ab982bfffa21d9bae68e3943`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:18:44 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 03:18:46 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 03:18:46 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 03:18:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 03:18:48 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 03:18:48 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 03:18:48 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 03:18:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 03:18:48 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 80
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 443
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 03:18:49 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 03:18:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a167b92bd92ca649523209f279d023d90edd2658f2dbbd5a79cd991b707a1bf4`  
		Last Modified: Sat, 16 Mar 2024 03:19:12 GMT  
		Size: 350.8 KB (350841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa65d2923419d52c79891c5c107216c8efc7534f740cafcddcb57fcd915fd61`  
		Last Modified: Sat, 16 Mar 2024 03:19:12 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832dc3f423aedf5c58d59571f7e5eebd543b4c31f0a0bacc36b509313473765e`  
		Last Modified: Sat, 16 Mar 2024 03:19:15 GMT  
		Size: 14.7 MB (14706436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:d5b956705aa5cb2d80a34b0da959c62f6e1b85d3b6af5d39bdd43a5ebad79732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17423235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637ed474101820123d027bf07c3bacd795eec60a114ec44aa0ab7c081f03fcdd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:36:00 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 06:36:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 06:36:01 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 06:36:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 06:36:04 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 06:36:04 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 06:36:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 06:36:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 06:36:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 80
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 443
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 06:36:05 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 06:36:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7e837cfa426b2a8d095055ea95ecda50deb35a29395410997280bf4efa14be`  
		Last Modified: Sat, 16 Mar 2024 06:36:25 GMT  
		Size: 347.6 KB (347629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aac6695e2937791ffb389edf1aee134b4e2e7c879173c70c5b0851017f402f5`  
		Last Modified: Sat, 16 Mar 2024 06:36:24 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a5dfabcee2609d8f2199b85fef83d4b0fa6612faa5a74b40f2809ccef87a5d`  
		Last Modified: Sat, 16 Mar 2024 06:36:27 GMT  
		Size: 13.9 MB (13921018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:d193bf8cf22c67a72ca3f4bc784363a0964ee0bc6481457a375beff0c515bb7b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17147117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c56baf0ceba318c0b5f456a51c90a5291492d8586689fa76bc097b01b50d670`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:36:34 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 08:36:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 08:36:35 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 08:36:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 08:36:38 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 08:36:38 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 08:36:38 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 08:36:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 08:36:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 80
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 443
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 08:36:39 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 08:36:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ad552b06977a907a460096cd3aa8d4cad657ae3a90be3bc63eba494b31a255`  
		Last Modified: Sat, 16 Mar 2024 08:36:59 GMT  
		Size: 344.5 KB (344462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7eb11427d968ddc8915316bd59544b644278fd1c3960927ab066c8cc916a8b`  
		Last Modified: Sat, 16 Mar 2024 08:36:58 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a13a58310f383c1986a52280e47b5d9a59f7ef7f02bf39ff3b494af779dab9`  
		Last Modified: Sat, 16 Mar 2024 08:37:02 GMT  
		Size: 13.9 MB (13893734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:aaf3497a43eee2656c636b04c5ac7dd7f81e15e6911be1c0509fcc51df3e6dbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f62720e336d430f97f77dea70bb3ceacea271cb1d7f6a246eb3c366e509827`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:55:39 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 02:55:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 02:55:41 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 02:55:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 02:55:43 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 02:55:43 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 02:55:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 80
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 443
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 02:55:44 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 02:55:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef488aa53de475202749fc28d385b1e4e59841fe4085a7edee2eb5026d11b95c`  
		Last Modified: Sat, 16 Mar 2024 02:56:01 GMT  
		Size: 360.7 KB (360666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322174feb81fda6e9c1e8e8ac7e49b8e77de2dca870243af972ee7545d4b7916`  
		Last Modified: Sat, 16 Mar 2024 02:56:01 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3360e007ed3153df2f6fbc7ef89943b1fc701d62c811d8855293b7df0f352d`  
		Last Modified: Sat, 16 Mar 2024 02:56:02 GMT  
		Size: 13.6 MB (13568947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:00e289b4657ffa0aec2c98f544cf7890e6cf6e4bd9dd1adfc01697d5fbb436a6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17052079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717f7ea5ec28ca8fed34729b1466cd1f5f96309057a0ec85b2e903833000f9ac`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:55:44 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 15 Mar 2024 23:55:46 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 15 Mar 2024 23:55:47 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 15 Mar 2024 23:55:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 15 Mar 2024 23:55:51 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 15 Mar 2024 23:55:51 GMT
ENV XDG_DATA_HOME=/data
# Fri, 15 Mar 2024 23:55:52 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 15 Mar 2024 23:55:52 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 15 Mar 2024 23:55:52 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 15 Mar 2024 23:55:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 15 Mar 2024 23:55:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 15 Mar 2024 23:55:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 15 Mar 2024 23:55:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 15 Mar 2024 23:55:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 15 Mar 2024 23:55:54 GMT
EXPOSE 80
# Fri, 15 Mar 2024 23:55:55 GMT
EXPOSE 443
# Fri, 15 Mar 2024 23:55:55 GMT
EXPOSE 443/udp
# Fri, 15 Mar 2024 23:55:55 GMT
EXPOSE 2019
# Fri, 15 Mar 2024 23:55:56 GMT
WORKDIR /srv
# Fri, 15 Mar 2024 23:55:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d58b091eab1c134ec71c79ecd145766a6b85840017d1e2223575349179f742c`  
		Last Modified: Fri, 15 Mar 2024 23:56:22 GMT  
		Size: 362.2 KB (362200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cfe42e2461424bcaa647db536a9454b1c48bf3410add89e0ec0367328cff78`  
		Last Modified: Fri, 15 Mar 2024 23:56:22 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103d176f7ec2158a797ee8c4909124a9a7cc2b8cff9b8c59e7368d8730563728`  
		Last Modified: Fri, 15 Mar 2024 23:56:24 GMT  
		Size: 13.3 MB (13333863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:aabd334d2f437365b8585670694b9cbe711132d5937a3d7f14b5840ff92fbf55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17818312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dd63d90fd552a57206bdfb4bb41bc51fd60b881c3ffe41f0852c6bac9ef68e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:48:00 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 04:48:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 04:48:01 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 04:48:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 04:48:04 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 04:48:04 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 04:48:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 04:48:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 04:48:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 04:48:05 GMT
EXPOSE 80
# Sat, 27 Jan 2024 04:48:05 GMT
EXPOSE 443
# Sat, 27 Jan 2024 04:48:05 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 04:48:06 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 04:48:06 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 04:48:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e608a3e3404a06a0444cc06a7949f9a4a2c56e2983aced16d2d32f009f2dbc17`  
		Last Modified: Sat, 27 Jan 2024 04:50:42 GMT  
		Size: 354.9 KB (354944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addd52ad78c14ade7e55ee491d32b0e51556e0c0a8b84d1fd1abc3a1430cc057`  
		Last Modified: Sat, 27 Jan 2024 04:50:42 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e597a1de66b259ef54ca1d052f65d662a6ea3ebf545513d9c91e80c67aa1f3`  
		Last Modified: Sat, 27 Jan 2024 04:50:44 GMT  
		Size: 14.2 MB (14238310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder`

```console
$ docker pull caddy@sha256:297a97b4f8f3f4467bcf9cfd5a6f5ba5bcfa38be56824c82e2c4f1c029701f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:a37704d2149bb703350b3e63704ecb468ec6f10cdc3784c818988e250484b2ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76973825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a6b943c698684ea914a9d08c8a00d2e573cbc2a95669142bc1b35350317cff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 03:18:55 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 03:18:55 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 03:18:55 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 03:18:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 03:18:55 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 03:18:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 03:18:57 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 03:18:57 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e791cb90c3d0bf08a988f13b405c9947c74b5bc31c7c939197a7175f6c7f0e`  
		Last Modified: Sat, 27 Jan 2024 01:36:33 GMT  
		Size: 284.7 KB (284690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3da9c61ef062502252a549dbc1f90925a8d7b6ef0644ffbfaea77be8b6f058`  
		Last Modified: Tue, 05 Mar 2024 19:25:57 GMT  
		Size: 67.0 MB (67010725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1741a7c0e9ce85801257b76332c08a3abdf5069bf46b0e764a32219d92189dc5`  
		Last Modified: Tue, 05 Mar 2024 19:25:45 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f302d3cc779898a1baa29b9dde46627021754a60a003a8ceb71b73f80af80bb2`  
		Last Modified: Sat, 16 Mar 2024 03:19:27 GMT  
		Size: 5.0 MB (4973021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51954c5f8bcd596606e74156291b16b5d0c2b430bb9f0a49db89dc03278cbd8e`  
		Last Modified: Sat, 16 Mar 2024 03:19:26 GMT  
		Size: 1.3 MB (1302235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351f34f77cd30086783b4d1e7bd91ac224af75f55690527012c4f114a65048b5`  
		Last Modified: Sat, 16 Mar 2024 03:19:26 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:042f6baf4a87f12037bf9a9146e994b03974edfdf6e94ef3a6c8ed9a5b0e01d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75407449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8104ab01bd342cfbbde6ad9a086efdba750ddaaeb6b4ce5acae4072b032808f1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 06:36:10 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 06:36:10 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 06:36:10 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 06:36:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 06:36:10 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 06:36:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 06:36:11 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 06:36:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18595ac3d5791e4d7e7dbcffcbf63e97e29974bd7191f7779889293f06709605`  
		Last Modified: Sat, 16 Mar 2024 01:27:12 GMT  
		Size: 284.9 KB (284879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67b0661c8b928f9ee07193e83a55962dc30ea03b3917d927fbfc6172db763d1`  
		Last Modified: Sat, 16 Mar 2024 01:28:25 GMT  
		Size: 65.8 MB (65767483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e94e3f035a7e84adb42051a6776fb957bb01e4afe261ef52850410749238c3e`  
		Last Modified: Sat, 16 Mar 2024 01:28:09 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90af61f594723149cbf4c52926248b7aa924edce2e71c1146dbfe1c4952d0e85`  
		Last Modified: Sat, 16 Mar 2024 06:36:39 GMT  
		Size: 5.0 MB (4958759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2b089f053b69b50a0ec1b57924c3f1dbab09af5f892a3f3824a1f1d91c4653`  
		Last Modified: Sat, 16 Mar 2024 06:36:39 GMT  
		Size: 1.2 MB (1248659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb3baf5a17563281d926d65bf039e75bafa0be92988b008e142f88f13e48831`  
		Last Modified: Sat, 16 Mar 2024 06:36:39 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:bba85446aa9cf082d96393b37ee2eb8948d32119f9f1b4a7de4264ed6265bc16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d75fc02eccf5b473914195c6b5a7f27a9c7b3af790feb14ca2afa4f0a1e6d2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 08:36:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 08:36:44 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 08:36:44 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 08:36:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 08:36:44 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 08:36:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 08:36:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 08:36:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03de95814623b83a4328b4db2e23b14214f57c18389a27379988469d9b6bbccc`  
		Last Modified: Sat, 16 Mar 2024 00:51:49 GMT  
		Size: 284.1 KB (284082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb316a6d2b1f8b686717aa026be6622630e91b4e2beff72260e41b9c26f5f328`  
		Last Modified: Sat, 16 Mar 2024 00:52:59 GMT  
		Size: 65.8 MB (65767446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3402119434a07f7977a54237330b21abbea9474c729d8bbbe43e79507612156`  
		Last Modified: Sat, 16 Mar 2024 00:52:46 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3e193cf2bcf63192347811ea80a7312b468b42f6341ff8912fb721dcdd07b1`  
		Last Modified: Sat, 16 Mar 2024 08:37:14 GMT  
		Size: 4.5 MB (4514679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302bab84b8a106df7129ce421df27645cf93461c26631a73c4c16dcc48213e33`  
		Last Modified: Sat, 16 Mar 2024 08:37:14 GMT  
		Size: 1.2 MB (1246087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa5da11b54d5792ea909f7bcbe533482069dd4540457779cb629671faadd4eb`  
		Last Modified: Sat, 16 Mar 2024 08:37:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:636495b6181fd6f900cfb1c3fafd4aa67ef8113e127a39c225dcd2b9f28018ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73993764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804083a23a5a42633ad7c22fc0b9908822db952792867afe4852db23de6882c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 02:55:47 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 02:55:48 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 02:55:48 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 02:55:48 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 02:55:48 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 02:55:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 02:55:49 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 02:55:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69c4102457739613c6fcb205a5a8e7dbc8383d57dade0a4502b1bca7b100a4d`  
		Last Modified: Sat, 16 Mar 2024 02:38:03 GMT  
		Size: 286.3 KB (286314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472e8443302a7aa2ee7c60f88cf1c1bff960c6982004fabf4d0b7dbb39552784`  
		Last Modified: Sat, 16 Mar 2024 02:38:55 GMT  
		Size: 64.1 MB (64111127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f3ae01babba08c7331e1311c66fc81f093559e9b48b75c7f09e492835df417`  
		Last Modified: Sat, 16 Mar 2024 02:38:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a47c8e46877caae3d8fa35784305f82b6173865f636c831581e413586174c9f`  
		Last Modified: Sat, 16 Mar 2024 02:56:14 GMT  
		Size: 5.1 MB (5063904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b458a517cc70120b5d5ad7b3624d14288f8fc2bb374503684e47dfb2d81ede41`  
		Last Modified: Sat, 16 Mar 2024 02:56:14 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e927a09144840e6a0520002506a03480353d2bf16acf387e392f67125a232f`  
		Last Modified: Sat, 16 Mar 2024 02:56:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:74036381f9b78d58ddddc74f279042dff06d05ac2b95c3faf063485eac603111
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74219852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afdeb2455afb0545182f73124c3e233abb4a6b803a834f42127d9a1eff4982c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 07:31:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 07:31:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 07:31:22 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 07:31:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 07:31:22 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 07:31:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 07:31:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 07:31:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e315e4c0ee7596e0eb7cc17d622c433e9fc4ef254b722e11e6794265328ea583`  
		Last Modified: Sat, 16 Mar 2024 00:32:12 GMT  
		Size: 286.7 KB (286670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee59a251903fa4e415f22830cd12da95ca1bcf671572b4a701a1d8f75a55d5ee`  
		Last Modified: Sat, 16 Mar 2024 00:33:15 GMT  
		Size: 64.1 MB (64126904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a227c25fca514ad52229d19315a3e0db7f235f9a840f9474237fadee44634bd1`  
		Last Modified: Sat, 16 Mar 2024 00:33:03 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da53f00025342b23cc1c1a712e9f3ff08b05bc0759f58b580a2081c4b925b9e8`  
		Last Modified: Sat, 16 Mar 2024 07:31:42 GMT  
		Size: 5.3 MB (5271003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1eb59d0f562ae579e22be9806e6ea172a7ee0399f354980329dfa3e8e04045`  
		Last Modified: Sat, 16 Mar 2024 07:31:41 GMT  
		Size: 1.2 MB (1186176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f27806532c2006d7f3b98c3ab37d72cf977ec4c488b65e389cb46e6b551627`  
		Last Modified: Sat, 16 Mar 2024 07:31:41 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:179342439e20a0f8308f5b3c8f51063386fb33fb38d9eda738dfd1d4b398280c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76101838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4eddf19e318b73f4fa90802285b549c08b6b015cfc8f36a11adbbf9c593fc2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Tue, 05 Mar 2024 20:58:12 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:58:12 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:58:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:58:13 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:58:13 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1b6899ff00172fd5c809d57028913a3c5aead2c05d0c3c01b15a5249c4ddec`  
		Last Modified: Sat, 27 Jan 2024 05:46:31 GMT  
		Size: 285.1 KB (285091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192deec459dbc25471d5ce96dbf84de90f9e77914e5074081b4aba0516977050`  
		Last Modified: Tue, 05 Mar 2024 20:12:42 GMT  
		Size: 66.2 MB (66218961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e6d46fb71afdd9825fc4397b4949daac74f5a564377560ed3cb3bb910da97f`  
		Last Modified: Tue, 05 Mar 2024 20:12:31 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad42b5ce4497969e7a2ebbdf9ada284081c50ce1744927873987c8075ed117fa`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 5.1 MB (5117256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea105a4685d829ffde13e2d0e06f02ec7f1e1381059eae15941a5aeb36d5f7a7`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 1.3 MB (1262390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1423e2dcf9499ee1179b946513f3194740bf64ee1f24d0a7688bde92f8773874`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:deed166abe77b412a506924346166c58e03f6e35fb2836e7af244be01925eddf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2054342050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7b95fb04081aaf80026e1bb52d4a79df79ea5aac969382123b16607318419f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 01:46:04 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Mar 2024 01:46:05 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Mar 2024 01:46:06 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Mar 2024 01:46:07 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Mar 2024 01:46:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 01:46:43 GMT
ENV GOPATH=C:\go
# Wed, 13 Mar 2024 01:47:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Mar 2024 02:01:45 GMT
ENV GOLANG_VERSION=1.21.8
# Wed, 13 Mar 2024 02:04:07 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 02:04:09 GMT
WORKDIR C:\go
# Wed, 13 Mar 2024 02:40:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:40:13 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 13 Mar 2024 02:40:14 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:40:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 13 Mar 2024 02:40:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 13 Mar 2024 02:40:40 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0a2d972d6c007b69f2c3ea41c1fe5fad6b189bfe40efacdcaf910b884fb6bb`  
		Last Modified: Wed, 13 Mar 2024 02:13:35 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f3068df504cd61566fc5e038c996322e35f58e08e0c6ef6ce589b11de4eb93`  
		Last Modified: Wed, 13 Mar 2024 02:13:34 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98750f7d798b8a0b5199088d4860bce5d51320b2fc07440f211ec692f4bf63b4`  
		Last Modified: Wed, 13 Mar 2024 02:13:33 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e43d1ea980f98746869d1942fc459ed402f307d4de5c435e325d2c9d534e99`  
		Last Modified: Wed, 13 Mar 2024 02:13:33 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fc4a2ae5d19f3b766991bfec5347bd5192c19ede11e7dfbf8b7d698fc1323d`  
		Last Modified: Wed, 13 Mar 2024 02:13:38 GMT  
		Size: 25.6 MB (25551948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251908e7b1f95da24e9f4ec7c727a2662105696c9de2925ab36938572cfb9f79`  
		Last Modified: Wed, 13 Mar 2024 02:13:31 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2927b1ac917c6e3261034f1c0cbb347c73f26593e997c505dfd04da18f966c1a`  
		Last Modified: Wed, 13 Mar 2024 02:13:31 GMT  
		Size: 273.7 KB (273727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5d297a0f5c09416c27b06ff859cb837506ffabdf0faa0cb5112e0a34839aab`  
		Last Modified: Wed, 13 Mar 2024 02:15:44 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1412d17e78321071b9d6a4dbb609e6a24c2e829a90ed9ca7e20a72ede74d04`  
		Last Modified: Wed, 13 Mar 2024 02:16:03 GMT  
		Size: 69.4 MB (69363257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619eb2756fc98681ecf9e1220a72f64f2e3f3fe9e72edd3a6021ad0249b9b2a5`  
		Last Modified: Wed, 13 Mar 2024 02:15:44 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf19d565f6ad05c073e69610b1e850eaf1a6aa6806195ea601c4a47303140d27`  
		Last Modified: Wed, 13 Mar 2024 02:42:22 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279cafbdd3019482f630ef1d502ea930d8ee1cfd8f9977bb52059c87ddff7a55`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e9d1117318fed479ece2fe1c6f9b896efcca03021ea368d722153aca1f8bc9`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d106feccb912e361adb23c8a586aad6b6c8493698e3893f4b1a2cd40bdd03cb4`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e766bc3c556143c937c2d95209a8d6370902ee4f31471f2a35c4d7045d361af6`  
		Last Modified: Wed, 13 Mar 2024 02:42:20 GMT  
		Size: 1.7 MB (1676188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39236cd34ad31ef892f22ac798c76cb384eb17ff72d5881539cbee398708be72`  
		Last Modified: Wed, 13 Mar 2024 02:42:20 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:53d965e8f604060a1c65cdf2a722300b8ff2f7a36494b6c0ba0c315fc7ffd2c2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221957582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0daee73c43fffad7bf7cfb8399d58db63aaa5f6727affb62b8d370b9760df81f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 01:49:48 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Mar 2024 01:49:49 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Mar 2024 01:49:50 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Mar 2024 01:49:51 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Mar 2024 01:51:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 01:51:29 GMT
ENV GOPATH=C:\go
# Wed, 13 Mar 2024 01:52:49 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Mar 2024 02:04:28 GMT
ENV GOLANG_VERSION=1.21.8
# Wed, 13 Mar 2024 02:07:38 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 02:07:39 GMT
WORKDIR C:\go
# Wed, 13 Mar 2024 02:38:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:38:30 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 13 Mar 2024 02:38:31 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:38:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 13 Mar 2024 02:39:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 13 Mar 2024 02:39:54 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc39f00be83bc8d2b0e0f2123fce0278f495e47f8a969bf03ec57df5f98cbda`  
		Last Modified: Wed, 13 Mar 2024 02:14:08 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f8b9e441646ef17118a0d394fa50244ef70c9e053c5b7d33e648796c8df90e`  
		Last Modified: Wed, 13 Mar 2024 02:14:07 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8759cd20778bf436a14e59cb31806b28212fcd510d8de32d44e49a9f39656f3d`  
		Last Modified: Wed, 13 Mar 2024 02:14:06 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d99a22ebabf5f80d07ad166a24eace1c2fa31cef2566a179bfec0d6407513e`  
		Last Modified: Wed, 13 Mar 2024 02:14:06 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfdb963b4125b258828e1fbac783c993a6845ad94973fad173f5dd25be3c34b`  
		Last Modified: Wed, 13 Mar 2024 02:14:12 GMT  
		Size: 25.5 MB (25540238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae89960ac90d33a751006d43faf1cbd1309b448658a447bb19dddabdbee17a9`  
		Last Modified: Wed, 13 Mar 2024 02:14:04 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff0bdcb61a7230b8b00d6e08d739c64fc0342dc675ed99fe6d35885cf1aa369`  
		Last Modified: Wed, 13 Mar 2024 02:14:05 GMT  
		Size: 272.6 KB (272572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c052d4b938689fbc1637386d1e61efa391787bd8128ee6d093464bad09b0231`  
		Last Modified: Wed, 13 Mar 2024 02:16:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e82772a8bffddc9f4a46c65cfa48f47938d84feb3730231762158c98014e47a`  
		Last Modified: Wed, 13 Mar 2024 02:16:31 GMT  
		Size: 69.4 MB (69350702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbffcc4012ecf27a404cc40eb63c43a880ad5104a82ee619fd0669acb2b5a710`  
		Last Modified: Wed, 13 Mar 2024 02:16:12 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fcd0eeed9adb7d9bf391df7f194150cb8ee56a63bc679cf147a14185381c3b`  
		Last Modified: Wed, 13 Mar 2024 02:42:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d74d351932d9ba6c92c9398e69d6736df75938a6ba3b7f1055206a1ed80b48`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db51f1e77d8641618afadb6f8c1ad073c4f72bb79099a00b0cabcbc8f5579248`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43620705f408ca0a7894137080f7947cc45d10badb0c7668ae1d46464494001b`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdaa0771d9c8b704195f821c3a9c23a5d9ff5e7e9b29335b835ce237f9d4dd50`  
		Last Modified: Wed, 13 Mar 2024 02:42:03 GMT  
		Size: 1.7 MB (1676257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010496734b493d0bc1b1a73566306e98777144ff64c5c886cf84de3af4fd971b`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:8308bb619e5ff5bc1842b8fc8480bb1584220a0c241f125727fa844918aac505
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
$ docker pull caddy@sha256:a37704d2149bb703350b3e63704ecb468ec6f10cdc3784c818988e250484b2ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76973825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a6b943c698684ea914a9d08c8a00d2e573cbc2a95669142bc1b35350317cff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 03:18:55 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 03:18:55 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 03:18:55 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 03:18:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 03:18:55 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 03:18:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 03:18:57 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 03:18:57 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e791cb90c3d0bf08a988f13b405c9947c74b5bc31c7c939197a7175f6c7f0e`  
		Last Modified: Sat, 27 Jan 2024 01:36:33 GMT  
		Size: 284.7 KB (284690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3da9c61ef062502252a549dbc1f90925a8d7b6ef0644ffbfaea77be8b6f058`  
		Last Modified: Tue, 05 Mar 2024 19:25:57 GMT  
		Size: 67.0 MB (67010725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1741a7c0e9ce85801257b76332c08a3abdf5069bf46b0e764a32219d92189dc5`  
		Last Modified: Tue, 05 Mar 2024 19:25:45 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f302d3cc779898a1baa29b9dde46627021754a60a003a8ceb71b73f80af80bb2`  
		Last Modified: Sat, 16 Mar 2024 03:19:27 GMT  
		Size: 5.0 MB (4973021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51954c5f8bcd596606e74156291b16b5d0c2b430bb9f0a49db89dc03278cbd8e`  
		Last Modified: Sat, 16 Mar 2024 03:19:26 GMT  
		Size: 1.3 MB (1302235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351f34f77cd30086783b4d1e7bd91ac224af75f55690527012c4f114a65048b5`  
		Last Modified: Sat, 16 Mar 2024 03:19:26 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:042f6baf4a87f12037bf9a9146e994b03974edfdf6e94ef3a6c8ed9a5b0e01d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75407449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8104ab01bd342cfbbde6ad9a086efdba750ddaaeb6b4ce5acae4072b032808f1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 06:36:10 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 06:36:10 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 06:36:10 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 06:36:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 06:36:10 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 06:36:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 06:36:11 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 06:36:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18595ac3d5791e4d7e7dbcffcbf63e97e29974bd7191f7779889293f06709605`  
		Last Modified: Sat, 16 Mar 2024 01:27:12 GMT  
		Size: 284.9 KB (284879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67b0661c8b928f9ee07193e83a55962dc30ea03b3917d927fbfc6172db763d1`  
		Last Modified: Sat, 16 Mar 2024 01:28:25 GMT  
		Size: 65.8 MB (65767483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e94e3f035a7e84adb42051a6776fb957bb01e4afe261ef52850410749238c3e`  
		Last Modified: Sat, 16 Mar 2024 01:28:09 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90af61f594723149cbf4c52926248b7aa924edce2e71c1146dbfe1c4952d0e85`  
		Last Modified: Sat, 16 Mar 2024 06:36:39 GMT  
		Size: 5.0 MB (4958759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2b089f053b69b50a0ec1b57924c3f1dbab09af5f892a3f3824a1f1d91c4653`  
		Last Modified: Sat, 16 Mar 2024 06:36:39 GMT  
		Size: 1.2 MB (1248659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb3baf5a17563281d926d65bf039e75bafa0be92988b008e142f88f13e48831`  
		Last Modified: Sat, 16 Mar 2024 06:36:39 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:bba85446aa9cf082d96393b37ee2eb8948d32119f9f1b4a7de4264ed6265bc16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d75fc02eccf5b473914195c6b5a7f27a9c7b3af790feb14ca2afa4f0a1e6d2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 08:36:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 08:36:44 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 08:36:44 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 08:36:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 08:36:44 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 08:36:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 08:36:46 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 08:36:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03de95814623b83a4328b4db2e23b14214f57c18389a27379988469d9b6bbccc`  
		Last Modified: Sat, 16 Mar 2024 00:51:49 GMT  
		Size: 284.1 KB (284082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb316a6d2b1f8b686717aa026be6622630e91b4e2beff72260e41b9c26f5f328`  
		Last Modified: Sat, 16 Mar 2024 00:52:59 GMT  
		Size: 65.8 MB (65767446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3402119434a07f7977a54237330b21abbea9474c729d8bbbe43e79507612156`  
		Last Modified: Sat, 16 Mar 2024 00:52:46 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3e193cf2bcf63192347811ea80a7312b468b42f6341ff8912fb721dcdd07b1`  
		Last Modified: Sat, 16 Mar 2024 08:37:14 GMT  
		Size: 4.5 MB (4514679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302bab84b8a106df7129ce421df27645cf93461c26631a73c4c16dcc48213e33`  
		Last Modified: Sat, 16 Mar 2024 08:37:14 GMT  
		Size: 1.2 MB (1246087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa5da11b54d5792ea909f7bcbe533482069dd4540457779cb629671faadd4eb`  
		Last Modified: Sat, 16 Mar 2024 08:37:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:636495b6181fd6f900cfb1c3fafd4aa67ef8113e127a39c225dcd2b9f28018ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73993764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804083a23a5a42633ad7c22fc0b9908822db952792867afe4852db23de6882c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 02:55:47 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 02:55:48 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 02:55:48 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 02:55:48 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 02:55:48 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 02:55:49 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 02:55:49 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 02:55:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69c4102457739613c6fcb205a5a8e7dbc8383d57dade0a4502b1bca7b100a4d`  
		Last Modified: Sat, 16 Mar 2024 02:38:03 GMT  
		Size: 286.3 KB (286314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472e8443302a7aa2ee7c60f88cf1c1bff960c6982004fabf4d0b7dbb39552784`  
		Last Modified: Sat, 16 Mar 2024 02:38:55 GMT  
		Size: 64.1 MB (64111127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f3ae01babba08c7331e1311c66fc81f093559e9b48b75c7f09e492835df417`  
		Last Modified: Sat, 16 Mar 2024 02:38:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a47c8e46877caae3d8fa35784305f82b6173865f636c831581e413586174c9f`  
		Last Modified: Sat, 16 Mar 2024 02:56:14 GMT  
		Size: 5.1 MB (5063904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b458a517cc70120b5d5ad7b3624d14288f8fc2bb374503684e47dfb2d81ede41`  
		Last Modified: Sat, 16 Mar 2024 02:56:14 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e927a09144840e6a0520002506a03480353d2bf16acf387e392f67125a232f`  
		Last Modified: Sat, 16 Mar 2024 02:56:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:74036381f9b78d58ddddc74f279042dff06d05ac2b95c3faf063485eac603111
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74219852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afdeb2455afb0545182f73124c3e233abb4a6b803a834f42127d9a1eff4982c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Sat, 16 Mar 2024 07:31:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 16 Mar 2024 07:31:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 16 Mar 2024 07:31:22 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 07:31:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 16 Mar 2024 07:31:22 GMT
ENV XCADDY_SETCAP=1
# Sat, 16 Mar 2024 07:31:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 16 Mar 2024 07:31:26 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 16 Mar 2024 07:31:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e315e4c0ee7596e0eb7cc17d622c433e9fc4ef254b722e11e6794265328ea583`  
		Last Modified: Sat, 16 Mar 2024 00:32:12 GMT  
		Size: 286.7 KB (286670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee59a251903fa4e415f22830cd12da95ca1bcf671572b4a701a1d8f75a55d5ee`  
		Last Modified: Sat, 16 Mar 2024 00:33:15 GMT  
		Size: 64.1 MB (64126904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a227c25fca514ad52229d19315a3e0db7f235f9a840f9474237fadee44634bd1`  
		Last Modified: Sat, 16 Mar 2024 00:33:03 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da53f00025342b23cc1c1a712e9f3ff08b05bc0759f58b580a2081c4b925b9e8`  
		Last Modified: Sat, 16 Mar 2024 07:31:42 GMT  
		Size: 5.3 MB (5271003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1eb59d0f562ae579e22be9806e6ea172a7ee0399f354980329dfa3e8e04045`  
		Last Modified: Sat, 16 Mar 2024 07:31:41 GMT  
		Size: 1.2 MB (1186176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f27806532c2006d7f3b98c3ab37d72cf977ec4c488b65e389cb46e6b551627`  
		Last Modified: Sat, 16 Mar 2024 07:31:41 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:179342439e20a0f8308f5b3c8f51063386fb33fb38d9eda738dfd1d4b398280c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76101838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4eddf19e318b73f4fa90802285b549c08b6b015cfc8f36a11adbbf9c593fc2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 18:06:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 Mar 2024 18:06:00 GMT
ENV GOPATH=/go
# Tue, 05 Mar 2024 18:06:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 18:06:00 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 Mar 2024 18:06:00 GMT
WORKDIR /go
# Tue, 05 Mar 2024 20:58:12 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:58:12 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:58:12 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:58:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:58:13 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:58:13 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1b6899ff00172fd5c809d57028913a3c5aead2c05d0c3c01b15a5249c4ddec`  
		Last Modified: Sat, 27 Jan 2024 05:46:31 GMT  
		Size: 285.1 KB (285091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192deec459dbc25471d5ce96dbf84de90f9e77914e5074081b4aba0516977050`  
		Last Modified: Tue, 05 Mar 2024 20:12:42 GMT  
		Size: 66.2 MB (66218961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e6d46fb71afdd9825fc4397b4949daac74f5a564377560ed3cb3bb910da97f`  
		Last Modified: Tue, 05 Mar 2024 20:12:31 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad42b5ce4497969e7a2ebbdf9ada284081c50ce1744927873987c8075ed117fa`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 5.1 MB (5117256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea105a4685d829ffde13e2d0e06f02ec7f1e1381059eae15941a5aeb36d5f7a7`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 1.3 MB (1262390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1423e2dcf9499ee1179b946513f3194740bf64ee1f24d0a7688bde92f8773874`  
		Last Modified: Tue, 05 Mar 2024 20:59:28 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:88480ae6cc843e1f4d7891d869f95182848a5414c6545cc2662d466a7c8dfdd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:53d965e8f604060a1c65cdf2a722300b8ff2f7a36494b6c0ba0c315fc7ffd2c2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221957582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0daee73c43fffad7bf7cfb8399d58db63aaa5f6727affb62b8d370b9760df81f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 01:49:48 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Mar 2024 01:49:49 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Mar 2024 01:49:50 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Mar 2024 01:49:51 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Mar 2024 01:51:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 01:51:29 GMT
ENV GOPATH=C:\go
# Wed, 13 Mar 2024 01:52:49 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Mar 2024 02:04:28 GMT
ENV GOLANG_VERSION=1.21.8
# Wed, 13 Mar 2024 02:07:38 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 02:07:39 GMT
WORKDIR C:\go
# Wed, 13 Mar 2024 02:38:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:38:30 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 13 Mar 2024 02:38:31 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:38:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 13 Mar 2024 02:39:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 13 Mar 2024 02:39:54 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc39f00be83bc8d2b0e0f2123fce0278f495e47f8a969bf03ec57df5f98cbda`  
		Last Modified: Wed, 13 Mar 2024 02:14:08 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f8b9e441646ef17118a0d394fa50244ef70c9e053c5b7d33e648796c8df90e`  
		Last Modified: Wed, 13 Mar 2024 02:14:07 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8759cd20778bf436a14e59cb31806b28212fcd510d8de32d44e49a9f39656f3d`  
		Last Modified: Wed, 13 Mar 2024 02:14:06 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d99a22ebabf5f80d07ad166a24eace1c2fa31cef2566a179bfec0d6407513e`  
		Last Modified: Wed, 13 Mar 2024 02:14:06 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfdb963b4125b258828e1fbac783c993a6845ad94973fad173f5dd25be3c34b`  
		Last Modified: Wed, 13 Mar 2024 02:14:12 GMT  
		Size: 25.5 MB (25540238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae89960ac90d33a751006d43faf1cbd1309b448658a447bb19dddabdbee17a9`  
		Last Modified: Wed, 13 Mar 2024 02:14:04 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff0bdcb61a7230b8b00d6e08d739c64fc0342dc675ed99fe6d35885cf1aa369`  
		Last Modified: Wed, 13 Mar 2024 02:14:05 GMT  
		Size: 272.6 KB (272572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c052d4b938689fbc1637386d1e61efa391787bd8128ee6d093464bad09b0231`  
		Last Modified: Wed, 13 Mar 2024 02:16:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e82772a8bffddc9f4a46c65cfa48f47938d84feb3730231762158c98014e47a`  
		Last Modified: Wed, 13 Mar 2024 02:16:31 GMT  
		Size: 69.4 MB (69350702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbffcc4012ecf27a404cc40eb63c43a880ad5104a82ee619fd0669acb2b5a710`  
		Last Modified: Wed, 13 Mar 2024 02:16:12 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fcd0eeed9adb7d9bf391df7f194150cb8ee56a63bc679cf147a14185381c3b`  
		Last Modified: Wed, 13 Mar 2024 02:42:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d74d351932d9ba6c92c9398e69d6736df75938a6ba3b7f1055206a1ed80b48`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db51f1e77d8641618afadb6f8c1ad073c4f72bb79099a00b0cabcbc8f5579248`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43620705f408ca0a7894137080f7947cc45d10badb0c7668ae1d46464494001b`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdaa0771d9c8b704195f821c3a9c23a5d9ff5e7e9b29335b835ce237f9d4dd50`  
		Last Modified: Wed, 13 Mar 2024 02:42:03 GMT  
		Size: 1.7 MB (1676257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010496734b493d0bc1b1a73566306e98777144ff64c5c886cf84de3af4fd971b`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:7904ec0c624b28630437b42e793d0e1bc2472c348c79b15b26d065162eafd9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:deed166abe77b412a506924346166c58e03f6e35fb2836e7af244be01925eddf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2054342050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7b95fb04081aaf80026e1bb52d4a79df79ea5aac969382123b16607318419f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 01:46:04 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Mar 2024 01:46:05 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Mar 2024 01:46:06 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Mar 2024 01:46:07 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Mar 2024 01:46:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 01:46:43 GMT
ENV GOPATH=C:\go
# Wed, 13 Mar 2024 01:47:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Mar 2024 02:01:45 GMT
ENV GOLANG_VERSION=1.21.8
# Wed, 13 Mar 2024 02:04:07 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 02:04:09 GMT
WORKDIR C:\go
# Wed, 13 Mar 2024 02:40:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:40:13 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 13 Mar 2024 02:40:14 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:40:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 13 Mar 2024 02:40:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 13 Mar 2024 02:40:40 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0a2d972d6c007b69f2c3ea41c1fe5fad6b189bfe40efacdcaf910b884fb6bb`  
		Last Modified: Wed, 13 Mar 2024 02:13:35 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f3068df504cd61566fc5e038c996322e35f58e08e0c6ef6ce589b11de4eb93`  
		Last Modified: Wed, 13 Mar 2024 02:13:34 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98750f7d798b8a0b5199088d4860bce5d51320b2fc07440f211ec692f4bf63b4`  
		Last Modified: Wed, 13 Mar 2024 02:13:33 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e43d1ea980f98746869d1942fc459ed402f307d4de5c435e325d2c9d534e99`  
		Last Modified: Wed, 13 Mar 2024 02:13:33 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fc4a2ae5d19f3b766991bfec5347bd5192c19ede11e7dfbf8b7d698fc1323d`  
		Last Modified: Wed, 13 Mar 2024 02:13:38 GMT  
		Size: 25.6 MB (25551948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251908e7b1f95da24e9f4ec7c727a2662105696c9de2925ab36938572cfb9f79`  
		Last Modified: Wed, 13 Mar 2024 02:13:31 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2927b1ac917c6e3261034f1c0cbb347c73f26593e997c505dfd04da18f966c1a`  
		Last Modified: Wed, 13 Mar 2024 02:13:31 GMT  
		Size: 273.7 KB (273727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5d297a0f5c09416c27b06ff859cb837506ffabdf0faa0cb5112e0a34839aab`  
		Last Modified: Wed, 13 Mar 2024 02:15:44 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1412d17e78321071b9d6a4dbb609e6a24c2e829a90ed9ca7e20a72ede74d04`  
		Last Modified: Wed, 13 Mar 2024 02:16:03 GMT  
		Size: 69.4 MB (69363257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619eb2756fc98681ecf9e1220a72f64f2e3f3fe9e72edd3a6021ad0249b9b2a5`  
		Last Modified: Wed, 13 Mar 2024 02:15:44 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf19d565f6ad05c073e69610b1e850eaf1a6aa6806195ea601c4a47303140d27`  
		Last Modified: Wed, 13 Mar 2024 02:42:22 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279cafbdd3019482f630ef1d502ea930d8ee1cfd8f9977bb52059c87ddff7a55`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e9d1117318fed479ece2fe1c6f9b896efcca03021ea368d722153aca1f8bc9`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d106feccb912e361adb23c8a586aad6b6c8493698e3893f4b1a2cd40bdd03cb4`  
		Last Modified: Wed, 13 Mar 2024 02:42:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e766bc3c556143c937c2d95209a8d6370902ee4f31471f2a35c4d7045d361af6`  
		Last Modified: Wed, 13 Mar 2024 02:42:20 GMT  
		Size: 1.7 MB (1676188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39236cd34ad31ef892f22ac798c76cb384eb17ff72d5881539cbee398708be72`  
		Last Modified: Wed, 13 Mar 2024 02:42:20 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:ce43091c481420028215c752115f25e501155b055ae9f4862bae373bda4c1308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:a6054d207060158cd0f019d6a35907bf47d1f8dacf58cdb63075a930d8ebca38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18467348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da4af4af9d73e970be3df873e00b8e658a7fc56ab982bfffa21d9bae68e3943`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:18:44 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 03:18:46 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 03:18:46 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 03:18:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 03:18:48 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 03:18:48 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 03:18:48 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 03:18:48 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 03:18:48 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 03:18:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 80
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 443
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 03:18:49 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 03:18:49 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 03:18:50 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a167b92bd92ca649523209f279d023d90edd2658f2dbbd5a79cd991b707a1bf4`  
		Last Modified: Sat, 16 Mar 2024 03:19:12 GMT  
		Size: 350.8 KB (350841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa65d2923419d52c79891c5c107216c8efc7534f740cafcddcb57fcd915fd61`  
		Last Modified: Sat, 16 Mar 2024 03:19:12 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832dc3f423aedf5c58d59571f7e5eebd543b4c31f0a0bacc36b509313473765e`  
		Last Modified: Sat, 16 Mar 2024 03:19:15 GMT  
		Size: 14.7 MB (14706436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:d5b956705aa5cb2d80a34b0da959c62f6e1b85d3b6af5d39bdd43a5ebad79732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17423235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637ed474101820123d027bf07c3bacd795eec60a114ec44aa0ab7c081f03fcdd`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:36:00 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 06:36:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 06:36:01 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 06:36:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 06:36:04 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 06:36:04 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 06:36:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 06:36:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 06:36:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 06:36:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 80
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 443
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 06:36:05 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 06:36:05 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 06:36:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7e837cfa426b2a8d095055ea95ecda50deb35a29395410997280bf4efa14be`  
		Last Modified: Sat, 16 Mar 2024 06:36:25 GMT  
		Size: 347.6 KB (347629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aac6695e2937791ffb389edf1aee134b4e2e7c879173c70c5b0851017f402f5`  
		Last Modified: Sat, 16 Mar 2024 06:36:24 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a5dfabcee2609d8f2199b85fef83d4b0fa6612faa5a74b40f2809ccef87a5d`  
		Last Modified: Sat, 16 Mar 2024 06:36:27 GMT  
		Size: 13.9 MB (13921018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:d193bf8cf22c67a72ca3f4bc784363a0964ee0bc6481457a375beff0c515bb7b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17147117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c56baf0ceba318c0b5f456a51c90a5291492d8586689fa76bc097b01b50d670`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:36:34 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 08:36:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 08:36:35 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 08:36:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 08:36:38 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 08:36:38 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 08:36:38 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 08:36:38 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 08:36:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 08:36:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 80
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 443
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 08:36:39 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 08:36:39 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 08:36:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ad552b06977a907a460096cd3aa8d4cad657ae3a90be3bc63eba494b31a255`  
		Last Modified: Sat, 16 Mar 2024 08:36:59 GMT  
		Size: 344.5 KB (344462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7eb11427d968ddc8915316bd59544b644278fd1c3960927ab066c8cc916a8b`  
		Last Modified: Sat, 16 Mar 2024 08:36:58 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a13a58310f383c1986a52280e47b5d9a59f7ef7f02bf39ff3b494af779dab9`  
		Last Modified: Sat, 16 Mar 2024 08:37:02 GMT  
		Size: 13.9 MB (13893734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:aaf3497a43eee2656c636b04c5ac7dd7f81e15e6911be1c0509fcc51df3e6dbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f62720e336d430f97f77dea70bb3ceacea271cb1d7f6a246eb3c366e509827`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:55:39 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 02:55:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 02:55:41 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 02:55:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 02:55:43 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 02:55:43 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 02:55:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 02:55:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 80
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 443
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 02:55:44 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 02:55:44 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 02:55:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef488aa53de475202749fc28d385b1e4e59841fe4085a7edee2eb5026d11b95c`  
		Last Modified: Sat, 16 Mar 2024 02:56:01 GMT  
		Size: 360.7 KB (360666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322174feb81fda6e9c1e8e8ac7e49b8e77de2dca870243af972ee7545d4b7916`  
		Last Modified: Sat, 16 Mar 2024 02:56:01 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3360e007ed3153df2f6fbc7ef89943b1fc701d62c811d8855293b7df0f352d`  
		Last Modified: Sat, 16 Mar 2024 02:56:02 GMT  
		Size: 13.6 MB (13568947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:00e289b4657ffa0aec2c98f544cf7890e6cf6e4bd9dd1adfc01697d5fbb436a6
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17052079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717f7ea5ec28ca8fed34729b1466cd1f5f96309057a0ec85b2e903833000f9ac`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:55:44 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Fri, 15 Mar 2024 23:55:46 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Fri, 15 Mar 2024 23:55:47 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 15 Mar 2024 23:55:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Fri, 15 Mar 2024 23:55:51 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 15 Mar 2024 23:55:51 GMT
ENV XDG_DATA_HOME=/data
# Fri, 15 Mar 2024 23:55:52 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 15 Mar 2024 23:55:52 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 15 Mar 2024 23:55:52 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 15 Mar 2024 23:55:53 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 15 Mar 2024 23:55:53 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 15 Mar 2024 23:55:53 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 15 Mar 2024 23:55:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 15 Mar 2024 23:55:54 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 15 Mar 2024 23:55:54 GMT
EXPOSE 80
# Fri, 15 Mar 2024 23:55:55 GMT
EXPOSE 443
# Fri, 15 Mar 2024 23:55:55 GMT
EXPOSE 443/udp
# Fri, 15 Mar 2024 23:55:55 GMT
EXPOSE 2019
# Fri, 15 Mar 2024 23:55:56 GMT
WORKDIR /srv
# Fri, 15 Mar 2024 23:55:56 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d58b091eab1c134ec71c79ecd145766a6b85840017d1e2223575349179f742c`  
		Last Modified: Fri, 15 Mar 2024 23:56:22 GMT  
		Size: 362.2 KB (362200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cfe42e2461424bcaa647db536a9454b1c48bf3410add89e0ec0367328cff78`  
		Last Modified: Fri, 15 Mar 2024 23:56:22 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103d176f7ec2158a797ee8c4909124a9a7cc2b8cff9b8c59e7368d8730563728`  
		Last Modified: Fri, 15 Mar 2024 23:56:24 GMT  
		Size: 13.3 MB (13333863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:aabd334d2f437365b8585670694b9cbe711132d5937a3d7f14b5840ff92fbf55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17818312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dd63d90fd552a57206bdfb4bb41bc51fd60b881c3ffe41f0852c6bac9ef68e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:48:00 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 04:48:01 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 04:48:01 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 04:48:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 04:48:04 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 04:48:04 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 04:48:04 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 04:48:04 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 04:48:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 04:48:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 04:48:05 GMT
EXPOSE 80
# Sat, 27 Jan 2024 04:48:05 GMT
EXPOSE 443
# Sat, 27 Jan 2024 04:48:05 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 04:48:06 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 04:48:06 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 04:48:06 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e608a3e3404a06a0444cc06a7949f9a4a2c56e2983aced16d2d32f009f2dbc17`  
		Last Modified: Sat, 27 Jan 2024 04:50:42 GMT  
		Size: 354.9 KB (354944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addd52ad78c14ade7e55ee491d32b0e51556e0c0a8b84d1fd1abc3a1430cc057`  
		Last Modified: Sat, 27 Jan 2024 04:50:42 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e597a1de66b259ef54ca1d052f65d662a6ea3ebf545513d9c91e80c67aa1f3`  
		Last Modified: Sat, 27 Jan 2024 04:50:44 GMT  
		Size: 14.2 MB (14238310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:e92a98f9befbcc685cba6014745c4c4e5573d524f98646666afae41fe635a647
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1973514153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c02263e4345786d822a7cbe2109be66b8bbc405dad0088432e203c583cdb8c4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:37:25 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:37:26 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:37:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:37:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:37:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:37:54 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:37:55 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:37:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:37:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:37:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:38:00 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:38:01 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:38:03 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:38:21 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:38:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3433f0cddf0bf50f831ae26d44034fb9ccdaea63173630b59cbe9dc33860a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:45 GMT  
		Size: 471.5 KB (471467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39aa89107a4c1ac15acc37ba98faa00f98774062e839984cd569c84acccbefa`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903c57abacc03a4132d1914d83b140d91cad6d3f72113588dbb0449668e5459e`  
		Last Modified: Wed, 13 Mar 2024 02:41:47 GMT  
		Size: 15.3 MB (15272331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c505d8db5c54f9f5b13a230f310c78e1daa9f0fa5baa7db6bb4b6f9b2824c64`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02c7783ff4e4ea0351aa496f9316d007b5d39dd7ac091772a53c788cc850835`  
		Last Modified: Wed, 13 Mar 2024 02:41:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2f6f475cd8b631685eb3441f13c0418b595dc3f64fc43f4de103cd270bd07a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c099338186092d8e8a9ee4e1aef2ac6bac6e0e37d05b00acc2519d4828eebc1a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66be30fd26f10adf7753fc7287726b290417f432503173cc8cfcc37c5970eed5`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdecded462eba57ac719ddeaf73027953397d9470c8d9ce91486b650688448d1`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b196924a8268e867bced4e92552ad7a24d5079dd5d3a5f2d32e98acf5b94ec`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83e0533daa0143428320795f95f747a318ce9dfaec9c1918dc09ddabff7ce6`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d6f7d580438b0f330c60e990071ee0a7fd2cb8e861b5b3673229aae5f40a97`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3043316cf0d3543d7ad8c2cf29b9f42217a7ff7ee358b9ccf49ec1c2742b40dc`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9d07b35dd72d9c89f56d604b5b5ff1096607de0b699a7845b4d4eef4542999`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7138f2320f3eb26befb56422d151646fa73d61b45b1fd7ba1a97e97b12b1794`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dd6eb25db87e92a30fe3a646b0ca820c3a8a855af39f49e9c1239e9e7e8fa8`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff49c00e60e2791dac19058d6bba6e562c80b90859f8e91ae70b474a582042`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c28453d92f8177a5ca4103ba031b5f02ceb70269930e8642e8bda358f1eef11`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 289.3 KB (289264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5958cc3ab872a13ea8011a1ae0a2290cefbfb5721bf58c5c16e2a1dfa216aa`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:2a10673838e2beefb539398925457319c1e7800b242f5c261bc40ddd7f16aa33
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2141123401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001b000d65334996d09969a3e79ce6304b5ea6811c67eb7add59f0c78b73ba5c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:34:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:34:08 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:35:29 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:35:30 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:35:31 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:35:31 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:35:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:35:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:35:35 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:35:36 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:35:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:35:39 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:35:40 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:36:47 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:36:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bb323765ff7b405cedec6f88daa8a1c8470f45c358d637c0062cf4c63d7e07`  
		Last Modified: Wed, 13 Mar 2024 02:41:21 GMT  
		Size: 465.6 KB (465620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b3f11ec4ee425a6a0b9f5ad200c9193592181f59520c9a80372e647787163a`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ffe491a522455b1d95c1d0d3384188ea361064259fffcadd657bebae4fa934`  
		Last Modified: Wed, 13 Mar 2024 02:41:24 GMT  
		Size: 15.3 MB (15277213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b62af40926c0d1a37e6126f41f63533166809b5b54434cf3b53ab5734357e59`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a9b1639ec2e8588ca4fd94f87b31b4e30adef3c0ac45ea4ac0e4cdce643d6`  
		Last Modified: Wed, 13 Mar 2024 02:41:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7a48958fcb11d52bb7a65f60d6f322d3326d4f2916e0547b764cbe4fe0eae8`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9eb36d28260e8ba5549b16a87d121a4d7b0d38f46e1127ee1fd95f2e31e6f2c`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d221a46e4e966da289289be19ac425d0199540bef1d6d7c890ba45ec255e79`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feeda3213337ce81d383bcb08c0b241e763185b91a2e180f35c59395e3c0290f`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d7bf5ae3a283a09c7a385afa5160b2d0f1d275fc23e0a1711bf734511fe0b1`  
		Last Modified: Wed, 13 Mar 2024 02:41:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f309d19b55289fe422d64dd24736be59a52f6eba872d8fb1054416f8b5d9c553`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4ac1a4021eeee54512dde50b437001408fd1dda9d896f68d38728f7dba8c6c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e117655b528b6e8f7ce8d4d2cb69d41a1735fec0e31e10dc40cddcf0d012be`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5524c6d618843e710fa22d77e57a844c7cdfd68676c809d2d1ecde656c16a81c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879784be55be2c5d212302ae42232de9bfeaccea0b1398ec0101ef36d542930c`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f8aadcc42505eea344cf0504c7312d01033f159e88d6eadab5abb9eefc98a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41580c6cc25a82ee1a4de9315ec98ce6e89bd73461a941248648d04292e9ff52`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1261dc2b6b686493c5c3989f8efdd404b912398f6a38933aba80fe65d5d6240c`  
		Last Modified: Wed, 13 Mar 2024 02:41:15 GMT  
		Size: 258.2 KB (258159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8856855cc09ca543e8712766ea12d12556af369305babcaf786f620c89c3450d`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:02e4ec422a43bbe257c0b6f52bc54f9e391ac2ed078f86fc4d80269ca8ef3533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `caddy:windowsservercore` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:e92a98f9befbcc685cba6014745c4c4e5573d524f98646666afae41fe635a647
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1973514153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c02263e4345786d822a7cbe2109be66b8bbc405dad0088432e203c583cdb8c4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:37:25 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:37:26 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:37:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:37:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:37:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:37:54 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:37:55 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:37:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:37:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:37:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:38:00 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:38:01 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:38:03 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:38:21 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:38:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3433f0cddf0bf50f831ae26d44034fb9ccdaea63173630b59cbe9dc33860a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:45 GMT  
		Size: 471.5 KB (471467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39aa89107a4c1ac15acc37ba98faa00f98774062e839984cd569c84acccbefa`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903c57abacc03a4132d1914d83b140d91cad6d3f72113588dbb0449668e5459e`  
		Last Modified: Wed, 13 Mar 2024 02:41:47 GMT  
		Size: 15.3 MB (15272331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c505d8db5c54f9f5b13a230f310c78e1daa9f0fa5baa7db6bb4b6f9b2824c64`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02c7783ff4e4ea0351aa496f9316d007b5d39dd7ac091772a53c788cc850835`  
		Last Modified: Wed, 13 Mar 2024 02:41:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2f6f475cd8b631685eb3441f13c0418b595dc3f64fc43f4de103cd270bd07a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c099338186092d8e8a9ee4e1aef2ac6bac6e0e37d05b00acc2519d4828eebc1a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66be30fd26f10adf7753fc7287726b290417f432503173cc8cfcc37c5970eed5`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdecded462eba57ac719ddeaf73027953397d9470c8d9ce91486b650688448d1`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b196924a8268e867bced4e92552ad7a24d5079dd5d3a5f2d32e98acf5b94ec`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83e0533daa0143428320795f95f747a318ce9dfaec9c1918dc09ddabff7ce6`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d6f7d580438b0f330c60e990071ee0a7fd2cb8e861b5b3673229aae5f40a97`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3043316cf0d3543d7ad8c2cf29b9f42217a7ff7ee358b9ccf49ec1c2742b40dc`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9d07b35dd72d9c89f56d604b5b5ff1096607de0b699a7845b4d4eef4542999`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7138f2320f3eb26befb56422d151646fa73d61b45b1fd7ba1a97e97b12b1794`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dd6eb25db87e92a30fe3a646b0ca820c3a8a855af39f49e9c1239e9e7e8fa8`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff49c00e60e2791dac19058d6bba6e562c80b90859f8e91ae70b474a582042`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c28453d92f8177a5ca4103ba031b5f02ceb70269930e8642e8bda358f1eef11`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 289.3 KB (289264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5958cc3ab872a13ea8011a1ae0a2290cefbfb5721bf58c5c16e2a1dfa216aa`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:2a10673838e2beefb539398925457319c1e7800b242f5c261bc40ddd7f16aa33
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2141123401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001b000d65334996d09969a3e79ce6304b5ea6811c67eb7add59f0c78b73ba5c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:34:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:34:08 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:35:29 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:35:30 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:35:31 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:35:31 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:35:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:35:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:35:35 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:35:36 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:35:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:35:39 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:35:40 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:36:47 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:36:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bb323765ff7b405cedec6f88daa8a1c8470f45c358d637c0062cf4c63d7e07`  
		Last Modified: Wed, 13 Mar 2024 02:41:21 GMT  
		Size: 465.6 KB (465620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b3f11ec4ee425a6a0b9f5ad200c9193592181f59520c9a80372e647787163a`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ffe491a522455b1d95c1d0d3384188ea361064259fffcadd657bebae4fa934`  
		Last Modified: Wed, 13 Mar 2024 02:41:24 GMT  
		Size: 15.3 MB (15277213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b62af40926c0d1a37e6126f41f63533166809b5b54434cf3b53ab5734357e59`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a9b1639ec2e8588ca4fd94f87b31b4e30adef3c0ac45ea4ac0e4cdce643d6`  
		Last Modified: Wed, 13 Mar 2024 02:41:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7a48958fcb11d52bb7a65f60d6f322d3326d4f2916e0547b764cbe4fe0eae8`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9eb36d28260e8ba5549b16a87d121a4d7b0d38f46e1127ee1fd95f2e31e6f2c`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d221a46e4e966da289289be19ac425d0199540bef1d6d7c890ba45ec255e79`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feeda3213337ce81d383bcb08c0b241e763185b91a2e180f35c59395e3c0290f`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d7bf5ae3a283a09c7a385afa5160b2d0f1d275fc23e0a1711bf734511fe0b1`  
		Last Modified: Wed, 13 Mar 2024 02:41:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f309d19b55289fe422d64dd24736be59a52f6eba872d8fb1054416f8b5d9c553`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4ac1a4021eeee54512dde50b437001408fd1dda9d896f68d38728f7dba8c6c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e117655b528b6e8f7ce8d4d2cb69d41a1735fec0e31e10dc40cddcf0d012be`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5524c6d618843e710fa22d77e57a844c7cdfd68676c809d2d1ecde656c16a81c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879784be55be2c5d212302ae42232de9bfeaccea0b1398ec0101ef36d542930c`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f8aadcc42505eea344cf0504c7312d01033f159e88d6eadab5abb9eefc98a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41580c6cc25a82ee1a4de9315ec98ce6e89bd73461a941248648d04292e9ff52`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1261dc2b6b686493c5c3989f8efdd404b912398f6a38933aba80fe65d5d6240c`  
		Last Modified: Wed, 13 Mar 2024 02:41:15 GMT  
		Size: 258.2 KB (258159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8856855cc09ca543e8712766ea12d12556af369305babcaf786f620c89c3450d`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:3e51c662d70a2bcf344a51331fb88b7d223db9cc683b01463633782351400cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:2a10673838e2beefb539398925457319c1e7800b242f5c261bc40ddd7f16aa33
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2141123401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001b000d65334996d09969a3e79ce6304b5ea6811c67eb7add59f0c78b73ba5c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:34:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:34:08 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:35:29 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:35:30 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:35:31 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:35:31 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:35:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:35:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:35:35 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:35:36 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:35:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:35:39 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:35:40 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:36:47 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:36:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bb323765ff7b405cedec6f88daa8a1c8470f45c358d637c0062cf4c63d7e07`  
		Last Modified: Wed, 13 Mar 2024 02:41:21 GMT  
		Size: 465.6 KB (465620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b3f11ec4ee425a6a0b9f5ad200c9193592181f59520c9a80372e647787163a`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ffe491a522455b1d95c1d0d3384188ea361064259fffcadd657bebae4fa934`  
		Last Modified: Wed, 13 Mar 2024 02:41:24 GMT  
		Size: 15.3 MB (15277213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b62af40926c0d1a37e6126f41f63533166809b5b54434cf3b53ab5734357e59`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a9b1639ec2e8588ca4fd94f87b31b4e30adef3c0ac45ea4ac0e4cdce643d6`  
		Last Modified: Wed, 13 Mar 2024 02:41:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7a48958fcb11d52bb7a65f60d6f322d3326d4f2916e0547b764cbe4fe0eae8`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9eb36d28260e8ba5549b16a87d121a4d7b0d38f46e1127ee1fd95f2e31e6f2c`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d221a46e4e966da289289be19ac425d0199540bef1d6d7c890ba45ec255e79`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feeda3213337ce81d383bcb08c0b241e763185b91a2e180f35c59395e3c0290f`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d7bf5ae3a283a09c7a385afa5160b2d0f1d275fc23e0a1711bf734511fe0b1`  
		Last Modified: Wed, 13 Mar 2024 02:41:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f309d19b55289fe422d64dd24736be59a52f6eba872d8fb1054416f8b5d9c553`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4ac1a4021eeee54512dde50b437001408fd1dda9d896f68d38728f7dba8c6c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e117655b528b6e8f7ce8d4d2cb69d41a1735fec0e31e10dc40cddcf0d012be`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5524c6d618843e710fa22d77e57a844c7cdfd68676c809d2d1ecde656c16a81c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879784be55be2c5d212302ae42232de9bfeaccea0b1398ec0101ef36d542930c`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f8aadcc42505eea344cf0504c7312d01033f159e88d6eadab5abb9eefc98a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41580c6cc25a82ee1a4de9315ec98ce6e89bd73461a941248648d04292e9ff52`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1261dc2b6b686493c5c3989f8efdd404b912398f6a38933aba80fe65d5d6240c`  
		Last Modified: Wed, 13 Mar 2024 02:41:15 GMT  
		Size: 258.2 KB (258159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8856855cc09ca543e8712766ea12d12556af369305babcaf786f620c89c3450d`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:e56fe39382d5d420f2ca9e2758ad977fc5a521e371d1658d8f98d8fd55615b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:e92a98f9befbcc685cba6014745c4c4e5573d524f98646666afae41fe635a647
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1973514153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c02263e4345786d822a7cbe2109be66b8bbc405dad0088432e203c583cdb8c4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:37:25 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:37:26 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:37:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:37:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:37:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:37:54 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:37:55 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:37:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:37:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:37:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:38:00 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:38:01 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:38:03 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:38:21 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:38:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3433f0cddf0bf50f831ae26d44034fb9ccdaea63173630b59cbe9dc33860a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:45 GMT  
		Size: 471.5 KB (471467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39aa89107a4c1ac15acc37ba98faa00f98774062e839984cd569c84acccbefa`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903c57abacc03a4132d1914d83b140d91cad6d3f72113588dbb0449668e5459e`  
		Last Modified: Wed, 13 Mar 2024 02:41:47 GMT  
		Size: 15.3 MB (15272331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c505d8db5c54f9f5b13a230f310c78e1daa9f0fa5baa7db6bb4b6f9b2824c64`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02c7783ff4e4ea0351aa496f9316d007b5d39dd7ac091772a53c788cc850835`  
		Last Modified: Wed, 13 Mar 2024 02:41:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2f6f475cd8b631685eb3441f13c0418b595dc3f64fc43f4de103cd270bd07a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c099338186092d8e8a9ee4e1aef2ac6bac6e0e37d05b00acc2519d4828eebc1a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66be30fd26f10adf7753fc7287726b290417f432503173cc8cfcc37c5970eed5`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdecded462eba57ac719ddeaf73027953397d9470c8d9ce91486b650688448d1`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b196924a8268e867bced4e92552ad7a24d5079dd5d3a5f2d32e98acf5b94ec`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83e0533daa0143428320795f95f747a318ce9dfaec9c1918dc09ddabff7ce6`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d6f7d580438b0f330c60e990071ee0a7fd2cb8e861b5b3673229aae5f40a97`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3043316cf0d3543d7ad8c2cf29b9f42217a7ff7ee358b9ccf49ec1c2742b40dc`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9d07b35dd72d9c89f56d604b5b5ff1096607de0b699a7845b4d4eef4542999`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7138f2320f3eb26befb56422d151646fa73d61b45b1fd7ba1a97e97b12b1794`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dd6eb25db87e92a30fe3a646b0ca820c3a8a855af39f49e9c1239e9e7e8fa8`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff49c00e60e2791dac19058d6bba6e562c80b90859f8e91ae70b474a582042`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c28453d92f8177a5ca4103ba031b5f02ceb70269930e8642e8bda358f1eef11`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 289.3 KB (289264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5958cc3ab872a13ea8011a1ae0a2290cefbfb5721bf58c5c16e2a1dfa216aa`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
