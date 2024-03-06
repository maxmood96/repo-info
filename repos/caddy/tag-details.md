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
$ docker pull caddy@sha256:2a0d069ea95d91641d201943a5a049e83cbfade8039670aebfb441b132189de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

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

### `caddy:2` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:f6e8f7815f3e03bc5d239d52a2bdeb473ff959a4b74bb86ee94b410cc2407c35
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1926683398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d9ff1f8c7723994d4a4f7c520159beedff8fe440b855a9fb6f57afdcae7b2b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:22:32 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:22:33 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:23:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:23:00 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:23:01 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:23:02 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:23:03 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:23:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:23:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:23:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:23:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:23:09 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:23:11 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:23:26 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:23:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ebcfc7e63facc5463d681dd534f084e021cc447cf46213aae377066d573493`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 458.4 KB (458447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bee2047afe4426d5715972f534b35ce0bc5ae241ae42982e37a64185c7a482`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39da07145bbe64c3ec2c032dafa6eb6ddf62130dba67e03a627cc2cb3788f9e2`  
		Last Modified: Wed, 14 Feb 2024 21:26:37 GMT  
		Size: 15.3 MB (15267126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c47f482128a80b23df310b1c1b71bfa176b010cdd91761fb1a9aa71c4812738`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dab75e60136c0cf03ae7e7ad030b7adb3aff8014f4fc0e412d1ce9c217bdd60`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db7f5e1b9057131a3d1e7f1439de34f87684add5ac177612296925ed37b654d`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ac08dfbec3219d30d64f54cc8e1b46009cf4327d55c288ca43d875eaff3763`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4fad3dd8e3739d27a2d3793ae4740b4cbf52999f2295ad370545f048730492`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91f700224a04849cd48e2ab6525d47b7188051110718ca045ca50452ce26cb3`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fe7f9176dbfd4a89d170a117169a90cd5f49a2c5b7a55ac4026288812b8b60`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4fc40cf63828021df321258238a85d39918d2749a117bb0538bda0afce3aef`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9621f5d2e06bf68f778ba42ec6ec5d4a80d1cfb1204ea19b5a2b42d2b1d87d`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398c5b0cde2fcd40c8ce079d93fd115bd8ee7d8028cabc4baf9ecc07ab226410`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60cb86bd52f82372e11b1b851709ccb6c10537dc9262f63ef8bcd0152efb235`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c35a9695bf632732db6dd52a7531c75c5243819b2b8d7c019a1e8fc796e13c7`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c98226f721bed207883df26f4d35276821dd38299a62458d2ba6c55fab5b0d`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b23541f7ccf5a2debb904fdc41eccc03284d7fbf3baff61798b726d7c9ba12`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ce3a452fdfcd413ac385a157633a0fe389a8c2fdb281ce79b5cdd4d16dcb9b`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 281.4 KB (281363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7be2379ebd2e4d0fca0bbf81dd2628e93d8efd2ef3ea28c3872855ca6e50ed`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:793d5d17edca1d44e963efc2d79f97a389420f253790a04d54f9388492ca70ff
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2096464983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2636f0474ebff3dfb86f6d92e45af2173f0773887039f3e30776eb3b2de1bd0c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:18:41 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:18:42 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:20:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:20:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:20:23 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:20:24 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:20:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:20:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:20:31 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:20:33 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:20:34 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:20:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:20:36 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:20:36 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:20:37 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:20:38 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:20:40 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:21:47 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:21:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936f6b22f9979fac96518b60eadd4d9156939b025d673ce61a2e6a18553dc2b1`  
		Last Modified: Wed, 14 Feb 2024 21:26:08 GMT  
		Size: 461.6 KB (461622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72873b058a9927d9ea1e4a234006a54fec29d1da3beb3f2834ce66fda6f4262f`  
		Last Modified: Wed, 14 Feb 2024 21:26:07 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc3d79323d38d65e8112fca8b77ad54434883a9104dd542fdc179cf782fab1e`  
		Last Modified: Wed, 14 Feb 2024 21:26:10 GMT  
		Size: 15.3 MB (15274562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4873aaa427e9ae13aeebcc096c23b92dd4d61d1f6b601a755dfaf268c4b85ab6`  
		Last Modified: Wed, 14 Feb 2024 21:26:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c57d3fae417c15ca2cf9d965bd8d05bab080154e20cd2e20f5d71aa86de5c0f`  
		Last Modified: Wed, 14 Feb 2024 21:26:06 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444c12e07ce56e352f094a12c03aa1ab4110c79d5daa78eea733580703bdef6a`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cf5cd505e0ce461fb00191ec16014104c1f3f38c373b2179b9cb0ecec44082`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f67f42fce82938d220cec3933239aedeffe9da096d14f3354eb2ffd49902c8`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb581bc05a23526a9b12256e17b6963201710bb71ae435fed4ccbdc69330fe8`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806d41685663d3f82e404087dda88f57f3f2534966be1a73998da0d9d3f15ae8`  
		Last Modified: Wed, 14 Feb 2024 21:26:04 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af65ac33d93c108086650ad059ffe57d44fcae5dfcfd80f331aeb3acb759145`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1d5135587234fcaf02c388f1fbf2e4a7be50b81f4c5296aeb7a99cb5fc2d13`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705d9a64f11bac49a31ef3cb6bfd926024e700d3daf666b277867cddcef7fcff`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac09729a4577f5fe6afe0d3a00560ec715f86b1e907e28917ca6d13dcafb3e7`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cd769674ca72532329328651bf168fe61494249405bb59e89832d94410289b`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a7dedf94b664393c8ae954445d5b582ffe6d8ffc604ddaaae79b20de72317`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a465dd935213cb9e1bd4aae1e392fd32e5fcb661c6bf3b7a50e113ea7077d7`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d18f93e3aab637778f45296a721f0857d0c5ec759335b634ae323255bbb0c29`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 257.6 KB (257571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11c0d021a3877f354347717399af0fe31b30ddd220f2b64b4ccf68fe7b6140b`  
		Last Modified: Wed, 14 Feb 2024 21:26:02 GMT  
		Size: 1.3 KB (1333 bytes)  
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
$ docker pull caddy@sha256:7954f9183f22718dfac36955b6cb281466256ae195f30ffcd0229596e2badc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:683161d33599ee7740b25d8c0466e82bfd94e491c63bef744eda38919853dd62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76973779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e7c249761d733da653482a2b5259eaae803dee4354bc3562e48a601315e6ff`
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
# Tue, 05 Mar 2024 19:42:13 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 19:42:13 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 19:42:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 19:42:15 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 19:42:15 GMT
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
	-	`sha256:ddc853d0ab24d3fe195e8492db2866ec9d01681c218bdff73afb081fa97cb002`  
		Last Modified: Tue, 05 Mar 2024 19:42:32 GMT  
		Size: 5.0 MB (4972975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea68e3f24bc6efb27b70b8c1870bf11b4a5fad53eb40e8ce77817c21586972d`  
		Last Modified: Tue, 05 Mar 2024 19:42:31 GMT  
		Size: 1.3 MB (1302236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ecce85dc39a9d244f2c3b1e0e89e72279e6d9f6b154afad2171642b11c137b`  
		Last Modified: Tue, 05 Mar 2024 19:42:31 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ece7f11958f255486a5be355c9180900873b391449f4258706b535d5177b40b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75407413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22234bb36f9348628e9caea0dac041e47e0df57676643cb27bc893380168cbd`
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
# Tue, 05 Mar 2024 23:00:43 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 23:00:43 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 23:00:44 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 23:00:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 23:00:44 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 23:00:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 23:00:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 23:00:49 GMT
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
	-	`sha256:bccd7f5c5a4f0abc0a23393d9a04f353b767b809c6ac950caaa731dd3768c8eb`  
		Last Modified: Tue, 05 Mar 2024 20:11:40 GMT  
		Size: 65.8 MB (65767479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33a4721f193119280f7dfc5baed0ce6a2d3b2eb94e31901d986ea54166c41ea`  
		Last Modified: Tue, 05 Mar 2024 20:11:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28b5e7a7f3d8467fb26f35d8b70ae0853d39fb4103058a0dc47dd62be3256d7`  
		Last Modified: Tue, 05 Mar 2024 23:01:07 GMT  
		Size: 5.0 MB (4958742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276c5f8fd9c641c6036e92487a700ea1b6cc811b8ac1578ff0f94803223f6e0d`  
		Last Modified: Tue, 05 Mar 2024 23:01:07 GMT  
		Size: 1.2 MB (1248648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db777cbc747c60df3dc9c90c42c55125b12f7c65e05a6b1ab52ec8de565848a9`  
		Last Modified: Tue, 05 Mar 2024 23:01:06 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:156f7188ad9f04c359241e42567a3cee24477cb1885639d634da45c042cc297e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2a4fac0ed075caa114df1d0fd560d017af28251032ec5015a49c0702fe3d48`
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
# Tue, 05 Mar 2024 20:48:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:48:44 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:48:45 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:48:45 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:48:45 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:48:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:48:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:48:48 GMT
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
	-	`sha256:17f0c2683a0605dfb4fff92a0c34044c42624cbc47515f2262026e23ffa28b15`  
		Last Modified: Tue, 05 Mar 2024 20:01:25 GMT  
		Size: 65.8 MB (65767445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1570cef4f4f43311a29ff4036cc73329f8fe806fb19c51f3413b3073bfc70634`  
		Last Modified: Tue, 05 Mar 2024 20:01:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2640aa4bbda58460e9e4fd9b0a0969303c9a30ba9b9ff6424d9349f7c0ffbcd`  
		Last Modified: Tue, 05 Mar 2024 20:49:09 GMT  
		Size: 4.5 MB (4514657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5f06f998d08d9a0ca561581720f1399d9e1c6f64b4637370acd8eddc90418e`  
		Last Modified: Tue, 05 Mar 2024 20:49:08 GMT  
		Size: 1.2 MB (1246081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f58b57eb0adfeabad656db0f59a85f8373054397123d068fe68452663713a9f`  
		Last Modified: Tue, 05 Mar 2024 20:49:08 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:b7d23a0e6f86ad993855c69a14f149837072ce99399627ee74d95e4705784d14
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73993792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0728d6faf4e6faebb8c082c95826cc671a39f43e1cd9ef0cfcd909a42435c9bd`
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
# Tue, 05 Mar 2024 20:00:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:00:21 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:00:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:00:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:00:23 GMT
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
	-	`sha256:5a91045fa00056cff12698db93bed8fe188f9895b74e96e29b6a9f6a6e047937`  
		Last Modified: Tue, 05 Mar 2024 19:44:44 GMT  
		Size: 64.1 MB (64111148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f155e563ada2bb78e99decac187a48adcf9db3cd56e543bc0694674ef8a234`  
		Last Modified: Tue, 05 Mar 2024 19:44:35 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f627d8e1519d50a70f854d0342a035bd62a8cedf0d7a61351f7ac191accf21`  
		Last Modified: Tue, 05 Mar 2024 20:00:40 GMT  
		Size: 5.1 MB (5063926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cf96a60cd43a372ff273debacac6160f6842de4adc5e79eef190c8a791eecc`  
		Last Modified: Tue, 05 Mar 2024 20:00:39 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113a17d73127a40aa417b169724fea00b3b34ed479e7d3fb2b656325c7d131a8`  
		Last Modified: Tue, 05 Mar 2024 20:00:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:3321233002d79314df5692f81246bbcc2d0c9ba268c61792fd6269b1e64e6ff9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74219843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b9b8fd2c1e8bd5b65bfbd17b919aabf00faf29ce73a1702c8a2610afe5427c`
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
# Tue, 05 Mar 2024 19:40:39 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 19:40:40 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 19:40:40 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 19:40:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 19:40:41 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 19:40:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 19:40:44 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 19:40:44 GMT
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
	-	`sha256:1e1323fc82438c3a0b40c7bcf18c7b4808edcec55b91135df534741787df9cbc`  
		Last Modified: Tue, 05 Mar 2024 19:25:03 GMT  
		Size: 64.1 MB (64126907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8630ef56928609490ea4cc1460f549f49e84ed6ff4f6bb7ffb5c3fa5e53f3027`  
		Last Modified: Tue, 05 Mar 2024 19:24:51 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c2f5a4fa35cf481005994eef4a926ba3b1cecb6ee2747d8080460c88a7fa6c`  
		Last Modified: Tue, 05 Mar 2024 19:41:02 GMT  
		Size: 5.3 MB (5270995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cba91d041ae77cf958d8509d23d6f741eec735e9bf9a24d489d0b8842db30c9`  
		Last Modified: Tue, 05 Mar 2024 19:41:01 GMT  
		Size: 1.2 MB (1186176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de13da806adead3ab5a4380c923e80ebddfc28b7b94d6e6f43b6cbb920acd85`  
		Last Modified: Tue, 05 Mar 2024 19:41:01 GMT  
		Size: 407.0 B  
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

### `caddy:2-builder` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:e924a818b35c77fa77b850501f876fa811c43019e884675210e1232eb23b13a6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2007476156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69198d50697c7c62515331afda3b6b548388fe7ecfbec519f7bcb8e8ab8e5155`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:27:24 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Feb 2024 20:27:25 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Feb 2024 20:27:26 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Feb 2024 20:27:27 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Feb 2024 20:28:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:28:04 GMT
ENV GOPATH=C:\go
# Wed, 14 Feb 2024 20:28:25 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Mar 2024 19:27:34 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 19:29:55 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Mar 2024 19:29:57 GMT
WORKDIR C:\go
# Tue, 05 Mar 2024 20:03:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Mar 2024 20:03:28 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:03:29 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:03:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:03:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 05 Mar 2024 20:03:52 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ac8de2d709384a84400f6f072b2d3d4c4d454ee27f8ec716db4964eabac3f8`  
		Last Modified: Wed, 14 Feb 2024 20:55:46 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70115ee0ce6c09f30645181ec6f80fe9ece4e9b51628fdbaa85ebd4e0ae979e1`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab323644de57af1911793c0a10501a7b21640f8e58484665dc2258f482cb943`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae53fd363daebfb127c2ba7e51543cf93130802d95e194fc71db09c52b9fe10c`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665a9a35030c2076331610dfe4c22866525c2b0ac219981d900f1b6178af5241`  
		Last Modified: Wed, 14 Feb 2024 20:55:50 GMT  
		Size: 25.5 MB (25534020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ab59c20a7391d04f68a3dc2b9d6eb4cfd1e7af0ddd33e30d2cd19f13535c0`  
		Last Modified: Wed, 14 Feb 2024 20:55:43 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a35884f3b4e6aa2080cc34668faeabacc75000ef04e2fe4ec3e76f166d992e4`  
		Last Modified: Wed, 14 Feb 2024 20:55:43 GMT  
		Size: 266.0 KB (265989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c81949701f9fd28f5c42cfa101f1e2c2858efdb4032e3c3a221ae64417094d`  
		Last Modified: Tue, 05 Mar 2024 19:41:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c07bf58a4a94d97d30abeee1c89ea03f4d6bb5ae58ba58a108ab8c14ce86d04`  
		Last Modified: Tue, 05 Mar 2024 19:42:12 GMT  
		Size: 69.4 MB (69350261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff66f61d5b04d89a7cd43a5718c2738ee8c932ff7976238576fcce4a9205188`  
		Last Modified: Tue, 05 Mar 2024 19:41:52 GMT  
		Size: 1.5 KB (1539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fff8f151323c49bef4ab32c69e1b7fb0bc1c38c418bc58f8d552450f83ddb4`  
		Last Modified: Tue, 05 Mar 2024 20:04:48 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad11e6d0d7e8e1cdeb21675479688d12574b1f3aaf78c017dcb3f3f0e461e94`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3bac1fc388577dc02e99cece1f2418b768a6b9131f03ccb3a12b5130d0657c`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2023c4236e1ee6e1e21d75518a4e0b041879053cca3a4d196a736c11ef937885`  
		Last Modified: Tue, 05 Mar 2024 20:04:45 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646022f7531f95a5e75674d8b4716cd2b10acf7080eacbcf1a9146ec3c17a381`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.7 MB (1653517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a594d21bdd61142fc0e9073bca5c902365dcacea37bc8513a5868bccebfd5e5`  
		Last Modified: Tue, 05 Mar 2024 20:04:45 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:63e3bb18f43a20a50a640e33d80c15d6447e5c49eb758ad2ac92dd3c2215e1d9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2177356061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51bf8c2ce948dfc3bc85a84137d8ed09be2f3b755821c887f151431733f69def`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:31:24 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Feb 2024 20:31:24 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Feb 2024 20:31:25 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Feb 2024 20:31:26 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Feb 2024 20:33:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:33:15 GMT
ENV GOPATH=C:\go
# Wed, 14 Feb 2024 20:34:38 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Mar 2024 19:30:18 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 19:33:39 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Mar 2024 19:33:40 GMT
WORKDIR C:\go
# Tue, 05 Mar 2024 20:00:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Mar 2024 20:00:06 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:00:06 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:00:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:03:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 05 Mar 2024 20:03:10 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001ba7ca58e0032ab21885ed5be98699fa0e8693d84ce59492bbdeb45a1f5b89`  
		Last Modified: Wed, 14 Feb 2024 20:57:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964f6547b697b5014d27c4ae5aa9115c1686907b1f2524f8f0de888da7a79bd8`  
		Last Modified: Wed, 14 Feb 2024 20:57:29 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f83e22effb8739ec3fdcae64612cffac4ee7579638549caf47c70342693285`  
		Last Modified: Wed, 14 Feb 2024 20:57:29 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce41b07883cf81f89185e0e1b4fc65b39258a3f1aaff0ce01028854071ddecb`  
		Last Modified: Wed, 14 Feb 2024 20:57:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7954912de33be8cc7e1e4ea36180acfc8bb6cc7b7dc043d43d5912cfd171cd3`  
		Last Modified: Wed, 14 Feb 2024 20:57:33 GMT  
		Size: 25.6 MB (25560320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c63eb439e08d84b2f39090a2a87819fe70e5dfe666f3d4c4d3985acfd1364b0`  
		Last Modified: Wed, 14 Feb 2024 20:57:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fef719b5ba36fc0af1638fb03777e938c25331563e1d178a89bae94d428c8fb`  
		Last Modified: Wed, 14 Feb 2024 20:57:27 GMT  
		Size: 285.4 KB (285394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8d167b3e7ee16cfc662a87231b4084716742686d31d5b82e887b234efec2e9`  
		Last Modified: Tue, 05 Mar 2024 19:42:21 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c28621adc2c564252debe98669a98b5db5ce45172ce843466e26b8b689b114a`  
		Last Modified: Tue, 05 Mar 2024 19:42:40 GMT  
		Size: 69.4 MB (69364712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5c43bdc8404f132a84e8a0f4c69e490b01b908e8633abcfe604de71e205648`  
		Last Modified: Tue, 05 Mar 2024 19:42:21 GMT  
		Size: 1.5 KB (1545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcc239c5226abef94ce51a464e18875c9ff8a1fded12c55a44a3396d065d9a0`  
		Last Modified: Tue, 05 Mar 2024 20:04:31 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92819fb904e989755feedb88fdac313dd0614617cb2124f845e1beb9ef0b7840`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866ca856d15d8b11f3251d0e1e751bce5ccd3d04170d016b81a7e721ee811cff`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478c6e5efb5198c62dae853963d276055bc2ce33ae70aca26cba13a16359a054`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806deb5a287a2c1cfa951ac44704c97b32856f31e9d0012590d79e5b068279f1`  
		Last Modified: Tue, 05 Mar 2024 20:04:30 GMT  
		Size: 1.7 MB (1678307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bb868ab3b0ea5f9e471cb10db42cf456ce7dfe4ecb2ec8769a9c97c105483e`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:efedb356080be1cd5584baa80df964cbe3d85af049bbfee7775d9659e1809360
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
$ docker pull caddy@sha256:683161d33599ee7740b25d8c0466e82bfd94e491c63bef744eda38919853dd62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76973779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e7c249761d733da653482a2b5259eaae803dee4354bc3562e48a601315e6ff`
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
# Tue, 05 Mar 2024 19:42:13 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 19:42:13 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 19:42:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 19:42:15 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 19:42:15 GMT
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
	-	`sha256:ddc853d0ab24d3fe195e8492db2866ec9d01681c218bdff73afb081fa97cb002`  
		Last Modified: Tue, 05 Mar 2024 19:42:32 GMT  
		Size: 5.0 MB (4972975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea68e3f24bc6efb27b70b8c1870bf11b4a5fad53eb40e8ce77817c21586972d`  
		Last Modified: Tue, 05 Mar 2024 19:42:31 GMT  
		Size: 1.3 MB (1302236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ecce85dc39a9d244f2c3b1e0e89e72279e6d9f6b154afad2171642b11c137b`  
		Last Modified: Tue, 05 Mar 2024 19:42:31 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ece7f11958f255486a5be355c9180900873b391449f4258706b535d5177b40b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75407413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22234bb36f9348628e9caea0dac041e47e0df57676643cb27bc893380168cbd`
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
# Tue, 05 Mar 2024 23:00:43 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 23:00:43 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 23:00:44 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 23:00:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 23:00:44 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 23:00:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 23:00:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 23:00:49 GMT
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
	-	`sha256:bccd7f5c5a4f0abc0a23393d9a04f353b767b809c6ac950caaa731dd3768c8eb`  
		Last Modified: Tue, 05 Mar 2024 20:11:40 GMT  
		Size: 65.8 MB (65767479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33a4721f193119280f7dfc5baed0ce6a2d3b2eb94e31901d986ea54166c41ea`  
		Last Modified: Tue, 05 Mar 2024 20:11:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28b5e7a7f3d8467fb26f35d8b70ae0853d39fb4103058a0dc47dd62be3256d7`  
		Last Modified: Tue, 05 Mar 2024 23:01:07 GMT  
		Size: 5.0 MB (4958742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276c5f8fd9c641c6036e92487a700ea1b6cc811b8ac1578ff0f94803223f6e0d`  
		Last Modified: Tue, 05 Mar 2024 23:01:07 GMT  
		Size: 1.2 MB (1248648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db777cbc747c60df3dc9c90c42c55125b12f7c65e05a6b1ab52ec8de565848a9`  
		Last Modified: Tue, 05 Mar 2024 23:01:06 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:156f7188ad9f04c359241e42567a3cee24477cb1885639d634da45c042cc297e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2a4fac0ed075caa114df1d0fd560d017af28251032ec5015a49c0702fe3d48`
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
# Tue, 05 Mar 2024 20:48:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:48:44 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:48:45 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:48:45 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:48:45 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:48:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:48:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:48:48 GMT
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
	-	`sha256:17f0c2683a0605dfb4fff92a0c34044c42624cbc47515f2262026e23ffa28b15`  
		Last Modified: Tue, 05 Mar 2024 20:01:25 GMT  
		Size: 65.8 MB (65767445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1570cef4f4f43311a29ff4036cc73329f8fe806fb19c51f3413b3073bfc70634`  
		Last Modified: Tue, 05 Mar 2024 20:01:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2640aa4bbda58460e9e4fd9b0a0969303c9a30ba9b9ff6424d9349f7c0ffbcd`  
		Last Modified: Tue, 05 Mar 2024 20:49:09 GMT  
		Size: 4.5 MB (4514657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5f06f998d08d9a0ca561581720f1399d9e1c6f64b4637370acd8eddc90418e`  
		Last Modified: Tue, 05 Mar 2024 20:49:08 GMT  
		Size: 1.2 MB (1246081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f58b57eb0adfeabad656db0f59a85f8373054397123d068fe68452663713a9f`  
		Last Modified: Tue, 05 Mar 2024 20:49:08 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:b7d23a0e6f86ad993855c69a14f149837072ce99399627ee74d95e4705784d14
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73993792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0728d6faf4e6faebb8c082c95826cc671a39f43e1cd9ef0cfcd909a42435c9bd`
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
# Tue, 05 Mar 2024 20:00:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:00:21 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:00:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:00:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:00:23 GMT
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
	-	`sha256:5a91045fa00056cff12698db93bed8fe188f9895b74e96e29b6a9f6a6e047937`  
		Last Modified: Tue, 05 Mar 2024 19:44:44 GMT  
		Size: 64.1 MB (64111148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f155e563ada2bb78e99decac187a48adcf9db3cd56e543bc0694674ef8a234`  
		Last Modified: Tue, 05 Mar 2024 19:44:35 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f627d8e1519d50a70f854d0342a035bd62a8cedf0d7a61351f7ac191accf21`  
		Last Modified: Tue, 05 Mar 2024 20:00:40 GMT  
		Size: 5.1 MB (5063926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cf96a60cd43a372ff273debacac6160f6842de4adc5e79eef190c8a791eecc`  
		Last Modified: Tue, 05 Mar 2024 20:00:39 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113a17d73127a40aa417b169724fea00b3b34ed479e7d3fb2b656325c7d131a8`  
		Last Modified: Tue, 05 Mar 2024 20:00:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:3321233002d79314df5692f81246bbcc2d0c9ba268c61792fd6269b1e64e6ff9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74219843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b9b8fd2c1e8bd5b65bfbd17b919aabf00faf29ce73a1702c8a2610afe5427c`
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
# Tue, 05 Mar 2024 19:40:39 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 19:40:40 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 19:40:40 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 19:40:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 19:40:41 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 19:40:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 19:40:44 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 19:40:44 GMT
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
	-	`sha256:1e1323fc82438c3a0b40c7bcf18c7b4808edcec55b91135df534741787df9cbc`  
		Last Modified: Tue, 05 Mar 2024 19:25:03 GMT  
		Size: 64.1 MB (64126907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8630ef56928609490ea4cc1460f549f49e84ed6ff4f6bb7ffb5c3fa5e53f3027`  
		Last Modified: Tue, 05 Mar 2024 19:24:51 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c2f5a4fa35cf481005994eef4a926ba3b1cecb6ee2747d8080460c88a7fa6c`  
		Last Modified: Tue, 05 Mar 2024 19:41:02 GMT  
		Size: 5.3 MB (5270995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cba91d041ae77cf958d8509d23d6f741eec735e9bf9a24d489d0b8842db30c9`  
		Last Modified: Tue, 05 Mar 2024 19:41:01 GMT  
		Size: 1.2 MB (1186176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de13da806adead3ab5a4380c923e80ebddfc28b7b94d6e6f43b6cbb920acd85`  
		Last Modified: Tue, 05 Mar 2024 19:41:01 GMT  
		Size: 407.0 B  
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
$ docker pull caddy@sha256:7a4365fc853bf4ac7b497c662da666883c7471fb89275c320e38fe77949144f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:63e3bb18f43a20a50a640e33d80c15d6447e5c49eb758ad2ac92dd3c2215e1d9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2177356061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51bf8c2ce948dfc3bc85a84137d8ed09be2f3b755821c887f151431733f69def`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:31:24 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Feb 2024 20:31:24 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Feb 2024 20:31:25 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Feb 2024 20:31:26 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Feb 2024 20:33:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:33:15 GMT
ENV GOPATH=C:\go
# Wed, 14 Feb 2024 20:34:38 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Mar 2024 19:30:18 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 19:33:39 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Mar 2024 19:33:40 GMT
WORKDIR C:\go
# Tue, 05 Mar 2024 20:00:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Mar 2024 20:00:06 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:00:06 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:00:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:03:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 05 Mar 2024 20:03:10 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001ba7ca58e0032ab21885ed5be98699fa0e8693d84ce59492bbdeb45a1f5b89`  
		Last Modified: Wed, 14 Feb 2024 20:57:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964f6547b697b5014d27c4ae5aa9115c1686907b1f2524f8f0de888da7a79bd8`  
		Last Modified: Wed, 14 Feb 2024 20:57:29 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f83e22effb8739ec3fdcae64612cffac4ee7579638549caf47c70342693285`  
		Last Modified: Wed, 14 Feb 2024 20:57:29 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce41b07883cf81f89185e0e1b4fc65b39258a3f1aaff0ce01028854071ddecb`  
		Last Modified: Wed, 14 Feb 2024 20:57:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7954912de33be8cc7e1e4ea36180acfc8bb6cc7b7dc043d43d5912cfd171cd3`  
		Last Modified: Wed, 14 Feb 2024 20:57:33 GMT  
		Size: 25.6 MB (25560320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c63eb439e08d84b2f39090a2a87819fe70e5dfe666f3d4c4d3985acfd1364b0`  
		Last Modified: Wed, 14 Feb 2024 20:57:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fef719b5ba36fc0af1638fb03777e938c25331563e1d178a89bae94d428c8fb`  
		Last Modified: Wed, 14 Feb 2024 20:57:27 GMT  
		Size: 285.4 KB (285394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8d167b3e7ee16cfc662a87231b4084716742686d31d5b82e887b234efec2e9`  
		Last Modified: Tue, 05 Mar 2024 19:42:21 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c28621adc2c564252debe98669a98b5db5ce45172ce843466e26b8b689b114a`  
		Last Modified: Tue, 05 Mar 2024 19:42:40 GMT  
		Size: 69.4 MB (69364712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5c43bdc8404f132a84e8a0f4c69e490b01b908e8633abcfe604de71e205648`  
		Last Modified: Tue, 05 Mar 2024 19:42:21 GMT  
		Size: 1.5 KB (1545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcc239c5226abef94ce51a464e18875c9ff8a1fded12c55a44a3396d065d9a0`  
		Last Modified: Tue, 05 Mar 2024 20:04:31 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92819fb904e989755feedb88fdac313dd0614617cb2124f845e1beb9ef0b7840`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866ca856d15d8b11f3251d0e1e751bce5ccd3d04170d016b81a7e721ee811cff`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478c6e5efb5198c62dae853963d276055bc2ce33ae70aca26cba13a16359a054`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806deb5a287a2c1cfa951ac44704c97b32856f31e9d0012590d79e5b068279f1`  
		Last Modified: Tue, 05 Mar 2024 20:04:30 GMT  
		Size: 1.7 MB (1678307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bb868ab3b0ea5f9e471cb10db42cf456ce7dfe4ecb2ec8769a9c97c105483e`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:9ffd2fc461bcd523f2c67f8692ea85156c40fb2b21e35b457547522153eb44b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:e924a818b35c77fa77b850501f876fa811c43019e884675210e1232eb23b13a6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2007476156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69198d50697c7c62515331afda3b6b548388fe7ecfbec519f7bcb8e8ab8e5155`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:27:24 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Feb 2024 20:27:25 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Feb 2024 20:27:26 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Feb 2024 20:27:27 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Feb 2024 20:28:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:28:04 GMT
ENV GOPATH=C:\go
# Wed, 14 Feb 2024 20:28:25 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Mar 2024 19:27:34 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 19:29:55 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Mar 2024 19:29:57 GMT
WORKDIR C:\go
# Tue, 05 Mar 2024 20:03:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Mar 2024 20:03:28 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:03:29 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:03:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:03:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 05 Mar 2024 20:03:52 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ac8de2d709384a84400f6f072b2d3d4c4d454ee27f8ec716db4964eabac3f8`  
		Last Modified: Wed, 14 Feb 2024 20:55:46 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70115ee0ce6c09f30645181ec6f80fe9ece4e9b51628fdbaa85ebd4e0ae979e1`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab323644de57af1911793c0a10501a7b21640f8e58484665dc2258f482cb943`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae53fd363daebfb127c2ba7e51543cf93130802d95e194fc71db09c52b9fe10c`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665a9a35030c2076331610dfe4c22866525c2b0ac219981d900f1b6178af5241`  
		Last Modified: Wed, 14 Feb 2024 20:55:50 GMT  
		Size: 25.5 MB (25534020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ab59c20a7391d04f68a3dc2b9d6eb4cfd1e7af0ddd33e30d2cd19f13535c0`  
		Last Modified: Wed, 14 Feb 2024 20:55:43 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a35884f3b4e6aa2080cc34668faeabacc75000ef04e2fe4ec3e76f166d992e4`  
		Last Modified: Wed, 14 Feb 2024 20:55:43 GMT  
		Size: 266.0 KB (265989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c81949701f9fd28f5c42cfa101f1e2c2858efdb4032e3c3a221ae64417094d`  
		Last Modified: Tue, 05 Mar 2024 19:41:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c07bf58a4a94d97d30abeee1c89ea03f4d6bb5ae58ba58a108ab8c14ce86d04`  
		Last Modified: Tue, 05 Mar 2024 19:42:12 GMT  
		Size: 69.4 MB (69350261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff66f61d5b04d89a7cd43a5718c2738ee8c932ff7976238576fcce4a9205188`  
		Last Modified: Tue, 05 Mar 2024 19:41:52 GMT  
		Size: 1.5 KB (1539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fff8f151323c49bef4ab32c69e1b7fb0bc1c38c418bc58f8d552450f83ddb4`  
		Last Modified: Tue, 05 Mar 2024 20:04:48 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad11e6d0d7e8e1cdeb21675479688d12574b1f3aaf78c017dcb3f3f0e461e94`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3bac1fc388577dc02e99cece1f2418b768a6b9131f03ccb3a12b5130d0657c`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2023c4236e1ee6e1e21d75518a4e0b041879053cca3a4d196a736c11ef937885`  
		Last Modified: Tue, 05 Mar 2024 20:04:45 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646022f7531f95a5e75674d8b4716cd2b10acf7080eacbcf1a9146ec3c17a381`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.7 MB (1653517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a594d21bdd61142fc0e9073bca5c902365dcacea37bc8513a5868bccebfd5e5`  
		Last Modified: Tue, 05 Mar 2024 20:04:45 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:444dc16652b598c3d6f69627e313944c17cb36a0adfc3c366fa738e2ed0e1895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `caddy:2-windowsservercore` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:f6e8f7815f3e03bc5d239d52a2bdeb473ff959a4b74bb86ee94b410cc2407c35
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1926683398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d9ff1f8c7723994d4a4f7c520159beedff8fe440b855a9fb6f57afdcae7b2b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:22:32 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:22:33 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:23:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:23:00 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:23:01 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:23:02 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:23:03 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:23:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:23:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:23:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:23:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:23:09 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:23:11 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:23:26 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:23:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ebcfc7e63facc5463d681dd534f084e021cc447cf46213aae377066d573493`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 458.4 KB (458447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bee2047afe4426d5715972f534b35ce0bc5ae241ae42982e37a64185c7a482`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39da07145bbe64c3ec2c032dafa6eb6ddf62130dba67e03a627cc2cb3788f9e2`  
		Last Modified: Wed, 14 Feb 2024 21:26:37 GMT  
		Size: 15.3 MB (15267126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c47f482128a80b23df310b1c1b71bfa176b010cdd91761fb1a9aa71c4812738`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dab75e60136c0cf03ae7e7ad030b7adb3aff8014f4fc0e412d1ce9c217bdd60`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db7f5e1b9057131a3d1e7f1439de34f87684add5ac177612296925ed37b654d`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ac08dfbec3219d30d64f54cc8e1b46009cf4327d55c288ca43d875eaff3763`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4fad3dd8e3739d27a2d3793ae4740b4cbf52999f2295ad370545f048730492`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91f700224a04849cd48e2ab6525d47b7188051110718ca045ca50452ce26cb3`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fe7f9176dbfd4a89d170a117169a90cd5f49a2c5b7a55ac4026288812b8b60`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4fc40cf63828021df321258238a85d39918d2749a117bb0538bda0afce3aef`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9621f5d2e06bf68f778ba42ec6ec5d4a80d1cfb1204ea19b5a2b42d2b1d87d`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398c5b0cde2fcd40c8ce079d93fd115bd8ee7d8028cabc4baf9ecc07ab226410`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60cb86bd52f82372e11b1b851709ccb6c10537dc9262f63ef8bcd0152efb235`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c35a9695bf632732db6dd52a7531c75c5243819b2b8d7c019a1e8fc796e13c7`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c98226f721bed207883df26f4d35276821dd38299a62458d2ba6c55fab5b0d`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b23541f7ccf5a2debb904fdc41eccc03284d7fbf3baff61798b726d7c9ba12`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ce3a452fdfcd413ac385a157633a0fe389a8c2fdb281ce79b5cdd4d16dcb9b`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 281.4 KB (281363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7be2379ebd2e4d0fca0bbf81dd2628e93d8efd2ef3ea28c3872855ca6e50ed`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:793d5d17edca1d44e963efc2d79f97a389420f253790a04d54f9388492ca70ff
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2096464983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2636f0474ebff3dfb86f6d92e45af2173f0773887039f3e30776eb3b2de1bd0c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:18:41 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:18:42 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:20:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:20:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:20:23 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:20:24 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:20:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:20:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:20:31 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:20:33 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:20:34 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:20:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:20:36 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:20:36 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:20:37 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:20:38 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:20:40 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:21:47 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:21:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936f6b22f9979fac96518b60eadd4d9156939b025d673ce61a2e6a18553dc2b1`  
		Last Modified: Wed, 14 Feb 2024 21:26:08 GMT  
		Size: 461.6 KB (461622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72873b058a9927d9ea1e4a234006a54fec29d1da3beb3f2834ce66fda6f4262f`  
		Last Modified: Wed, 14 Feb 2024 21:26:07 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc3d79323d38d65e8112fca8b77ad54434883a9104dd542fdc179cf782fab1e`  
		Last Modified: Wed, 14 Feb 2024 21:26:10 GMT  
		Size: 15.3 MB (15274562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4873aaa427e9ae13aeebcc096c23b92dd4d61d1f6b601a755dfaf268c4b85ab6`  
		Last Modified: Wed, 14 Feb 2024 21:26:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c57d3fae417c15ca2cf9d965bd8d05bab080154e20cd2e20f5d71aa86de5c0f`  
		Last Modified: Wed, 14 Feb 2024 21:26:06 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444c12e07ce56e352f094a12c03aa1ab4110c79d5daa78eea733580703bdef6a`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cf5cd505e0ce461fb00191ec16014104c1f3f38c373b2179b9cb0ecec44082`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f67f42fce82938d220cec3933239aedeffe9da096d14f3354eb2ffd49902c8`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb581bc05a23526a9b12256e17b6963201710bb71ae435fed4ccbdc69330fe8`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806d41685663d3f82e404087dda88f57f3f2534966be1a73998da0d9d3f15ae8`  
		Last Modified: Wed, 14 Feb 2024 21:26:04 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af65ac33d93c108086650ad059ffe57d44fcae5dfcfd80f331aeb3acb759145`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1d5135587234fcaf02c388f1fbf2e4a7be50b81f4c5296aeb7a99cb5fc2d13`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705d9a64f11bac49a31ef3cb6bfd926024e700d3daf666b277867cddcef7fcff`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac09729a4577f5fe6afe0d3a00560ec715f86b1e907e28917ca6d13dcafb3e7`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cd769674ca72532329328651bf168fe61494249405bb59e89832d94410289b`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a7dedf94b664393c8ae954445d5b582ffe6d8ffc604ddaaae79b20de72317`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a465dd935213cb9e1bd4aae1e392fd32e5fcb661c6bf3b7a50e113ea7077d7`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d18f93e3aab637778f45296a721f0857d0c5ec759335b634ae323255bbb0c29`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 257.6 KB (257571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11c0d021a3877f354347717399af0fe31b30ddd220f2b64b4ccf68fe7b6140b`  
		Last Modified: Wed, 14 Feb 2024 21:26:02 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:fa377f42fcef67994cd1ff2eca1715f8ddbb6836a84cc7a6b796df01353d6f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:793d5d17edca1d44e963efc2d79f97a389420f253790a04d54f9388492ca70ff
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2096464983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2636f0474ebff3dfb86f6d92e45af2173f0773887039f3e30776eb3b2de1bd0c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:18:41 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:18:42 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:20:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:20:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:20:23 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:20:24 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:20:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:20:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:20:31 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:20:33 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:20:34 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:20:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:20:36 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:20:36 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:20:37 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:20:38 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:20:40 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:21:47 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:21:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936f6b22f9979fac96518b60eadd4d9156939b025d673ce61a2e6a18553dc2b1`  
		Last Modified: Wed, 14 Feb 2024 21:26:08 GMT  
		Size: 461.6 KB (461622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72873b058a9927d9ea1e4a234006a54fec29d1da3beb3f2834ce66fda6f4262f`  
		Last Modified: Wed, 14 Feb 2024 21:26:07 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc3d79323d38d65e8112fca8b77ad54434883a9104dd542fdc179cf782fab1e`  
		Last Modified: Wed, 14 Feb 2024 21:26:10 GMT  
		Size: 15.3 MB (15274562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4873aaa427e9ae13aeebcc096c23b92dd4d61d1f6b601a755dfaf268c4b85ab6`  
		Last Modified: Wed, 14 Feb 2024 21:26:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c57d3fae417c15ca2cf9d965bd8d05bab080154e20cd2e20f5d71aa86de5c0f`  
		Last Modified: Wed, 14 Feb 2024 21:26:06 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444c12e07ce56e352f094a12c03aa1ab4110c79d5daa78eea733580703bdef6a`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cf5cd505e0ce461fb00191ec16014104c1f3f38c373b2179b9cb0ecec44082`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f67f42fce82938d220cec3933239aedeffe9da096d14f3354eb2ffd49902c8`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb581bc05a23526a9b12256e17b6963201710bb71ae435fed4ccbdc69330fe8`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806d41685663d3f82e404087dda88f57f3f2534966be1a73998da0d9d3f15ae8`  
		Last Modified: Wed, 14 Feb 2024 21:26:04 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af65ac33d93c108086650ad059ffe57d44fcae5dfcfd80f331aeb3acb759145`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1d5135587234fcaf02c388f1fbf2e4a7be50b81f4c5296aeb7a99cb5fc2d13`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705d9a64f11bac49a31ef3cb6bfd926024e700d3daf666b277867cddcef7fcff`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac09729a4577f5fe6afe0d3a00560ec715f86b1e907e28917ca6d13dcafb3e7`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cd769674ca72532329328651bf168fe61494249405bb59e89832d94410289b`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a7dedf94b664393c8ae954445d5b582ffe6d8ffc604ddaaae79b20de72317`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a465dd935213cb9e1bd4aae1e392fd32e5fcb661c6bf3b7a50e113ea7077d7`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d18f93e3aab637778f45296a721f0857d0c5ec759335b634ae323255bbb0c29`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 257.6 KB (257571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11c0d021a3877f354347717399af0fe31b30ddd220f2b64b4ccf68fe7b6140b`  
		Last Modified: Wed, 14 Feb 2024 21:26:02 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:6e915ccce3def5db60e3af13d28e398bfdbde6a3298781b0cf53cbb174b0f23e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:f6e8f7815f3e03bc5d239d52a2bdeb473ff959a4b74bb86ee94b410cc2407c35
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1926683398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d9ff1f8c7723994d4a4f7c520159beedff8fe440b855a9fb6f57afdcae7b2b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:22:32 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:22:33 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:23:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:23:00 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:23:01 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:23:02 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:23:03 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:23:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:23:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:23:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:23:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:23:09 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:23:11 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:23:26 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:23:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ebcfc7e63facc5463d681dd534f084e021cc447cf46213aae377066d573493`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 458.4 KB (458447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bee2047afe4426d5715972f534b35ce0bc5ae241ae42982e37a64185c7a482`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39da07145bbe64c3ec2c032dafa6eb6ddf62130dba67e03a627cc2cb3788f9e2`  
		Last Modified: Wed, 14 Feb 2024 21:26:37 GMT  
		Size: 15.3 MB (15267126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c47f482128a80b23df310b1c1b71bfa176b010cdd91761fb1a9aa71c4812738`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dab75e60136c0cf03ae7e7ad030b7adb3aff8014f4fc0e412d1ce9c217bdd60`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db7f5e1b9057131a3d1e7f1439de34f87684add5ac177612296925ed37b654d`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ac08dfbec3219d30d64f54cc8e1b46009cf4327d55c288ca43d875eaff3763`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4fad3dd8e3739d27a2d3793ae4740b4cbf52999f2295ad370545f048730492`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91f700224a04849cd48e2ab6525d47b7188051110718ca045ca50452ce26cb3`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fe7f9176dbfd4a89d170a117169a90cd5f49a2c5b7a55ac4026288812b8b60`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4fc40cf63828021df321258238a85d39918d2749a117bb0538bda0afce3aef`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9621f5d2e06bf68f778ba42ec6ec5d4a80d1cfb1204ea19b5a2b42d2b1d87d`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398c5b0cde2fcd40c8ce079d93fd115bd8ee7d8028cabc4baf9ecc07ab226410`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60cb86bd52f82372e11b1b851709ccb6c10537dc9262f63ef8bcd0152efb235`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c35a9695bf632732db6dd52a7531c75c5243819b2b8d7c019a1e8fc796e13c7`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c98226f721bed207883df26f4d35276821dd38299a62458d2ba6c55fab5b0d`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b23541f7ccf5a2debb904fdc41eccc03284d7fbf3baff61798b726d7c9ba12`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ce3a452fdfcd413ac385a157633a0fe389a8c2fdb281ce79b5cdd4d16dcb9b`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 281.4 KB (281363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7be2379ebd2e4d0fca0bbf81dd2628e93d8efd2ef3ea28c3872855ca6e50ed`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7`

```console
$ docker pull caddy@sha256:2a0d069ea95d91641d201943a5a049e83cbfade8039670aebfb441b132189de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

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

### `caddy:2.7` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:f6e8f7815f3e03bc5d239d52a2bdeb473ff959a4b74bb86ee94b410cc2407c35
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1926683398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d9ff1f8c7723994d4a4f7c520159beedff8fe440b855a9fb6f57afdcae7b2b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:22:32 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:22:33 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:23:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:23:00 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:23:01 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:23:02 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:23:03 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:23:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:23:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:23:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:23:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:23:09 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:23:11 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:23:26 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:23:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ebcfc7e63facc5463d681dd534f084e021cc447cf46213aae377066d573493`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 458.4 KB (458447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bee2047afe4426d5715972f534b35ce0bc5ae241ae42982e37a64185c7a482`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39da07145bbe64c3ec2c032dafa6eb6ddf62130dba67e03a627cc2cb3788f9e2`  
		Last Modified: Wed, 14 Feb 2024 21:26:37 GMT  
		Size: 15.3 MB (15267126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c47f482128a80b23df310b1c1b71bfa176b010cdd91761fb1a9aa71c4812738`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dab75e60136c0cf03ae7e7ad030b7adb3aff8014f4fc0e412d1ce9c217bdd60`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db7f5e1b9057131a3d1e7f1439de34f87684add5ac177612296925ed37b654d`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ac08dfbec3219d30d64f54cc8e1b46009cf4327d55c288ca43d875eaff3763`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4fad3dd8e3739d27a2d3793ae4740b4cbf52999f2295ad370545f048730492`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91f700224a04849cd48e2ab6525d47b7188051110718ca045ca50452ce26cb3`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fe7f9176dbfd4a89d170a117169a90cd5f49a2c5b7a55ac4026288812b8b60`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4fc40cf63828021df321258238a85d39918d2749a117bb0538bda0afce3aef`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9621f5d2e06bf68f778ba42ec6ec5d4a80d1cfb1204ea19b5a2b42d2b1d87d`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398c5b0cde2fcd40c8ce079d93fd115bd8ee7d8028cabc4baf9ecc07ab226410`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60cb86bd52f82372e11b1b851709ccb6c10537dc9262f63ef8bcd0152efb235`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c35a9695bf632732db6dd52a7531c75c5243819b2b8d7c019a1e8fc796e13c7`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c98226f721bed207883df26f4d35276821dd38299a62458d2ba6c55fab5b0d`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b23541f7ccf5a2debb904fdc41eccc03284d7fbf3baff61798b726d7c9ba12`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ce3a452fdfcd413ac385a157633a0fe389a8c2fdb281ce79b5cdd4d16dcb9b`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 281.4 KB (281363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7be2379ebd2e4d0fca0bbf81dd2628e93d8efd2ef3ea28c3872855ca6e50ed`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:793d5d17edca1d44e963efc2d79f97a389420f253790a04d54f9388492ca70ff
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2096464983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2636f0474ebff3dfb86f6d92e45af2173f0773887039f3e30776eb3b2de1bd0c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:18:41 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:18:42 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:20:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:20:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:20:23 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:20:24 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:20:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:20:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:20:31 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:20:33 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:20:34 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:20:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:20:36 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:20:36 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:20:37 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:20:38 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:20:40 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:21:47 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:21:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936f6b22f9979fac96518b60eadd4d9156939b025d673ce61a2e6a18553dc2b1`  
		Last Modified: Wed, 14 Feb 2024 21:26:08 GMT  
		Size: 461.6 KB (461622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72873b058a9927d9ea1e4a234006a54fec29d1da3beb3f2834ce66fda6f4262f`  
		Last Modified: Wed, 14 Feb 2024 21:26:07 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc3d79323d38d65e8112fca8b77ad54434883a9104dd542fdc179cf782fab1e`  
		Last Modified: Wed, 14 Feb 2024 21:26:10 GMT  
		Size: 15.3 MB (15274562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4873aaa427e9ae13aeebcc096c23b92dd4d61d1f6b601a755dfaf268c4b85ab6`  
		Last Modified: Wed, 14 Feb 2024 21:26:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c57d3fae417c15ca2cf9d965bd8d05bab080154e20cd2e20f5d71aa86de5c0f`  
		Last Modified: Wed, 14 Feb 2024 21:26:06 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444c12e07ce56e352f094a12c03aa1ab4110c79d5daa78eea733580703bdef6a`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cf5cd505e0ce461fb00191ec16014104c1f3f38c373b2179b9cb0ecec44082`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f67f42fce82938d220cec3933239aedeffe9da096d14f3354eb2ffd49902c8`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb581bc05a23526a9b12256e17b6963201710bb71ae435fed4ccbdc69330fe8`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806d41685663d3f82e404087dda88f57f3f2534966be1a73998da0d9d3f15ae8`  
		Last Modified: Wed, 14 Feb 2024 21:26:04 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af65ac33d93c108086650ad059ffe57d44fcae5dfcfd80f331aeb3acb759145`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1d5135587234fcaf02c388f1fbf2e4a7be50b81f4c5296aeb7a99cb5fc2d13`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705d9a64f11bac49a31ef3cb6bfd926024e700d3daf666b277867cddcef7fcff`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac09729a4577f5fe6afe0d3a00560ec715f86b1e907e28917ca6d13dcafb3e7`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cd769674ca72532329328651bf168fe61494249405bb59e89832d94410289b`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a7dedf94b664393c8ae954445d5b582ffe6d8ffc604ddaaae79b20de72317`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a465dd935213cb9e1bd4aae1e392fd32e5fcb661c6bf3b7a50e113ea7077d7`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d18f93e3aab637778f45296a721f0857d0c5ec759335b634ae323255bbb0c29`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 257.6 KB (257571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11c0d021a3877f354347717399af0fe31b30ddd220f2b64b4ccf68fe7b6140b`  
		Last Modified: Wed, 14 Feb 2024 21:26:02 GMT  
		Size: 1.3 KB (1333 bytes)  
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
$ docker pull caddy@sha256:7954f9183f22718dfac36955b6cb281466256ae195f30ffcd0229596e2badc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `caddy:2.7-builder` - linux; amd64

```console
$ docker pull caddy@sha256:683161d33599ee7740b25d8c0466e82bfd94e491c63bef744eda38919853dd62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76973779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e7c249761d733da653482a2b5259eaae803dee4354bc3562e48a601315e6ff`
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
# Tue, 05 Mar 2024 19:42:13 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 19:42:13 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 19:42:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 19:42:15 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 19:42:15 GMT
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
	-	`sha256:ddc853d0ab24d3fe195e8492db2866ec9d01681c218bdff73afb081fa97cb002`  
		Last Modified: Tue, 05 Mar 2024 19:42:32 GMT  
		Size: 5.0 MB (4972975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea68e3f24bc6efb27b70b8c1870bf11b4a5fad53eb40e8ce77817c21586972d`  
		Last Modified: Tue, 05 Mar 2024 19:42:31 GMT  
		Size: 1.3 MB (1302236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ecce85dc39a9d244f2c3b1e0e89e72279e6d9f6b154afad2171642b11c137b`  
		Last Modified: Tue, 05 Mar 2024 19:42:31 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ece7f11958f255486a5be355c9180900873b391449f4258706b535d5177b40b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75407413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22234bb36f9348628e9caea0dac041e47e0df57676643cb27bc893380168cbd`
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
# Tue, 05 Mar 2024 23:00:43 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 23:00:43 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 23:00:44 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 23:00:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 23:00:44 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 23:00:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 23:00:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 23:00:49 GMT
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
	-	`sha256:bccd7f5c5a4f0abc0a23393d9a04f353b767b809c6ac950caaa731dd3768c8eb`  
		Last Modified: Tue, 05 Mar 2024 20:11:40 GMT  
		Size: 65.8 MB (65767479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33a4721f193119280f7dfc5baed0ce6a2d3b2eb94e31901d986ea54166c41ea`  
		Last Modified: Tue, 05 Mar 2024 20:11:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28b5e7a7f3d8467fb26f35d8b70ae0853d39fb4103058a0dc47dd62be3256d7`  
		Last Modified: Tue, 05 Mar 2024 23:01:07 GMT  
		Size: 5.0 MB (4958742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276c5f8fd9c641c6036e92487a700ea1b6cc811b8ac1578ff0f94803223f6e0d`  
		Last Modified: Tue, 05 Mar 2024 23:01:07 GMT  
		Size: 1.2 MB (1248648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db777cbc747c60df3dc9c90c42c55125b12f7c65e05a6b1ab52ec8de565848a9`  
		Last Modified: Tue, 05 Mar 2024 23:01:06 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:156f7188ad9f04c359241e42567a3cee24477cb1885639d634da45c042cc297e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2a4fac0ed075caa114df1d0fd560d017af28251032ec5015a49c0702fe3d48`
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
# Tue, 05 Mar 2024 20:48:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:48:44 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:48:45 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:48:45 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:48:45 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:48:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:48:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:48:48 GMT
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
	-	`sha256:17f0c2683a0605dfb4fff92a0c34044c42624cbc47515f2262026e23ffa28b15`  
		Last Modified: Tue, 05 Mar 2024 20:01:25 GMT  
		Size: 65.8 MB (65767445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1570cef4f4f43311a29ff4036cc73329f8fe806fb19c51f3413b3073bfc70634`  
		Last Modified: Tue, 05 Mar 2024 20:01:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2640aa4bbda58460e9e4fd9b0a0969303c9a30ba9b9ff6424d9349f7c0ffbcd`  
		Last Modified: Tue, 05 Mar 2024 20:49:09 GMT  
		Size: 4.5 MB (4514657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5f06f998d08d9a0ca561581720f1399d9e1c6f64b4637370acd8eddc90418e`  
		Last Modified: Tue, 05 Mar 2024 20:49:08 GMT  
		Size: 1.2 MB (1246081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f58b57eb0adfeabad656db0f59a85f8373054397123d068fe68452663713a9f`  
		Last Modified: Tue, 05 Mar 2024 20:49:08 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:b7d23a0e6f86ad993855c69a14f149837072ce99399627ee74d95e4705784d14
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73993792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0728d6faf4e6faebb8c082c95826cc671a39f43e1cd9ef0cfcd909a42435c9bd`
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
# Tue, 05 Mar 2024 20:00:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:00:21 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:00:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:00:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:00:23 GMT
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
	-	`sha256:5a91045fa00056cff12698db93bed8fe188f9895b74e96e29b6a9f6a6e047937`  
		Last Modified: Tue, 05 Mar 2024 19:44:44 GMT  
		Size: 64.1 MB (64111148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f155e563ada2bb78e99decac187a48adcf9db3cd56e543bc0694674ef8a234`  
		Last Modified: Tue, 05 Mar 2024 19:44:35 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f627d8e1519d50a70f854d0342a035bd62a8cedf0d7a61351f7ac191accf21`  
		Last Modified: Tue, 05 Mar 2024 20:00:40 GMT  
		Size: 5.1 MB (5063926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cf96a60cd43a372ff273debacac6160f6842de4adc5e79eef190c8a791eecc`  
		Last Modified: Tue, 05 Mar 2024 20:00:39 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113a17d73127a40aa417b169724fea00b3b34ed479e7d3fb2b656325c7d131a8`  
		Last Modified: Tue, 05 Mar 2024 20:00:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:3321233002d79314df5692f81246bbcc2d0c9ba268c61792fd6269b1e64e6ff9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74219843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b9b8fd2c1e8bd5b65bfbd17b919aabf00faf29ce73a1702c8a2610afe5427c`
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
# Tue, 05 Mar 2024 19:40:39 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 19:40:40 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 19:40:40 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 19:40:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 19:40:41 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 19:40:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 19:40:44 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 19:40:44 GMT
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
	-	`sha256:1e1323fc82438c3a0b40c7bcf18c7b4808edcec55b91135df534741787df9cbc`  
		Last Modified: Tue, 05 Mar 2024 19:25:03 GMT  
		Size: 64.1 MB (64126907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8630ef56928609490ea4cc1460f549f49e84ed6ff4f6bb7ffb5c3fa5e53f3027`  
		Last Modified: Tue, 05 Mar 2024 19:24:51 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c2f5a4fa35cf481005994eef4a926ba3b1cecb6ee2747d8080460c88a7fa6c`  
		Last Modified: Tue, 05 Mar 2024 19:41:02 GMT  
		Size: 5.3 MB (5270995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cba91d041ae77cf958d8509d23d6f741eec735e9bf9a24d489d0b8842db30c9`  
		Last Modified: Tue, 05 Mar 2024 19:41:01 GMT  
		Size: 1.2 MB (1186176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de13da806adead3ab5a4380c923e80ebddfc28b7b94d6e6f43b6cbb920acd85`  
		Last Modified: Tue, 05 Mar 2024 19:41:01 GMT  
		Size: 407.0 B  
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

### `caddy:2.7-builder` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:e924a818b35c77fa77b850501f876fa811c43019e884675210e1232eb23b13a6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2007476156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69198d50697c7c62515331afda3b6b548388fe7ecfbec519f7bcb8e8ab8e5155`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:27:24 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Feb 2024 20:27:25 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Feb 2024 20:27:26 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Feb 2024 20:27:27 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Feb 2024 20:28:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:28:04 GMT
ENV GOPATH=C:\go
# Wed, 14 Feb 2024 20:28:25 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Mar 2024 19:27:34 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 19:29:55 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Mar 2024 19:29:57 GMT
WORKDIR C:\go
# Tue, 05 Mar 2024 20:03:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Mar 2024 20:03:28 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:03:29 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:03:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:03:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 05 Mar 2024 20:03:52 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ac8de2d709384a84400f6f072b2d3d4c4d454ee27f8ec716db4964eabac3f8`  
		Last Modified: Wed, 14 Feb 2024 20:55:46 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70115ee0ce6c09f30645181ec6f80fe9ece4e9b51628fdbaa85ebd4e0ae979e1`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab323644de57af1911793c0a10501a7b21640f8e58484665dc2258f482cb943`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae53fd363daebfb127c2ba7e51543cf93130802d95e194fc71db09c52b9fe10c`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665a9a35030c2076331610dfe4c22866525c2b0ac219981d900f1b6178af5241`  
		Last Modified: Wed, 14 Feb 2024 20:55:50 GMT  
		Size: 25.5 MB (25534020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ab59c20a7391d04f68a3dc2b9d6eb4cfd1e7af0ddd33e30d2cd19f13535c0`  
		Last Modified: Wed, 14 Feb 2024 20:55:43 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a35884f3b4e6aa2080cc34668faeabacc75000ef04e2fe4ec3e76f166d992e4`  
		Last Modified: Wed, 14 Feb 2024 20:55:43 GMT  
		Size: 266.0 KB (265989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c81949701f9fd28f5c42cfa101f1e2c2858efdb4032e3c3a221ae64417094d`  
		Last Modified: Tue, 05 Mar 2024 19:41:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c07bf58a4a94d97d30abeee1c89ea03f4d6bb5ae58ba58a108ab8c14ce86d04`  
		Last Modified: Tue, 05 Mar 2024 19:42:12 GMT  
		Size: 69.4 MB (69350261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff66f61d5b04d89a7cd43a5718c2738ee8c932ff7976238576fcce4a9205188`  
		Last Modified: Tue, 05 Mar 2024 19:41:52 GMT  
		Size: 1.5 KB (1539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fff8f151323c49bef4ab32c69e1b7fb0bc1c38c418bc58f8d552450f83ddb4`  
		Last Modified: Tue, 05 Mar 2024 20:04:48 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad11e6d0d7e8e1cdeb21675479688d12574b1f3aaf78c017dcb3f3f0e461e94`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3bac1fc388577dc02e99cece1f2418b768a6b9131f03ccb3a12b5130d0657c`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2023c4236e1ee6e1e21d75518a4e0b041879053cca3a4d196a736c11ef937885`  
		Last Modified: Tue, 05 Mar 2024 20:04:45 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646022f7531f95a5e75674d8b4716cd2b10acf7080eacbcf1a9146ec3c17a381`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.7 MB (1653517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a594d21bdd61142fc0e9073bca5c902365dcacea37bc8513a5868bccebfd5e5`  
		Last Modified: Tue, 05 Mar 2024 20:04:45 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:63e3bb18f43a20a50a640e33d80c15d6447e5c49eb758ad2ac92dd3c2215e1d9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2177356061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51bf8c2ce948dfc3bc85a84137d8ed09be2f3b755821c887f151431733f69def`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:31:24 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Feb 2024 20:31:24 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Feb 2024 20:31:25 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Feb 2024 20:31:26 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Feb 2024 20:33:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:33:15 GMT
ENV GOPATH=C:\go
# Wed, 14 Feb 2024 20:34:38 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Mar 2024 19:30:18 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 19:33:39 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Mar 2024 19:33:40 GMT
WORKDIR C:\go
# Tue, 05 Mar 2024 20:00:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Mar 2024 20:00:06 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:00:06 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:00:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:03:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 05 Mar 2024 20:03:10 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001ba7ca58e0032ab21885ed5be98699fa0e8693d84ce59492bbdeb45a1f5b89`  
		Last Modified: Wed, 14 Feb 2024 20:57:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964f6547b697b5014d27c4ae5aa9115c1686907b1f2524f8f0de888da7a79bd8`  
		Last Modified: Wed, 14 Feb 2024 20:57:29 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f83e22effb8739ec3fdcae64612cffac4ee7579638549caf47c70342693285`  
		Last Modified: Wed, 14 Feb 2024 20:57:29 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce41b07883cf81f89185e0e1b4fc65b39258a3f1aaff0ce01028854071ddecb`  
		Last Modified: Wed, 14 Feb 2024 20:57:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7954912de33be8cc7e1e4ea36180acfc8bb6cc7b7dc043d43d5912cfd171cd3`  
		Last Modified: Wed, 14 Feb 2024 20:57:33 GMT  
		Size: 25.6 MB (25560320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c63eb439e08d84b2f39090a2a87819fe70e5dfe666f3d4c4d3985acfd1364b0`  
		Last Modified: Wed, 14 Feb 2024 20:57:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fef719b5ba36fc0af1638fb03777e938c25331563e1d178a89bae94d428c8fb`  
		Last Modified: Wed, 14 Feb 2024 20:57:27 GMT  
		Size: 285.4 KB (285394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8d167b3e7ee16cfc662a87231b4084716742686d31d5b82e887b234efec2e9`  
		Last Modified: Tue, 05 Mar 2024 19:42:21 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c28621adc2c564252debe98669a98b5db5ce45172ce843466e26b8b689b114a`  
		Last Modified: Tue, 05 Mar 2024 19:42:40 GMT  
		Size: 69.4 MB (69364712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5c43bdc8404f132a84e8a0f4c69e490b01b908e8633abcfe604de71e205648`  
		Last Modified: Tue, 05 Mar 2024 19:42:21 GMT  
		Size: 1.5 KB (1545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcc239c5226abef94ce51a464e18875c9ff8a1fded12c55a44a3396d065d9a0`  
		Last Modified: Tue, 05 Mar 2024 20:04:31 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92819fb904e989755feedb88fdac313dd0614617cb2124f845e1beb9ef0b7840`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866ca856d15d8b11f3251d0e1e751bce5ccd3d04170d016b81a7e721ee811cff`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478c6e5efb5198c62dae853963d276055bc2ce33ae70aca26cba13a16359a054`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806deb5a287a2c1cfa951ac44704c97b32856f31e9d0012590d79e5b068279f1`  
		Last Modified: Tue, 05 Mar 2024 20:04:30 GMT  
		Size: 1.7 MB (1678307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bb868ab3b0ea5f9e471cb10db42cf456ce7dfe4ecb2ec8769a9c97c105483e`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-alpine`

```console
$ docker pull caddy@sha256:efedb356080be1cd5584baa80df964cbe3d85af049bbfee7775d9659e1809360
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
$ docker pull caddy@sha256:683161d33599ee7740b25d8c0466e82bfd94e491c63bef744eda38919853dd62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76973779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e7c249761d733da653482a2b5259eaae803dee4354bc3562e48a601315e6ff`
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
# Tue, 05 Mar 2024 19:42:13 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 19:42:13 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 19:42:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 19:42:15 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 19:42:15 GMT
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
	-	`sha256:ddc853d0ab24d3fe195e8492db2866ec9d01681c218bdff73afb081fa97cb002`  
		Last Modified: Tue, 05 Mar 2024 19:42:32 GMT  
		Size: 5.0 MB (4972975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea68e3f24bc6efb27b70b8c1870bf11b4a5fad53eb40e8ce77817c21586972d`  
		Last Modified: Tue, 05 Mar 2024 19:42:31 GMT  
		Size: 1.3 MB (1302236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ecce85dc39a9d244f2c3b1e0e89e72279e6d9f6b154afad2171642b11c137b`  
		Last Modified: Tue, 05 Mar 2024 19:42:31 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ece7f11958f255486a5be355c9180900873b391449f4258706b535d5177b40b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75407413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22234bb36f9348628e9caea0dac041e47e0df57676643cb27bc893380168cbd`
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
# Tue, 05 Mar 2024 23:00:43 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 23:00:43 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 23:00:44 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 23:00:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 23:00:44 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 23:00:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 23:00:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 23:00:49 GMT
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
	-	`sha256:bccd7f5c5a4f0abc0a23393d9a04f353b767b809c6ac950caaa731dd3768c8eb`  
		Last Modified: Tue, 05 Mar 2024 20:11:40 GMT  
		Size: 65.8 MB (65767479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33a4721f193119280f7dfc5baed0ce6a2d3b2eb94e31901d986ea54166c41ea`  
		Last Modified: Tue, 05 Mar 2024 20:11:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28b5e7a7f3d8467fb26f35d8b70ae0853d39fb4103058a0dc47dd62be3256d7`  
		Last Modified: Tue, 05 Mar 2024 23:01:07 GMT  
		Size: 5.0 MB (4958742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276c5f8fd9c641c6036e92487a700ea1b6cc811b8ac1578ff0f94803223f6e0d`  
		Last Modified: Tue, 05 Mar 2024 23:01:07 GMT  
		Size: 1.2 MB (1248648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db777cbc747c60df3dc9c90c42c55125b12f7c65e05a6b1ab52ec8de565848a9`  
		Last Modified: Tue, 05 Mar 2024 23:01:06 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:156f7188ad9f04c359241e42567a3cee24477cb1885639d634da45c042cc297e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2a4fac0ed075caa114df1d0fd560d017af28251032ec5015a49c0702fe3d48`
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
# Tue, 05 Mar 2024 20:48:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:48:44 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:48:45 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:48:45 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:48:45 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:48:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:48:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:48:48 GMT
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
	-	`sha256:17f0c2683a0605dfb4fff92a0c34044c42624cbc47515f2262026e23ffa28b15`  
		Last Modified: Tue, 05 Mar 2024 20:01:25 GMT  
		Size: 65.8 MB (65767445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1570cef4f4f43311a29ff4036cc73329f8fe806fb19c51f3413b3073bfc70634`  
		Last Modified: Tue, 05 Mar 2024 20:01:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2640aa4bbda58460e9e4fd9b0a0969303c9a30ba9b9ff6424d9349f7c0ffbcd`  
		Last Modified: Tue, 05 Mar 2024 20:49:09 GMT  
		Size: 4.5 MB (4514657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5f06f998d08d9a0ca561581720f1399d9e1c6f64b4637370acd8eddc90418e`  
		Last Modified: Tue, 05 Mar 2024 20:49:08 GMT  
		Size: 1.2 MB (1246081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f58b57eb0adfeabad656db0f59a85f8373054397123d068fe68452663713a9f`  
		Last Modified: Tue, 05 Mar 2024 20:49:08 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:b7d23a0e6f86ad993855c69a14f149837072ce99399627ee74d95e4705784d14
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73993792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0728d6faf4e6faebb8c082c95826cc671a39f43e1cd9ef0cfcd909a42435c9bd`
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
# Tue, 05 Mar 2024 20:00:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:00:21 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:00:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:00:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:00:23 GMT
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
	-	`sha256:5a91045fa00056cff12698db93bed8fe188f9895b74e96e29b6a9f6a6e047937`  
		Last Modified: Tue, 05 Mar 2024 19:44:44 GMT  
		Size: 64.1 MB (64111148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f155e563ada2bb78e99decac187a48adcf9db3cd56e543bc0694674ef8a234`  
		Last Modified: Tue, 05 Mar 2024 19:44:35 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f627d8e1519d50a70f854d0342a035bd62a8cedf0d7a61351f7ac191accf21`  
		Last Modified: Tue, 05 Mar 2024 20:00:40 GMT  
		Size: 5.1 MB (5063926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cf96a60cd43a372ff273debacac6160f6842de4adc5e79eef190c8a791eecc`  
		Last Modified: Tue, 05 Mar 2024 20:00:39 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113a17d73127a40aa417b169724fea00b3b34ed479e7d3fb2b656325c7d131a8`  
		Last Modified: Tue, 05 Mar 2024 20:00:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:3321233002d79314df5692f81246bbcc2d0c9ba268c61792fd6269b1e64e6ff9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74219843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b9b8fd2c1e8bd5b65bfbd17b919aabf00faf29ce73a1702c8a2610afe5427c`
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
# Tue, 05 Mar 2024 19:40:39 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 19:40:40 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 19:40:40 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 19:40:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 19:40:41 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 19:40:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 19:40:44 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 19:40:44 GMT
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
	-	`sha256:1e1323fc82438c3a0b40c7bcf18c7b4808edcec55b91135df534741787df9cbc`  
		Last Modified: Tue, 05 Mar 2024 19:25:03 GMT  
		Size: 64.1 MB (64126907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8630ef56928609490ea4cc1460f549f49e84ed6ff4f6bb7ffb5c3fa5e53f3027`  
		Last Modified: Tue, 05 Mar 2024 19:24:51 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c2f5a4fa35cf481005994eef4a926ba3b1cecb6ee2747d8080460c88a7fa6c`  
		Last Modified: Tue, 05 Mar 2024 19:41:02 GMT  
		Size: 5.3 MB (5270995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cba91d041ae77cf958d8509d23d6f741eec735e9bf9a24d489d0b8842db30c9`  
		Last Modified: Tue, 05 Mar 2024 19:41:01 GMT  
		Size: 1.2 MB (1186176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de13da806adead3ab5a4380c923e80ebddfc28b7b94d6e6f43b6cbb920acd85`  
		Last Modified: Tue, 05 Mar 2024 19:41:01 GMT  
		Size: 407.0 B  
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
$ docker pull caddy@sha256:7a4365fc853bf4ac7b497c662da666883c7471fb89275c320e38fe77949144f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `caddy:2.7-builder-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:63e3bb18f43a20a50a640e33d80c15d6447e5c49eb758ad2ac92dd3c2215e1d9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2177356061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51bf8c2ce948dfc3bc85a84137d8ed09be2f3b755821c887f151431733f69def`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:31:24 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Feb 2024 20:31:24 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Feb 2024 20:31:25 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Feb 2024 20:31:26 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Feb 2024 20:33:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:33:15 GMT
ENV GOPATH=C:\go
# Wed, 14 Feb 2024 20:34:38 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Mar 2024 19:30:18 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 19:33:39 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Mar 2024 19:33:40 GMT
WORKDIR C:\go
# Tue, 05 Mar 2024 20:00:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Mar 2024 20:00:06 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:00:06 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:00:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:03:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 05 Mar 2024 20:03:10 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001ba7ca58e0032ab21885ed5be98699fa0e8693d84ce59492bbdeb45a1f5b89`  
		Last Modified: Wed, 14 Feb 2024 20:57:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964f6547b697b5014d27c4ae5aa9115c1686907b1f2524f8f0de888da7a79bd8`  
		Last Modified: Wed, 14 Feb 2024 20:57:29 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f83e22effb8739ec3fdcae64612cffac4ee7579638549caf47c70342693285`  
		Last Modified: Wed, 14 Feb 2024 20:57:29 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce41b07883cf81f89185e0e1b4fc65b39258a3f1aaff0ce01028854071ddecb`  
		Last Modified: Wed, 14 Feb 2024 20:57:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7954912de33be8cc7e1e4ea36180acfc8bb6cc7b7dc043d43d5912cfd171cd3`  
		Last Modified: Wed, 14 Feb 2024 20:57:33 GMT  
		Size: 25.6 MB (25560320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c63eb439e08d84b2f39090a2a87819fe70e5dfe666f3d4c4d3985acfd1364b0`  
		Last Modified: Wed, 14 Feb 2024 20:57:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fef719b5ba36fc0af1638fb03777e938c25331563e1d178a89bae94d428c8fb`  
		Last Modified: Wed, 14 Feb 2024 20:57:27 GMT  
		Size: 285.4 KB (285394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8d167b3e7ee16cfc662a87231b4084716742686d31d5b82e887b234efec2e9`  
		Last Modified: Tue, 05 Mar 2024 19:42:21 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c28621adc2c564252debe98669a98b5db5ce45172ce843466e26b8b689b114a`  
		Last Modified: Tue, 05 Mar 2024 19:42:40 GMT  
		Size: 69.4 MB (69364712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5c43bdc8404f132a84e8a0f4c69e490b01b908e8633abcfe604de71e205648`  
		Last Modified: Tue, 05 Mar 2024 19:42:21 GMT  
		Size: 1.5 KB (1545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcc239c5226abef94ce51a464e18875c9ff8a1fded12c55a44a3396d065d9a0`  
		Last Modified: Tue, 05 Mar 2024 20:04:31 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92819fb904e989755feedb88fdac313dd0614617cb2124f845e1beb9ef0b7840`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866ca856d15d8b11f3251d0e1e751bce5ccd3d04170d016b81a7e721ee811cff`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478c6e5efb5198c62dae853963d276055bc2ce33ae70aca26cba13a16359a054`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806deb5a287a2c1cfa951ac44704c97b32856f31e9d0012590d79e5b068279f1`  
		Last Modified: Tue, 05 Mar 2024 20:04:30 GMT  
		Size: 1.7 MB (1678307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bb868ab3b0ea5f9e471cb10db42cf456ce7dfe4ecb2ec8769a9c97c105483e`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:9ffd2fc461bcd523f2c67f8692ea85156c40fb2b21e35b457547522153eb44b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `caddy:2.7-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:e924a818b35c77fa77b850501f876fa811c43019e884675210e1232eb23b13a6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2007476156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69198d50697c7c62515331afda3b6b548388fe7ecfbec519f7bcb8e8ab8e5155`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:27:24 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Feb 2024 20:27:25 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Feb 2024 20:27:26 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Feb 2024 20:27:27 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Feb 2024 20:28:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:28:04 GMT
ENV GOPATH=C:\go
# Wed, 14 Feb 2024 20:28:25 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Mar 2024 19:27:34 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 19:29:55 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Mar 2024 19:29:57 GMT
WORKDIR C:\go
# Tue, 05 Mar 2024 20:03:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Mar 2024 20:03:28 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:03:29 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:03:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:03:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 05 Mar 2024 20:03:52 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ac8de2d709384a84400f6f072b2d3d4c4d454ee27f8ec716db4964eabac3f8`  
		Last Modified: Wed, 14 Feb 2024 20:55:46 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70115ee0ce6c09f30645181ec6f80fe9ece4e9b51628fdbaa85ebd4e0ae979e1`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab323644de57af1911793c0a10501a7b21640f8e58484665dc2258f482cb943`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae53fd363daebfb127c2ba7e51543cf93130802d95e194fc71db09c52b9fe10c`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665a9a35030c2076331610dfe4c22866525c2b0ac219981d900f1b6178af5241`  
		Last Modified: Wed, 14 Feb 2024 20:55:50 GMT  
		Size: 25.5 MB (25534020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ab59c20a7391d04f68a3dc2b9d6eb4cfd1e7af0ddd33e30d2cd19f13535c0`  
		Last Modified: Wed, 14 Feb 2024 20:55:43 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a35884f3b4e6aa2080cc34668faeabacc75000ef04e2fe4ec3e76f166d992e4`  
		Last Modified: Wed, 14 Feb 2024 20:55:43 GMT  
		Size: 266.0 KB (265989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c81949701f9fd28f5c42cfa101f1e2c2858efdb4032e3c3a221ae64417094d`  
		Last Modified: Tue, 05 Mar 2024 19:41:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c07bf58a4a94d97d30abeee1c89ea03f4d6bb5ae58ba58a108ab8c14ce86d04`  
		Last Modified: Tue, 05 Mar 2024 19:42:12 GMT  
		Size: 69.4 MB (69350261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff66f61d5b04d89a7cd43a5718c2738ee8c932ff7976238576fcce4a9205188`  
		Last Modified: Tue, 05 Mar 2024 19:41:52 GMT  
		Size: 1.5 KB (1539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fff8f151323c49bef4ab32c69e1b7fb0bc1c38c418bc58f8d552450f83ddb4`  
		Last Modified: Tue, 05 Mar 2024 20:04:48 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad11e6d0d7e8e1cdeb21675479688d12574b1f3aaf78c017dcb3f3f0e461e94`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3bac1fc388577dc02e99cece1f2418b768a6b9131f03ccb3a12b5130d0657c`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2023c4236e1ee6e1e21d75518a4e0b041879053cca3a4d196a736c11ef937885`  
		Last Modified: Tue, 05 Mar 2024 20:04:45 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646022f7531f95a5e75674d8b4716cd2b10acf7080eacbcf1a9146ec3c17a381`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.7 MB (1653517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a594d21bdd61142fc0e9073bca5c902365dcacea37bc8513a5868bccebfd5e5`  
		Last Modified: Tue, 05 Mar 2024 20:04:45 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-windowsservercore`

```console
$ docker pull caddy@sha256:444dc16652b598c3d6f69627e313944c17cb36a0adfc3c366fa738e2ed0e1895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `caddy:2.7-windowsservercore` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:f6e8f7815f3e03bc5d239d52a2bdeb473ff959a4b74bb86ee94b410cc2407c35
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1926683398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d9ff1f8c7723994d4a4f7c520159beedff8fe440b855a9fb6f57afdcae7b2b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:22:32 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:22:33 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:23:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:23:00 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:23:01 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:23:02 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:23:03 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:23:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:23:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:23:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:23:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:23:09 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:23:11 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:23:26 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:23:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ebcfc7e63facc5463d681dd534f084e021cc447cf46213aae377066d573493`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 458.4 KB (458447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bee2047afe4426d5715972f534b35ce0bc5ae241ae42982e37a64185c7a482`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39da07145bbe64c3ec2c032dafa6eb6ddf62130dba67e03a627cc2cb3788f9e2`  
		Last Modified: Wed, 14 Feb 2024 21:26:37 GMT  
		Size: 15.3 MB (15267126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c47f482128a80b23df310b1c1b71bfa176b010cdd91761fb1a9aa71c4812738`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dab75e60136c0cf03ae7e7ad030b7adb3aff8014f4fc0e412d1ce9c217bdd60`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db7f5e1b9057131a3d1e7f1439de34f87684add5ac177612296925ed37b654d`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ac08dfbec3219d30d64f54cc8e1b46009cf4327d55c288ca43d875eaff3763`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4fad3dd8e3739d27a2d3793ae4740b4cbf52999f2295ad370545f048730492`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91f700224a04849cd48e2ab6525d47b7188051110718ca045ca50452ce26cb3`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fe7f9176dbfd4a89d170a117169a90cd5f49a2c5b7a55ac4026288812b8b60`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4fc40cf63828021df321258238a85d39918d2749a117bb0538bda0afce3aef`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9621f5d2e06bf68f778ba42ec6ec5d4a80d1cfb1204ea19b5a2b42d2b1d87d`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398c5b0cde2fcd40c8ce079d93fd115bd8ee7d8028cabc4baf9ecc07ab226410`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60cb86bd52f82372e11b1b851709ccb6c10537dc9262f63ef8bcd0152efb235`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c35a9695bf632732db6dd52a7531c75c5243819b2b8d7c019a1e8fc796e13c7`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c98226f721bed207883df26f4d35276821dd38299a62458d2ba6c55fab5b0d`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b23541f7ccf5a2debb904fdc41eccc03284d7fbf3baff61798b726d7c9ba12`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ce3a452fdfcd413ac385a157633a0fe389a8c2fdb281ce79b5cdd4d16dcb9b`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 281.4 KB (281363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7be2379ebd2e4d0fca0bbf81dd2628e93d8efd2ef3ea28c3872855ca6e50ed`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:793d5d17edca1d44e963efc2d79f97a389420f253790a04d54f9388492ca70ff
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2096464983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2636f0474ebff3dfb86f6d92e45af2173f0773887039f3e30776eb3b2de1bd0c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:18:41 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:18:42 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:20:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:20:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:20:23 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:20:24 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:20:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:20:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:20:31 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:20:33 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:20:34 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:20:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:20:36 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:20:36 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:20:37 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:20:38 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:20:40 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:21:47 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:21:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936f6b22f9979fac96518b60eadd4d9156939b025d673ce61a2e6a18553dc2b1`  
		Last Modified: Wed, 14 Feb 2024 21:26:08 GMT  
		Size: 461.6 KB (461622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72873b058a9927d9ea1e4a234006a54fec29d1da3beb3f2834ce66fda6f4262f`  
		Last Modified: Wed, 14 Feb 2024 21:26:07 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc3d79323d38d65e8112fca8b77ad54434883a9104dd542fdc179cf782fab1e`  
		Last Modified: Wed, 14 Feb 2024 21:26:10 GMT  
		Size: 15.3 MB (15274562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4873aaa427e9ae13aeebcc096c23b92dd4d61d1f6b601a755dfaf268c4b85ab6`  
		Last Modified: Wed, 14 Feb 2024 21:26:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c57d3fae417c15ca2cf9d965bd8d05bab080154e20cd2e20f5d71aa86de5c0f`  
		Last Modified: Wed, 14 Feb 2024 21:26:06 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444c12e07ce56e352f094a12c03aa1ab4110c79d5daa78eea733580703bdef6a`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cf5cd505e0ce461fb00191ec16014104c1f3f38c373b2179b9cb0ecec44082`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f67f42fce82938d220cec3933239aedeffe9da096d14f3354eb2ffd49902c8`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb581bc05a23526a9b12256e17b6963201710bb71ae435fed4ccbdc69330fe8`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806d41685663d3f82e404087dda88f57f3f2534966be1a73998da0d9d3f15ae8`  
		Last Modified: Wed, 14 Feb 2024 21:26:04 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af65ac33d93c108086650ad059ffe57d44fcae5dfcfd80f331aeb3acb759145`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1d5135587234fcaf02c388f1fbf2e4a7be50b81f4c5296aeb7a99cb5fc2d13`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705d9a64f11bac49a31ef3cb6bfd926024e700d3daf666b277867cddcef7fcff`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac09729a4577f5fe6afe0d3a00560ec715f86b1e907e28917ca6d13dcafb3e7`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cd769674ca72532329328651bf168fe61494249405bb59e89832d94410289b`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a7dedf94b664393c8ae954445d5b582ffe6d8ffc604ddaaae79b20de72317`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a465dd935213cb9e1bd4aae1e392fd32e5fcb661c6bf3b7a50e113ea7077d7`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d18f93e3aab637778f45296a721f0857d0c5ec759335b634ae323255bbb0c29`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 257.6 KB (257571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11c0d021a3877f354347717399af0fe31b30ddd220f2b64b4ccf68fe7b6140b`  
		Last Modified: Wed, 14 Feb 2024 21:26:02 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-windowsservercore-1809`

```console
$ docker pull caddy@sha256:fa377f42fcef67994cd1ff2eca1715f8ddbb6836a84cc7a6b796df01353d6f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `caddy:2.7-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:793d5d17edca1d44e963efc2d79f97a389420f253790a04d54f9388492ca70ff
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2096464983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2636f0474ebff3dfb86f6d92e45af2173f0773887039f3e30776eb3b2de1bd0c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:18:41 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:18:42 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:20:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:20:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:20:23 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:20:24 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:20:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:20:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:20:31 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:20:33 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:20:34 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:20:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:20:36 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:20:36 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:20:37 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:20:38 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:20:40 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:21:47 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:21:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936f6b22f9979fac96518b60eadd4d9156939b025d673ce61a2e6a18553dc2b1`  
		Last Modified: Wed, 14 Feb 2024 21:26:08 GMT  
		Size: 461.6 KB (461622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72873b058a9927d9ea1e4a234006a54fec29d1da3beb3f2834ce66fda6f4262f`  
		Last Modified: Wed, 14 Feb 2024 21:26:07 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc3d79323d38d65e8112fca8b77ad54434883a9104dd542fdc179cf782fab1e`  
		Last Modified: Wed, 14 Feb 2024 21:26:10 GMT  
		Size: 15.3 MB (15274562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4873aaa427e9ae13aeebcc096c23b92dd4d61d1f6b601a755dfaf268c4b85ab6`  
		Last Modified: Wed, 14 Feb 2024 21:26:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c57d3fae417c15ca2cf9d965bd8d05bab080154e20cd2e20f5d71aa86de5c0f`  
		Last Modified: Wed, 14 Feb 2024 21:26:06 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444c12e07ce56e352f094a12c03aa1ab4110c79d5daa78eea733580703bdef6a`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cf5cd505e0ce461fb00191ec16014104c1f3f38c373b2179b9cb0ecec44082`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f67f42fce82938d220cec3933239aedeffe9da096d14f3354eb2ffd49902c8`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb581bc05a23526a9b12256e17b6963201710bb71ae435fed4ccbdc69330fe8`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806d41685663d3f82e404087dda88f57f3f2534966be1a73998da0d9d3f15ae8`  
		Last Modified: Wed, 14 Feb 2024 21:26:04 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af65ac33d93c108086650ad059ffe57d44fcae5dfcfd80f331aeb3acb759145`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1d5135587234fcaf02c388f1fbf2e4a7be50b81f4c5296aeb7a99cb5fc2d13`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705d9a64f11bac49a31ef3cb6bfd926024e700d3daf666b277867cddcef7fcff`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac09729a4577f5fe6afe0d3a00560ec715f86b1e907e28917ca6d13dcafb3e7`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cd769674ca72532329328651bf168fe61494249405bb59e89832d94410289b`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a7dedf94b664393c8ae954445d5b582ffe6d8ffc604ddaaae79b20de72317`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a465dd935213cb9e1bd4aae1e392fd32e5fcb661c6bf3b7a50e113ea7077d7`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d18f93e3aab637778f45296a721f0857d0c5ec759335b634ae323255bbb0c29`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 257.6 KB (257571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11c0d021a3877f354347717399af0fe31b30ddd220f2b64b4ccf68fe7b6140b`  
		Last Modified: Wed, 14 Feb 2024 21:26:02 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:6e915ccce3def5db60e3af13d28e398bfdbde6a3298781b0cf53cbb174b0f23e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `caddy:2.7-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:f6e8f7815f3e03bc5d239d52a2bdeb473ff959a4b74bb86ee94b410cc2407c35
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1926683398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d9ff1f8c7723994d4a4f7c520159beedff8fe440b855a9fb6f57afdcae7b2b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:22:32 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:22:33 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:23:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:23:00 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:23:01 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:23:02 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:23:03 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:23:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:23:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:23:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:23:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:23:09 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:23:11 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:23:26 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:23:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ebcfc7e63facc5463d681dd534f084e021cc447cf46213aae377066d573493`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 458.4 KB (458447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bee2047afe4426d5715972f534b35ce0bc5ae241ae42982e37a64185c7a482`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39da07145bbe64c3ec2c032dafa6eb6ddf62130dba67e03a627cc2cb3788f9e2`  
		Last Modified: Wed, 14 Feb 2024 21:26:37 GMT  
		Size: 15.3 MB (15267126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c47f482128a80b23df310b1c1b71bfa176b010cdd91761fb1a9aa71c4812738`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dab75e60136c0cf03ae7e7ad030b7adb3aff8014f4fc0e412d1ce9c217bdd60`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db7f5e1b9057131a3d1e7f1439de34f87684add5ac177612296925ed37b654d`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ac08dfbec3219d30d64f54cc8e1b46009cf4327d55c288ca43d875eaff3763`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4fad3dd8e3739d27a2d3793ae4740b4cbf52999f2295ad370545f048730492`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91f700224a04849cd48e2ab6525d47b7188051110718ca045ca50452ce26cb3`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fe7f9176dbfd4a89d170a117169a90cd5f49a2c5b7a55ac4026288812b8b60`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4fc40cf63828021df321258238a85d39918d2749a117bb0538bda0afce3aef`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9621f5d2e06bf68f778ba42ec6ec5d4a80d1cfb1204ea19b5a2b42d2b1d87d`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398c5b0cde2fcd40c8ce079d93fd115bd8ee7d8028cabc4baf9ecc07ab226410`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60cb86bd52f82372e11b1b851709ccb6c10537dc9262f63ef8bcd0152efb235`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c35a9695bf632732db6dd52a7531c75c5243819b2b8d7c019a1e8fc796e13c7`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c98226f721bed207883df26f4d35276821dd38299a62458d2ba6c55fab5b0d`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b23541f7ccf5a2debb904fdc41eccc03284d7fbf3baff61798b726d7c9ba12`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ce3a452fdfcd413ac385a157633a0fe389a8c2fdb281ce79b5cdd4d16dcb9b`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 281.4 KB (281363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7be2379ebd2e4d0fca0bbf81dd2628e93d8efd2ef3ea28c3872855ca6e50ed`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6`

```console
$ docker pull caddy@sha256:2a0d069ea95d91641d201943a5a049e83cbfade8039670aebfb441b132189de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

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

### `caddy:2.7.6` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:f6e8f7815f3e03bc5d239d52a2bdeb473ff959a4b74bb86ee94b410cc2407c35
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1926683398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d9ff1f8c7723994d4a4f7c520159beedff8fe440b855a9fb6f57afdcae7b2b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:22:32 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:22:33 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:23:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:23:00 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:23:01 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:23:02 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:23:03 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:23:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:23:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:23:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:23:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:23:09 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:23:11 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:23:26 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:23:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ebcfc7e63facc5463d681dd534f084e021cc447cf46213aae377066d573493`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 458.4 KB (458447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bee2047afe4426d5715972f534b35ce0bc5ae241ae42982e37a64185c7a482`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39da07145bbe64c3ec2c032dafa6eb6ddf62130dba67e03a627cc2cb3788f9e2`  
		Last Modified: Wed, 14 Feb 2024 21:26:37 GMT  
		Size: 15.3 MB (15267126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c47f482128a80b23df310b1c1b71bfa176b010cdd91761fb1a9aa71c4812738`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dab75e60136c0cf03ae7e7ad030b7adb3aff8014f4fc0e412d1ce9c217bdd60`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db7f5e1b9057131a3d1e7f1439de34f87684add5ac177612296925ed37b654d`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ac08dfbec3219d30d64f54cc8e1b46009cf4327d55c288ca43d875eaff3763`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4fad3dd8e3739d27a2d3793ae4740b4cbf52999f2295ad370545f048730492`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91f700224a04849cd48e2ab6525d47b7188051110718ca045ca50452ce26cb3`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fe7f9176dbfd4a89d170a117169a90cd5f49a2c5b7a55ac4026288812b8b60`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4fc40cf63828021df321258238a85d39918d2749a117bb0538bda0afce3aef`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9621f5d2e06bf68f778ba42ec6ec5d4a80d1cfb1204ea19b5a2b42d2b1d87d`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398c5b0cde2fcd40c8ce079d93fd115bd8ee7d8028cabc4baf9ecc07ab226410`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60cb86bd52f82372e11b1b851709ccb6c10537dc9262f63ef8bcd0152efb235`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c35a9695bf632732db6dd52a7531c75c5243819b2b8d7c019a1e8fc796e13c7`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c98226f721bed207883df26f4d35276821dd38299a62458d2ba6c55fab5b0d`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b23541f7ccf5a2debb904fdc41eccc03284d7fbf3baff61798b726d7c9ba12`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ce3a452fdfcd413ac385a157633a0fe389a8c2fdb281ce79b5cdd4d16dcb9b`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 281.4 KB (281363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7be2379ebd2e4d0fca0bbf81dd2628e93d8efd2ef3ea28c3872855ca6e50ed`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:793d5d17edca1d44e963efc2d79f97a389420f253790a04d54f9388492ca70ff
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2096464983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2636f0474ebff3dfb86f6d92e45af2173f0773887039f3e30776eb3b2de1bd0c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:18:41 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:18:42 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:20:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:20:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:20:23 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:20:24 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:20:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:20:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:20:31 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:20:33 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:20:34 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:20:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:20:36 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:20:36 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:20:37 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:20:38 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:20:40 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:21:47 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:21:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936f6b22f9979fac96518b60eadd4d9156939b025d673ce61a2e6a18553dc2b1`  
		Last Modified: Wed, 14 Feb 2024 21:26:08 GMT  
		Size: 461.6 KB (461622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72873b058a9927d9ea1e4a234006a54fec29d1da3beb3f2834ce66fda6f4262f`  
		Last Modified: Wed, 14 Feb 2024 21:26:07 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc3d79323d38d65e8112fca8b77ad54434883a9104dd542fdc179cf782fab1e`  
		Last Modified: Wed, 14 Feb 2024 21:26:10 GMT  
		Size: 15.3 MB (15274562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4873aaa427e9ae13aeebcc096c23b92dd4d61d1f6b601a755dfaf268c4b85ab6`  
		Last Modified: Wed, 14 Feb 2024 21:26:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c57d3fae417c15ca2cf9d965bd8d05bab080154e20cd2e20f5d71aa86de5c0f`  
		Last Modified: Wed, 14 Feb 2024 21:26:06 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444c12e07ce56e352f094a12c03aa1ab4110c79d5daa78eea733580703bdef6a`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cf5cd505e0ce461fb00191ec16014104c1f3f38c373b2179b9cb0ecec44082`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f67f42fce82938d220cec3933239aedeffe9da096d14f3354eb2ffd49902c8`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb581bc05a23526a9b12256e17b6963201710bb71ae435fed4ccbdc69330fe8`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806d41685663d3f82e404087dda88f57f3f2534966be1a73998da0d9d3f15ae8`  
		Last Modified: Wed, 14 Feb 2024 21:26:04 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af65ac33d93c108086650ad059ffe57d44fcae5dfcfd80f331aeb3acb759145`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1d5135587234fcaf02c388f1fbf2e4a7be50b81f4c5296aeb7a99cb5fc2d13`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705d9a64f11bac49a31ef3cb6bfd926024e700d3daf666b277867cddcef7fcff`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac09729a4577f5fe6afe0d3a00560ec715f86b1e907e28917ca6d13dcafb3e7`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cd769674ca72532329328651bf168fe61494249405bb59e89832d94410289b`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a7dedf94b664393c8ae954445d5b582ffe6d8ffc604ddaaae79b20de72317`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a465dd935213cb9e1bd4aae1e392fd32e5fcb661c6bf3b7a50e113ea7077d7`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d18f93e3aab637778f45296a721f0857d0c5ec759335b634ae323255bbb0c29`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 257.6 KB (257571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11c0d021a3877f354347717399af0fe31b30ddd220f2b64b4ccf68fe7b6140b`  
		Last Modified: Wed, 14 Feb 2024 21:26:02 GMT  
		Size: 1.3 KB (1333 bytes)  
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
$ docker pull caddy@sha256:7954f9183f22718dfac36955b6cb281466256ae195f30ffcd0229596e2badc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `caddy:2.7.6-builder` - linux; amd64

```console
$ docker pull caddy@sha256:683161d33599ee7740b25d8c0466e82bfd94e491c63bef744eda38919853dd62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76973779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e7c249761d733da653482a2b5259eaae803dee4354bc3562e48a601315e6ff`
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
# Tue, 05 Mar 2024 19:42:13 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 19:42:13 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 19:42:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 19:42:15 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 19:42:15 GMT
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
	-	`sha256:ddc853d0ab24d3fe195e8492db2866ec9d01681c218bdff73afb081fa97cb002`  
		Last Modified: Tue, 05 Mar 2024 19:42:32 GMT  
		Size: 5.0 MB (4972975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea68e3f24bc6efb27b70b8c1870bf11b4a5fad53eb40e8ce77817c21586972d`  
		Last Modified: Tue, 05 Mar 2024 19:42:31 GMT  
		Size: 1.3 MB (1302236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ecce85dc39a9d244f2c3b1e0e89e72279e6d9f6b154afad2171642b11c137b`  
		Last Modified: Tue, 05 Mar 2024 19:42:31 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ece7f11958f255486a5be355c9180900873b391449f4258706b535d5177b40b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75407413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22234bb36f9348628e9caea0dac041e47e0df57676643cb27bc893380168cbd`
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
# Tue, 05 Mar 2024 23:00:43 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 23:00:43 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 23:00:44 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 23:00:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 23:00:44 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 23:00:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 23:00:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 23:00:49 GMT
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
	-	`sha256:bccd7f5c5a4f0abc0a23393d9a04f353b767b809c6ac950caaa731dd3768c8eb`  
		Last Modified: Tue, 05 Mar 2024 20:11:40 GMT  
		Size: 65.8 MB (65767479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33a4721f193119280f7dfc5baed0ce6a2d3b2eb94e31901d986ea54166c41ea`  
		Last Modified: Tue, 05 Mar 2024 20:11:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28b5e7a7f3d8467fb26f35d8b70ae0853d39fb4103058a0dc47dd62be3256d7`  
		Last Modified: Tue, 05 Mar 2024 23:01:07 GMT  
		Size: 5.0 MB (4958742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276c5f8fd9c641c6036e92487a700ea1b6cc811b8ac1578ff0f94803223f6e0d`  
		Last Modified: Tue, 05 Mar 2024 23:01:07 GMT  
		Size: 1.2 MB (1248648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db777cbc747c60df3dc9c90c42c55125b12f7c65e05a6b1ab52ec8de565848a9`  
		Last Modified: Tue, 05 Mar 2024 23:01:06 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:156f7188ad9f04c359241e42567a3cee24477cb1885639d634da45c042cc297e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2a4fac0ed075caa114df1d0fd560d017af28251032ec5015a49c0702fe3d48`
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
# Tue, 05 Mar 2024 20:48:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:48:44 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:48:45 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:48:45 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:48:45 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:48:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:48:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:48:48 GMT
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
	-	`sha256:17f0c2683a0605dfb4fff92a0c34044c42624cbc47515f2262026e23ffa28b15`  
		Last Modified: Tue, 05 Mar 2024 20:01:25 GMT  
		Size: 65.8 MB (65767445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1570cef4f4f43311a29ff4036cc73329f8fe806fb19c51f3413b3073bfc70634`  
		Last Modified: Tue, 05 Mar 2024 20:01:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2640aa4bbda58460e9e4fd9b0a0969303c9a30ba9b9ff6424d9349f7c0ffbcd`  
		Last Modified: Tue, 05 Mar 2024 20:49:09 GMT  
		Size: 4.5 MB (4514657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5f06f998d08d9a0ca561581720f1399d9e1c6f64b4637370acd8eddc90418e`  
		Last Modified: Tue, 05 Mar 2024 20:49:08 GMT  
		Size: 1.2 MB (1246081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f58b57eb0adfeabad656db0f59a85f8373054397123d068fe68452663713a9f`  
		Last Modified: Tue, 05 Mar 2024 20:49:08 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:b7d23a0e6f86ad993855c69a14f149837072ce99399627ee74d95e4705784d14
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73993792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0728d6faf4e6faebb8c082c95826cc671a39f43e1cd9ef0cfcd909a42435c9bd`
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
# Tue, 05 Mar 2024 20:00:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:00:21 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:00:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:00:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:00:23 GMT
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
	-	`sha256:5a91045fa00056cff12698db93bed8fe188f9895b74e96e29b6a9f6a6e047937`  
		Last Modified: Tue, 05 Mar 2024 19:44:44 GMT  
		Size: 64.1 MB (64111148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f155e563ada2bb78e99decac187a48adcf9db3cd56e543bc0694674ef8a234`  
		Last Modified: Tue, 05 Mar 2024 19:44:35 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f627d8e1519d50a70f854d0342a035bd62a8cedf0d7a61351f7ac191accf21`  
		Last Modified: Tue, 05 Mar 2024 20:00:40 GMT  
		Size: 5.1 MB (5063926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cf96a60cd43a372ff273debacac6160f6842de4adc5e79eef190c8a791eecc`  
		Last Modified: Tue, 05 Mar 2024 20:00:39 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113a17d73127a40aa417b169724fea00b3b34ed479e7d3fb2b656325c7d131a8`  
		Last Modified: Tue, 05 Mar 2024 20:00:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:3321233002d79314df5692f81246bbcc2d0c9ba268c61792fd6269b1e64e6ff9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74219843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b9b8fd2c1e8bd5b65bfbd17b919aabf00faf29ce73a1702c8a2610afe5427c`
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
# Tue, 05 Mar 2024 19:40:39 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 19:40:40 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 19:40:40 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 19:40:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 19:40:41 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 19:40:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 19:40:44 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 19:40:44 GMT
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
	-	`sha256:1e1323fc82438c3a0b40c7bcf18c7b4808edcec55b91135df534741787df9cbc`  
		Last Modified: Tue, 05 Mar 2024 19:25:03 GMT  
		Size: 64.1 MB (64126907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8630ef56928609490ea4cc1460f549f49e84ed6ff4f6bb7ffb5c3fa5e53f3027`  
		Last Modified: Tue, 05 Mar 2024 19:24:51 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c2f5a4fa35cf481005994eef4a926ba3b1cecb6ee2747d8080460c88a7fa6c`  
		Last Modified: Tue, 05 Mar 2024 19:41:02 GMT  
		Size: 5.3 MB (5270995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cba91d041ae77cf958d8509d23d6f741eec735e9bf9a24d489d0b8842db30c9`  
		Last Modified: Tue, 05 Mar 2024 19:41:01 GMT  
		Size: 1.2 MB (1186176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de13da806adead3ab5a4380c923e80ebddfc28b7b94d6e6f43b6cbb920acd85`  
		Last Modified: Tue, 05 Mar 2024 19:41:01 GMT  
		Size: 407.0 B  
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

### `caddy:2.7.6-builder` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:e924a818b35c77fa77b850501f876fa811c43019e884675210e1232eb23b13a6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2007476156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69198d50697c7c62515331afda3b6b548388fe7ecfbec519f7bcb8e8ab8e5155`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:27:24 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Feb 2024 20:27:25 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Feb 2024 20:27:26 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Feb 2024 20:27:27 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Feb 2024 20:28:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:28:04 GMT
ENV GOPATH=C:\go
# Wed, 14 Feb 2024 20:28:25 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Mar 2024 19:27:34 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 19:29:55 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Mar 2024 19:29:57 GMT
WORKDIR C:\go
# Tue, 05 Mar 2024 20:03:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Mar 2024 20:03:28 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:03:29 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:03:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:03:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 05 Mar 2024 20:03:52 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ac8de2d709384a84400f6f072b2d3d4c4d454ee27f8ec716db4964eabac3f8`  
		Last Modified: Wed, 14 Feb 2024 20:55:46 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70115ee0ce6c09f30645181ec6f80fe9ece4e9b51628fdbaa85ebd4e0ae979e1`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab323644de57af1911793c0a10501a7b21640f8e58484665dc2258f482cb943`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae53fd363daebfb127c2ba7e51543cf93130802d95e194fc71db09c52b9fe10c`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665a9a35030c2076331610dfe4c22866525c2b0ac219981d900f1b6178af5241`  
		Last Modified: Wed, 14 Feb 2024 20:55:50 GMT  
		Size: 25.5 MB (25534020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ab59c20a7391d04f68a3dc2b9d6eb4cfd1e7af0ddd33e30d2cd19f13535c0`  
		Last Modified: Wed, 14 Feb 2024 20:55:43 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a35884f3b4e6aa2080cc34668faeabacc75000ef04e2fe4ec3e76f166d992e4`  
		Last Modified: Wed, 14 Feb 2024 20:55:43 GMT  
		Size: 266.0 KB (265989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c81949701f9fd28f5c42cfa101f1e2c2858efdb4032e3c3a221ae64417094d`  
		Last Modified: Tue, 05 Mar 2024 19:41:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c07bf58a4a94d97d30abeee1c89ea03f4d6bb5ae58ba58a108ab8c14ce86d04`  
		Last Modified: Tue, 05 Mar 2024 19:42:12 GMT  
		Size: 69.4 MB (69350261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff66f61d5b04d89a7cd43a5718c2738ee8c932ff7976238576fcce4a9205188`  
		Last Modified: Tue, 05 Mar 2024 19:41:52 GMT  
		Size: 1.5 KB (1539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fff8f151323c49bef4ab32c69e1b7fb0bc1c38c418bc58f8d552450f83ddb4`  
		Last Modified: Tue, 05 Mar 2024 20:04:48 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad11e6d0d7e8e1cdeb21675479688d12574b1f3aaf78c017dcb3f3f0e461e94`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3bac1fc388577dc02e99cece1f2418b768a6b9131f03ccb3a12b5130d0657c`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2023c4236e1ee6e1e21d75518a4e0b041879053cca3a4d196a736c11ef937885`  
		Last Modified: Tue, 05 Mar 2024 20:04:45 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646022f7531f95a5e75674d8b4716cd2b10acf7080eacbcf1a9146ec3c17a381`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.7 MB (1653517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a594d21bdd61142fc0e9073bca5c902365dcacea37bc8513a5868bccebfd5e5`  
		Last Modified: Tue, 05 Mar 2024 20:04:45 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:63e3bb18f43a20a50a640e33d80c15d6447e5c49eb758ad2ac92dd3c2215e1d9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2177356061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51bf8c2ce948dfc3bc85a84137d8ed09be2f3b755821c887f151431733f69def`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:31:24 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Feb 2024 20:31:24 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Feb 2024 20:31:25 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Feb 2024 20:31:26 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Feb 2024 20:33:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:33:15 GMT
ENV GOPATH=C:\go
# Wed, 14 Feb 2024 20:34:38 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Mar 2024 19:30:18 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 19:33:39 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Mar 2024 19:33:40 GMT
WORKDIR C:\go
# Tue, 05 Mar 2024 20:00:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Mar 2024 20:00:06 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:00:06 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:00:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:03:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 05 Mar 2024 20:03:10 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001ba7ca58e0032ab21885ed5be98699fa0e8693d84ce59492bbdeb45a1f5b89`  
		Last Modified: Wed, 14 Feb 2024 20:57:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964f6547b697b5014d27c4ae5aa9115c1686907b1f2524f8f0de888da7a79bd8`  
		Last Modified: Wed, 14 Feb 2024 20:57:29 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f83e22effb8739ec3fdcae64612cffac4ee7579638549caf47c70342693285`  
		Last Modified: Wed, 14 Feb 2024 20:57:29 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce41b07883cf81f89185e0e1b4fc65b39258a3f1aaff0ce01028854071ddecb`  
		Last Modified: Wed, 14 Feb 2024 20:57:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7954912de33be8cc7e1e4ea36180acfc8bb6cc7b7dc043d43d5912cfd171cd3`  
		Last Modified: Wed, 14 Feb 2024 20:57:33 GMT  
		Size: 25.6 MB (25560320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c63eb439e08d84b2f39090a2a87819fe70e5dfe666f3d4c4d3985acfd1364b0`  
		Last Modified: Wed, 14 Feb 2024 20:57:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fef719b5ba36fc0af1638fb03777e938c25331563e1d178a89bae94d428c8fb`  
		Last Modified: Wed, 14 Feb 2024 20:57:27 GMT  
		Size: 285.4 KB (285394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8d167b3e7ee16cfc662a87231b4084716742686d31d5b82e887b234efec2e9`  
		Last Modified: Tue, 05 Mar 2024 19:42:21 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c28621adc2c564252debe98669a98b5db5ce45172ce843466e26b8b689b114a`  
		Last Modified: Tue, 05 Mar 2024 19:42:40 GMT  
		Size: 69.4 MB (69364712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5c43bdc8404f132a84e8a0f4c69e490b01b908e8633abcfe604de71e205648`  
		Last Modified: Tue, 05 Mar 2024 19:42:21 GMT  
		Size: 1.5 KB (1545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcc239c5226abef94ce51a464e18875c9ff8a1fded12c55a44a3396d065d9a0`  
		Last Modified: Tue, 05 Mar 2024 20:04:31 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92819fb904e989755feedb88fdac313dd0614617cb2124f845e1beb9ef0b7840`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866ca856d15d8b11f3251d0e1e751bce5ccd3d04170d016b81a7e721ee811cff`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478c6e5efb5198c62dae853963d276055bc2ce33ae70aca26cba13a16359a054`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806deb5a287a2c1cfa951ac44704c97b32856f31e9d0012590d79e5b068279f1`  
		Last Modified: Tue, 05 Mar 2024 20:04:30 GMT  
		Size: 1.7 MB (1678307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bb868ab3b0ea5f9e471cb10db42cf456ce7dfe4ecb2ec8769a9c97c105483e`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder-alpine`

```console
$ docker pull caddy@sha256:efedb356080be1cd5584baa80df964cbe3d85af049bbfee7775d9659e1809360
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
$ docker pull caddy@sha256:683161d33599ee7740b25d8c0466e82bfd94e491c63bef744eda38919853dd62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76973779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e7c249761d733da653482a2b5259eaae803dee4354bc3562e48a601315e6ff`
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
# Tue, 05 Mar 2024 19:42:13 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 19:42:13 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 19:42:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 19:42:15 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 19:42:15 GMT
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
	-	`sha256:ddc853d0ab24d3fe195e8492db2866ec9d01681c218bdff73afb081fa97cb002`  
		Last Modified: Tue, 05 Mar 2024 19:42:32 GMT  
		Size: 5.0 MB (4972975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea68e3f24bc6efb27b70b8c1870bf11b4a5fad53eb40e8ce77817c21586972d`  
		Last Modified: Tue, 05 Mar 2024 19:42:31 GMT  
		Size: 1.3 MB (1302236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ecce85dc39a9d244f2c3b1e0e89e72279e6d9f6b154afad2171642b11c137b`  
		Last Modified: Tue, 05 Mar 2024 19:42:31 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ece7f11958f255486a5be355c9180900873b391449f4258706b535d5177b40b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75407413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22234bb36f9348628e9caea0dac041e47e0df57676643cb27bc893380168cbd`
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
# Tue, 05 Mar 2024 23:00:43 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 23:00:43 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 23:00:44 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 23:00:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 23:00:44 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 23:00:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 23:00:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 23:00:49 GMT
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
	-	`sha256:bccd7f5c5a4f0abc0a23393d9a04f353b767b809c6ac950caaa731dd3768c8eb`  
		Last Modified: Tue, 05 Mar 2024 20:11:40 GMT  
		Size: 65.8 MB (65767479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33a4721f193119280f7dfc5baed0ce6a2d3b2eb94e31901d986ea54166c41ea`  
		Last Modified: Tue, 05 Mar 2024 20:11:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28b5e7a7f3d8467fb26f35d8b70ae0853d39fb4103058a0dc47dd62be3256d7`  
		Last Modified: Tue, 05 Mar 2024 23:01:07 GMT  
		Size: 5.0 MB (4958742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276c5f8fd9c641c6036e92487a700ea1b6cc811b8ac1578ff0f94803223f6e0d`  
		Last Modified: Tue, 05 Mar 2024 23:01:07 GMT  
		Size: 1.2 MB (1248648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db777cbc747c60df3dc9c90c42c55125b12f7c65e05a6b1ab52ec8de565848a9`  
		Last Modified: Tue, 05 Mar 2024 23:01:06 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:156f7188ad9f04c359241e42567a3cee24477cb1885639d634da45c042cc297e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2a4fac0ed075caa114df1d0fd560d017af28251032ec5015a49c0702fe3d48`
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
# Tue, 05 Mar 2024 20:48:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:48:44 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:48:45 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:48:45 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:48:45 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:48:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:48:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:48:48 GMT
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
	-	`sha256:17f0c2683a0605dfb4fff92a0c34044c42624cbc47515f2262026e23ffa28b15`  
		Last Modified: Tue, 05 Mar 2024 20:01:25 GMT  
		Size: 65.8 MB (65767445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1570cef4f4f43311a29ff4036cc73329f8fe806fb19c51f3413b3073bfc70634`  
		Last Modified: Tue, 05 Mar 2024 20:01:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2640aa4bbda58460e9e4fd9b0a0969303c9a30ba9b9ff6424d9349f7c0ffbcd`  
		Last Modified: Tue, 05 Mar 2024 20:49:09 GMT  
		Size: 4.5 MB (4514657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5f06f998d08d9a0ca561581720f1399d9e1c6f64b4637370acd8eddc90418e`  
		Last Modified: Tue, 05 Mar 2024 20:49:08 GMT  
		Size: 1.2 MB (1246081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f58b57eb0adfeabad656db0f59a85f8373054397123d068fe68452663713a9f`  
		Last Modified: Tue, 05 Mar 2024 20:49:08 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:b7d23a0e6f86ad993855c69a14f149837072ce99399627ee74d95e4705784d14
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73993792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0728d6faf4e6faebb8c082c95826cc671a39f43e1cd9ef0cfcd909a42435c9bd`
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
# Tue, 05 Mar 2024 20:00:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:00:21 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:00:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:00:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:00:23 GMT
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
	-	`sha256:5a91045fa00056cff12698db93bed8fe188f9895b74e96e29b6a9f6a6e047937`  
		Last Modified: Tue, 05 Mar 2024 19:44:44 GMT  
		Size: 64.1 MB (64111148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f155e563ada2bb78e99decac187a48adcf9db3cd56e543bc0694674ef8a234`  
		Last Modified: Tue, 05 Mar 2024 19:44:35 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f627d8e1519d50a70f854d0342a035bd62a8cedf0d7a61351f7ac191accf21`  
		Last Modified: Tue, 05 Mar 2024 20:00:40 GMT  
		Size: 5.1 MB (5063926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cf96a60cd43a372ff273debacac6160f6842de4adc5e79eef190c8a791eecc`  
		Last Modified: Tue, 05 Mar 2024 20:00:39 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113a17d73127a40aa417b169724fea00b3b34ed479e7d3fb2b656325c7d131a8`  
		Last Modified: Tue, 05 Mar 2024 20:00:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:3321233002d79314df5692f81246bbcc2d0c9ba268c61792fd6269b1e64e6ff9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74219843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b9b8fd2c1e8bd5b65bfbd17b919aabf00faf29ce73a1702c8a2610afe5427c`
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
# Tue, 05 Mar 2024 19:40:39 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 19:40:40 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 19:40:40 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 19:40:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 19:40:41 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 19:40:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 19:40:44 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 19:40:44 GMT
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
	-	`sha256:1e1323fc82438c3a0b40c7bcf18c7b4808edcec55b91135df534741787df9cbc`  
		Last Modified: Tue, 05 Mar 2024 19:25:03 GMT  
		Size: 64.1 MB (64126907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8630ef56928609490ea4cc1460f549f49e84ed6ff4f6bb7ffb5c3fa5e53f3027`  
		Last Modified: Tue, 05 Mar 2024 19:24:51 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c2f5a4fa35cf481005994eef4a926ba3b1cecb6ee2747d8080460c88a7fa6c`  
		Last Modified: Tue, 05 Mar 2024 19:41:02 GMT  
		Size: 5.3 MB (5270995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cba91d041ae77cf958d8509d23d6f741eec735e9bf9a24d489d0b8842db30c9`  
		Last Modified: Tue, 05 Mar 2024 19:41:01 GMT  
		Size: 1.2 MB (1186176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de13da806adead3ab5a4380c923e80ebddfc28b7b94d6e6f43b6cbb920acd85`  
		Last Modified: Tue, 05 Mar 2024 19:41:01 GMT  
		Size: 407.0 B  
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
$ docker pull caddy@sha256:7a4365fc853bf4ac7b497c662da666883c7471fb89275c320e38fe77949144f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `caddy:2.7.6-builder-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:63e3bb18f43a20a50a640e33d80c15d6447e5c49eb758ad2ac92dd3c2215e1d9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2177356061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51bf8c2ce948dfc3bc85a84137d8ed09be2f3b755821c887f151431733f69def`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:31:24 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Feb 2024 20:31:24 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Feb 2024 20:31:25 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Feb 2024 20:31:26 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Feb 2024 20:33:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:33:15 GMT
ENV GOPATH=C:\go
# Wed, 14 Feb 2024 20:34:38 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Mar 2024 19:30:18 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 19:33:39 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Mar 2024 19:33:40 GMT
WORKDIR C:\go
# Tue, 05 Mar 2024 20:00:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Mar 2024 20:00:06 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:00:06 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:00:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:03:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 05 Mar 2024 20:03:10 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001ba7ca58e0032ab21885ed5be98699fa0e8693d84ce59492bbdeb45a1f5b89`  
		Last Modified: Wed, 14 Feb 2024 20:57:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964f6547b697b5014d27c4ae5aa9115c1686907b1f2524f8f0de888da7a79bd8`  
		Last Modified: Wed, 14 Feb 2024 20:57:29 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f83e22effb8739ec3fdcae64612cffac4ee7579638549caf47c70342693285`  
		Last Modified: Wed, 14 Feb 2024 20:57:29 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce41b07883cf81f89185e0e1b4fc65b39258a3f1aaff0ce01028854071ddecb`  
		Last Modified: Wed, 14 Feb 2024 20:57:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7954912de33be8cc7e1e4ea36180acfc8bb6cc7b7dc043d43d5912cfd171cd3`  
		Last Modified: Wed, 14 Feb 2024 20:57:33 GMT  
		Size: 25.6 MB (25560320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c63eb439e08d84b2f39090a2a87819fe70e5dfe666f3d4c4d3985acfd1364b0`  
		Last Modified: Wed, 14 Feb 2024 20:57:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fef719b5ba36fc0af1638fb03777e938c25331563e1d178a89bae94d428c8fb`  
		Last Modified: Wed, 14 Feb 2024 20:57:27 GMT  
		Size: 285.4 KB (285394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8d167b3e7ee16cfc662a87231b4084716742686d31d5b82e887b234efec2e9`  
		Last Modified: Tue, 05 Mar 2024 19:42:21 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c28621adc2c564252debe98669a98b5db5ce45172ce843466e26b8b689b114a`  
		Last Modified: Tue, 05 Mar 2024 19:42:40 GMT  
		Size: 69.4 MB (69364712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5c43bdc8404f132a84e8a0f4c69e490b01b908e8633abcfe604de71e205648`  
		Last Modified: Tue, 05 Mar 2024 19:42:21 GMT  
		Size: 1.5 KB (1545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcc239c5226abef94ce51a464e18875c9ff8a1fded12c55a44a3396d065d9a0`  
		Last Modified: Tue, 05 Mar 2024 20:04:31 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92819fb904e989755feedb88fdac313dd0614617cb2124f845e1beb9ef0b7840`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866ca856d15d8b11f3251d0e1e751bce5ccd3d04170d016b81a7e721ee811cff`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478c6e5efb5198c62dae853963d276055bc2ce33ae70aca26cba13a16359a054`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806deb5a287a2c1cfa951ac44704c97b32856f31e9d0012590d79e5b068279f1`  
		Last Modified: Tue, 05 Mar 2024 20:04:30 GMT  
		Size: 1.7 MB (1678307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bb868ab3b0ea5f9e471cb10db42cf456ce7dfe4ecb2ec8769a9c97c105483e`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:9ffd2fc461bcd523f2c67f8692ea85156c40fb2b21e35b457547522153eb44b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `caddy:2.7.6-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:e924a818b35c77fa77b850501f876fa811c43019e884675210e1232eb23b13a6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2007476156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69198d50697c7c62515331afda3b6b548388fe7ecfbec519f7bcb8e8ab8e5155`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:27:24 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Feb 2024 20:27:25 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Feb 2024 20:27:26 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Feb 2024 20:27:27 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Feb 2024 20:28:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:28:04 GMT
ENV GOPATH=C:\go
# Wed, 14 Feb 2024 20:28:25 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Mar 2024 19:27:34 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 19:29:55 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Mar 2024 19:29:57 GMT
WORKDIR C:\go
# Tue, 05 Mar 2024 20:03:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Mar 2024 20:03:28 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:03:29 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:03:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:03:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 05 Mar 2024 20:03:52 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ac8de2d709384a84400f6f072b2d3d4c4d454ee27f8ec716db4964eabac3f8`  
		Last Modified: Wed, 14 Feb 2024 20:55:46 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70115ee0ce6c09f30645181ec6f80fe9ece4e9b51628fdbaa85ebd4e0ae979e1`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab323644de57af1911793c0a10501a7b21640f8e58484665dc2258f482cb943`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae53fd363daebfb127c2ba7e51543cf93130802d95e194fc71db09c52b9fe10c`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665a9a35030c2076331610dfe4c22866525c2b0ac219981d900f1b6178af5241`  
		Last Modified: Wed, 14 Feb 2024 20:55:50 GMT  
		Size: 25.5 MB (25534020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ab59c20a7391d04f68a3dc2b9d6eb4cfd1e7af0ddd33e30d2cd19f13535c0`  
		Last Modified: Wed, 14 Feb 2024 20:55:43 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a35884f3b4e6aa2080cc34668faeabacc75000ef04e2fe4ec3e76f166d992e4`  
		Last Modified: Wed, 14 Feb 2024 20:55:43 GMT  
		Size: 266.0 KB (265989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c81949701f9fd28f5c42cfa101f1e2c2858efdb4032e3c3a221ae64417094d`  
		Last Modified: Tue, 05 Mar 2024 19:41:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c07bf58a4a94d97d30abeee1c89ea03f4d6bb5ae58ba58a108ab8c14ce86d04`  
		Last Modified: Tue, 05 Mar 2024 19:42:12 GMT  
		Size: 69.4 MB (69350261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff66f61d5b04d89a7cd43a5718c2738ee8c932ff7976238576fcce4a9205188`  
		Last Modified: Tue, 05 Mar 2024 19:41:52 GMT  
		Size: 1.5 KB (1539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fff8f151323c49bef4ab32c69e1b7fb0bc1c38c418bc58f8d552450f83ddb4`  
		Last Modified: Tue, 05 Mar 2024 20:04:48 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad11e6d0d7e8e1cdeb21675479688d12574b1f3aaf78c017dcb3f3f0e461e94`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3bac1fc388577dc02e99cece1f2418b768a6b9131f03ccb3a12b5130d0657c`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2023c4236e1ee6e1e21d75518a4e0b041879053cca3a4d196a736c11ef937885`  
		Last Modified: Tue, 05 Mar 2024 20:04:45 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646022f7531f95a5e75674d8b4716cd2b10acf7080eacbcf1a9146ec3c17a381`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.7 MB (1653517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a594d21bdd61142fc0e9073bca5c902365dcacea37bc8513a5868bccebfd5e5`  
		Last Modified: Tue, 05 Mar 2024 20:04:45 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-windowsservercore`

```console
$ docker pull caddy@sha256:444dc16652b598c3d6f69627e313944c17cb36a0adfc3c366fa738e2ed0e1895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `caddy:2.7.6-windowsservercore` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:f6e8f7815f3e03bc5d239d52a2bdeb473ff959a4b74bb86ee94b410cc2407c35
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1926683398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d9ff1f8c7723994d4a4f7c520159beedff8fe440b855a9fb6f57afdcae7b2b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:22:32 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:22:33 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:23:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:23:00 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:23:01 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:23:02 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:23:03 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:23:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:23:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:23:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:23:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:23:09 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:23:11 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:23:26 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:23:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ebcfc7e63facc5463d681dd534f084e021cc447cf46213aae377066d573493`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 458.4 KB (458447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bee2047afe4426d5715972f534b35ce0bc5ae241ae42982e37a64185c7a482`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39da07145bbe64c3ec2c032dafa6eb6ddf62130dba67e03a627cc2cb3788f9e2`  
		Last Modified: Wed, 14 Feb 2024 21:26:37 GMT  
		Size: 15.3 MB (15267126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c47f482128a80b23df310b1c1b71bfa176b010cdd91761fb1a9aa71c4812738`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dab75e60136c0cf03ae7e7ad030b7adb3aff8014f4fc0e412d1ce9c217bdd60`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db7f5e1b9057131a3d1e7f1439de34f87684add5ac177612296925ed37b654d`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ac08dfbec3219d30d64f54cc8e1b46009cf4327d55c288ca43d875eaff3763`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4fad3dd8e3739d27a2d3793ae4740b4cbf52999f2295ad370545f048730492`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91f700224a04849cd48e2ab6525d47b7188051110718ca045ca50452ce26cb3`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fe7f9176dbfd4a89d170a117169a90cd5f49a2c5b7a55ac4026288812b8b60`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4fc40cf63828021df321258238a85d39918d2749a117bb0538bda0afce3aef`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9621f5d2e06bf68f778ba42ec6ec5d4a80d1cfb1204ea19b5a2b42d2b1d87d`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398c5b0cde2fcd40c8ce079d93fd115bd8ee7d8028cabc4baf9ecc07ab226410`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60cb86bd52f82372e11b1b851709ccb6c10537dc9262f63ef8bcd0152efb235`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c35a9695bf632732db6dd52a7531c75c5243819b2b8d7c019a1e8fc796e13c7`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c98226f721bed207883df26f4d35276821dd38299a62458d2ba6c55fab5b0d`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b23541f7ccf5a2debb904fdc41eccc03284d7fbf3baff61798b726d7c9ba12`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ce3a452fdfcd413ac385a157633a0fe389a8c2fdb281ce79b5cdd4d16dcb9b`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 281.4 KB (281363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7be2379ebd2e4d0fca0bbf81dd2628e93d8efd2ef3ea28c3872855ca6e50ed`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:793d5d17edca1d44e963efc2d79f97a389420f253790a04d54f9388492ca70ff
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2096464983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2636f0474ebff3dfb86f6d92e45af2173f0773887039f3e30776eb3b2de1bd0c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:18:41 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:18:42 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:20:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:20:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:20:23 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:20:24 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:20:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:20:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:20:31 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:20:33 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:20:34 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:20:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:20:36 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:20:36 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:20:37 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:20:38 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:20:40 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:21:47 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:21:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936f6b22f9979fac96518b60eadd4d9156939b025d673ce61a2e6a18553dc2b1`  
		Last Modified: Wed, 14 Feb 2024 21:26:08 GMT  
		Size: 461.6 KB (461622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72873b058a9927d9ea1e4a234006a54fec29d1da3beb3f2834ce66fda6f4262f`  
		Last Modified: Wed, 14 Feb 2024 21:26:07 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc3d79323d38d65e8112fca8b77ad54434883a9104dd542fdc179cf782fab1e`  
		Last Modified: Wed, 14 Feb 2024 21:26:10 GMT  
		Size: 15.3 MB (15274562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4873aaa427e9ae13aeebcc096c23b92dd4d61d1f6b601a755dfaf268c4b85ab6`  
		Last Modified: Wed, 14 Feb 2024 21:26:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c57d3fae417c15ca2cf9d965bd8d05bab080154e20cd2e20f5d71aa86de5c0f`  
		Last Modified: Wed, 14 Feb 2024 21:26:06 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444c12e07ce56e352f094a12c03aa1ab4110c79d5daa78eea733580703bdef6a`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cf5cd505e0ce461fb00191ec16014104c1f3f38c373b2179b9cb0ecec44082`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f67f42fce82938d220cec3933239aedeffe9da096d14f3354eb2ffd49902c8`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb581bc05a23526a9b12256e17b6963201710bb71ae435fed4ccbdc69330fe8`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806d41685663d3f82e404087dda88f57f3f2534966be1a73998da0d9d3f15ae8`  
		Last Modified: Wed, 14 Feb 2024 21:26:04 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af65ac33d93c108086650ad059ffe57d44fcae5dfcfd80f331aeb3acb759145`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1d5135587234fcaf02c388f1fbf2e4a7be50b81f4c5296aeb7a99cb5fc2d13`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705d9a64f11bac49a31ef3cb6bfd926024e700d3daf666b277867cddcef7fcff`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac09729a4577f5fe6afe0d3a00560ec715f86b1e907e28917ca6d13dcafb3e7`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cd769674ca72532329328651bf168fe61494249405bb59e89832d94410289b`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a7dedf94b664393c8ae954445d5b582ffe6d8ffc604ddaaae79b20de72317`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a465dd935213cb9e1bd4aae1e392fd32e5fcb661c6bf3b7a50e113ea7077d7`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d18f93e3aab637778f45296a721f0857d0c5ec759335b634ae323255bbb0c29`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 257.6 KB (257571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11c0d021a3877f354347717399af0fe31b30ddd220f2b64b4ccf68fe7b6140b`  
		Last Modified: Wed, 14 Feb 2024 21:26:02 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-windowsservercore-1809`

```console
$ docker pull caddy@sha256:fa377f42fcef67994cd1ff2eca1715f8ddbb6836a84cc7a6b796df01353d6f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `caddy:2.7.6-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:793d5d17edca1d44e963efc2d79f97a389420f253790a04d54f9388492ca70ff
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2096464983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2636f0474ebff3dfb86f6d92e45af2173f0773887039f3e30776eb3b2de1bd0c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:18:41 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:18:42 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:20:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:20:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:20:23 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:20:24 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:20:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:20:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:20:31 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:20:33 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:20:34 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:20:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:20:36 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:20:36 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:20:37 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:20:38 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:20:40 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:21:47 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:21:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936f6b22f9979fac96518b60eadd4d9156939b025d673ce61a2e6a18553dc2b1`  
		Last Modified: Wed, 14 Feb 2024 21:26:08 GMT  
		Size: 461.6 KB (461622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72873b058a9927d9ea1e4a234006a54fec29d1da3beb3f2834ce66fda6f4262f`  
		Last Modified: Wed, 14 Feb 2024 21:26:07 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc3d79323d38d65e8112fca8b77ad54434883a9104dd542fdc179cf782fab1e`  
		Last Modified: Wed, 14 Feb 2024 21:26:10 GMT  
		Size: 15.3 MB (15274562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4873aaa427e9ae13aeebcc096c23b92dd4d61d1f6b601a755dfaf268c4b85ab6`  
		Last Modified: Wed, 14 Feb 2024 21:26:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c57d3fae417c15ca2cf9d965bd8d05bab080154e20cd2e20f5d71aa86de5c0f`  
		Last Modified: Wed, 14 Feb 2024 21:26:06 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444c12e07ce56e352f094a12c03aa1ab4110c79d5daa78eea733580703bdef6a`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cf5cd505e0ce461fb00191ec16014104c1f3f38c373b2179b9cb0ecec44082`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f67f42fce82938d220cec3933239aedeffe9da096d14f3354eb2ffd49902c8`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb581bc05a23526a9b12256e17b6963201710bb71ae435fed4ccbdc69330fe8`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806d41685663d3f82e404087dda88f57f3f2534966be1a73998da0d9d3f15ae8`  
		Last Modified: Wed, 14 Feb 2024 21:26:04 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af65ac33d93c108086650ad059ffe57d44fcae5dfcfd80f331aeb3acb759145`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1d5135587234fcaf02c388f1fbf2e4a7be50b81f4c5296aeb7a99cb5fc2d13`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705d9a64f11bac49a31ef3cb6bfd926024e700d3daf666b277867cddcef7fcff`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac09729a4577f5fe6afe0d3a00560ec715f86b1e907e28917ca6d13dcafb3e7`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cd769674ca72532329328651bf168fe61494249405bb59e89832d94410289b`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a7dedf94b664393c8ae954445d5b582ffe6d8ffc604ddaaae79b20de72317`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a465dd935213cb9e1bd4aae1e392fd32e5fcb661c6bf3b7a50e113ea7077d7`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d18f93e3aab637778f45296a721f0857d0c5ec759335b634ae323255bbb0c29`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 257.6 KB (257571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11c0d021a3877f354347717399af0fe31b30ddd220f2b64b4ccf68fe7b6140b`  
		Last Modified: Wed, 14 Feb 2024 21:26:02 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:6e915ccce3def5db60e3af13d28e398bfdbde6a3298781b0cf53cbb174b0f23e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `caddy:2.7.6-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:f6e8f7815f3e03bc5d239d52a2bdeb473ff959a4b74bb86ee94b410cc2407c35
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1926683398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d9ff1f8c7723994d4a4f7c520159beedff8fe440b855a9fb6f57afdcae7b2b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:22:32 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:22:33 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:23:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:23:00 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:23:01 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:23:02 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:23:03 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:23:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:23:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:23:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:23:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:23:09 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:23:11 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:23:26 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:23:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ebcfc7e63facc5463d681dd534f084e021cc447cf46213aae377066d573493`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 458.4 KB (458447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bee2047afe4426d5715972f534b35ce0bc5ae241ae42982e37a64185c7a482`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39da07145bbe64c3ec2c032dafa6eb6ddf62130dba67e03a627cc2cb3788f9e2`  
		Last Modified: Wed, 14 Feb 2024 21:26:37 GMT  
		Size: 15.3 MB (15267126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c47f482128a80b23df310b1c1b71bfa176b010cdd91761fb1a9aa71c4812738`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dab75e60136c0cf03ae7e7ad030b7adb3aff8014f4fc0e412d1ce9c217bdd60`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db7f5e1b9057131a3d1e7f1439de34f87684add5ac177612296925ed37b654d`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ac08dfbec3219d30d64f54cc8e1b46009cf4327d55c288ca43d875eaff3763`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4fad3dd8e3739d27a2d3793ae4740b4cbf52999f2295ad370545f048730492`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91f700224a04849cd48e2ab6525d47b7188051110718ca045ca50452ce26cb3`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fe7f9176dbfd4a89d170a117169a90cd5f49a2c5b7a55ac4026288812b8b60`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4fc40cf63828021df321258238a85d39918d2749a117bb0538bda0afce3aef`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9621f5d2e06bf68f778ba42ec6ec5d4a80d1cfb1204ea19b5a2b42d2b1d87d`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398c5b0cde2fcd40c8ce079d93fd115bd8ee7d8028cabc4baf9ecc07ab226410`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60cb86bd52f82372e11b1b851709ccb6c10537dc9262f63ef8bcd0152efb235`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c35a9695bf632732db6dd52a7531c75c5243819b2b8d7c019a1e8fc796e13c7`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c98226f721bed207883df26f4d35276821dd38299a62458d2ba6c55fab5b0d`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b23541f7ccf5a2debb904fdc41eccc03284d7fbf3baff61798b726d7c9ba12`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ce3a452fdfcd413ac385a157633a0fe389a8c2fdb281ce79b5cdd4d16dcb9b`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 281.4 KB (281363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7be2379ebd2e4d0fca0bbf81dd2628e93d8efd2ef3ea28c3872855ca6e50ed`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1297 bytes)  
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
$ docker pull caddy@sha256:7954f9183f22718dfac36955b6cb281466256ae195f30ffcd0229596e2badc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:683161d33599ee7740b25d8c0466e82bfd94e491c63bef744eda38919853dd62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76973779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e7c249761d733da653482a2b5259eaae803dee4354bc3562e48a601315e6ff`
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
# Tue, 05 Mar 2024 19:42:13 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 19:42:13 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 19:42:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 19:42:15 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 19:42:15 GMT
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
	-	`sha256:ddc853d0ab24d3fe195e8492db2866ec9d01681c218bdff73afb081fa97cb002`  
		Last Modified: Tue, 05 Mar 2024 19:42:32 GMT  
		Size: 5.0 MB (4972975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea68e3f24bc6efb27b70b8c1870bf11b4a5fad53eb40e8ce77817c21586972d`  
		Last Modified: Tue, 05 Mar 2024 19:42:31 GMT  
		Size: 1.3 MB (1302236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ecce85dc39a9d244f2c3b1e0e89e72279e6d9f6b154afad2171642b11c137b`  
		Last Modified: Tue, 05 Mar 2024 19:42:31 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ece7f11958f255486a5be355c9180900873b391449f4258706b535d5177b40b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75407413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22234bb36f9348628e9caea0dac041e47e0df57676643cb27bc893380168cbd`
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
# Tue, 05 Mar 2024 23:00:43 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 23:00:43 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 23:00:44 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 23:00:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 23:00:44 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 23:00:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 23:00:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 23:00:49 GMT
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
	-	`sha256:bccd7f5c5a4f0abc0a23393d9a04f353b767b809c6ac950caaa731dd3768c8eb`  
		Last Modified: Tue, 05 Mar 2024 20:11:40 GMT  
		Size: 65.8 MB (65767479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33a4721f193119280f7dfc5baed0ce6a2d3b2eb94e31901d986ea54166c41ea`  
		Last Modified: Tue, 05 Mar 2024 20:11:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28b5e7a7f3d8467fb26f35d8b70ae0853d39fb4103058a0dc47dd62be3256d7`  
		Last Modified: Tue, 05 Mar 2024 23:01:07 GMT  
		Size: 5.0 MB (4958742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276c5f8fd9c641c6036e92487a700ea1b6cc811b8ac1578ff0f94803223f6e0d`  
		Last Modified: Tue, 05 Mar 2024 23:01:07 GMT  
		Size: 1.2 MB (1248648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db777cbc747c60df3dc9c90c42c55125b12f7c65e05a6b1ab52ec8de565848a9`  
		Last Modified: Tue, 05 Mar 2024 23:01:06 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:156f7188ad9f04c359241e42567a3cee24477cb1885639d634da45c042cc297e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2a4fac0ed075caa114df1d0fd560d017af28251032ec5015a49c0702fe3d48`
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
# Tue, 05 Mar 2024 20:48:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:48:44 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:48:45 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:48:45 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:48:45 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:48:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:48:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:48:48 GMT
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
	-	`sha256:17f0c2683a0605dfb4fff92a0c34044c42624cbc47515f2262026e23ffa28b15`  
		Last Modified: Tue, 05 Mar 2024 20:01:25 GMT  
		Size: 65.8 MB (65767445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1570cef4f4f43311a29ff4036cc73329f8fe806fb19c51f3413b3073bfc70634`  
		Last Modified: Tue, 05 Mar 2024 20:01:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2640aa4bbda58460e9e4fd9b0a0969303c9a30ba9b9ff6424d9349f7c0ffbcd`  
		Last Modified: Tue, 05 Mar 2024 20:49:09 GMT  
		Size: 4.5 MB (4514657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5f06f998d08d9a0ca561581720f1399d9e1c6f64b4637370acd8eddc90418e`  
		Last Modified: Tue, 05 Mar 2024 20:49:08 GMT  
		Size: 1.2 MB (1246081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f58b57eb0adfeabad656db0f59a85f8373054397123d068fe68452663713a9f`  
		Last Modified: Tue, 05 Mar 2024 20:49:08 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:b7d23a0e6f86ad993855c69a14f149837072ce99399627ee74d95e4705784d14
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73993792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0728d6faf4e6faebb8c082c95826cc671a39f43e1cd9ef0cfcd909a42435c9bd`
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
# Tue, 05 Mar 2024 20:00:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:00:21 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:00:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:00:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:00:23 GMT
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
	-	`sha256:5a91045fa00056cff12698db93bed8fe188f9895b74e96e29b6a9f6a6e047937`  
		Last Modified: Tue, 05 Mar 2024 19:44:44 GMT  
		Size: 64.1 MB (64111148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f155e563ada2bb78e99decac187a48adcf9db3cd56e543bc0694674ef8a234`  
		Last Modified: Tue, 05 Mar 2024 19:44:35 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f627d8e1519d50a70f854d0342a035bd62a8cedf0d7a61351f7ac191accf21`  
		Last Modified: Tue, 05 Mar 2024 20:00:40 GMT  
		Size: 5.1 MB (5063926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cf96a60cd43a372ff273debacac6160f6842de4adc5e79eef190c8a791eecc`  
		Last Modified: Tue, 05 Mar 2024 20:00:39 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113a17d73127a40aa417b169724fea00b3b34ed479e7d3fb2b656325c7d131a8`  
		Last Modified: Tue, 05 Mar 2024 20:00:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:3321233002d79314df5692f81246bbcc2d0c9ba268c61792fd6269b1e64e6ff9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74219843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b9b8fd2c1e8bd5b65bfbd17b919aabf00faf29ce73a1702c8a2610afe5427c`
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
# Tue, 05 Mar 2024 19:40:39 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 19:40:40 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 19:40:40 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 19:40:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 19:40:41 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 19:40:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 19:40:44 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 19:40:44 GMT
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
	-	`sha256:1e1323fc82438c3a0b40c7bcf18c7b4808edcec55b91135df534741787df9cbc`  
		Last Modified: Tue, 05 Mar 2024 19:25:03 GMT  
		Size: 64.1 MB (64126907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8630ef56928609490ea4cc1460f549f49e84ed6ff4f6bb7ffb5c3fa5e53f3027`  
		Last Modified: Tue, 05 Mar 2024 19:24:51 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c2f5a4fa35cf481005994eef4a926ba3b1cecb6ee2747d8080460c88a7fa6c`  
		Last Modified: Tue, 05 Mar 2024 19:41:02 GMT  
		Size: 5.3 MB (5270995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cba91d041ae77cf958d8509d23d6f741eec735e9bf9a24d489d0b8842db30c9`  
		Last Modified: Tue, 05 Mar 2024 19:41:01 GMT  
		Size: 1.2 MB (1186176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de13da806adead3ab5a4380c923e80ebddfc28b7b94d6e6f43b6cbb920acd85`  
		Last Modified: Tue, 05 Mar 2024 19:41:01 GMT  
		Size: 407.0 B  
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

### `caddy:builder` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:e924a818b35c77fa77b850501f876fa811c43019e884675210e1232eb23b13a6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2007476156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69198d50697c7c62515331afda3b6b548388fe7ecfbec519f7bcb8e8ab8e5155`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:27:24 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Feb 2024 20:27:25 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Feb 2024 20:27:26 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Feb 2024 20:27:27 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Feb 2024 20:28:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:28:04 GMT
ENV GOPATH=C:\go
# Wed, 14 Feb 2024 20:28:25 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Mar 2024 19:27:34 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 19:29:55 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Mar 2024 19:29:57 GMT
WORKDIR C:\go
# Tue, 05 Mar 2024 20:03:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Mar 2024 20:03:28 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:03:29 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:03:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:03:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 05 Mar 2024 20:03:52 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ac8de2d709384a84400f6f072b2d3d4c4d454ee27f8ec716db4964eabac3f8`  
		Last Modified: Wed, 14 Feb 2024 20:55:46 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70115ee0ce6c09f30645181ec6f80fe9ece4e9b51628fdbaa85ebd4e0ae979e1`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab323644de57af1911793c0a10501a7b21640f8e58484665dc2258f482cb943`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae53fd363daebfb127c2ba7e51543cf93130802d95e194fc71db09c52b9fe10c`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665a9a35030c2076331610dfe4c22866525c2b0ac219981d900f1b6178af5241`  
		Last Modified: Wed, 14 Feb 2024 20:55:50 GMT  
		Size: 25.5 MB (25534020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ab59c20a7391d04f68a3dc2b9d6eb4cfd1e7af0ddd33e30d2cd19f13535c0`  
		Last Modified: Wed, 14 Feb 2024 20:55:43 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a35884f3b4e6aa2080cc34668faeabacc75000ef04e2fe4ec3e76f166d992e4`  
		Last Modified: Wed, 14 Feb 2024 20:55:43 GMT  
		Size: 266.0 KB (265989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c81949701f9fd28f5c42cfa101f1e2c2858efdb4032e3c3a221ae64417094d`  
		Last Modified: Tue, 05 Mar 2024 19:41:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c07bf58a4a94d97d30abeee1c89ea03f4d6bb5ae58ba58a108ab8c14ce86d04`  
		Last Modified: Tue, 05 Mar 2024 19:42:12 GMT  
		Size: 69.4 MB (69350261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff66f61d5b04d89a7cd43a5718c2738ee8c932ff7976238576fcce4a9205188`  
		Last Modified: Tue, 05 Mar 2024 19:41:52 GMT  
		Size: 1.5 KB (1539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fff8f151323c49bef4ab32c69e1b7fb0bc1c38c418bc58f8d552450f83ddb4`  
		Last Modified: Tue, 05 Mar 2024 20:04:48 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad11e6d0d7e8e1cdeb21675479688d12574b1f3aaf78c017dcb3f3f0e461e94`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3bac1fc388577dc02e99cece1f2418b768a6b9131f03ccb3a12b5130d0657c`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2023c4236e1ee6e1e21d75518a4e0b041879053cca3a4d196a736c11ef937885`  
		Last Modified: Tue, 05 Mar 2024 20:04:45 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646022f7531f95a5e75674d8b4716cd2b10acf7080eacbcf1a9146ec3c17a381`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.7 MB (1653517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a594d21bdd61142fc0e9073bca5c902365dcacea37bc8513a5868bccebfd5e5`  
		Last Modified: Tue, 05 Mar 2024 20:04:45 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:63e3bb18f43a20a50a640e33d80c15d6447e5c49eb758ad2ac92dd3c2215e1d9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2177356061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51bf8c2ce948dfc3bc85a84137d8ed09be2f3b755821c887f151431733f69def`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:31:24 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Feb 2024 20:31:24 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Feb 2024 20:31:25 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Feb 2024 20:31:26 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Feb 2024 20:33:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:33:15 GMT
ENV GOPATH=C:\go
# Wed, 14 Feb 2024 20:34:38 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Mar 2024 19:30:18 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 19:33:39 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Mar 2024 19:33:40 GMT
WORKDIR C:\go
# Tue, 05 Mar 2024 20:00:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Mar 2024 20:00:06 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:00:06 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:00:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:03:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 05 Mar 2024 20:03:10 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001ba7ca58e0032ab21885ed5be98699fa0e8693d84ce59492bbdeb45a1f5b89`  
		Last Modified: Wed, 14 Feb 2024 20:57:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964f6547b697b5014d27c4ae5aa9115c1686907b1f2524f8f0de888da7a79bd8`  
		Last Modified: Wed, 14 Feb 2024 20:57:29 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f83e22effb8739ec3fdcae64612cffac4ee7579638549caf47c70342693285`  
		Last Modified: Wed, 14 Feb 2024 20:57:29 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce41b07883cf81f89185e0e1b4fc65b39258a3f1aaff0ce01028854071ddecb`  
		Last Modified: Wed, 14 Feb 2024 20:57:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7954912de33be8cc7e1e4ea36180acfc8bb6cc7b7dc043d43d5912cfd171cd3`  
		Last Modified: Wed, 14 Feb 2024 20:57:33 GMT  
		Size: 25.6 MB (25560320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c63eb439e08d84b2f39090a2a87819fe70e5dfe666f3d4c4d3985acfd1364b0`  
		Last Modified: Wed, 14 Feb 2024 20:57:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fef719b5ba36fc0af1638fb03777e938c25331563e1d178a89bae94d428c8fb`  
		Last Modified: Wed, 14 Feb 2024 20:57:27 GMT  
		Size: 285.4 KB (285394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8d167b3e7ee16cfc662a87231b4084716742686d31d5b82e887b234efec2e9`  
		Last Modified: Tue, 05 Mar 2024 19:42:21 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c28621adc2c564252debe98669a98b5db5ce45172ce843466e26b8b689b114a`  
		Last Modified: Tue, 05 Mar 2024 19:42:40 GMT  
		Size: 69.4 MB (69364712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5c43bdc8404f132a84e8a0f4c69e490b01b908e8633abcfe604de71e205648`  
		Last Modified: Tue, 05 Mar 2024 19:42:21 GMT  
		Size: 1.5 KB (1545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcc239c5226abef94ce51a464e18875c9ff8a1fded12c55a44a3396d065d9a0`  
		Last Modified: Tue, 05 Mar 2024 20:04:31 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92819fb904e989755feedb88fdac313dd0614617cb2124f845e1beb9ef0b7840`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866ca856d15d8b11f3251d0e1e751bce5ccd3d04170d016b81a7e721ee811cff`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478c6e5efb5198c62dae853963d276055bc2ce33ae70aca26cba13a16359a054`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806deb5a287a2c1cfa951ac44704c97b32856f31e9d0012590d79e5b068279f1`  
		Last Modified: Tue, 05 Mar 2024 20:04:30 GMT  
		Size: 1.7 MB (1678307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bb868ab3b0ea5f9e471cb10db42cf456ce7dfe4ecb2ec8769a9c97c105483e`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:efedb356080be1cd5584baa80df964cbe3d85af049bbfee7775d9659e1809360
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
$ docker pull caddy@sha256:683161d33599ee7740b25d8c0466e82bfd94e491c63bef744eda38919853dd62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76973779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e7c249761d733da653482a2b5259eaae803dee4354bc3562e48a601315e6ff`
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
# Tue, 05 Mar 2024 19:42:13 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 19:42:13 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 19:42:13 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 19:42:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 19:42:15 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 19:42:15 GMT
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
	-	`sha256:ddc853d0ab24d3fe195e8492db2866ec9d01681c218bdff73afb081fa97cb002`  
		Last Modified: Tue, 05 Mar 2024 19:42:32 GMT  
		Size: 5.0 MB (4972975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea68e3f24bc6efb27b70b8c1870bf11b4a5fad53eb40e8ce77817c21586972d`  
		Last Modified: Tue, 05 Mar 2024 19:42:31 GMT  
		Size: 1.3 MB (1302236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ecce85dc39a9d244f2c3b1e0e89e72279e6d9f6b154afad2171642b11c137b`  
		Last Modified: Tue, 05 Mar 2024 19:42:31 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:ece7f11958f255486a5be355c9180900873b391449f4258706b535d5177b40b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75407413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22234bb36f9348628e9caea0dac041e47e0df57676643cb27bc893380168cbd`
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
# Tue, 05 Mar 2024 23:00:43 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 23:00:43 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 23:00:44 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 23:00:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 23:00:44 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 23:00:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 23:00:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 23:00:49 GMT
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
	-	`sha256:bccd7f5c5a4f0abc0a23393d9a04f353b767b809c6ac950caaa731dd3768c8eb`  
		Last Modified: Tue, 05 Mar 2024 20:11:40 GMT  
		Size: 65.8 MB (65767479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33a4721f193119280f7dfc5baed0ce6a2d3b2eb94e31901d986ea54166c41ea`  
		Last Modified: Tue, 05 Mar 2024 20:11:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28b5e7a7f3d8467fb26f35d8b70ae0853d39fb4103058a0dc47dd62be3256d7`  
		Last Modified: Tue, 05 Mar 2024 23:01:07 GMT  
		Size: 5.0 MB (4958742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276c5f8fd9c641c6036e92487a700ea1b6cc811b8ac1578ff0f94803223f6e0d`  
		Last Modified: Tue, 05 Mar 2024 23:01:07 GMT  
		Size: 1.2 MB (1248648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db777cbc747c60df3dc9c90c42c55125b12f7c65e05a6b1ab52ec8de565848a9`  
		Last Modified: Tue, 05 Mar 2024 23:01:06 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:156f7188ad9f04c359241e42567a3cee24477cb1885639d634da45c042cc297e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2a4fac0ed075caa114df1d0fd560d017af28251032ec5015a49c0702fe3d48`
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
# Tue, 05 Mar 2024 20:48:44 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:48:44 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:48:45 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:48:45 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:48:45 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:48:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:48:48 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:48:48 GMT
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
	-	`sha256:17f0c2683a0605dfb4fff92a0c34044c42624cbc47515f2262026e23ffa28b15`  
		Last Modified: Tue, 05 Mar 2024 20:01:25 GMT  
		Size: 65.8 MB (65767445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1570cef4f4f43311a29ff4036cc73329f8fe806fb19c51f3413b3073bfc70634`  
		Last Modified: Tue, 05 Mar 2024 20:01:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2640aa4bbda58460e9e4fd9b0a0969303c9a30ba9b9ff6424d9349f7c0ffbcd`  
		Last Modified: Tue, 05 Mar 2024 20:49:09 GMT  
		Size: 4.5 MB (4514657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5f06f998d08d9a0ca561581720f1399d9e1c6f64b4637370acd8eddc90418e`  
		Last Modified: Tue, 05 Mar 2024 20:49:08 GMT  
		Size: 1.2 MB (1246081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f58b57eb0adfeabad656db0f59a85f8373054397123d068fe68452663713a9f`  
		Last Modified: Tue, 05 Mar 2024 20:49:08 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:b7d23a0e6f86ad993855c69a14f149837072ce99399627ee74d95e4705784d14
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73993792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0728d6faf4e6faebb8c082c95826cc671a39f43e1cd9ef0cfcd909a42435c9bd`
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
# Tue, 05 Mar 2024 20:00:21 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:00:21 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:00:21 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 20:00:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 20:00:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 20:00:23 GMT
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
	-	`sha256:5a91045fa00056cff12698db93bed8fe188f9895b74e96e29b6a9f6a6e047937`  
		Last Modified: Tue, 05 Mar 2024 19:44:44 GMT  
		Size: 64.1 MB (64111148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f155e563ada2bb78e99decac187a48adcf9db3cd56e543bc0694674ef8a234`  
		Last Modified: Tue, 05 Mar 2024 19:44:35 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f627d8e1519d50a70f854d0342a035bd62a8cedf0d7a61351f7ac191accf21`  
		Last Modified: Tue, 05 Mar 2024 20:00:40 GMT  
		Size: 5.1 MB (5063926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cf96a60cd43a372ff273debacac6160f6842de4adc5e79eef190c8a791eecc`  
		Last Modified: Tue, 05 Mar 2024 20:00:39 GMT  
		Size: 1.2 MB (1198448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113a17d73127a40aa417b169724fea00b3b34ed479e7d3fb2b656325c7d131a8`  
		Last Modified: Tue, 05 Mar 2024 20:00:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:3321233002d79314df5692f81246bbcc2d0c9ba268c61792fd6269b1e64e6ff9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74219843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b9b8fd2c1e8bd5b65bfbd17b919aabf00faf29ce73a1702c8a2610afe5427c`
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
# Tue, 05 Mar 2024 19:40:39 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Tue, 05 Mar 2024 19:40:40 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 19:40:40 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 19:40:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 19:40:41 GMT
ENV XCADDY_SETCAP=1
# Tue, 05 Mar 2024 19:40:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Mar 2024 19:40:44 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Mar 2024 19:40:44 GMT
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
	-	`sha256:1e1323fc82438c3a0b40c7bcf18c7b4808edcec55b91135df534741787df9cbc`  
		Last Modified: Tue, 05 Mar 2024 19:25:03 GMT  
		Size: 64.1 MB (64126907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8630ef56928609490ea4cc1460f549f49e84ed6ff4f6bb7ffb5c3fa5e53f3027`  
		Last Modified: Tue, 05 Mar 2024 19:24:51 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c2f5a4fa35cf481005994eef4a926ba3b1cecb6ee2747d8080460c88a7fa6c`  
		Last Modified: Tue, 05 Mar 2024 19:41:02 GMT  
		Size: 5.3 MB (5270995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cba91d041ae77cf958d8509d23d6f741eec735e9bf9a24d489d0b8842db30c9`  
		Last Modified: Tue, 05 Mar 2024 19:41:01 GMT  
		Size: 1.2 MB (1186176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de13da806adead3ab5a4380c923e80ebddfc28b7b94d6e6f43b6cbb920acd85`  
		Last Modified: Tue, 05 Mar 2024 19:41:01 GMT  
		Size: 407.0 B  
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
$ docker pull caddy@sha256:7a4365fc853bf4ac7b497c662da666883c7471fb89275c320e38fe77949144f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:63e3bb18f43a20a50a640e33d80c15d6447e5c49eb758ad2ac92dd3c2215e1d9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2177356061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51bf8c2ce948dfc3bc85a84137d8ed09be2f3b755821c887f151431733f69def`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:31:24 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Feb 2024 20:31:24 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Feb 2024 20:31:25 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Feb 2024 20:31:26 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Feb 2024 20:33:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:33:15 GMT
ENV GOPATH=C:\go
# Wed, 14 Feb 2024 20:34:38 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Mar 2024 19:30:18 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 19:33:39 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Mar 2024 19:33:40 GMT
WORKDIR C:\go
# Tue, 05 Mar 2024 20:00:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Mar 2024 20:00:06 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:00:06 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:00:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:03:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 05 Mar 2024 20:03:10 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001ba7ca58e0032ab21885ed5be98699fa0e8693d84ce59492bbdeb45a1f5b89`  
		Last Modified: Wed, 14 Feb 2024 20:57:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964f6547b697b5014d27c4ae5aa9115c1686907b1f2524f8f0de888da7a79bd8`  
		Last Modified: Wed, 14 Feb 2024 20:57:29 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f83e22effb8739ec3fdcae64612cffac4ee7579638549caf47c70342693285`  
		Last Modified: Wed, 14 Feb 2024 20:57:29 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce41b07883cf81f89185e0e1b4fc65b39258a3f1aaff0ce01028854071ddecb`  
		Last Modified: Wed, 14 Feb 2024 20:57:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7954912de33be8cc7e1e4ea36180acfc8bb6cc7b7dc043d43d5912cfd171cd3`  
		Last Modified: Wed, 14 Feb 2024 20:57:33 GMT  
		Size: 25.6 MB (25560320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c63eb439e08d84b2f39090a2a87819fe70e5dfe666f3d4c4d3985acfd1364b0`  
		Last Modified: Wed, 14 Feb 2024 20:57:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fef719b5ba36fc0af1638fb03777e938c25331563e1d178a89bae94d428c8fb`  
		Last Modified: Wed, 14 Feb 2024 20:57:27 GMT  
		Size: 285.4 KB (285394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8d167b3e7ee16cfc662a87231b4084716742686d31d5b82e887b234efec2e9`  
		Last Modified: Tue, 05 Mar 2024 19:42:21 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c28621adc2c564252debe98669a98b5db5ce45172ce843466e26b8b689b114a`  
		Last Modified: Tue, 05 Mar 2024 19:42:40 GMT  
		Size: 69.4 MB (69364712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5c43bdc8404f132a84e8a0f4c69e490b01b908e8633abcfe604de71e205648`  
		Last Modified: Tue, 05 Mar 2024 19:42:21 GMT  
		Size: 1.5 KB (1545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcc239c5226abef94ce51a464e18875c9ff8a1fded12c55a44a3396d065d9a0`  
		Last Modified: Tue, 05 Mar 2024 20:04:31 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92819fb904e989755feedb88fdac313dd0614617cb2124f845e1beb9ef0b7840`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866ca856d15d8b11f3251d0e1e751bce5ccd3d04170d016b81a7e721ee811cff`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478c6e5efb5198c62dae853963d276055bc2ce33ae70aca26cba13a16359a054`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806deb5a287a2c1cfa951ac44704c97b32856f31e9d0012590d79e5b068279f1`  
		Last Modified: Tue, 05 Mar 2024 20:04:30 GMT  
		Size: 1.7 MB (1678307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bb868ab3b0ea5f9e471cb10db42cf456ce7dfe4ecb2ec8769a9c97c105483e`  
		Last Modified: Tue, 05 Mar 2024 20:04:29 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:9ffd2fc461bcd523f2c67f8692ea85156c40fb2b21e35b457547522153eb44b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:e924a818b35c77fa77b850501f876fa811c43019e884675210e1232eb23b13a6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2007476156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69198d50697c7c62515331afda3b6b548388fe7ecfbec519f7bcb8e8ab8e5155`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:27:24 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Feb 2024 20:27:25 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Feb 2024 20:27:26 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Feb 2024 20:27:27 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Feb 2024 20:28:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:28:04 GMT
ENV GOPATH=C:\go
# Wed, 14 Feb 2024 20:28:25 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Mar 2024 19:27:34 GMT
ENV GOLANG_VERSION=1.21.8
# Tue, 05 Mar 2024 19:29:55 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Mar 2024 19:29:57 GMT
WORKDIR C:\go
# Tue, 05 Mar 2024 20:03:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Mar 2024 20:03:28 GMT
ENV XCADDY_VERSION=v0.3.5
# Tue, 05 Mar 2024 20:03:29 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 05 Mar 2024 20:03:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Mar 2024 20:03:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 05 Mar 2024 20:03:52 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ac8de2d709384a84400f6f072b2d3d4c4d454ee27f8ec716db4964eabac3f8`  
		Last Modified: Wed, 14 Feb 2024 20:55:46 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70115ee0ce6c09f30645181ec6f80fe9ece4e9b51628fdbaa85ebd4e0ae979e1`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab323644de57af1911793c0a10501a7b21640f8e58484665dc2258f482cb943`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae53fd363daebfb127c2ba7e51543cf93130802d95e194fc71db09c52b9fe10c`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665a9a35030c2076331610dfe4c22866525c2b0ac219981d900f1b6178af5241`  
		Last Modified: Wed, 14 Feb 2024 20:55:50 GMT  
		Size: 25.5 MB (25534020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ab59c20a7391d04f68a3dc2b9d6eb4cfd1e7af0ddd33e30d2cd19f13535c0`  
		Last Modified: Wed, 14 Feb 2024 20:55:43 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a35884f3b4e6aa2080cc34668faeabacc75000ef04e2fe4ec3e76f166d992e4`  
		Last Modified: Wed, 14 Feb 2024 20:55:43 GMT  
		Size: 266.0 KB (265989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c81949701f9fd28f5c42cfa101f1e2c2858efdb4032e3c3a221ae64417094d`  
		Last Modified: Tue, 05 Mar 2024 19:41:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c07bf58a4a94d97d30abeee1c89ea03f4d6bb5ae58ba58a108ab8c14ce86d04`  
		Last Modified: Tue, 05 Mar 2024 19:42:12 GMT  
		Size: 69.4 MB (69350261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff66f61d5b04d89a7cd43a5718c2738ee8c932ff7976238576fcce4a9205188`  
		Last Modified: Tue, 05 Mar 2024 19:41:52 GMT  
		Size: 1.5 KB (1539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fff8f151323c49bef4ab32c69e1b7fb0bc1c38c418bc58f8d552450f83ddb4`  
		Last Modified: Tue, 05 Mar 2024 20:04:48 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad11e6d0d7e8e1cdeb21675479688d12574b1f3aaf78c017dcb3f3f0e461e94`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3bac1fc388577dc02e99cece1f2418b768a6b9131f03ccb3a12b5130d0657c`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2023c4236e1ee6e1e21d75518a4e0b041879053cca3a4d196a736c11ef937885`  
		Last Modified: Tue, 05 Mar 2024 20:04:45 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646022f7531f95a5e75674d8b4716cd2b10acf7080eacbcf1a9146ec3c17a381`  
		Last Modified: Tue, 05 Mar 2024 20:04:46 GMT  
		Size: 1.7 MB (1653517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a594d21bdd61142fc0e9073bca5c902365dcacea37bc8513a5868bccebfd5e5`  
		Last Modified: Tue, 05 Mar 2024 20:04:45 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:latest`

```console
$ docker pull caddy@sha256:2a0d069ea95d91641d201943a5a049e83cbfade8039670aebfb441b132189de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

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

### `caddy:latest` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:f6e8f7815f3e03bc5d239d52a2bdeb473ff959a4b74bb86ee94b410cc2407c35
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1926683398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d9ff1f8c7723994d4a4f7c520159beedff8fe440b855a9fb6f57afdcae7b2b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:22:32 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:22:33 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:23:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:23:00 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:23:01 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:23:02 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:23:03 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:23:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:23:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:23:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:23:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:23:09 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:23:11 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:23:26 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:23:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ebcfc7e63facc5463d681dd534f084e021cc447cf46213aae377066d573493`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 458.4 KB (458447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bee2047afe4426d5715972f534b35ce0bc5ae241ae42982e37a64185c7a482`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39da07145bbe64c3ec2c032dafa6eb6ddf62130dba67e03a627cc2cb3788f9e2`  
		Last Modified: Wed, 14 Feb 2024 21:26:37 GMT  
		Size: 15.3 MB (15267126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c47f482128a80b23df310b1c1b71bfa176b010cdd91761fb1a9aa71c4812738`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dab75e60136c0cf03ae7e7ad030b7adb3aff8014f4fc0e412d1ce9c217bdd60`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db7f5e1b9057131a3d1e7f1439de34f87684add5ac177612296925ed37b654d`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ac08dfbec3219d30d64f54cc8e1b46009cf4327d55c288ca43d875eaff3763`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4fad3dd8e3739d27a2d3793ae4740b4cbf52999f2295ad370545f048730492`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91f700224a04849cd48e2ab6525d47b7188051110718ca045ca50452ce26cb3`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fe7f9176dbfd4a89d170a117169a90cd5f49a2c5b7a55ac4026288812b8b60`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4fc40cf63828021df321258238a85d39918d2749a117bb0538bda0afce3aef`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9621f5d2e06bf68f778ba42ec6ec5d4a80d1cfb1204ea19b5a2b42d2b1d87d`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398c5b0cde2fcd40c8ce079d93fd115bd8ee7d8028cabc4baf9ecc07ab226410`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60cb86bd52f82372e11b1b851709ccb6c10537dc9262f63ef8bcd0152efb235`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c35a9695bf632732db6dd52a7531c75c5243819b2b8d7c019a1e8fc796e13c7`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c98226f721bed207883df26f4d35276821dd38299a62458d2ba6c55fab5b0d`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b23541f7ccf5a2debb904fdc41eccc03284d7fbf3baff61798b726d7c9ba12`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ce3a452fdfcd413ac385a157633a0fe389a8c2fdb281ce79b5cdd4d16dcb9b`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 281.4 KB (281363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7be2379ebd2e4d0fca0bbf81dd2628e93d8efd2ef3ea28c3872855ca6e50ed`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:793d5d17edca1d44e963efc2d79f97a389420f253790a04d54f9388492ca70ff
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2096464983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2636f0474ebff3dfb86f6d92e45af2173f0773887039f3e30776eb3b2de1bd0c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:18:41 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:18:42 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:20:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:20:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:20:23 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:20:24 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:20:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:20:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:20:31 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:20:33 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:20:34 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:20:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:20:36 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:20:36 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:20:37 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:20:38 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:20:40 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:21:47 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:21:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936f6b22f9979fac96518b60eadd4d9156939b025d673ce61a2e6a18553dc2b1`  
		Last Modified: Wed, 14 Feb 2024 21:26:08 GMT  
		Size: 461.6 KB (461622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72873b058a9927d9ea1e4a234006a54fec29d1da3beb3f2834ce66fda6f4262f`  
		Last Modified: Wed, 14 Feb 2024 21:26:07 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc3d79323d38d65e8112fca8b77ad54434883a9104dd542fdc179cf782fab1e`  
		Last Modified: Wed, 14 Feb 2024 21:26:10 GMT  
		Size: 15.3 MB (15274562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4873aaa427e9ae13aeebcc096c23b92dd4d61d1f6b601a755dfaf268c4b85ab6`  
		Last Modified: Wed, 14 Feb 2024 21:26:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c57d3fae417c15ca2cf9d965bd8d05bab080154e20cd2e20f5d71aa86de5c0f`  
		Last Modified: Wed, 14 Feb 2024 21:26:06 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444c12e07ce56e352f094a12c03aa1ab4110c79d5daa78eea733580703bdef6a`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cf5cd505e0ce461fb00191ec16014104c1f3f38c373b2179b9cb0ecec44082`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f67f42fce82938d220cec3933239aedeffe9da096d14f3354eb2ffd49902c8`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb581bc05a23526a9b12256e17b6963201710bb71ae435fed4ccbdc69330fe8`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806d41685663d3f82e404087dda88f57f3f2534966be1a73998da0d9d3f15ae8`  
		Last Modified: Wed, 14 Feb 2024 21:26:04 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af65ac33d93c108086650ad059ffe57d44fcae5dfcfd80f331aeb3acb759145`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1d5135587234fcaf02c388f1fbf2e4a7be50b81f4c5296aeb7a99cb5fc2d13`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705d9a64f11bac49a31ef3cb6bfd926024e700d3daf666b277867cddcef7fcff`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac09729a4577f5fe6afe0d3a00560ec715f86b1e907e28917ca6d13dcafb3e7`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cd769674ca72532329328651bf168fe61494249405bb59e89832d94410289b`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a7dedf94b664393c8ae954445d5b582ffe6d8ffc604ddaaae79b20de72317`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a465dd935213cb9e1bd4aae1e392fd32e5fcb661c6bf3b7a50e113ea7077d7`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d18f93e3aab637778f45296a721f0857d0c5ec759335b634ae323255bbb0c29`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 257.6 KB (257571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11c0d021a3877f354347717399af0fe31b30ddd220f2b64b4ccf68fe7b6140b`  
		Last Modified: Wed, 14 Feb 2024 21:26:02 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:444dc16652b598c3d6f69627e313944c17cb36a0adfc3c366fa738e2ed0e1895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `caddy:windowsservercore` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:f6e8f7815f3e03bc5d239d52a2bdeb473ff959a4b74bb86ee94b410cc2407c35
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1926683398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d9ff1f8c7723994d4a4f7c520159beedff8fe440b855a9fb6f57afdcae7b2b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:22:32 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:22:33 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:23:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:23:00 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:23:01 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:23:02 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:23:03 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:23:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:23:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:23:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:23:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:23:09 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:23:11 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:23:26 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:23:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ebcfc7e63facc5463d681dd534f084e021cc447cf46213aae377066d573493`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 458.4 KB (458447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bee2047afe4426d5715972f534b35ce0bc5ae241ae42982e37a64185c7a482`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39da07145bbe64c3ec2c032dafa6eb6ddf62130dba67e03a627cc2cb3788f9e2`  
		Last Modified: Wed, 14 Feb 2024 21:26:37 GMT  
		Size: 15.3 MB (15267126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c47f482128a80b23df310b1c1b71bfa176b010cdd91761fb1a9aa71c4812738`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dab75e60136c0cf03ae7e7ad030b7adb3aff8014f4fc0e412d1ce9c217bdd60`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db7f5e1b9057131a3d1e7f1439de34f87684add5ac177612296925ed37b654d`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ac08dfbec3219d30d64f54cc8e1b46009cf4327d55c288ca43d875eaff3763`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4fad3dd8e3739d27a2d3793ae4740b4cbf52999f2295ad370545f048730492`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91f700224a04849cd48e2ab6525d47b7188051110718ca045ca50452ce26cb3`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fe7f9176dbfd4a89d170a117169a90cd5f49a2c5b7a55ac4026288812b8b60`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4fc40cf63828021df321258238a85d39918d2749a117bb0538bda0afce3aef`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9621f5d2e06bf68f778ba42ec6ec5d4a80d1cfb1204ea19b5a2b42d2b1d87d`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398c5b0cde2fcd40c8ce079d93fd115bd8ee7d8028cabc4baf9ecc07ab226410`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60cb86bd52f82372e11b1b851709ccb6c10537dc9262f63ef8bcd0152efb235`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c35a9695bf632732db6dd52a7531c75c5243819b2b8d7c019a1e8fc796e13c7`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c98226f721bed207883df26f4d35276821dd38299a62458d2ba6c55fab5b0d`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b23541f7ccf5a2debb904fdc41eccc03284d7fbf3baff61798b726d7c9ba12`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ce3a452fdfcd413ac385a157633a0fe389a8c2fdb281ce79b5cdd4d16dcb9b`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 281.4 KB (281363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7be2379ebd2e4d0fca0bbf81dd2628e93d8efd2ef3ea28c3872855ca6e50ed`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:793d5d17edca1d44e963efc2d79f97a389420f253790a04d54f9388492ca70ff
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2096464983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2636f0474ebff3dfb86f6d92e45af2173f0773887039f3e30776eb3b2de1bd0c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:18:41 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:18:42 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:20:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:20:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:20:23 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:20:24 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:20:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:20:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:20:31 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:20:33 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:20:34 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:20:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:20:36 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:20:36 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:20:37 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:20:38 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:20:40 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:21:47 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:21:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936f6b22f9979fac96518b60eadd4d9156939b025d673ce61a2e6a18553dc2b1`  
		Last Modified: Wed, 14 Feb 2024 21:26:08 GMT  
		Size: 461.6 KB (461622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72873b058a9927d9ea1e4a234006a54fec29d1da3beb3f2834ce66fda6f4262f`  
		Last Modified: Wed, 14 Feb 2024 21:26:07 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc3d79323d38d65e8112fca8b77ad54434883a9104dd542fdc179cf782fab1e`  
		Last Modified: Wed, 14 Feb 2024 21:26:10 GMT  
		Size: 15.3 MB (15274562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4873aaa427e9ae13aeebcc096c23b92dd4d61d1f6b601a755dfaf268c4b85ab6`  
		Last Modified: Wed, 14 Feb 2024 21:26:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c57d3fae417c15ca2cf9d965bd8d05bab080154e20cd2e20f5d71aa86de5c0f`  
		Last Modified: Wed, 14 Feb 2024 21:26:06 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444c12e07ce56e352f094a12c03aa1ab4110c79d5daa78eea733580703bdef6a`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cf5cd505e0ce461fb00191ec16014104c1f3f38c373b2179b9cb0ecec44082`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f67f42fce82938d220cec3933239aedeffe9da096d14f3354eb2ffd49902c8`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb581bc05a23526a9b12256e17b6963201710bb71ae435fed4ccbdc69330fe8`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806d41685663d3f82e404087dda88f57f3f2534966be1a73998da0d9d3f15ae8`  
		Last Modified: Wed, 14 Feb 2024 21:26:04 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af65ac33d93c108086650ad059ffe57d44fcae5dfcfd80f331aeb3acb759145`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1d5135587234fcaf02c388f1fbf2e4a7be50b81f4c5296aeb7a99cb5fc2d13`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705d9a64f11bac49a31ef3cb6bfd926024e700d3daf666b277867cddcef7fcff`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac09729a4577f5fe6afe0d3a00560ec715f86b1e907e28917ca6d13dcafb3e7`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cd769674ca72532329328651bf168fe61494249405bb59e89832d94410289b`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a7dedf94b664393c8ae954445d5b582ffe6d8ffc604ddaaae79b20de72317`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a465dd935213cb9e1bd4aae1e392fd32e5fcb661c6bf3b7a50e113ea7077d7`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d18f93e3aab637778f45296a721f0857d0c5ec759335b634ae323255bbb0c29`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 257.6 KB (257571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11c0d021a3877f354347717399af0fe31b30ddd220f2b64b4ccf68fe7b6140b`  
		Last Modified: Wed, 14 Feb 2024 21:26:02 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:fa377f42fcef67994cd1ff2eca1715f8ddbb6836a84cc7a6b796df01353d6f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:793d5d17edca1d44e963efc2d79f97a389420f253790a04d54f9388492ca70ff
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2096464983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2636f0474ebff3dfb86f6d92e45af2173f0773887039f3e30776eb3b2de1bd0c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:18:41 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:18:42 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:20:03 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:20:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:20:23 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:20:24 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:20:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:20:29 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:20:31 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:20:33 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:20:34 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:20:35 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:20:36 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:20:36 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:20:37 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:20:38 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:20:40 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:21:47 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:21:48 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5cf1b8dc4236433b7c7119f02020edc4978b089d198a909e7c51554ff6703`  
		Last Modified: Wed, 14 Feb 2024 20:57:31 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936f6b22f9979fac96518b60eadd4d9156939b025d673ce61a2e6a18553dc2b1`  
		Last Modified: Wed, 14 Feb 2024 21:26:08 GMT  
		Size: 461.6 KB (461622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72873b058a9927d9ea1e4a234006a54fec29d1da3beb3f2834ce66fda6f4262f`  
		Last Modified: Wed, 14 Feb 2024 21:26:07 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc3d79323d38d65e8112fca8b77ad54434883a9104dd542fdc179cf782fab1e`  
		Last Modified: Wed, 14 Feb 2024 21:26:10 GMT  
		Size: 15.3 MB (15274562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4873aaa427e9ae13aeebcc096c23b92dd4d61d1f6b601a755dfaf268c4b85ab6`  
		Last Modified: Wed, 14 Feb 2024 21:26:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c57d3fae417c15ca2cf9d965bd8d05bab080154e20cd2e20f5d71aa86de5c0f`  
		Last Modified: Wed, 14 Feb 2024 21:26:06 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444c12e07ce56e352f094a12c03aa1ab4110c79d5daa78eea733580703bdef6a`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cf5cd505e0ce461fb00191ec16014104c1f3f38c373b2179b9cb0ecec44082`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f67f42fce82938d220cec3933239aedeffe9da096d14f3354eb2ffd49902c8`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb581bc05a23526a9b12256e17b6963201710bb71ae435fed4ccbdc69330fe8`  
		Last Modified: Wed, 14 Feb 2024 21:26:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806d41685663d3f82e404087dda88f57f3f2534966be1a73998da0d9d3f15ae8`  
		Last Modified: Wed, 14 Feb 2024 21:26:04 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af65ac33d93c108086650ad059ffe57d44fcae5dfcfd80f331aeb3acb759145`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1d5135587234fcaf02c388f1fbf2e4a7be50b81f4c5296aeb7a99cb5fc2d13`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705d9a64f11bac49a31ef3cb6bfd926024e700d3daf666b277867cddcef7fcff`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac09729a4577f5fe6afe0d3a00560ec715f86b1e907e28917ca6d13dcafb3e7`  
		Last Modified: Wed, 14 Feb 2024 21:26:03 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cd769674ca72532329328651bf168fe61494249405bb59e89832d94410289b`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464a7dedf94b664393c8ae954445d5b582ffe6d8ffc604ddaaae79b20de72317`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a465dd935213cb9e1bd4aae1e392fd32e5fcb661c6bf3b7a50e113ea7077d7`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d18f93e3aab637778f45296a721f0857d0c5ec759335b634ae323255bbb0c29`  
		Last Modified: Wed, 14 Feb 2024 21:26:01 GMT  
		Size: 257.6 KB (257571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11c0d021a3877f354347717399af0fe31b30ddd220f2b64b4ccf68fe7b6140b`  
		Last Modified: Wed, 14 Feb 2024 21:26:02 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:6e915ccce3def5db60e3af13d28e398bfdbde6a3298781b0cf53cbb174b0f23e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:f6e8f7815f3e03bc5d239d52a2bdeb473ff959a4b74bb86ee94b410cc2407c35
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1926683398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d9ff1f8c7723994d4a4f7c520159beedff8fe440b855a9fb6f57afdcae7b2b`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:22:32 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Feb 2024 21:22:33 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:23:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Feb 2024 21:23:00 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Feb 2024 21:23:01 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Feb 2024 21:23:02 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 14 Feb 2024 21:23:03 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Feb 2024 21:23:04 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Feb 2024 21:23:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Feb 2024 21:23:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Feb 2024 21:23:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Feb 2024 21:23:08 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Feb 2024 21:23:09 GMT
EXPOSE 80
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443
# Wed, 14 Feb 2024 21:23:10 GMT
EXPOSE 443/udp
# Wed, 14 Feb 2024 21:23:11 GMT
EXPOSE 2019
# Wed, 14 Feb 2024 21:23:26 GMT
RUN caddy version
# Wed, 14 Feb 2024 21:23:27 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ebcfc7e63facc5463d681dd534f084e021cc447cf46213aae377066d573493`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 458.4 KB (458447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bee2047afe4426d5715972f534b35ce0bc5ae241ae42982e37a64185c7a482`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39da07145bbe64c3ec2c032dafa6eb6ddf62130dba67e03a627cc2cb3788f9e2`  
		Last Modified: Wed, 14 Feb 2024 21:26:37 GMT  
		Size: 15.3 MB (15267126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c47f482128a80b23df310b1c1b71bfa176b010cdd91761fb1a9aa71c4812738`  
		Last Modified: Wed, 14 Feb 2024 21:26:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dab75e60136c0cf03ae7e7ad030b7adb3aff8014f4fc0e412d1ce9c217bdd60`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db7f5e1b9057131a3d1e7f1439de34f87684add5ac177612296925ed37b654d`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ac08dfbec3219d30d64f54cc8e1b46009cf4327d55c288ca43d875eaff3763`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4fad3dd8e3739d27a2d3793ae4740b4cbf52999f2295ad370545f048730492`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91f700224a04849cd48e2ab6525d47b7188051110718ca045ca50452ce26cb3`  
		Last Modified: Wed, 14 Feb 2024 21:26:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fe7f9176dbfd4a89d170a117169a90cd5f49a2c5b7a55ac4026288812b8b60`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4fc40cf63828021df321258238a85d39918d2749a117bb0538bda0afce3aef`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9621f5d2e06bf68f778ba42ec6ec5d4a80d1cfb1204ea19b5a2b42d2b1d87d`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398c5b0cde2fcd40c8ce079d93fd115bd8ee7d8028cabc4baf9ecc07ab226410`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60cb86bd52f82372e11b1b851709ccb6c10537dc9262f63ef8bcd0152efb235`  
		Last Modified: Wed, 14 Feb 2024 21:26:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c35a9695bf632732db6dd52a7531c75c5243819b2b8d7c019a1e8fc796e13c7`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c98226f721bed207883df26f4d35276821dd38299a62458d2ba6c55fab5b0d`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b23541f7ccf5a2debb904fdc41eccc03284d7fbf3baff61798b726d7c9ba12`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ce3a452fdfcd413ac385a157633a0fe389a8c2fdb281ce79b5cdd4d16dcb9b`  
		Last Modified: Wed, 14 Feb 2024 21:26:28 GMT  
		Size: 281.4 KB (281363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7be2379ebd2e4d0fca0bbf81dd2628e93d8efd2ef3ea28c3872855ca6e50ed`  
		Last Modified: Wed, 14 Feb 2024 21:26:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
