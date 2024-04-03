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
$ docker pull caddy@sha256:d8d3637a26f50bf0bd27a6151d2bd4f7a9f0455936fe7ca2498abbc2e26c841e
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
$ docker pull caddy@sha256:7fe86b8d0a4ab9cc95af609981d9cc4785288153254527b6ce37c9aae294c41b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17818318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647d08542df608b54d411f5170ded798422f492e7ca52d28335302b19ab8bb04`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:47:10 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 22:47:12 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 22:47:12 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 22:47:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 22:47:14 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 22:47:15 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 80
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 443
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 22:47:16 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 22:47:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d8802929e2d48f3cf4a528aefc7062f333f3187f4f49ddcbef8f085f8e8521`  
		Last Modified: Sat, 16 Mar 2024 22:49:52 GMT  
		Size: 355.0 KB (354951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe969db5b07e129eba5337dc67eab96b2be79254dab504472f04a8999fafc606`  
		Last Modified: Sat, 16 Mar 2024 22:49:52 GMT  
		Size: 7.5 KB (7527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47567cb4f626213c881a07becf3291a6a7f2590ed16ee927285be3725fc56c5a`  
		Last Modified: Sat, 16 Mar 2024 22:49:54 GMT  
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
$ docker pull caddy@sha256:95ce04978787e23e35143d23b8af2fbb6d6de55213b54a2e9ed2dbf8ffe7313c
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
$ docker pull caddy@sha256:7fe86b8d0a4ab9cc95af609981d9cc4785288153254527b6ce37c9aae294c41b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17818318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647d08542df608b54d411f5170ded798422f492e7ca52d28335302b19ab8bb04`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:47:10 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 22:47:12 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 22:47:12 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 22:47:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 22:47:14 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 22:47:15 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 80
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 443
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 22:47:16 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 22:47:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d8802929e2d48f3cf4a528aefc7062f333f3187f4f49ddcbef8f085f8e8521`  
		Last Modified: Sat, 16 Mar 2024 22:49:52 GMT  
		Size: 355.0 KB (354951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe969db5b07e129eba5337dc67eab96b2be79254dab504472f04a8999fafc606`  
		Last Modified: Sat, 16 Mar 2024 22:49:52 GMT  
		Size: 7.5 KB (7527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47567cb4f626213c881a07becf3291a6a7f2590ed16ee927285be3725fc56c5a`  
		Last Modified: Sat, 16 Mar 2024 22:49:54 GMT  
		Size: 14.2 MB (14238310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder`

```console
$ docker pull caddy@sha256:cc5f4cfd38d48b496b9d5e2a86a32243dd711af077e55dd18bca97ba3055c1d4
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
$ docker pull caddy@sha256:1b98f3fd892c1605c157cc3a049bded9d706ffd51d9a753e18ab07510d0d9e2a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76971330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e800cc7a9c84d26699931116102217b923104964e820bba39098ea1b544f5e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:41:31 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:41:31 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:41:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:41:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:41:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7862e08f4a3ed79ba32d02613b9c596dea827892605f23ebad6c4860ecfd1a4d`  
		Last Modified: Sat, 16 Mar 2024 08:03:57 GMT  
		Size: 284.7 KB (284695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df492c9dc93cdba9fed81e4389415b485127c9cb37c86b79b3f142702574a5a`  
		Last Modified: Wed, 03 Apr 2024 17:02:10 GMT  
		Size: 67.0 MB (67008211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7629e6793208752706519ae9acfbe8b7ad6bdd634d81a69dbcfed6930884369c`  
		Last Modified: Wed, 03 Apr 2024 17:02:00 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3317a43f465a5aebb363d397b3672606d18a5e247747ffd2684c1d0f74de0c6`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 5.0 MB (4973037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f015372e3250fa052df943aed69b26ce6d683b45328456139b9ab7ea453fdf`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 1.3 MB (1302233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6212759f5b367912c99a78b73d4277c50b224f19fe85ce2a3a9fbc94ed16be`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 405.0 B  
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
$ docker pull caddy@sha256:a31ab129389e3b3ac05560de4c52b0c6eada751beddf9acac3e8f35b9ef8c890
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64ab8f668dda6c40c8b5f34a24568989c2d59aa3868bca24a60d427bae87453`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:19:54 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:19:54 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:19:55 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:19:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:19:56 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:19:59 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:19:59 GMT
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
	-	`sha256:fef743b67b508d786f3e8c07ac7dca5aae6ea84a61aa62040b9488dcb2a61415`  
		Last Modified: Wed, 03 Apr 2024 17:04:20 GMT  
		Size: 65.8 MB (65766731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebfed2c271f130a93577b99cfaa3d4478590defaf383477153c1651a8e99a9`  
		Last Modified: Wed, 03 Apr 2024 17:04:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b09688e6219de2aeb2517b1fa78a0827e04df6051fd6bffe0eaec255bef97a`  
		Last Modified: Wed, 03 Apr 2024 17:20:22 GMT  
		Size: 4.5 MB (4514632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c14897ae7beed5a75683641e846e60b36c4ee61bdc37b9f469f54e1f4cf3fa`  
		Last Modified: Wed, 03 Apr 2024 17:20:21 GMT  
		Size: 1.2 MB (1246085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b24f949532888fed8d67d1c3b6a71965df7120dca4ae0931796d19ed24f9eb0`  
		Last Modified: Wed, 03 Apr 2024 17:20:21 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:9abc7c94f1374507e4fb3b81219f95268cd31f587383aa65ed562e3632f31ad3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73990594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53bd0a763baf79c779ab2df43b12f525bb58428beda8002ee1d684d7d6b97bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:17:39 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:17:39 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:17:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:17:41 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:17:41 GMT
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
	-	`sha256:d6de4b400683f0c2362cd880beab320a91316cc24f9f1ecbf576711db2be1bcd`  
		Last Modified: Wed, 03 Apr 2024 17:02:05 GMT  
		Size: 64.1 MB (64107935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cb2a7552d02e7b8e08bf29d0ad4ff98976de8d65f841ce2d42311feeefde4c`  
		Last Modified: Wed, 03 Apr 2024 17:00:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47f7261edc01476f5c0b0525e8f13cc9657f43606014d847afa574f072909ac`  
		Last Modified: Wed, 03 Apr 2024 17:17:57 GMT  
		Size: 5.1 MB (5063925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84aaf63ffe94c0dc9204c45df4cc7bb295e68028c5dc918d66c4b6a947a90783`  
		Last Modified: Wed, 03 Apr 2024 17:17:56 GMT  
		Size: 1.2 MB (1198447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c212b8dc9ff8e7943ac82424077aa3c9fa166ec6c2b15e1391120730607c83`  
		Last Modified: Wed, 03 Apr 2024 17:17:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:3a698c4439f62c22b347f40670cca759481b4368e86535ff7c8c90e26974a7b9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74222636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4c6495ce537716c6f5656c4b703e10cdc4908c76fee2d10efcde9ba1428bf2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:21:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:21:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:22:00 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:22:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:22:00 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:22:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:22:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:22:03 GMT
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
	-	`sha256:3dc9420a97e4b56d60b6f6e43e57c1a0d5699839dfc799b4251d0499da4fdd88`  
		Last Modified: Wed, 03 Apr 2024 17:06:19 GMT  
		Size: 64.1 MB (64129697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a95c9b8692b60f2d2834350493299931b57072a905e77764ab2a07c7be44b7`  
		Last Modified: Wed, 03 Apr 2024 17:06:07 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c79cba53bb3aec5e78f2aa326cb786811cad80519236a541f8cafc627e297c`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 5.3 MB (5270996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69323be82d9f1dfdc2a178ab91b6388fa9c05bec31f9f1df95e1e1429ca4a3c7`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3f305185cfe4c977fae095795eb511d3544f159d8622f4d8fc7b172edd3643`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:71bc6c7a27089f10bb8fb6a701c2d6e2e1b1b097cc301c0d7e0537f1a97b550d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76102402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06da9a536513bc321f389c5c495c8f107c86b098d3db35fd0730f8a8de9d99d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 18:44:19 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 18:44:20 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 18:44:20 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 18:44:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 18:44:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 18:44:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 18:44:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 18:44:26 GMT
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
	-	`sha256:a9c0594d97c8cf4a046ce171a13f9a84a6bbb0b217f0694c3c2bd4d4e5b04be4`  
		Last Modified: Wed, 03 Apr 2024 17:30:50 GMT  
		Size: 66.2 MB (66219505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd26c37806dce963a4a27ef2b2db557bd73ac7834ed03be5caee0fb00f7fd04`  
		Last Modified: Wed, 03 Apr 2024 17:30:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab984370b902d79aea4a3b6f6836818ad0c6ea617bb48b1d51510bdafc407394`  
		Last Modified: Wed, 03 Apr 2024 18:46:09 GMT  
		Size: 5.1 MB (5117274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddb778247a116db89ac5778d4d4f54943f6cb5761fa79984dc7b1e230388caf`  
		Last Modified: Wed, 03 Apr 2024 18:46:08 GMT  
		Size: 1.3 MB (1262392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fa7a5ae42d88199c81c0faeb5c2cbdc5d23284280bf6fc75f5392621db3480`  
		Last Modified: Wed, 03 Apr 2024 18:46:08 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:217de50aa2da8ce751fcf86af874352c567fd2890a7af933d96b71b9cd686ab7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2054329601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5fca8b12e88afae211f90e44879d0eff32c2faddcf2f98239f84ff801975ab`
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
# Wed, 03 Apr 2024 17:11:09 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 17:13:34 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Apr 2024 17:13:36 GMT
WORKDIR C:\go
# Wed, 03 Apr 2024 17:46:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Apr 2024 17:46:15 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:46:16 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:46:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:46:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 03 Apr 2024 17:46:41 GMT
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
	-	`sha256:bba8f7ecb6aa5358813c663a8a821d1558f9fc231d3724d61963281d33c2e29d`  
		Last Modified: Wed, 03 Apr 2024 17:26:14 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645f42306e40e7cd27968b015e4ffd34928e43341ed0891a002a7038a0e92aad`  
		Last Modified: Wed, 03 Apr 2024 17:26:34 GMT  
		Size: 69.4 MB (69360591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b143f0a2277fa1d64dd7e4b237cdd6dee7b9588492e8f25e1f9a6f851ea84e3b`  
		Last Modified: Wed, 03 Apr 2024 17:26:14 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1547026bfff2e6197321109a9232c8d890758f34e98389383329811ca6d0cc2a`  
		Last Modified: Wed, 03 Apr 2024 17:47:34 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07757497ec2b71297a55c100a7253a5180839f418c47af25edff072294bba64`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3f141b6cc8b1b397eaca67bc234dff3e69a2a848385cd18a6f71f0e672d18c`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0988228d5bf035f168b753ec12db6dd4984f8758ac9c0c1ff3d92dabaa4ea452`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebf104fa97c496c43790a481b80954576c09380b483c4bef5fea5a1d017cab4`  
		Last Modified: Wed, 03 Apr 2024 17:47:33 GMT  
		Size: 1.7 MB (1666185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c7907d9819b9165f71f85f596a1a535a4857f3af02b44444b224cf8d588e38`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:8d209986e9cd0835be85e8f65905a45f09bbcf92d15c8d09fc474cfd921f042b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221960398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb43e28d9922862c630fec0d1ba1aa98980080ac6eee5431d9d200d7d373590`
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
# Wed, 03 Apr 2024 17:13:54 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 17:17:31 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Apr 2024 17:17:33 GMT
WORKDIR C:\go
# Wed, 03 Apr 2024 17:44:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Apr 2024 17:44:32 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:44:32 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:44:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:45:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 03 Apr 2024 17:45:58 GMT
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
	-	`sha256:584a26f47e4b040924987f5714e3904994464b2082794beebf1b84e0a4a711b3`  
		Last Modified: Wed, 03 Apr 2024 17:26:44 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e106baac3b372ef5b64f477236dcdd8c76bd7692c1d1a9a8c61596376a474f5e`  
		Last Modified: Wed, 03 Apr 2024 17:27:04 GMT  
		Size: 69.4 MB (69363419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e891eced875ee145e4fc5c147c8f84ff77215d4e5a1a86cff047c2697b417650`  
		Last Modified: Wed, 03 Apr 2024 17:26:44 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb621e6ec00bf92d79e37d3cb91e9ce4d633edce6c6618cbeeb19e40e482988`  
		Last Modified: Wed, 03 Apr 2024 17:47:18 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b816cd0d77c5e8e4f9e8e648b807ffb2e79e861b17670d9841ae2bf48852d2ba`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d0826717e8d6b364230bdd7ed7dd491d35a95be7323df3a90a68ded19a6ff5`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c00c4e7e6cf5e71b9dabdc9e7e221f5ce9450755ca1ad90c402e483f199ae8`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a2f091b6ab0aebf8b669a0f95d00a5b934be2ed7563f5bbf55986abe9d2efe`  
		Last Modified: Wed, 03 Apr 2024 17:47:17 GMT  
		Size: 1.7 MB (1666239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427e8173580c10665cb7ac17da9df0fdf012ced3b7aeb9262a86eced50bbb7c8`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:721348b9c1549c1d715b571c48ca9764ad81bdf5f7ef34682b09856c300e1f56
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
$ docker pull caddy@sha256:1b98f3fd892c1605c157cc3a049bded9d706ffd51d9a753e18ab07510d0d9e2a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76971330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e800cc7a9c84d26699931116102217b923104964e820bba39098ea1b544f5e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:41:31 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:41:31 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:41:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:41:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:41:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7862e08f4a3ed79ba32d02613b9c596dea827892605f23ebad6c4860ecfd1a4d`  
		Last Modified: Sat, 16 Mar 2024 08:03:57 GMT  
		Size: 284.7 KB (284695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df492c9dc93cdba9fed81e4389415b485127c9cb37c86b79b3f142702574a5a`  
		Last Modified: Wed, 03 Apr 2024 17:02:10 GMT  
		Size: 67.0 MB (67008211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7629e6793208752706519ae9acfbe8b7ad6bdd634d81a69dbcfed6930884369c`  
		Last Modified: Wed, 03 Apr 2024 17:02:00 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3317a43f465a5aebb363d397b3672606d18a5e247747ffd2684c1d0f74de0c6`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 5.0 MB (4973037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f015372e3250fa052df943aed69b26ce6d683b45328456139b9ab7ea453fdf`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 1.3 MB (1302233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6212759f5b367912c99a78b73d4277c50b224f19fe85ce2a3a9fbc94ed16be`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 405.0 B  
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
$ docker pull caddy@sha256:a31ab129389e3b3ac05560de4c52b0c6eada751beddf9acac3e8f35b9ef8c890
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64ab8f668dda6c40c8b5f34a24568989c2d59aa3868bca24a60d427bae87453`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:19:54 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:19:54 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:19:55 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:19:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:19:56 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:19:59 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:19:59 GMT
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
	-	`sha256:fef743b67b508d786f3e8c07ac7dca5aae6ea84a61aa62040b9488dcb2a61415`  
		Last Modified: Wed, 03 Apr 2024 17:04:20 GMT  
		Size: 65.8 MB (65766731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebfed2c271f130a93577b99cfaa3d4478590defaf383477153c1651a8e99a9`  
		Last Modified: Wed, 03 Apr 2024 17:04:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b09688e6219de2aeb2517b1fa78a0827e04df6051fd6bffe0eaec255bef97a`  
		Last Modified: Wed, 03 Apr 2024 17:20:22 GMT  
		Size: 4.5 MB (4514632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c14897ae7beed5a75683641e846e60b36c4ee61bdc37b9f469f54e1f4cf3fa`  
		Last Modified: Wed, 03 Apr 2024 17:20:21 GMT  
		Size: 1.2 MB (1246085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b24f949532888fed8d67d1c3b6a71965df7120dca4ae0931796d19ed24f9eb0`  
		Last Modified: Wed, 03 Apr 2024 17:20:21 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:9abc7c94f1374507e4fb3b81219f95268cd31f587383aa65ed562e3632f31ad3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73990594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53bd0a763baf79c779ab2df43b12f525bb58428beda8002ee1d684d7d6b97bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:17:39 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:17:39 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:17:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:17:41 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:17:41 GMT
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
	-	`sha256:d6de4b400683f0c2362cd880beab320a91316cc24f9f1ecbf576711db2be1bcd`  
		Last Modified: Wed, 03 Apr 2024 17:02:05 GMT  
		Size: 64.1 MB (64107935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cb2a7552d02e7b8e08bf29d0ad4ff98976de8d65f841ce2d42311feeefde4c`  
		Last Modified: Wed, 03 Apr 2024 17:00:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47f7261edc01476f5c0b0525e8f13cc9657f43606014d847afa574f072909ac`  
		Last Modified: Wed, 03 Apr 2024 17:17:57 GMT  
		Size: 5.1 MB (5063925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84aaf63ffe94c0dc9204c45df4cc7bb295e68028c5dc918d66c4b6a947a90783`  
		Last Modified: Wed, 03 Apr 2024 17:17:56 GMT  
		Size: 1.2 MB (1198447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c212b8dc9ff8e7943ac82424077aa3c9fa166ec6c2b15e1391120730607c83`  
		Last Modified: Wed, 03 Apr 2024 17:17:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:3a698c4439f62c22b347f40670cca759481b4368e86535ff7c8c90e26974a7b9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74222636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4c6495ce537716c6f5656c4b703e10cdc4908c76fee2d10efcde9ba1428bf2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:21:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:21:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:22:00 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:22:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:22:00 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:22:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:22:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:22:03 GMT
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
	-	`sha256:3dc9420a97e4b56d60b6f6e43e57c1a0d5699839dfc799b4251d0499da4fdd88`  
		Last Modified: Wed, 03 Apr 2024 17:06:19 GMT  
		Size: 64.1 MB (64129697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a95c9b8692b60f2d2834350493299931b57072a905e77764ab2a07c7be44b7`  
		Last Modified: Wed, 03 Apr 2024 17:06:07 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c79cba53bb3aec5e78f2aa326cb786811cad80519236a541f8cafc627e297c`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 5.3 MB (5270996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69323be82d9f1dfdc2a178ab91b6388fa9c05bec31f9f1df95e1e1429ca4a3c7`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3f305185cfe4c977fae095795eb511d3544f159d8622f4d8fc7b172edd3643`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:71bc6c7a27089f10bb8fb6a701c2d6e2e1b1b097cc301c0d7e0537f1a97b550d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76102402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06da9a536513bc321f389c5c495c8f107c86b098d3db35fd0730f8a8de9d99d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 18:44:19 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 18:44:20 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 18:44:20 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 18:44:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 18:44:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 18:44:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 18:44:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 18:44:26 GMT
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
	-	`sha256:a9c0594d97c8cf4a046ce171a13f9a84a6bbb0b217f0694c3c2bd4d4e5b04be4`  
		Last Modified: Wed, 03 Apr 2024 17:30:50 GMT  
		Size: 66.2 MB (66219505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd26c37806dce963a4a27ef2b2db557bd73ac7834ed03be5caee0fb00f7fd04`  
		Last Modified: Wed, 03 Apr 2024 17:30:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab984370b902d79aea4a3b6f6836818ad0c6ea617bb48b1d51510bdafc407394`  
		Last Modified: Wed, 03 Apr 2024 18:46:09 GMT  
		Size: 5.1 MB (5117274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddb778247a116db89ac5778d4d4f54943f6cb5761fa79984dc7b1e230388caf`  
		Last Modified: Wed, 03 Apr 2024 18:46:08 GMT  
		Size: 1.3 MB (1262392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fa7a5ae42d88199c81c0faeb5c2cbdc5d23284280bf6fc75f5392621db3480`  
		Last Modified: Wed, 03 Apr 2024 18:46:08 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:65ffb8f02fbc79cbba4dbb361a8be92005f342bfc1892f7e98f08a843e194a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:8d209986e9cd0835be85e8f65905a45f09bbcf92d15c8d09fc474cfd921f042b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221960398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb43e28d9922862c630fec0d1ba1aa98980080ac6eee5431d9d200d7d373590`
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
# Wed, 03 Apr 2024 17:13:54 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 17:17:31 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Apr 2024 17:17:33 GMT
WORKDIR C:\go
# Wed, 03 Apr 2024 17:44:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Apr 2024 17:44:32 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:44:32 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:44:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:45:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 03 Apr 2024 17:45:58 GMT
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
	-	`sha256:584a26f47e4b040924987f5714e3904994464b2082794beebf1b84e0a4a711b3`  
		Last Modified: Wed, 03 Apr 2024 17:26:44 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e106baac3b372ef5b64f477236dcdd8c76bd7692c1d1a9a8c61596376a474f5e`  
		Last Modified: Wed, 03 Apr 2024 17:27:04 GMT  
		Size: 69.4 MB (69363419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e891eced875ee145e4fc5c147c8f84ff77215d4e5a1a86cff047c2697b417650`  
		Last Modified: Wed, 03 Apr 2024 17:26:44 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb621e6ec00bf92d79e37d3cb91e9ce4d633edce6c6618cbeeb19e40e482988`  
		Last Modified: Wed, 03 Apr 2024 17:47:18 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b816cd0d77c5e8e4f9e8e648b807ffb2e79e861b17670d9841ae2bf48852d2ba`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d0826717e8d6b364230bdd7ed7dd491d35a95be7323df3a90a68ded19a6ff5`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c00c4e7e6cf5e71b9dabdc9e7e221f5ce9450755ca1ad90c402e483f199ae8`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a2f091b6ab0aebf8b669a0f95d00a5b934be2ed7563f5bbf55986abe9d2efe`  
		Last Modified: Wed, 03 Apr 2024 17:47:17 GMT  
		Size: 1.7 MB (1666239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427e8173580c10665cb7ac17da9df0fdf012ced3b7aeb9262a86eced50bbb7c8`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:64f0be6cf22b5b3c1d98a73d8d2e0ec0205594c9246accc32259bf88172be5f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:217de50aa2da8ce751fcf86af874352c567fd2890a7af933d96b71b9cd686ab7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2054329601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5fca8b12e88afae211f90e44879d0eff32c2faddcf2f98239f84ff801975ab`
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
# Wed, 03 Apr 2024 17:11:09 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 17:13:34 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Apr 2024 17:13:36 GMT
WORKDIR C:\go
# Wed, 03 Apr 2024 17:46:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Apr 2024 17:46:15 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:46:16 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:46:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:46:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 03 Apr 2024 17:46:41 GMT
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
	-	`sha256:bba8f7ecb6aa5358813c663a8a821d1558f9fc231d3724d61963281d33c2e29d`  
		Last Modified: Wed, 03 Apr 2024 17:26:14 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645f42306e40e7cd27968b015e4ffd34928e43341ed0891a002a7038a0e92aad`  
		Last Modified: Wed, 03 Apr 2024 17:26:34 GMT  
		Size: 69.4 MB (69360591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b143f0a2277fa1d64dd7e4b237cdd6dee7b9588492e8f25e1f9a6f851ea84e3b`  
		Last Modified: Wed, 03 Apr 2024 17:26:14 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1547026bfff2e6197321109a9232c8d890758f34e98389383329811ca6d0cc2a`  
		Last Modified: Wed, 03 Apr 2024 17:47:34 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07757497ec2b71297a55c100a7253a5180839f418c47af25edff072294bba64`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3f141b6cc8b1b397eaca67bc234dff3e69a2a848385cd18a6f71f0e672d18c`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0988228d5bf035f168b753ec12db6dd4984f8758ac9c0c1ff3d92dabaa4ea452`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebf104fa97c496c43790a481b80954576c09380b483c4bef5fea5a1d017cab4`  
		Last Modified: Wed, 03 Apr 2024 17:47:33 GMT  
		Size: 1.7 MB (1666185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c7907d9819b9165f71f85f596a1a535a4857f3af02b44444b224cf8d588e38`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1281 bytes)  
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
$ docker pull caddy@sha256:d8d3637a26f50bf0bd27a6151d2bd4f7a9f0455936fe7ca2498abbc2e26c841e
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
$ docker pull caddy@sha256:7fe86b8d0a4ab9cc95af609981d9cc4785288153254527b6ce37c9aae294c41b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17818318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647d08542df608b54d411f5170ded798422f492e7ca52d28335302b19ab8bb04`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:47:10 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 22:47:12 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 22:47:12 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 22:47:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 22:47:14 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 22:47:15 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 80
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 443
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 22:47:16 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 22:47:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d8802929e2d48f3cf4a528aefc7062f333f3187f4f49ddcbef8f085f8e8521`  
		Last Modified: Sat, 16 Mar 2024 22:49:52 GMT  
		Size: 355.0 KB (354951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe969db5b07e129eba5337dc67eab96b2be79254dab504472f04a8999fafc606`  
		Last Modified: Sat, 16 Mar 2024 22:49:52 GMT  
		Size: 7.5 KB (7527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47567cb4f626213c881a07becf3291a6a7f2590ed16ee927285be3725fc56c5a`  
		Last Modified: Sat, 16 Mar 2024 22:49:54 GMT  
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
$ docker pull caddy@sha256:95ce04978787e23e35143d23b8af2fbb6d6de55213b54a2e9ed2dbf8ffe7313c
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
$ docker pull caddy@sha256:7fe86b8d0a4ab9cc95af609981d9cc4785288153254527b6ce37c9aae294c41b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17818318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647d08542df608b54d411f5170ded798422f492e7ca52d28335302b19ab8bb04`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:47:10 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 22:47:12 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 22:47:12 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 22:47:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 22:47:14 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 22:47:15 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 80
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 443
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 22:47:16 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 22:47:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d8802929e2d48f3cf4a528aefc7062f333f3187f4f49ddcbef8f085f8e8521`  
		Last Modified: Sat, 16 Mar 2024 22:49:52 GMT  
		Size: 355.0 KB (354951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe969db5b07e129eba5337dc67eab96b2be79254dab504472f04a8999fafc606`  
		Last Modified: Sat, 16 Mar 2024 22:49:52 GMT  
		Size: 7.5 KB (7527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47567cb4f626213c881a07becf3291a6a7f2590ed16ee927285be3725fc56c5a`  
		Last Modified: Sat, 16 Mar 2024 22:49:54 GMT  
		Size: 14.2 MB (14238310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder`

```console
$ docker pull caddy@sha256:cc5f4cfd38d48b496b9d5e2a86a32243dd711af077e55dd18bca97ba3055c1d4
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
$ docker pull caddy@sha256:1b98f3fd892c1605c157cc3a049bded9d706ffd51d9a753e18ab07510d0d9e2a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76971330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e800cc7a9c84d26699931116102217b923104964e820bba39098ea1b544f5e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:41:31 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:41:31 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:41:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:41:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:41:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7862e08f4a3ed79ba32d02613b9c596dea827892605f23ebad6c4860ecfd1a4d`  
		Last Modified: Sat, 16 Mar 2024 08:03:57 GMT  
		Size: 284.7 KB (284695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df492c9dc93cdba9fed81e4389415b485127c9cb37c86b79b3f142702574a5a`  
		Last Modified: Wed, 03 Apr 2024 17:02:10 GMT  
		Size: 67.0 MB (67008211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7629e6793208752706519ae9acfbe8b7ad6bdd634d81a69dbcfed6930884369c`  
		Last Modified: Wed, 03 Apr 2024 17:02:00 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3317a43f465a5aebb363d397b3672606d18a5e247747ffd2684c1d0f74de0c6`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 5.0 MB (4973037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f015372e3250fa052df943aed69b26ce6d683b45328456139b9ab7ea453fdf`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 1.3 MB (1302233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6212759f5b367912c99a78b73d4277c50b224f19fe85ce2a3a9fbc94ed16be`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 405.0 B  
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
$ docker pull caddy@sha256:a31ab129389e3b3ac05560de4c52b0c6eada751beddf9acac3e8f35b9ef8c890
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64ab8f668dda6c40c8b5f34a24568989c2d59aa3868bca24a60d427bae87453`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:19:54 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:19:54 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:19:55 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:19:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:19:56 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:19:59 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:19:59 GMT
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
	-	`sha256:fef743b67b508d786f3e8c07ac7dca5aae6ea84a61aa62040b9488dcb2a61415`  
		Last Modified: Wed, 03 Apr 2024 17:04:20 GMT  
		Size: 65.8 MB (65766731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebfed2c271f130a93577b99cfaa3d4478590defaf383477153c1651a8e99a9`  
		Last Modified: Wed, 03 Apr 2024 17:04:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b09688e6219de2aeb2517b1fa78a0827e04df6051fd6bffe0eaec255bef97a`  
		Last Modified: Wed, 03 Apr 2024 17:20:22 GMT  
		Size: 4.5 MB (4514632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c14897ae7beed5a75683641e846e60b36c4ee61bdc37b9f469f54e1f4cf3fa`  
		Last Modified: Wed, 03 Apr 2024 17:20:21 GMT  
		Size: 1.2 MB (1246085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b24f949532888fed8d67d1c3b6a71965df7120dca4ae0931796d19ed24f9eb0`  
		Last Modified: Wed, 03 Apr 2024 17:20:21 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:9abc7c94f1374507e4fb3b81219f95268cd31f587383aa65ed562e3632f31ad3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73990594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53bd0a763baf79c779ab2df43b12f525bb58428beda8002ee1d684d7d6b97bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:17:39 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:17:39 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:17:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:17:41 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:17:41 GMT
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
	-	`sha256:d6de4b400683f0c2362cd880beab320a91316cc24f9f1ecbf576711db2be1bcd`  
		Last Modified: Wed, 03 Apr 2024 17:02:05 GMT  
		Size: 64.1 MB (64107935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cb2a7552d02e7b8e08bf29d0ad4ff98976de8d65f841ce2d42311feeefde4c`  
		Last Modified: Wed, 03 Apr 2024 17:00:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47f7261edc01476f5c0b0525e8f13cc9657f43606014d847afa574f072909ac`  
		Last Modified: Wed, 03 Apr 2024 17:17:57 GMT  
		Size: 5.1 MB (5063925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84aaf63ffe94c0dc9204c45df4cc7bb295e68028c5dc918d66c4b6a947a90783`  
		Last Modified: Wed, 03 Apr 2024 17:17:56 GMT  
		Size: 1.2 MB (1198447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c212b8dc9ff8e7943ac82424077aa3c9fa166ec6c2b15e1391120730607c83`  
		Last Modified: Wed, 03 Apr 2024 17:17:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:3a698c4439f62c22b347f40670cca759481b4368e86535ff7c8c90e26974a7b9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74222636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4c6495ce537716c6f5656c4b703e10cdc4908c76fee2d10efcde9ba1428bf2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:21:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:21:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:22:00 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:22:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:22:00 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:22:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:22:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:22:03 GMT
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
	-	`sha256:3dc9420a97e4b56d60b6f6e43e57c1a0d5699839dfc799b4251d0499da4fdd88`  
		Last Modified: Wed, 03 Apr 2024 17:06:19 GMT  
		Size: 64.1 MB (64129697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a95c9b8692b60f2d2834350493299931b57072a905e77764ab2a07c7be44b7`  
		Last Modified: Wed, 03 Apr 2024 17:06:07 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c79cba53bb3aec5e78f2aa326cb786811cad80519236a541f8cafc627e297c`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 5.3 MB (5270996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69323be82d9f1dfdc2a178ab91b6388fa9c05bec31f9f1df95e1e1429ca4a3c7`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3f305185cfe4c977fae095795eb511d3544f159d8622f4d8fc7b172edd3643`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; s390x

```console
$ docker pull caddy@sha256:71bc6c7a27089f10bb8fb6a701c2d6e2e1b1b097cc301c0d7e0537f1a97b550d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76102402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06da9a536513bc321f389c5c495c8f107c86b098d3db35fd0730f8a8de9d99d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 18:44:19 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 18:44:20 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 18:44:20 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 18:44:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 18:44:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 18:44:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 18:44:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 18:44:26 GMT
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
	-	`sha256:a9c0594d97c8cf4a046ce171a13f9a84a6bbb0b217f0694c3c2bd4d4e5b04be4`  
		Last Modified: Wed, 03 Apr 2024 17:30:50 GMT  
		Size: 66.2 MB (66219505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd26c37806dce963a4a27ef2b2db557bd73ac7834ed03be5caee0fb00f7fd04`  
		Last Modified: Wed, 03 Apr 2024 17:30:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab984370b902d79aea4a3b6f6836818ad0c6ea617bb48b1d51510bdafc407394`  
		Last Modified: Wed, 03 Apr 2024 18:46:09 GMT  
		Size: 5.1 MB (5117274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddb778247a116db89ac5778d4d4f54943f6cb5761fa79984dc7b1e230388caf`  
		Last Modified: Wed, 03 Apr 2024 18:46:08 GMT  
		Size: 1.3 MB (1262392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fa7a5ae42d88199c81c0faeb5c2cbdc5d23284280bf6fc75f5392621db3480`  
		Last Modified: Wed, 03 Apr 2024 18:46:08 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:217de50aa2da8ce751fcf86af874352c567fd2890a7af933d96b71b9cd686ab7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2054329601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5fca8b12e88afae211f90e44879d0eff32c2faddcf2f98239f84ff801975ab`
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
# Wed, 03 Apr 2024 17:11:09 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 17:13:34 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Apr 2024 17:13:36 GMT
WORKDIR C:\go
# Wed, 03 Apr 2024 17:46:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Apr 2024 17:46:15 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:46:16 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:46:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:46:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 03 Apr 2024 17:46:41 GMT
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
	-	`sha256:bba8f7ecb6aa5358813c663a8a821d1558f9fc231d3724d61963281d33c2e29d`  
		Last Modified: Wed, 03 Apr 2024 17:26:14 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645f42306e40e7cd27968b015e4ffd34928e43341ed0891a002a7038a0e92aad`  
		Last Modified: Wed, 03 Apr 2024 17:26:34 GMT  
		Size: 69.4 MB (69360591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b143f0a2277fa1d64dd7e4b237cdd6dee7b9588492e8f25e1f9a6f851ea84e3b`  
		Last Modified: Wed, 03 Apr 2024 17:26:14 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1547026bfff2e6197321109a9232c8d890758f34e98389383329811ca6d0cc2a`  
		Last Modified: Wed, 03 Apr 2024 17:47:34 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07757497ec2b71297a55c100a7253a5180839f418c47af25edff072294bba64`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3f141b6cc8b1b397eaca67bc234dff3e69a2a848385cd18a6f71f0e672d18c`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0988228d5bf035f168b753ec12db6dd4984f8758ac9c0c1ff3d92dabaa4ea452`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebf104fa97c496c43790a481b80954576c09380b483c4bef5fea5a1d017cab4`  
		Last Modified: Wed, 03 Apr 2024 17:47:33 GMT  
		Size: 1.7 MB (1666185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c7907d9819b9165f71f85f596a1a535a4857f3af02b44444b224cf8d588e38`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:8d209986e9cd0835be85e8f65905a45f09bbcf92d15c8d09fc474cfd921f042b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221960398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb43e28d9922862c630fec0d1ba1aa98980080ac6eee5431d9d200d7d373590`
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
# Wed, 03 Apr 2024 17:13:54 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 17:17:31 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Apr 2024 17:17:33 GMT
WORKDIR C:\go
# Wed, 03 Apr 2024 17:44:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Apr 2024 17:44:32 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:44:32 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:44:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:45:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 03 Apr 2024 17:45:58 GMT
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
	-	`sha256:584a26f47e4b040924987f5714e3904994464b2082794beebf1b84e0a4a711b3`  
		Last Modified: Wed, 03 Apr 2024 17:26:44 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e106baac3b372ef5b64f477236dcdd8c76bd7692c1d1a9a8c61596376a474f5e`  
		Last Modified: Wed, 03 Apr 2024 17:27:04 GMT  
		Size: 69.4 MB (69363419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e891eced875ee145e4fc5c147c8f84ff77215d4e5a1a86cff047c2697b417650`  
		Last Modified: Wed, 03 Apr 2024 17:26:44 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb621e6ec00bf92d79e37d3cb91e9ce4d633edce6c6618cbeeb19e40e482988`  
		Last Modified: Wed, 03 Apr 2024 17:47:18 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b816cd0d77c5e8e4f9e8e648b807ffb2e79e861b17670d9841ae2bf48852d2ba`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d0826717e8d6b364230bdd7ed7dd491d35a95be7323df3a90a68ded19a6ff5`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c00c4e7e6cf5e71b9dabdc9e7e221f5ce9450755ca1ad90c402e483f199ae8`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a2f091b6ab0aebf8b669a0f95d00a5b934be2ed7563f5bbf55986abe9d2efe`  
		Last Modified: Wed, 03 Apr 2024 17:47:17 GMT  
		Size: 1.7 MB (1666239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427e8173580c10665cb7ac17da9df0fdf012ced3b7aeb9262a86eced50bbb7c8`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-alpine`

```console
$ docker pull caddy@sha256:721348b9c1549c1d715b571c48ca9764ad81bdf5f7ef34682b09856c300e1f56
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
$ docker pull caddy@sha256:1b98f3fd892c1605c157cc3a049bded9d706ffd51d9a753e18ab07510d0d9e2a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76971330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e800cc7a9c84d26699931116102217b923104964e820bba39098ea1b544f5e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:41:31 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:41:31 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:41:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:41:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:41:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7862e08f4a3ed79ba32d02613b9c596dea827892605f23ebad6c4860ecfd1a4d`  
		Last Modified: Sat, 16 Mar 2024 08:03:57 GMT  
		Size: 284.7 KB (284695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df492c9dc93cdba9fed81e4389415b485127c9cb37c86b79b3f142702574a5a`  
		Last Modified: Wed, 03 Apr 2024 17:02:10 GMT  
		Size: 67.0 MB (67008211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7629e6793208752706519ae9acfbe8b7ad6bdd634d81a69dbcfed6930884369c`  
		Last Modified: Wed, 03 Apr 2024 17:02:00 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3317a43f465a5aebb363d397b3672606d18a5e247747ffd2684c1d0f74de0c6`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 5.0 MB (4973037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f015372e3250fa052df943aed69b26ce6d683b45328456139b9ab7ea453fdf`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 1.3 MB (1302233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6212759f5b367912c99a78b73d4277c50b224f19fe85ce2a3a9fbc94ed16be`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 405.0 B  
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
$ docker pull caddy@sha256:a31ab129389e3b3ac05560de4c52b0c6eada751beddf9acac3e8f35b9ef8c890
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64ab8f668dda6c40c8b5f34a24568989c2d59aa3868bca24a60d427bae87453`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:19:54 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:19:54 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:19:55 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:19:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:19:56 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:19:59 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:19:59 GMT
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
	-	`sha256:fef743b67b508d786f3e8c07ac7dca5aae6ea84a61aa62040b9488dcb2a61415`  
		Last Modified: Wed, 03 Apr 2024 17:04:20 GMT  
		Size: 65.8 MB (65766731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebfed2c271f130a93577b99cfaa3d4478590defaf383477153c1651a8e99a9`  
		Last Modified: Wed, 03 Apr 2024 17:04:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b09688e6219de2aeb2517b1fa78a0827e04df6051fd6bffe0eaec255bef97a`  
		Last Modified: Wed, 03 Apr 2024 17:20:22 GMT  
		Size: 4.5 MB (4514632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c14897ae7beed5a75683641e846e60b36c4ee61bdc37b9f469f54e1f4cf3fa`  
		Last Modified: Wed, 03 Apr 2024 17:20:21 GMT  
		Size: 1.2 MB (1246085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b24f949532888fed8d67d1c3b6a71965df7120dca4ae0931796d19ed24f9eb0`  
		Last Modified: Wed, 03 Apr 2024 17:20:21 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:9abc7c94f1374507e4fb3b81219f95268cd31f587383aa65ed562e3632f31ad3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73990594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53bd0a763baf79c779ab2df43b12f525bb58428beda8002ee1d684d7d6b97bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:17:39 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:17:39 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:17:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:17:41 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:17:41 GMT
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
	-	`sha256:d6de4b400683f0c2362cd880beab320a91316cc24f9f1ecbf576711db2be1bcd`  
		Last Modified: Wed, 03 Apr 2024 17:02:05 GMT  
		Size: 64.1 MB (64107935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cb2a7552d02e7b8e08bf29d0ad4ff98976de8d65f841ce2d42311feeefde4c`  
		Last Modified: Wed, 03 Apr 2024 17:00:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47f7261edc01476f5c0b0525e8f13cc9657f43606014d847afa574f072909ac`  
		Last Modified: Wed, 03 Apr 2024 17:17:57 GMT  
		Size: 5.1 MB (5063925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84aaf63ffe94c0dc9204c45df4cc7bb295e68028c5dc918d66c4b6a947a90783`  
		Last Modified: Wed, 03 Apr 2024 17:17:56 GMT  
		Size: 1.2 MB (1198447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c212b8dc9ff8e7943ac82424077aa3c9fa166ec6c2b15e1391120730607c83`  
		Last Modified: Wed, 03 Apr 2024 17:17:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:3a698c4439f62c22b347f40670cca759481b4368e86535ff7c8c90e26974a7b9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74222636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4c6495ce537716c6f5656c4b703e10cdc4908c76fee2d10efcde9ba1428bf2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:21:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:21:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:22:00 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:22:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:22:00 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:22:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:22:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:22:03 GMT
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
	-	`sha256:3dc9420a97e4b56d60b6f6e43e57c1a0d5699839dfc799b4251d0499da4fdd88`  
		Last Modified: Wed, 03 Apr 2024 17:06:19 GMT  
		Size: 64.1 MB (64129697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a95c9b8692b60f2d2834350493299931b57072a905e77764ab2a07c7be44b7`  
		Last Modified: Wed, 03 Apr 2024 17:06:07 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c79cba53bb3aec5e78f2aa326cb786811cad80519236a541f8cafc627e297c`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 5.3 MB (5270996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69323be82d9f1dfdc2a178ab91b6388fa9c05bec31f9f1df95e1e1429ca4a3c7`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3f305185cfe4c977fae095795eb511d3544f159d8622f4d8fc7b172edd3643`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:71bc6c7a27089f10bb8fb6a701c2d6e2e1b1b097cc301c0d7e0537f1a97b550d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76102402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06da9a536513bc321f389c5c495c8f107c86b098d3db35fd0730f8a8de9d99d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 18:44:19 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 18:44:20 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 18:44:20 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 18:44:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 18:44:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 18:44:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 18:44:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 18:44:26 GMT
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
	-	`sha256:a9c0594d97c8cf4a046ce171a13f9a84a6bbb0b217f0694c3c2bd4d4e5b04be4`  
		Last Modified: Wed, 03 Apr 2024 17:30:50 GMT  
		Size: 66.2 MB (66219505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd26c37806dce963a4a27ef2b2db557bd73ac7834ed03be5caee0fb00f7fd04`  
		Last Modified: Wed, 03 Apr 2024 17:30:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab984370b902d79aea4a3b6f6836818ad0c6ea617bb48b1d51510bdafc407394`  
		Last Modified: Wed, 03 Apr 2024 18:46:09 GMT  
		Size: 5.1 MB (5117274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddb778247a116db89ac5778d4d4f54943f6cb5761fa79984dc7b1e230388caf`  
		Last Modified: Wed, 03 Apr 2024 18:46:08 GMT  
		Size: 1.3 MB (1262392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fa7a5ae42d88199c81c0faeb5c2cbdc5d23284280bf6fc75f5392621db3480`  
		Last Modified: Wed, 03 Apr 2024 18:46:08 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:65ffb8f02fbc79cbba4dbb361a8be92005f342bfc1892f7e98f08a843e194a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `caddy:2.7-builder-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:8d209986e9cd0835be85e8f65905a45f09bbcf92d15c8d09fc474cfd921f042b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221960398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb43e28d9922862c630fec0d1ba1aa98980080ac6eee5431d9d200d7d373590`
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
# Wed, 03 Apr 2024 17:13:54 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 17:17:31 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Apr 2024 17:17:33 GMT
WORKDIR C:\go
# Wed, 03 Apr 2024 17:44:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Apr 2024 17:44:32 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:44:32 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:44:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:45:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 03 Apr 2024 17:45:58 GMT
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
	-	`sha256:584a26f47e4b040924987f5714e3904994464b2082794beebf1b84e0a4a711b3`  
		Last Modified: Wed, 03 Apr 2024 17:26:44 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e106baac3b372ef5b64f477236dcdd8c76bd7692c1d1a9a8c61596376a474f5e`  
		Last Modified: Wed, 03 Apr 2024 17:27:04 GMT  
		Size: 69.4 MB (69363419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e891eced875ee145e4fc5c147c8f84ff77215d4e5a1a86cff047c2697b417650`  
		Last Modified: Wed, 03 Apr 2024 17:26:44 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb621e6ec00bf92d79e37d3cb91e9ce4d633edce6c6618cbeeb19e40e482988`  
		Last Modified: Wed, 03 Apr 2024 17:47:18 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b816cd0d77c5e8e4f9e8e648b807ffb2e79e861b17670d9841ae2bf48852d2ba`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d0826717e8d6b364230bdd7ed7dd491d35a95be7323df3a90a68ded19a6ff5`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c00c4e7e6cf5e71b9dabdc9e7e221f5ce9450755ca1ad90c402e483f199ae8`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a2f091b6ab0aebf8b669a0f95d00a5b934be2ed7563f5bbf55986abe9d2efe`  
		Last Modified: Wed, 03 Apr 2024 17:47:17 GMT  
		Size: 1.7 MB (1666239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427e8173580c10665cb7ac17da9df0fdf012ced3b7aeb9262a86eced50bbb7c8`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:64f0be6cf22b5b3c1d98a73d8d2e0ec0205594c9246accc32259bf88172be5f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `caddy:2.7-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:217de50aa2da8ce751fcf86af874352c567fd2890a7af933d96b71b9cd686ab7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2054329601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5fca8b12e88afae211f90e44879d0eff32c2faddcf2f98239f84ff801975ab`
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
# Wed, 03 Apr 2024 17:11:09 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 17:13:34 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Apr 2024 17:13:36 GMT
WORKDIR C:\go
# Wed, 03 Apr 2024 17:46:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Apr 2024 17:46:15 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:46:16 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:46:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:46:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 03 Apr 2024 17:46:41 GMT
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
	-	`sha256:bba8f7ecb6aa5358813c663a8a821d1558f9fc231d3724d61963281d33c2e29d`  
		Last Modified: Wed, 03 Apr 2024 17:26:14 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645f42306e40e7cd27968b015e4ffd34928e43341ed0891a002a7038a0e92aad`  
		Last Modified: Wed, 03 Apr 2024 17:26:34 GMT  
		Size: 69.4 MB (69360591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b143f0a2277fa1d64dd7e4b237cdd6dee7b9588492e8f25e1f9a6f851ea84e3b`  
		Last Modified: Wed, 03 Apr 2024 17:26:14 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1547026bfff2e6197321109a9232c8d890758f34e98389383329811ca6d0cc2a`  
		Last Modified: Wed, 03 Apr 2024 17:47:34 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07757497ec2b71297a55c100a7253a5180839f418c47af25edff072294bba64`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3f141b6cc8b1b397eaca67bc234dff3e69a2a848385cd18a6f71f0e672d18c`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0988228d5bf035f168b753ec12db6dd4984f8758ac9c0c1ff3d92dabaa4ea452`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebf104fa97c496c43790a481b80954576c09380b483c4bef5fea5a1d017cab4`  
		Last Modified: Wed, 03 Apr 2024 17:47:33 GMT  
		Size: 1.7 MB (1666185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c7907d9819b9165f71f85f596a1a535a4857f3af02b44444b224cf8d588e38`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1281 bytes)  
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
$ docker pull caddy@sha256:d8d3637a26f50bf0bd27a6151d2bd4f7a9f0455936fe7ca2498abbc2e26c841e
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
$ docker pull caddy@sha256:7fe86b8d0a4ab9cc95af609981d9cc4785288153254527b6ce37c9aae294c41b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17818318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647d08542df608b54d411f5170ded798422f492e7ca52d28335302b19ab8bb04`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:47:10 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 22:47:12 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 22:47:12 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 22:47:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 22:47:14 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 22:47:15 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 80
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 443
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 22:47:16 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 22:47:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d8802929e2d48f3cf4a528aefc7062f333f3187f4f49ddcbef8f085f8e8521`  
		Last Modified: Sat, 16 Mar 2024 22:49:52 GMT  
		Size: 355.0 KB (354951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe969db5b07e129eba5337dc67eab96b2be79254dab504472f04a8999fafc606`  
		Last Modified: Sat, 16 Mar 2024 22:49:52 GMT  
		Size: 7.5 KB (7527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47567cb4f626213c881a07becf3291a6a7f2590ed16ee927285be3725fc56c5a`  
		Last Modified: Sat, 16 Mar 2024 22:49:54 GMT  
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
$ docker pull caddy@sha256:95ce04978787e23e35143d23b8af2fbb6d6de55213b54a2e9ed2dbf8ffe7313c
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
$ docker pull caddy@sha256:7fe86b8d0a4ab9cc95af609981d9cc4785288153254527b6ce37c9aae294c41b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17818318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647d08542df608b54d411f5170ded798422f492e7ca52d28335302b19ab8bb04`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:47:10 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 22:47:12 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 22:47:12 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 22:47:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 22:47:14 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 22:47:15 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 80
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 443
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 22:47:16 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 22:47:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d8802929e2d48f3cf4a528aefc7062f333f3187f4f49ddcbef8f085f8e8521`  
		Last Modified: Sat, 16 Mar 2024 22:49:52 GMT  
		Size: 355.0 KB (354951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe969db5b07e129eba5337dc67eab96b2be79254dab504472f04a8999fafc606`  
		Last Modified: Sat, 16 Mar 2024 22:49:52 GMT  
		Size: 7.5 KB (7527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47567cb4f626213c881a07becf3291a6a7f2590ed16ee927285be3725fc56c5a`  
		Last Modified: Sat, 16 Mar 2024 22:49:54 GMT  
		Size: 14.2 MB (14238310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder`

```console
$ docker pull caddy@sha256:cc5f4cfd38d48b496b9d5e2a86a32243dd711af077e55dd18bca97ba3055c1d4
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
$ docker pull caddy@sha256:1b98f3fd892c1605c157cc3a049bded9d706ffd51d9a753e18ab07510d0d9e2a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76971330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e800cc7a9c84d26699931116102217b923104964e820bba39098ea1b544f5e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:41:31 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:41:31 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:41:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:41:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:41:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7862e08f4a3ed79ba32d02613b9c596dea827892605f23ebad6c4860ecfd1a4d`  
		Last Modified: Sat, 16 Mar 2024 08:03:57 GMT  
		Size: 284.7 KB (284695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df492c9dc93cdba9fed81e4389415b485127c9cb37c86b79b3f142702574a5a`  
		Last Modified: Wed, 03 Apr 2024 17:02:10 GMT  
		Size: 67.0 MB (67008211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7629e6793208752706519ae9acfbe8b7ad6bdd634d81a69dbcfed6930884369c`  
		Last Modified: Wed, 03 Apr 2024 17:02:00 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3317a43f465a5aebb363d397b3672606d18a5e247747ffd2684c1d0f74de0c6`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 5.0 MB (4973037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f015372e3250fa052df943aed69b26ce6d683b45328456139b9ab7ea453fdf`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 1.3 MB (1302233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6212759f5b367912c99a78b73d4277c50b224f19fe85ce2a3a9fbc94ed16be`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 405.0 B  
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
$ docker pull caddy@sha256:a31ab129389e3b3ac05560de4c52b0c6eada751beddf9acac3e8f35b9ef8c890
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64ab8f668dda6c40c8b5f34a24568989c2d59aa3868bca24a60d427bae87453`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:19:54 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:19:54 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:19:55 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:19:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:19:56 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:19:59 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:19:59 GMT
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
	-	`sha256:fef743b67b508d786f3e8c07ac7dca5aae6ea84a61aa62040b9488dcb2a61415`  
		Last Modified: Wed, 03 Apr 2024 17:04:20 GMT  
		Size: 65.8 MB (65766731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebfed2c271f130a93577b99cfaa3d4478590defaf383477153c1651a8e99a9`  
		Last Modified: Wed, 03 Apr 2024 17:04:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b09688e6219de2aeb2517b1fa78a0827e04df6051fd6bffe0eaec255bef97a`  
		Last Modified: Wed, 03 Apr 2024 17:20:22 GMT  
		Size: 4.5 MB (4514632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c14897ae7beed5a75683641e846e60b36c4ee61bdc37b9f469f54e1f4cf3fa`  
		Last Modified: Wed, 03 Apr 2024 17:20:21 GMT  
		Size: 1.2 MB (1246085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b24f949532888fed8d67d1c3b6a71965df7120dca4ae0931796d19ed24f9eb0`  
		Last Modified: Wed, 03 Apr 2024 17:20:21 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:9abc7c94f1374507e4fb3b81219f95268cd31f587383aa65ed562e3632f31ad3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73990594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53bd0a763baf79c779ab2df43b12f525bb58428beda8002ee1d684d7d6b97bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:17:39 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:17:39 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:17:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:17:41 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:17:41 GMT
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
	-	`sha256:d6de4b400683f0c2362cd880beab320a91316cc24f9f1ecbf576711db2be1bcd`  
		Last Modified: Wed, 03 Apr 2024 17:02:05 GMT  
		Size: 64.1 MB (64107935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cb2a7552d02e7b8e08bf29d0ad4ff98976de8d65f841ce2d42311feeefde4c`  
		Last Modified: Wed, 03 Apr 2024 17:00:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47f7261edc01476f5c0b0525e8f13cc9657f43606014d847afa574f072909ac`  
		Last Modified: Wed, 03 Apr 2024 17:17:57 GMT  
		Size: 5.1 MB (5063925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84aaf63ffe94c0dc9204c45df4cc7bb295e68028c5dc918d66c4b6a947a90783`  
		Last Modified: Wed, 03 Apr 2024 17:17:56 GMT  
		Size: 1.2 MB (1198447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c212b8dc9ff8e7943ac82424077aa3c9fa166ec6c2b15e1391120730607c83`  
		Last Modified: Wed, 03 Apr 2024 17:17:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:3a698c4439f62c22b347f40670cca759481b4368e86535ff7c8c90e26974a7b9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74222636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4c6495ce537716c6f5656c4b703e10cdc4908c76fee2d10efcde9ba1428bf2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:21:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:21:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:22:00 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:22:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:22:00 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:22:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:22:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:22:03 GMT
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
	-	`sha256:3dc9420a97e4b56d60b6f6e43e57c1a0d5699839dfc799b4251d0499da4fdd88`  
		Last Modified: Wed, 03 Apr 2024 17:06:19 GMT  
		Size: 64.1 MB (64129697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a95c9b8692b60f2d2834350493299931b57072a905e77764ab2a07c7be44b7`  
		Last Modified: Wed, 03 Apr 2024 17:06:07 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c79cba53bb3aec5e78f2aa326cb786811cad80519236a541f8cafc627e297c`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 5.3 MB (5270996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69323be82d9f1dfdc2a178ab91b6388fa9c05bec31f9f1df95e1e1429ca4a3c7`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3f305185cfe4c977fae095795eb511d3544f159d8622f4d8fc7b172edd3643`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; s390x

```console
$ docker pull caddy@sha256:71bc6c7a27089f10bb8fb6a701c2d6e2e1b1b097cc301c0d7e0537f1a97b550d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76102402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06da9a536513bc321f389c5c495c8f107c86b098d3db35fd0730f8a8de9d99d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 18:44:19 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 18:44:20 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 18:44:20 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 18:44:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 18:44:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 18:44:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 18:44:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 18:44:26 GMT
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
	-	`sha256:a9c0594d97c8cf4a046ce171a13f9a84a6bbb0b217f0694c3c2bd4d4e5b04be4`  
		Last Modified: Wed, 03 Apr 2024 17:30:50 GMT  
		Size: 66.2 MB (66219505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd26c37806dce963a4a27ef2b2db557bd73ac7834ed03be5caee0fb00f7fd04`  
		Last Modified: Wed, 03 Apr 2024 17:30:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab984370b902d79aea4a3b6f6836818ad0c6ea617bb48b1d51510bdafc407394`  
		Last Modified: Wed, 03 Apr 2024 18:46:09 GMT  
		Size: 5.1 MB (5117274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddb778247a116db89ac5778d4d4f54943f6cb5761fa79984dc7b1e230388caf`  
		Last Modified: Wed, 03 Apr 2024 18:46:08 GMT  
		Size: 1.3 MB (1262392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fa7a5ae42d88199c81c0faeb5c2cbdc5d23284280bf6fc75f5392621db3480`  
		Last Modified: Wed, 03 Apr 2024 18:46:08 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:217de50aa2da8ce751fcf86af874352c567fd2890a7af933d96b71b9cd686ab7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2054329601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5fca8b12e88afae211f90e44879d0eff32c2faddcf2f98239f84ff801975ab`
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
# Wed, 03 Apr 2024 17:11:09 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 17:13:34 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Apr 2024 17:13:36 GMT
WORKDIR C:\go
# Wed, 03 Apr 2024 17:46:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Apr 2024 17:46:15 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:46:16 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:46:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:46:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 03 Apr 2024 17:46:41 GMT
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
	-	`sha256:bba8f7ecb6aa5358813c663a8a821d1558f9fc231d3724d61963281d33c2e29d`  
		Last Modified: Wed, 03 Apr 2024 17:26:14 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645f42306e40e7cd27968b015e4ffd34928e43341ed0891a002a7038a0e92aad`  
		Last Modified: Wed, 03 Apr 2024 17:26:34 GMT  
		Size: 69.4 MB (69360591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b143f0a2277fa1d64dd7e4b237cdd6dee7b9588492e8f25e1f9a6f851ea84e3b`  
		Last Modified: Wed, 03 Apr 2024 17:26:14 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1547026bfff2e6197321109a9232c8d890758f34e98389383329811ca6d0cc2a`  
		Last Modified: Wed, 03 Apr 2024 17:47:34 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07757497ec2b71297a55c100a7253a5180839f418c47af25edff072294bba64`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3f141b6cc8b1b397eaca67bc234dff3e69a2a848385cd18a6f71f0e672d18c`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0988228d5bf035f168b753ec12db6dd4984f8758ac9c0c1ff3d92dabaa4ea452`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebf104fa97c496c43790a481b80954576c09380b483c4bef5fea5a1d017cab4`  
		Last Modified: Wed, 03 Apr 2024 17:47:33 GMT  
		Size: 1.7 MB (1666185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c7907d9819b9165f71f85f596a1a535a4857f3af02b44444b224cf8d588e38`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:8d209986e9cd0835be85e8f65905a45f09bbcf92d15c8d09fc474cfd921f042b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221960398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb43e28d9922862c630fec0d1ba1aa98980080ac6eee5431d9d200d7d373590`
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
# Wed, 03 Apr 2024 17:13:54 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 17:17:31 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Apr 2024 17:17:33 GMT
WORKDIR C:\go
# Wed, 03 Apr 2024 17:44:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Apr 2024 17:44:32 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:44:32 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:44:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:45:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 03 Apr 2024 17:45:58 GMT
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
	-	`sha256:584a26f47e4b040924987f5714e3904994464b2082794beebf1b84e0a4a711b3`  
		Last Modified: Wed, 03 Apr 2024 17:26:44 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e106baac3b372ef5b64f477236dcdd8c76bd7692c1d1a9a8c61596376a474f5e`  
		Last Modified: Wed, 03 Apr 2024 17:27:04 GMT  
		Size: 69.4 MB (69363419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e891eced875ee145e4fc5c147c8f84ff77215d4e5a1a86cff047c2697b417650`  
		Last Modified: Wed, 03 Apr 2024 17:26:44 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb621e6ec00bf92d79e37d3cb91e9ce4d633edce6c6618cbeeb19e40e482988`  
		Last Modified: Wed, 03 Apr 2024 17:47:18 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b816cd0d77c5e8e4f9e8e648b807ffb2e79e861b17670d9841ae2bf48852d2ba`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d0826717e8d6b364230bdd7ed7dd491d35a95be7323df3a90a68ded19a6ff5`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c00c4e7e6cf5e71b9dabdc9e7e221f5ce9450755ca1ad90c402e483f199ae8`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a2f091b6ab0aebf8b669a0f95d00a5b934be2ed7563f5bbf55986abe9d2efe`  
		Last Modified: Wed, 03 Apr 2024 17:47:17 GMT  
		Size: 1.7 MB (1666239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427e8173580c10665cb7ac17da9df0fdf012ced3b7aeb9262a86eced50bbb7c8`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder-alpine`

```console
$ docker pull caddy@sha256:721348b9c1549c1d715b571c48ca9764ad81bdf5f7ef34682b09856c300e1f56
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
$ docker pull caddy@sha256:1b98f3fd892c1605c157cc3a049bded9d706ffd51d9a753e18ab07510d0d9e2a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76971330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e800cc7a9c84d26699931116102217b923104964e820bba39098ea1b544f5e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:41:31 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:41:31 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:41:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:41:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:41:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7862e08f4a3ed79ba32d02613b9c596dea827892605f23ebad6c4860ecfd1a4d`  
		Last Modified: Sat, 16 Mar 2024 08:03:57 GMT  
		Size: 284.7 KB (284695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df492c9dc93cdba9fed81e4389415b485127c9cb37c86b79b3f142702574a5a`  
		Last Modified: Wed, 03 Apr 2024 17:02:10 GMT  
		Size: 67.0 MB (67008211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7629e6793208752706519ae9acfbe8b7ad6bdd634d81a69dbcfed6930884369c`  
		Last Modified: Wed, 03 Apr 2024 17:02:00 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3317a43f465a5aebb363d397b3672606d18a5e247747ffd2684c1d0f74de0c6`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 5.0 MB (4973037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f015372e3250fa052df943aed69b26ce6d683b45328456139b9ab7ea453fdf`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 1.3 MB (1302233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6212759f5b367912c99a78b73d4277c50b224f19fe85ce2a3a9fbc94ed16be`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 405.0 B  
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
$ docker pull caddy@sha256:a31ab129389e3b3ac05560de4c52b0c6eada751beddf9acac3e8f35b9ef8c890
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64ab8f668dda6c40c8b5f34a24568989c2d59aa3868bca24a60d427bae87453`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:19:54 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:19:54 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:19:55 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:19:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:19:56 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:19:59 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:19:59 GMT
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
	-	`sha256:fef743b67b508d786f3e8c07ac7dca5aae6ea84a61aa62040b9488dcb2a61415`  
		Last Modified: Wed, 03 Apr 2024 17:04:20 GMT  
		Size: 65.8 MB (65766731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebfed2c271f130a93577b99cfaa3d4478590defaf383477153c1651a8e99a9`  
		Last Modified: Wed, 03 Apr 2024 17:04:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b09688e6219de2aeb2517b1fa78a0827e04df6051fd6bffe0eaec255bef97a`  
		Last Modified: Wed, 03 Apr 2024 17:20:22 GMT  
		Size: 4.5 MB (4514632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c14897ae7beed5a75683641e846e60b36c4ee61bdc37b9f469f54e1f4cf3fa`  
		Last Modified: Wed, 03 Apr 2024 17:20:21 GMT  
		Size: 1.2 MB (1246085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b24f949532888fed8d67d1c3b6a71965df7120dca4ae0931796d19ed24f9eb0`  
		Last Modified: Wed, 03 Apr 2024 17:20:21 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:9abc7c94f1374507e4fb3b81219f95268cd31f587383aa65ed562e3632f31ad3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73990594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53bd0a763baf79c779ab2df43b12f525bb58428beda8002ee1d684d7d6b97bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:17:39 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:17:39 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:17:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:17:41 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:17:41 GMT
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
	-	`sha256:d6de4b400683f0c2362cd880beab320a91316cc24f9f1ecbf576711db2be1bcd`  
		Last Modified: Wed, 03 Apr 2024 17:02:05 GMT  
		Size: 64.1 MB (64107935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cb2a7552d02e7b8e08bf29d0ad4ff98976de8d65f841ce2d42311feeefde4c`  
		Last Modified: Wed, 03 Apr 2024 17:00:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47f7261edc01476f5c0b0525e8f13cc9657f43606014d847afa574f072909ac`  
		Last Modified: Wed, 03 Apr 2024 17:17:57 GMT  
		Size: 5.1 MB (5063925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84aaf63ffe94c0dc9204c45df4cc7bb295e68028c5dc918d66c4b6a947a90783`  
		Last Modified: Wed, 03 Apr 2024 17:17:56 GMT  
		Size: 1.2 MB (1198447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c212b8dc9ff8e7943ac82424077aa3c9fa166ec6c2b15e1391120730607c83`  
		Last Modified: Wed, 03 Apr 2024 17:17:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:3a698c4439f62c22b347f40670cca759481b4368e86535ff7c8c90e26974a7b9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74222636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4c6495ce537716c6f5656c4b703e10cdc4908c76fee2d10efcde9ba1428bf2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:21:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:21:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:22:00 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:22:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:22:00 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:22:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:22:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:22:03 GMT
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
	-	`sha256:3dc9420a97e4b56d60b6f6e43e57c1a0d5699839dfc799b4251d0499da4fdd88`  
		Last Modified: Wed, 03 Apr 2024 17:06:19 GMT  
		Size: 64.1 MB (64129697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a95c9b8692b60f2d2834350493299931b57072a905e77764ab2a07c7be44b7`  
		Last Modified: Wed, 03 Apr 2024 17:06:07 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c79cba53bb3aec5e78f2aa326cb786811cad80519236a541f8cafc627e297c`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 5.3 MB (5270996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69323be82d9f1dfdc2a178ab91b6388fa9c05bec31f9f1df95e1e1429ca4a3c7`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3f305185cfe4c977fae095795eb511d3544f159d8622f4d8fc7b172edd3643`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:71bc6c7a27089f10bb8fb6a701c2d6e2e1b1b097cc301c0d7e0537f1a97b550d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76102402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06da9a536513bc321f389c5c495c8f107c86b098d3db35fd0730f8a8de9d99d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 18:44:19 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 18:44:20 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 18:44:20 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 18:44:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 18:44:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 18:44:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 18:44:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 18:44:26 GMT
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
	-	`sha256:a9c0594d97c8cf4a046ce171a13f9a84a6bbb0b217f0694c3c2bd4d4e5b04be4`  
		Last Modified: Wed, 03 Apr 2024 17:30:50 GMT  
		Size: 66.2 MB (66219505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd26c37806dce963a4a27ef2b2db557bd73ac7834ed03be5caee0fb00f7fd04`  
		Last Modified: Wed, 03 Apr 2024 17:30:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab984370b902d79aea4a3b6f6836818ad0c6ea617bb48b1d51510bdafc407394`  
		Last Modified: Wed, 03 Apr 2024 18:46:09 GMT  
		Size: 5.1 MB (5117274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddb778247a116db89ac5778d4d4f54943f6cb5761fa79984dc7b1e230388caf`  
		Last Modified: Wed, 03 Apr 2024 18:46:08 GMT  
		Size: 1.3 MB (1262392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fa7a5ae42d88199c81c0faeb5c2cbdc5d23284280bf6fc75f5392621db3480`  
		Last Modified: Wed, 03 Apr 2024 18:46:08 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:65ffb8f02fbc79cbba4dbb361a8be92005f342bfc1892f7e98f08a843e194a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `caddy:2.7.6-builder-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:8d209986e9cd0835be85e8f65905a45f09bbcf92d15c8d09fc474cfd921f042b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221960398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb43e28d9922862c630fec0d1ba1aa98980080ac6eee5431d9d200d7d373590`
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
# Wed, 03 Apr 2024 17:13:54 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 17:17:31 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Apr 2024 17:17:33 GMT
WORKDIR C:\go
# Wed, 03 Apr 2024 17:44:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Apr 2024 17:44:32 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:44:32 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:44:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:45:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 03 Apr 2024 17:45:58 GMT
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
	-	`sha256:584a26f47e4b040924987f5714e3904994464b2082794beebf1b84e0a4a711b3`  
		Last Modified: Wed, 03 Apr 2024 17:26:44 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e106baac3b372ef5b64f477236dcdd8c76bd7692c1d1a9a8c61596376a474f5e`  
		Last Modified: Wed, 03 Apr 2024 17:27:04 GMT  
		Size: 69.4 MB (69363419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e891eced875ee145e4fc5c147c8f84ff77215d4e5a1a86cff047c2697b417650`  
		Last Modified: Wed, 03 Apr 2024 17:26:44 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb621e6ec00bf92d79e37d3cb91e9ce4d633edce6c6618cbeeb19e40e482988`  
		Last Modified: Wed, 03 Apr 2024 17:47:18 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b816cd0d77c5e8e4f9e8e648b807ffb2e79e861b17670d9841ae2bf48852d2ba`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d0826717e8d6b364230bdd7ed7dd491d35a95be7323df3a90a68ded19a6ff5`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c00c4e7e6cf5e71b9dabdc9e7e221f5ce9450755ca1ad90c402e483f199ae8`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a2f091b6ab0aebf8b669a0f95d00a5b934be2ed7563f5bbf55986abe9d2efe`  
		Last Modified: Wed, 03 Apr 2024 17:47:17 GMT  
		Size: 1.7 MB (1666239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427e8173580c10665cb7ac17da9df0fdf012ced3b7aeb9262a86eced50bbb7c8`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:64f0be6cf22b5b3c1d98a73d8d2e0ec0205594c9246accc32259bf88172be5f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `caddy:2.7.6-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:217de50aa2da8ce751fcf86af874352c567fd2890a7af933d96b71b9cd686ab7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2054329601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5fca8b12e88afae211f90e44879d0eff32c2faddcf2f98239f84ff801975ab`
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
# Wed, 03 Apr 2024 17:11:09 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 17:13:34 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Apr 2024 17:13:36 GMT
WORKDIR C:\go
# Wed, 03 Apr 2024 17:46:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Apr 2024 17:46:15 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:46:16 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:46:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:46:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 03 Apr 2024 17:46:41 GMT
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
	-	`sha256:bba8f7ecb6aa5358813c663a8a821d1558f9fc231d3724d61963281d33c2e29d`  
		Last Modified: Wed, 03 Apr 2024 17:26:14 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645f42306e40e7cd27968b015e4ffd34928e43341ed0891a002a7038a0e92aad`  
		Last Modified: Wed, 03 Apr 2024 17:26:34 GMT  
		Size: 69.4 MB (69360591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b143f0a2277fa1d64dd7e4b237cdd6dee7b9588492e8f25e1f9a6f851ea84e3b`  
		Last Modified: Wed, 03 Apr 2024 17:26:14 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1547026bfff2e6197321109a9232c8d890758f34e98389383329811ca6d0cc2a`  
		Last Modified: Wed, 03 Apr 2024 17:47:34 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07757497ec2b71297a55c100a7253a5180839f418c47af25edff072294bba64`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3f141b6cc8b1b397eaca67bc234dff3e69a2a848385cd18a6f71f0e672d18c`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0988228d5bf035f168b753ec12db6dd4984f8758ac9c0c1ff3d92dabaa4ea452`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebf104fa97c496c43790a481b80954576c09380b483c4bef5fea5a1d017cab4`  
		Last Modified: Wed, 03 Apr 2024 17:47:33 GMT  
		Size: 1.7 MB (1666185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c7907d9819b9165f71f85f596a1a535a4857f3af02b44444b224cf8d588e38`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1281 bytes)  
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
$ docker pull caddy@sha256:95ce04978787e23e35143d23b8af2fbb6d6de55213b54a2e9ed2dbf8ffe7313c
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
$ docker pull caddy@sha256:7fe86b8d0a4ab9cc95af609981d9cc4785288153254527b6ce37c9aae294c41b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17818318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647d08542df608b54d411f5170ded798422f492e7ca52d28335302b19ab8bb04`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:47:10 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 22:47:12 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 22:47:12 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 22:47:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 22:47:14 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 22:47:15 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 80
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 443
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 22:47:16 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 22:47:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d8802929e2d48f3cf4a528aefc7062f333f3187f4f49ddcbef8f085f8e8521`  
		Last Modified: Sat, 16 Mar 2024 22:49:52 GMT  
		Size: 355.0 KB (354951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe969db5b07e129eba5337dc67eab96b2be79254dab504472f04a8999fafc606`  
		Last Modified: Sat, 16 Mar 2024 22:49:52 GMT  
		Size: 7.5 KB (7527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47567cb4f626213c881a07becf3291a6a7f2590ed16ee927285be3725fc56c5a`  
		Last Modified: Sat, 16 Mar 2024 22:49:54 GMT  
		Size: 14.2 MB (14238310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder`

```console
$ docker pull caddy@sha256:cc5f4cfd38d48b496b9d5e2a86a32243dd711af077e55dd18bca97ba3055c1d4
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
$ docker pull caddy@sha256:1b98f3fd892c1605c157cc3a049bded9d706ffd51d9a753e18ab07510d0d9e2a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76971330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e800cc7a9c84d26699931116102217b923104964e820bba39098ea1b544f5e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:41:31 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:41:31 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:41:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:41:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:41:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7862e08f4a3ed79ba32d02613b9c596dea827892605f23ebad6c4860ecfd1a4d`  
		Last Modified: Sat, 16 Mar 2024 08:03:57 GMT  
		Size: 284.7 KB (284695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df492c9dc93cdba9fed81e4389415b485127c9cb37c86b79b3f142702574a5a`  
		Last Modified: Wed, 03 Apr 2024 17:02:10 GMT  
		Size: 67.0 MB (67008211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7629e6793208752706519ae9acfbe8b7ad6bdd634d81a69dbcfed6930884369c`  
		Last Modified: Wed, 03 Apr 2024 17:02:00 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3317a43f465a5aebb363d397b3672606d18a5e247747ffd2684c1d0f74de0c6`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 5.0 MB (4973037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f015372e3250fa052df943aed69b26ce6d683b45328456139b9ab7ea453fdf`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 1.3 MB (1302233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6212759f5b367912c99a78b73d4277c50b224f19fe85ce2a3a9fbc94ed16be`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 405.0 B  
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
$ docker pull caddy@sha256:a31ab129389e3b3ac05560de4c52b0c6eada751beddf9acac3e8f35b9ef8c890
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64ab8f668dda6c40c8b5f34a24568989c2d59aa3868bca24a60d427bae87453`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:19:54 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:19:54 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:19:55 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:19:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:19:56 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:19:59 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:19:59 GMT
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
	-	`sha256:fef743b67b508d786f3e8c07ac7dca5aae6ea84a61aa62040b9488dcb2a61415`  
		Last Modified: Wed, 03 Apr 2024 17:04:20 GMT  
		Size: 65.8 MB (65766731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebfed2c271f130a93577b99cfaa3d4478590defaf383477153c1651a8e99a9`  
		Last Modified: Wed, 03 Apr 2024 17:04:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b09688e6219de2aeb2517b1fa78a0827e04df6051fd6bffe0eaec255bef97a`  
		Last Modified: Wed, 03 Apr 2024 17:20:22 GMT  
		Size: 4.5 MB (4514632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c14897ae7beed5a75683641e846e60b36c4ee61bdc37b9f469f54e1f4cf3fa`  
		Last Modified: Wed, 03 Apr 2024 17:20:21 GMT  
		Size: 1.2 MB (1246085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b24f949532888fed8d67d1c3b6a71965df7120dca4ae0931796d19ed24f9eb0`  
		Last Modified: Wed, 03 Apr 2024 17:20:21 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:9abc7c94f1374507e4fb3b81219f95268cd31f587383aa65ed562e3632f31ad3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73990594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53bd0a763baf79c779ab2df43b12f525bb58428beda8002ee1d684d7d6b97bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:17:39 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:17:39 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:17:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:17:41 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:17:41 GMT
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
	-	`sha256:d6de4b400683f0c2362cd880beab320a91316cc24f9f1ecbf576711db2be1bcd`  
		Last Modified: Wed, 03 Apr 2024 17:02:05 GMT  
		Size: 64.1 MB (64107935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cb2a7552d02e7b8e08bf29d0ad4ff98976de8d65f841ce2d42311feeefde4c`  
		Last Modified: Wed, 03 Apr 2024 17:00:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47f7261edc01476f5c0b0525e8f13cc9657f43606014d847afa574f072909ac`  
		Last Modified: Wed, 03 Apr 2024 17:17:57 GMT  
		Size: 5.1 MB (5063925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84aaf63ffe94c0dc9204c45df4cc7bb295e68028c5dc918d66c4b6a947a90783`  
		Last Modified: Wed, 03 Apr 2024 17:17:56 GMT  
		Size: 1.2 MB (1198447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c212b8dc9ff8e7943ac82424077aa3c9fa166ec6c2b15e1391120730607c83`  
		Last Modified: Wed, 03 Apr 2024 17:17:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:3a698c4439f62c22b347f40670cca759481b4368e86535ff7c8c90e26974a7b9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74222636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4c6495ce537716c6f5656c4b703e10cdc4908c76fee2d10efcde9ba1428bf2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:21:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:21:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:22:00 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:22:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:22:00 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:22:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:22:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:22:03 GMT
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
	-	`sha256:3dc9420a97e4b56d60b6f6e43e57c1a0d5699839dfc799b4251d0499da4fdd88`  
		Last Modified: Wed, 03 Apr 2024 17:06:19 GMT  
		Size: 64.1 MB (64129697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a95c9b8692b60f2d2834350493299931b57072a905e77764ab2a07c7be44b7`  
		Last Modified: Wed, 03 Apr 2024 17:06:07 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c79cba53bb3aec5e78f2aa326cb786811cad80519236a541f8cafc627e297c`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 5.3 MB (5270996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69323be82d9f1dfdc2a178ab91b6388fa9c05bec31f9f1df95e1e1429ca4a3c7`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3f305185cfe4c977fae095795eb511d3544f159d8622f4d8fc7b172edd3643`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:71bc6c7a27089f10bb8fb6a701c2d6e2e1b1b097cc301c0d7e0537f1a97b550d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76102402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06da9a536513bc321f389c5c495c8f107c86b098d3db35fd0730f8a8de9d99d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 18:44:19 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 18:44:20 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 18:44:20 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 18:44:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 18:44:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 18:44:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 18:44:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 18:44:26 GMT
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
	-	`sha256:a9c0594d97c8cf4a046ce171a13f9a84a6bbb0b217f0694c3c2bd4d4e5b04be4`  
		Last Modified: Wed, 03 Apr 2024 17:30:50 GMT  
		Size: 66.2 MB (66219505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd26c37806dce963a4a27ef2b2db557bd73ac7834ed03be5caee0fb00f7fd04`  
		Last Modified: Wed, 03 Apr 2024 17:30:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab984370b902d79aea4a3b6f6836818ad0c6ea617bb48b1d51510bdafc407394`  
		Last Modified: Wed, 03 Apr 2024 18:46:09 GMT  
		Size: 5.1 MB (5117274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddb778247a116db89ac5778d4d4f54943f6cb5761fa79984dc7b1e230388caf`  
		Last Modified: Wed, 03 Apr 2024 18:46:08 GMT  
		Size: 1.3 MB (1262392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fa7a5ae42d88199c81c0faeb5c2cbdc5d23284280bf6fc75f5392621db3480`  
		Last Modified: Wed, 03 Apr 2024 18:46:08 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:217de50aa2da8ce751fcf86af874352c567fd2890a7af933d96b71b9cd686ab7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2054329601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5fca8b12e88afae211f90e44879d0eff32c2faddcf2f98239f84ff801975ab`
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
# Wed, 03 Apr 2024 17:11:09 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 17:13:34 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Apr 2024 17:13:36 GMT
WORKDIR C:\go
# Wed, 03 Apr 2024 17:46:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Apr 2024 17:46:15 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:46:16 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:46:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:46:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 03 Apr 2024 17:46:41 GMT
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
	-	`sha256:bba8f7ecb6aa5358813c663a8a821d1558f9fc231d3724d61963281d33c2e29d`  
		Last Modified: Wed, 03 Apr 2024 17:26:14 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645f42306e40e7cd27968b015e4ffd34928e43341ed0891a002a7038a0e92aad`  
		Last Modified: Wed, 03 Apr 2024 17:26:34 GMT  
		Size: 69.4 MB (69360591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b143f0a2277fa1d64dd7e4b237cdd6dee7b9588492e8f25e1f9a6f851ea84e3b`  
		Last Modified: Wed, 03 Apr 2024 17:26:14 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1547026bfff2e6197321109a9232c8d890758f34e98389383329811ca6d0cc2a`  
		Last Modified: Wed, 03 Apr 2024 17:47:34 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07757497ec2b71297a55c100a7253a5180839f418c47af25edff072294bba64`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3f141b6cc8b1b397eaca67bc234dff3e69a2a848385cd18a6f71f0e672d18c`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0988228d5bf035f168b753ec12db6dd4984f8758ac9c0c1ff3d92dabaa4ea452`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebf104fa97c496c43790a481b80954576c09380b483c4bef5fea5a1d017cab4`  
		Last Modified: Wed, 03 Apr 2024 17:47:33 GMT  
		Size: 1.7 MB (1666185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c7907d9819b9165f71f85f596a1a535a4857f3af02b44444b224cf8d588e38`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:8d209986e9cd0835be85e8f65905a45f09bbcf92d15c8d09fc474cfd921f042b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221960398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb43e28d9922862c630fec0d1ba1aa98980080ac6eee5431d9d200d7d373590`
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
# Wed, 03 Apr 2024 17:13:54 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 17:17:31 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Apr 2024 17:17:33 GMT
WORKDIR C:\go
# Wed, 03 Apr 2024 17:44:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Apr 2024 17:44:32 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:44:32 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:44:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:45:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 03 Apr 2024 17:45:58 GMT
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
	-	`sha256:584a26f47e4b040924987f5714e3904994464b2082794beebf1b84e0a4a711b3`  
		Last Modified: Wed, 03 Apr 2024 17:26:44 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e106baac3b372ef5b64f477236dcdd8c76bd7692c1d1a9a8c61596376a474f5e`  
		Last Modified: Wed, 03 Apr 2024 17:27:04 GMT  
		Size: 69.4 MB (69363419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e891eced875ee145e4fc5c147c8f84ff77215d4e5a1a86cff047c2697b417650`  
		Last Modified: Wed, 03 Apr 2024 17:26:44 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb621e6ec00bf92d79e37d3cb91e9ce4d633edce6c6618cbeeb19e40e482988`  
		Last Modified: Wed, 03 Apr 2024 17:47:18 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b816cd0d77c5e8e4f9e8e648b807ffb2e79e861b17670d9841ae2bf48852d2ba`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d0826717e8d6b364230bdd7ed7dd491d35a95be7323df3a90a68ded19a6ff5`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c00c4e7e6cf5e71b9dabdc9e7e221f5ce9450755ca1ad90c402e483f199ae8`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a2f091b6ab0aebf8b669a0f95d00a5b934be2ed7563f5bbf55986abe9d2efe`  
		Last Modified: Wed, 03 Apr 2024 17:47:17 GMT  
		Size: 1.7 MB (1666239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427e8173580c10665cb7ac17da9df0fdf012ced3b7aeb9262a86eced50bbb7c8`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:721348b9c1549c1d715b571c48ca9764ad81bdf5f7ef34682b09856c300e1f56
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
$ docker pull caddy@sha256:1b98f3fd892c1605c157cc3a049bded9d706ffd51d9a753e18ab07510d0d9e2a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76971330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e800cc7a9c84d26699931116102217b923104964e820bba39098ea1b544f5e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:41:31 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:41:31 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:41:31 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:41:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:41:33 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:41:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7862e08f4a3ed79ba32d02613b9c596dea827892605f23ebad6c4860ecfd1a4d`  
		Last Modified: Sat, 16 Mar 2024 08:03:57 GMT  
		Size: 284.7 KB (284695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df492c9dc93cdba9fed81e4389415b485127c9cb37c86b79b3f142702574a5a`  
		Last Modified: Wed, 03 Apr 2024 17:02:10 GMT  
		Size: 67.0 MB (67008211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7629e6793208752706519ae9acfbe8b7ad6bdd634d81a69dbcfed6930884369c`  
		Last Modified: Wed, 03 Apr 2024 17:02:00 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3317a43f465a5aebb363d397b3672606d18a5e247747ffd2684c1d0f74de0c6`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 5.0 MB (4973037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f015372e3250fa052df943aed69b26ce6d683b45328456139b9ab7ea453fdf`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 1.3 MB (1302233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6212759f5b367912c99a78b73d4277c50b224f19fe85ce2a3a9fbc94ed16be`  
		Last Modified: Wed, 03 Apr 2024 17:41:49 GMT  
		Size: 405.0 B  
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
$ docker pull caddy@sha256:a31ab129389e3b3ac05560de4c52b0c6eada751beddf9acac3e8f35b9ef8c890
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64ab8f668dda6c40c8b5f34a24568989c2d59aa3868bca24a60d427bae87453`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:19:54 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:19:54 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:19:55 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:19:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:19:56 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:19:59 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:19:59 GMT
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
	-	`sha256:fef743b67b508d786f3e8c07ac7dca5aae6ea84a61aa62040b9488dcb2a61415`  
		Last Modified: Wed, 03 Apr 2024 17:04:20 GMT  
		Size: 65.8 MB (65766731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ebfed2c271f130a93577b99cfaa3d4478590defaf383477153c1651a8e99a9`  
		Last Modified: Wed, 03 Apr 2024 17:04:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b09688e6219de2aeb2517b1fa78a0827e04df6051fd6bffe0eaec255bef97a`  
		Last Modified: Wed, 03 Apr 2024 17:20:22 GMT  
		Size: 4.5 MB (4514632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c14897ae7beed5a75683641e846e60b36c4ee61bdc37b9f469f54e1f4cf3fa`  
		Last Modified: Wed, 03 Apr 2024 17:20:21 GMT  
		Size: 1.2 MB (1246085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b24f949532888fed8d67d1c3b6a71965df7120dca4ae0931796d19ed24f9eb0`  
		Last Modified: Wed, 03 Apr 2024 17:20:21 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:9abc7c94f1374507e4fb3b81219f95268cd31f587383aa65ed562e3632f31ad3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73990594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53bd0a763baf79c779ab2df43b12f525bb58428beda8002ee1d684d7d6b97bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:17:39 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:17:39 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:17:39 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:17:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:17:41 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:17:41 GMT
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
	-	`sha256:d6de4b400683f0c2362cd880beab320a91316cc24f9f1ecbf576711db2be1bcd`  
		Last Modified: Wed, 03 Apr 2024 17:02:05 GMT  
		Size: 64.1 MB (64107935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cb2a7552d02e7b8e08bf29d0ad4ff98976de8d65f841ce2d42311feeefde4c`  
		Last Modified: Wed, 03 Apr 2024 17:00:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47f7261edc01476f5c0b0525e8f13cc9657f43606014d847afa574f072909ac`  
		Last Modified: Wed, 03 Apr 2024 17:17:57 GMT  
		Size: 5.1 MB (5063925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84aaf63ffe94c0dc9204c45df4cc7bb295e68028c5dc918d66c4b6a947a90783`  
		Last Modified: Wed, 03 Apr 2024 17:17:56 GMT  
		Size: 1.2 MB (1198447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c212b8dc9ff8e7943ac82424077aa3c9fa166ec6c2b15e1391120730607c83`  
		Last Modified: Wed, 03 Apr 2024 17:17:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:3a698c4439f62c22b347f40670cca759481b4368e86535ff7c8c90e26974a7b9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74222636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4c6495ce537716c6f5656c4b703e10cdc4908c76fee2d10efcde9ba1428bf2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 17:21:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 17:21:59 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:22:00 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:22:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:22:00 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 17:22:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 17:22:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 17:22:03 GMT
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
	-	`sha256:3dc9420a97e4b56d60b6f6e43e57c1a0d5699839dfc799b4251d0499da4fdd88`  
		Last Modified: Wed, 03 Apr 2024 17:06:19 GMT  
		Size: 64.1 MB (64129697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a95c9b8692b60f2d2834350493299931b57072a905e77764ab2a07c7be44b7`  
		Last Modified: Wed, 03 Apr 2024 17:06:07 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c79cba53bb3aec5e78f2aa326cb786811cad80519236a541f8cafc627e297c`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 5.3 MB (5270996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69323be82d9f1dfdc2a178ab91b6388fa9c05bec31f9f1df95e1e1429ca4a3c7`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3f305185cfe4c977fae095795eb511d3544f159d8622f4d8fc7b172edd3643`  
		Last Modified: Wed, 03 Apr 2024 17:22:19 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:71bc6c7a27089f10bb8fb6a701c2d6e2e1b1b097cc301c0d7e0537f1a97b550d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76102402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06da9a536513bc321f389c5c495c8f107c86b098d3db35fd0730f8a8de9d99d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Wed, 03 Apr 2024 15:58:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Apr 2024 15:58:57 GMT
ENV GOPATH=/go
# Wed, 03 Apr 2024 15:58:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Apr 2024 15:58:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Apr 2024 15:58:57 GMT
WORKDIR /go
# Wed, 03 Apr 2024 18:44:19 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 18:44:20 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 18:44:20 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 18:44:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 18:44:21 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 18:44:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 18:44:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 18:44:26 GMT
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
	-	`sha256:a9c0594d97c8cf4a046ce171a13f9a84a6bbb0b217f0694c3c2bd4d4e5b04be4`  
		Last Modified: Wed, 03 Apr 2024 17:30:50 GMT  
		Size: 66.2 MB (66219505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd26c37806dce963a4a27ef2b2db557bd73ac7834ed03be5caee0fb00f7fd04`  
		Last Modified: Wed, 03 Apr 2024 17:30:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab984370b902d79aea4a3b6f6836818ad0c6ea617bb48b1d51510bdafc407394`  
		Last Modified: Wed, 03 Apr 2024 18:46:09 GMT  
		Size: 5.1 MB (5117274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddb778247a116db89ac5778d4d4f54943f6cb5761fa79984dc7b1e230388caf`  
		Last Modified: Wed, 03 Apr 2024 18:46:08 GMT  
		Size: 1.3 MB (1262392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fa7a5ae42d88199c81c0faeb5c2cbdc5d23284280bf6fc75f5392621db3480`  
		Last Modified: Wed, 03 Apr 2024 18:46:08 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:65ffb8f02fbc79cbba4dbb361a8be92005f342bfc1892f7e98f08a843e194a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:8d209986e9cd0835be85e8f65905a45f09bbcf92d15c8d09fc474cfd921f042b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221960398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb43e28d9922862c630fec0d1ba1aa98980080ac6eee5431d9d200d7d373590`
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
# Wed, 03 Apr 2024 17:13:54 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 17:17:31 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Apr 2024 17:17:33 GMT
WORKDIR C:\go
# Wed, 03 Apr 2024 17:44:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Apr 2024 17:44:32 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:44:32 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:44:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:45:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 03 Apr 2024 17:45:58 GMT
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
	-	`sha256:584a26f47e4b040924987f5714e3904994464b2082794beebf1b84e0a4a711b3`  
		Last Modified: Wed, 03 Apr 2024 17:26:44 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e106baac3b372ef5b64f477236dcdd8c76bd7692c1d1a9a8c61596376a474f5e`  
		Last Modified: Wed, 03 Apr 2024 17:27:04 GMT  
		Size: 69.4 MB (69363419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e891eced875ee145e4fc5c147c8f84ff77215d4e5a1a86cff047c2697b417650`  
		Last Modified: Wed, 03 Apr 2024 17:26:44 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb621e6ec00bf92d79e37d3cb91e9ce4d633edce6c6618cbeeb19e40e482988`  
		Last Modified: Wed, 03 Apr 2024 17:47:18 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b816cd0d77c5e8e4f9e8e648b807ffb2e79e861b17670d9841ae2bf48852d2ba`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d0826717e8d6b364230bdd7ed7dd491d35a95be7323df3a90a68ded19a6ff5`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c00c4e7e6cf5e71b9dabdc9e7e221f5ce9450755ca1ad90c402e483f199ae8`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a2f091b6ab0aebf8b669a0f95d00a5b934be2ed7563f5bbf55986abe9d2efe`  
		Last Modified: Wed, 03 Apr 2024 17:47:17 GMT  
		Size: 1.7 MB (1666239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427e8173580c10665cb7ac17da9df0fdf012ced3b7aeb9262a86eced50bbb7c8`  
		Last Modified: Wed, 03 Apr 2024 17:47:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:64f0be6cf22b5b3c1d98a73d8d2e0ec0205594c9246accc32259bf88172be5f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:217de50aa2da8ce751fcf86af874352c567fd2890a7af933d96b71b9cd686ab7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2054329601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5fca8b12e88afae211f90e44879d0eff32c2faddcf2f98239f84ff801975ab`
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
# Wed, 03 Apr 2024 17:11:09 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 03 Apr 2024 17:13:34 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Apr 2024 17:13:36 GMT
WORKDIR C:\go
# Wed, 03 Apr 2024 17:46:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Apr 2024 17:46:15 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 17:46:16 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 17:46:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 17:46:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 03 Apr 2024 17:46:41 GMT
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
	-	`sha256:bba8f7ecb6aa5358813c663a8a821d1558f9fc231d3724d61963281d33c2e29d`  
		Last Modified: Wed, 03 Apr 2024 17:26:14 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645f42306e40e7cd27968b015e4ffd34928e43341ed0891a002a7038a0e92aad`  
		Last Modified: Wed, 03 Apr 2024 17:26:34 GMT  
		Size: 69.4 MB (69360591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b143f0a2277fa1d64dd7e4b237cdd6dee7b9588492e8f25e1f9a6f851ea84e3b`  
		Last Modified: Wed, 03 Apr 2024 17:26:14 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1547026bfff2e6197321109a9232c8d890758f34e98389383329811ca6d0cc2a`  
		Last Modified: Wed, 03 Apr 2024 17:47:34 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07757497ec2b71297a55c100a7253a5180839f418c47af25edff072294bba64`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3f141b6cc8b1b397eaca67bc234dff3e69a2a848385cd18a6f71f0e672d18c`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0988228d5bf035f168b753ec12db6dd4984f8758ac9c0c1ff3d92dabaa4ea452`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebf104fa97c496c43790a481b80954576c09380b483c4bef5fea5a1d017cab4`  
		Last Modified: Wed, 03 Apr 2024 17:47:33 GMT  
		Size: 1.7 MB (1666185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c7907d9819b9165f71f85f596a1a535a4857f3af02b44444b224cf8d588e38`  
		Last Modified: Wed, 03 Apr 2024 17:47:32 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:d8d3637a26f50bf0bd27a6151d2bd4f7a9f0455936fe7ca2498abbc2e26c841e
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
$ docker pull caddy@sha256:7fe86b8d0a4ab9cc95af609981d9cc4785288153254527b6ce37c9aae294c41b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17818318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647d08542df608b54d411f5170ded798422f492e7ca52d28335302b19ab8bb04`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:47:10 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 16 Mar 2024 22:47:12 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 16 Mar 2024 22:47:12 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 16 Mar 2024 22:47:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 16 Mar 2024 22:47:14 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 16 Mar 2024 22:47:15 GMT
ENV XDG_DATA_HOME=/data
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Mar 2024 22:47:15 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 80
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 443
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 443/udp
# Sat, 16 Mar 2024 22:47:16 GMT
EXPOSE 2019
# Sat, 16 Mar 2024 22:47:16 GMT
WORKDIR /srv
# Sat, 16 Mar 2024 22:47:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d8802929e2d48f3cf4a528aefc7062f333f3187f4f49ddcbef8f085f8e8521`  
		Last Modified: Sat, 16 Mar 2024 22:49:52 GMT  
		Size: 355.0 KB (354951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe969db5b07e129eba5337dc67eab96b2be79254dab504472f04a8999fafc606`  
		Last Modified: Sat, 16 Mar 2024 22:49:52 GMT  
		Size: 7.5 KB (7527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47567cb4f626213c881a07becf3291a6a7f2590ed16ee927285be3725fc56c5a`  
		Last Modified: Sat, 16 Mar 2024 22:49:54 GMT  
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
