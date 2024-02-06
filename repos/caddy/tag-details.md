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
$ docker pull caddy@sha256:245e14283de7392fd14ef9e425580fe689cc0f8eedf28376016dab4109bc76b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `caddy:2` - linux; amd64

```console
$ docker pull caddy@sha256:67d0aa24ce021bee77049ddd2c0cc64732dd43d04598085ec39f950a13981bd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18467338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66978cebfbcc9c0a17709b108582a40a369c525c764e9a8882f6cae260b32f4d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:39:14 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 03:39:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 03:39:16 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:39:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 03:39:18 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 03:39:18 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 03:39:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 80
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 443
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 03:39:19 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 03:39:19 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf3211613d439d6da6e22998ce1ca109a902f861e1c1d55f59750636c8b7dc`  
		Last Modified: Sat, 27 Jan 2024 03:39:38 GMT  
		Size: 350.8 KB (350837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3505501083aeee1ff957f129e7d5dbdec0a32b80fee88cba62665e91547eeee0`  
		Last Modified: Sat, 27 Jan 2024 03:39:38 GMT  
		Size: 7.5 KB (7523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcbb25232b8128478b3c2ba4fe7e03fafdbf5024b74db396eef024b547f95ca`  
		Last Modified: Sat, 27 Jan 2024 03:39:40 GMT  
		Size: 14.7 MB (14706436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v6

```console
$ docker pull caddy@sha256:6fb5cfba87d2f8f1e7f89e7f61fad3a9e2ef76dc7f58aaffdf5af8997dc6dac4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17423230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3a842d1153c178390b3187d16d1ea0f4d691fd1c72bc5fd0a2ff32c6915a02`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:05:40 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 00:05:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 00:05:42 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:05:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 00:05:45 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 00:05:45 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 00:05:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 00:05:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 80
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 443
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 00:05:46 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 00:05:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a63a43f994064f0597fc36462d12376175178fc2c5486a9edcb36b198de411`  
		Last Modified: Sat, 27 Jan 2024 00:06:02 GMT  
		Size: 347.6 KB (347620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2327a8d9853b0ed7c134359a0fb7d0ea93d16621dd29a136c22bb30c59493703`  
		Last Modified: Sat, 27 Jan 2024 00:06:02 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71ff73f86184e48aa48d9298e97a824ab7316cc6134da0983587197e162a4d6`  
		Last Modified: Sat, 27 Jan 2024 00:06:04 GMT  
		Size: 13.9 MB (13921023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm variant v7

```console
$ docker pull caddy@sha256:56128992f412b5e862c705f3ea06a9e290a1caa484f80111556fb1f13c15ce16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17147114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71cfdc5faaa533682a397011b220a59fa9e54a42f98146bfb1080c102a0ebc86`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:44:33 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 00:44:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 00:44:35 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:44:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 00:44:41 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 00:44:41 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 00:44:42 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 00:44:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 00:44:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 00:44:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 00:44:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 00:44:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 00:44:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 00:44:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 00:44:44 GMT
EXPOSE 80
# Sat, 27 Jan 2024 00:44:45 GMT
EXPOSE 443
# Sat, 27 Jan 2024 00:44:45 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 00:44:46 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 00:44:46 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 00:44:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2a6e8e98d60ee548724a36c2a41ee2f4053b409052e45ab4b015360e73c808`  
		Last Modified: Sat, 27 Jan 2024 00:45:17 GMT  
		Size: 344.5 KB (344463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9afd4ba62ae2a5b6f5ffd0c7d900582f8e684b0d45670317b63e3b8f51dc9b`  
		Last Modified: Sat, 27 Jan 2024 00:45:17 GMT  
		Size: 7.5 KB (7527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b8e42e4efab7a06b51ee74ffac1bca9bf70812dd543cb7ab60135515565e13`  
		Last Modified: Sat, 27 Jan 2024 00:45:20 GMT  
		Size: 13.9 MB (13893732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:2ec95d40ce2d1f18f92eee012a5dd18b352075d92eb6c4f4e0ea18c46ad4b069
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09733d8f0611adb987aea99d5144981331f8b6de5c2397bef43678ba50066f4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:44:36 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 03:44:38 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 03:44:38 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:44:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 03:44:40 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 03:44:40 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 80
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 443
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 03:44:41 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 03:44:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8d53bc0303fbf7f349016b59b6ac8710ba2639505e276c3816ecca679bdac7`  
		Last Modified: Sat, 27 Jan 2024 03:44:57 GMT  
		Size: 360.7 KB (360652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764cd8cdd6e6b377bd4cd13dbb53eb18d9fc7e0045323401614398d5a85b9c65`  
		Last Modified: Sat, 27 Jan 2024 03:44:56 GMT  
		Size: 7.5 KB (7526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00acba9333616526f5fc17192a0abd4e29624bba1500c6068db189bdcbee5468`  
		Last Modified: Sat, 27 Jan 2024 03:44:58 GMT  
		Size: 13.6 MB (13568965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - linux; ppc64le

```console
$ docker pull caddy@sha256:53a5136ccffab422016068b77862678ad9b19430fc52f7e911188703d0123939
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17052070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9c424cec6fbefc3fd4578ed97634fbe37d2590a0e474a0dce3a35ff23a8352`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:48:34 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 00:48:36 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 00:48:36 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:48:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 00:48:41 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 00:48:41 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 00:48:42 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 00:48:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 00:48:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 00:48:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 00:48:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 00:48:44 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 00:48:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 00:48:45 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 00:48:45 GMT
EXPOSE 80
# Sat, 27 Jan 2024 00:48:46 GMT
EXPOSE 443
# Sat, 27 Jan 2024 00:48:46 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 00:48:47 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 00:48:47 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 00:48:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5469759827ceaac50f13afad48892591b541bff7fa92b64936e2059ba28db3`  
		Last Modified: Sat, 27 Jan 2024 00:49:05 GMT  
		Size: 362.2 KB (362186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2c06e0d1950f2257265e78e914ebe1d4e1b0cfbfc32ba881b844fd13beb05b`  
		Last Modified: Sat, 27 Jan 2024 00:49:05 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2689e7d4f2d85097f8a724b4e3e41a875ff392132743a088b133a4d6802f6238`  
		Last Modified: Sat, 27 Jan 2024 00:49:07 GMT  
		Size: 13.3 MB (13333868 bytes)  
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

### `caddy:2` - windows version 10.0.20348.2227; amd64

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

### `caddy:2` - windows version 10.0.17763.5329; amd64

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

## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:80ca561981768b2c3568cc4bef3d4cd1f11c2a625c806bedeb8453aef98779a0
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
$ docker pull caddy@sha256:67d0aa24ce021bee77049ddd2c0cc64732dd43d04598085ec39f950a13981bd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18467338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66978cebfbcc9c0a17709b108582a40a369c525c764e9a8882f6cae260b32f4d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:39:14 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 03:39:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 03:39:16 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:39:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 03:39:18 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 03:39:18 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 03:39:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 80
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 443
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 03:39:19 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 03:39:19 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf3211613d439d6da6e22998ce1ca109a902f861e1c1d55f59750636c8b7dc`  
		Last Modified: Sat, 27 Jan 2024 03:39:38 GMT  
		Size: 350.8 KB (350837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3505501083aeee1ff957f129e7d5dbdec0a32b80fee88cba62665e91547eeee0`  
		Last Modified: Sat, 27 Jan 2024 03:39:38 GMT  
		Size: 7.5 KB (7523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcbb25232b8128478b3c2ba4fe7e03fafdbf5024b74db396eef024b547f95ca`  
		Last Modified: Sat, 27 Jan 2024 03:39:40 GMT  
		Size: 14.7 MB (14706436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:6fb5cfba87d2f8f1e7f89e7f61fad3a9e2ef76dc7f58aaffdf5af8997dc6dac4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17423230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3a842d1153c178390b3187d16d1ea0f4d691fd1c72bc5fd0a2ff32c6915a02`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:05:40 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 00:05:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 00:05:42 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:05:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 00:05:45 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 00:05:45 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 00:05:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 00:05:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 80
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 443
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 00:05:46 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 00:05:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a63a43f994064f0597fc36462d12376175178fc2c5486a9edcb36b198de411`  
		Last Modified: Sat, 27 Jan 2024 00:06:02 GMT  
		Size: 347.6 KB (347620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2327a8d9853b0ed7c134359a0fb7d0ea93d16621dd29a136c22bb30c59493703`  
		Last Modified: Sat, 27 Jan 2024 00:06:02 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71ff73f86184e48aa48d9298e97a824ab7316cc6134da0983587197e162a4d6`  
		Last Modified: Sat, 27 Jan 2024 00:06:04 GMT  
		Size: 13.9 MB (13921023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:56128992f412b5e862c705f3ea06a9e290a1caa484f80111556fb1f13c15ce16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17147114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71cfdc5faaa533682a397011b220a59fa9e54a42f98146bfb1080c102a0ebc86`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:44:33 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 00:44:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 00:44:35 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:44:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 00:44:41 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 00:44:41 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 00:44:42 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 00:44:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 00:44:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 00:44:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 00:44:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 00:44:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 00:44:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 00:44:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 00:44:44 GMT
EXPOSE 80
# Sat, 27 Jan 2024 00:44:45 GMT
EXPOSE 443
# Sat, 27 Jan 2024 00:44:45 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 00:44:46 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 00:44:46 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 00:44:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2a6e8e98d60ee548724a36c2a41ee2f4053b409052e45ab4b015360e73c808`  
		Last Modified: Sat, 27 Jan 2024 00:45:17 GMT  
		Size: 344.5 KB (344463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9afd4ba62ae2a5b6f5ffd0c7d900582f8e684b0d45670317b63e3b8f51dc9b`  
		Last Modified: Sat, 27 Jan 2024 00:45:17 GMT  
		Size: 7.5 KB (7527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b8e42e4efab7a06b51ee74ffac1bca9bf70812dd543cb7ab60135515565e13`  
		Last Modified: Sat, 27 Jan 2024 00:45:20 GMT  
		Size: 13.9 MB (13893732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:2ec95d40ce2d1f18f92eee012a5dd18b352075d92eb6c4f4e0ea18c46ad4b069
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09733d8f0611adb987aea99d5144981331f8b6de5c2397bef43678ba50066f4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:44:36 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 03:44:38 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 03:44:38 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:44:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 03:44:40 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 03:44:40 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 80
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 443
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 03:44:41 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 03:44:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8d53bc0303fbf7f349016b59b6ac8710ba2639505e276c3816ecca679bdac7`  
		Last Modified: Sat, 27 Jan 2024 03:44:57 GMT  
		Size: 360.7 KB (360652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764cd8cdd6e6b377bd4cd13dbb53eb18d9fc7e0045323401614398d5a85b9c65`  
		Last Modified: Sat, 27 Jan 2024 03:44:56 GMT  
		Size: 7.5 KB (7526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00acba9333616526f5fc17192a0abd4e29624bba1500c6068db189bdcbee5468`  
		Last Modified: Sat, 27 Jan 2024 03:44:58 GMT  
		Size: 13.6 MB (13568965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:53a5136ccffab422016068b77862678ad9b19430fc52f7e911188703d0123939
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17052070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9c424cec6fbefc3fd4578ed97634fbe37d2590a0e474a0dce3a35ff23a8352`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:48:34 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 00:48:36 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 00:48:36 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:48:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 00:48:41 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 00:48:41 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 00:48:42 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 00:48:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 00:48:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 00:48:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 00:48:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 00:48:44 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 00:48:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 00:48:45 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 00:48:45 GMT
EXPOSE 80
# Sat, 27 Jan 2024 00:48:46 GMT
EXPOSE 443
# Sat, 27 Jan 2024 00:48:46 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 00:48:47 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 00:48:47 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 00:48:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5469759827ceaac50f13afad48892591b541bff7fa92b64936e2059ba28db3`  
		Last Modified: Sat, 27 Jan 2024 00:49:05 GMT  
		Size: 362.2 KB (362186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2c06e0d1950f2257265e78e914ebe1d4e1b0cfbfc32ba881b844fd13beb05b`  
		Last Modified: Sat, 27 Jan 2024 00:49:05 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2689e7d4f2d85097f8a724b4e3e41a875ff392132743a088b133a4d6802f6238`  
		Last Modified: Sat, 27 Jan 2024 00:49:07 GMT  
		Size: 13.3 MB (13333868 bytes)  
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
$ docker pull caddy@sha256:42442569a853bd5e5ce825d52baaee3fc919d1fa0e2fb7b9db30f246bec05c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:09513acee0757eaafeea861313a51d37b907cde693899b4d85bffa691d7eca06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77024166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e2950806b4846bc8384039f8e0ced6b55a43843627c3c7bcb574d00da87e36`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 03:39:23 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 03:39:23 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 03:39:24 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:39:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 03:39:24 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 03:39:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 03:39:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 03:39:25 GMT
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
	-	`sha256:c4b77ba268427b27996c293cddcbb1af065ac97d6f64fff6d3ee0adce318de44`  
		Last Modified: Sat, 27 Jan 2024 01:37:37 GMT  
		Size: 67.1 MB (67061623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5c147192a9317b4f575377244f4c3d96df9c9108d6147e10cd2becfdcfdc75`  
		Last Modified: Sat, 27 Jan 2024 01:37:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426789fa51aac91ce386d0cf62e3c5b4fd91cc19da6cb9449035a1aad2a1cb4b`  
		Last Modified: Sat, 27 Jan 2024 03:39:53 GMT  
		Size: 5.0 MB (4972458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848439cf5d4cf7d00a316abe8d0c04005a28d2e60f11875549cbbeec7db5cafc`  
		Last Modified: Sat, 27 Jan 2024 03:39:53 GMT  
		Size: 1.3 MB (1302243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61744c717cfe93977f876b739f3c692e919bb8cf098d233db8af67c532d77cd`  
		Last Modified: Sat, 27 Jan 2024 03:39:52 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:f7f15d8dc37358732c441ac4c62c2ac4967b16eb93863621dfc5cacf0b9dc1c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75479956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b694cc61283aebb38db78010935fc8281778bc08c35e7816a8c8819d3727a6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 13:22:00 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 13:22:00 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 13:22:00 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 13:22:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 13:22:01 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 13:22:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 13:22:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 13:22:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6033bb349d654a4ba7602191ed0372313ceca193751253005ad66a23d4dcb0ec`  
		Last Modified: Sat, 27 Jan 2024 09:20:38 GMT  
		Size: 284.9 KB (284872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31e5472cbeca7cc0b8f9272fbe547db898349f9b598c6b975f2c4efeeb63aee`  
		Last Modified: Sat, 27 Jan 2024 09:21:48 GMT  
		Size: 65.8 MB (65832091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b979a15e6ae0ded8491c78ec0740e6ece1aaaa584d10fdb89131c53427aba66`  
		Last Modified: Sat, 27 Jan 2024 09:21:32 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31abdea622b745b38e9215bf8062f71c377f48b2049bf07a5cd650743c069abb`  
		Last Modified: Sat, 27 Jan 2024 13:22:18 GMT  
		Size: 5.0 MB (4966664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f06e6a7ead4077a0b30ee09128ded6d14cd9bd7f450ef457f559c9e5b59938`  
		Last Modified: Sat, 27 Jan 2024 13:22:18 GMT  
		Size: 1.2 MB (1248661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba060f027200c3446f1acab0c00b2f4a9e8acf8610c46591daa3d8d7434aafd`  
		Last Modified: Sat, 27 Jan 2024 13:22:17 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:c80d0eabc3c5c1e92b026b7e2c2c35b4783472f984fe455da2ddddedce5b416c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25cc1ad71b8526356adff18f79ddbb3ff658a705a74e76800ee8f8172d4551f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 21:55:58 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:55:58 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:55:58 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:55:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:55:59 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:56:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:56:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:56:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf835181e2f4c73f7de0fe69c219658c3feddb5ba4e6850bc5b5af9555c08d1`  
		Last Modified: Sat, 27 Jan 2024 00:41:32 GMT  
		Size: 284.1 KB (284079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e2cd4f5b6025c32b2853d34aa0bcf57d85f2d44b2e412e2ba4e6dd0159ac1f`  
		Last Modified: Tue, 06 Feb 2024 21:29:51 GMT  
		Size: 65.8 MB (65767453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d160b5a79dd98fde6c0642c78daa3c77f077ad44a16b27b65a3b24fff23c603f`  
		Last Modified: Tue, 06 Feb 2024 21:29:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5735d56095a062d062dbd8c2d92cff873a457010035f0a7bf754444cdda79e1`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 4.5 MB (4514266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e601fac0470697a15f02c34e269f0e19119d88f46ffbcdddc5300417e3aab4b`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 1.2 MB (1246089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caff9a4e5a9e81ccc2e586bdbd72039b0d2bcc929751e08afbcffd6dbff11931`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:31f32db6814a94ad3cac5661dbda0a586162eb0b22b3e6ccdeb3e72b55cb9b76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73998584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c56aa1b8e6d877694eff62d87142b579cb7d523e8f22c16615b9ec3c5e3bae3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 21:33:04 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:33:04 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:33:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:33:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:33:06 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e59bef827dc10d9c33cdf4762faf3f2987df2a0296378e2349ec6d5bc6a37f4`  
		Last Modified: Sat, 27 Jan 2024 05:33:17 GMT  
		Size: 286.3 KB (286302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328d8fad75fb04ebff991b2c11c5988722931b5300239657bc1b4961655df05f`  
		Last Modified: Tue, 06 Feb 2024 20:50:08 GMT  
		Size: 64.1 MB (64109254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62899699addead1db84d09ab10dc0a0cbde16beb64c81cde0f84af2fa9b30f39`  
		Last Modified: Tue, 06 Feb 2024 20:50:00 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1745cea878add1608edd8710a879d4925a33b6e27329531c9c1cdd2c0e79c91a`  
		Last Modified: Tue, 06 Feb 2024 21:33:21 GMT  
		Size: 5.1 MB (5070613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235f6d9da6844caff2a0af124b9c01f0bf0abd2be340e5d2c67ab135a7cca76d`  
		Last Modified: Tue, 06 Feb 2024 21:33:21 GMT  
		Size: 1.2 MB (1198444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca8afc86b60749044b9b64230a9f9c67c20aa089b99562732169c4e6a807628`  
		Last Modified: Tue, 06 Feb 2024 21:33:20 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:b4effdad9be7ca7509b54d46638823940081fdf20f3000aaf9b3a691ace61f17
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74213039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10cf81cb43dc269c0ea9f820417d703e172313e228a17bdf7cffe96f4d2e742`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 21:14:22 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:14:22 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:14:23 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:14:23 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:14:24 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:14:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:14:27 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:14:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f92ca388ce06d6dddf0b5ad5ca0d5b82049994f1ad4da72bb5e48c5783dc009`  
		Last Modified: Sat, 27 Jan 2024 01:13:46 GMT  
		Size: 286.7 KB (286665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ef3661c7b713c28d8e0ae3c73dc823022f6a6e8a65c6fd2f00aa13dd6be4e4`  
		Last Modified: Tue, 06 Feb 2024 20:39:21 GMT  
		Size: 64.1 MB (64120440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7f0aa3654740d4016d469bad05baafdfc3be78e2f6ebc6f938501a1f4cd056`  
		Last Modified: Tue, 06 Feb 2024 20:39:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53242ccbc16994912810b389fdd1f7cb7cb1a3223cec7dcac1d4d00340e2f6de`  
		Last Modified: Tue, 06 Feb 2024 21:14:45 GMT  
		Size: 5.3 MB (5270660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c055ede766eec14283da8e4f87ab21f6a84f8ceff065d702bc31c9bf9ef23757`  
		Last Modified: Tue, 06 Feb 2024 21:14:45 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbe5c0b6966115344269e3c2b83ef21af0ebd897ee5a670604887f27d3da882`  
		Last Modified: Tue, 06 Feb 2024 21:14:44 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:25c4422b5cf06de48acecb96441e14f50db37a05c9353138f1f0f8b476680bb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76167035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06a921e90d95d0edd27e62d87f24a3fced554bde075b4b48f9099611fecb599`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 14:17:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 14:17:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 14:17:32 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 14:17:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 14:17:33 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 14:17:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 14:17:36 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 14:17:36 GMT
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
	-	`sha256:b94763531102ae1af628e5b55ca073b0c0fbd6aab9f221a28f3895303ddd975d`  
		Last Modified: Sat, 27 Jan 2024 05:47:26 GMT  
		Size: 66.3 MB (66284463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd03f53bee613b790f5b2286c4561428b2b2da6234df368a3a50d5ad91d58b9a`  
		Last Modified: Sat, 27 Jan 2024 05:47:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c299d55132b1737b4877e997f9881e05bd66727a05f8502f6fc38969031381ce`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 5.1 MB (5116950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60611bccc71deeef6872096a6f8a89a7e7af13c5027eb639b2ee7c182855d85`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 1.3 MB (1262387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fda9b2eed36da0393b2486d62a5c2c8ed03d6f3e38b27aae0fb6a57259b22e`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.20348.2227; amd64

```console
$ docker pull caddy@sha256:4814d63f1ac1d7e2334ff267279eed3b5533e0f94ad926fe9b3f11064e087406
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1997072166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d833851f7e1c400f60d5591428c91912a576258fb5b2fd93a0cdd0b228b07d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jan 2024 23:22:59 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Jan 2024 23:23:00 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Jan 2024 23:23:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Jan 2024 23:23:02 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Jan 2024 23:23:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Jan 2024 23:23:36 GMT
ENV GOPATH=C:\go
# Wed, 10 Jan 2024 23:23:55 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 Feb 2024 20:15:33 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 20:17:57 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 Feb 2024 20:17:58 GMT
WORKDIR C:\go
# Tue, 06 Feb 2024 21:01:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Feb 2024 21:01:18 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:01:19 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:01:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:01:44 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 06 Feb 2024 21:01:45 GMT
WORKDIR C:\
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
	-	`sha256:a3069ddb372bc0087899e61a271374e1b4423cfd9056ff2725874a89af15c2a1`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0841fad0c7557916603463fc9615983e0ad786338880d3d99c005dd50ecf3b6`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d1ae6fa2010fb779b06f0fc8a74830b01c9a87769fc35818fccdd5b7e7ea45`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4cd94fbe72557ed410a8f0aa0361ffc9ec2b2ecd96dc803b91c5ce0f34d077`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b3e385378ebc3f79f2c065897b323f0b1cfc97f3f8979c4530d0791e3e9523`  
		Last Modified: Thu, 11 Jan 2024 00:01:30 GMT  
		Size: 25.5 MB (25529890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbdf5bbf3fb6a215313abb55339dcee6260ef50d2c50d2b781476d5af12e840`  
		Last Modified: Thu, 11 Jan 2024 00:01:23 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7fd79e14c60629d3157a4363f602b919ba92aa10209a2e6ac40b7c86a75316`  
		Last Modified: Thu, 11 Jan 2024 00:01:23 GMT  
		Size: 261.7 KB (261737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d6abeee495b14ea2e44bb00f28c38212af6d923a1d5c148dd3eb083e1788d2`  
		Last Modified: Tue, 06 Feb 2024 20:38:27 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699b8adf45cf387aabdaea0b829e6bf5dee7a05e7eaf5519d3b0f5fe071e14a`  
		Last Modified: Tue, 06 Feb 2024 20:38:45 GMT  
		Size: 69.4 MB (69373765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd60a6e8aaafdd337241c619e2cd664dbfd6052a133b148c86845f227a25ea14`  
		Last Modified: Tue, 06 Feb 2024 20:38:27 GMT  
		Size: 1.5 KB (1531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6796689d52835dc674b67907c3e03bb20425e0e76be6963eaeb04e035d2c7f`  
		Last Modified: Tue, 06 Feb 2024 21:02:41 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657c487d0aab792a6141c8f2b5d1ef4564310178c60f883cb8e301cb752930ff`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bcd5a55d300a69a6a7202fda4cdb55a8e4f3645145c962279bc958c9efdf5a`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f9fc1b6232aab1694132043a6674117073dc98b00635546605582fabd31300`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005f7ea8d310ffb3ab0f46fbb75e4a90192f694357210b16fa4867a1c593cf2e`  
		Last Modified: Tue, 06 Feb 2024 21:02:39 GMT  
		Size: 1.7 MB (1675717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f756efa4d252460db4055d7da93b4667f4b1537f46882db730596bac57eb677`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.5329; amd64

```console
$ docker pull caddy@sha256:882f417e3efb3b9a8d1ade5245808ac22c5c1ea57a1352c72b6652b3a3238ecf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2166627810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6206308760870c6bbbd479176af11a35608423c94c08b69c418649ce2d281f3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jan 2024 23:26:43 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Jan 2024 23:26:44 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Jan 2024 23:26:45 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Jan 2024 23:26:46 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Jan 2024 23:28:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Jan 2024 23:28:09 GMT
ENV GOPATH=C:\go
# Wed, 10 Jan 2024 23:29:17 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 Feb 2024 20:18:16 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 20:21:36 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 Feb 2024 20:21:37 GMT
WORKDIR C:\go
# Tue, 06 Feb 2024 20:59:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Feb 2024 20:59:49 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 20:59:50 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 20:59:51 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:01:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 06 Feb 2024 21:01:01 GMT
WORKDIR C:\
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
	-	`sha256:58a2d0f9e9eca6932479b4446cdad2350fe376cd5102106ac4938d8552073ee1`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3baf188f2343abdd0b6b9307f8adcc91c698473839c28dbba9e3b50117d7df5`  
		Last Modified: Thu, 11 Jan 2024 00:03:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83f321def9731da0b67b8c9c7c573a95237ff9d906d16394dfc3dd845bd806`  
		Last Modified: Thu, 11 Jan 2024 00:03:01 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3185717e4484ba21a137fb6d471a72ee842364637f999013cbd8b7a633ccfa`  
		Last Modified: Thu, 11 Jan 2024 00:03:01 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d432d7f01be369829a69831b58f259bc1d30ccb67bc46a16211f95454e2d026b`  
		Last Modified: Thu, 11 Jan 2024 00:03:06 GMT  
		Size: 25.6 MB (25555277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481ab54aaa7ea3f3af1db424c6fda8a4bf6e63fe0bc92e2e319db55c66952d5`  
		Last Modified: Thu, 11 Jan 2024 00:02:59 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4579730b543c234b271242a1f8b94332944911daa12fe4493f4daad09e6e6a1`  
		Last Modified: Thu, 11 Jan 2024 00:02:59 GMT  
		Size: 284.0 KB (284031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57342fc3b749de0a8e32c9f1f9eece3c3855ea5d8b63b70682518058c40ba349`  
		Last Modified: Tue, 06 Feb 2024 20:38:59 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d092fd3744c0081064bac79e4fb322e2f6e9d0d8e744bb837bccd7f9b844e8`  
		Last Modified: Tue, 06 Feb 2024 20:39:17 GMT  
		Size: 69.4 MB (69370513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a8538533cb5606cc3e717f0431791fcd99ca7c1b935f5586f465bbd0c9d457`  
		Last Modified: Tue, 06 Feb 2024 20:38:59 GMT  
		Size: 1.6 KB (1586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ba50226998b42d6500ba479c1fbf0f3e588807488f728c91715ac893e69838`  
		Last Modified: Tue, 06 Feb 2024 21:02:24 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74292b50264f2db380dc5a9a8baaa5d229ff8efd2699e40fc6f478a25d59c0d0`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e574cef27624cb2b445968d4f051529c8c02dc6bf599ea131f51164de4939536`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14832cf23b08465f9e60489cda03b116fb6be01de86762232ed2f3b3aa8cf2a4`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e89456cebd7c16015a94dda1edb8a055ef730bc8c289b8eae13b1867371376f`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.7 MB (1677010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874ea9f0878170aeeae3da252653488f0677348bdb3f6cd9a87ccb3d064bde10`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:8a0f239bbd24b1a0973d0e3e22ef69d2e9f27b2f860c50247deead9c47b8b81e
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
$ docker pull caddy@sha256:09513acee0757eaafeea861313a51d37b907cde693899b4d85bffa691d7eca06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77024166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e2950806b4846bc8384039f8e0ced6b55a43843627c3c7bcb574d00da87e36`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 03:39:23 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 03:39:23 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 03:39:24 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:39:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 03:39:24 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 03:39:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 03:39:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 03:39:25 GMT
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
	-	`sha256:c4b77ba268427b27996c293cddcbb1af065ac97d6f64fff6d3ee0adce318de44`  
		Last Modified: Sat, 27 Jan 2024 01:37:37 GMT  
		Size: 67.1 MB (67061623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5c147192a9317b4f575377244f4c3d96df9c9108d6147e10cd2becfdcfdc75`  
		Last Modified: Sat, 27 Jan 2024 01:37:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426789fa51aac91ce386d0cf62e3c5b4fd91cc19da6cb9449035a1aad2a1cb4b`  
		Last Modified: Sat, 27 Jan 2024 03:39:53 GMT  
		Size: 5.0 MB (4972458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848439cf5d4cf7d00a316abe8d0c04005a28d2e60f11875549cbbeec7db5cafc`  
		Last Modified: Sat, 27 Jan 2024 03:39:53 GMT  
		Size: 1.3 MB (1302243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61744c717cfe93977f876b739f3c692e919bb8cf098d233db8af67c532d77cd`  
		Last Modified: Sat, 27 Jan 2024 03:39:52 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:f7f15d8dc37358732c441ac4c62c2ac4967b16eb93863621dfc5cacf0b9dc1c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75479956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b694cc61283aebb38db78010935fc8281778bc08c35e7816a8c8819d3727a6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 13:22:00 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 13:22:00 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 13:22:00 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 13:22:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 13:22:01 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 13:22:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 13:22:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 13:22:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6033bb349d654a4ba7602191ed0372313ceca193751253005ad66a23d4dcb0ec`  
		Last Modified: Sat, 27 Jan 2024 09:20:38 GMT  
		Size: 284.9 KB (284872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31e5472cbeca7cc0b8f9272fbe547db898349f9b598c6b975f2c4efeeb63aee`  
		Last Modified: Sat, 27 Jan 2024 09:21:48 GMT  
		Size: 65.8 MB (65832091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b979a15e6ae0ded8491c78ec0740e6ece1aaaa584d10fdb89131c53427aba66`  
		Last Modified: Sat, 27 Jan 2024 09:21:32 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31abdea622b745b38e9215bf8062f71c377f48b2049bf07a5cd650743c069abb`  
		Last Modified: Sat, 27 Jan 2024 13:22:18 GMT  
		Size: 5.0 MB (4966664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f06e6a7ead4077a0b30ee09128ded6d14cd9bd7f450ef457f559c9e5b59938`  
		Last Modified: Sat, 27 Jan 2024 13:22:18 GMT  
		Size: 1.2 MB (1248661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba060f027200c3446f1acab0c00b2f4a9e8acf8610c46591daa3d8d7434aafd`  
		Last Modified: Sat, 27 Jan 2024 13:22:17 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:c80d0eabc3c5c1e92b026b7e2c2c35b4783472f984fe455da2ddddedce5b416c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25cc1ad71b8526356adff18f79ddbb3ff658a705a74e76800ee8f8172d4551f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 21:55:58 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:55:58 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:55:58 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:55:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:55:59 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:56:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:56:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:56:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf835181e2f4c73f7de0fe69c219658c3feddb5ba4e6850bc5b5af9555c08d1`  
		Last Modified: Sat, 27 Jan 2024 00:41:32 GMT  
		Size: 284.1 KB (284079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e2cd4f5b6025c32b2853d34aa0bcf57d85f2d44b2e412e2ba4e6dd0159ac1f`  
		Last Modified: Tue, 06 Feb 2024 21:29:51 GMT  
		Size: 65.8 MB (65767453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d160b5a79dd98fde6c0642c78daa3c77f077ad44a16b27b65a3b24fff23c603f`  
		Last Modified: Tue, 06 Feb 2024 21:29:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5735d56095a062d062dbd8c2d92cff873a457010035f0a7bf754444cdda79e1`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 4.5 MB (4514266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e601fac0470697a15f02c34e269f0e19119d88f46ffbcdddc5300417e3aab4b`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 1.2 MB (1246089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caff9a4e5a9e81ccc2e586bdbd72039b0d2bcc929751e08afbcffd6dbff11931`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:31f32db6814a94ad3cac5661dbda0a586162eb0b22b3e6ccdeb3e72b55cb9b76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73998584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c56aa1b8e6d877694eff62d87142b579cb7d523e8f22c16615b9ec3c5e3bae3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 21:33:04 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:33:04 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:33:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:33:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:33:06 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e59bef827dc10d9c33cdf4762faf3f2987df2a0296378e2349ec6d5bc6a37f4`  
		Last Modified: Sat, 27 Jan 2024 05:33:17 GMT  
		Size: 286.3 KB (286302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328d8fad75fb04ebff991b2c11c5988722931b5300239657bc1b4961655df05f`  
		Last Modified: Tue, 06 Feb 2024 20:50:08 GMT  
		Size: 64.1 MB (64109254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62899699addead1db84d09ab10dc0a0cbde16beb64c81cde0f84af2fa9b30f39`  
		Last Modified: Tue, 06 Feb 2024 20:50:00 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1745cea878add1608edd8710a879d4925a33b6e27329531c9c1cdd2c0e79c91a`  
		Last Modified: Tue, 06 Feb 2024 21:33:21 GMT  
		Size: 5.1 MB (5070613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235f6d9da6844caff2a0af124b9c01f0bf0abd2be340e5d2c67ab135a7cca76d`  
		Last Modified: Tue, 06 Feb 2024 21:33:21 GMT  
		Size: 1.2 MB (1198444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca8afc86b60749044b9b64230a9f9c67c20aa089b99562732169c4e6a807628`  
		Last Modified: Tue, 06 Feb 2024 21:33:20 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:b4effdad9be7ca7509b54d46638823940081fdf20f3000aaf9b3a691ace61f17
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74213039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10cf81cb43dc269c0ea9f820417d703e172313e228a17bdf7cffe96f4d2e742`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 21:14:22 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:14:22 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:14:23 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:14:23 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:14:24 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:14:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:14:27 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:14:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f92ca388ce06d6dddf0b5ad5ca0d5b82049994f1ad4da72bb5e48c5783dc009`  
		Last Modified: Sat, 27 Jan 2024 01:13:46 GMT  
		Size: 286.7 KB (286665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ef3661c7b713c28d8e0ae3c73dc823022f6a6e8a65c6fd2f00aa13dd6be4e4`  
		Last Modified: Tue, 06 Feb 2024 20:39:21 GMT  
		Size: 64.1 MB (64120440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7f0aa3654740d4016d469bad05baafdfc3be78e2f6ebc6f938501a1f4cd056`  
		Last Modified: Tue, 06 Feb 2024 20:39:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53242ccbc16994912810b389fdd1f7cb7cb1a3223cec7dcac1d4d00340e2f6de`  
		Last Modified: Tue, 06 Feb 2024 21:14:45 GMT  
		Size: 5.3 MB (5270660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c055ede766eec14283da8e4f87ab21f6a84f8ceff065d702bc31c9bf9ef23757`  
		Last Modified: Tue, 06 Feb 2024 21:14:45 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbe5c0b6966115344269e3c2b83ef21af0ebd897ee5a670604887f27d3da882`  
		Last Modified: Tue, 06 Feb 2024 21:14:44 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:25c4422b5cf06de48acecb96441e14f50db37a05c9353138f1f0f8b476680bb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76167035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06a921e90d95d0edd27e62d87f24a3fced554bde075b4b48f9099611fecb599`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 14:17:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 14:17:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 14:17:32 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 14:17:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 14:17:33 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 14:17:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 14:17:36 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 14:17:36 GMT
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
	-	`sha256:b94763531102ae1af628e5b55ca073b0c0fbd6aab9f221a28f3895303ddd975d`  
		Last Modified: Sat, 27 Jan 2024 05:47:26 GMT  
		Size: 66.3 MB (66284463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd03f53bee613b790f5b2286c4561428b2b2da6234df368a3a50d5ad91d58b9a`  
		Last Modified: Sat, 27 Jan 2024 05:47:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c299d55132b1737b4877e997f9881e05bd66727a05f8502f6fc38969031381ce`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 5.1 MB (5116950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60611bccc71deeef6872096a6f8a89a7e7af13c5027eb639b2ee7c182855d85`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 1.3 MB (1262387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fda9b2eed36da0393b2486d62a5c2c8ed03d6f3e38b27aae0fb6a57259b22e`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:e794dda1d2a08c7fe472d7b929a4d86621c3ea9ac1252d7fe1134e724a2115a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull caddy@sha256:882f417e3efb3b9a8d1ade5245808ac22c5c1ea57a1352c72b6652b3a3238ecf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2166627810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6206308760870c6bbbd479176af11a35608423c94c08b69c418649ce2d281f3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jan 2024 23:26:43 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Jan 2024 23:26:44 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Jan 2024 23:26:45 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Jan 2024 23:26:46 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Jan 2024 23:28:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Jan 2024 23:28:09 GMT
ENV GOPATH=C:\go
# Wed, 10 Jan 2024 23:29:17 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 Feb 2024 20:18:16 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 20:21:36 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 Feb 2024 20:21:37 GMT
WORKDIR C:\go
# Tue, 06 Feb 2024 20:59:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Feb 2024 20:59:49 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 20:59:50 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 20:59:51 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:01:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 06 Feb 2024 21:01:01 GMT
WORKDIR C:\
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
	-	`sha256:58a2d0f9e9eca6932479b4446cdad2350fe376cd5102106ac4938d8552073ee1`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3baf188f2343abdd0b6b9307f8adcc91c698473839c28dbba9e3b50117d7df5`  
		Last Modified: Thu, 11 Jan 2024 00:03:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83f321def9731da0b67b8c9c7c573a95237ff9d906d16394dfc3dd845bd806`  
		Last Modified: Thu, 11 Jan 2024 00:03:01 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3185717e4484ba21a137fb6d471a72ee842364637f999013cbd8b7a633ccfa`  
		Last Modified: Thu, 11 Jan 2024 00:03:01 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d432d7f01be369829a69831b58f259bc1d30ccb67bc46a16211f95454e2d026b`  
		Last Modified: Thu, 11 Jan 2024 00:03:06 GMT  
		Size: 25.6 MB (25555277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481ab54aaa7ea3f3af1db424c6fda8a4bf6e63fe0bc92e2e319db55c66952d5`  
		Last Modified: Thu, 11 Jan 2024 00:02:59 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4579730b543c234b271242a1f8b94332944911daa12fe4493f4daad09e6e6a1`  
		Last Modified: Thu, 11 Jan 2024 00:02:59 GMT  
		Size: 284.0 KB (284031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57342fc3b749de0a8e32c9f1f9eece3c3855ea5d8b63b70682518058c40ba349`  
		Last Modified: Tue, 06 Feb 2024 20:38:59 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d092fd3744c0081064bac79e4fb322e2f6e9d0d8e744bb837bccd7f9b844e8`  
		Last Modified: Tue, 06 Feb 2024 20:39:17 GMT  
		Size: 69.4 MB (69370513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a8538533cb5606cc3e717f0431791fcd99ca7c1b935f5586f465bbd0c9d457`  
		Last Modified: Tue, 06 Feb 2024 20:38:59 GMT  
		Size: 1.6 KB (1586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ba50226998b42d6500ba479c1fbf0f3e588807488f728c91715ac893e69838`  
		Last Modified: Tue, 06 Feb 2024 21:02:24 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74292b50264f2db380dc5a9a8baaa5d229ff8efd2699e40fc6f478a25d59c0d0`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e574cef27624cb2b445968d4f051529c8c02dc6bf599ea131f51164de4939536`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14832cf23b08465f9e60489cda03b116fb6be01de86762232ed2f3b3aa8cf2a4`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e89456cebd7c16015a94dda1edb8a055ef730bc8c289b8eae13b1867371376f`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.7 MB (1677010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874ea9f0878170aeeae3da252653488f0677348bdb3f6cd9a87ccb3d064bde10`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:97e329cd72c287551121f0de0749affc40ba296a42f67b3774c972dfc63239d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull caddy@sha256:4814d63f1ac1d7e2334ff267279eed3b5533e0f94ad926fe9b3f11064e087406
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1997072166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d833851f7e1c400f60d5591428c91912a576258fb5b2fd93a0cdd0b228b07d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jan 2024 23:22:59 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Jan 2024 23:23:00 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Jan 2024 23:23:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Jan 2024 23:23:02 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Jan 2024 23:23:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Jan 2024 23:23:36 GMT
ENV GOPATH=C:\go
# Wed, 10 Jan 2024 23:23:55 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 Feb 2024 20:15:33 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 20:17:57 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 Feb 2024 20:17:58 GMT
WORKDIR C:\go
# Tue, 06 Feb 2024 21:01:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Feb 2024 21:01:18 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:01:19 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:01:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:01:44 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 06 Feb 2024 21:01:45 GMT
WORKDIR C:\
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
	-	`sha256:a3069ddb372bc0087899e61a271374e1b4423cfd9056ff2725874a89af15c2a1`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0841fad0c7557916603463fc9615983e0ad786338880d3d99c005dd50ecf3b6`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d1ae6fa2010fb779b06f0fc8a74830b01c9a87769fc35818fccdd5b7e7ea45`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4cd94fbe72557ed410a8f0aa0361ffc9ec2b2ecd96dc803b91c5ce0f34d077`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b3e385378ebc3f79f2c065897b323f0b1cfc97f3f8979c4530d0791e3e9523`  
		Last Modified: Thu, 11 Jan 2024 00:01:30 GMT  
		Size: 25.5 MB (25529890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbdf5bbf3fb6a215313abb55339dcee6260ef50d2c50d2b781476d5af12e840`  
		Last Modified: Thu, 11 Jan 2024 00:01:23 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7fd79e14c60629d3157a4363f602b919ba92aa10209a2e6ac40b7c86a75316`  
		Last Modified: Thu, 11 Jan 2024 00:01:23 GMT  
		Size: 261.7 KB (261737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d6abeee495b14ea2e44bb00f28c38212af6d923a1d5c148dd3eb083e1788d2`  
		Last Modified: Tue, 06 Feb 2024 20:38:27 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699b8adf45cf387aabdaea0b829e6bf5dee7a05e7eaf5519d3b0f5fe071e14a`  
		Last Modified: Tue, 06 Feb 2024 20:38:45 GMT  
		Size: 69.4 MB (69373765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd60a6e8aaafdd337241c619e2cd664dbfd6052a133b148c86845f227a25ea14`  
		Last Modified: Tue, 06 Feb 2024 20:38:27 GMT  
		Size: 1.5 KB (1531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6796689d52835dc674b67907c3e03bb20425e0e76be6963eaeb04e035d2c7f`  
		Last Modified: Tue, 06 Feb 2024 21:02:41 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657c487d0aab792a6141c8f2b5d1ef4564310178c60f883cb8e301cb752930ff`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bcd5a55d300a69a6a7202fda4cdb55a8e4f3645145c962279bc958c9efdf5a`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f9fc1b6232aab1694132043a6674117073dc98b00635546605582fabd31300`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005f7ea8d310ffb3ab0f46fbb75e4a90192f694357210b16fa4867a1c593cf2e`  
		Last Modified: Tue, 06 Feb 2024 21:02:39 GMT  
		Size: 1.7 MB (1675717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f756efa4d252460db4055d7da93b4667f4b1537f46882db730596bac57eb677`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:c6e3f25c93c35d4a519395eb595f46de5889867e37acd83bac72b8d2d9dcef3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `caddy:2-windowsservercore` - windows version 10.0.20348.2227; amd64

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

### `caddy:2-windowsservercore` - windows version 10.0.17763.5329; amd64

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

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:f7e06b6f876505ed8ae83c339c860ab40d8287d52669bddf6dad0302470155d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

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

## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:cdb4600df8fe3e27d97f1fb21ba9d5fdb1bd8198a1f025ca2458154f28d76934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

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

## `caddy:2.7`

```console
$ docker pull caddy@sha256:245e14283de7392fd14ef9e425580fe689cc0f8eedf28376016dab4109bc76b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `caddy:2.7` - linux; amd64

```console
$ docker pull caddy@sha256:67d0aa24ce021bee77049ddd2c0cc64732dd43d04598085ec39f950a13981bd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18467338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66978cebfbcc9c0a17709b108582a40a369c525c764e9a8882f6cae260b32f4d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:39:14 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 03:39:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 03:39:16 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:39:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 03:39:18 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 03:39:18 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 03:39:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 80
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 443
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 03:39:19 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 03:39:19 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf3211613d439d6da6e22998ce1ca109a902f861e1c1d55f59750636c8b7dc`  
		Last Modified: Sat, 27 Jan 2024 03:39:38 GMT  
		Size: 350.8 KB (350837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3505501083aeee1ff957f129e7d5dbdec0a32b80fee88cba62665e91547eeee0`  
		Last Modified: Sat, 27 Jan 2024 03:39:38 GMT  
		Size: 7.5 KB (7523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcbb25232b8128478b3c2ba4fe7e03fafdbf5024b74db396eef024b547f95ca`  
		Last Modified: Sat, 27 Jan 2024 03:39:40 GMT  
		Size: 14.7 MB (14706436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - linux; arm variant v6

```console
$ docker pull caddy@sha256:6fb5cfba87d2f8f1e7f89e7f61fad3a9e2ef76dc7f58aaffdf5af8997dc6dac4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17423230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3a842d1153c178390b3187d16d1ea0f4d691fd1c72bc5fd0a2ff32c6915a02`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:05:40 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 00:05:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 00:05:42 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:05:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 00:05:45 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 00:05:45 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 00:05:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 00:05:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 80
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 443
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 00:05:46 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 00:05:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a63a43f994064f0597fc36462d12376175178fc2c5486a9edcb36b198de411`  
		Last Modified: Sat, 27 Jan 2024 00:06:02 GMT  
		Size: 347.6 KB (347620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2327a8d9853b0ed7c134359a0fb7d0ea93d16621dd29a136c22bb30c59493703`  
		Last Modified: Sat, 27 Jan 2024 00:06:02 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71ff73f86184e48aa48d9298e97a824ab7316cc6134da0983587197e162a4d6`  
		Last Modified: Sat, 27 Jan 2024 00:06:04 GMT  
		Size: 13.9 MB (13921023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - linux; arm variant v7

```console
$ docker pull caddy@sha256:56128992f412b5e862c705f3ea06a9e290a1caa484f80111556fb1f13c15ce16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17147114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71cfdc5faaa533682a397011b220a59fa9e54a42f98146bfb1080c102a0ebc86`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:44:33 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 00:44:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 00:44:35 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:44:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 00:44:41 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 00:44:41 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 00:44:42 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 00:44:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 00:44:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 00:44:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 00:44:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 00:44:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 00:44:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 00:44:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 00:44:44 GMT
EXPOSE 80
# Sat, 27 Jan 2024 00:44:45 GMT
EXPOSE 443
# Sat, 27 Jan 2024 00:44:45 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 00:44:46 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 00:44:46 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 00:44:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2a6e8e98d60ee548724a36c2a41ee2f4053b409052e45ab4b015360e73c808`  
		Last Modified: Sat, 27 Jan 2024 00:45:17 GMT  
		Size: 344.5 KB (344463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9afd4ba62ae2a5b6f5ffd0c7d900582f8e684b0d45670317b63e3b8f51dc9b`  
		Last Modified: Sat, 27 Jan 2024 00:45:17 GMT  
		Size: 7.5 KB (7527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b8e42e4efab7a06b51ee74ffac1bca9bf70812dd543cb7ab60135515565e13`  
		Last Modified: Sat, 27 Jan 2024 00:45:20 GMT  
		Size: 13.9 MB (13893732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:2ec95d40ce2d1f18f92eee012a5dd18b352075d92eb6c4f4e0ea18c46ad4b069
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09733d8f0611adb987aea99d5144981331f8b6de5c2397bef43678ba50066f4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:44:36 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 03:44:38 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 03:44:38 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:44:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 03:44:40 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 03:44:40 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 80
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 443
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 03:44:41 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 03:44:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8d53bc0303fbf7f349016b59b6ac8710ba2639505e276c3816ecca679bdac7`  
		Last Modified: Sat, 27 Jan 2024 03:44:57 GMT  
		Size: 360.7 KB (360652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764cd8cdd6e6b377bd4cd13dbb53eb18d9fc7e0045323401614398d5a85b9c65`  
		Last Modified: Sat, 27 Jan 2024 03:44:56 GMT  
		Size: 7.5 KB (7526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00acba9333616526f5fc17192a0abd4e29624bba1500c6068db189bdcbee5468`  
		Last Modified: Sat, 27 Jan 2024 03:44:58 GMT  
		Size: 13.6 MB (13568965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - linux; ppc64le

```console
$ docker pull caddy@sha256:53a5136ccffab422016068b77862678ad9b19430fc52f7e911188703d0123939
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17052070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9c424cec6fbefc3fd4578ed97634fbe37d2590a0e474a0dce3a35ff23a8352`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:48:34 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 00:48:36 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 00:48:36 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:48:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 00:48:41 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 00:48:41 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 00:48:42 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 00:48:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 00:48:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 00:48:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 00:48:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 00:48:44 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 00:48:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 00:48:45 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 00:48:45 GMT
EXPOSE 80
# Sat, 27 Jan 2024 00:48:46 GMT
EXPOSE 443
# Sat, 27 Jan 2024 00:48:46 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 00:48:47 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 00:48:47 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 00:48:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5469759827ceaac50f13afad48892591b541bff7fa92b64936e2059ba28db3`  
		Last Modified: Sat, 27 Jan 2024 00:49:05 GMT  
		Size: 362.2 KB (362186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2c06e0d1950f2257265e78e914ebe1d4e1b0cfbfc32ba881b844fd13beb05b`  
		Last Modified: Sat, 27 Jan 2024 00:49:05 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2689e7d4f2d85097f8a724b4e3e41a875ff392132743a088b133a4d6802f6238`  
		Last Modified: Sat, 27 Jan 2024 00:49:07 GMT  
		Size: 13.3 MB (13333868 bytes)  
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

### `caddy:2.7` - windows version 10.0.20348.2227; amd64

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

### `caddy:2.7` - windows version 10.0.17763.5329; amd64

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

## `caddy:2.7-alpine`

```console
$ docker pull caddy@sha256:80ca561981768b2c3568cc4bef3d4cd1f11c2a625c806bedeb8453aef98779a0
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
$ docker pull caddy@sha256:67d0aa24ce021bee77049ddd2c0cc64732dd43d04598085ec39f950a13981bd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18467338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66978cebfbcc9c0a17709b108582a40a369c525c764e9a8882f6cae260b32f4d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:39:14 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 03:39:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 03:39:16 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:39:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 03:39:18 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 03:39:18 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 03:39:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 80
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 443
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 03:39:19 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 03:39:19 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf3211613d439d6da6e22998ce1ca109a902f861e1c1d55f59750636c8b7dc`  
		Last Modified: Sat, 27 Jan 2024 03:39:38 GMT  
		Size: 350.8 KB (350837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3505501083aeee1ff957f129e7d5dbdec0a32b80fee88cba62665e91547eeee0`  
		Last Modified: Sat, 27 Jan 2024 03:39:38 GMT  
		Size: 7.5 KB (7523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcbb25232b8128478b3c2ba4fe7e03fafdbf5024b74db396eef024b547f95ca`  
		Last Modified: Sat, 27 Jan 2024 03:39:40 GMT  
		Size: 14.7 MB (14706436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:6fb5cfba87d2f8f1e7f89e7f61fad3a9e2ef76dc7f58aaffdf5af8997dc6dac4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17423230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3a842d1153c178390b3187d16d1ea0f4d691fd1c72bc5fd0a2ff32c6915a02`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:05:40 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 00:05:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 00:05:42 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:05:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 00:05:45 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 00:05:45 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 00:05:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 00:05:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 80
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 443
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 00:05:46 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 00:05:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a63a43f994064f0597fc36462d12376175178fc2c5486a9edcb36b198de411`  
		Last Modified: Sat, 27 Jan 2024 00:06:02 GMT  
		Size: 347.6 KB (347620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2327a8d9853b0ed7c134359a0fb7d0ea93d16621dd29a136c22bb30c59493703`  
		Last Modified: Sat, 27 Jan 2024 00:06:02 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71ff73f86184e48aa48d9298e97a824ab7316cc6134da0983587197e162a4d6`  
		Last Modified: Sat, 27 Jan 2024 00:06:04 GMT  
		Size: 13.9 MB (13921023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:56128992f412b5e862c705f3ea06a9e290a1caa484f80111556fb1f13c15ce16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17147114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71cfdc5faaa533682a397011b220a59fa9e54a42f98146bfb1080c102a0ebc86`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:44:33 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 00:44:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 00:44:35 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:44:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 00:44:41 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 00:44:41 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 00:44:42 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 00:44:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 00:44:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 00:44:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 00:44:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 00:44:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 00:44:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 00:44:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 00:44:44 GMT
EXPOSE 80
# Sat, 27 Jan 2024 00:44:45 GMT
EXPOSE 443
# Sat, 27 Jan 2024 00:44:45 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 00:44:46 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 00:44:46 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 00:44:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2a6e8e98d60ee548724a36c2a41ee2f4053b409052e45ab4b015360e73c808`  
		Last Modified: Sat, 27 Jan 2024 00:45:17 GMT  
		Size: 344.5 KB (344463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9afd4ba62ae2a5b6f5ffd0c7d900582f8e684b0d45670317b63e3b8f51dc9b`  
		Last Modified: Sat, 27 Jan 2024 00:45:17 GMT  
		Size: 7.5 KB (7527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b8e42e4efab7a06b51ee74ffac1bca9bf70812dd543cb7ab60135515565e13`  
		Last Modified: Sat, 27 Jan 2024 00:45:20 GMT  
		Size: 13.9 MB (13893732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:2ec95d40ce2d1f18f92eee012a5dd18b352075d92eb6c4f4e0ea18c46ad4b069
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09733d8f0611adb987aea99d5144981331f8b6de5c2397bef43678ba50066f4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:44:36 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 03:44:38 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 03:44:38 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:44:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 03:44:40 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 03:44:40 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 80
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 443
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 03:44:41 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 03:44:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8d53bc0303fbf7f349016b59b6ac8710ba2639505e276c3816ecca679bdac7`  
		Last Modified: Sat, 27 Jan 2024 03:44:57 GMT  
		Size: 360.7 KB (360652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764cd8cdd6e6b377bd4cd13dbb53eb18d9fc7e0045323401614398d5a85b9c65`  
		Last Modified: Sat, 27 Jan 2024 03:44:56 GMT  
		Size: 7.5 KB (7526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00acba9333616526f5fc17192a0abd4e29624bba1500c6068db189bdcbee5468`  
		Last Modified: Sat, 27 Jan 2024 03:44:58 GMT  
		Size: 13.6 MB (13568965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:53a5136ccffab422016068b77862678ad9b19430fc52f7e911188703d0123939
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17052070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9c424cec6fbefc3fd4578ed97634fbe37d2590a0e474a0dce3a35ff23a8352`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:48:34 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 00:48:36 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 00:48:36 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:48:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 00:48:41 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 00:48:41 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 00:48:42 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 00:48:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 00:48:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 00:48:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 00:48:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 00:48:44 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 00:48:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 00:48:45 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 00:48:45 GMT
EXPOSE 80
# Sat, 27 Jan 2024 00:48:46 GMT
EXPOSE 443
# Sat, 27 Jan 2024 00:48:46 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 00:48:47 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 00:48:47 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 00:48:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5469759827ceaac50f13afad48892591b541bff7fa92b64936e2059ba28db3`  
		Last Modified: Sat, 27 Jan 2024 00:49:05 GMT  
		Size: 362.2 KB (362186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2c06e0d1950f2257265e78e914ebe1d4e1b0cfbfc32ba881b844fd13beb05b`  
		Last Modified: Sat, 27 Jan 2024 00:49:05 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2689e7d4f2d85097f8a724b4e3e41a875ff392132743a088b133a4d6802f6238`  
		Last Modified: Sat, 27 Jan 2024 00:49:07 GMT  
		Size: 13.3 MB (13333868 bytes)  
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
$ docker pull caddy@sha256:42442569a853bd5e5ce825d52baaee3fc919d1fa0e2fb7b9db30f246bec05c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `caddy:2.7-builder` - linux; amd64

```console
$ docker pull caddy@sha256:09513acee0757eaafeea861313a51d37b907cde693899b4d85bffa691d7eca06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77024166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e2950806b4846bc8384039f8e0ced6b55a43843627c3c7bcb574d00da87e36`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 03:39:23 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 03:39:23 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 03:39:24 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:39:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 03:39:24 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 03:39:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 03:39:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 03:39:25 GMT
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
	-	`sha256:c4b77ba268427b27996c293cddcbb1af065ac97d6f64fff6d3ee0adce318de44`  
		Last Modified: Sat, 27 Jan 2024 01:37:37 GMT  
		Size: 67.1 MB (67061623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5c147192a9317b4f575377244f4c3d96df9c9108d6147e10cd2becfdcfdc75`  
		Last Modified: Sat, 27 Jan 2024 01:37:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426789fa51aac91ce386d0cf62e3c5b4fd91cc19da6cb9449035a1aad2a1cb4b`  
		Last Modified: Sat, 27 Jan 2024 03:39:53 GMT  
		Size: 5.0 MB (4972458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848439cf5d4cf7d00a316abe8d0c04005a28d2e60f11875549cbbeec7db5cafc`  
		Last Modified: Sat, 27 Jan 2024 03:39:53 GMT  
		Size: 1.3 MB (1302243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61744c717cfe93977f876b739f3c692e919bb8cf098d233db8af67c532d77cd`  
		Last Modified: Sat, 27 Jan 2024 03:39:52 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:f7f15d8dc37358732c441ac4c62c2ac4967b16eb93863621dfc5cacf0b9dc1c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75479956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b694cc61283aebb38db78010935fc8281778bc08c35e7816a8c8819d3727a6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 13:22:00 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 13:22:00 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 13:22:00 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 13:22:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 13:22:01 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 13:22:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 13:22:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 13:22:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6033bb349d654a4ba7602191ed0372313ceca193751253005ad66a23d4dcb0ec`  
		Last Modified: Sat, 27 Jan 2024 09:20:38 GMT  
		Size: 284.9 KB (284872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31e5472cbeca7cc0b8f9272fbe547db898349f9b598c6b975f2c4efeeb63aee`  
		Last Modified: Sat, 27 Jan 2024 09:21:48 GMT  
		Size: 65.8 MB (65832091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b979a15e6ae0ded8491c78ec0740e6ece1aaaa584d10fdb89131c53427aba66`  
		Last Modified: Sat, 27 Jan 2024 09:21:32 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31abdea622b745b38e9215bf8062f71c377f48b2049bf07a5cd650743c069abb`  
		Last Modified: Sat, 27 Jan 2024 13:22:18 GMT  
		Size: 5.0 MB (4966664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f06e6a7ead4077a0b30ee09128ded6d14cd9bd7f450ef457f559c9e5b59938`  
		Last Modified: Sat, 27 Jan 2024 13:22:18 GMT  
		Size: 1.2 MB (1248661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba060f027200c3446f1acab0c00b2f4a9e8acf8610c46591daa3d8d7434aafd`  
		Last Modified: Sat, 27 Jan 2024 13:22:17 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:c80d0eabc3c5c1e92b026b7e2c2c35b4783472f984fe455da2ddddedce5b416c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25cc1ad71b8526356adff18f79ddbb3ff658a705a74e76800ee8f8172d4551f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 21:55:58 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:55:58 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:55:58 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:55:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:55:59 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:56:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:56:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:56:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf835181e2f4c73f7de0fe69c219658c3feddb5ba4e6850bc5b5af9555c08d1`  
		Last Modified: Sat, 27 Jan 2024 00:41:32 GMT  
		Size: 284.1 KB (284079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e2cd4f5b6025c32b2853d34aa0bcf57d85f2d44b2e412e2ba4e6dd0159ac1f`  
		Last Modified: Tue, 06 Feb 2024 21:29:51 GMT  
		Size: 65.8 MB (65767453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d160b5a79dd98fde6c0642c78daa3c77f077ad44a16b27b65a3b24fff23c603f`  
		Last Modified: Tue, 06 Feb 2024 21:29:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5735d56095a062d062dbd8c2d92cff873a457010035f0a7bf754444cdda79e1`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 4.5 MB (4514266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e601fac0470697a15f02c34e269f0e19119d88f46ffbcdddc5300417e3aab4b`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 1.2 MB (1246089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caff9a4e5a9e81ccc2e586bdbd72039b0d2bcc929751e08afbcffd6dbff11931`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:31f32db6814a94ad3cac5661dbda0a586162eb0b22b3e6ccdeb3e72b55cb9b76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73998584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c56aa1b8e6d877694eff62d87142b579cb7d523e8f22c16615b9ec3c5e3bae3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 21:33:04 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:33:04 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:33:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:33:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:33:06 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e59bef827dc10d9c33cdf4762faf3f2987df2a0296378e2349ec6d5bc6a37f4`  
		Last Modified: Sat, 27 Jan 2024 05:33:17 GMT  
		Size: 286.3 KB (286302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328d8fad75fb04ebff991b2c11c5988722931b5300239657bc1b4961655df05f`  
		Last Modified: Tue, 06 Feb 2024 20:50:08 GMT  
		Size: 64.1 MB (64109254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62899699addead1db84d09ab10dc0a0cbde16beb64c81cde0f84af2fa9b30f39`  
		Last Modified: Tue, 06 Feb 2024 20:50:00 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1745cea878add1608edd8710a879d4925a33b6e27329531c9c1cdd2c0e79c91a`  
		Last Modified: Tue, 06 Feb 2024 21:33:21 GMT  
		Size: 5.1 MB (5070613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235f6d9da6844caff2a0af124b9c01f0bf0abd2be340e5d2c67ab135a7cca76d`  
		Last Modified: Tue, 06 Feb 2024 21:33:21 GMT  
		Size: 1.2 MB (1198444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca8afc86b60749044b9b64230a9f9c67c20aa089b99562732169c4e6a807628`  
		Last Modified: Tue, 06 Feb 2024 21:33:20 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:b4effdad9be7ca7509b54d46638823940081fdf20f3000aaf9b3a691ace61f17
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74213039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10cf81cb43dc269c0ea9f820417d703e172313e228a17bdf7cffe96f4d2e742`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 21:14:22 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:14:22 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:14:23 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:14:23 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:14:24 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:14:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:14:27 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:14:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f92ca388ce06d6dddf0b5ad5ca0d5b82049994f1ad4da72bb5e48c5783dc009`  
		Last Modified: Sat, 27 Jan 2024 01:13:46 GMT  
		Size: 286.7 KB (286665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ef3661c7b713c28d8e0ae3c73dc823022f6a6e8a65c6fd2f00aa13dd6be4e4`  
		Last Modified: Tue, 06 Feb 2024 20:39:21 GMT  
		Size: 64.1 MB (64120440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7f0aa3654740d4016d469bad05baafdfc3be78e2f6ebc6f938501a1f4cd056`  
		Last Modified: Tue, 06 Feb 2024 20:39:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53242ccbc16994912810b389fdd1f7cb7cb1a3223cec7dcac1d4d00340e2f6de`  
		Last Modified: Tue, 06 Feb 2024 21:14:45 GMT  
		Size: 5.3 MB (5270660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c055ede766eec14283da8e4f87ab21f6a84f8ceff065d702bc31c9bf9ef23757`  
		Last Modified: Tue, 06 Feb 2024 21:14:45 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbe5c0b6966115344269e3c2b83ef21af0ebd897ee5a670604887f27d3da882`  
		Last Modified: Tue, 06 Feb 2024 21:14:44 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; s390x

```console
$ docker pull caddy@sha256:25c4422b5cf06de48acecb96441e14f50db37a05c9353138f1f0f8b476680bb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76167035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06a921e90d95d0edd27e62d87f24a3fced554bde075b4b48f9099611fecb599`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 14:17:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 14:17:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 14:17:32 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 14:17:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 14:17:33 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 14:17:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 14:17:36 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 14:17:36 GMT
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
	-	`sha256:b94763531102ae1af628e5b55ca073b0c0fbd6aab9f221a28f3895303ddd975d`  
		Last Modified: Sat, 27 Jan 2024 05:47:26 GMT  
		Size: 66.3 MB (66284463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd03f53bee613b790f5b2286c4561428b2b2da6234df368a3a50d5ad91d58b9a`  
		Last Modified: Sat, 27 Jan 2024 05:47:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c299d55132b1737b4877e997f9881e05bd66727a05f8502f6fc38969031381ce`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 5.1 MB (5116950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60611bccc71deeef6872096a6f8a89a7e7af13c5027eb639b2ee7c182855d85`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 1.3 MB (1262387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fda9b2eed36da0393b2486d62a5c2c8ed03d6f3e38b27aae0fb6a57259b22e`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - windows version 10.0.20348.2227; amd64

```console
$ docker pull caddy@sha256:4814d63f1ac1d7e2334ff267279eed3b5533e0f94ad926fe9b3f11064e087406
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1997072166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d833851f7e1c400f60d5591428c91912a576258fb5b2fd93a0cdd0b228b07d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jan 2024 23:22:59 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Jan 2024 23:23:00 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Jan 2024 23:23:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Jan 2024 23:23:02 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Jan 2024 23:23:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Jan 2024 23:23:36 GMT
ENV GOPATH=C:\go
# Wed, 10 Jan 2024 23:23:55 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 Feb 2024 20:15:33 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 20:17:57 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 Feb 2024 20:17:58 GMT
WORKDIR C:\go
# Tue, 06 Feb 2024 21:01:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Feb 2024 21:01:18 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:01:19 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:01:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:01:44 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 06 Feb 2024 21:01:45 GMT
WORKDIR C:\
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
	-	`sha256:a3069ddb372bc0087899e61a271374e1b4423cfd9056ff2725874a89af15c2a1`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0841fad0c7557916603463fc9615983e0ad786338880d3d99c005dd50ecf3b6`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d1ae6fa2010fb779b06f0fc8a74830b01c9a87769fc35818fccdd5b7e7ea45`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4cd94fbe72557ed410a8f0aa0361ffc9ec2b2ecd96dc803b91c5ce0f34d077`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b3e385378ebc3f79f2c065897b323f0b1cfc97f3f8979c4530d0791e3e9523`  
		Last Modified: Thu, 11 Jan 2024 00:01:30 GMT  
		Size: 25.5 MB (25529890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbdf5bbf3fb6a215313abb55339dcee6260ef50d2c50d2b781476d5af12e840`  
		Last Modified: Thu, 11 Jan 2024 00:01:23 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7fd79e14c60629d3157a4363f602b919ba92aa10209a2e6ac40b7c86a75316`  
		Last Modified: Thu, 11 Jan 2024 00:01:23 GMT  
		Size: 261.7 KB (261737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d6abeee495b14ea2e44bb00f28c38212af6d923a1d5c148dd3eb083e1788d2`  
		Last Modified: Tue, 06 Feb 2024 20:38:27 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699b8adf45cf387aabdaea0b829e6bf5dee7a05e7eaf5519d3b0f5fe071e14a`  
		Last Modified: Tue, 06 Feb 2024 20:38:45 GMT  
		Size: 69.4 MB (69373765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd60a6e8aaafdd337241c619e2cd664dbfd6052a133b148c86845f227a25ea14`  
		Last Modified: Tue, 06 Feb 2024 20:38:27 GMT  
		Size: 1.5 KB (1531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6796689d52835dc674b67907c3e03bb20425e0e76be6963eaeb04e035d2c7f`  
		Last Modified: Tue, 06 Feb 2024 21:02:41 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657c487d0aab792a6141c8f2b5d1ef4564310178c60f883cb8e301cb752930ff`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bcd5a55d300a69a6a7202fda4cdb55a8e4f3645145c962279bc958c9efdf5a`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f9fc1b6232aab1694132043a6674117073dc98b00635546605582fabd31300`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005f7ea8d310ffb3ab0f46fbb75e4a90192f694357210b16fa4867a1c593cf2e`  
		Last Modified: Tue, 06 Feb 2024 21:02:39 GMT  
		Size: 1.7 MB (1675717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f756efa4d252460db4055d7da93b4667f4b1537f46882db730596bac57eb677`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - windows version 10.0.17763.5329; amd64

```console
$ docker pull caddy@sha256:882f417e3efb3b9a8d1ade5245808ac22c5c1ea57a1352c72b6652b3a3238ecf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2166627810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6206308760870c6bbbd479176af11a35608423c94c08b69c418649ce2d281f3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jan 2024 23:26:43 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Jan 2024 23:26:44 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Jan 2024 23:26:45 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Jan 2024 23:26:46 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Jan 2024 23:28:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Jan 2024 23:28:09 GMT
ENV GOPATH=C:\go
# Wed, 10 Jan 2024 23:29:17 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 Feb 2024 20:18:16 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 20:21:36 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 Feb 2024 20:21:37 GMT
WORKDIR C:\go
# Tue, 06 Feb 2024 20:59:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Feb 2024 20:59:49 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 20:59:50 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 20:59:51 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:01:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 06 Feb 2024 21:01:01 GMT
WORKDIR C:\
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
	-	`sha256:58a2d0f9e9eca6932479b4446cdad2350fe376cd5102106ac4938d8552073ee1`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3baf188f2343abdd0b6b9307f8adcc91c698473839c28dbba9e3b50117d7df5`  
		Last Modified: Thu, 11 Jan 2024 00:03:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83f321def9731da0b67b8c9c7c573a95237ff9d906d16394dfc3dd845bd806`  
		Last Modified: Thu, 11 Jan 2024 00:03:01 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3185717e4484ba21a137fb6d471a72ee842364637f999013cbd8b7a633ccfa`  
		Last Modified: Thu, 11 Jan 2024 00:03:01 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d432d7f01be369829a69831b58f259bc1d30ccb67bc46a16211f95454e2d026b`  
		Last Modified: Thu, 11 Jan 2024 00:03:06 GMT  
		Size: 25.6 MB (25555277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481ab54aaa7ea3f3af1db424c6fda8a4bf6e63fe0bc92e2e319db55c66952d5`  
		Last Modified: Thu, 11 Jan 2024 00:02:59 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4579730b543c234b271242a1f8b94332944911daa12fe4493f4daad09e6e6a1`  
		Last Modified: Thu, 11 Jan 2024 00:02:59 GMT  
		Size: 284.0 KB (284031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57342fc3b749de0a8e32c9f1f9eece3c3855ea5d8b63b70682518058c40ba349`  
		Last Modified: Tue, 06 Feb 2024 20:38:59 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d092fd3744c0081064bac79e4fb322e2f6e9d0d8e744bb837bccd7f9b844e8`  
		Last Modified: Tue, 06 Feb 2024 20:39:17 GMT  
		Size: 69.4 MB (69370513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a8538533cb5606cc3e717f0431791fcd99ca7c1b935f5586f465bbd0c9d457`  
		Last Modified: Tue, 06 Feb 2024 20:38:59 GMT  
		Size: 1.6 KB (1586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ba50226998b42d6500ba479c1fbf0f3e588807488f728c91715ac893e69838`  
		Last Modified: Tue, 06 Feb 2024 21:02:24 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74292b50264f2db380dc5a9a8baaa5d229ff8efd2699e40fc6f478a25d59c0d0`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e574cef27624cb2b445968d4f051529c8c02dc6bf599ea131f51164de4939536`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14832cf23b08465f9e60489cda03b116fb6be01de86762232ed2f3b3aa8cf2a4`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e89456cebd7c16015a94dda1edb8a055ef730bc8c289b8eae13b1867371376f`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.7 MB (1677010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874ea9f0878170aeeae3da252653488f0677348bdb3f6cd9a87ccb3d064bde10`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-alpine`

```console
$ docker pull caddy@sha256:8a0f239bbd24b1a0973d0e3e22ef69d2e9f27b2f860c50247deead9c47b8b81e
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
$ docker pull caddy@sha256:09513acee0757eaafeea861313a51d37b907cde693899b4d85bffa691d7eca06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77024166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e2950806b4846bc8384039f8e0ced6b55a43843627c3c7bcb574d00da87e36`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 03:39:23 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 03:39:23 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 03:39:24 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:39:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 03:39:24 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 03:39:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 03:39:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 03:39:25 GMT
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
	-	`sha256:c4b77ba268427b27996c293cddcbb1af065ac97d6f64fff6d3ee0adce318de44`  
		Last Modified: Sat, 27 Jan 2024 01:37:37 GMT  
		Size: 67.1 MB (67061623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5c147192a9317b4f575377244f4c3d96df9c9108d6147e10cd2becfdcfdc75`  
		Last Modified: Sat, 27 Jan 2024 01:37:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426789fa51aac91ce386d0cf62e3c5b4fd91cc19da6cb9449035a1aad2a1cb4b`  
		Last Modified: Sat, 27 Jan 2024 03:39:53 GMT  
		Size: 5.0 MB (4972458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848439cf5d4cf7d00a316abe8d0c04005a28d2e60f11875549cbbeec7db5cafc`  
		Last Modified: Sat, 27 Jan 2024 03:39:53 GMT  
		Size: 1.3 MB (1302243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61744c717cfe93977f876b739f3c692e919bb8cf098d233db8af67c532d77cd`  
		Last Modified: Sat, 27 Jan 2024 03:39:52 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:f7f15d8dc37358732c441ac4c62c2ac4967b16eb93863621dfc5cacf0b9dc1c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75479956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b694cc61283aebb38db78010935fc8281778bc08c35e7816a8c8819d3727a6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 13:22:00 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 13:22:00 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 13:22:00 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 13:22:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 13:22:01 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 13:22:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 13:22:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 13:22:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6033bb349d654a4ba7602191ed0372313ceca193751253005ad66a23d4dcb0ec`  
		Last Modified: Sat, 27 Jan 2024 09:20:38 GMT  
		Size: 284.9 KB (284872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31e5472cbeca7cc0b8f9272fbe547db898349f9b598c6b975f2c4efeeb63aee`  
		Last Modified: Sat, 27 Jan 2024 09:21:48 GMT  
		Size: 65.8 MB (65832091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b979a15e6ae0ded8491c78ec0740e6ece1aaaa584d10fdb89131c53427aba66`  
		Last Modified: Sat, 27 Jan 2024 09:21:32 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31abdea622b745b38e9215bf8062f71c377f48b2049bf07a5cd650743c069abb`  
		Last Modified: Sat, 27 Jan 2024 13:22:18 GMT  
		Size: 5.0 MB (4966664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f06e6a7ead4077a0b30ee09128ded6d14cd9bd7f450ef457f559c9e5b59938`  
		Last Modified: Sat, 27 Jan 2024 13:22:18 GMT  
		Size: 1.2 MB (1248661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba060f027200c3446f1acab0c00b2f4a9e8acf8610c46591daa3d8d7434aafd`  
		Last Modified: Sat, 27 Jan 2024 13:22:17 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:c80d0eabc3c5c1e92b026b7e2c2c35b4783472f984fe455da2ddddedce5b416c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25cc1ad71b8526356adff18f79ddbb3ff658a705a74e76800ee8f8172d4551f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 21:55:58 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:55:58 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:55:58 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:55:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:55:59 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:56:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:56:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:56:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf835181e2f4c73f7de0fe69c219658c3feddb5ba4e6850bc5b5af9555c08d1`  
		Last Modified: Sat, 27 Jan 2024 00:41:32 GMT  
		Size: 284.1 KB (284079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e2cd4f5b6025c32b2853d34aa0bcf57d85f2d44b2e412e2ba4e6dd0159ac1f`  
		Last Modified: Tue, 06 Feb 2024 21:29:51 GMT  
		Size: 65.8 MB (65767453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d160b5a79dd98fde6c0642c78daa3c77f077ad44a16b27b65a3b24fff23c603f`  
		Last Modified: Tue, 06 Feb 2024 21:29:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5735d56095a062d062dbd8c2d92cff873a457010035f0a7bf754444cdda79e1`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 4.5 MB (4514266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e601fac0470697a15f02c34e269f0e19119d88f46ffbcdddc5300417e3aab4b`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 1.2 MB (1246089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caff9a4e5a9e81ccc2e586bdbd72039b0d2bcc929751e08afbcffd6dbff11931`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:31f32db6814a94ad3cac5661dbda0a586162eb0b22b3e6ccdeb3e72b55cb9b76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73998584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c56aa1b8e6d877694eff62d87142b579cb7d523e8f22c16615b9ec3c5e3bae3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 21:33:04 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:33:04 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:33:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:33:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:33:06 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e59bef827dc10d9c33cdf4762faf3f2987df2a0296378e2349ec6d5bc6a37f4`  
		Last Modified: Sat, 27 Jan 2024 05:33:17 GMT  
		Size: 286.3 KB (286302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328d8fad75fb04ebff991b2c11c5988722931b5300239657bc1b4961655df05f`  
		Last Modified: Tue, 06 Feb 2024 20:50:08 GMT  
		Size: 64.1 MB (64109254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62899699addead1db84d09ab10dc0a0cbde16beb64c81cde0f84af2fa9b30f39`  
		Last Modified: Tue, 06 Feb 2024 20:50:00 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1745cea878add1608edd8710a879d4925a33b6e27329531c9c1cdd2c0e79c91a`  
		Last Modified: Tue, 06 Feb 2024 21:33:21 GMT  
		Size: 5.1 MB (5070613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235f6d9da6844caff2a0af124b9c01f0bf0abd2be340e5d2c67ab135a7cca76d`  
		Last Modified: Tue, 06 Feb 2024 21:33:21 GMT  
		Size: 1.2 MB (1198444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca8afc86b60749044b9b64230a9f9c67c20aa089b99562732169c4e6a807628`  
		Last Modified: Tue, 06 Feb 2024 21:33:20 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:b4effdad9be7ca7509b54d46638823940081fdf20f3000aaf9b3a691ace61f17
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74213039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10cf81cb43dc269c0ea9f820417d703e172313e228a17bdf7cffe96f4d2e742`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 21:14:22 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:14:22 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:14:23 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:14:23 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:14:24 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:14:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:14:27 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:14:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f92ca388ce06d6dddf0b5ad5ca0d5b82049994f1ad4da72bb5e48c5783dc009`  
		Last Modified: Sat, 27 Jan 2024 01:13:46 GMT  
		Size: 286.7 KB (286665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ef3661c7b713c28d8e0ae3c73dc823022f6a6e8a65c6fd2f00aa13dd6be4e4`  
		Last Modified: Tue, 06 Feb 2024 20:39:21 GMT  
		Size: 64.1 MB (64120440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7f0aa3654740d4016d469bad05baafdfc3be78e2f6ebc6f938501a1f4cd056`  
		Last Modified: Tue, 06 Feb 2024 20:39:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53242ccbc16994912810b389fdd1f7cb7cb1a3223cec7dcac1d4d00340e2f6de`  
		Last Modified: Tue, 06 Feb 2024 21:14:45 GMT  
		Size: 5.3 MB (5270660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c055ede766eec14283da8e4f87ab21f6a84f8ceff065d702bc31c9bf9ef23757`  
		Last Modified: Tue, 06 Feb 2024 21:14:45 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbe5c0b6966115344269e3c2b83ef21af0ebd897ee5a670604887f27d3da882`  
		Last Modified: Tue, 06 Feb 2024 21:14:44 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:25c4422b5cf06de48acecb96441e14f50db37a05c9353138f1f0f8b476680bb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76167035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06a921e90d95d0edd27e62d87f24a3fced554bde075b4b48f9099611fecb599`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 14:17:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 14:17:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 14:17:32 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 14:17:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 14:17:33 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 14:17:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 14:17:36 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 14:17:36 GMT
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
	-	`sha256:b94763531102ae1af628e5b55ca073b0c0fbd6aab9f221a28f3895303ddd975d`  
		Last Modified: Sat, 27 Jan 2024 05:47:26 GMT  
		Size: 66.3 MB (66284463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd03f53bee613b790f5b2286c4561428b2b2da6234df368a3a50d5ad91d58b9a`  
		Last Modified: Sat, 27 Jan 2024 05:47:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c299d55132b1737b4877e997f9881e05bd66727a05f8502f6fc38969031381ce`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 5.1 MB (5116950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60611bccc71deeef6872096a6f8a89a7e7af13c5027eb639b2ee7c182855d85`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 1.3 MB (1262387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fda9b2eed36da0393b2486d62a5c2c8ed03d6f3e38b27aae0fb6a57259b22e`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:e794dda1d2a08c7fe472d7b929a4d86621c3ea9ac1252d7fe1134e724a2115a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `caddy:2.7-builder-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull caddy@sha256:882f417e3efb3b9a8d1ade5245808ac22c5c1ea57a1352c72b6652b3a3238ecf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2166627810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6206308760870c6bbbd479176af11a35608423c94c08b69c418649ce2d281f3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jan 2024 23:26:43 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Jan 2024 23:26:44 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Jan 2024 23:26:45 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Jan 2024 23:26:46 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Jan 2024 23:28:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Jan 2024 23:28:09 GMT
ENV GOPATH=C:\go
# Wed, 10 Jan 2024 23:29:17 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 Feb 2024 20:18:16 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 20:21:36 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 Feb 2024 20:21:37 GMT
WORKDIR C:\go
# Tue, 06 Feb 2024 20:59:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Feb 2024 20:59:49 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 20:59:50 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 20:59:51 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:01:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 06 Feb 2024 21:01:01 GMT
WORKDIR C:\
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
	-	`sha256:58a2d0f9e9eca6932479b4446cdad2350fe376cd5102106ac4938d8552073ee1`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3baf188f2343abdd0b6b9307f8adcc91c698473839c28dbba9e3b50117d7df5`  
		Last Modified: Thu, 11 Jan 2024 00:03:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83f321def9731da0b67b8c9c7c573a95237ff9d906d16394dfc3dd845bd806`  
		Last Modified: Thu, 11 Jan 2024 00:03:01 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3185717e4484ba21a137fb6d471a72ee842364637f999013cbd8b7a633ccfa`  
		Last Modified: Thu, 11 Jan 2024 00:03:01 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d432d7f01be369829a69831b58f259bc1d30ccb67bc46a16211f95454e2d026b`  
		Last Modified: Thu, 11 Jan 2024 00:03:06 GMT  
		Size: 25.6 MB (25555277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481ab54aaa7ea3f3af1db424c6fda8a4bf6e63fe0bc92e2e319db55c66952d5`  
		Last Modified: Thu, 11 Jan 2024 00:02:59 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4579730b543c234b271242a1f8b94332944911daa12fe4493f4daad09e6e6a1`  
		Last Modified: Thu, 11 Jan 2024 00:02:59 GMT  
		Size: 284.0 KB (284031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57342fc3b749de0a8e32c9f1f9eece3c3855ea5d8b63b70682518058c40ba349`  
		Last Modified: Tue, 06 Feb 2024 20:38:59 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d092fd3744c0081064bac79e4fb322e2f6e9d0d8e744bb837bccd7f9b844e8`  
		Last Modified: Tue, 06 Feb 2024 20:39:17 GMT  
		Size: 69.4 MB (69370513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a8538533cb5606cc3e717f0431791fcd99ca7c1b935f5586f465bbd0c9d457`  
		Last Modified: Tue, 06 Feb 2024 20:38:59 GMT  
		Size: 1.6 KB (1586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ba50226998b42d6500ba479c1fbf0f3e588807488f728c91715ac893e69838`  
		Last Modified: Tue, 06 Feb 2024 21:02:24 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74292b50264f2db380dc5a9a8baaa5d229ff8efd2699e40fc6f478a25d59c0d0`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e574cef27624cb2b445968d4f051529c8c02dc6bf599ea131f51164de4939536`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14832cf23b08465f9e60489cda03b116fb6be01de86762232ed2f3b3aa8cf2a4`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e89456cebd7c16015a94dda1edb8a055ef730bc8c289b8eae13b1867371376f`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.7 MB (1677010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874ea9f0878170aeeae3da252653488f0677348bdb3f6cd9a87ccb3d064bde10`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:97e329cd72c287551121f0de0749affc40ba296a42f67b3774c972dfc63239d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `caddy:2.7-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull caddy@sha256:4814d63f1ac1d7e2334ff267279eed3b5533e0f94ad926fe9b3f11064e087406
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1997072166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d833851f7e1c400f60d5591428c91912a576258fb5b2fd93a0cdd0b228b07d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jan 2024 23:22:59 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Jan 2024 23:23:00 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Jan 2024 23:23:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Jan 2024 23:23:02 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Jan 2024 23:23:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Jan 2024 23:23:36 GMT
ENV GOPATH=C:\go
# Wed, 10 Jan 2024 23:23:55 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 Feb 2024 20:15:33 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 20:17:57 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 Feb 2024 20:17:58 GMT
WORKDIR C:\go
# Tue, 06 Feb 2024 21:01:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Feb 2024 21:01:18 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:01:19 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:01:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:01:44 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 06 Feb 2024 21:01:45 GMT
WORKDIR C:\
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
	-	`sha256:a3069ddb372bc0087899e61a271374e1b4423cfd9056ff2725874a89af15c2a1`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0841fad0c7557916603463fc9615983e0ad786338880d3d99c005dd50ecf3b6`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d1ae6fa2010fb779b06f0fc8a74830b01c9a87769fc35818fccdd5b7e7ea45`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4cd94fbe72557ed410a8f0aa0361ffc9ec2b2ecd96dc803b91c5ce0f34d077`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b3e385378ebc3f79f2c065897b323f0b1cfc97f3f8979c4530d0791e3e9523`  
		Last Modified: Thu, 11 Jan 2024 00:01:30 GMT  
		Size: 25.5 MB (25529890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbdf5bbf3fb6a215313abb55339dcee6260ef50d2c50d2b781476d5af12e840`  
		Last Modified: Thu, 11 Jan 2024 00:01:23 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7fd79e14c60629d3157a4363f602b919ba92aa10209a2e6ac40b7c86a75316`  
		Last Modified: Thu, 11 Jan 2024 00:01:23 GMT  
		Size: 261.7 KB (261737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d6abeee495b14ea2e44bb00f28c38212af6d923a1d5c148dd3eb083e1788d2`  
		Last Modified: Tue, 06 Feb 2024 20:38:27 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699b8adf45cf387aabdaea0b829e6bf5dee7a05e7eaf5519d3b0f5fe071e14a`  
		Last Modified: Tue, 06 Feb 2024 20:38:45 GMT  
		Size: 69.4 MB (69373765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd60a6e8aaafdd337241c619e2cd664dbfd6052a133b148c86845f227a25ea14`  
		Last Modified: Tue, 06 Feb 2024 20:38:27 GMT  
		Size: 1.5 KB (1531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6796689d52835dc674b67907c3e03bb20425e0e76be6963eaeb04e035d2c7f`  
		Last Modified: Tue, 06 Feb 2024 21:02:41 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657c487d0aab792a6141c8f2b5d1ef4564310178c60f883cb8e301cb752930ff`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bcd5a55d300a69a6a7202fda4cdb55a8e4f3645145c962279bc958c9efdf5a`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f9fc1b6232aab1694132043a6674117073dc98b00635546605582fabd31300`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005f7ea8d310ffb3ab0f46fbb75e4a90192f694357210b16fa4867a1c593cf2e`  
		Last Modified: Tue, 06 Feb 2024 21:02:39 GMT  
		Size: 1.7 MB (1675717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f756efa4d252460db4055d7da93b4667f4b1537f46882db730596bac57eb677`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-windowsservercore`

```console
$ docker pull caddy@sha256:c6e3f25c93c35d4a519395eb595f46de5889867e37acd83bac72b8d2d9dcef3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `caddy:2.7-windowsservercore` - windows version 10.0.20348.2227; amd64

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

### `caddy:2.7-windowsservercore` - windows version 10.0.17763.5329; amd64

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

## `caddy:2.7-windowsservercore-1809`

```console
$ docker pull caddy@sha256:f7e06b6f876505ed8ae83c339c860ab40d8287d52669bddf6dad0302470155d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `caddy:2.7-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

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

## `caddy:2.7-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:cdb4600df8fe3e27d97f1fb21ba9d5fdb1bd8198a1f025ca2458154f28d76934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `caddy:2.7-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

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

## `caddy:2.7.6`

```console
$ docker pull caddy@sha256:245e14283de7392fd14ef9e425580fe689cc0f8eedf28376016dab4109bc76b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `caddy:2.7.6` - linux; amd64

```console
$ docker pull caddy@sha256:67d0aa24ce021bee77049ddd2c0cc64732dd43d04598085ec39f950a13981bd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18467338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66978cebfbcc9c0a17709b108582a40a369c525c764e9a8882f6cae260b32f4d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:39:14 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 03:39:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 03:39:16 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:39:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 03:39:18 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 03:39:18 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 03:39:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 80
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 443
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 03:39:19 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 03:39:19 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf3211613d439d6da6e22998ce1ca109a902f861e1c1d55f59750636c8b7dc`  
		Last Modified: Sat, 27 Jan 2024 03:39:38 GMT  
		Size: 350.8 KB (350837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3505501083aeee1ff957f129e7d5dbdec0a32b80fee88cba62665e91547eeee0`  
		Last Modified: Sat, 27 Jan 2024 03:39:38 GMT  
		Size: 7.5 KB (7523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcbb25232b8128478b3c2ba4fe7e03fafdbf5024b74db396eef024b547f95ca`  
		Last Modified: Sat, 27 Jan 2024 03:39:40 GMT  
		Size: 14.7 MB (14706436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6` - linux; arm variant v6

```console
$ docker pull caddy@sha256:6fb5cfba87d2f8f1e7f89e7f61fad3a9e2ef76dc7f58aaffdf5af8997dc6dac4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17423230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3a842d1153c178390b3187d16d1ea0f4d691fd1c72bc5fd0a2ff32c6915a02`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:05:40 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 00:05:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 00:05:42 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:05:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 00:05:45 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 00:05:45 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 00:05:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 00:05:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 80
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 443
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 00:05:46 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 00:05:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a63a43f994064f0597fc36462d12376175178fc2c5486a9edcb36b198de411`  
		Last Modified: Sat, 27 Jan 2024 00:06:02 GMT  
		Size: 347.6 KB (347620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2327a8d9853b0ed7c134359a0fb7d0ea93d16621dd29a136c22bb30c59493703`  
		Last Modified: Sat, 27 Jan 2024 00:06:02 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71ff73f86184e48aa48d9298e97a824ab7316cc6134da0983587197e162a4d6`  
		Last Modified: Sat, 27 Jan 2024 00:06:04 GMT  
		Size: 13.9 MB (13921023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6` - linux; arm variant v7

```console
$ docker pull caddy@sha256:56128992f412b5e862c705f3ea06a9e290a1caa484f80111556fb1f13c15ce16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17147114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71cfdc5faaa533682a397011b220a59fa9e54a42f98146bfb1080c102a0ebc86`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:44:33 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 00:44:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 00:44:35 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:44:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 00:44:41 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 00:44:41 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 00:44:42 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 00:44:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 00:44:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 00:44:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 00:44:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 00:44:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 00:44:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 00:44:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 00:44:44 GMT
EXPOSE 80
# Sat, 27 Jan 2024 00:44:45 GMT
EXPOSE 443
# Sat, 27 Jan 2024 00:44:45 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 00:44:46 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 00:44:46 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 00:44:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2a6e8e98d60ee548724a36c2a41ee2f4053b409052e45ab4b015360e73c808`  
		Last Modified: Sat, 27 Jan 2024 00:45:17 GMT  
		Size: 344.5 KB (344463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9afd4ba62ae2a5b6f5ffd0c7d900582f8e684b0d45670317b63e3b8f51dc9b`  
		Last Modified: Sat, 27 Jan 2024 00:45:17 GMT  
		Size: 7.5 KB (7527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b8e42e4efab7a06b51ee74ffac1bca9bf70812dd543cb7ab60135515565e13`  
		Last Modified: Sat, 27 Jan 2024 00:45:20 GMT  
		Size: 13.9 MB (13893732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:2ec95d40ce2d1f18f92eee012a5dd18b352075d92eb6c4f4e0ea18c46ad4b069
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09733d8f0611adb987aea99d5144981331f8b6de5c2397bef43678ba50066f4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:44:36 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 03:44:38 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 03:44:38 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:44:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 03:44:40 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 03:44:40 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 80
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 443
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 03:44:41 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 03:44:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8d53bc0303fbf7f349016b59b6ac8710ba2639505e276c3816ecca679bdac7`  
		Last Modified: Sat, 27 Jan 2024 03:44:57 GMT  
		Size: 360.7 KB (360652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764cd8cdd6e6b377bd4cd13dbb53eb18d9fc7e0045323401614398d5a85b9c65`  
		Last Modified: Sat, 27 Jan 2024 03:44:56 GMT  
		Size: 7.5 KB (7526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00acba9333616526f5fc17192a0abd4e29624bba1500c6068db189bdcbee5468`  
		Last Modified: Sat, 27 Jan 2024 03:44:58 GMT  
		Size: 13.6 MB (13568965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6` - linux; ppc64le

```console
$ docker pull caddy@sha256:53a5136ccffab422016068b77862678ad9b19430fc52f7e911188703d0123939
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17052070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9c424cec6fbefc3fd4578ed97634fbe37d2590a0e474a0dce3a35ff23a8352`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:48:34 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 00:48:36 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 00:48:36 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:48:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 00:48:41 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 00:48:41 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 00:48:42 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 00:48:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 00:48:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 00:48:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 00:48:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 00:48:44 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 00:48:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 00:48:45 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 00:48:45 GMT
EXPOSE 80
# Sat, 27 Jan 2024 00:48:46 GMT
EXPOSE 443
# Sat, 27 Jan 2024 00:48:46 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 00:48:47 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 00:48:47 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 00:48:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5469759827ceaac50f13afad48892591b541bff7fa92b64936e2059ba28db3`  
		Last Modified: Sat, 27 Jan 2024 00:49:05 GMT  
		Size: 362.2 KB (362186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2c06e0d1950f2257265e78e914ebe1d4e1b0cfbfc32ba881b844fd13beb05b`  
		Last Modified: Sat, 27 Jan 2024 00:49:05 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2689e7d4f2d85097f8a724b4e3e41a875ff392132743a088b133a4d6802f6238`  
		Last Modified: Sat, 27 Jan 2024 00:49:07 GMT  
		Size: 13.3 MB (13333868 bytes)  
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

### `caddy:2.7.6` - windows version 10.0.20348.2227; amd64

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

### `caddy:2.7.6` - windows version 10.0.17763.5329; amd64

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

## `caddy:2.7.6-alpine`

```console
$ docker pull caddy@sha256:80ca561981768b2c3568cc4bef3d4cd1f11c2a625c806bedeb8453aef98779a0
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
$ docker pull caddy@sha256:67d0aa24ce021bee77049ddd2c0cc64732dd43d04598085ec39f950a13981bd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18467338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66978cebfbcc9c0a17709b108582a40a369c525c764e9a8882f6cae260b32f4d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:39:14 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 03:39:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 03:39:16 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:39:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 03:39:18 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 03:39:18 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 03:39:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 80
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 443
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 03:39:19 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 03:39:19 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf3211613d439d6da6e22998ce1ca109a902f861e1c1d55f59750636c8b7dc`  
		Last Modified: Sat, 27 Jan 2024 03:39:38 GMT  
		Size: 350.8 KB (350837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3505501083aeee1ff957f129e7d5dbdec0a32b80fee88cba62665e91547eeee0`  
		Last Modified: Sat, 27 Jan 2024 03:39:38 GMT  
		Size: 7.5 KB (7523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcbb25232b8128478b3c2ba4fe7e03fafdbf5024b74db396eef024b547f95ca`  
		Last Modified: Sat, 27 Jan 2024 03:39:40 GMT  
		Size: 14.7 MB (14706436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:6fb5cfba87d2f8f1e7f89e7f61fad3a9e2ef76dc7f58aaffdf5af8997dc6dac4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17423230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3a842d1153c178390b3187d16d1ea0f4d691fd1c72bc5fd0a2ff32c6915a02`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:05:40 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 00:05:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 00:05:42 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:05:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 00:05:45 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 00:05:45 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 00:05:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 00:05:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 80
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 443
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 00:05:46 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 00:05:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a63a43f994064f0597fc36462d12376175178fc2c5486a9edcb36b198de411`  
		Last Modified: Sat, 27 Jan 2024 00:06:02 GMT  
		Size: 347.6 KB (347620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2327a8d9853b0ed7c134359a0fb7d0ea93d16621dd29a136c22bb30c59493703`  
		Last Modified: Sat, 27 Jan 2024 00:06:02 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71ff73f86184e48aa48d9298e97a824ab7316cc6134da0983587197e162a4d6`  
		Last Modified: Sat, 27 Jan 2024 00:06:04 GMT  
		Size: 13.9 MB (13921023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:56128992f412b5e862c705f3ea06a9e290a1caa484f80111556fb1f13c15ce16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17147114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71cfdc5faaa533682a397011b220a59fa9e54a42f98146bfb1080c102a0ebc86`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:44:33 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 00:44:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 00:44:35 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:44:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 00:44:41 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 00:44:41 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 00:44:42 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 00:44:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 00:44:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 00:44:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 00:44:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 00:44:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 00:44:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 00:44:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 00:44:44 GMT
EXPOSE 80
# Sat, 27 Jan 2024 00:44:45 GMT
EXPOSE 443
# Sat, 27 Jan 2024 00:44:45 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 00:44:46 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 00:44:46 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 00:44:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2a6e8e98d60ee548724a36c2a41ee2f4053b409052e45ab4b015360e73c808`  
		Last Modified: Sat, 27 Jan 2024 00:45:17 GMT  
		Size: 344.5 KB (344463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9afd4ba62ae2a5b6f5ffd0c7d900582f8e684b0d45670317b63e3b8f51dc9b`  
		Last Modified: Sat, 27 Jan 2024 00:45:17 GMT  
		Size: 7.5 KB (7527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b8e42e4efab7a06b51ee74ffac1bca9bf70812dd543cb7ab60135515565e13`  
		Last Modified: Sat, 27 Jan 2024 00:45:20 GMT  
		Size: 13.9 MB (13893732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:2ec95d40ce2d1f18f92eee012a5dd18b352075d92eb6c4f4e0ea18c46ad4b069
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09733d8f0611adb987aea99d5144981331f8b6de5c2397bef43678ba50066f4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:44:36 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 03:44:38 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 03:44:38 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:44:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 03:44:40 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 03:44:40 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 80
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 443
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 03:44:41 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 03:44:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8d53bc0303fbf7f349016b59b6ac8710ba2639505e276c3816ecca679bdac7`  
		Last Modified: Sat, 27 Jan 2024 03:44:57 GMT  
		Size: 360.7 KB (360652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764cd8cdd6e6b377bd4cd13dbb53eb18d9fc7e0045323401614398d5a85b9c65`  
		Last Modified: Sat, 27 Jan 2024 03:44:56 GMT  
		Size: 7.5 KB (7526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00acba9333616526f5fc17192a0abd4e29624bba1500c6068db189bdcbee5468`  
		Last Modified: Sat, 27 Jan 2024 03:44:58 GMT  
		Size: 13.6 MB (13568965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:53a5136ccffab422016068b77862678ad9b19430fc52f7e911188703d0123939
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17052070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9c424cec6fbefc3fd4578ed97634fbe37d2590a0e474a0dce3a35ff23a8352`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:48:34 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 00:48:36 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 00:48:36 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:48:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 00:48:41 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 00:48:41 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 00:48:42 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 00:48:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 00:48:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 00:48:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 00:48:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 00:48:44 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 00:48:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 00:48:45 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 00:48:45 GMT
EXPOSE 80
# Sat, 27 Jan 2024 00:48:46 GMT
EXPOSE 443
# Sat, 27 Jan 2024 00:48:46 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 00:48:47 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 00:48:47 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 00:48:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5469759827ceaac50f13afad48892591b541bff7fa92b64936e2059ba28db3`  
		Last Modified: Sat, 27 Jan 2024 00:49:05 GMT  
		Size: 362.2 KB (362186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2c06e0d1950f2257265e78e914ebe1d4e1b0cfbfc32ba881b844fd13beb05b`  
		Last Modified: Sat, 27 Jan 2024 00:49:05 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2689e7d4f2d85097f8a724b4e3e41a875ff392132743a088b133a4d6802f6238`  
		Last Modified: Sat, 27 Jan 2024 00:49:07 GMT  
		Size: 13.3 MB (13333868 bytes)  
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
$ docker pull caddy@sha256:42442569a853bd5e5ce825d52baaee3fc919d1fa0e2fb7b9db30f246bec05c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `caddy:2.7.6-builder` - linux; amd64

```console
$ docker pull caddy@sha256:09513acee0757eaafeea861313a51d37b907cde693899b4d85bffa691d7eca06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77024166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e2950806b4846bc8384039f8e0ced6b55a43843627c3c7bcb574d00da87e36`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 03:39:23 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 03:39:23 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 03:39:24 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:39:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 03:39:24 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 03:39:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 03:39:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 03:39:25 GMT
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
	-	`sha256:c4b77ba268427b27996c293cddcbb1af065ac97d6f64fff6d3ee0adce318de44`  
		Last Modified: Sat, 27 Jan 2024 01:37:37 GMT  
		Size: 67.1 MB (67061623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5c147192a9317b4f575377244f4c3d96df9c9108d6147e10cd2becfdcfdc75`  
		Last Modified: Sat, 27 Jan 2024 01:37:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426789fa51aac91ce386d0cf62e3c5b4fd91cc19da6cb9449035a1aad2a1cb4b`  
		Last Modified: Sat, 27 Jan 2024 03:39:53 GMT  
		Size: 5.0 MB (4972458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848439cf5d4cf7d00a316abe8d0c04005a28d2e60f11875549cbbeec7db5cafc`  
		Last Modified: Sat, 27 Jan 2024 03:39:53 GMT  
		Size: 1.3 MB (1302243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61744c717cfe93977f876b739f3c692e919bb8cf098d233db8af67c532d77cd`  
		Last Modified: Sat, 27 Jan 2024 03:39:52 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:f7f15d8dc37358732c441ac4c62c2ac4967b16eb93863621dfc5cacf0b9dc1c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75479956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b694cc61283aebb38db78010935fc8281778bc08c35e7816a8c8819d3727a6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 13:22:00 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 13:22:00 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 13:22:00 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 13:22:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 13:22:01 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 13:22:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 13:22:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 13:22:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6033bb349d654a4ba7602191ed0372313ceca193751253005ad66a23d4dcb0ec`  
		Last Modified: Sat, 27 Jan 2024 09:20:38 GMT  
		Size: 284.9 KB (284872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31e5472cbeca7cc0b8f9272fbe547db898349f9b598c6b975f2c4efeeb63aee`  
		Last Modified: Sat, 27 Jan 2024 09:21:48 GMT  
		Size: 65.8 MB (65832091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b979a15e6ae0ded8491c78ec0740e6ece1aaaa584d10fdb89131c53427aba66`  
		Last Modified: Sat, 27 Jan 2024 09:21:32 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31abdea622b745b38e9215bf8062f71c377f48b2049bf07a5cd650743c069abb`  
		Last Modified: Sat, 27 Jan 2024 13:22:18 GMT  
		Size: 5.0 MB (4966664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f06e6a7ead4077a0b30ee09128ded6d14cd9bd7f450ef457f559c9e5b59938`  
		Last Modified: Sat, 27 Jan 2024 13:22:18 GMT  
		Size: 1.2 MB (1248661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba060f027200c3446f1acab0c00b2f4a9e8acf8610c46591daa3d8d7434aafd`  
		Last Modified: Sat, 27 Jan 2024 13:22:17 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:c80d0eabc3c5c1e92b026b7e2c2c35b4783472f984fe455da2ddddedce5b416c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25cc1ad71b8526356adff18f79ddbb3ff658a705a74e76800ee8f8172d4551f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 21:55:58 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:55:58 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:55:58 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:55:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:55:59 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:56:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:56:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:56:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf835181e2f4c73f7de0fe69c219658c3feddb5ba4e6850bc5b5af9555c08d1`  
		Last Modified: Sat, 27 Jan 2024 00:41:32 GMT  
		Size: 284.1 KB (284079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e2cd4f5b6025c32b2853d34aa0bcf57d85f2d44b2e412e2ba4e6dd0159ac1f`  
		Last Modified: Tue, 06 Feb 2024 21:29:51 GMT  
		Size: 65.8 MB (65767453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d160b5a79dd98fde6c0642c78daa3c77f077ad44a16b27b65a3b24fff23c603f`  
		Last Modified: Tue, 06 Feb 2024 21:29:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5735d56095a062d062dbd8c2d92cff873a457010035f0a7bf754444cdda79e1`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 4.5 MB (4514266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e601fac0470697a15f02c34e269f0e19119d88f46ffbcdddc5300417e3aab4b`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 1.2 MB (1246089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caff9a4e5a9e81ccc2e586bdbd72039b0d2bcc929751e08afbcffd6dbff11931`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:31f32db6814a94ad3cac5661dbda0a586162eb0b22b3e6ccdeb3e72b55cb9b76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73998584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c56aa1b8e6d877694eff62d87142b579cb7d523e8f22c16615b9ec3c5e3bae3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 21:33:04 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:33:04 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:33:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:33:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:33:06 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e59bef827dc10d9c33cdf4762faf3f2987df2a0296378e2349ec6d5bc6a37f4`  
		Last Modified: Sat, 27 Jan 2024 05:33:17 GMT  
		Size: 286.3 KB (286302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328d8fad75fb04ebff991b2c11c5988722931b5300239657bc1b4961655df05f`  
		Last Modified: Tue, 06 Feb 2024 20:50:08 GMT  
		Size: 64.1 MB (64109254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62899699addead1db84d09ab10dc0a0cbde16beb64c81cde0f84af2fa9b30f39`  
		Last Modified: Tue, 06 Feb 2024 20:50:00 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1745cea878add1608edd8710a879d4925a33b6e27329531c9c1cdd2c0e79c91a`  
		Last Modified: Tue, 06 Feb 2024 21:33:21 GMT  
		Size: 5.1 MB (5070613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235f6d9da6844caff2a0af124b9c01f0bf0abd2be340e5d2c67ab135a7cca76d`  
		Last Modified: Tue, 06 Feb 2024 21:33:21 GMT  
		Size: 1.2 MB (1198444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca8afc86b60749044b9b64230a9f9c67c20aa089b99562732169c4e6a807628`  
		Last Modified: Tue, 06 Feb 2024 21:33:20 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:b4effdad9be7ca7509b54d46638823940081fdf20f3000aaf9b3a691ace61f17
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74213039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10cf81cb43dc269c0ea9f820417d703e172313e228a17bdf7cffe96f4d2e742`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 21:14:22 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:14:22 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:14:23 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:14:23 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:14:24 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:14:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:14:27 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:14:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f92ca388ce06d6dddf0b5ad5ca0d5b82049994f1ad4da72bb5e48c5783dc009`  
		Last Modified: Sat, 27 Jan 2024 01:13:46 GMT  
		Size: 286.7 KB (286665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ef3661c7b713c28d8e0ae3c73dc823022f6a6e8a65c6fd2f00aa13dd6be4e4`  
		Last Modified: Tue, 06 Feb 2024 20:39:21 GMT  
		Size: 64.1 MB (64120440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7f0aa3654740d4016d469bad05baafdfc3be78e2f6ebc6f938501a1f4cd056`  
		Last Modified: Tue, 06 Feb 2024 20:39:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53242ccbc16994912810b389fdd1f7cb7cb1a3223cec7dcac1d4d00340e2f6de`  
		Last Modified: Tue, 06 Feb 2024 21:14:45 GMT  
		Size: 5.3 MB (5270660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c055ede766eec14283da8e4f87ab21f6a84f8ceff065d702bc31c9bf9ef23757`  
		Last Modified: Tue, 06 Feb 2024 21:14:45 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbe5c0b6966115344269e3c2b83ef21af0ebd897ee5a670604887f27d3da882`  
		Last Modified: Tue, 06 Feb 2024 21:14:44 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; s390x

```console
$ docker pull caddy@sha256:25c4422b5cf06de48acecb96441e14f50db37a05c9353138f1f0f8b476680bb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76167035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06a921e90d95d0edd27e62d87f24a3fced554bde075b4b48f9099611fecb599`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 14:17:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 14:17:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 14:17:32 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 14:17:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 14:17:33 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 14:17:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 14:17:36 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 14:17:36 GMT
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
	-	`sha256:b94763531102ae1af628e5b55ca073b0c0fbd6aab9f221a28f3895303ddd975d`  
		Last Modified: Sat, 27 Jan 2024 05:47:26 GMT  
		Size: 66.3 MB (66284463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd03f53bee613b790f5b2286c4561428b2b2da6234df368a3a50d5ad91d58b9a`  
		Last Modified: Sat, 27 Jan 2024 05:47:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c299d55132b1737b4877e997f9881e05bd66727a05f8502f6fc38969031381ce`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 5.1 MB (5116950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60611bccc71deeef6872096a6f8a89a7e7af13c5027eb639b2ee7c182855d85`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 1.3 MB (1262387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fda9b2eed36da0393b2486d62a5c2c8ed03d6f3e38b27aae0fb6a57259b22e`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - windows version 10.0.20348.2227; amd64

```console
$ docker pull caddy@sha256:4814d63f1ac1d7e2334ff267279eed3b5533e0f94ad926fe9b3f11064e087406
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1997072166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d833851f7e1c400f60d5591428c91912a576258fb5b2fd93a0cdd0b228b07d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jan 2024 23:22:59 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Jan 2024 23:23:00 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Jan 2024 23:23:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Jan 2024 23:23:02 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Jan 2024 23:23:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Jan 2024 23:23:36 GMT
ENV GOPATH=C:\go
# Wed, 10 Jan 2024 23:23:55 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 Feb 2024 20:15:33 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 20:17:57 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 Feb 2024 20:17:58 GMT
WORKDIR C:\go
# Tue, 06 Feb 2024 21:01:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Feb 2024 21:01:18 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:01:19 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:01:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:01:44 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 06 Feb 2024 21:01:45 GMT
WORKDIR C:\
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
	-	`sha256:a3069ddb372bc0087899e61a271374e1b4423cfd9056ff2725874a89af15c2a1`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0841fad0c7557916603463fc9615983e0ad786338880d3d99c005dd50ecf3b6`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d1ae6fa2010fb779b06f0fc8a74830b01c9a87769fc35818fccdd5b7e7ea45`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4cd94fbe72557ed410a8f0aa0361ffc9ec2b2ecd96dc803b91c5ce0f34d077`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b3e385378ebc3f79f2c065897b323f0b1cfc97f3f8979c4530d0791e3e9523`  
		Last Modified: Thu, 11 Jan 2024 00:01:30 GMT  
		Size: 25.5 MB (25529890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbdf5bbf3fb6a215313abb55339dcee6260ef50d2c50d2b781476d5af12e840`  
		Last Modified: Thu, 11 Jan 2024 00:01:23 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7fd79e14c60629d3157a4363f602b919ba92aa10209a2e6ac40b7c86a75316`  
		Last Modified: Thu, 11 Jan 2024 00:01:23 GMT  
		Size: 261.7 KB (261737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d6abeee495b14ea2e44bb00f28c38212af6d923a1d5c148dd3eb083e1788d2`  
		Last Modified: Tue, 06 Feb 2024 20:38:27 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699b8adf45cf387aabdaea0b829e6bf5dee7a05e7eaf5519d3b0f5fe071e14a`  
		Last Modified: Tue, 06 Feb 2024 20:38:45 GMT  
		Size: 69.4 MB (69373765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd60a6e8aaafdd337241c619e2cd664dbfd6052a133b148c86845f227a25ea14`  
		Last Modified: Tue, 06 Feb 2024 20:38:27 GMT  
		Size: 1.5 KB (1531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6796689d52835dc674b67907c3e03bb20425e0e76be6963eaeb04e035d2c7f`  
		Last Modified: Tue, 06 Feb 2024 21:02:41 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657c487d0aab792a6141c8f2b5d1ef4564310178c60f883cb8e301cb752930ff`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bcd5a55d300a69a6a7202fda4cdb55a8e4f3645145c962279bc958c9efdf5a`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f9fc1b6232aab1694132043a6674117073dc98b00635546605582fabd31300`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005f7ea8d310ffb3ab0f46fbb75e4a90192f694357210b16fa4867a1c593cf2e`  
		Last Modified: Tue, 06 Feb 2024 21:02:39 GMT  
		Size: 1.7 MB (1675717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f756efa4d252460db4055d7da93b4667f4b1537f46882db730596bac57eb677`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - windows version 10.0.17763.5329; amd64

```console
$ docker pull caddy@sha256:882f417e3efb3b9a8d1ade5245808ac22c5c1ea57a1352c72b6652b3a3238ecf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2166627810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6206308760870c6bbbd479176af11a35608423c94c08b69c418649ce2d281f3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jan 2024 23:26:43 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Jan 2024 23:26:44 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Jan 2024 23:26:45 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Jan 2024 23:26:46 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Jan 2024 23:28:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Jan 2024 23:28:09 GMT
ENV GOPATH=C:\go
# Wed, 10 Jan 2024 23:29:17 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 Feb 2024 20:18:16 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 20:21:36 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 Feb 2024 20:21:37 GMT
WORKDIR C:\go
# Tue, 06 Feb 2024 20:59:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Feb 2024 20:59:49 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 20:59:50 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 20:59:51 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:01:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 06 Feb 2024 21:01:01 GMT
WORKDIR C:\
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
	-	`sha256:58a2d0f9e9eca6932479b4446cdad2350fe376cd5102106ac4938d8552073ee1`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3baf188f2343abdd0b6b9307f8adcc91c698473839c28dbba9e3b50117d7df5`  
		Last Modified: Thu, 11 Jan 2024 00:03:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83f321def9731da0b67b8c9c7c573a95237ff9d906d16394dfc3dd845bd806`  
		Last Modified: Thu, 11 Jan 2024 00:03:01 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3185717e4484ba21a137fb6d471a72ee842364637f999013cbd8b7a633ccfa`  
		Last Modified: Thu, 11 Jan 2024 00:03:01 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d432d7f01be369829a69831b58f259bc1d30ccb67bc46a16211f95454e2d026b`  
		Last Modified: Thu, 11 Jan 2024 00:03:06 GMT  
		Size: 25.6 MB (25555277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481ab54aaa7ea3f3af1db424c6fda8a4bf6e63fe0bc92e2e319db55c66952d5`  
		Last Modified: Thu, 11 Jan 2024 00:02:59 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4579730b543c234b271242a1f8b94332944911daa12fe4493f4daad09e6e6a1`  
		Last Modified: Thu, 11 Jan 2024 00:02:59 GMT  
		Size: 284.0 KB (284031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57342fc3b749de0a8e32c9f1f9eece3c3855ea5d8b63b70682518058c40ba349`  
		Last Modified: Tue, 06 Feb 2024 20:38:59 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d092fd3744c0081064bac79e4fb322e2f6e9d0d8e744bb837bccd7f9b844e8`  
		Last Modified: Tue, 06 Feb 2024 20:39:17 GMT  
		Size: 69.4 MB (69370513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a8538533cb5606cc3e717f0431791fcd99ca7c1b935f5586f465bbd0c9d457`  
		Last Modified: Tue, 06 Feb 2024 20:38:59 GMT  
		Size: 1.6 KB (1586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ba50226998b42d6500ba479c1fbf0f3e588807488f728c91715ac893e69838`  
		Last Modified: Tue, 06 Feb 2024 21:02:24 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74292b50264f2db380dc5a9a8baaa5d229ff8efd2699e40fc6f478a25d59c0d0`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e574cef27624cb2b445968d4f051529c8c02dc6bf599ea131f51164de4939536`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14832cf23b08465f9e60489cda03b116fb6be01de86762232ed2f3b3aa8cf2a4`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e89456cebd7c16015a94dda1edb8a055ef730bc8c289b8eae13b1867371376f`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.7 MB (1677010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874ea9f0878170aeeae3da252653488f0677348bdb3f6cd9a87ccb3d064bde10`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder-alpine`

```console
$ docker pull caddy@sha256:8a0f239bbd24b1a0973d0e3e22ef69d2e9f27b2f860c50247deead9c47b8b81e
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
$ docker pull caddy@sha256:09513acee0757eaafeea861313a51d37b907cde693899b4d85bffa691d7eca06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77024166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e2950806b4846bc8384039f8e0ced6b55a43843627c3c7bcb574d00da87e36`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 03:39:23 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 03:39:23 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 03:39:24 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:39:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 03:39:24 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 03:39:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 03:39:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 03:39:25 GMT
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
	-	`sha256:c4b77ba268427b27996c293cddcbb1af065ac97d6f64fff6d3ee0adce318de44`  
		Last Modified: Sat, 27 Jan 2024 01:37:37 GMT  
		Size: 67.1 MB (67061623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5c147192a9317b4f575377244f4c3d96df9c9108d6147e10cd2becfdcfdc75`  
		Last Modified: Sat, 27 Jan 2024 01:37:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426789fa51aac91ce386d0cf62e3c5b4fd91cc19da6cb9449035a1aad2a1cb4b`  
		Last Modified: Sat, 27 Jan 2024 03:39:53 GMT  
		Size: 5.0 MB (4972458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848439cf5d4cf7d00a316abe8d0c04005a28d2e60f11875549cbbeec7db5cafc`  
		Last Modified: Sat, 27 Jan 2024 03:39:53 GMT  
		Size: 1.3 MB (1302243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61744c717cfe93977f876b739f3c692e919bb8cf098d233db8af67c532d77cd`  
		Last Modified: Sat, 27 Jan 2024 03:39:52 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:f7f15d8dc37358732c441ac4c62c2ac4967b16eb93863621dfc5cacf0b9dc1c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75479956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b694cc61283aebb38db78010935fc8281778bc08c35e7816a8c8819d3727a6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 13:22:00 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 13:22:00 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 13:22:00 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 13:22:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 13:22:01 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 13:22:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 13:22:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 13:22:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6033bb349d654a4ba7602191ed0372313ceca193751253005ad66a23d4dcb0ec`  
		Last Modified: Sat, 27 Jan 2024 09:20:38 GMT  
		Size: 284.9 KB (284872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31e5472cbeca7cc0b8f9272fbe547db898349f9b598c6b975f2c4efeeb63aee`  
		Last Modified: Sat, 27 Jan 2024 09:21:48 GMT  
		Size: 65.8 MB (65832091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b979a15e6ae0ded8491c78ec0740e6ece1aaaa584d10fdb89131c53427aba66`  
		Last Modified: Sat, 27 Jan 2024 09:21:32 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31abdea622b745b38e9215bf8062f71c377f48b2049bf07a5cd650743c069abb`  
		Last Modified: Sat, 27 Jan 2024 13:22:18 GMT  
		Size: 5.0 MB (4966664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f06e6a7ead4077a0b30ee09128ded6d14cd9bd7f450ef457f559c9e5b59938`  
		Last Modified: Sat, 27 Jan 2024 13:22:18 GMT  
		Size: 1.2 MB (1248661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba060f027200c3446f1acab0c00b2f4a9e8acf8610c46591daa3d8d7434aafd`  
		Last Modified: Sat, 27 Jan 2024 13:22:17 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:c80d0eabc3c5c1e92b026b7e2c2c35b4783472f984fe455da2ddddedce5b416c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25cc1ad71b8526356adff18f79ddbb3ff658a705a74e76800ee8f8172d4551f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 21:55:58 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:55:58 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:55:58 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:55:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:55:59 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:56:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:56:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:56:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf835181e2f4c73f7de0fe69c219658c3feddb5ba4e6850bc5b5af9555c08d1`  
		Last Modified: Sat, 27 Jan 2024 00:41:32 GMT  
		Size: 284.1 KB (284079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e2cd4f5b6025c32b2853d34aa0bcf57d85f2d44b2e412e2ba4e6dd0159ac1f`  
		Last Modified: Tue, 06 Feb 2024 21:29:51 GMT  
		Size: 65.8 MB (65767453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d160b5a79dd98fde6c0642c78daa3c77f077ad44a16b27b65a3b24fff23c603f`  
		Last Modified: Tue, 06 Feb 2024 21:29:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5735d56095a062d062dbd8c2d92cff873a457010035f0a7bf754444cdda79e1`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 4.5 MB (4514266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e601fac0470697a15f02c34e269f0e19119d88f46ffbcdddc5300417e3aab4b`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 1.2 MB (1246089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caff9a4e5a9e81ccc2e586bdbd72039b0d2bcc929751e08afbcffd6dbff11931`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:31f32db6814a94ad3cac5661dbda0a586162eb0b22b3e6ccdeb3e72b55cb9b76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73998584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c56aa1b8e6d877694eff62d87142b579cb7d523e8f22c16615b9ec3c5e3bae3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 21:33:04 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:33:04 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:33:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:33:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:33:06 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e59bef827dc10d9c33cdf4762faf3f2987df2a0296378e2349ec6d5bc6a37f4`  
		Last Modified: Sat, 27 Jan 2024 05:33:17 GMT  
		Size: 286.3 KB (286302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328d8fad75fb04ebff991b2c11c5988722931b5300239657bc1b4961655df05f`  
		Last Modified: Tue, 06 Feb 2024 20:50:08 GMT  
		Size: 64.1 MB (64109254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62899699addead1db84d09ab10dc0a0cbde16beb64c81cde0f84af2fa9b30f39`  
		Last Modified: Tue, 06 Feb 2024 20:50:00 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1745cea878add1608edd8710a879d4925a33b6e27329531c9c1cdd2c0e79c91a`  
		Last Modified: Tue, 06 Feb 2024 21:33:21 GMT  
		Size: 5.1 MB (5070613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235f6d9da6844caff2a0af124b9c01f0bf0abd2be340e5d2c67ab135a7cca76d`  
		Last Modified: Tue, 06 Feb 2024 21:33:21 GMT  
		Size: 1.2 MB (1198444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca8afc86b60749044b9b64230a9f9c67c20aa089b99562732169c4e6a807628`  
		Last Modified: Tue, 06 Feb 2024 21:33:20 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:b4effdad9be7ca7509b54d46638823940081fdf20f3000aaf9b3a691ace61f17
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74213039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10cf81cb43dc269c0ea9f820417d703e172313e228a17bdf7cffe96f4d2e742`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 21:14:22 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:14:22 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:14:23 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:14:23 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:14:24 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:14:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:14:27 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:14:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f92ca388ce06d6dddf0b5ad5ca0d5b82049994f1ad4da72bb5e48c5783dc009`  
		Last Modified: Sat, 27 Jan 2024 01:13:46 GMT  
		Size: 286.7 KB (286665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ef3661c7b713c28d8e0ae3c73dc823022f6a6e8a65c6fd2f00aa13dd6be4e4`  
		Last Modified: Tue, 06 Feb 2024 20:39:21 GMT  
		Size: 64.1 MB (64120440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7f0aa3654740d4016d469bad05baafdfc3be78e2f6ebc6f938501a1f4cd056`  
		Last Modified: Tue, 06 Feb 2024 20:39:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53242ccbc16994912810b389fdd1f7cb7cb1a3223cec7dcac1d4d00340e2f6de`  
		Last Modified: Tue, 06 Feb 2024 21:14:45 GMT  
		Size: 5.3 MB (5270660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c055ede766eec14283da8e4f87ab21f6a84f8ceff065d702bc31c9bf9ef23757`  
		Last Modified: Tue, 06 Feb 2024 21:14:45 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbe5c0b6966115344269e3c2b83ef21af0ebd897ee5a670604887f27d3da882`  
		Last Modified: Tue, 06 Feb 2024 21:14:44 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:25c4422b5cf06de48acecb96441e14f50db37a05c9353138f1f0f8b476680bb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76167035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06a921e90d95d0edd27e62d87f24a3fced554bde075b4b48f9099611fecb599`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 14:17:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 14:17:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 14:17:32 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 14:17:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 14:17:33 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 14:17:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 14:17:36 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 14:17:36 GMT
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
	-	`sha256:b94763531102ae1af628e5b55ca073b0c0fbd6aab9f221a28f3895303ddd975d`  
		Last Modified: Sat, 27 Jan 2024 05:47:26 GMT  
		Size: 66.3 MB (66284463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd03f53bee613b790f5b2286c4561428b2b2da6234df368a3a50d5ad91d58b9a`  
		Last Modified: Sat, 27 Jan 2024 05:47:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c299d55132b1737b4877e997f9881e05bd66727a05f8502f6fc38969031381ce`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 5.1 MB (5116950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60611bccc71deeef6872096a6f8a89a7e7af13c5027eb639b2ee7c182855d85`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 1.3 MB (1262387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fda9b2eed36da0393b2486d62a5c2c8ed03d6f3e38b27aae0fb6a57259b22e`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:e794dda1d2a08c7fe472d7b929a4d86621c3ea9ac1252d7fe1134e724a2115a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `caddy:2.7.6-builder-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull caddy@sha256:882f417e3efb3b9a8d1ade5245808ac22c5c1ea57a1352c72b6652b3a3238ecf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2166627810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6206308760870c6bbbd479176af11a35608423c94c08b69c418649ce2d281f3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jan 2024 23:26:43 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Jan 2024 23:26:44 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Jan 2024 23:26:45 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Jan 2024 23:26:46 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Jan 2024 23:28:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Jan 2024 23:28:09 GMT
ENV GOPATH=C:\go
# Wed, 10 Jan 2024 23:29:17 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 Feb 2024 20:18:16 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 20:21:36 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 Feb 2024 20:21:37 GMT
WORKDIR C:\go
# Tue, 06 Feb 2024 20:59:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Feb 2024 20:59:49 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 20:59:50 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 20:59:51 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:01:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 06 Feb 2024 21:01:01 GMT
WORKDIR C:\
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
	-	`sha256:58a2d0f9e9eca6932479b4446cdad2350fe376cd5102106ac4938d8552073ee1`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3baf188f2343abdd0b6b9307f8adcc91c698473839c28dbba9e3b50117d7df5`  
		Last Modified: Thu, 11 Jan 2024 00:03:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83f321def9731da0b67b8c9c7c573a95237ff9d906d16394dfc3dd845bd806`  
		Last Modified: Thu, 11 Jan 2024 00:03:01 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3185717e4484ba21a137fb6d471a72ee842364637f999013cbd8b7a633ccfa`  
		Last Modified: Thu, 11 Jan 2024 00:03:01 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d432d7f01be369829a69831b58f259bc1d30ccb67bc46a16211f95454e2d026b`  
		Last Modified: Thu, 11 Jan 2024 00:03:06 GMT  
		Size: 25.6 MB (25555277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481ab54aaa7ea3f3af1db424c6fda8a4bf6e63fe0bc92e2e319db55c66952d5`  
		Last Modified: Thu, 11 Jan 2024 00:02:59 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4579730b543c234b271242a1f8b94332944911daa12fe4493f4daad09e6e6a1`  
		Last Modified: Thu, 11 Jan 2024 00:02:59 GMT  
		Size: 284.0 KB (284031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57342fc3b749de0a8e32c9f1f9eece3c3855ea5d8b63b70682518058c40ba349`  
		Last Modified: Tue, 06 Feb 2024 20:38:59 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d092fd3744c0081064bac79e4fb322e2f6e9d0d8e744bb837bccd7f9b844e8`  
		Last Modified: Tue, 06 Feb 2024 20:39:17 GMT  
		Size: 69.4 MB (69370513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a8538533cb5606cc3e717f0431791fcd99ca7c1b935f5586f465bbd0c9d457`  
		Last Modified: Tue, 06 Feb 2024 20:38:59 GMT  
		Size: 1.6 KB (1586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ba50226998b42d6500ba479c1fbf0f3e588807488f728c91715ac893e69838`  
		Last Modified: Tue, 06 Feb 2024 21:02:24 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74292b50264f2db380dc5a9a8baaa5d229ff8efd2699e40fc6f478a25d59c0d0`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e574cef27624cb2b445968d4f051529c8c02dc6bf599ea131f51164de4939536`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14832cf23b08465f9e60489cda03b116fb6be01de86762232ed2f3b3aa8cf2a4`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e89456cebd7c16015a94dda1edb8a055ef730bc8c289b8eae13b1867371376f`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.7 MB (1677010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874ea9f0878170aeeae3da252653488f0677348bdb3f6cd9a87ccb3d064bde10`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:97e329cd72c287551121f0de0749affc40ba296a42f67b3774c972dfc63239d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `caddy:2.7.6-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull caddy@sha256:4814d63f1ac1d7e2334ff267279eed3b5533e0f94ad926fe9b3f11064e087406
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1997072166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d833851f7e1c400f60d5591428c91912a576258fb5b2fd93a0cdd0b228b07d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jan 2024 23:22:59 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Jan 2024 23:23:00 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Jan 2024 23:23:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Jan 2024 23:23:02 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Jan 2024 23:23:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Jan 2024 23:23:36 GMT
ENV GOPATH=C:\go
# Wed, 10 Jan 2024 23:23:55 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 Feb 2024 20:15:33 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 20:17:57 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 Feb 2024 20:17:58 GMT
WORKDIR C:\go
# Tue, 06 Feb 2024 21:01:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Feb 2024 21:01:18 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:01:19 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:01:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:01:44 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 06 Feb 2024 21:01:45 GMT
WORKDIR C:\
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
	-	`sha256:a3069ddb372bc0087899e61a271374e1b4423cfd9056ff2725874a89af15c2a1`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0841fad0c7557916603463fc9615983e0ad786338880d3d99c005dd50ecf3b6`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d1ae6fa2010fb779b06f0fc8a74830b01c9a87769fc35818fccdd5b7e7ea45`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4cd94fbe72557ed410a8f0aa0361ffc9ec2b2ecd96dc803b91c5ce0f34d077`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b3e385378ebc3f79f2c065897b323f0b1cfc97f3f8979c4530d0791e3e9523`  
		Last Modified: Thu, 11 Jan 2024 00:01:30 GMT  
		Size: 25.5 MB (25529890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbdf5bbf3fb6a215313abb55339dcee6260ef50d2c50d2b781476d5af12e840`  
		Last Modified: Thu, 11 Jan 2024 00:01:23 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7fd79e14c60629d3157a4363f602b919ba92aa10209a2e6ac40b7c86a75316`  
		Last Modified: Thu, 11 Jan 2024 00:01:23 GMT  
		Size: 261.7 KB (261737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d6abeee495b14ea2e44bb00f28c38212af6d923a1d5c148dd3eb083e1788d2`  
		Last Modified: Tue, 06 Feb 2024 20:38:27 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699b8adf45cf387aabdaea0b829e6bf5dee7a05e7eaf5519d3b0f5fe071e14a`  
		Last Modified: Tue, 06 Feb 2024 20:38:45 GMT  
		Size: 69.4 MB (69373765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd60a6e8aaafdd337241c619e2cd664dbfd6052a133b148c86845f227a25ea14`  
		Last Modified: Tue, 06 Feb 2024 20:38:27 GMT  
		Size: 1.5 KB (1531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6796689d52835dc674b67907c3e03bb20425e0e76be6963eaeb04e035d2c7f`  
		Last Modified: Tue, 06 Feb 2024 21:02:41 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657c487d0aab792a6141c8f2b5d1ef4564310178c60f883cb8e301cb752930ff`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bcd5a55d300a69a6a7202fda4cdb55a8e4f3645145c962279bc958c9efdf5a`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f9fc1b6232aab1694132043a6674117073dc98b00635546605582fabd31300`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005f7ea8d310ffb3ab0f46fbb75e4a90192f694357210b16fa4867a1c593cf2e`  
		Last Modified: Tue, 06 Feb 2024 21:02:39 GMT  
		Size: 1.7 MB (1675717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f756efa4d252460db4055d7da93b4667f4b1537f46882db730596bac57eb677`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-windowsservercore`

```console
$ docker pull caddy@sha256:c6e3f25c93c35d4a519395eb595f46de5889867e37acd83bac72b8d2d9dcef3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `caddy:2.7.6-windowsservercore` - windows version 10.0.20348.2227; amd64

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

### `caddy:2.7.6-windowsservercore` - windows version 10.0.17763.5329; amd64

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

## `caddy:2.7.6-windowsservercore-1809`

```console
$ docker pull caddy@sha256:f7e06b6f876505ed8ae83c339c860ab40d8287d52669bddf6dad0302470155d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `caddy:2.7.6-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

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

## `caddy:2.7.6-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:cdb4600df8fe3e27d97f1fb21ba9d5fdb1bd8198a1f025ca2458154f28d76934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `caddy:2.7.6-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

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

## `caddy:alpine`

```console
$ docker pull caddy@sha256:80ca561981768b2c3568cc4bef3d4cd1f11c2a625c806bedeb8453aef98779a0
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
$ docker pull caddy@sha256:67d0aa24ce021bee77049ddd2c0cc64732dd43d04598085ec39f950a13981bd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18467338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66978cebfbcc9c0a17709b108582a40a369c525c764e9a8882f6cae260b32f4d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:39:14 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 03:39:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 03:39:16 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:39:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 03:39:18 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 03:39:18 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 03:39:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 80
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 443
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 03:39:19 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 03:39:19 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf3211613d439d6da6e22998ce1ca109a902f861e1c1d55f59750636c8b7dc`  
		Last Modified: Sat, 27 Jan 2024 03:39:38 GMT  
		Size: 350.8 KB (350837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3505501083aeee1ff957f129e7d5dbdec0a32b80fee88cba62665e91547eeee0`  
		Last Modified: Sat, 27 Jan 2024 03:39:38 GMT  
		Size: 7.5 KB (7523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcbb25232b8128478b3c2ba4fe7e03fafdbf5024b74db396eef024b547f95ca`  
		Last Modified: Sat, 27 Jan 2024 03:39:40 GMT  
		Size: 14.7 MB (14706436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:6fb5cfba87d2f8f1e7f89e7f61fad3a9e2ef76dc7f58aaffdf5af8997dc6dac4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17423230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3a842d1153c178390b3187d16d1ea0f4d691fd1c72bc5fd0a2ff32c6915a02`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:05:40 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 00:05:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 00:05:42 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:05:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 00:05:45 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 00:05:45 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 00:05:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 00:05:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 80
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 443
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 00:05:46 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 00:05:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a63a43f994064f0597fc36462d12376175178fc2c5486a9edcb36b198de411`  
		Last Modified: Sat, 27 Jan 2024 00:06:02 GMT  
		Size: 347.6 KB (347620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2327a8d9853b0ed7c134359a0fb7d0ea93d16621dd29a136c22bb30c59493703`  
		Last Modified: Sat, 27 Jan 2024 00:06:02 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71ff73f86184e48aa48d9298e97a824ab7316cc6134da0983587197e162a4d6`  
		Last Modified: Sat, 27 Jan 2024 00:06:04 GMT  
		Size: 13.9 MB (13921023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:56128992f412b5e862c705f3ea06a9e290a1caa484f80111556fb1f13c15ce16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17147114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71cfdc5faaa533682a397011b220a59fa9e54a42f98146bfb1080c102a0ebc86`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:44:33 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 00:44:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 00:44:35 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:44:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 00:44:41 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 00:44:41 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 00:44:42 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 00:44:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 00:44:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 00:44:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 00:44:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 00:44:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 00:44:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 00:44:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 00:44:44 GMT
EXPOSE 80
# Sat, 27 Jan 2024 00:44:45 GMT
EXPOSE 443
# Sat, 27 Jan 2024 00:44:45 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 00:44:46 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 00:44:46 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 00:44:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2a6e8e98d60ee548724a36c2a41ee2f4053b409052e45ab4b015360e73c808`  
		Last Modified: Sat, 27 Jan 2024 00:45:17 GMT  
		Size: 344.5 KB (344463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9afd4ba62ae2a5b6f5ffd0c7d900582f8e684b0d45670317b63e3b8f51dc9b`  
		Last Modified: Sat, 27 Jan 2024 00:45:17 GMT  
		Size: 7.5 KB (7527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b8e42e4efab7a06b51ee74ffac1bca9bf70812dd543cb7ab60135515565e13`  
		Last Modified: Sat, 27 Jan 2024 00:45:20 GMT  
		Size: 13.9 MB (13893732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:2ec95d40ce2d1f18f92eee012a5dd18b352075d92eb6c4f4e0ea18c46ad4b069
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09733d8f0611adb987aea99d5144981331f8b6de5c2397bef43678ba50066f4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:44:36 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 03:44:38 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 03:44:38 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:44:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 03:44:40 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 03:44:40 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 80
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 443
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 03:44:41 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 03:44:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8d53bc0303fbf7f349016b59b6ac8710ba2639505e276c3816ecca679bdac7`  
		Last Modified: Sat, 27 Jan 2024 03:44:57 GMT  
		Size: 360.7 KB (360652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764cd8cdd6e6b377bd4cd13dbb53eb18d9fc7e0045323401614398d5a85b9c65`  
		Last Modified: Sat, 27 Jan 2024 03:44:56 GMT  
		Size: 7.5 KB (7526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00acba9333616526f5fc17192a0abd4e29624bba1500c6068db189bdcbee5468`  
		Last Modified: Sat, 27 Jan 2024 03:44:58 GMT  
		Size: 13.6 MB (13568965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:53a5136ccffab422016068b77862678ad9b19430fc52f7e911188703d0123939
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17052070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9c424cec6fbefc3fd4578ed97634fbe37d2590a0e474a0dce3a35ff23a8352`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:48:34 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 00:48:36 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 00:48:36 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:48:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 00:48:41 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 00:48:41 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 00:48:42 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 00:48:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 00:48:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 00:48:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 00:48:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 00:48:44 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 00:48:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 00:48:45 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 00:48:45 GMT
EXPOSE 80
# Sat, 27 Jan 2024 00:48:46 GMT
EXPOSE 443
# Sat, 27 Jan 2024 00:48:46 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 00:48:47 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 00:48:47 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 00:48:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5469759827ceaac50f13afad48892591b541bff7fa92b64936e2059ba28db3`  
		Last Modified: Sat, 27 Jan 2024 00:49:05 GMT  
		Size: 362.2 KB (362186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2c06e0d1950f2257265e78e914ebe1d4e1b0cfbfc32ba881b844fd13beb05b`  
		Last Modified: Sat, 27 Jan 2024 00:49:05 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2689e7d4f2d85097f8a724b4e3e41a875ff392132743a088b133a4d6802f6238`  
		Last Modified: Sat, 27 Jan 2024 00:49:07 GMT  
		Size: 13.3 MB (13333868 bytes)  
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
$ docker pull caddy@sha256:42442569a853bd5e5ce825d52baaee3fc919d1fa0e2fb7b9db30f246bec05c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:09513acee0757eaafeea861313a51d37b907cde693899b4d85bffa691d7eca06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77024166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e2950806b4846bc8384039f8e0ced6b55a43843627c3c7bcb574d00da87e36`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 03:39:23 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 03:39:23 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 03:39:24 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:39:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 03:39:24 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 03:39:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 03:39:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 03:39:25 GMT
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
	-	`sha256:c4b77ba268427b27996c293cddcbb1af065ac97d6f64fff6d3ee0adce318de44`  
		Last Modified: Sat, 27 Jan 2024 01:37:37 GMT  
		Size: 67.1 MB (67061623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5c147192a9317b4f575377244f4c3d96df9c9108d6147e10cd2becfdcfdc75`  
		Last Modified: Sat, 27 Jan 2024 01:37:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426789fa51aac91ce386d0cf62e3c5b4fd91cc19da6cb9449035a1aad2a1cb4b`  
		Last Modified: Sat, 27 Jan 2024 03:39:53 GMT  
		Size: 5.0 MB (4972458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848439cf5d4cf7d00a316abe8d0c04005a28d2e60f11875549cbbeec7db5cafc`  
		Last Modified: Sat, 27 Jan 2024 03:39:53 GMT  
		Size: 1.3 MB (1302243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61744c717cfe93977f876b739f3c692e919bb8cf098d233db8af67c532d77cd`  
		Last Modified: Sat, 27 Jan 2024 03:39:52 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:f7f15d8dc37358732c441ac4c62c2ac4967b16eb93863621dfc5cacf0b9dc1c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75479956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b694cc61283aebb38db78010935fc8281778bc08c35e7816a8c8819d3727a6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 13:22:00 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 13:22:00 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 13:22:00 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 13:22:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 13:22:01 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 13:22:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 13:22:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 13:22:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6033bb349d654a4ba7602191ed0372313ceca193751253005ad66a23d4dcb0ec`  
		Last Modified: Sat, 27 Jan 2024 09:20:38 GMT  
		Size: 284.9 KB (284872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31e5472cbeca7cc0b8f9272fbe547db898349f9b598c6b975f2c4efeeb63aee`  
		Last Modified: Sat, 27 Jan 2024 09:21:48 GMT  
		Size: 65.8 MB (65832091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b979a15e6ae0ded8491c78ec0740e6ece1aaaa584d10fdb89131c53427aba66`  
		Last Modified: Sat, 27 Jan 2024 09:21:32 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31abdea622b745b38e9215bf8062f71c377f48b2049bf07a5cd650743c069abb`  
		Last Modified: Sat, 27 Jan 2024 13:22:18 GMT  
		Size: 5.0 MB (4966664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f06e6a7ead4077a0b30ee09128ded6d14cd9bd7f450ef457f559c9e5b59938`  
		Last Modified: Sat, 27 Jan 2024 13:22:18 GMT  
		Size: 1.2 MB (1248661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba060f027200c3446f1acab0c00b2f4a9e8acf8610c46591daa3d8d7434aafd`  
		Last Modified: Sat, 27 Jan 2024 13:22:17 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:c80d0eabc3c5c1e92b026b7e2c2c35b4783472f984fe455da2ddddedce5b416c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25cc1ad71b8526356adff18f79ddbb3ff658a705a74e76800ee8f8172d4551f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 21:55:58 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:55:58 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:55:58 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:55:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:55:59 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:56:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:56:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:56:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf835181e2f4c73f7de0fe69c219658c3feddb5ba4e6850bc5b5af9555c08d1`  
		Last Modified: Sat, 27 Jan 2024 00:41:32 GMT  
		Size: 284.1 KB (284079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e2cd4f5b6025c32b2853d34aa0bcf57d85f2d44b2e412e2ba4e6dd0159ac1f`  
		Last Modified: Tue, 06 Feb 2024 21:29:51 GMT  
		Size: 65.8 MB (65767453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d160b5a79dd98fde6c0642c78daa3c77f077ad44a16b27b65a3b24fff23c603f`  
		Last Modified: Tue, 06 Feb 2024 21:29:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5735d56095a062d062dbd8c2d92cff873a457010035f0a7bf754444cdda79e1`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 4.5 MB (4514266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e601fac0470697a15f02c34e269f0e19119d88f46ffbcdddc5300417e3aab4b`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 1.2 MB (1246089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caff9a4e5a9e81ccc2e586bdbd72039b0d2bcc929751e08afbcffd6dbff11931`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:31f32db6814a94ad3cac5661dbda0a586162eb0b22b3e6ccdeb3e72b55cb9b76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73998584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c56aa1b8e6d877694eff62d87142b579cb7d523e8f22c16615b9ec3c5e3bae3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 21:33:04 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:33:04 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:33:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:33:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:33:06 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e59bef827dc10d9c33cdf4762faf3f2987df2a0296378e2349ec6d5bc6a37f4`  
		Last Modified: Sat, 27 Jan 2024 05:33:17 GMT  
		Size: 286.3 KB (286302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328d8fad75fb04ebff991b2c11c5988722931b5300239657bc1b4961655df05f`  
		Last Modified: Tue, 06 Feb 2024 20:50:08 GMT  
		Size: 64.1 MB (64109254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62899699addead1db84d09ab10dc0a0cbde16beb64c81cde0f84af2fa9b30f39`  
		Last Modified: Tue, 06 Feb 2024 20:50:00 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1745cea878add1608edd8710a879d4925a33b6e27329531c9c1cdd2c0e79c91a`  
		Last Modified: Tue, 06 Feb 2024 21:33:21 GMT  
		Size: 5.1 MB (5070613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235f6d9da6844caff2a0af124b9c01f0bf0abd2be340e5d2c67ab135a7cca76d`  
		Last Modified: Tue, 06 Feb 2024 21:33:21 GMT  
		Size: 1.2 MB (1198444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca8afc86b60749044b9b64230a9f9c67c20aa089b99562732169c4e6a807628`  
		Last Modified: Tue, 06 Feb 2024 21:33:20 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:b4effdad9be7ca7509b54d46638823940081fdf20f3000aaf9b3a691ace61f17
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74213039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10cf81cb43dc269c0ea9f820417d703e172313e228a17bdf7cffe96f4d2e742`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 21:14:22 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:14:22 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:14:23 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:14:23 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:14:24 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:14:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:14:27 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:14:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f92ca388ce06d6dddf0b5ad5ca0d5b82049994f1ad4da72bb5e48c5783dc009`  
		Last Modified: Sat, 27 Jan 2024 01:13:46 GMT  
		Size: 286.7 KB (286665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ef3661c7b713c28d8e0ae3c73dc823022f6a6e8a65c6fd2f00aa13dd6be4e4`  
		Last Modified: Tue, 06 Feb 2024 20:39:21 GMT  
		Size: 64.1 MB (64120440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7f0aa3654740d4016d469bad05baafdfc3be78e2f6ebc6f938501a1f4cd056`  
		Last Modified: Tue, 06 Feb 2024 20:39:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53242ccbc16994912810b389fdd1f7cb7cb1a3223cec7dcac1d4d00340e2f6de`  
		Last Modified: Tue, 06 Feb 2024 21:14:45 GMT  
		Size: 5.3 MB (5270660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c055ede766eec14283da8e4f87ab21f6a84f8ceff065d702bc31c9bf9ef23757`  
		Last Modified: Tue, 06 Feb 2024 21:14:45 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbe5c0b6966115344269e3c2b83ef21af0ebd897ee5a670604887f27d3da882`  
		Last Modified: Tue, 06 Feb 2024 21:14:44 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:25c4422b5cf06de48acecb96441e14f50db37a05c9353138f1f0f8b476680bb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76167035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06a921e90d95d0edd27e62d87f24a3fced554bde075b4b48f9099611fecb599`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 14:17:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 14:17:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 14:17:32 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 14:17:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 14:17:33 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 14:17:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 14:17:36 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 14:17:36 GMT
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
	-	`sha256:b94763531102ae1af628e5b55ca073b0c0fbd6aab9f221a28f3895303ddd975d`  
		Last Modified: Sat, 27 Jan 2024 05:47:26 GMT  
		Size: 66.3 MB (66284463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd03f53bee613b790f5b2286c4561428b2b2da6234df368a3a50d5ad91d58b9a`  
		Last Modified: Sat, 27 Jan 2024 05:47:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c299d55132b1737b4877e997f9881e05bd66727a05f8502f6fc38969031381ce`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 5.1 MB (5116950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60611bccc71deeef6872096a6f8a89a7e7af13c5027eb639b2ee7c182855d85`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 1.3 MB (1262387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fda9b2eed36da0393b2486d62a5c2c8ed03d6f3e38b27aae0fb6a57259b22e`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.20348.2227; amd64

```console
$ docker pull caddy@sha256:4814d63f1ac1d7e2334ff267279eed3b5533e0f94ad926fe9b3f11064e087406
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1997072166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d833851f7e1c400f60d5591428c91912a576258fb5b2fd93a0cdd0b228b07d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jan 2024 23:22:59 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Jan 2024 23:23:00 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Jan 2024 23:23:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Jan 2024 23:23:02 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Jan 2024 23:23:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Jan 2024 23:23:36 GMT
ENV GOPATH=C:\go
# Wed, 10 Jan 2024 23:23:55 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 Feb 2024 20:15:33 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 20:17:57 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 Feb 2024 20:17:58 GMT
WORKDIR C:\go
# Tue, 06 Feb 2024 21:01:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Feb 2024 21:01:18 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:01:19 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:01:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:01:44 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 06 Feb 2024 21:01:45 GMT
WORKDIR C:\
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
	-	`sha256:a3069ddb372bc0087899e61a271374e1b4423cfd9056ff2725874a89af15c2a1`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0841fad0c7557916603463fc9615983e0ad786338880d3d99c005dd50ecf3b6`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d1ae6fa2010fb779b06f0fc8a74830b01c9a87769fc35818fccdd5b7e7ea45`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4cd94fbe72557ed410a8f0aa0361ffc9ec2b2ecd96dc803b91c5ce0f34d077`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b3e385378ebc3f79f2c065897b323f0b1cfc97f3f8979c4530d0791e3e9523`  
		Last Modified: Thu, 11 Jan 2024 00:01:30 GMT  
		Size: 25.5 MB (25529890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbdf5bbf3fb6a215313abb55339dcee6260ef50d2c50d2b781476d5af12e840`  
		Last Modified: Thu, 11 Jan 2024 00:01:23 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7fd79e14c60629d3157a4363f602b919ba92aa10209a2e6ac40b7c86a75316`  
		Last Modified: Thu, 11 Jan 2024 00:01:23 GMT  
		Size: 261.7 KB (261737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d6abeee495b14ea2e44bb00f28c38212af6d923a1d5c148dd3eb083e1788d2`  
		Last Modified: Tue, 06 Feb 2024 20:38:27 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699b8adf45cf387aabdaea0b829e6bf5dee7a05e7eaf5519d3b0f5fe071e14a`  
		Last Modified: Tue, 06 Feb 2024 20:38:45 GMT  
		Size: 69.4 MB (69373765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd60a6e8aaafdd337241c619e2cd664dbfd6052a133b148c86845f227a25ea14`  
		Last Modified: Tue, 06 Feb 2024 20:38:27 GMT  
		Size: 1.5 KB (1531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6796689d52835dc674b67907c3e03bb20425e0e76be6963eaeb04e035d2c7f`  
		Last Modified: Tue, 06 Feb 2024 21:02:41 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657c487d0aab792a6141c8f2b5d1ef4564310178c60f883cb8e301cb752930ff`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bcd5a55d300a69a6a7202fda4cdb55a8e4f3645145c962279bc958c9efdf5a`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f9fc1b6232aab1694132043a6674117073dc98b00635546605582fabd31300`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005f7ea8d310ffb3ab0f46fbb75e4a90192f694357210b16fa4867a1c593cf2e`  
		Last Modified: Tue, 06 Feb 2024 21:02:39 GMT  
		Size: 1.7 MB (1675717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f756efa4d252460db4055d7da93b4667f4b1537f46882db730596bac57eb677`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.5329; amd64

```console
$ docker pull caddy@sha256:882f417e3efb3b9a8d1ade5245808ac22c5c1ea57a1352c72b6652b3a3238ecf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2166627810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6206308760870c6bbbd479176af11a35608423c94c08b69c418649ce2d281f3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jan 2024 23:26:43 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Jan 2024 23:26:44 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Jan 2024 23:26:45 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Jan 2024 23:26:46 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Jan 2024 23:28:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Jan 2024 23:28:09 GMT
ENV GOPATH=C:\go
# Wed, 10 Jan 2024 23:29:17 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 Feb 2024 20:18:16 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 20:21:36 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 Feb 2024 20:21:37 GMT
WORKDIR C:\go
# Tue, 06 Feb 2024 20:59:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Feb 2024 20:59:49 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 20:59:50 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 20:59:51 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:01:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 06 Feb 2024 21:01:01 GMT
WORKDIR C:\
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
	-	`sha256:58a2d0f9e9eca6932479b4446cdad2350fe376cd5102106ac4938d8552073ee1`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3baf188f2343abdd0b6b9307f8adcc91c698473839c28dbba9e3b50117d7df5`  
		Last Modified: Thu, 11 Jan 2024 00:03:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83f321def9731da0b67b8c9c7c573a95237ff9d906d16394dfc3dd845bd806`  
		Last Modified: Thu, 11 Jan 2024 00:03:01 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3185717e4484ba21a137fb6d471a72ee842364637f999013cbd8b7a633ccfa`  
		Last Modified: Thu, 11 Jan 2024 00:03:01 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d432d7f01be369829a69831b58f259bc1d30ccb67bc46a16211f95454e2d026b`  
		Last Modified: Thu, 11 Jan 2024 00:03:06 GMT  
		Size: 25.6 MB (25555277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481ab54aaa7ea3f3af1db424c6fda8a4bf6e63fe0bc92e2e319db55c66952d5`  
		Last Modified: Thu, 11 Jan 2024 00:02:59 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4579730b543c234b271242a1f8b94332944911daa12fe4493f4daad09e6e6a1`  
		Last Modified: Thu, 11 Jan 2024 00:02:59 GMT  
		Size: 284.0 KB (284031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57342fc3b749de0a8e32c9f1f9eece3c3855ea5d8b63b70682518058c40ba349`  
		Last Modified: Tue, 06 Feb 2024 20:38:59 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d092fd3744c0081064bac79e4fb322e2f6e9d0d8e744bb837bccd7f9b844e8`  
		Last Modified: Tue, 06 Feb 2024 20:39:17 GMT  
		Size: 69.4 MB (69370513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a8538533cb5606cc3e717f0431791fcd99ca7c1b935f5586f465bbd0c9d457`  
		Last Modified: Tue, 06 Feb 2024 20:38:59 GMT  
		Size: 1.6 KB (1586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ba50226998b42d6500ba479c1fbf0f3e588807488f728c91715ac893e69838`  
		Last Modified: Tue, 06 Feb 2024 21:02:24 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74292b50264f2db380dc5a9a8baaa5d229ff8efd2699e40fc6f478a25d59c0d0`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e574cef27624cb2b445968d4f051529c8c02dc6bf599ea131f51164de4939536`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14832cf23b08465f9e60489cda03b116fb6be01de86762232ed2f3b3aa8cf2a4`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e89456cebd7c16015a94dda1edb8a055ef730bc8c289b8eae13b1867371376f`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.7 MB (1677010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874ea9f0878170aeeae3da252653488f0677348bdb3f6cd9a87ccb3d064bde10`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:8a0f239bbd24b1a0973d0e3e22ef69d2e9f27b2f860c50247deead9c47b8b81e
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
$ docker pull caddy@sha256:09513acee0757eaafeea861313a51d37b907cde693899b4d85bffa691d7eca06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77024166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e2950806b4846bc8384039f8e0ced6b55a43843627c3c7bcb574d00da87e36`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 03:39:23 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 03:39:23 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 03:39:24 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:39:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 03:39:24 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 03:39:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 03:39:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 03:39:25 GMT
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
	-	`sha256:c4b77ba268427b27996c293cddcbb1af065ac97d6f64fff6d3ee0adce318de44`  
		Last Modified: Sat, 27 Jan 2024 01:37:37 GMT  
		Size: 67.1 MB (67061623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5c147192a9317b4f575377244f4c3d96df9c9108d6147e10cd2becfdcfdc75`  
		Last Modified: Sat, 27 Jan 2024 01:37:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426789fa51aac91ce386d0cf62e3c5b4fd91cc19da6cb9449035a1aad2a1cb4b`  
		Last Modified: Sat, 27 Jan 2024 03:39:53 GMT  
		Size: 5.0 MB (4972458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848439cf5d4cf7d00a316abe8d0c04005a28d2e60f11875549cbbeec7db5cafc`  
		Last Modified: Sat, 27 Jan 2024 03:39:53 GMT  
		Size: 1.3 MB (1302243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61744c717cfe93977f876b739f3c692e919bb8cf098d233db8af67c532d77cd`  
		Last Modified: Sat, 27 Jan 2024 03:39:52 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:f7f15d8dc37358732c441ac4c62c2ac4967b16eb93863621dfc5cacf0b9dc1c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75479956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b694cc61283aebb38db78010935fc8281778bc08c35e7816a8c8819d3727a6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 13:22:00 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 13:22:00 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 13:22:00 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 13:22:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 13:22:01 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 13:22:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 13:22:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 13:22:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6033bb349d654a4ba7602191ed0372313ceca193751253005ad66a23d4dcb0ec`  
		Last Modified: Sat, 27 Jan 2024 09:20:38 GMT  
		Size: 284.9 KB (284872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31e5472cbeca7cc0b8f9272fbe547db898349f9b598c6b975f2c4efeeb63aee`  
		Last Modified: Sat, 27 Jan 2024 09:21:48 GMT  
		Size: 65.8 MB (65832091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b979a15e6ae0ded8491c78ec0740e6ece1aaaa584d10fdb89131c53427aba66`  
		Last Modified: Sat, 27 Jan 2024 09:21:32 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31abdea622b745b38e9215bf8062f71c377f48b2049bf07a5cd650743c069abb`  
		Last Modified: Sat, 27 Jan 2024 13:22:18 GMT  
		Size: 5.0 MB (4966664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f06e6a7ead4077a0b30ee09128ded6d14cd9bd7f450ef457f559c9e5b59938`  
		Last Modified: Sat, 27 Jan 2024 13:22:18 GMT  
		Size: 1.2 MB (1248661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba060f027200c3446f1acab0c00b2f4a9e8acf8610c46591daa3d8d7434aafd`  
		Last Modified: Sat, 27 Jan 2024 13:22:17 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:c80d0eabc3c5c1e92b026b7e2c2c35b4783472f984fe455da2ddddedce5b416c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25cc1ad71b8526356adff18f79ddbb3ff658a705a74e76800ee8f8172d4551f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 21:55:58 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:55:58 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:55:58 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:55:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:55:59 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:56:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:56:02 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:56:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf835181e2f4c73f7de0fe69c219658c3feddb5ba4e6850bc5b5af9555c08d1`  
		Last Modified: Sat, 27 Jan 2024 00:41:32 GMT  
		Size: 284.1 KB (284079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e2cd4f5b6025c32b2853d34aa0bcf57d85f2d44b2e412e2ba4e6dd0159ac1f`  
		Last Modified: Tue, 06 Feb 2024 21:29:51 GMT  
		Size: 65.8 MB (65767453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d160b5a79dd98fde6c0642c78daa3c77f077ad44a16b27b65a3b24fff23c603f`  
		Last Modified: Tue, 06 Feb 2024 21:29:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5735d56095a062d062dbd8c2d92cff873a457010035f0a7bf754444cdda79e1`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 4.5 MB (4514266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e601fac0470697a15f02c34e269f0e19119d88f46ffbcdddc5300417e3aab4b`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 1.2 MB (1246089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caff9a4e5a9e81ccc2e586bdbd72039b0d2bcc929751e08afbcffd6dbff11931`  
		Last Modified: Tue, 06 Feb 2024 21:56:24 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:31f32db6814a94ad3cac5661dbda0a586162eb0b22b3e6ccdeb3e72b55cb9b76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73998584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c56aa1b8e6d877694eff62d87142b579cb7d523e8f22c16615b9ec3c5e3bae3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 21:33:04 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:33:04 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:33:04 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:33:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:33:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:33:06 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e59bef827dc10d9c33cdf4762faf3f2987df2a0296378e2349ec6d5bc6a37f4`  
		Last Modified: Sat, 27 Jan 2024 05:33:17 GMT  
		Size: 286.3 KB (286302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328d8fad75fb04ebff991b2c11c5988722931b5300239657bc1b4961655df05f`  
		Last Modified: Tue, 06 Feb 2024 20:50:08 GMT  
		Size: 64.1 MB (64109254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62899699addead1db84d09ab10dc0a0cbde16beb64c81cde0f84af2fa9b30f39`  
		Last Modified: Tue, 06 Feb 2024 20:50:00 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1745cea878add1608edd8710a879d4925a33b6e27329531c9c1cdd2c0e79c91a`  
		Last Modified: Tue, 06 Feb 2024 21:33:21 GMT  
		Size: 5.1 MB (5070613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235f6d9da6844caff2a0af124b9c01f0bf0abd2be340e5d2c67ab135a7cca76d`  
		Last Modified: Tue, 06 Feb 2024 21:33:21 GMT  
		Size: 1.2 MB (1198444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca8afc86b60749044b9b64230a9f9c67c20aa089b99562732169c4e6a807628`  
		Last Modified: Tue, 06 Feb 2024 21:33:20 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:b4effdad9be7ca7509b54d46638823940081fdf20f3000aaf9b3a691ace61f17
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74213039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10cf81cb43dc269c0ea9f820417d703e172313e228a17bdf7cffe96f4d2e742`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 18:23:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 18:23:15 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 18:23:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 18:23:15 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 18:23:15 GMT
WORKDIR /go
# Tue, 06 Feb 2024 21:14:22 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 06 Feb 2024 21:14:22 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:14:23 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:14:23 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:14:24 GMT
ENV XCADDY_SETCAP=1
# Tue, 06 Feb 2024 21:14:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 06 Feb 2024 21:14:27 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 06 Feb 2024 21:14:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f92ca388ce06d6dddf0b5ad5ca0d5b82049994f1ad4da72bb5e48c5783dc009`  
		Last Modified: Sat, 27 Jan 2024 01:13:46 GMT  
		Size: 286.7 KB (286665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ef3661c7b713c28d8e0ae3c73dc823022f6a6e8a65c6fd2f00aa13dd6be4e4`  
		Last Modified: Tue, 06 Feb 2024 20:39:21 GMT  
		Size: 64.1 MB (64120440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7f0aa3654740d4016d469bad05baafdfc3be78e2f6ebc6f938501a1f4cd056`  
		Last Modified: Tue, 06 Feb 2024 20:39:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53242ccbc16994912810b389fdd1f7cb7cb1a3223cec7dcac1d4d00340e2f6de`  
		Last Modified: Tue, 06 Feb 2024 21:14:45 GMT  
		Size: 5.3 MB (5270660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c055ede766eec14283da8e4f87ab21f6a84f8ceff065d702bc31c9bf9ef23757`  
		Last Modified: Tue, 06 Feb 2024 21:14:45 GMT  
		Size: 1.2 MB (1186174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbe5c0b6966115344269e3c2b83ef21af0ebd897ee5a670604887f27d3da882`  
		Last Modified: Tue, 06 Feb 2024 21:14:44 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:25c4422b5cf06de48acecb96441e14f50db37a05c9353138f1f0f8b476680bb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76167035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06a921e90d95d0edd27e62d87f24a3fced554bde075b4b48f9099611fecb599`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 21:13:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOLANG_VERSION=1.21.6
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Jan 2024 21:13:58 GMT
ENV GOPATH=/go
# Tue, 16 Jan 2024 21:13:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 21:13:58 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Jan 2024 21:13:58 GMT
WORKDIR /go
# Sat, 27 Jan 2024 14:17:30 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Sat, 27 Jan 2024 14:17:31 GMT
ENV XCADDY_VERSION=v0.3.5
# Sat, 27 Jan 2024 14:17:32 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 14:17:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 27 Jan 2024 14:17:33 GMT
ENV XCADDY_SETCAP=1
# Sat, 27 Jan 2024 14:17:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Sat, 27 Jan 2024 14:17:36 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Sat, 27 Jan 2024 14:17:36 GMT
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
	-	`sha256:b94763531102ae1af628e5b55ca073b0c0fbd6aab9f221a28f3895303ddd975d`  
		Last Modified: Sat, 27 Jan 2024 05:47:26 GMT  
		Size: 66.3 MB (66284463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd03f53bee613b790f5b2286c4561428b2b2da6234df368a3a50d5ad91d58b9a`  
		Last Modified: Sat, 27 Jan 2024 05:47:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c299d55132b1737b4877e997f9881e05bd66727a05f8502f6fc38969031381ce`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 5.1 MB (5116950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60611bccc71deeef6872096a6f8a89a7e7af13c5027eb639b2ee7c182855d85`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 1.3 MB (1262387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fda9b2eed36da0393b2486d62a5c2c8ed03d6f3e38b27aae0fb6a57259b22e`  
		Last Modified: Sat, 27 Jan 2024 14:19:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:e794dda1d2a08c7fe472d7b929a4d86621c3ea9ac1252d7fe1134e724a2115a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull caddy@sha256:882f417e3efb3b9a8d1ade5245808ac22c5c1ea57a1352c72b6652b3a3238ecf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2166627810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6206308760870c6bbbd479176af11a35608423c94c08b69c418649ce2d281f3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jan 2024 23:26:43 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Jan 2024 23:26:44 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Jan 2024 23:26:45 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Jan 2024 23:26:46 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Jan 2024 23:28:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Jan 2024 23:28:09 GMT
ENV GOPATH=C:\go
# Wed, 10 Jan 2024 23:29:17 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 Feb 2024 20:18:16 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 20:21:36 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 Feb 2024 20:21:37 GMT
WORKDIR C:\go
# Tue, 06 Feb 2024 20:59:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Feb 2024 20:59:49 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 20:59:50 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 20:59:51 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:01:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 06 Feb 2024 21:01:01 GMT
WORKDIR C:\
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
	-	`sha256:58a2d0f9e9eca6932479b4446cdad2350fe376cd5102106ac4938d8552073ee1`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3baf188f2343abdd0b6b9307f8adcc91c698473839c28dbba9e3b50117d7df5`  
		Last Modified: Thu, 11 Jan 2024 00:03:02 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83f321def9731da0b67b8c9c7c573a95237ff9d906d16394dfc3dd845bd806`  
		Last Modified: Thu, 11 Jan 2024 00:03:01 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3185717e4484ba21a137fb6d471a72ee842364637f999013cbd8b7a633ccfa`  
		Last Modified: Thu, 11 Jan 2024 00:03:01 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d432d7f01be369829a69831b58f259bc1d30ccb67bc46a16211f95454e2d026b`  
		Last Modified: Thu, 11 Jan 2024 00:03:06 GMT  
		Size: 25.6 MB (25555277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b481ab54aaa7ea3f3af1db424c6fda8a4bf6e63fe0bc92e2e319db55c66952d5`  
		Last Modified: Thu, 11 Jan 2024 00:02:59 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4579730b543c234b271242a1f8b94332944911daa12fe4493f4daad09e6e6a1`  
		Last Modified: Thu, 11 Jan 2024 00:02:59 GMT  
		Size: 284.0 KB (284031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57342fc3b749de0a8e32c9f1f9eece3c3855ea5d8b63b70682518058c40ba349`  
		Last Modified: Tue, 06 Feb 2024 20:38:59 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d092fd3744c0081064bac79e4fb322e2f6e9d0d8e744bb837bccd7f9b844e8`  
		Last Modified: Tue, 06 Feb 2024 20:39:17 GMT  
		Size: 69.4 MB (69370513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a8538533cb5606cc3e717f0431791fcd99ca7c1b935f5586f465bbd0c9d457`  
		Last Modified: Tue, 06 Feb 2024 20:38:59 GMT  
		Size: 1.6 KB (1586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ba50226998b42d6500ba479c1fbf0f3e588807488f728c91715ac893e69838`  
		Last Modified: Tue, 06 Feb 2024 21:02:24 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74292b50264f2db380dc5a9a8baaa5d229ff8efd2699e40fc6f478a25d59c0d0`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e574cef27624cb2b445968d4f051529c8c02dc6bf599ea131f51164de4939536`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14832cf23b08465f9e60489cda03b116fb6be01de86762232ed2f3b3aa8cf2a4`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e89456cebd7c16015a94dda1edb8a055ef730bc8c289b8eae13b1867371376f`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.7 MB (1677010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874ea9f0878170aeeae3da252653488f0677348bdb3f6cd9a87ccb3d064bde10`  
		Last Modified: Tue, 06 Feb 2024 21:02:22 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:97e329cd72c287551121f0de0749affc40ba296a42f67b3774c972dfc63239d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull caddy@sha256:4814d63f1ac1d7e2334ff267279eed3b5533e0f94ad926fe9b3f11064e087406
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1997072166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d833851f7e1c400f60d5591428c91912a576258fb5b2fd93a0cdd0b228b07d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 10 Jan 2024 22:36:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jan 2024 23:22:59 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Jan 2024 23:23:00 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Jan 2024 23:23:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Jan 2024 23:23:02 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Jan 2024 23:23:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Jan 2024 23:23:36 GMT
ENV GOPATH=C:\go
# Wed, 10 Jan 2024 23:23:55 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 Feb 2024 20:15:33 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 20:17:57 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 Feb 2024 20:17:58 GMT
WORKDIR C:\go
# Tue, 06 Feb 2024 21:01:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Feb 2024 21:01:18 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 06 Feb 2024 21:01:19 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 06 Feb 2024 21:01:20 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Feb 2024 21:01:44 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 06 Feb 2024 21:01:45 GMT
WORKDIR C:\
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
	-	`sha256:a3069ddb372bc0087899e61a271374e1b4423cfd9056ff2725874a89af15c2a1`  
		Last Modified: Thu, 11 Jan 2024 00:01:27 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0841fad0c7557916603463fc9615983e0ad786338880d3d99c005dd50ecf3b6`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d1ae6fa2010fb779b06f0fc8a74830b01c9a87769fc35818fccdd5b7e7ea45`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4cd94fbe72557ed410a8f0aa0361ffc9ec2b2ecd96dc803b91c5ce0f34d077`  
		Last Modified: Thu, 11 Jan 2024 00:01:25 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b3e385378ebc3f79f2c065897b323f0b1cfc97f3f8979c4530d0791e3e9523`  
		Last Modified: Thu, 11 Jan 2024 00:01:30 GMT  
		Size: 25.5 MB (25529890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbdf5bbf3fb6a215313abb55339dcee6260ef50d2c50d2b781476d5af12e840`  
		Last Modified: Thu, 11 Jan 2024 00:01:23 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7fd79e14c60629d3157a4363f602b919ba92aa10209a2e6ac40b7c86a75316`  
		Last Modified: Thu, 11 Jan 2024 00:01:23 GMT  
		Size: 261.7 KB (261737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d6abeee495b14ea2e44bb00f28c38212af6d923a1d5c148dd3eb083e1788d2`  
		Last Modified: Tue, 06 Feb 2024 20:38:27 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6699b8adf45cf387aabdaea0b829e6bf5dee7a05e7eaf5519d3b0f5fe071e14a`  
		Last Modified: Tue, 06 Feb 2024 20:38:45 GMT  
		Size: 69.4 MB (69373765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd60a6e8aaafdd337241c619e2cd664dbfd6052a133b148c86845f227a25ea14`  
		Last Modified: Tue, 06 Feb 2024 20:38:27 GMT  
		Size: 1.5 KB (1531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6796689d52835dc674b67907c3e03bb20425e0e76be6963eaeb04e035d2c7f`  
		Last Modified: Tue, 06 Feb 2024 21:02:41 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657c487d0aab792a6141c8f2b5d1ef4564310178c60f883cb8e301cb752930ff`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bcd5a55d300a69a6a7202fda4cdb55a8e4f3645145c962279bc958c9efdf5a`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f9fc1b6232aab1694132043a6674117073dc98b00635546605582fabd31300`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005f7ea8d310ffb3ab0f46fbb75e4a90192f694357210b16fa4867a1c593cf2e`  
		Last Modified: Tue, 06 Feb 2024 21:02:39 GMT  
		Size: 1.7 MB (1675717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f756efa4d252460db4055d7da93b4667f4b1537f46882db730596bac57eb677`  
		Last Modified: Tue, 06 Feb 2024 21:02:38 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:245e14283de7392fd14ef9e425580fe689cc0f8eedf28376016dab4109bc76b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:67d0aa24ce021bee77049ddd2c0cc64732dd43d04598085ec39f950a13981bd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18467338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66978cebfbcc9c0a17709b108582a40a369c525c764e9a8882f6cae260b32f4d`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:39:14 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 03:39:16 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 03:39:16 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:39:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 03:39:18 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 03:39:18 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 03:39:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 03:39:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 80
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 443
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 03:39:19 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 03:39:19 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 03:39:19 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf3211613d439d6da6e22998ce1ca109a902f861e1c1d55f59750636c8b7dc`  
		Last Modified: Sat, 27 Jan 2024 03:39:38 GMT  
		Size: 350.8 KB (350837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3505501083aeee1ff957f129e7d5dbdec0a32b80fee88cba62665e91547eeee0`  
		Last Modified: Sat, 27 Jan 2024 03:39:38 GMT  
		Size: 7.5 KB (7523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcbb25232b8128478b3c2ba4fe7e03fafdbf5024b74db396eef024b547f95ca`  
		Last Modified: Sat, 27 Jan 2024 03:39:40 GMT  
		Size: 14.7 MB (14706436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:6fb5cfba87d2f8f1e7f89e7f61fad3a9e2ef76dc7f58aaffdf5af8997dc6dac4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17423230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3a842d1153c178390b3187d16d1ea0f4d691fd1c72bc5fd0a2ff32c6915a02`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:05:40 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 00:05:42 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 00:05:42 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:05:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 00:05:45 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 00:05:45 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 00:05:45 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 00:05:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 00:05:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 80
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 443
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 00:05:46 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 00:05:46 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 00:05:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a63a43f994064f0597fc36462d12376175178fc2c5486a9edcb36b198de411`  
		Last Modified: Sat, 27 Jan 2024 00:06:02 GMT  
		Size: 347.6 KB (347620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2327a8d9853b0ed7c134359a0fb7d0ea93d16621dd29a136c22bb30c59493703`  
		Last Modified: Sat, 27 Jan 2024 00:06:02 GMT  
		Size: 7.5 KB (7528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71ff73f86184e48aa48d9298e97a824ab7316cc6134da0983587197e162a4d6`  
		Last Modified: Sat, 27 Jan 2024 00:06:04 GMT  
		Size: 13.9 MB (13921023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:56128992f412b5e862c705f3ea06a9e290a1caa484f80111556fb1f13c15ce16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17147114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71cfdc5faaa533682a397011b220a59fa9e54a42f98146bfb1080c102a0ebc86`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:44:33 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 00:44:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 00:44:35 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:44:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 00:44:41 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 00:44:41 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 00:44:42 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 00:44:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 00:44:42 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 00:44:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 00:44:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 00:44:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 00:44:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 00:44:44 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 00:44:44 GMT
EXPOSE 80
# Sat, 27 Jan 2024 00:44:45 GMT
EXPOSE 443
# Sat, 27 Jan 2024 00:44:45 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 00:44:46 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 00:44:46 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 00:44:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2a6e8e98d60ee548724a36c2a41ee2f4053b409052e45ab4b015360e73c808`  
		Last Modified: Sat, 27 Jan 2024 00:45:17 GMT  
		Size: 344.5 KB (344463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9afd4ba62ae2a5b6f5ffd0c7d900582f8e684b0d45670317b63e3b8f51dc9b`  
		Last Modified: Sat, 27 Jan 2024 00:45:17 GMT  
		Size: 7.5 KB (7527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b8e42e4efab7a06b51ee74ffac1bca9bf70812dd543cb7ab60135515565e13`  
		Last Modified: Sat, 27 Jan 2024 00:45:20 GMT  
		Size: 13.9 MB (13893732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:2ec95d40ce2d1f18f92eee012a5dd18b352075d92eb6c4f4e0ea18c46ad4b069
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09733d8f0611adb987aea99d5144981331f8b6de5c2397bef43678ba50066f4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:44:36 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 03:44:38 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 03:44:38 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 03:44:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 03:44:40 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 03:44:40 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 03:44:40 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 80
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 443
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 03:44:41 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 03:44:41 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 03:44:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8d53bc0303fbf7f349016b59b6ac8710ba2639505e276c3816ecca679bdac7`  
		Last Modified: Sat, 27 Jan 2024 03:44:57 GMT  
		Size: 360.7 KB (360652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764cd8cdd6e6b377bd4cd13dbb53eb18d9fc7e0045323401614398d5a85b9c65`  
		Last Modified: Sat, 27 Jan 2024 03:44:56 GMT  
		Size: 7.5 KB (7526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00acba9333616526f5fc17192a0abd4e29624bba1500c6068db189bdcbee5468`  
		Last Modified: Sat, 27 Jan 2024 03:44:58 GMT  
		Size: 13.6 MB (13568965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:53a5136ccffab422016068b77862678ad9b19430fc52f7e911188703d0123939
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17052070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9c424cec6fbefc3fd4578ed97634fbe37d2590a0e474a0dce3a35ff23a8352`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:48:34 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap
# Sat, 27 Jan 2024 00:48:36 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"
# Sat, 27 Jan 2024 00:48:36 GMT
ENV CADDY_VERSION=v2.7.6
# Sat, 27 Jan 2024 00:48:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version
# Sat, 27 Jan 2024 00:48:41 GMT
ENV XDG_CONFIG_HOME=/config
# Sat, 27 Jan 2024 00:48:41 GMT
ENV XDG_DATA_HOME=/data
# Sat, 27 Jan 2024 00:48:42 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Sat, 27 Jan 2024 00:48:42 GMT
LABEL org.opencontainers.image.title=Caddy
# Sat, 27 Jan 2024 00:48:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Sat, 27 Jan 2024 00:48:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Sat, 27 Jan 2024 00:48:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Sat, 27 Jan 2024 00:48:44 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Sat, 27 Jan 2024 00:48:44 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 27 Jan 2024 00:48:45 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Sat, 27 Jan 2024 00:48:45 GMT
EXPOSE 80
# Sat, 27 Jan 2024 00:48:46 GMT
EXPOSE 443
# Sat, 27 Jan 2024 00:48:46 GMT
EXPOSE 443/udp
# Sat, 27 Jan 2024 00:48:47 GMT
EXPOSE 2019
# Sat, 27 Jan 2024 00:48:47 GMT
WORKDIR /srv
# Sat, 27 Jan 2024 00:48:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5469759827ceaac50f13afad48892591b541bff7fa92b64936e2059ba28db3`  
		Last Modified: Sat, 27 Jan 2024 00:49:05 GMT  
		Size: 362.2 KB (362186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2c06e0d1950f2257265e78e914ebe1d4e1b0cfbfc32ba881b844fd13beb05b`  
		Last Modified: Sat, 27 Jan 2024 00:49:05 GMT  
		Size: 7.5 KB (7529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2689e7d4f2d85097f8a724b4e3e41a875ff392132743a088b133a4d6802f6238`  
		Last Modified: Sat, 27 Jan 2024 00:49:07 GMT  
		Size: 13.3 MB (13333868 bytes)  
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

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:c6e3f25c93c35d4a519395eb595f46de5889867e37acd83bac72b8d2d9dcef3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `caddy:windowsservercore` - windows version 10.0.20348.2227; amd64

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

### `caddy:windowsservercore` - windows version 10.0.17763.5329; amd64

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

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:f7e06b6f876505ed8ae83c339c860ab40d8287d52669bddf6dad0302470155d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.5329; amd64

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

## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:cdb4600df8fe3e27d97f1fb21ba9d5fdb1bd8198a1f025ca2458154f28d76934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

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
