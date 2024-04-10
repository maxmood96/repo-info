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
$ docker pull caddy@sha256:ca031cd33c788ebe467c94348400e5bf263178f9619f3993af8373f18681b8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

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

### `caddy:2` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:b4de45abdf801e6fe4e627d4a9146c7f3822666f9795f1fe35921da33d3b5920
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2015415021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1c537b274bb6928ea6772a745ddf910765f287696f3d596a64a2aef5bb3a49`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:59:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:59:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:00:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 02:00:12 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 02:00:13 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 02:00:13 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 02:00:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 02:00:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 02:00:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 02:00:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 02:00:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 02:00:20 GMT
EXPOSE 80
# Wed, 10 Apr 2024 02:00:21 GMT
EXPOSE 443
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 02:00:42 GMT
RUN caddy version
# Wed, 10 Apr 2024 02:00:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9cb628e4a7ceb9e124a728aba733c7b7837d0fe602c1af1c86af5ba7db1afe`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 462.4 KB (462386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe6244a1b7fd00d56255f78e7951d14811b06f10e069d90e75458e8f5198d6a`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fd5220e89ae5a44a14c920f948c28b3238c83307ad30f5955882930d72a23b`  
		Last Modified: Wed, 10 Apr 2024 04:39:56 GMT  
		Size: 15.3 MB (15272884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8711ac4c34fb1beb0cb9e799010a337864f252ea20a91c74e9ffb9dc4dd8f4`  
		Last Modified: Wed, 10 Apr 2024 04:39:52 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1bffa02c717094b56095d1f166aa11c19ba43f7481d7673313c862126f3434`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e554dc514103b8d140d5ab4e9437abe3875ce416cd9a69161836f9676d14b650`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f583dd206e697664bb89b8647ac1fe5d98933b1d6540b249433dae65d02dd09`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35fa3d4abc62509fa7c8c8b31d11482d23090a1f7e45393d43cbde05d0cd7e9`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254f688302923c46000c0526a060b43160db4d9314cbd342a3fc31620052ceaa`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e052187f5af8dbfaa36325485d886d7d47bbe36c18a5789d95efea81dfbf12`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea08dd4e4a398c33acb70cc8863ba300fad5cbf499840ed420b14ce06717f83`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc50e94c9c5e82f27b76ddd1796de52ee67ba64c275a531ee0d38c08757baf9e`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af1603a6bd4dacbf08b4c974a5db996c73e892cbe440e2d5339aa355847e5a0`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaaeba50589b199d8e988596dada19daaec59e8b26f7835e17a29fff8ac88f7`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b4695f6c339c5917ad1b57b3db1345b8cc1ac6b4e03d56d5f1de12f8e249a2`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d5e030bf8b034231beb875dd3a70af4fcf82b6350b60b23a72cef369792a29`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9280f84d3173ce915aa30f755697f993ca2d484caa9f8cd42334927563008d`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e2de6ed998eca032f334174172a69a2345072eda08fddd105b73a6e6238c81`  
		Last Modified: Wed, 10 Apr 2024 04:39:47 GMT  
		Size: 282.0 KB (282045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426ed15821e9616ced2fee524860d8e5554c359d0332601d4e035474c8a54964`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:650f5144a6e8b1d947f54c017a1002956e096891718dc7edf9aa8661be3f82ce
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2180450650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e356a94cf89f9d5eb0399e9f2ae7bbba82bc08e09f5dbc1d964352dfa2497f34`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:55:53 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:55:54 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 01:57:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 01:57:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 01:57:26 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 01:57:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 01:57:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 01:57:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 01:57:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 01:57:33 GMT
EXPOSE 80
# Wed, 10 Apr 2024 01:57:34 GMT
EXPOSE 443
# Wed, 10 Apr 2024 01:57:35 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 01:57:36 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 01:58:56 GMT
RUN caddy version
# Wed, 10 Apr 2024 01:58:57 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218ffc757feed37e26b36ff35084f4357219272c3ef8ce663a0db97763750bec`  
		Last Modified: Wed, 10 Apr 2024 04:39:29 GMT  
		Size: 465.0 KB (465007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f41e339dc34abe966a19ca999fece15bcf0a5e9eb2d36d4d42b84482e8e2ba`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac8e68361bdc1deb2d5d4e50f2da825b25f026f558a03aeeba18d6c7665e654`  
		Last Modified: Wed, 10 Apr 2024 04:39:32 GMT  
		Size: 15.3 MB (15281747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05561518ae50169e6e15468669f8195d9b2ee80d945dd94c107d20afda067318`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0720408b82b77dc7b0d925d39741de50fe2f9139768729af189a0f783b43519b`  
		Last Modified: Wed, 10 Apr 2024 04:39:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d8585bb3ff3b6a72b43181fc6df1c46ce88f6393295f32d2315e71c85e7295`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177da9a277ef013596e849aa2ea825a25dddcec2db12d81c6a4ab6fa02e77e57`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4686dffa2d26bcedea0a3b07e3d11640141e4a3888ddca8fc167fce49a67e102`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7411e6d276896da1fd4087fb7dbbe4e2169637862d1bee25144443263947ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966957575920790399f90fd33923b9cb27715dc7dd38e430480922326f86e953`  
		Last Modified: Wed, 10 Apr 2024 04:39:25 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa479db7e2e01c3cdda82927bbd2250f6933c5e4f6d67f09b4f090c26df209ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173767522133c716cc5b0c32c5c8778faa06e95a3933bab867e4569bb468420`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a488b5ddbaaac25b5ac6ce9375b9c9eb44e109874b5cd47d7f6591a446084bb`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27825614feb810c19f64b918a625f414d9f32098460aefcc9dad624bd2be669`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcc1e73eb545e48d76e61fd1029ab3a682c27085f1b3d23b2e7be300cd8eca8`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2713b7318664d7438093b75892a477ec691872f2c8fb13408d4d27d9bddd9`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce420a03b259096e6668f2765ce31ad5694523c86afe5c81bc0277d8b2bc861`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7baa1c6f084d5ad95cabb52b0d9aaed5e906928249958cb374cf25fe5e51e921`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 253.5 KB (253500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d599502ec7d608e46d6398aebafdee3aea525c5a3a58d826220dd06d128bb939`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.4 KB (1419 bytes)  
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
$ docker pull caddy@sha256:d8a2ad006009b25b7017ab7190128cdd3a0fccee518f5b14fe6c749c6a6293b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

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
$ docker pull caddy@sha256:a925804363a91c2468468c2ab1c1de2c770fe02812a21b1bdc1e9d8d65a5241b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75406613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acc712a703abf58b426c0681a4f724105efc534e813fca8d7e1769f2df5ebfe`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
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
# Wed, 03 Apr 2024 20:22:32 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 20:22:32 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 20:22:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 20:22:34 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 20:22:34 GMT
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
	-	`sha256:d72bd013141c752021b5b309e9868c02341e86fc25f37a89ccec1311ad14b2fd`  
		Last Modified: Wed, 03 Apr 2024 17:01:10 GMT  
		Size: 65.8 MB (65766638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abea289abae69e0933683886761310d242609c9941f5964366d9fb5bae890969`  
		Last Modified: Wed, 03 Apr 2024 17:00:57 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c466f5631c550594140cdcbad1c11c2549f51578de8dbf2181ab68d36e3860`  
		Last Modified: Wed, 03 Apr 2024 20:22:50 GMT  
		Size: 5.0 MB (4958760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c206e1c4695681bec33b38b6cb25bc40da76dd756937418fda1f1841f07a6b`  
		Last Modified: Wed, 03 Apr 2024 20:22:49 GMT  
		Size: 1.2 MB (1248664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1617709771cc71f393f3e93e93292a3024d9ec67376e73101934b6f2d2a14c`  
		Last Modified: Wed, 03 Apr 2024 20:22:48 GMT  
		Size: 406.0 B  
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

### `caddy:2-builder` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:dd65119faf3e9848dfe903b2d36c44473682ef85d053853873e864f46e68a3f7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2096172662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf83f7bc549933a30beb62be150c320ee6ee873beb730199fe7c91d066d7b9cc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:06:58 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Apr 2024 01:06:59 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Apr 2024 01:06:59 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Apr 2024 01:07:00 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Apr 2024 01:07:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:07:38 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:07:59 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 01:22:55 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 10 Apr 2024 01:25:11 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:25:13 GMT
WORKDIR C:\go
# Wed, 10 Apr 2024 02:02:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 02:02:41 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 10 Apr 2024 02:02:42 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:02:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Apr 2024 02:03:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Apr 2024 02:03:12 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5ca144c62db12ea36d3f00f6640c6e4758e616b730c3d993fb57c3c8ebad9`  
		Last Modified: Wed, 10 Apr 2024 01:34:50 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d031792c46321e7a0a81f081515ffa50d7c86201a35780d03b0a1a0ecd68ebac`  
		Last Modified: Wed, 10 Apr 2024 01:34:49 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91b14b8df5887a0feab0adbfcf0dea95d1aab9c3e32619bf6ec5bdc4971a9a4`  
		Last Modified: Wed, 10 Apr 2024 01:34:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099fb3ff689379a9da8dc64f6c1c8d941fb9f0cf66715dc1af16055bdb8e63ec`  
		Last Modified: Wed, 10 Apr 2024 01:34:48 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ca11c05a0028bb84d4b2b76249dfcce87ea1f22340e50e79681c2055ee1d27`  
		Last Modified: Wed, 10 Apr 2024 01:34:54 GMT  
		Size: 25.5 MB (25528844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587f661259fd2478a26bea01012713bd3afd154dfc37f4aafd87ca98d67f75b7`  
		Last Modified: Wed, 10 Apr 2024 01:34:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5830a087830d60f2ed8f1cf87fba9d92cdf7706d61f7692f8aada1a5aec889e8`  
		Last Modified: Wed, 10 Apr 2024 01:34:47 GMT  
		Size: 255.6 KB (255649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5ba249752b259ec30317e6d9be24c9ae184897a3f96774f0a1f61fa6f8c196`  
		Last Modified: Wed, 10 Apr 2024 01:36:59 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc595e8d9ffdc13e2a491f83d29bbcf6e4fbbc1872cdf9b6d33156900f593be`  
		Last Modified: Wed, 10 Apr 2024 01:37:20 GMT  
		Size: 69.3 MB (69339784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9666572ffef44cedd89a1bf02be297824dcbb0e1db30b6f9a52cf06b09d181a0`  
		Last Modified: Wed, 10 Apr 2024 01:36:59 GMT  
		Size: 1.6 KB (1566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474f61eee778c75a6072d92f90f33cb8c3ba21ea0eded3d3a82ff35a91a50864`  
		Last Modified: Wed, 10 Apr 2024 04:40:31 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2f4771e42fee7692dd61c00fd5b5d18d7d8130854ee6dd737e581fc1ed2763`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86a9ad5c8f8b619270cd40a575f612322b7315fdf2105e6397a45d3707de156`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b4a4ffb9e9f9938b9bd40929d0422b0b5c111eba84c460246a970170261047`  
		Last Modified: Wed, 10 Apr 2024 04:40:28 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328e4a9a7a4cffe0480ebc46c068396be1a07000e05c24701ee9f2adf7e13cd3`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.7 MB (1656674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222acab8b494945e613aea2cd196dcf87a6f607c426f4d8a77b721a5c3ccb00b`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:390a1ca91ca1409e1ddd37368179b927e08a5076b250132ee200be24319015bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261258422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc64e898993fdebf28e22269619414d6e7fed095f21d000c00b8d70339b915b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:10:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Apr 2024 01:10:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Apr 2024 01:10:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Apr 2024 01:10:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Apr 2024 01:12:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:12:15 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:13:36 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 01:25:25 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 10 Apr 2024 01:29:01 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:29:02 GMT
WORKDIR C:\go
# Wed, 10 Apr 2024 02:00:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 02:00:57 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 10 Apr 2024 02:00:58 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:00:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Apr 2024 02:02:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Apr 2024 02:02:33 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843b97b1625fa02e123dfc05bebcf9f05077e6dbdd1f5253c3c6d07b95f0f55f`  
		Last Modified: Wed, 10 Apr 2024 01:35:25 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6532f7333203cbc41355f91a4431427f575a24ad3dc3dd393b4292b4c2660d76`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c34d692c7e9d5e97e4674c9fefa41e1c78447d2e9c8db3a3f94f325b6188af`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cead4e65b4492e37b01dc6043de135f9dfad18c9f01232c605eb59e7da4a98`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7638380d4eb3933d8241dfe83deaffc516e8bed7b2ab01f96b42864a0d722760`  
		Last Modified: Wed, 10 Apr 2024 01:35:27 GMT  
		Size: 25.5 MB (25535896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159dd7a1de12391b28b5260b6132a515d19e87a7e18b64d7bc843df2c26fb615`  
		Last Modified: Wed, 10 Apr 2024 01:35:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3004df08705794a49d57aabf8c97ae8dfe750cedd45eb476bd574ce29807e152`  
		Last Modified: Wed, 10 Apr 2024 01:35:21 GMT  
		Size: 263.3 KB (263307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4eb7e47773f01051ff8bed6e1e75760df109971229c7a276fc7299c77e1444`  
		Last Modified: Wed, 10 Apr 2024 01:37:33 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe828248e339ed1213f1728c3774b3fcbe81883eb47c39a77bded1d31b619866`  
		Last Modified: Wed, 10 Apr 2024 01:37:53 GMT  
		Size: 69.4 MB (69351371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0187d4b9bc619f6e5b9b6b4b45022d6f5f885398842d5e7b19103f3eff6d5d7d`  
		Last Modified: Wed, 10 Apr 2024 01:37:33 GMT  
		Size: 1.5 KB (1546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6320d39f2704b0c1762e0721121d0880c199f6dfe049f437c31318022f8d00d2`  
		Last Modified: Wed, 10 Apr 2024 04:40:13 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305f4502d0cf4a9a57015ac8a097d5f6636708172c5a249cdf37f4b7b5c2dfe2`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45625e4d8a700993f0fb347856d0df08e31374fca8b1a737332323ff07cf8ca`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb3362bfb653595714774c2d1cce61d5a02893675414b7d23b462602a727f20`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db153c0587fdf29cfded01b1cd48082057e376ad8636a6a254d3cc5d030775ca`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.7 MB (1661731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c45da18daa8ebd71fd796480f9850e0e1df9ce87467e733d09a937d867e369`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:481c3357e533d892e2621d69ce3747a459e40af2f56159bcbd64b38bee1aa5bd
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
$ docker pull caddy@sha256:a925804363a91c2468468c2ab1c1de2c770fe02812a21b1bdc1e9d8d65a5241b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75406613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acc712a703abf58b426c0681a4f724105efc534e813fca8d7e1769f2df5ebfe`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
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
# Wed, 03 Apr 2024 20:22:32 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 20:22:32 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 20:22:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 20:22:34 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 20:22:34 GMT
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
	-	`sha256:d72bd013141c752021b5b309e9868c02341e86fc25f37a89ccec1311ad14b2fd`  
		Last Modified: Wed, 03 Apr 2024 17:01:10 GMT  
		Size: 65.8 MB (65766638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abea289abae69e0933683886761310d242609c9941f5964366d9fb5bae890969`  
		Last Modified: Wed, 03 Apr 2024 17:00:57 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c466f5631c550594140cdcbad1c11c2549f51578de8dbf2181ab68d36e3860`  
		Last Modified: Wed, 03 Apr 2024 20:22:50 GMT  
		Size: 5.0 MB (4958760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c206e1c4695681bec33b38b6cb25bc40da76dd756937418fda1f1841f07a6b`  
		Last Modified: Wed, 03 Apr 2024 20:22:49 GMT  
		Size: 1.2 MB (1248664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1617709771cc71f393f3e93e93292a3024d9ec67376e73101934b6f2d2a14c`  
		Last Modified: Wed, 03 Apr 2024 20:22:48 GMT  
		Size: 406.0 B  
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
$ docker pull caddy@sha256:737e66da3299a8c95988bbf4d40a3c4598cca4f803e9a27e3a7bd8fa63b109c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:390a1ca91ca1409e1ddd37368179b927e08a5076b250132ee200be24319015bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261258422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc64e898993fdebf28e22269619414d6e7fed095f21d000c00b8d70339b915b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:10:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Apr 2024 01:10:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Apr 2024 01:10:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Apr 2024 01:10:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Apr 2024 01:12:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:12:15 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:13:36 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 01:25:25 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 10 Apr 2024 01:29:01 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:29:02 GMT
WORKDIR C:\go
# Wed, 10 Apr 2024 02:00:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 02:00:57 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 10 Apr 2024 02:00:58 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:00:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Apr 2024 02:02:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Apr 2024 02:02:33 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843b97b1625fa02e123dfc05bebcf9f05077e6dbdd1f5253c3c6d07b95f0f55f`  
		Last Modified: Wed, 10 Apr 2024 01:35:25 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6532f7333203cbc41355f91a4431427f575a24ad3dc3dd393b4292b4c2660d76`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c34d692c7e9d5e97e4674c9fefa41e1c78447d2e9c8db3a3f94f325b6188af`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cead4e65b4492e37b01dc6043de135f9dfad18c9f01232c605eb59e7da4a98`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7638380d4eb3933d8241dfe83deaffc516e8bed7b2ab01f96b42864a0d722760`  
		Last Modified: Wed, 10 Apr 2024 01:35:27 GMT  
		Size: 25.5 MB (25535896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159dd7a1de12391b28b5260b6132a515d19e87a7e18b64d7bc843df2c26fb615`  
		Last Modified: Wed, 10 Apr 2024 01:35:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3004df08705794a49d57aabf8c97ae8dfe750cedd45eb476bd574ce29807e152`  
		Last Modified: Wed, 10 Apr 2024 01:35:21 GMT  
		Size: 263.3 KB (263307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4eb7e47773f01051ff8bed6e1e75760df109971229c7a276fc7299c77e1444`  
		Last Modified: Wed, 10 Apr 2024 01:37:33 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe828248e339ed1213f1728c3774b3fcbe81883eb47c39a77bded1d31b619866`  
		Last Modified: Wed, 10 Apr 2024 01:37:53 GMT  
		Size: 69.4 MB (69351371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0187d4b9bc619f6e5b9b6b4b45022d6f5f885398842d5e7b19103f3eff6d5d7d`  
		Last Modified: Wed, 10 Apr 2024 01:37:33 GMT  
		Size: 1.5 KB (1546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6320d39f2704b0c1762e0721121d0880c199f6dfe049f437c31318022f8d00d2`  
		Last Modified: Wed, 10 Apr 2024 04:40:13 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305f4502d0cf4a9a57015ac8a097d5f6636708172c5a249cdf37f4b7b5c2dfe2`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45625e4d8a700993f0fb347856d0df08e31374fca8b1a737332323ff07cf8ca`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb3362bfb653595714774c2d1cce61d5a02893675414b7d23b462602a727f20`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db153c0587fdf29cfded01b1cd48082057e376ad8636a6a254d3cc5d030775ca`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.7 MB (1661731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c45da18daa8ebd71fd796480f9850e0e1df9ce87467e733d09a937d867e369`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:5803daadce4687e1b203ced81b669960c05ad08be85e392562ecaba8efd6a48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:dd65119faf3e9848dfe903b2d36c44473682ef85d053853873e864f46e68a3f7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2096172662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf83f7bc549933a30beb62be150c320ee6ee873beb730199fe7c91d066d7b9cc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:06:58 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Apr 2024 01:06:59 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Apr 2024 01:06:59 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Apr 2024 01:07:00 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Apr 2024 01:07:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:07:38 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:07:59 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 01:22:55 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 10 Apr 2024 01:25:11 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:25:13 GMT
WORKDIR C:\go
# Wed, 10 Apr 2024 02:02:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 02:02:41 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 10 Apr 2024 02:02:42 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:02:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Apr 2024 02:03:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Apr 2024 02:03:12 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5ca144c62db12ea36d3f00f6640c6e4758e616b730c3d993fb57c3c8ebad9`  
		Last Modified: Wed, 10 Apr 2024 01:34:50 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d031792c46321e7a0a81f081515ffa50d7c86201a35780d03b0a1a0ecd68ebac`  
		Last Modified: Wed, 10 Apr 2024 01:34:49 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91b14b8df5887a0feab0adbfcf0dea95d1aab9c3e32619bf6ec5bdc4971a9a4`  
		Last Modified: Wed, 10 Apr 2024 01:34:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099fb3ff689379a9da8dc64f6c1c8d941fb9f0cf66715dc1af16055bdb8e63ec`  
		Last Modified: Wed, 10 Apr 2024 01:34:48 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ca11c05a0028bb84d4b2b76249dfcce87ea1f22340e50e79681c2055ee1d27`  
		Last Modified: Wed, 10 Apr 2024 01:34:54 GMT  
		Size: 25.5 MB (25528844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587f661259fd2478a26bea01012713bd3afd154dfc37f4aafd87ca98d67f75b7`  
		Last Modified: Wed, 10 Apr 2024 01:34:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5830a087830d60f2ed8f1cf87fba9d92cdf7706d61f7692f8aada1a5aec889e8`  
		Last Modified: Wed, 10 Apr 2024 01:34:47 GMT  
		Size: 255.6 KB (255649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5ba249752b259ec30317e6d9be24c9ae184897a3f96774f0a1f61fa6f8c196`  
		Last Modified: Wed, 10 Apr 2024 01:36:59 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc595e8d9ffdc13e2a491f83d29bbcf6e4fbbc1872cdf9b6d33156900f593be`  
		Last Modified: Wed, 10 Apr 2024 01:37:20 GMT  
		Size: 69.3 MB (69339784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9666572ffef44cedd89a1bf02be297824dcbb0e1db30b6f9a52cf06b09d181a0`  
		Last Modified: Wed, 10 Apr 2024 01:36:59 GMT  
		Size: 1.6 KB (1566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474f61eee778c75a6072d92f90f33cb8c3ba21ea0eded3d3a82ff35a91a50864`  
		Last Modified: Wed, 10 Apr 2024 04:40:31 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2f4771e42fee7692dd61c00fd5b5d18d7d8130854ee6dd737e581fc1ed2763`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86a9ad5c8f8b619270cd40a575f612322b7315fdf2105e6397a45d3707de156`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b4a4ffb9e9f9938b9bd40929d0422b0b5c111eba84c460246a970170261047`  
		Last Modified: Wed, 10 Apr 2024 04:40:28 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328e4a9a7a4cffe0480ebc46c068396be1a07000e05c24701ee9f2adf7e13cd3`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.7 MB (1656674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222acab8b494945e613aea2cd196dcf87a6f607c426f4d8a77b721a5c3ccb00b`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:399999da333b248fef2da843177c302602a2e3f939228d52df499d197ea08cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `caddy:2-windowsservercore` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:b4de45abdf801e6fe4e627d4a9146c7f3822666f9795f1fe35921da33d3b5920
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2015415021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1c537b274bb6928ea6772a745ddf910765f287696f3d596a64a2aef5bb3a49`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:59:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:59:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:00:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 02:00:12 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 02:00:13 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 02:00:13 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 02:00:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 02:00:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 02:00:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 02:00:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 02:00:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 02:00:20 GMT
EXPOSE 80
# Wed, 10 Apr 2024 02:00:21 GMT
EXPOSE 443
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 02:00:42 GMT
RUN caddy version
# Wed, 10 Apr 2024 02:00:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9cb628e4a7ceb9e124a728aba733c7b7837d0fe602c1af1c86af5ba7db1afe`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 462.4 KB (462386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe6244a1b7fd00d56255f78e7951d14811b06f10e069d90e75458e8f5198d6a`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fd5220e89ae5a44a14c920f948c28b3238c83307ad30f5955882930d72a23b`  
		Last Modified: Wed, 10 Apr 2024 04:39:56 GMT  
		Size: 15.3 MB (15272884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8711ac4c34fb1beb0cb9e799010a337864f252ea20a91c74e9ffb9dc4dd8f4`  
		Last Modified: Wed, 10 Apr 2024 04:39:52 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1bffa02c717094b56095d1f166aa11c19ba43f7481d7673313c862126f3434`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e554dc514103b8d140d5ab4e9437abe3875ce416cd9a69161836f9676d14b650`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f583dd206e697664bb89b8647ac1fe5d98933b1d6540b249433dae65d02dd09`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35fa3d4abc62509fa7c8c8b31d11482d23090a1f7e45393d43cbde05d0cd7e9`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254f688302923c46000c0526a060b43160db4d9314cbd342a3fc31620052ceaa`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e052187f5af8dbfaa36325485d886d7d47bbe36c18a5789d95efea81dfbf12`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea08dd4e4a398c33acb70cc8863ba300fad5cbf499840ed420b14ce06717f83`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc50e94c9c5e82f27b76ddd1796de52ee67ba64c275a531ee0d38c08757baf9e`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af1603a6bd4dacbf08b4c974a5db996c73e892cbe440e2d5339aa355847e5a0`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaaeba50589b199d8e988596dada19daaec59e8b26f7835e17a29fff8ac88f7`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b4695f6c339c5917ad1b57b3db1345b8cc1ac6b4e03d56d5f1de12f8e249a2`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d5e030bf8b034231beb875dd3a70af4fcf82b6350b60b23a72cef369792a29`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9280f84d3173ce915aa30f755697f993ca2d484caa9f8cd42334927563008d`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e2de6ed998eca032f334174172a69a2345072eda08fddd105b73a6e6238c81`  
		Last Modified: Wed, 10 Apr 2024 04:39:47 GMT  
		Size: 282.0 KB (282045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426ed15821e9616ced2fee524860d8e5554c359d0332601d4e035474c8a54964`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:650f5144a6e8b1d947f54c017a1002956e096891718dc7edf9aa8661be3f82ce
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2180450650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e356a94cf89f9d5eb0399e9f2ae7bbba82bc08e09f5dbc1d964352dfa2497f34`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:55:53 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:55:54 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 01:57:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 01:57:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 01:57:26 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 01:57:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 01:57:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 01:57:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 01:57:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 01:57:33 GMT
EXPOSE 80
# Wed, 10 Apr 2024 01:57:34 GMT
EXPOSE 443
# Wed, 10 Apr 2024 01:57:35 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 01:57:36 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 01:58:56 GMT
RUN caddy version
# Wed, 10 Apr 2024 01:58:57 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218ffc757feed37e26b36ff35084f4357219272c3ef8ce663a0db97763750bec`  
		Last Modified: Wed, 10 Apr 2024 04:39:29 GMT  
		Size: 465.0 KB (465007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f41e339dc34abe966a19ca999fece15bcf0a5e9eb2d36d4d42b84482e8e2ba`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac8e68361bdc1deb2d5d4e50f2da825b25f026f558a03aeeba18d6c7665e654`  
		Last Modified: Wed, 10 Apr 2024 04:39:32 GMT  
		Size: 15.3 MB (15281747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05561518ae50169e6e15468669f8195d9b2ee80d945dd94c107d20afda067318`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0720408b82b77dc7b0d925d39741de50fe2f9139768729af189a0f783b43519b`  
		Last Modified: Wed, 10 Apr 2024 04:39:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d8585bb3ff3b6a72b43181fc6df1c46ce88f6393295f32d2315e71c85e7295`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177da9a277ef013596e849aa2ea825a25dddcec2db12d81c6a4ab6fa02e77e57`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4686dffa2d26bcedea0a3b07e3d11640141e4a3888ddca8fc167fce49a67e102`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7411e6d276896da1fd4087fb7dbbe4e2169637862d1bee25144443263947ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966957575920790399f90fd33923b9cb27715dc7dd38e430480922326f86e953`  
		Last Modified: Wed, 10 Apr 2024 04:39:25 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa479db7e2e01c3cdda82927bbd2250f6933c5e4f6d67f09b4f090c26df209ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173767522133c716cc5b0c32c5c8778faa06e95a3933bab867e4569bb468420`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a488b5ddbaaac25b5ac6ce9375b9c9eb44e109874b5cd47d7f6591a446084bb`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27825614feb810c19f64b918a625f414d9f32098460aefcc9dad624bd2be669`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcc1e73eb545e48d76e61fd1029ab3a682c27085f1b3d23b2e7be300cd8eca8`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2713b7318664d7438093b75892a477ec691872f2c8fb13408d4d27d9bddd9`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce420a03b259096e6668f2765ce31ad5694523c86afe5c81bc0277d8b2bc861`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7baa1c6f084d5ad95cabb52b0d9aaed5e906928249958cb374cf25fe5e51e921`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 253.5 KB (253500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d599502ec7d608e46d6398aebafdee3aea525c5a3a58d826220dd06d128bb939`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:7c607664734ef3b7e94195c98f76a77c5be5ef8134d490741cf848306b1dbb4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:650f5144a6e8b1d947f54c017a1002956e096891718dc7edf9aa8661be3f82ce
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2180450650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e356a94cf89f9d5eb0399e9f2ae7bbba82bc08e09f5dbc1d964352dfa2497f34`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:55:53 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:55:54 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 01:57:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 01:57:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 01:57:26 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 01:57:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 01:57:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 01:57:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 01:57:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 01:57:33 GMT
EXPOSE 80
# Wed, 10 Apr 2024 01:57:34 GMT
EXPOSE 443
# Wed, 10 Apr 2024 01:57:35 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 01:57:36 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 01:58:56 GMT
RUN caddy version
# Wed, 10 Apr 2024 01:58:57 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218ffc757feed37e26b36ff35084f4357219272c3ef8ce663a0db97763750bec`  
		Last Modified: Wed, 10 Apr 2024 04:39:29 GMT  
		Size: 465.0 KB (465007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f41e339dc34abe966a19ca999fece15bcf0a5e9eb2d36d4d42b84482e8e2ba`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac8e68361bdc1deb2d5d4e50f2da825b25f026f558a03aeeba18d6c7665e654`  
		Last Modified: Wed, 10 Apr 2024 04:39:32 GMT  
		Size: 15.3 MB (15281747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05561518ae50169e6e15468669f8195d9b2ee80d945dd94c107d20afda067318`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0720408b82b77dc7b0d925d39741de50fe2f9139768729af189a0f783b43519b`  
		Last Modified: Wed, 10 Apr 2024 04:39:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d8585bb3ff3b6a72b43181fc6df1c46ce88f6393295f32d2315e71c85e7295`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177da9a277ef013596e849aa2ea825a25dddcec2db12d81c6a4ab6fa02e77e57`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4686dffa2d26bcedea0a3b07e3d11640141e4a3888ddca8fc167fce49a67e102`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7411e6d276896da1fd4087fb7dbbe4e2169637862d1bee25144443263947ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966957575920790399f90fd33923b9cb27715dc7dd38e430480922326f86e953`  
		Last Modified: Wed, 10 Apr 2024 04:39:25 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa479db7e2e01c3cdda82927bbd2250f6933c5e4f6d67f09b4f090c26df209ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173767522133c716cc5b0c32c5c8778faa06e95a3933bab867e4569bb468420`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a488b5ddbaaac25b5ac6ce9375b9c9eb44e109874b5cd47d7f6591a446084bb`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27825614feb810c19f64b918a625f414d9f32098460aefcc9dad624bd2be669`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcc1e73eb545e48d76e61fd1029ab3a682c27085f1b3d23b2e7be300cd8eca8`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2713b7318664d7438093b75892a477ec691872f2c8fb13408d4d27d9bddd9`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce420a03b259096e6668f2765ce31ad5694523c86afe5c81bc0277d8b2bc861`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7baa1c6f084d5ad95cabb52b0d9aaed5e906928249958cb374cf25fe5e51e921`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 253.5 KB (253500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d599502ec7d608e46d6398aebafdee3aea525c5a3a58d826220dd06d128bb939`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:e4749c1b0666aee331315ab98ffcab70c25aa1d1121f25f567c4278ae5d3f96c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:b4de45abdf801e6fe4e627d4a9146c7f3822666f9795f1fe35921da33d3b5920
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2015415021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1c537b274bb6928ea6772a745ddf910765f287696f3d596a64a2aef5bb3a49`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:59:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:59:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:00:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 02:00:12 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 02:00:13 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 02:00:13 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 02:00:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 02:00:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 02:00:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 02:00:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 02:00:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 02:00:20 GMT
EXPOSE 80
# Wed, 10 Apr 2024 02:00:21 GMT
EXPOSE 443
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 02:00:42 GMT
RUN caddy version
# Wed, 10 Apr 2024 02:00:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9cb628e4a7ceb9e124a728aba733c7b7837d0fe602c1af1c86af5ba7db1afe`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 462.4 KB (462386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe6244a1b7fd00d56255f78e7951d14811b06f10e069d90e75458e8f5198d6a`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fd5220e89ae5a44a14c920f948c28b3238c83307ad30f5955882930d72a23b`  
		Last Modified: Wed, 10 Apr 2024 04:39:56 GMT  
		Size: 15.3 MB (15272884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8711ac4c34fb1beb0cb9e799010a337864f252ea20a91c74e9ffb9dc4dd8f4`  
		Last Modified: Wed, 10 Apr 2024 04:39:52 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1bffa02c717094b56095d1f166aa11c19ba43f7481d7673313c862126f3434`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e554dc514103b8d140d5ab4e9437abe3875ce416cd9a69161836f9676d14b650`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f583dd206e697664bb89b8647ac1fe5d98933b1d6540b249433dae65d02dd09`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35fa3d4abc62509fa7c8c8b31d11482d23090a1f7e45393d43cbde05d0cd7e9`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254f688302923c46000c0526a060b43160db4d9314cbd342a3fc31620052ceaa`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e052187f5af8dbfaa36325485d886d7d47bbe36c18a5789d95efea81dfbf12`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea08dd4e4a398c33acb70cc8863ba300fad5cbf499840ed420b14ce06717f83`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc50e94c9c5e82f27b76ddd1796de52ee67ba64c275a531ee0d38c08757baf9e`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af1603a6bd4dacbf08b4c974a5db996c73e892cbe440e2d5339aa355847e5a0`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaaeba50589b199d8e988596dada19daaec59e8b26f7835e17a29fff8ac88f7`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b4695f6c339c5917ad1b57b3db1345b8cc1ac6b4e03d56d5f1de12f8e249a2`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d5e030bf8b034231beb875dd3a70af4fcf82b6350b60b23a72cef369792a29`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9280f84d3173ce915aa30f755697f993ca2d484caa9f8cd42334927563008d`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e2de6ed998eca032f334174172a69a2345072eda08fddd105b73a6e6238c81`  
		Last Modified: Wed, 10 Apr 2024 04:39:47 GMT  
		Size: 282.0 KB (282045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426ed15821e9616ced2fee524860d8e5554c359d0332601d4e035474c8a54964`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7`

```console
$ docker pull caddy@sha256:ca031cd33c788ebe467c94348400e5bf263178f9619f3993af8373f18681b8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

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

### `caddy:2.7` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:b4de45abdf801e6fe4e627d4a9146c7f3822666f9795f1fe35921da33d3b5920
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2015415021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1c537b274bb6928ea6772a745ddf910765f287696f3d596a64a2aef5bb3a49`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:59:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:59:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:00:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 02:00:12 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 02:00:13 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 02:00:13 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 02:00:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 02:00:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 02:00:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 02:00:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 02:00:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 02:00:20 GMT
EXPOSE 80
# Wed, 10 Apr 2024 02:00:21 GMT
EXPOSE 443
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 02:00:42 GMT
RUN caddy version
# Wed, 10 Apr 2024 02:00:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9cb628e4a7ceb9e124a728aba733c7b7837d0fe602c1af1c86af5ba7db1afe`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 462.4 KB (462386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe6244a1b7fd00d56255f78e7951d14811b06f10e069d90e75458e8f5198d6a`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fd5220e89ae5a44a14c920f948c28b3238c83307ad30f5955882930d72a23b`  
		Last Modified: Wed, 10 Apr 2024 04:39:56 GMT  
		Size: 15.3 MB (15272884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8711ac4c34fb1beb0cb9e799010a337864f252ea20a91c74e9ffb9dc4dd8f4`  
		Last Modified: Wed, 10 Apr 2024 04:39:52 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1bffa02c717094b56095d1f166aa11c19ba43f7481d7673313c862126f3434`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e554dc514103b8d140d5ab4e9437abe3875ce416cd9a69161836f9676d14b650`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f583dd206e697664bb89b8647ac1fe5d98933b1d6540b249433dae65d02dd09`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35fa3d4abc62509fa7c8c8b31d11482d23090a1f7e45393d43cbde05d0cd7e9`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254f688302923c46000c0526a060b43160db4d9314cbd342a3fc31620052ceaa`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e052187f5af8dbfaa36325485d886d7d47bbe36c18a5789d95efea81dfbf12`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea08dd4e4a398c33acb70cc8863ba300fad5cbf499840ed420b14ce06717f83`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc50e94c9c5e82f27b76ddd1796de52ee67ba64c275a531ee0d38c08757baf9e`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af1603a6bd4dacbf08b4c974a5db996c73e892cbe440e2d5339aa355847e5a0`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaaeba50589b199d8e988596dada19daaec59e8b26f7835e17a29fff8ac88f7`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b4695f6c339c5917ad1b57b3db1345b8cc1ac6b4e03d56d5f1de12f8e249a2`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d5e030bf8b034231beb875dd3a70af4fcf82b6350b60b23a72cef369792a29`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9280f84d3173ce915aa30f755697f993ca2d484caa9f8cd42334927563008d`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e2de6ed998eca032f334174172a69a2345072eda08fddd105b73a6e6238c81`  
		Last Modified: Wed, 10 Apr 2024 04:39:47 GMT  
		Size: 282.0 KB (282045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426ed15821e9616ced2fee524860d8e5554c359d0332601d4e035474c8a54964`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:650f5144a6e8b1d947f54c017a1002956e096891718dc7edf9aa8661be3f82ce
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2180450650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e356a94cf89f9d5eb0399e9f2ae7bbba82bc08e09f5dbc1d964352dfa2497f34`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:55:53 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:55:54 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 01:57:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 01:57:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 01:57:26 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 01:57:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 01:57:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 01:57:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 01:57:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 01:57:33 GMT
EXPOSE 80
# Wed, 10 Apr 2024 01:57:34 GMT
EXPOSE 443
# Wed, 10 Apr 2024 01:57:35 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 01:57:36 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 01:58:56 GMT
RUN caddy version
# Wed, 10 Apr 2024 01:58:57 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218ffc757feed37e26b36ff35084f4357219272c3ef8ce663a0db97763750bec`  
		Last Modified: Wed, 10 Apr 2024 04:39:29 GMT  
		Size: 465.0 KB (465007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f41e339dc34abe966a19ca999fece15bcf0a5e9eb2d36d4d42b84482e8e2ba`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac8e68361bdc1deb2d5d4e50f2da825b25f026f558a03aeeba18d6c7665e654`  
		Last Modified: Wed, 10 Apr 2024 04:39:32 GMT  
		Size: 15.3 MB (15281747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05561518ae50169e6e15468669f8195d9b2ee80d945dd94c107d20afda067318`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0720408b82b77dc7b0d925d39741de50fe2f9139768729af189a0f783b43519b`  
		Last Modified: Wed, 10 Apr 2024 04:39:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d8585bb3ff3b6a72b43181fc6df1c46ce88f6393295f32d2315e71c85e7295`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177da9a277ef013596e849aa2ea825a25dddcec2db12d81c6a4ab6fa02e77e57`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4686dffa2d26bcedea0a3b07e3d11640141e4a3888ddca8fc167fce49a67e102`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7411e6d276896da1fd4087fb7dbbe4e2169637862d1bee25144443263947ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966957575920790399f90fd33923b9cb27715dc7dd38e430480922326f86e953`  
		Last Modified: Wed, 10 Apr 2024 04:39:25 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa479db7e2e01c3cdda82927bbd2250f6933c5e4f6d67f09b4f090c26df209ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173767522133c716cc5b0c32c5c8778faa06e95a3933bab867e4569bb468420`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a488b5ddbaaac25b5ac6ce9375b9c9eb44e109874b5cd47d7f6591a446084bb`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27825614feb810c19f64b918a625f414d9f32098460aefcc9dad624bd2be669`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcc1e73eb545e48d76e61fd1029ab3a682c27085f1b3d23b2e7be300cd8eca8`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2713b7318664d7438093b75892a477ec691872f2c8fb13408d4d27d9bddd9`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce420a03b259096e6668f2765ce31ad5694523c86afe5c81bc0277d8b2bc861`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7baa1c6f084d5ad95cabb52b0d9aaed5e906928249958cb374cf25fe5e51e921`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 253.5 KB (253500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d599502ec7d608e46d6398aebafdee3aea525c5a3a58d826220dd06d128bb939`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.4 KB (1419 bytes)  
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
$ docker pull caddy@sha256:d8a2ad006009b25b7017ab7190128cdd3a0fccee518f5b14fe6c749c6a6293b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

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
$ docker pull caddy@sha256:a925804363a91c2468468c2ab1c1de2c770fe02812a21b1bdc1e9d8d65a5241b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75406613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acc712a703abf58b426c0681a4f724105efc534e813fca8d7e1769f2df5ebfe`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
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
# Wed, 03 Apr 2024 20:22:32 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 20:22:32 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 20:22:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 20:22:34 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 20:22:34 GMT
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
	-	`sha256:d72bd013141c752021b5b309e9868c02341e86fc25f37a89ccec1311ad14b2fd`  
		Last Modified: Wed, 03 Apr 2024 17:01:10 GMT  
		Size: 65.8 MB (65766638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abea289abae69e0933683886761310d242609c9941f5964366d9fb5bae890969`  
		Last Modified: Wed, 03 Apr 2024 17:00:57 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c466f5631c550594140cdcbad1c11c2549f51578de8dbf2181ab68d36e3860`  
		Last Modified: Wed, 03 Apr 2024 20:22:50 GMT  
		Size: 5.0 MB (4958760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c206e1c4695681bec33b38b6cb25bc40da76dd756937418fda1f1841f07a6b`  
		Last Modified: Wed, 03 Apr 2024 20:22:49 GMT  
		Size: 1.2 MB (1248664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1617709771cc71f393f3e93e93292a3024d9ec67376e73101934b6f2d2a14c`  
		Last Modified: Wed, 03 Apr 2024 20:22:48 GMT  
		Size: 406.0 B  
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

### `caddy:2.7-builder` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:dd65119faf3e9848dfe903b2d36c44473682ef85d053853873e864f46e68a3f7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2096172662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf83f7bc549933a30beb62be150c320ee6ee873beb730199fe7c91d066d7b9cc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:06:58 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Apr 2024 01:06:59 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Apr 2024 01:06:59 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Apr 2024 01:07:00 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Apr 2024 01:07:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:07:38 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:07:59 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 01:22:55 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 10 Apr 2024 01:25:11 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:25:13 GMT
WORKDIR C:\go
# Wed, 10 Apr 2024 02:02:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 02:02:41 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 10 Apr 2024 02:02:42 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:02:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Apr 2024 02:03:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Apr 2024 02:03:12 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5ca144c62db12ea36d3f00f6640c6e4758e616b730c3d993fb57c3c8ebad9`  
		Last Modified: Wed, 10 Apr 2024 01:34:50 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d031792c46321e7a0a81f081515ffa50d7c86201a35780d03b0a1a0ecd68ebac`  
		Last Modified: Wed, 10 Apr 2024 01:34:49 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91b14b8df5887a0feab0adbfcf0dea95d1aab9c3e32619bf6ec5bdc4971a9a4`  
		Last Modified: Wed, 10 Apr 2024 01:34:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099fb3ff689379a9da8dc64f6c1c8d941fb9f0cf66715dc1af16055bdb8e63ec`  
		Last Modified: Wed, 10 Apr 2024 01:34:48 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ca11c05a0028bb84d4b2b76249dfcce87ea1f22340e50e79681c2055ee1d27`  
		Last Modified: Wed, 10 Apr 2024 01:34:54 GMT  
		Size: 25.5 MB (25528844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587f661259fd2478a26bea01012713bd3afd154dfc37f4aafd87ca98d67f75b7`  
		Last Modified: Wed, 10 Apr 2024 01:34:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5830a087830d60f2ed8f1cf87fba9d92cdf7706d61f7692f8aada1a5aec889e8`  
		Last Modified: Wed, 10 Apr 2024 01:34:47 GMT  
		Size: 255.6 KB (255649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5ba249752b259ec30317e6d9be24c9ae184897a3f96774f0a1f61fa6f8c196`  
		Last Modified: Wed, 10 Apr 2024 01:36:59 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc595e8d9ffdc13e2a491f83d29bbcf6e4fbbc1872cdf9b6d33156900f593be`  
		Last Modified: Wed, 10 Apr 2024 01:37:20 GMT  
		Size: 69.3 MB (69339784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9666572ffef44cedd89a1bf02be297824dcbb0e1db30b6f9a52cf06b09d181a0`  
		Last Modified: Wed, 10 Apr 2024 01:36:59 GMT  
		Size: 1.6 KB (1566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474f61eee778c75a6072d92f90f33cb8c3ba21ea0eded3d3a82ff35a91a50864`  
		Last Modified: Wed, 10 Apr 2024 04:40:31 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2f4771e42fee7692dd61c00fd5b5d18d7d8130854ee6dd737e581fc1ed2763`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86a9ad5c8f8b619270cd40a575f612322b7315fdf2105e6397a45d3707de156`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b4a4ffb9e9f9938b9bd40929d0422b0b5c111eba84c460246a970170261047`  
		Last Modified: Wed, 10 Apr 2024 04:40:28 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328e4a9a7a4cffe0480ebc46c068396be1a07000e05c24701ee9f2adf7e13cd3`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.7 MB (1656674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222acab8b494945e613aea2cd196dcf87a6f607c426f4d8a77b721a5c3ccb00b`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:390a1ca91ca1409e1ddd37368179b927e08a5076b250132ee200be24319015bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261258422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc64e898993fdebf28e22269619414d6e7fed095f21d000c00b8d70339b915b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:10:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Apr 2024 01:10:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Apr 2024 01:10:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Apr 2024 01:10:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Apr 2024 01:12:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:12:15 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:13:36 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 01:25:25 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 10 Apr 2024 01:29:01 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:29:02 GMT
WORKDIR C:\go
# Wed, 10 Apr 2024 02:00:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 02:00:57 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 10 Apr 2024 02:00:58 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:00:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Apr 2024 02:02:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Apr 2024 02:02:33 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843b97b1625fa02e123dfc05bebcf9f05077e6dbdd1f5253c3c6d07b95f0f55f`  
		Last Modified: Wed, 10 Apr 2024 01:35:25 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6532f7333203cbc41355f91a4431427f575a24ad3dc3dd393b4292b4c2660d76`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c34d692c7e9d5e97e4674c9fefa41e1c78447d2e9c8db3a3f94f325b6188af`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cead4e65b4492e37b01dc6043de135f9dfad18c9f01232c605eb59e7da4a98`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7638380d4eb3933d8241dfe83deaffc516e8bed7b2ab01f96b42864a0d722760`  
		Last Modified: Wed, 10 Apr 2024 01:35:27 GMT  
		Size: 25.5 MB (25535896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159dd7a1de12391b28b5260b6132a515d19e87a7e18b64d7bc843df2c26fb615`  
		Last Modified: Wed, 10 Apr 2024 01:35:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3004df08705794a49d57aabf8c97ae8dfe750cedd45eb476bd574ce29807e152`  
		Last Modified: Wed, 10 Apr 2024 01:35:21 GMT  
		Size: 263.3 KB (263307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4eb7e47773f01051ff8bed6e1e75760df109971229c7a276fc7299c77e1444`  
		Last Modified: Wed, 10 Apr 2024 01:37:33 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe828248e339ed1213f1728c3774b3fcbe81883eb47c39a77bded1d31b619866`  
		Last Modified: Wed, 10 Apr 2024 01:37:53 GMT  
		Size: 69.4 MB (69351371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0187d4b9bc619f6e5b9b6b4b45022d6f5f885398842d5e7b19103f3eff6d5d7d`  
		Last Modified: Wed, 10 Apr 2024 01:37:33 GMT  
		Size: 1.5 KB (1546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6320d39f2704b0c1762e0721121d0880c199f6dfe049f437c31318022f8d00d2`  
		Last Modified: Wed, 10 Apr 2024 04:40:13 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305f4502d0cf4a9a57015ac8a097d5f6636708172c5a249cdf37f4b7b5c2dfe2`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45625e4d8a700993f0fb347856d0df08e31374fca8b1a737332323ff07cf8ca`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb3362bfb653595714774c2d1cce61d5a02893675414b7d23b462602a727f20`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db153c0587fdf29cfded01b1cd48082057e376ad8636a6a254d3cc5d030775ca`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.7 MB (1661731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c45da18daa8ebd71fd796480f9850e0e1df9ce87467e733d09a937d867e369`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-alpine`

```console
$ docker pull caddy@sha256:481c3357e533d892e2621d69ce3747a459e40af2f56159bcbd64b38bee1aa5bd
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
$ docker pull caddy@sha256:a925804363a91c2468468c2ab1c1de2c770fe02812a21b1bdc1e9d8d65a5241b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75406613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acc712a703abf58b426c0681a4f724105efc534e813fca8d7e1769f2df5ebfe`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
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
# Wed, 03 Apr 2024 20:22:32 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 20:22:32 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 20:22:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 20:22:34 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 20:22:34 GMT
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
	-	`sha256:d72bd013141c752021b5b309e9868c02341e86fc25f37a89ccec1311ad14b2fd`  
		Last Modified: Wed, 03 Apr 2024 17:01:10 GMT  
		Size: 65.8 MB (65766638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abea289abae69e0933683886761310d242609c9941f5964366d9fb5bae890969`  
		Last Modified: Wed, 03 Apr 2024 17:00:57 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c466f5631c550594140cdcbad1c11c2549f51578de8dbf2181ab68d36e3860`  
		Last Modified: Wed, 03 Apr 2024 20:22:50 GMT  
		Size: 5.0 MB (4958760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c206e1c4695681bec33b38b6cb25bc40da76dd756937418fda1f1841f07a6b`  
		Last Modified: Wed, 03 Apr 2024 20:22:49 GMT  
		Size: 1.2 MB (1248664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1617709771cc71f393f3e93e93292a3024d9ec67376e73101934b6f2d2a14c`  
		Last Modified: Wed, 03 Apr 2024 20:22:48 GMT  
		Size: 406.0 B  
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
$ docker pull caddy@sha256:737e66da3299a8c95988bbf4d40a3c4598cca4f803e9a27e3a7bd8fa63b109c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `caddy:2.7-builder-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:390a1ca91ca1409e1ddd37368179b927e08a5076b250132ee200be24319015bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261258422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc64e898993fdebf28e22269619414d6e7fed095f21d000c00b8d70339b915b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:10:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Apr 2024 01:10:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Apr 2024 01:10:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Apr 2024 01:10:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Apr 2024 01:12:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:12:15 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:13:36 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 01:25:25 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 10 Apr 2024 01:29:01 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:29:02 GMT
WORKDIR C:\go
# Wed, 10 Apr 2024 02:00:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 02:00:57 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 10 Apr 2024 02:00:58 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:00:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Apr 2024 02:02:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Apr 2024 02:02:33 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843b97b1625fa02e123dfc05bebcf9f05077e6dbdd1f5253c3c6d07b95f0f55f`  
		Last Modified: Wed, 10 Apr 2024 01:35:25 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6532f7333203cbc41355f91a4431427f575a24ad3dc3dd393b4292b4c2660d76`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c34d692c7e9d5e97e4674c9fefa41e1c78447d2e9c8db3a3f94f325b6188af`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cead4e65b4492e37b01dc6043de135f9dfad18c9f01232c605eb59e7da4a98`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7638380d4eb3933d8241dfe83deaffc516e8bed7b2ab01f96b42864a0d722760`  
		Last Modified: Wed, 10 Apr 2024 01:35:27 GMT  
		Size: 25.5 MB (25535896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159dd7a1de12391b28b5260b6132a515d19e87a7e18b64d7bc843df2c26fb615`  
		Last Modified: Wed, 10 Apr 2024 01:35:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3004df08705794a49d57aabf8c97ae8dfe750cedd45eb476bd574ce29807e152`  
		Last Modified: Wed, 10 Apr 2024 01:35:21 GMT  
		Size: 263.3 KB (263307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4eb7e47773f01051ff8bed6e1e75760df109971229c7a276fc7299c77e1444`  
		Last Modified: Wed, 10 Apr 2024 01:37:33 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe828248e339ed1213f1728c3774b3fcbe81883eb47c39a77bded1d31b619866`  
		Last Modified: Wed, 10 Apr 2024 01:37:53 GMT  
		Size: 69.4 MB (69351371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0187d4b9bc619f6e5b9b6b4b45022d6f5f885398842d5e7b19103f3eff6d5d7d`  
		Last Modified: Wed, 10 Apr 2024 01:37:33 GMT  
		Size: 1.5 KB (1546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6320d39f2704b0c1762e0721121d0880c199f6dfe049f437c31318022f8d00d2`  
		Last Modified: Wed, 10 Apr 2024 04:40:13 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305f4502d0cf4a9a57015ac8a097d5f6636708172c5a249cdf37f4b7b5c2dfe2`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45625e4d8a700993f0fb347856d0df08e31374fca8b1a737332323ff07cf8ca`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb3362bfb653595714774c2d1cce61d5a02893675414b7d23b462602a727f20`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db153c0587fdf29cfded01b1cd48082057e376ad8636a6a254d3cc5d030775ca`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.7 MB (1661731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c45da18daa8ebd71fd796480f9850e0e1df9ce87467e733d09a937d867e369`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:5803daadce4687e1b203ced81b669960c05ad08be85e392562ecaba8efd6a48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `caddy:2.7-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:dd65119faf3e9848dfe903b2d36c44473682ef85d053853873e864f46e68a3f7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2096172662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf83f7bc549933a30beb62be150c320ee6ee873beb730199fe7c91d066d7b9cc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:06:58 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Apr 2024 01:06:59 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Apr 2024 01:06:59 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Apr 2024 01:07:00 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Apr 2024 01:07:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:07:38 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:07:59 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 01:22:55 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 10 Apr 2024 01:25:11 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:25:13 GMT
WORKDIR C:\go
# Wed, 10 Apr 2024 02:02:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 02:02:41 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 10 Apr 2024 02:02:42 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:02:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Apr 2024 02:03:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Apr 2024 02:03:12 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5ca144c62db12ea36d3f00f6640c6e4758e616b730c3d993fb57c3c8ebad9`  
		Last Modified: Wed, 10 Apr 2024 01:34:50 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d031792c46321e7a0a81f081515ffa50d7c86201a35780d03b0a1a0ecd68ebac`  
		Last Modified: Wed, 10 Apr 2024 01:34:49 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91b14b8df5887a0feab0adbfcf0dea95d1aab9c3e32619bf6ec5bdc4971a9a4`  
		Last Modified: Wed, 10 Apr 2024 01:34:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099fb3ff689379a9da8dc64f6c1c8d941fb9f0cf66715dc1af16055bdb8e63ec`  
		Last Modified: Wed, 10 Apr 2024 01:34:48 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ca11c05a0028bb84d4b2b76249dfcce87ea1f22340e50e79681c2055ee1d27`  
		Last Modified: Wed, 10 Apr 2024 01:34:54 GMT  
		Size: 25.5 MB (25528844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587f661259fd2478a26bea01012713bd3afd154dfc37f4aafd87ca98d67f75b7`  
		Last Modified: Wed, 10 Apr 2024 01:34:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5830a087830d60f2ed8f1cf87fba9d92cdf7706d61f7692f8aada1a5aec889e8`  
		Last Modified: Wed, 10 Apr 2024 01:34:47 GMT  
		Size: 255.6 KB (255649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5ba249752b259ec30317e6d9be24c9ae184897a3f96774f0a1f61fa6f8c196`  
		Last Modified: Wed, 10 Apr 2024 01:36:59 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc595e8d9ffdc13e2a491f83d29bbcf6e4fbbc1872cdf9b6d33156900f593be`  
		Last Modified: Wed, 10 Apr 2024 01:37:20 GMT  
		Size: 69.3 MB (69339784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9666572ffef44cedd89a1bf02be297824dcbb0e1db30b6f9a52cf06b09d181a0`  
		Last Modified: Wed, 10 Apr 2024 01:36:59 GMT  
		Size: 1.6 KB (1566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474f61eee778c75a6072d92f90f33cb8c3ba21ea0eded3d3a82ff35a91a50864`  
		Last Modified: Wed, 10 Apr 2024 04:40:31 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2f4771e42fee7692dd61c00fd5b5d18d7d8130854ee6dd737e581fc1ed2763`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86a9ad5c8f8b619270cd40a575f612322b7315fdf2105e6397a45d3707de156`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b4a4ffb9e9f9938b9bd40929d0422b0b5c111eba84c460246a970170261047`  
		Last Modified: Wed, 10 Apr 2024 04:40:28 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328e4a9a7a4cffe0480ebc46c068396be1a07000e05c24701ee9f2adf7e13cd3`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.7 MB (1656674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222acab8b494945e613aea2cd196dcf87a6f607c426f4d8a77b721a5c3ccb00b`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-windowsservercore`

```console
$ docker pull caddy@sha256:399999da333b248fef2da843177c302602a2e3f939228d52df499d197ea08cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `caddy:2.7-windowsservercore` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:b4de45abdf801e6fe4e627d4a9146c7f3822666f9795f1fe35921da33d3b5920
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2015415021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1c537b274bb6928ea6772a745ddf910765f287696f3d596a64a2aef5bb3a49`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:59:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:59:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:00:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 02:00:12 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 02:00:13 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 02:00:13 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 02:00:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 02:00:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 02:00:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 02:00:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 02:00:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 02:00:20 GMT
EXPOSE 80
# Wed, 10 Apr 2024 02:00:21 GMT
EXPOSE 443
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 02:00:42 GMT
RUN caddy version
# Wed, 10 Apr 2024 02:00:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9cb628e4a7ceb9e124a728aba733c7b7837d0fe602c1af1c86af5ba7db1afe`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 462.4 KB (462386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe6244a1b7fd00d56255f78e7951d14811b06f10e069d90e75458e8f5198d6a`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fd5220e89ae5a44a14c920f948c28b3238c83307ad30f5955882930d72a23b`  
		Last Modified: Wed, 10 Apr 2024 04:39:56 GMT  
		Size: 15.3 MB (15272884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8711ac4c34fb1beb0cb9e799010a337864f252ea20a91c74e9ffb9dc4dd8f4`  
		Last Modified: Wed, 10 Apr 2024 04:39:52 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1bffa02c717094b56095d1f166aa11c19ba43f7481d7673313c862126f3434`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e554dc514103b8d140d5ab4e9437abe3875ce416cd9a69161836f9676d14b650`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f583dd206e697664bb89b8647ac1fe5d98933b1d6540b249433dae65d02dd09`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35fa3d4abc62509fa7c8c8b31d11482d23090a1f7e45393d43cbde05d0cd7e9`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254f688302923c46000c0526a060b43160db4d9314cbd342a3fc31620052ceaa`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e052187f5af8dbfaa36325485d886d7d47bbe36c18a5789d95efea81dfbf12`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea08dd4e4a398c33acb70cc8863ba300fad5cbf499840ed420b14ce06717f83`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc50e94c9c5e82f27b76ddd1796de52ee67ba64c275a531ee0d38c08757baf9e`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af1603a6bd4dacbf08b4c974a5db996c73e892cbe440e2d5339aa355847e5a0`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaaeba50589b199d8e988596dada19daaec59e8b26f7835e17a29fff8ac88f7`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b4695f6c339c5917ad1b57b3db1345b8cc1ac6b4e03d56d5f1de12f8e249a2`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d5e030bf8b034231beb875dd3a70af4fcf82b6350b60b23a72cef369792a29`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9280f84d3173ce915aa30f755697f993ca2d484caa9f8cd42334927563008d`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e2de6ed998eca032f334174172a69a2345072eda08fddd105b73a6e6238c81`  
		Last Modified: Wed, 10 Apr 2024 04:39:47 GMT  
		Size: 282.0 KB (282045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426ed15821e9616ced2fee524860d8e5554c359d0332601d4e035474c8a54964`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-windowsservercore` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:650f5144a6e8b1d947f54c017a1002956e096891718dc7edf9aa8661be3f82ce
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2180450650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e356a94cf89f9d5eb0399e9f2ae7bbba82bc08e09f5dbc1d964352dfa2497f34`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:55:53 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:55:54 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 01:57:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 01:57:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 01:57:26 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 01:57:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 01:57:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 01:57:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 01:57:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 01:57:33 GMT
EXPOSE 80
# Wed, 10 Apr 2024 01:57:34 GMT
EXPOSE 443
# Wed, 10 Apr 2024 01:57:35 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 01:57:36 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 01:58:56 GMT
RUN caddy version
# Wed, 10 Apr 2024 01:58:57 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218ffc757feed37e26b36ff35084f4357219272c3ef8ce663a0db97763750bec`  
		Last Modified: Wed, 10 Apr 2024 04:39:29 GMT  
		Size: 465.0 KB (465007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f41e339dc34abe966a19ca999fece15bcf0a5e9eb2d36d4d42b84482e8e2ba`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac8e68361bdc1deb2d5d4e50f2da825b25f026f558a03aeeba18d6c7665e654`  
		Last Modified: Wed, 10 Apr 2024 04:39:32 GMT  
		Size: 15.3 MB (15281747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05561518ae50169e6e15468669f8195d9b2ee80d945dd94c107d20afda067318`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0720408b82b77dc7b0d925d39741de50fe2f9139768729af189a0f783b43519b`  
		Last Modified: Wed, 10 Apr 2024 04:39:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d8585bb3ff3b6a72b43181fc6df1c46ce88f6393295f32d2315e71c85e7295`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177da9a277ef013596e849aa2ea825a25dddcec2db12d81c6a4ab6fa02e77e57`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4686dffa2d26bcedea0a3b07e3d11640141e4a3888ddca8fc167fce49a67e102`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7411e6d276896da1fd4087fb7dbbe4e2169637862d1bee25144443263947ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966957575920790399f90fd33923b9cb27715dc7dd38e430480922326f86e953`  
		Last Modified: Wed, 10 Apr 2024 04:39:25 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa479db7e2e01c3cdda82927bbd2250f6933c5e4f6d67f09b4f090c26df209ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173767522133c716cc5b0c32c5c8778faa06e95a3933bab867e4569bb468420`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a488b5ddbaaac25b5ac6ce9375b9c9eb44e109874b5cd47d7f6591a446084bb`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27825614feb810c19f64b918a625f414d9f32098460aefcc9dad624bd2be669`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcc1e73eb545e48d76e61fd1029ab3a682c27085f1b3d23b2e7be300cd8eca8`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2713b7318664d7438093b75892a477ec691872f2c8fb13408d4d27d9bddd9`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce420a03b259096e6668f2765ce31ad5694523c86afe5c81bc0277d8b2bc861`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7baa1c6f084d5ad95cabb52b0d9aaed5e906928249958cb374cf25fe5e51e921`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 253.5 KB (253500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d599502ec7d608e46d6398aebafdee3aea525c5a3a58d826220dd06d128bb939`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-windowsservercore-1809`

```console
$ docker pull caddy@sha256:7c607664734ef3b7e94195c98f76a77c5be5ef8134d490741cf848306b1dbb4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `caddy:2.7-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:650f5144a6e8b1d947f54c017a1002956e096891718dc7edf9aa8661be3f82ce
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2180450650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e356a94cf89f9d5eb0399e9f2ae7bbba82bc08e09f5dbc1d964352dfa2497f34`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:55:53 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:55:54 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 01:57:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 01:57:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 01:57:26 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 01:57:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 01:57:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 01:57:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 01:57:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 01:57:33 GMT
EXPOSE 80
# Wed, 10 Apr 2024 01:57:34 GMT
EXPOSE 443
# Wed, 10 Apr 2024 01:57:35 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 01:57:36 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 01:58:56 GMT
RUN caddy version
# Wed, 10 Apr 2024 01:58:57 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218ffc757feed37e26b36ff35084f4357219272c3ef8ce663a0db97763750bec`  
		Last Modified: Wed, 10 Apr 2024 04:39:29 GMT  
		Size: 465.0 KB (465007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f41e339dc34abe966a19ca999fece15bcf0a5e9eb2d36d4d42b84482e8e2ba`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac8e68361bdc1deb2d5d4e50f2da825b25f026f558a03aeeba18d6c7665e654`  
		Last Modified: Wed, 10 Apr 2024 04:39:32 GMT  
		Size: 15.3 MB (15281747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05561518ae50169e6e15468669f8195d9b2ee80d945dd94c107d20afda067318`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0720408b82b77dc7b0d925d39741de50fe2f9139768729af189a0f783b43519b`  
		Last Modified: Wed, 10 Apr 2024 04:39:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d8585bb3ff3b6a72b43181fc6df1c46ce88f6393295f32d2315e71c85e7295`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177da9a277ef013596e849aa2ea825a25dddcec2db12d81c6a4ab6fa02e77e57`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4686dffa2d26bcedea0a3b07e3d11640141e4a3888ddca8fc167fce49a67e102`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7411e6d276896da1fd4087fb7dbbe4e2169637862d1bee25144443263947ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966957575920790399f90fd33923b9cb27715dc7dd38e430480922326f86e953`  
		Last Modified: Wed, 10 Apr 2024 04:39:25 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa479db7e2e01c3cdda82927bbd2250f6933c5e4f6d67f09b4f090c26df209ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173767522133c716cc5b0c32c5c8778faa06e95a3933bab867e4569bb468420`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a488b5ddbaaac25b5ac6ce9375b9c9eb44e109874b5cd47d7f6591a446084bb`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27825614feb810c19f64b918a625f414d9f32098460aefcc9dad624bd2be669`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcc1e73eb545e48d76e61fd1029ab3a682c27085f1b3d23b2e7be300cd8eca8`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2713b7318664d7438093b75892a477ec691872f2c8fb13408d4d27d9bddd9`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce420a03b259096e6668f2765ce31ad5694523c86afe5c81bc0277d8b2bc861`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7baa1c6f084d5ad95cabb52b0d9aaed5e906928249958cb374cf25fe5e51e921`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 253.5 KB (253500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d599502ec7d608e46d6398aebafdee3aea525c5a3a58d826220dd06d128bb939`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:e4749c1b0666aee331315ab98ffcab70c25aa1d1121f25f567c4278ae5d3f96c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `caddy:2.7-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:b4de45abdf801e6fe4e627d4a9146c7f3822666f9795f1fe35921da33d3b5920
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2015415021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1c537b274bb6928ea6772a745ddf910765f287696f3d596a64a2aef5bb3a49`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:59:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:59:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:00:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 02:00:12 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 02:00:13 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 02:00:13 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 02:00:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 02:00:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 02:00:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 02:00:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 02:00:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 02:00:20 GMT
EXPOSE 80
# Wed, 10 Apr 2024 02:00:21 GMT
EXPOSE 443
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 02:00:42 GMT
RUN caddy version
# Wed, 10 Apr 2024 02:00:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9cb628e4a7ceb9e124a728aba733c7b7837d0fe602c1af1c86af5ba7db1afe`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 462.4 KB (462386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe6244a1b7fd00d56255f78e7951d14811b06f10e069d90e75458e8f5198d6a`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fd5220e89ae5a44a14c920f948c28b3238c83307ad30f5955882930d72a23b`  
		Last Modified: Wed, 10 Apr 2024 04:39:56 GMT  
		Size: 15.3 MB (15272884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8711ac4c34fb1beb0cb9e799010a337864f252ea20a91c74e9ffb9dc4dd8f4`  
		Last Modified: Wed, 10 Apr 2024 04:39:52 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1bffa02c717094b56095d1f166aa11c19ba43f7481d7673313c862126f3434`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e554dc514103b8d140d5ab4e9437abe3875ce416cd9a69161836f9676d14b650`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f583dd206e697664bb89b8647ac1fe5d98933b1d6540b249433dae65d02dd09`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35fa3d4abc62509fa7c8c8b31d11482d23090a1f7e45393d43cbde05d0cd7e9`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254f688302923c46000c0526a060b43160db4d9314cbd342a3fc31620052ceaa`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e052187f5af8dbfaa36325485d886d7d47bbe36c18a5789d95efea81dfbf12`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea08dd4e4a398c33acb70cc8863ba300fad5cbf499840ed420b14ce06717f83`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc50e94c9c5e82f27b76ddd1796de52ee67ba64c275a531ee0d38c08757baf9e`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af1603a6bd4dacbf08b4c974a5db996c73e892cbe440e2d5339aa355847e5a0`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaaeba50589b199d8e988596dada19daaec59e8b26f7835e17a29fff8ac88f7`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b4695f6c339c5917ad1b57b3db1345b8cc1ac6b4e03d56d5f1de12f8e249a2`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d5e030bf8b034231beb875dd3a70af4fcf82b6350b60b23a72cef369792a29`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9280f84d3173ce915aa30f755697f993ca2d484caa9f8cd42334927563008d`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e2de6ed998eca032f334174172a69a2345072eda08fddd105b73a6e6238c81`  
		Last Modified: Wed, 10 Apr 2024 04:39:47 GMT  
		Size: 282.0 KB (282045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426ed15821e9616ced2fee524860d8e5554c359d0332601d4e035474c8a54964`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6`

```console
$ docker pull caddy@sha256:ca031cd33c788ebe467c94348400e5bf263178f9619f3993af8373f18681b8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

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

### `caddy:2.7.6` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:b4de45abdf801e6fe4e627d4a9146c7f3822666f9795f1fe35921da33d3b5920
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2015415021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1c537b274bb6928ea6772a745ddf910765f287696f3d596a64a2aef5bb3a49`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:59:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:59:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:00:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 02:00:12 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 02:00:13 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 02:00:13 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 02:00:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 02:00:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 02:00:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 02:00:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 02:00:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 02:00:20 GMT
EXPOSE 80
# Wed, 10 Apr 2024 02:00:21 GMT
EXPOSE 443
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 02:00:42 GMT
RUN caddy version
# Wed, 10 Apr 2024 02:00:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9cb628e4a7ceb9e124a728aba733c7b7837d0fe602c1af1c86af5ba7db1afe`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 462.4 KB (462386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe6244a1b7fd00d56255f78e7951d14811b06f10e069d90e75458e8f5198d6a`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fd5220e89ae5a44a14c920f948c28b3238c83307ad30f5955882930d72a23b`  
		Last Modified: Wed, 10 Apr 2024 04:39:56 GMT  
		Size: 15.3 MB (15272884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8711ac4c34fb1beb0cb9e799010a337864f252ea20a91c74e9ffb9dc4dd8f4`  
		Last Modified: Wed, 10 Apr 2024 04:39:52 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1bffa02c717094b56095d1f166aa11c19ba43f7481d7673313c862126f3434`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e554dc514103b8d140d5ab4e9437abe3875ce416cd9a69161836f9676d14b650`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f583dd206e697664bb89b8647ac1fe5d98933b1d6540b249433dae65d02dd09`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35fa3d4abc62509fa7c8c8b31d11482d23090a1f7e45393d43cbde05d0cd7e9`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254f688302923c46000c0526a060b43160db4d9314cbd342a3fc31620052ceaa`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e052187f5af8dbfaa36325485d886d7d47bbe36c18a5789d95efea81dfbf12`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea08dd4e4a398c33acb70cc8863ba300fad5cbf499840ed420b14ce06717f83`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc50e94c9c5e82f27b76ddd1796de52ee67ba64c275a531ee0d38c08757baf9e`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af1603a6bd4dacbf08b4c974a5db996c73e892cbe440e2d5339aa355847e5a0`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaaeba50589b199d8e988596dada19daaec59e8b26f7835e17a29fff8ac88f7`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b4695f6c339c5917ad1b57b3db1345b8cc1ac6b4e03d56d5f1de12f8e249a2`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d5e030bf8b034231beb875dd3a70af4fcf82b6350b60b23a72cef369792a29`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9280f84d3173ce915aa30f755697f993ca2d484caa9f8cd42334927563008d`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e2de6ed998eca032f334174172a69a2345072eda08fddd105b73a6e6238c81`  
		Last Modified: Wed, 10 Apr 2024 04:39:47 GMT  
		Size: 282.0 KB (282045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426ed15821e9616ced2fee524860d8e5554c359d0332601d4e035474c8a54964`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:650f5144a6e8b1d947f54c017a1002956e096891718dc7edf9aa8661be3f82ce
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2180450650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e356a94cf89f9d5eb0399e9f2ae7bbba82bc08e09f5dbc1d964352dfa2497f34`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:55:53 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:55:54 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 01:57:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 01:57:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 01:57:26 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 01:57:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 01:57:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 01:57:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 01:57:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 01:57:33 GMT
EXPOSE 80
# Wed, 10 Apr 2024 01:57:34 GMT
EXPOSE 443
# Wed, 10 Apr 2024 01:57:35 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 01:57:36 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 01:58:56 GMT
RUN caddy version
# Wed, 10 Apr 2024 01:58:57 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218ffc757feed37e26b36ff35084f4357219272c3ef8ce663a0db97763750bec`  
		Last Modified: Wed, 10 Apr 2024 04:39:29 GMT  
		Size: 465.0 KB (465007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f41e339dc34abe966a19ca999fece15bcf0a5e9eb2d36d4d42b84482e8e2ba`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac8e68361bdc1deb2d5d4e50f2da825b25f026f558a03aeeba18d6c7665e654`  
		Last Modified: Wed, 10 Apr 2024 04:39:32 GMT  
		Size: 15.3 MB (15281747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05561518ae50169e6e15468669f8195d9b2ee80d945dd94c107d20afda067318`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0720408b82b77dc7b0d925d39741de50fe2f9139768729af189a0f783b43519b`  
		Last Modified: Wed, 10 Apr 2024 04:39:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d8585bb3ff3b6a72b43181fc6df1c46ce88f6393295f32d2315e71c85e7295`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177da9a277ef013596e849aa2ea825a25dddcec2db12d81c6a4ab6fa02e77e57`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4686dffa2d26bcedea0a3b07e3d11640141e4a3888ddca8fc167fce49a67e102`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7411e6d276896da1fd4087fb7dbbe4e2169637862d1bee25144443263947ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966957575920790399f90fd33923b9cb27715dc7dd38e430480922326f86e953`  
		Last Modified: Wed, 10 Apr 2024 04:39:25 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa479db7e2e01c3cdda82927bbd2250f6933c5e4f6d67f09b4f090c26df209ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173767522133c716cc5b0c32c5c8778faa06e95a3933bab867e4569bb468420`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a488b5ddbaaac25b5ac6ce9375b9c9eb44e109874b5cd47d7f6591a446084bb`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27825614feb810c19f64b918a625f414d9f32098460aefcc9dad624bd2be669`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcc1e73eb545e48d76e61fd1029ab3a682c27085f1b3d23b2e7be300cd8eca8`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2713b7318664d7438093b75892a477ec691872f2c8fb13408d4d27d9bddd9`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce420a03b259096e6668f2765ce31ad5694523c86afe5c81bc0277d8b2bc861`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7baa1c6f084d5ad95cabb52b0d9aaed5e906928249958cb374cf25fe5e51e921`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 253.5 KB (253500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d599502ec7d608e46d6398aebafdee3aea525c5a3a58d826220dd06d128bb939`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.4 KB (1419 bytes)  
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
$ docker pull caddy@sha256:d8a2ad006009b25b7017ab7190128cdd3a0fccee518f5b14fe6c749c6a6293b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

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
$ docker pull caddy@sha256:a925804363a91c2468468c2ab1c1de2c770fe02812a21b1bdc1e9d8d65a5241b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75406613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acc712a703abf58b426c0681a4f724105efc534e813fca8d7e1769f2df5ebfe`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
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
# Wed, 03 Apr 2024 20:22:32 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 20:22:32 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 20:22:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 20:22:34 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 20:22:34 GMT
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
	-	`sha256:d72bd013141c752021b5b309e9868c02341e86fc25f37a89ccec1311ad14b2fd`  
		Last Modified: Wed, 03 Apr 2024 17:01:10 GMT  
		Size: 65.8 MB (65766638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abea289abae69e0933683886761310d242609c9941f5964366d9fb5bae890969`  
		Last Modified: Wed, 03 Apr 2024 17:00:57 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c466f5631c550594140cdcbad1c11c2549f51578de8dbf2181ab68d36e3860`  
		Last Modified: Wed, 03 Apr 2024 20:22:50 GMT  
		Size: 5.0 MB (4958760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c206e1c4695681bec33b38b6cb25bc40da76dd756937418fda1f1841f07a6b`  
		Last Modified: Wed, 03 Apr 2024 20:22:49 GMT  
		Size: 1.2 MB (1248664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1617709771cc71f393f3e93e93292a3024d9ec67376e73101934b6f2d2a14c`  
		Last Modified: Wed, 03 Apr 2024 20:22:48 GMT  
		Size: 406.0 B  
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

### `caddy:2.7.6-builder` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:dd65119faf3e9848dfe903b2d36c44473682ef85d053853873e864f46e68a3f7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2096172662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf83f7bc549933a30beb62be150c320ee6ee873beb730199fe7c91d066d7b9cc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:06:58 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Apr 2024 01:06:59 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Apr 2024 01:06:59 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Apr 2024 01:07:00 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Apr 2024 01:07:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:07:38 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:07:59 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 01:22:55 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 10 Apr 2024 01:25:11 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:25:13 GMT
WORKDIR C:\go
# Wed, 10 Apr 2024 02:02:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 02:02:41 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 10 Apr 2024 02:02:42 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:02:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Apr 2024 02:03:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Apr 2024 02:03:12 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5ca144c62db12ea36d3f00f6640c6e4758e616b730c3d993fb57c3c8ebad9`  
		Last Modified: Wed, 10 Apr 2024 01:34:50 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d031792c46321e7a0a81f081515ffa50d7c86201a35780d03b0a1a0ecd68ebac`  
		Last Modified: Wed, 10 Apr 2024 01:34:49 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91b14b8df5887a0feab0adbfcf0dea95d1aab9c3e32619bf6ec5bdc4971a9a4`  
		Last Modified: Wed, 10 Apr 2024 01:34:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099fb3ff689379a9da8dc64f6c1c8d941fb9f0cf66715dc1af16055bdb8e63ec`  
		Last Modified: Wed, 10 Apr 2024 01:34:48 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ca11c05a0028bb84d4b2b76249dfcce87ea1f22340e50e79681c2055ee1d27`  
		Last Modified: Wed, 10 Apr 2024 01:34:54 GMT  
		Size: 25.5 MB (25528844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587f661259fd2478a26bea01012713bd3afd154dfc37f4aafd87ca98d67f75b7`  
		Last Modified: Wed, 10 Apr 2024 01:34:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5830a087830d60f2ed8f1cf87fba9d92cdf7706d61f7692f8aada1a5aec889e8`  
		Last Modified: Wed, 10 Apr 2024 01:34:47 GMT  
		Size: 255.6 KB (255649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5ba249752b259ec30317e6d9be24c9ae184897a3f96774f0a1f61fa6f8c196`  
		Last Modified: Wed, 10 Apr 2024 01:36:59 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc595e8d9ffdc13e2a491f83d29bbcf6e4fbbc1872cdf9b6d33156900f593be`  
		Last Modified: Wed, 10 Apr 2024 01:37:20 GMT  
		Size: 69.3 MB (69339784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9666572ffef44cedd89a1bf02be297824dcbb0e1db30b6f9a52cf06b09d181a0`  
		Last Modified: Wed, 10 Apr 2024 01:36:59 GMT  
		Size: 1.6 KB (1566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474f61eee778c75a6072d92f90f33cb8c3ba21ea0eded3d3a82ff35a91a50864`  
		Last Modified: Wed, 10 Apr 2024 04:40:31 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2f4771e42fee7692dd61c00fd5b5d18d7d8130854ee6dd737e581fc1ed2763`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86a9ad5c8f8b619270cd40a575f612322b7315fdf2105e6397a45d3707de156`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b4a4ffb9e9f9938b9bd40929d0422b0b5c111eba84c460246a970170261047`  
		Last Modified: Wed, 10 Apr 2024 04:40:28 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328e4a9a7a4cffe0480ebc46c068396be1a07000e05c24701ee9f2adf7e13cd3`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.7 MB (1656674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222acab8b494945e613aea2cd196dcf87a6f607c426f4d8a77b721a5c3ccb00b`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:390a1ca91ca1409e1ddd37368179b927e08a5076b250132ee200be24319015bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261258422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc64e898993fdebf28e22269619414d6e7fed095f21d000c00b8d70339b915b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:10:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Apr 2024 01:10:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Apr 2024 01:10:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Apr 2024 01:10:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Apr 2024 01:12:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:12:15 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:13:36 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 01:25:25 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 10 Apr 2024 01:29:01 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:29:02 GMT
WORKDIR C:\go
# Wed, 10 Apr 2024 02:00:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 02:00:57 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 10 Apr 2024 02:00:58 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:00:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Apr 2024 02:02:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Apr 2024 02:02:33 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843b97b1625fa02e123dfc05bebcf9f05077e6dbdd1f5253c3c6d07b95f0f55f`  
		Last Modified: Wed, 10 Apr 2024 01:35:25 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6532f7333203cbc41355f91a4431427f575a24ad3dc3dd393b4292b4c2660d76`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c34d692c7e9d5e97e4674c9fefa41e1c78447d2e9c8db3a3f94f325b6188af`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cead4e65b4492e37b01dc6043de135f9dfad18c9f01232c605eb59e7da4a98`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7638380d4eb3933d8241dfe83deaffc516e8bed7b2ab01f96b42864a0d722760`  
		Last Modified: Wed, 10 Apr 2024 01:35:27 GMT  
		Size: 25.5 MB (25535896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159dd7a1de12391b28b5260b6132a515d19e87a7e18b64d7bc843df2c26fb615`  
		Last Modified: Wed, 10 Apr 2024 01:35:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3004df08705794a49d57aabf8c97ae8dfe750cedd45eb476bd574ce29807e152`  
		Last Modified: Wed, 10 Apr 2024 01:35:21 GMT  
		Size: 263.3 KB (263307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4eb7e47773f01051ff8bed6e1e75760df109971229c7a276fc7299c77e1444`  
		Last Modified: Wed, 10 Apr 2024 01:37:33 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe828248e339ed1213f1728c3774b3fcbe81883eb47c39a77bded1d31b619866`  
		Last Modified: Wed, 10 Apr 2024 01:37:53 GMT  
		Size: 69.4 MB (69351371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0187d4b9bc619f6e5b9b6b4b45022d6f5f885398842d5e7b19103f3eff6d5d7d`  
		Last Modified: Wed, 10 Apr 2024 01:37:33 GMT  
		Size: 1.5 KB (1546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6320d39f2704b0c1762e0721121d0880c199f6dfe049f437c31318022f8d00d2`  
		Last Modified: Wed, 10 Apr 2024 04:40:13 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305f4502d0cf4a9a57015ac8a097d5f6636708172c5a249cdf37f4b7b5c2dfe2`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45625e4d8a700993f0fb347856d0df08e31374fca8b1a737332323ff07cf8ca`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb3362bfb653595714774c2d1cce61d5a02893675414b7d23b462602a727f20`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db153c0587fdf29cfded01b1cd48082057e376ad8636a6a254d3cc5d030775ca`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.7 MB (1661731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c45da18daa8ebd71fd796480f9850e0e1df9ce87467e733d09a937d867e369`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder-alpine`

```console
$ docker pull caddy@sha256:481c3357e533d892e2621d69ce3747a459e40af2f56159bcbd64b38bee1aa5bd
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
$ docker pull caddy@sha256:a925804363a91c2468468c2ab1c1de2c770fe02812a21b1bdc1e9d8d65a5241b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75406613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acc712a703abf58b426c0681a4f724105efc534e813fca8d7e1769f2df5ebfe`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
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
# Wed, 03 Apr 2024 20:22:32 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 20:22:32 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 20:22:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 20:22:34 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 20:22:34 GMT
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
	-	`sha256:d72bd013141c752021b5b309e9868c02341e86fc25f37a89ccec1311ad14b2fd`  
		Last Modified: Wed, 03 Apr 2024 17:01:10 GMT  
		Size: 65.8 MB (65766638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abea289abae69e0933683886761310d242609c9941f5964366d9fb5bae890969`  
		Last Modified: Wed, 03 Apr 2024 17:00:57 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c466f5631c550594140cdcbad1c11c2549f51578de8dbf2181ab68d36e3860`  
		Last Modified: Wed, 03 Apr 2024 20:22:50 GMT  
		Size: 5.0 MB (4958760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c206e1c4695681bec33b38b6cb25bc40da76dd756937418fda1f1841f07a6b`  
		Last Modified: Wed, 03 Apr 2024 20:22:49 GMT  
		Size: 1.2 MB (1248664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1617709771cc71f393f3e93e93292a3024d9ec67376e73101934b6f2d2a14c`  
		Last Modified: Wed, 03 Apr 2024 20:22:48 GMT  
		Size: 406.0 B  
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
$ docker pull caddy@sha256:737e66da3299a8c95988bbf4d40a3c4598cca4f803e9a27e3a7bd8fa63b109c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `caddy:2.7.6-builder-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:390a1ca91ca1409e1ddd37368179b927e08a5076b250132ee200be24319015bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261258422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc64e898993fdebf28e22269619414d6e7fed095f21d000c00b8d70339b915b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:10:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Apr 2024 01:10:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Apr 2024 01:10:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Apr 2024 01:10:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Apr 2024 01:12:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:12:15 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:13:36 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 01:25:25 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 10 Apr 2024 01:29:01 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:29:02 GMT
WORKDIR C:\go
# Wed, 10 Apr 2024 02:00:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 02:00:57 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 10 Apr 2024 02:00:58 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:00:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Apr 2024 02:02:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Apr 2024 02:02:33 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843b97b1625fa02e123dfc05bebcf9f05077e6dbdd1f5253c3c6d07b95f0f55f`  
		Last Modified: Wed, 10 Apr 2024 01:35:25 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6532f7333203cbc41355f91a4431427f575a24ad3dc3dd393b4292b4c2660d76`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c34d692c7e9d5e97e4674c9fefa41e1c78447d2e9c8db3a3f94f325b6188af`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cead4e65b4492e37b01dc6043de135f9dfad18c9f01232c605eb59e7da4a98`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7638380d4eb3933d8241dfe83deaffc516e8bed7b2ab01f96b42864a0d722760`  
		Last Modified: Wed, 10 Apr 2024 01:35:27 GMT  
		Size: 25.5 MB (25535896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159dd7a1de12391b28b5260b6132a515d19e87a7e18b64d7bc843df2c26fb615`  
		Last Modified: Wed, 10 Apr 2024 01:35:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3004df08705794a49d57aabf8c97ae8dfe750cedd45eb476bd574ce29807e152`  
		Last Modified: Wed, 10 Apr 2024 01:35:21 GMT  
		Size: 263.3 KB (263307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4eb7e47773f01051ff8bed6e1e75760df109971229c7a276fc7299c77e1444`  
		Last Modified: Wed, 10 Apr 2024 01:37:33 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe828248e339ed1213f1728c3774b3fcbe81883eb47c39a77bded1d31b619866`  
		Last Modified: Wed, 10 Apr 2024 01:37:53 GMT  
		Size: 69.4 MB (69351371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0187d4b9bc619f6e5b9b6b4b45022d6f5f885398842d5e7b19103f3eff6d5d7d`  
		Last Modified: Wed, 10 Apr 2024 01:37:33 GMT  
		Size: 1.5 KB (1546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6320d39f2704b0c1762e0721121d0880c199f6dfe049f437c31318022f8d00d2`  
		Last Modified: Wed, 10 Apr 2024 04:40:13 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305f4502d0cf4a9a57015ac8a097d5f6636708172c5a249cdf37f4b7b5c2dfe2`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45625e4d8a700993f0fb347856d0df08e31374fca8b1a737332323ff07cf8ca`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb3362bfb653595714774c2d1cce61d5a02893675414b7d23b462602a727f20`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db153c0587fdf29cfded01b1cd48082057e376ad8636a6a254d3cc5d030775ca`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.7 MB (1661731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c45da18daa8ebd71fd796480f9850e0e1df9ce87467e733d09a937d867e369`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:5803daadce4687e1b203ced81b669960c05ad08be85e392562ecaba8efd6a48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `caddy:2.7.6-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:dd65119faf3e9848dfe903b2d36c44473682ef85d053853873e864f46e68a3f7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2096172662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf83f7bc549933a30beb62be150c320ee6ee873beb730199fe7c91d066d7b9cc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:06:58 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Apr 2024 01:06:59 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Apr 2024 01:06:59 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Apr 2024 01:07:00 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Apr 2024 01:07:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:07:38 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:07:59 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 01:22:55 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 10 Apr 2024 01:25:11 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:25:13 GMT
WORKDIR C:\go
# Wed, 10 Apr 2024 02:02:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 02:02:41 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 10 Apr 2024 02:02:42 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:02:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Apr 2024 02:03:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Apr 2024 02:03:12 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5ca144c62db12ea36d3f00f6640c6e4758e616b730c3d993fb57c3c8ebad9`  
		Last Modified: Wed, 10 Apr 2024 01:34:50 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d031792c46321e7a0a81f081515ffa50d7c86201a35780d03b0a1a0ecd68ebac`  
		Last Modified: Wed, 10 Apr 2024 01:34:49 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91b14b8df5887a0feab0adbfcf0dea95d1aab9c3e32619bf6ec5bdc4971a9a4`  
		Last Modified: Wed, 10 Apr 2024 01:34:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099fb3ff689379a9da8dc64f6c1c8d941fb9f0cf66715dc1af16055bdb8e63ec`  
		Last Modified: Wed, 10 Apr 2024 01:34:48 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ca11c05a0028bb84d4b2b76249dfcce87ea1f22340e50e79681c2055ee1d27`  
		Last Modified: Wed, 10 Apr 2024 01:34:54 GMT  
		Size: 25.5 MB (25528844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587f661259fd2478a26bea01012713bd3afd154dfc37f4aafd87ca98d67f75b7`  
		Last Modified: Wed, 10 Apr 2024 01:34:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5830a087830d60f2ed8f1cf87fba9d92cdf7706d61f7692f8aada1a5aec889e8`  
		Last Modified: Wed, 10 Apr 2024 01:34:47 GMT  
		Size: 255.6 KB (255649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5ba249752b259ec30317e6d9be24c9ae184897a3f96774f0a1f61fa6f8c196`  
		Last Modified: Wed, 10 Apr 2024 01:36:59 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc595e8d9ffdc13e2a491f83d29bbcf6e4fbbc1872cdf9b6d33156900f593be`  
		Last Modified: Wed, 10 Apr 2024 01:37:20 GMT  
		Size: 69.3 MB (69339784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9666572ffef44cedd89a1bf02be297824dcbb0e1db30b6f9a52cf06b09d181a0`  
		Last Modified: Wed, 10 Apr 2024 01:36:59 GMT  
		Size: 1.6 KB (1566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474f61eee778c75a6072d92f90f33cb8c3ba21ea0eded3d3a82ff35a91a50864`  
		Last Modified: Wed, 10 Apr 2024 04:40:31 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2f4771e42fee7692dd61c00fd5b5d18d7d8130854ee6dd737e581fc1ed2763`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86a9ad5c8f8b619270cd40a575f612322b7315fdf2105e6397a45d3707de156`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b4a4ffb9e9f9938b9bd40929d0422b0b5c111eba84c460246a970170261047`  
		Last Modified: Wed, 10 Apr 2024 04:40:28 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328e4a9a7a4cffe0480ebc46c068396be1a07000e05c24701ee9f2adf7e13cd3`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.7 MB (1656674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222acab8b494945e613aea2cd196dcf87a6f607c426f4d8a77b721a5c3ccb00b`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-windowsservercore`

```console
$ docker pull caddy@sha256:399999da333b248fef2da843177c302602a2e3f939228d52df499d197ea08cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `caddy:2.7.6-windowsservercore` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:b4de45abdf801e6fe4e627d4a9146c7f3822666f9795f1fe35921da33d3b5920
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2015415021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1c537b274bb6928ea6772a745ddf910765f287696f3d596a64a2aef5bb3a49`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:59:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:59:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:00:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 02:00:12 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 02:00:13 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 02:00:13 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 02:00:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 02:00:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 02:00:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 02:00:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 02:00:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 02:00:20 GMT
EXPOSE 80
# Wed, 10 Apr 2024 02:00:21 GMT
EXPOSE 443
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 02:00:42 GMT
RUN caddy version
# Wed, 10 Apr 2024 02:00:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9cb628e4a7ceb9e124a728aba733c7b7837d0fe602c1af1c86af5ba7db1afe`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 462.4 KB (462386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe6244a1b7fd00d56255f78e7951d14811b06f10e069d90e75458e8f5198d6a`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fd5220e89ae5a44a14c920f948c28b3238c83307ad30f5955882930d72a23b`  
		Last Modified: Wed, 10 Apr 2024 04:39:56 GMT  
		Size: 15.3 MB (15272884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8711ac4c34fb1beb0cb9e799010a337864f252ea20a91c74e9ffb9dc4dd8f4`  
		Last Modified: Wed, 10 Apr 2024 04:39:52 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1bffa02c717094b56095d1f166aa11c19ba43f7481d7673313c862126f3434`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e554dc514103b8d140d5ab4e9437abe3875ce416cd9a69161836f9676d14b650`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f583dd206e697664bb89b8647ac1fe5d98933b1d6540b249433dae65d02dd09`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35fa3d4abc62509fa7c8c8b31d11482d23090a1f7e45393d43cbde05d0cd7e9`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254f688302923c46000c0526a060b43160db4d9314cbd342a3fc31620052ceaa`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e052187f5af8dbfaa36325485d886d7d47bbe36c18a5789d95efea81dfbf12`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea08dd4e4a398c33acb70cc8863ba300fad5cbf499840ed420b14ce06717f83`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc50e94c9c5e82f27b76ddd1796de52ee67ba64c275a531ee0d38c08757baf9e`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af1603a6bd4dacbf08b4c974a5db996c73e892cbe440e2d5339aa355847e5a0`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaaeba50589b199d8e988596dada19daaec59e8b26f7835e17a29fff8ac88f7`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b4695f6c339c5917ad1b57b3db1345b8cc1ac6b4e03d56d5f1de12f8e249a2`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d5e030bf8b034231beb875dd3a70af4fcf82b6350b60b23a72cef369792a29`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9280f84d3173ce915aa30f755697f993ca2d484caa9f8cd42334927563008d`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e2de6ed998eca032f334174172a69a2345072eda08fddd105b73a6e6238c81`  
		Last Modified: Wed, 10 Apr 2024 04:39:47 GMT  
		Size: 282.0 KB (282045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426ed15821e9616ced2fee524860d8e5554c359d0332601d4e035474c8a54964`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-windowsservercore` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:650f5144a6e8b1d947f54c017a1002956e096891718dc7edf9aa8661be3f82ce
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2180450650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e356a94cf89f9d5eb0399e9f2ae7bbba82bc08e09f5dbc1d964352dfa2497f34`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:55:53 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:55:54 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 01:57:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 01:57:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 01:57:26 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 01:57:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 01:57:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 01:57:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 01:57:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 01:57:33 GMT
EXPOSE 80
# Wed, 10 Apr 2024 01:57:34 GMT
EXPOSE 443
# Wed, 10 Apr 2024 01:57:35 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 01:57:36 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 01:58:56 GMT
RUN caddy version
# Wed, 10 Apr 2024 01:58:57 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218ffc757feed37e26b36ff35084f4357219272c3ef8ce663a0db97763750bec`  
		Last Modified: Wed, 10 Apr 2024 04:39:29 GMT  
		Size: 465.0 KB (465007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f41e339dc34abe966a19ca999fece15bcf0a5e9eb2d36d4d42b84482e8e2ba`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac8e68361bdc1deb2d5d4e50f2da825b25f026f558a03aeeba18d6c7665e654`  
		Last Modified: Wed, 10 Apr 2024 04:39:32 GMT  
		Size: 15.3 MB (15281747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05561518ae50169e6e15468669f8195d9b2ee80d945dd94c107d20afda067318`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0720408b82b77dc7b0d925d39741de50fe2f9139768729af189a0f783b43519b`  
		Last Modified: Wed, 10 Apr 2024 04:39:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d8585bb3ff3b6a72b43181fc6df1c46ce88f6393295f32d2315e71c85e7295`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177da9a277ef013596e849aa2ea825a25dddcec2db12d81c6a4ab6fa02e77e57`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4686dffa2d26bcedea0a3b07e3d11640141e4a3888ddca8fc167fce49a67e102`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7411e6d276896da1fd4087fb7dbbe4e2169637862d1bee25144443263947ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966957575920790399f90fd33923b9cb27715dc7dd38e430480922326f86e953`  
		Last Modified: Wed, 10 Apr 2024 04:39:25 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa479db7e2e01c3cdda82927bbd2250f6933c5e4f6d67f09b4f090c26df209ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173767522133c716cc5b0c32c5c8778faa06e95a3933bab867e4569bb468420`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a488b5ddbaaac25b5ac6ce9375b9c9eb44e109874b5cd47d7f6591a446084bb`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27825614feb810c19f64b918a625f414d9f32098460aefcc9dad624bd2be669`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcc1e73eb545e48d76e61fd1029ab3a682c27085f1b3d23b2e7be300cd8eca8`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2713b7318664d7438093b75892a477ec691872f2c8fb13408d4d27d9bddd9`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce420a03b259096e6668f2765ce31ad5694523c86afe5c81bc0277d8b2bc861`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7baa1c6f084d5ad95cabb52b0d9aaed5e906928249958cb374cf25fe5e51e921`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 253.5 KB (253500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d599502ec7d608e46d6398aebafdee3aea525c5a3a58d826220dd06d128bb939`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-windowsservercore-1809`

```console
$ docker pull caddy@sha256:7c607664734ef3b7e94195c98f76a77c5be5ef8134d490741cf848306b1dbb4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `caddy:2.7.6-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:650f5144a6e8b1d947f54c017a1002956e096891718dc7edf9aa8661be3f82ce
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2180450650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e356a94cf89f9d5eb0399e9f2ae7bbba82bc08e09f5dbc1d964352dfa2497f34`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:55:53 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:55:54 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 01:57:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 01:57:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 01:57:26 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 01:57:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 01:57:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 01:57:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 01:57:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 01:57:33 GMT
EXPOSE 80
# Wed, 10 Apr 2024 01:57:34 GMT
EXPOSE 443
# Wed, 10 Apr 2024 01:57:35 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 01:57:36 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 01:58:56 GMT
RUN caddy version
# Wed, 10 Apr 2024 01:58:57 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218ffc757feed37e26b36ff35084f4357219272c3ef8ce663a0db97763750bec`  
		Last Modified: Wed, 10 Apr 2024 04:39:29 GMT  
		Size: 465.0 KB (465007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f41e339dc34abe966a19ca999fece15bcf0a5e9eb2d36d4d42b84482e8e2ba`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac8e68361bdc1deb2d5d4e50f2da825b25f026f558a03aeeba18d6c7665e654`  
		Last Modified: Wed, 10 Apr 2024 04:39:32 GMT  
		Size: 15.3 MB (15281747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05561518ae50169e6e15468669f8195d9b2ee80d945dd94c107d20afda067318`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0720408b82b77dc7b0d925d39741de50fe2f9139768729af189a0f783b43519b`  
		Last Modified: Wed, 10 Apr 2024 04:39:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d8585bb3ff3b6a72b43181fc6df1c46ce88f6393295f32d2315e71c85e7295`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177da9a277ef013596e849aa2ea825a25dddcec2db12d81c6a4ab6fa02e77e57`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4686dffa2d26bcedea0a3b07e3d11640141e4a3888ddca8fc167fce49a67e102`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7411e6d276896da1fd4087fb7dbbe4e2169637862d1bee25144443263947ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966957575920790399f90fd33923b9cb27715dc7dd38e430480922326f86e953`  
		Last Modified: Wed, 10 Apr 2024 04:39:25 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa479db7e2e01c3cdda82927bbd2250f6933c5e4f6d67f09b4f090c26df209ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173767522133c716cc5b0c32c5c8778faa06e95a3933bab867e4569bb468420`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a488b5ddbaaac25b5ac6ce9375b9c9eb44e109874b5cd47d7f6591a446084bb`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27825614feb810c19f64b918a625f414d9f32098460aefcc9dad624bd2be669`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcc1e73eb545e48d76e61fd1029ab3a682c27085f1b3d23b2e7be300cd8eca8`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2713b7318664d7438093b75892a477ec691872f2c8fb13408d4d27d9bddd9`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce420a03b259096e6668f2765ce31ad5694523c86afe5c81bc0277d8b2bc861`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7baa1c6f084d5ad95cabb52b0d9aaed5e906928249958cb374cf25fe5e51e921`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 253.5 KB (253500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d599502ec7d608e46d6398aebafdee3aea525c5a3a58d826220dd06d128bb939`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:e4749c1b0666aee331315ab98ffcab70c25aa1d1121f25f567c4278ae5d3f96c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `caddy:2.7.6-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:b4de45abdf801e6fe4e627d4a9146c7f3822666f9795f1fe35921da33d3b5920
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2015415021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1c537b274bb6928ea6772a745ddf910765f287696f3d596a64a2aef5bb3a49`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:59:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:59:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:00:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 02:00:12 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 02:00:13 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 02:00:13 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 02:00:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 02:00:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 02:00:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 02:00:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 02:00:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 02:00:20 GMT
EXPOSE 80
# Wed, 10 Apr 2024 02:00:21 GMT
EXPOSE 443
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 02:00:42 GMT
RUN caddy version
# Wed, 10 Apr 2024 02:00:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9cb628e4a7ceb9e124a728aba733c7b7837d0fe602c1af1c86af5ba7db1afe`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 462.4 KB (462386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe6244a1b7fd00d56255f78e7951d14811b06f10e069d90e75458e8f5198d6a`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fd5220e89ae5a44a14c920f948c28b3238c83307ad30f5955882930d72a23b`  
		Last Modified: Wed, 10 Apr 2024 04:39:56 GMT  
		Size: 15.3 MB (15272884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8711ac4c34fb1beb0cb9e799010a337864f252ea20a91c74e9ffb9dc4dd8f4`  
		Last Modified: Wed, 10 Apr 2024 04:39:52 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1bffa02c717094b56095d1f166aa11c19ba43f7481d7673313c862126f3434`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e554dc514103b8d140d5ab4e9437abe3875ce416cd9a69161836f9676d14b650`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f583dd206e697664bb89b8647ac1fe5d98933b1d6540b249433dae65d02dd09`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35fa3d4abc62509fa7c8c8b31d11482d23090a1f7e45393d43cbde05d0cd7e9`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254f688302923c46000c0526a060b43160db4d9314cbd342a3fc31620052ceaa`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e052187f5af8dbfaa36325485d886d7d47bbe36c18a5789d95efea81dfbf12`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea08dd4e4a398c33acb70cc8863ba300fad5cbf499840ed420b14ce06717f83`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc50e94c9c5e82f27b76ddd1796de52ee67ba64c275a531ee0d38c08757baf9e`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af1603a6bd4dacbf08b4c974a5db996c73e892cbe440e2d5339aa355847e5a0`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaaeba50589b199d8e988596dada19daaec59e8b26f7835e17a29fff8ac88f7`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b4695f6c339c5917ad1b57b3db1345b8cc1ac6b4e03d56d5f1de12f8e249a2`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d5e030bf8b034231beb875dd3a70af4fcf82b6350b60b23a72cef369792a29`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9280f84d3173ce915aa30f755697f993ca2d484caa9f8cd42334927563008d`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e2de6ed998eca032f334174172a69a2345072eda08fddd105b73a6e6238c81`  
		Last Modified: Wed, 10 Apr 2024 04:39:47 GMT  
		Size: 282.0 KB (282045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426ed15821e9616ced2fee524860d8e5554c359d0332601d4e035474c8a54964`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1416 bytes)  
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
$ docker pull caddy@sha256:d8a2ad006009b25b7017ab7190128cdd3a0fccee518f5b14fe6c749c6a6293b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

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
$ docker pull caddy@sha256:a925804363a91c2468468c2ab1c1de2c770fe02812a21b1bdc1e9d8d65a5241b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75406613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acc712a703abf58b426c0681a4f724105efc534e813fca8d7e1769f2df5ebfe`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
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
# Wed, 03 Apr 2024 20:22:32 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 20:22:32 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 20:22:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 20:22:34 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 20:22:34 GMT
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
	-	`sha256:d72bd013141c752021b5b309e9868c02341e86fc25f37a89ccec1311ad14b2fd`  
		Last Modified: Wed, 03 Apr 2024 17:01:10 GMT  
		Size: 65.8 MB (65766638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abea289abae69e0933683886761310d242609c9941f5964366d9fb5bae890969`  
		Last Modified: Wed, 03 Apr 2024 17:00:57 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c466f5631c550594140cdcbad1c11c2549f51578de8dbf2181ab68d36e3860`  
		Last Modified: Wed, 03 Apr 2024 20:22:50 GMT  
		Size: 5.0 MB (4958760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c206e1c4695681bec33b38b6cb25bc40da76dd756937418fda1f1841f07a6b`  
		Last Modified: Wed, 03 Apr 2024 20:22:49 GMT  
		Size: 1.2 MB (1248664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1617709771cc71f393f3e93e93292a3024d9ec67376e73101934b6f2d2a14c`  
		Last Modified: Wed, 03 Apr 2024 20:22:48 GMT  
		Size: 406.0 B  
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

### `caddy:builder` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:dd65119faf3e9848dfe903b2d36c44473682ef85d053853873e864f46e68a3f7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2096172662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf83f7bc549933a30beb62be150c320ee6ee873beb730199fe7c91d066d7b9cc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:06:58 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Apr 2024 01:06:59 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Apr 2024 01:06:59 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Apr 2024 01:07:00 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Apr 2024 01:07:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:07:38 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:07:59 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 01:22:55 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 10 Apr 2024 01:25:11 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:25:13 GMT
WORKDIR C:\go
# Wed, 10 Apr 2024 02:02:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 02:02:41 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 10 Apr 2024 02:02:42 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:02:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Apr 2024 02:03:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Apr 2024 02:03:12 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5ca144c62db12ea36d3f00f6640c6e4758e616b730c3d993fb57c3c8ebad9`  
		Last Modified: Wed, 10 Apr 2024 01:34:50 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d031792c46321e7a0a81f081515ffa50d7c86201a35780d03b0a1a0ecd68ebac`  
		Last Modified: Wed, 10 Apr 2024 01:34:49 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91b14b8df5887a0feab0adbfcf0dea95d1aab9c3e32619bf6ec5bdc4971a9a4`  
		Last Modified: Wed, 10 Apr 2024 01:34:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099fb3ff689379a9da8dc64f6c1c8d941fb9f0cf66715dc1af16055bdb8e63ec`  
		Last Modified: Wed, 10 Apr 2024 01:34:48 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ca11c05a0028bb84d4b2b76249dfcce87ea1f22340e50e79681c2055ee1d27`  
		Last Modified: Wed, 10 Apr 2024 01:34:54 GMT  
		Size: 25.5 MB (25528844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587f661259fd2478a26bea01012713bd3afd154dfc37f4aafd87ca98d67f75b7`  
		Last Modified: Wed, 10 Apr 2024 01:34:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5830a087830d60f2ed8f1cf87fba9d92cdf7706d61f7692f8aada1a5aec889e8`  
		Last Modified: Wed, 10 Apr 2024 01:34:47 GMT  
		Size: 255.6 KB (255649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5ba249752b259ec30317e6d9be24c9ae184897a3f96774f0a1f61fa6f8c196`  
		Last Modified: Wed, 10 Apr 2024 01:36:59 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc595e8d9ffdc13e2a491f83d29bbcf6e4fbbc1872cdf9b6d33156900f593be`  
		Last Modified: Wed, 10 Apr 2024 01:37:20 GMT  
		Size: 69.3 MB (69339784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9666572ffef44cedd89a1bf02be297824dcbb0e1db30b6f9a52cf06b09d181a0`  
		Last Modified: Wed, 10 Apr 2024 01:36:59 GMT  
		Size: 1.6 KB (1566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474f61eee778c75a6072d92f90f33cb8c3ba21ea0eded3d3a82ff35a91a50864`  
		Last Modified: Wed, 10 Apr 2024 04:40:31 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2f4771e42fee7692dd61c00fd5b5d18d7d8130854ee6dd737e581fc1ed2763`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86a9ad5c8f8b619270cd40a575f612322b7315fdf2105e6397a45d3707de156`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b4a4ffb9e9f9938b9bd40929d0422b0b5c111eba84c460246a970170261047`  
		Last Modified: Wed, 10 Apr 2024 04:40:28 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328e4a9a7a4cffe0480ebc46c068396be1a07000e05c24701ee9f2adf7e13cd3`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.7 MB (1656674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222acab8b494945e613aea2cd196dcf87a6f607c426f4d8a77b721a5c3ccb00b`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:390a1ca91ca1409e1ddd37368179b927e08a5076b250132ee200be24319015bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261258422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc64e898993fdebf28e22269619414d6e7fed095f21d000c00b8d70339b915b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:10:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Apr 2024 01:10:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Apr 2024 01:10:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Apr 2024 01:10:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Apr 2024 01:12:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:12:15 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:13:36 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 01:25:25 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 10 Apr 2024 01:29:01 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:29:02 GMT
WORKDIR C:\go
# Wed, 10 Apr 2024 02:00:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 02:00:57 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 10 Apr 2024 02:00:58 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:00:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Apr 2024 02:02:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Apr 2024 02:02:33 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843b97b1625fa02e123dfc05bebcf9f05077e6dbdd1f5253c3c6d07b95f0f55f`  
		Last Modified: Wed, 10 Apr 2024 01:35:25 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6532f7333203cbc41355f91a4431427f575a24ad3dc3dd393b4292b4c2660d76`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c34d692c7e9d5e97e4674c9fefa41e1c78447d2e9c8db3a3f94f325b6188af`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cead4e65b4492e37b01dc6043de135f9dfad18c9f01232c605eb59e7da4a98`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7638380d4eb3933d8241dfe83deaffc516e8bed7b2ab01f96b42864a0d722760`  
		Last Modified: Wed, 10 Apr 2024 01:35:27 GMT  
		Size: 25.5 MB (25535896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159dd7a1de12391b28b5260b6132a515d19e87a7e18b64d7bc843df2c26fb615`  
		Last Modified: Wed, 10 Apr 2024 01:35:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3004df08705794a49d57aabf8c97ae8dfe750cedd45eb476bd574ce29807e152`  
		Last Modified: Wed, 10 Apr 2024 01:35:21 GMT  
		Size: 263.3 KB (263307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4eb7e47773f01051ff8bed6e1e75760df109971229c7a276fc7299c77e1444`  
		Last Modified: Wed, 10 Apr 2024 01:37:33 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe828248e339ed1213f1728c3774b3fcbe81883eb47c39a77bded1d31b619866`  
		Last Modified: Wed, 10 Apr 2024 01:37:53 GMT  
		Size: 69.4 MB (69351371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0187d4b9bc619f6e5b9b6b4b45022d6f5f885398842d5e7b19103f3eff6d5d7d`  
		Last Modified: Wed, 10 Apr 2024 01:37:33 GMT  
		Size: 1.5 KB (1546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6320d39f2704b0c1762e0721121d0880c199f6dfe049f437c31318022f8d00d2`  
		Last Modified: Wed, 10 Apr 2024 04:40:13 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305f4502d0cf4a9a57015ac8a097d5f6636708172c5a249cdf37f4b7b5c2dfe2`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45625e4d8a700993f0fb347856d0df08e31374fca8b1a737332323ff07cf8ca`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb3362bfb653595714774c2d1cce61d5a02893675414b7d23b462602a727f20`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db153c0587fdf29cfded01b1cd48082057e376ad8636a6a254d3cc5d030775ca`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.7 MB (1661731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c45da18daa8ebd71fd796480f9850e0e1df9ce87467e733d09a937d867e369`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:481c3357e533d892e2621d69ce3747a459e40af2f56159bcbd64b38bee1aa5bd
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
$ docker pull caddy@sha256:a925804363a91c2468468c2ab1c1de2c770fe02812a21b1bdc1e9d8d65a5241b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75406613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acc712a703abf58b426c0681a4f724105efc534e813fca8d7e1769f2df5ebfe`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
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
# Wed, 03 Apr 2024 20:22:32 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 03 Apr 2024 20:22:32 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Apr 2024 20:22:32 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Apr 2024 20:22:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 03 Apr 2024 20:22:34 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 03 Apr 2024 20:22:34 GMT
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
	-	`sha256:d72bd013141c752021b5b309e9868c02341e86fc25f37a89ccec1311ad14b2fd`  
		Last Modified: Wed, 03 Apr 2024 17:01:10 GMT  
		Size: 65.8 MB (65766638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abea289abae69e0933683886761310d242609c9941f5964366d9fb5bae890969`  
		Last Modified: Wed, 03 Apr 2024 17:00:57 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c466f5631c550594140cdcbad1c11c2549f51578de8dbf2181ab68d36e3860`  
		Last Modified: Wed, 03 Apr 2024 20:22:50 GMT  
		Size: 5.0 MB (4958760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c206e1c4695681bec33b38b6cb25bc40da76dd756937418fda1f1841f07a6b`  
		Last Modified: Wed, 03 Apr 2024 20:22:49 GMT  
		Size: 1.2 MB (1248664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1617709771cc71f393f3e93e93292a3024d9ec67376e73101934b6f2d2a14c`  
		Last Modified: Wed, 03 Apr 2024 20:22:48 GMT  
		Size: 406.0 B  
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
$ docker pull caddy@sha256:737e66da3299a8c95988bbf4d40a3c4598cca4f803e9a27e3a7bd8fa63b109c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:390a1ca91ca1409e1ddd37368179b927e08a5076b250132ee200be24319015bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261258422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc64e898993fdebf28e22269619414d6e7fed095f21d000c00b8d70339b915b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:10:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Apr 2024 01:10:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Apr 2024 01:10:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Apr 2024 01:10:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Apr 2024 01:12:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:12:15 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:13:36 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 01:25:25 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 10 Apr 2024 01:29:01 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:29:02 GMT
WORKDIR C:\go
# Wed, 10 Apr 2024 02:00:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 02:00:57 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 10 Apr 2024 02:00:58 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:00:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Apr 2024 02:02:32 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Apr 2024 02:02:33 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843b97b1625fa02e123dfc05bebcf9f05077e6dbdd1f5253c3c6d07b95f0f55f`  
		Last Modified: Wed, 10 Apr 2024 01:35:25 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6532f7333203cbc41355f91a4431427f575a24ad3dc3dd393b4292b4c2660d76`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c34d692c7e9d5e97e4674c9fefa41e1c78447d2e9c8db3a3f94f325b6188af`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cead4e65b4492e37b01dc6043de135f9dfad18c9f01232c605eb59e7da4a98`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7638380d4eb3933d8241dfe83deaffc516e8bed7b2ab01f96b42864a0d722760`  
		Last Modified: Wed, 10 Apr 2024 01:35:27 GMT  
		Size: 25.5 MB (25535896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159dd7a1de12391b28b5260b6132a515d19e87a7e18b64d7bc843df2c26fb615`  
		Last Modified: Wed, 10 Apr 2024 01:35:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3004df08705794a49d57aabf8c97ae8dfe750cedd45eb476bd574ce29807e152`  
		Last Modified: Wed, 10 Apr 2024 01:35:21 GMT  
		Size: 263.3 KB (263307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4eb7e47773f01051ff8bed6e1e75760df109971229c7a276fc7299c77e1444`  
		Last Modified: Wed, 10 Apr 2024 01:37:33 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe828248e339ed1213f1728c3774b3fcbe81883eb47c39a77bded1d31b619866`  
		Last Modified: Wed, 10 Apr 2024 01:37:53 GMT  
		Size: 69.4 MB (69351371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0187d4b9bc619f6e5b9b6b4b45022d6f5f885398842d5e7b19103f3eff6d5d7d`  
		Last Modified: Wed, 10 Apr 2024 01:37:33 GMT  
		Size: 1.5 KB (1546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6320d39f2704b0c1762e0721121d0880c199f6dfe049f437c31318022f8d00d2`  
		Last Modified: Wed, 10 Apr 2024 04:40:13 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305f4502d0cf4a9a57015ac8a097d5f6636708172c5a249cdf37f4b7b5c2dfe2`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45625e4d8a700993f0fb347856d0df08e31374fca8b1a737332323ff07cf8ca`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb3362bfb653595714774c2d1cce61d5a02893675414b7d23b462602a727f20`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db153c0587fdf29cfded01b1cd48082057e376ad8636a6a254d3cc5d030775ca`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.7 MB (1661731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c45da18daa8ebd71fd796480f9850e0e1df9ce87467e733d09a937d867e369`  
		Last Modified: Wed, 10 Apr 2024 04:40:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:5803daadce4687e1b203ced81b669960c05ad08be85e392562ecaba8efd6a48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:dd65119faf3e9848dfe903b2d36c44473682ef85d053853873e864f46e68a3f7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2096172662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf83f7bc549933a30beb62be150c320ee6ee873beb730199fe7c91d066d7b9cc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:06:58 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Apr 2024 01:06:59 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Apr 2024 01:06:59 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Apr 2024 01:07:00 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Apr 2024 01:07:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:07:38 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:07:59 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 01:22:55 GMT
ENV GOLANG_VERSION=1.21.9
# Wed, 10 Apr 2024 01:25:11 GMT
RUN $url = 'https://dl.google.com/go/go1.21.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '7a365354362b05fa9cef4953bb86a4f028c90072f69fe54bec3af852e63378a3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:25:13 GMT
WORKDIR C:\go
# Wed, 10 Apr 2024 02:02:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 02:02:41 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 10 Apr 2024 02:02:42 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:02:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Apr 2024 02:03:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Apr 2024 02:03:12 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5ca144c62db12ea36d3f00f6640c6e4758e616b730c3d993fb57c3c8ebad9`  
		Last Modified: Wed, 10 Apr 2024 01:34:50 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d031792c46321e7a0a81f081515ffa50d7c86201a35780d03b0a1a0ecd68ebac`  
		Last Modified: Wed, 10 Apr 2024 01:34:49 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91b14b8df5887a0feab0adbfcf0dea95d1aab9c3e32619bf6ec5bdc4971a9a4`  
		Last Modified: Wed, 10 Apr 2024 01:34:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099fb3ff689379a9da8dc64f6c1c8d941fb9f0cf66715dc1af16055bdb8e63ec`  
		Last Modified: Wed, 10 Apr 2024 01:34:48 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ca11c05a0028bb84d4b2b76249dfcce87ea1f22340e50e79681c2055ee1d27`  
		Last Modified: Wed, 10 Apr 2024 01:34:54 GMT  
		Size: 25.5 MB (25528844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587f661259fd2478a26bea01012713bd3afd154dfc37f4aafd87ca98d67f75b7`  
		Last Modified: Wed, 10 Apr 2024 01:34:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5830a087830d60f2ed8f1cf87fba9d92cdf7706d61f7692f8aada1a5aec889e8`  
		Last Modified: Wed, 10 Apr 2024 01:34:47 GMT  
		Size: 255.6 KB (255649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5ba249752b259ec30317e6d9be24c9ae184897a3f96774f0a1f61fa6f8c196`  
		Last Modified: Wed, 10 Apr 2024 01:36:59 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc595e8d9ffdc13e2a491f83d29bbcf6e4fbbc1872cdf9b6d33156900f593be`  
		Last Modified: Wed, 10 Apr 2024 01:37:20 GMT  
		Size: 69.3 MB (69339784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9666572ffef44cedd89a1bf02be297824dcbb0e1db30b6f9a52cf06b09d181a0`  
		Last Modified: Wed, 10 Apr 2024 01:36:59 GMT  
		Size: 1.6 KB (1566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474f61eee778c75a6072d92f90f33cb8c3ba21ea0eded3d3a82ff35a91a50864`  
		Last Modified: Wed, 10 Apr 2024 04:40:31 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2f4771e42fee7692dd61c00fd5b5d18d7d8130854ee6dd737e581fc1ed2763`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86a9ad5c8f8b619270cd40a575f612322b7315fdf2105e6397a45d3707de156`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b4a4ffb9e9f9938b9bd40929d0422b0b5c111eba84c460246a970170261047`  
		Last Modified: Wed, 10 Apr 2024 04:40:28 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328e4a9a7a4cffe0480ebc46c068396be1a07000e05c24701ee9f2adf7e13cd3`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.7 MB (1656674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222acab8b494945e613aea2cd196dcf87a6f607c426f4d8a77b721a5c3ccb00b`  
		Last Modified: Wed, 10 Apr 2024 04:40:29 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:ca031cd33c788ebe467c94348400e5bf263178f9619f3993af8373f18681b8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

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

### `caddy:latest` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:b4de45abdf801e6fe4e627d4a9146c7f3822666f9795f1fe35921da33d3b5920
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2015415021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1c537b274bb6928ea6772a745ddf910765f287696f3d596a64a2aef5bb3a49`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:59:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:59:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:00:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 02:00:12 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 02:00:13 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 02:00:13 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 02:00:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 02:00:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 02:00:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 02:00:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 02:00:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 02:00:20 GMT
EXPOSE 80
# Wed, 10 Apr 2024 02:00:21 GMT
EXPOSE 443
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 02:00:42 GMT
RUN caddy version
# Wed, 10 Apr 2024 02:00:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9cb628e4a7ceb9e124a728aba733c7b7837d0fe602c1af1c86af5ba7db1afe`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 462.4 KB (462386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe6244a1b7fd00d56255f78e7951d14811b06f10e069d90e75458e8f5198d6a`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fd5220e89ae5a44a14c920f948c28b3238c83307ad30f5955882930d72a23b`  
		Last Modified: Wed, 10 Apr 2024 04:39:56 GMT  
		Size: 15.3 MB (15272884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8711ac4c34fb1beb0cb9e799010a337864f252ea20a91c74e9ffb9dc4dd8f4`  
		Last Modified: Wed, 10 Apr 2024 04:39:52 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1bffa02c717094b56095d1f166aa11c19ba43f7481d7673313c862126f3434`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e554dc514103b8d140d5ab4e9437abe3875ce416cd9a69161836f9676d14b650`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f583dd206e697664bb89b8647ac1fe5d98933b1d6540b249433dae65d02dd09`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35fa3d4abc62509fa7c8c8b31d11482d23090a1f7e45393d43cbde05d0cd7e9`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254f688302923c46000c0526a060b43160db4d9314cbd342a3fc31620052ceaa`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e052187f5af8dbfaa36325485d886d7d47bbe36c18a5789d95efea81dfbf12`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea08dd4e4a398c33acb70cc8863ba300fad5cbf499840ed420b14ce06717f83`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc50e94c9c5e82f27b76ddd1796de52ee67ba64c275a531ee0d38c08757baf9e`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af1603a6bd4dacbf08b4c974a5db996c73e892cbe440e2d5339aa355847e5a0`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaaeba50589b199d8e988596dada19daaec59e8b26f7835e17a29fff8ac88f7`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b4695f6c339c5917ad1b57b3db1345b8cc1ac6b4e03d56d5f1de12f8e249a2`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d5e030bf8b034231beb875dd3a70af4fcf82b6350b60b23a72cef369792a29`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9280f84d3173ce915aa30f755697f993ca2d484caa9f8cd42334927563008d`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e2de6ed998eca032f334174172a69a2345072eda08fddd105b73a6e6238c81`  
		Last Modified: Wed, 10 Apr 2024 04:39:47 GMT  
		Size: 282.0 KB (282045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426ed15821e9616ced2fee524860d8e5554c359d0332601d4e035474c8a54964`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:650f5144a6e8b1d947f54c017a1002956e096891718dc7edf9aa8661be3f82ce
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2180450650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e356a94cf89f9d5eb0399e9f2ae7bbba82bc08e09f5dbc1d964352dfa2497f34`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:55:53 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:55:54 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 01:57:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 01:57:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 01:57:26 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 01:57:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 01:57:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 01:57:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 01:57:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 01:57:33 GMT
EXPOSE 80
# Wed, 10 Apr 2024 01:57:34 GMT
EXPOSE 443
# Wed, 10 Apr 2024 01:57:35 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 01:57:36 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 01:58:56 GMT
RUN caddy version
# Wed, 10 Apr 2024 01:58:57 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218ffc757feed37e26b36ff35084f4357219272c3ef8ce663a0db97763750bec`  
		Last Modified: Wed, 10 Apr 2024 04:39:29 GMT  
		Size: 465.0 KB (465007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f41e339dc34abe966a19ca999fece15bcf0a5e9eb2d36d4d42b84482e8e2ba`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac8e68361bdc1deb2d5d4e50f2da825b25f026f558a03aeeba18d6c7665e654`  
		Last Modified: Wed, 10 Apr 2024 04:39:32 GMT  
		Size: 15.3 MB (15281747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05561518ae50169e6e15468669f8195d9b2ee80d945dd94c107d20afda067318`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0720408b82b77dc7b0d925d39741de50fe2f9139768729af189a0f783b43519b`  
		Last Modified: Wed, 10 Apr 2024 04:39:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d8585bb3ff3b6a72b43181fc6df1c46ce88f6393295f32d2315e71c85e7295`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177da9a277ef013596e849aa2ea825a25dddcec2db12d81c6a4ab6fa02e77e57`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4686dffa2d26bcedea0a3b07e3d11640141e4a3888ddca8fc167fce49a67e102`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7411e6d276896da1fd4087fb7dbbe4e2169637862d1bee25144443263947ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966957575920790399f90fd33923b9cb27715dc7dd38e430480922326f86e953`  
		Last Modified: Wed, 10 Apr 2024 04:39:25 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa479db7e2e01c3cdda82927bbd2250f6933c5e4f6d67f09b4f090c26df209ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173767522133c716cc5b0c32c5c8778faa06e95a3933bab867e4569bb468420`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a488b5ddbaaac25b5ac6ce9375b9c9eb44e109874b5cd47d7f6591a446084bb`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27825614feb810c19f64b918a625f414d9f32098460aefcc9dad624bd2be669`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcc1e73eb545e48d76e61fd1029ab3a682c27085f1b3d23b2e7be300cd8eca8`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2713b7318664d7438093b75892a477ec691872f2c8fb13408d4d27d9bddd9`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce420a03b259096e6668f2765ce31ad5694523c86afe5c81bc0277d8b2bc861`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7baa1c6f084d5ad95cabb52b0d9aaed5e906928249958cb374cf25fe5e51e921`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 253.5 KB (253500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d599502ec7d608e46d6398aebafdee3aea525c5a3a58d826220dd06d128bb939`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:399999da333b248fef2da843177c302602a2e3f939228d52df499d197ea08cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `caddy:windowsservercore` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:b4de45abdf801e6fe4e627d4a9146c7f3822666f9795f1fe35921da33d3b5920
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2015415021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1c537b274bb6928ea6772a745ddf910765f287696f3d596a64a2aef5bb3a49`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:59:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:59:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:00:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 02:00:12 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 02:00:13 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 02:00:13 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 02:00:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 02:00:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 02:00:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 02:00:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 02:00:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 02:00:20 GMT
EXPOSE 80
# Wed, 10 Apr 2024 02:00:21 GMT
EXPOSE 443
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 02:00:42 GMT
RUN caddy version
# Wed, 10 Apr 2024 02:00:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9cb628e4a7ceb9e124a728aba733c7b7837d0fe602c1af1c86af5ba7db1afe`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 462.4 KB (462386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe6244a1b7fd00d56255f78e7951d14811b06f10e069d90e75458e8f5198d6a`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fd5220e89ae5a44a14c920f948c28b3238c83307ad30f5955882930d72a23b`  
		Last Modified: Wed, 10 Apr 2024 04:39:56 GMT  
		Size: 15.3 MB (15272884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8711ac4c34fb1beb0cb9e799010a337864f252ea20a91c74e9ffb9dc4dd8f4`  
		Last Modified: Wed, 10 Apr 2024 04:39:52 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1bffa02c717094b56095d1f166aa11c19ba43f7481d7673313c862126f3434`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e554dc514103b8d140d5ab4e9437abe3875ce416cd9a69161836f9676d14b650`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f583dd206e697664bb89b8647ac1fe5d98933b1d6540b249433dae65d02dd09`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35fa3d4abc62509fa7c8c8b31d11482d23090a1f7e45393d43cbde05d0cd7e9`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254f688302923c46000c0526a060b43160db4d9314cbd342a3fc31620052ceaa`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e052187f5af8dbfaa36325485d886d7d47bbe36c18a5789d95efea81dfbf12`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea08dd4e4a398c33acb70cc8863ba300fad5cbf499840ed420b14ce06717f83`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc50e94c9c5e82f27b76ddd1796de52ee67ba64c275a531ee0d38c08757baf9e`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af1603a6bd4dacbf08b4c974a5db996c73e892cbe440e2d5339aa355847e5a0`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaaeba50589b199d8e988596dada19daaec59e8b26f7835e17a29fff8ac88f7`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b4695f6c339c5917ad1b57b3db1345b8cc1ac6b4e03d56d5f1de12f8e249a2`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d5e030bf8b034231beb875dd3a70af4fcf82b6350b60b23a72cef369792a29`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9280f84d3173ce915aa30f755697f993ca2d484caa9f8cd42334927563008d`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e2de6ed998eca032f334174172a69a2345072eda08fddd105b73a6e6238c81`  
		Last Modified: Wed, 10 Apr 2024 04:39:47 GMT  
		Size: 282.0 KB (282045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426ed15821e9616ced2fee524860d8e5554c359d0332601d4e035474c8a54964`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:650f5144a6e8b1d947f54c017a1002956e096891718dc7edf9aa8661be3f82ce
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2180450650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e356a94cf89f9d5eb0399e9f2ae7bbba82bc08e09f5dbc1d964352dfa2497f34`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:55:53 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:55:54 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 01:57:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 01:57:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 01:57:26 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 01:57:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 01:57:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 01:57:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 01:57:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 01:57:33 GMT
EXPOSE 80
# Wed, 10 Apr 2024 01:57:34 GMT
EXPOSE 443
# Wed, 10 Apr 2024 01:57:35 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 01:57:36 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 01:58:56 GMT
RUN caddy version
# Wed, 10 Apr 2024 01:58:57 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218ffc757feed37e26b36ff35084f4357219272c3ef8ce663a0db97763750bec`  
		Last Modified: Wed, 10 Apr 2024 04:39:29 GMT  
		Size: 465.0 KB (465007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f41e339dc34abe966a19ca999fece15bcf0a5e9eb2d36d4d42b84482e8e2ba`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac8e68361bdc1deb2d5d4e50f2da825b25f026f558a03aeeba18d6c7665e654`  
		Last Modified: Wed, 10 Apr 2024 04:39:32 GMT  
		Size: 15.3 MB (15281747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05561518ae50169e6e15468669f8195d9b2ee80d945dd94c107d20afda067318`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0720408b82b77dc7b0d925d39741de50fe2f9139768729af189a0f783b43519b`  
		Last Modified: Wed, 10 Apr 2024 04:39:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d8585bb3ff3b6a72b43181fc6df1c46ce88f6393295f32d2315e71c85e7295`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177da9a277ef013596e849aa2ea825a25dddcec2db12d81c6a4ab6fa02e77e57`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4686dffa2d26bcedea0a3b07e3d11640141e4a3888ddca8fc167fce49a67e102`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7411e6d276896da1fd4087fb7dbbe4e2169637862d1bee25144443263947ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966957575920790399f90fd33923b9cb27715dc7dd38e430480922326f86e953`  
		Last Modified: Wed, 10 Apr 2024 04:39:25 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa479db7e2e01c3cdda82927bbd2250f6933c5e4f6d67f09b4f090c26df209ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173767522133c716cc5b0c32c5c8778faa06e95a3933bab867e4569bb468420`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a488b5ddbaaac25b5ac6ce9375b9c9eb44e109874b5cd47d7f6591a446084bb`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27825614feb810c19f64b918a625f414d9f32098460aefcc9dad624bd2be669`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcc1e73eb545e48d76e61fd1029ab3a682c27085f1b3d23b2e7be300cd8eca8`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2713b7318664d7438093b75892a477ec691872f2c8fb13408d4d27d9bddd9`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce420a03b259096e6668f2765ce31ad5694523c86afe5c81bc0277d8b2bc861`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7baa1c6f084d5ad95cabb52b0d9aaed5e906928249958cb374cf25fe5e51e921`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 253.5 KB (253500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d599502ec7d608e46d6398aebafdee3aea525c5a3a58d826220dd06d128bb939`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:7c607664734ef3b7e94195c98f76a77c5be5ef8134d490741cf848306b1dbb4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:650f5144a6e8b1d947f54c017a1002956e096891718dc7edf9aa8661be3f82ce
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2180450650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e356a94cf89f9d5eb0399e9f2ae7bbba82bc08e09f5dbc1d964352dfa2497f34`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:55:53 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:55:54 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 01:57:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 01:57:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 01:57:26 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 01:57:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 01:57:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 01:57:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 01:57:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 01:57:33 GMT
EXPOSE 80
# Wed, 10 Apr 2024 01:57:34 GMT
EXPOSE 443
# Wed, 10 Apr 2024 01:57:35 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 01:57:36 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 01:58:56 GMT
RUN caddy version
# Wed, 10 Apr 2024 01:58:57 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218ffc757feed37e26b36ff35084f4357219272c3ef8ce663a0db97763750bec`  
		Last Modified: Wed, 10 Apr 2024 04:39:29 GMT  
		Size: 465.0 KB (465007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f41e339dc34abe966a19ca999fece15bcf0a5e9eb2d36d4d42b84482e8e2ba`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac8e68361bdc1deb2d5d4e50f2da825b25f026f558a03aeeba18d6c7665e654`  
		Last Modified: Wed, 10 Apr 2024 04:39:32 GMT  
		Size: 15.3 MB (15281747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05561518ae50169e6e15468669f8195d9b2ee80d945dd94c107d20afda067318`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0720408b82b77dc7b0d925d39741de50fe2f9139768729af189a0f783b43519b`  
		Last Modified: Wed, 10 Apr 2024 04:39:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d8585bb3ff3b6a72b43181fc6df1c46ce88f6393295f32d2315e71c85e7295`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177da9a277ef013596e849aa2ea825a25dddcec2db12d81c6a4ab6fa02e77e57`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4686dffa2d26bcedea0a3b07e3d11640141e4a3888ddca8fc167fce49a67e102`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7411e6d276896da1fd4087fb7dbbe4e2169637862d1bee25144443263947ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966957575920790399f90fd33923b9cb27715dc7dd38e430480922326f86e953`  
		Last Modified: Wed, 10 Apr 2024 04:39:25 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa479db7e2e01c3cdda82927bbd2250f6933c5e4f6d67f09b4f090c26df209ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173767522133c716cc5b0c32c5c8778faa06e95a3933bab867e4569bb468420`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a488b5ddbaaac25b5ac6ce9375b9c9eb44e109874b5cd47d7f6591a446084bb`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27825614feb810c19f64b918a625f414d9f32098460aefcc9dad624bd2be669`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcc1e73eb545e48d76e61fd1029ab3a682c27085f1b3d23b2e7be300cd8eca8`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2713b7318664d7438093b75892a477ec691872f2c8fb13408d4d27d9bddd9`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce420a03b259096e6668f2765ce31ad5694523c86afe5c81bc0277d8b2bc861`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7baa1c6f084d5ad95cabb52b0d9aaed5e906928249958cb374cf25fe5e51e921`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 253.5 KB (253500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d599502ec7d608e46d6398aebafdee3aea525c5a3a58d826220dd06d128bb939`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:e4749c1b0666aee331315ab98ffcab70c25aa1d1121f25f567c4278ae5d3f96c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:b4de45abdf801e6fe4e627d4a9146c7f3822666f9795f1fe35921da33d3b5920
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2015415021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1c537b274bb6928ea6772a745ddf910765f287696f3d596a64a2aef5bb3a49`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:59:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:59:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:00:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 02:00:12 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 02:00:13 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 02:00:13 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 02:00:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 02:00:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 02:00:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 02:00:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 02:00:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 02:00:20 GMT
EXPOSE 80
# Wed, 10 Apr 2024 02:00:21 GMT
EXPOSE 443
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 02:00:42 GMT
RUN caddy version
# Wed, 10 Apr 2024 02:00:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9cb628e4a7ceb9e124a728aba733c7b7837d0fe602c1af1c86af5ba7db1afe`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 462.4 KB (462386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe6244a1b7fd00d56255f78e7951d14811b06f10e069d90e75458e8f5198d6a`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fd5220e89ae5a44a14c920f948c28b3238c83307ad30f5955882930d72a23b`  
		Last Modified: Wed, 10 Apr 2024 04:39:56 GMT  
		Size: 15.3 MB (15272884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8711ac4c34fb1beb0cb9e799010a337864f252ea20a91c74e9ffb9dc4dd8f4`  
		Last Modified: Wed, 10 Apr 2024 04:39:52 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1bffa02c717094b56095d1f166aa11c19ba43f7481d7673313c862126f3434`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e554dc514103b8d140d5ab4e9437abe3875ce416cd9a69161836f9676d14b650`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f583dd206e697664bb89b8647ac1fe5d98933b1d6540b249433dae65d02dd09`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35fa3d4abc62509fa7c8c8b31d11482d23090a1f7e45393d43cbde05d0cd7e9`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254f688302923c46000c0526a060b43160db4d9314cbd342a3fc31620052ceaa`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e052187f5af8dbfaa36325485d886d7d47bbe36c18a5789d95efea81dfbf12`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea08dd4e4a398c33acb70cc8863ba300fad5cbf499840ed420b14ce06717f83`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc50e94c9c5e82f27b76ddd1796de52ee67ba64c275a531ee0d38c08757baf9e`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af1603a6bd4dacbf08b4c974a5db996c73e892cbe440e2d5339aa355847e5a0`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaaeba50589b199d8e988596dada19daaec59e8b26f7835e17a29fff8ac88f7`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b4695f6c339c5917ad1b57b3db1345b8cc1ac6b4e03d56d5f1de12f8e249a2`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d5e030bf8b034231beb875dd3a70af4fcf82b6350b60b23a72cef369792a29`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9280f84d3173ce915aa30f755697f993ca2d484caa9f8cd42334927563008d`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e2de6ed998eca032f334174172a69a2345072eda08fddd105b73a6e6238c81`  
		Last Modified: Wed, 10 Apr 2024 04:39:47 GMT  
		Size: 282.0 KB (282045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426ed15821e9616ced2fee524860d8e5554c359d0332601d4e035474c8a54964`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
