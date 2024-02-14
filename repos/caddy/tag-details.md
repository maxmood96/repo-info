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
$ docker pull caddy@sha256:52b96e26a80a1694b7195f1be152643f7a27b85d1b809e38f7b4d2def10a03a1
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
$ docker pull caddy@sha256:8fee3614a6b6cabdab16312c9ec1062982ef3d655b99bcc8e983cbc777572fa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76972175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2decac0840cd748d459d2f76eebc64754108ee601a66e06fca48c6880efcdb02`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 20:10:42 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 20:10:42 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 20:10:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 20:10:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 20:10:43 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 20:10:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 20:10:44 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 20:10:44 GMT
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
	-	`sha256:d18ba8e8dd02491f11cea93df354c71628a2360674a625c205e213ef6fd82127`  
		Last Modified: Tue, 06 Feb 2024 23:56:58 GMT  
		Size: 67.0 MB (67009643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8daf023d266d667210cf5767c01f2f4f68e40c297e0bdecf73799744ddac1026`  
		Last Modified: Tue, 06 Feb 2024 23:56:47 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23298fdc181f9cc9b4b9e297a84c2ff9119ed9ccef7ee4188033e1e62b835a71`  
		Last Modified: Wed, 07 Feb 2024 20:11:02 GMT  
		Size: 5.0 MB (4972450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2716cf52013dbd506ec1fae43d30c4339d959e635e237a5f6b1e8311fba51b4a`  
		Last Modified: Wed, 07 Feb 2024 20:11:02 GMT  
		Size: 1.3 MB (1302239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1a06d10c122c1efe42b77b107513d80c320d5adadaeeaec6ffe0235d8738c1`  
		Last Modified: Wed, 07 Feb 2024 20:11:02 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:89493aa84b348e455d5d5d3dd0f050644d7e3a9400cdc1a09d07545d95e85fd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75415278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921e0138a2eb31837973f479ce9117ffd13a871b9e3c1e3332f0689b85ec2e5d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 07:28:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 07:28:02 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 07:28:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 07:28:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 07:28:03 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 07:28:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 07:28:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 07:28:04 GMT
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
	-	`sha256:fa53b2f66831ea2a6a71d6469b90663284dc2a4ce3cb48320dd55896f9cd8d84`  
		Last Modified: Tue, 06 Feb 2024 23:32:01 GMT  
		Size: 65.8 MB (65767452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6d1ac72f2f91d206a9c3fa198f2e45b1f18fcfd8da385ab8c5e3288262790`  
		Last Modified: Tue, 06 Feb 2024 23:31:47 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6fbc6c4773d705c6048f1330050fc6200a9ae262d156ab7492ac01fc483010`  
		Last Modified: Wed, 07 Feb 2024 07:28:17 GMT  
		Size: 5.0 MB (4966629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cdc84144fd70dfac8f705109ec0a92dc10a7dfc50838c6af32b442b918fcc6`  
		Last Modified: Wed, 07 Feb 2024 07:28:17 GMT  
		Size: 1.2 MB (1248656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78e6ef661fee931920aa3236f1af661d851378c52b31aa87ffc8558da5e48a5`  
		Last Modified: Wed, 07 Feb 2024 07:28:16 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ff0b3bb63b15b33debf9aea993bd84f4b246b7c7d4484db77832556ef074ca51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c07a4329692996a3988717e0eba3652501b15f09abc9597e4ad3b87250cb63d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 02:48:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 02:48:33 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 02:48:33 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 02:48:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 02:48:34 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 02:48:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 02:48:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 02:48:38 GMT
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
	-	`sha256:7113cf104f60011eb6444102f15ef72cdd45fcb4c9caf77828b5fbc38dab492e`  
		Last Modified: Wed, 07 Feb 2024 02:23:31 GMT  
		Size: 65.8 MB (65767658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a6e0f5354f83f214823ce1d03ea8a7eab56425405c4ca69940f2f3dde97a80`  
		Last Modified: Wed, 07 Feb 2024 02:23:15 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f390b29274db9c266f41d8708269d5dda362068060acd663c445ce335597d742`  
		Last Modified: Wed, 07 Feb 2024 02:49:00 GMT  
		Size: 4.5 MB (4514221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399e806721f760b662ba77d6b0d28a03a0c91cfb57e9d60a85f9016392605507`  
		Last Modified: Wed, 07 Feb 2024 02:48:59 GMT  
		Size: 1.2 MB (1246089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5225c4821fb8eb5d3c9024e1b8b00504669f1ced491c2e93b97b5400673970c2`  
		Last Modified: Wed, 07 Feb 2024 02:48:59 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:bee0d79c6d83f0f253201d3c21afebe471923903c79a57fc165382018992582b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73998590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43afba92f6c2f26ccd2d5a34a29409424cb5d7437f186994917fd86a2a330c21`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 03:27:19 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 03:27:19 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 03:27:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 03:27:21 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 03:27:21 GMT
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
	-	`sha256:49ff1670edc3c20a6a9614ecb3f794095053b0a2bc5c3d8a27ffb6771b4e8de5`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 5.1 MB (5070614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6bfbf28b1c962164432ab027c42dcb68debdd9c90fe50d3fdec0bac01a2a1b`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 1.2 MB (1198449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dec8839aa12d34c5fc6d220df303a7b58562c777e2281fb6b912cabcb3b808`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:ff608ed0346698200d108d948d192f9d9977f35b9ee6dba5dc437eecb95eff13
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74213050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3961610a4cc67151079da941b2fa3b5f9e84fdbadf7ddfc2345914f2e7d34270`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 02:38:42 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 02:38:43 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 02:38:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 02:38:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 02:38:44 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 02:38:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 02:38:47 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 02:38:48 GMT
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
	-	`sha256:189f1d64ec6387010de82030584f95d2f1cb77480534f720a6c8051e1c053202`  
		Last Modified: Wed, 07 Feb 2024 02:39:06 GMT  
		Size: 5.3 MB (5270668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439fb1dfa6333e4624dc554a68c980b15bda052268ac48be84e477697d3fa5fc`  
		Last Modified: Wed, 07 Feb 2024 02:39:05 GMT  
		Size: 1.2 MB (1186180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b46e2bfe6d57573d777ff909c837b014c894d5f5c65212804d738620cb252e2`  
		Last Modified: Wed, 07 Feb 2024 02:39:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:fad88c033e71179f3df4bf1a5b2e9d0d0264bcbaa498b911238fc07787bbace2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76100380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914aa8aec00e9a7014cfcc15953ecea9afcc02ceae16b98a5643c211c018e323`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 03:55:22 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 03:55:23 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 03:55:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 03:55:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 03:55:24 GMT
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
	-	`sha256:667df4a2c04946a51104abaa6f5ed310f5428e8423a5229c6a93e33a7bfd3afa`  
		Last Modified: Tue, 06 Feb 2024 22:15:10 GMT  
		Size: 66.2 MB (66217776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed37103477a46e4048ca49195fde1e764f57b71cb5abadd05970bee2e2f29cc`  
		Last Modified: Tue, 06 Feb 2024 22:14:59 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d511e031e1b91b289c43c1a2190ee22aa5f38fe22568e3b6e23cdf96db48b`  
		Last Modified: Wed, 07 Feb 2024 03:56:50 GMT  
		Size: 5.1 MB (5116980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255f032cffa62a5bea76ec237a6dfe24caf125994ad6151aed12f4ae30860c02`  
		Last Modified: Wed, 07 Feb 2024 03:56:50 GMT  
		Size: 1.3 MB (1262391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8b53fd06bb1ce493aa5cc33297d87b8edfe9fd834896df28185e9c3f9b8480`  
		Last Modified: Wed, 07 Feb 2024 03:56:49 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:f21fcacb51baed792b0310844331fa37b39b4235d5cbb8274b453b4abdbeb68b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2007478332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfd7236ef3ba33c49b0293ddeaed24ed8f1a4a4be50d73bb5daf279ed0d1067`
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
# Wed, 14 Feb 2024 20:43:58 GMT
ENV GOLANG_VERSION=1.21.7
# Wed, 14 Feb 2024 20:46:14 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:46:15 GMT
WORKDIR C:\go
# Wed, 14 Feb 2024 21:25:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:25:03 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 14 Feb 2024 21:25:04 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:25:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Feb 2024 21:25:28 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Feb 2024 21:25:29 GMT
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
	-	`sha256:6a320e20304175d59e4aee6ec77d02f07509c042e71352229d992e5a71178266`  
		Last Modified: Wed, 14 Feb 2024 21:00:19 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70d6b39cc331fef21be1e6e1e4f8a09002d3e8c2cbe5510f9b576f73a103a11`  
		Last Modified: Wed, 14 Feb 2024 21:00:38 GMT  
		Size: 69.3 MB (69339697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e925967ba6e0e9ec84f4892a901f9137d074b01da5967f3f02cca1d17c55401`  
		Last Modified: Wed, 14 Feb 2024 21:00:18 GMT  
		Size: 1.5 KB (1465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5be391477771ac6ef063dfff5f60c2bf3720c4c3e438914ad4f83d4186dd419`  
		Last Modified: Wed, 14 Feb 2024 21:27:15 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8040861524a92cd1ef40205f09edcc78fca950bc460c86dabddb5b7c9d207e1`  
		Last Modified: Wed, 14 Feb 2024 21:27:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146989057ff74f0c65231a30d9ae96ef9aca638ac186e5133ab6e62f60daa4e4`  
		Last Modified: Wed, 14 Feb 2024 21:27:13 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a1e9fdf12fec3886fbcf530321f59f401f9a8e9ca54deb5a50e1ef7035857c`  
		Last Modified: Wed, 14 Feb 2024 21:27:14 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f0b7658ba93600fbb3d46955c4030818eab0d9ee14ac0f2e17afd2728e1ea8`  
		Last Modified: Wed, 14 Feb 2024 21:27:14 GMT  
		Size: 1.7 MB (1666295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ffc354f7064866e9a01cd793241fe9fb0e6c82dc2388b1ed8ca9c0c70428b3`  
		Last Modified: Wed, 14 Feb 2024 21:27:13 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:536798cc04c493719ee143f8570a8ce2c06929deaefd229e15de08e0ad26d554
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2177347938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1022bc7754872a576d582646d52e18dcb896332104dc5ae6edbb3c7130f6fe10`
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
# Wed, 14 Feb 2024 20:46:27 GMT
ENV GOLANG_VERSION=1.21.7
# Wed, 14 Feb 2024 20:49:46 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:49:47 GMT
WORKDIR C:\go
# Wed, 14 Feb 2024 21:23:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:23:35 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 14 Feb 2024 21:23:36 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:23:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Feb 2024 21:24:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Feb 2024 21:24:54 GMT
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
	-	`sha256:fc4a495babb42867e41e9e0341672d9c3dc4342d7d1ca2089393548a9394712c`  
		Last Modified: Wed, 14 Feb 2024 21:00:48 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88628d70e4f0b09c4b4d93d847ecc1af2c6287a6ee7f2c02f8574d79323b7e94`  
		Last Modified: Wed, 14 Feb 2024 21:01:08 GMT  
		Size: 69.4 MB (69351914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9c7605984ae14daab7f947cbb370c489f648caa2436563473651ccbd225379`  
		Last Modified: Wed, 14 Feb 2024 21:00:48 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7d44e23d90802e1136be2c8be711e41683f02e6106a295dc7cc9e3567c3a79`  
		Last Modified: Wed, 14 Feb 2024 21:26:56 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b8bb132d080a4d6cdfdac7bc8d37ba32d8e594b8117bee0a7149d2e0e10a59`  
		Last Modified: Wed, 14 Feb 2024 21:26:54 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0da4afa5ca0ec4b0e5f6e0ba7198a70aebf33635612ae7f8538cd3b623178c`  
		Last Modified: Wed, 14 Feb 2024 21:26:53 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b40cba54a5386a0889184fc68012a0626b7585c728882c037f3c0778a0c5365`  
		Last Modified: Wed, 14 Feb 2024 21:26:54 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9a8a348cc99b33e0367f75baaa076f55305110bd2f991bf2ca49cdde949ea6`  
		Last Modified: Wed, 14 Feb 2024 21:26:54 GMT  
		Size: 1.7 MB (1683480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f900898726315c327700e5fd8845b66a9965afeafa8abbe836093c700afe897d`  
		Last Modified: Wed, 14 Feb 2024 21:26:53 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:33a92d10027f0a21785908d646f81c6c23b4abd130fc123200f00a9381693be9
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
$ docker pull caddy@sha256:8fee3614a6b6cabdab16312c9ec1062982ef3d655b99bcc8e983cbc777572fa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76972175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2decac0840cd748d459d2f76eebc64754108ee601a66e06fca48c6880efcdb02`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 20:10:42 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 20:10:42 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 20:10:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 20:10:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 20:10:43 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 20:10:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 20:10:44 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 20:10:44 GMT
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
	-	`sha256:d18ba8e8dd02491f11cea93df354c71628a2360674a625c205e213ef6fd82127`  
		Last Modified: Tue, 06 Feb 2024 23:56:58 GMT  
		Size: 67.0 MB (67009643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8daf023d266d667210cf5767c01f2f4f68e40c297e0bdecf73799744ddac1026`  
		Last Modified: Tue, 06 Feb 2024 23:56:47 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23298fdc181f9cc9b4b9e297a84c2ff9119ed9ccef7ee4188033e1e62b835a71`  
		Last Modified: Wed, 07 Feb 2024 20:11:02 GMT  
		Size: 5.0 MB (4972450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2716cf52013dbd506ec1fae43d30c4339d959e635e237a5f6b1e8311fba51b4a`  
		Last Modified: Wed, 07 Feb 2024 20:11:02 GMT  
		Size: 1.3 MB (1302239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1a06d10c122c1efe42b77b107513d80c320d5adadaeeaec6ffe0235d8738c1`  
		Last Modified: Wed, 07 Feb 2024 20:11:02 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:89493aa84b348e455d5d5d3dd0f050644d7e3a9400cdc1a09d07545d95e85fd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75415278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921e0138a2eb31837973f479ce9117ffd13a871b9e3c1e3332f0689b85ec2e5d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 07:28:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 07:28:02 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 07:28:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 07:28:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 07:28:03 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 07:28:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 07:28:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 07:28:04 GMT
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
	-	`sha256:fa53b2f66831ea2a6a71d6469b90663284dc2a4ce3cb48320dd55896f9cd8d84`  
		Last Modified: Tue, 06 Feb 2024 23:32:01 GMT  
		Size: 65.8 MB (65767452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6d1ac72f2f91d206a9c3fa198f2e45b1f18fcfd8da385ab8c5e3288262790`  
		Last Modified: Tue, 06 Feb 2024 23:31:47 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6fbc6c4773d705c6048f1330050fc6200a9ae262d156ab7492ac01fc483010`  
		Last Modified: Wed, 07 Feb 2024 07:28:17 GMT  
		Size: 5.0 MB (4966629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cdc84144fd70dfac8f705109ec0a92dc10a7dfc50838c6af32b442b918fcc6`  
		Last Modified: Wed, 07 Feb 2024 07:28:17 GMT  
		Size: 1.2 MB (1248656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78e6ef661fee931920aa3236f1af661d851378c52b31aa87ffc8558da5e48a5`  
		Last Modified: Wed, 07 Feb 2024 07:28:16 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ff0b3bb63b15b33debf9aea993bd84f4b246b7c7d4484db77832556ef074ca51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c07a4329692996a3988717e0eba3652501b15f09abc9597e4ad3b87250cb63d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 02:48:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 02:48:33 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 02:48:33 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 02:48:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 02:48:34 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 02:48:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 02:48:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 02:48:38 GMT
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
	-	`sha256:7113cf104f60011eb6444102f15ef72cdd45fcb4c9caf77828b5fbc38dab492e`  
		Last Modified: Wed, 07 Feb 2024 02:23:31 GMT  
		Size: 65.8 MB (65767658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a6e0f5354f83f214823ce1d03ea8a7eab56425405c4ca69940f2f3dde97a80`  
		Last Modified: Wed, 07 Feb 2024 02:23:15 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f390b29274db9c266f41d8708269d5dda362068060acd663c445ce335597d742`  
		Last Modified: Wed, 07 Feb 2024 02:49:00 GMT  
		Size: 4.5 MB (4514221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399e806721f760b662ba77d6b0d28a03a0c91cfb57e9d60a85f9016392605507`  
		Last Modified: Wed, 07 Feb 2024 02:48:59 GMT  
		Size: 1.2 MB (1246089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5225c4821fb8eb5d3c9024e1b8b00504669f1ced491c2e93b97b5400673970c2`  
		Last Modified: Wed, 07 Feb 2024 02:48:59 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:bee0d79c6d83f0f253201d3c21afebe471923903c79a57fc165382018992582b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73998590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43afba92f6c2f26ccd2d5a34a29409424cb5d7437f186994917fd86a2a330c21`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 03:27:19 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 03:27:19 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 03:27:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 03:27:21 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 03:27:21 GMT
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
	-	`sha256:49ff1670edc3c20a6a9614ecb3f794095053b0a2bc5c3d8a27ffb6771b4e8de5`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 5.1 MB (5070614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6bfbf28b1c962164432ab027c42dcb68debdd9c90fe50d3fdec0bac01a2a1b`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 1.2 MB (1198449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dec8839aa12d34c5fc6d220df303a7b58562c777e2281fb6b912cabcb3b808`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:ff608ed0346698200d108d948d192f9d9977f35b9ee6dba5dc437eecb95eff13
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74213050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3961610a4cc67151079da941b2fa3b5f9e84fdbadf7ddfc2345914f2e7d34270`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 02:38:42 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 02:38:43 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 02:38:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 02:38:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 02:38:44 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 02:38:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 02:38:47 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 02:38:48 GMT
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
	-	`sha256:189f1d64ec6387010de82030584f95d2f1cb77480534f720a6c8051e1c053202`  
		Last Modified: Wed, 07 Feb 2024 02:39:06 GMT  
		Size: 5.3 MB (5270668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439fb1dfa6333e4624dc554a68c980b15bda052268ac48be84e477697d3fa5fc`  
		Last Modified: Wed, 07 Feb 2024 02:39:05 GMT  
		Size: 1.2 MB (1186180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b46e2bfe6d57573d777ff909c837b014c894d5f5c65212804d738620cb252e2`  
		Last Modified: Wed, 07 Feb 2024 02:39:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:fad88c033e71179f3df4bf1a5b2e9d0d0264bcbaa498b911238fc07787bbace2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76100380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914aa8aec00e9a7014cfcc15953ecea9afcc02ceae16b98a5643c211c018e323`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 03:55:22 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 03:55:23 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 03:55:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 03:55:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 03:55:24 GMT
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
	-	`sha256:667df4a2c04946a51104abaa6f5ed310f5428e8423a5229c6a93e33a7bfd3afa`  
		Last Modified: Tue, 06 Feb 2024 22:15:10 GMT  
		Size: 66.2 MB (66217776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed37103477a46e4048ca49195fde1e764f57b71cb5abadd05970bee2e2f29cc`  
		Last Modified: Tue, 06 Feb 2024 22:14:59 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d511e031e1b91b289c43c1a2190ee22aa5f38fe22568e3b6e23cdf96db48b`  
		Last Modified: Wed, 07 Feb 2024 03:56:50 GMT  
		Size: 5.1 MB (5116980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255f032cffa62a5bea76ec237a6dfe24caf125994ad6151aed12f4ae30860c02`  
		Last Modified: Wed, 07 Feb 2024 03:56:50 GMT  
		Size: 1.3 MB (1262391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8b53fd06bb1ce493aa5cc33297d87b8edfe9fd834896df28185e9c3f9b8480`  
		Last Modified: Wed, 07 Feb 2024 03:56:49 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:3f8db6e8a2fe203d75df858bb7930fe4be2c30c957a28c2bcf5c21302a39c66d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:536798cc04c493719ee143f8570a8ce2c06929deaefd229e15de08e0ad26d554
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2177347938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1022bc7754872a576d582646d52e18dcb896332104dc5ae6edbb3c7130f6fe10`
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
# Wed, 14 Feb 2024 20:46:27 GMT
ENV GOLANG_VERSION=1.21.7
# Wed, 14 Feb 2024 20:49:46 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:49:47 GMT
WORKDIR C:\go
# Wed, 14 Feb 2024 21:23:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:23:35 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 14 Feb 2024 21:23:36 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:23:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Feb 2024 21:24:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Feb 2024 21:24:54 GMT
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
	-	`sha256:fc4a495babb42867e41e9e0341672d9c3dc4342d7d1ca2089393548a9394712c`  
		Last Modified: Wed, 14 Feb 2024 21:00:48 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88628d70e4f0b09c4b4d93d847ecc1af2c6287a6ee7f2c02f8574d79323b7e94`  
		Last Modified: Wed, 14 Feb 2024 21:01:08 GMT  
		Size: 69.4 MB (69351914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9c7605984ae14daab7f947cbb370c489f648caa2436563473651ccbd225379`  
		Last Modified: Wed, 14 Feb 2024 21:00:48 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7d44e23d90802e1136be2c8be711e41683f02e6106a295dc7cc9e3567c3a79`  
		Last Modified: Wed, 14 Feb 2024 21:26:56 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b8bb132d080a4d6cdfdac7bc8d37ba32d8e594b8117bee0a7149d2e0e10a59`  
		Last Modified: Wed, 14 Feb 2024 21:26:54 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0da4afa5ca0ec4b0e5f6e0ba7198a70aebf33635612ae7f8538cd3b623178c`  
		Last Modified: Wed, 14 Feb 2024 21:26:53 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b40cba54a5386a0889184fc68012a0626b7585c728882c037f3c0778a0c5365`  
		Last Modified: Wed, 14 Feb 2024 21:26:54 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9a8a348cc99b33e0367f75baaa076f55305110bd2f991bf2ca49cdde949ea6`  
		Last Modified: Wed, 14 Feb 2024 21:26:54 GMT  
		Size: 1.7 MB (1683480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f900898726315c327700e5fd8845b66a9965afeafa8abbe836093c700afe897d`  
		Last Modified: Wed, 14 Feb 2024 21:26:53 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:c902b48fcec4254e6ed5eeb752b75d08e42bbd1bbd67398e45da91dcfa46a841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:f21fcacb51baed792b0310844331fa37b39b4235d5cbb8274b453b4abdbeb68b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2007478332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfd7236ef3ba33c49b0293ddeaed24ed8f1a4a4be50d73bb5daf279ed0d1067`
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
# Wed, 14 Feb 2024 20:43:58 GMT
ENV GOLANG_VERSION=1.21.7
# Wed, 14 Feb 2024 20:46:14 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:46:15 GMT
WORKDIR C:\go
# Wed, 14 Feb 2024 21:25:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:25:03 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 14 Feb 2024 21:25:04 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:25:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Feb 2024 21:25:28 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Feb 2024 21:25:29 GMT
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
	-	`sha256:6a320e20304175d59e4aee6ec77d02f07509c042e71352229d992e5a71178266`  
		Last Modified: Wed, 14 Feb 2024 21:00:19 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70d6b39cc331fef21be1e6e1e4f8a09002d3e8c2cbe5510f9b576f73a103a11`  
		Last Modified: Wed, 14 Feb 2024 21:00:38 GMT  
		Size: 69.3 MB (69339697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e925967ba6e0e9ec84f4892a901f9137d074b01da5967f3f02cca1d17c55401`  
		Last Modified: Wed, 14 Feb 2024 21:00:18 GMT  
		Size: 1.5 KB (1465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5be391477771ac6ef063dfff5f60c2bf3720c4c3e438914ad4f83d4186dd419`  
		Last Modified: Wed, 14 Feb 2024 21:27:15 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8040861524a92cd1ef40205f09edcc78fca950bc460c86dabddb5b7c9d207e1`  
		Last Modified: Wed, 14 Feb 2024 21:27:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146989057ff74f0c65231a30d9ae96ef9aca638ac186e5133ab6e62f60daa4e4`  
		Last Modified: Wed, 14 Feb 2024 21:27:13 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a1e9fdf12fec3886fbcf530321f59f401f9a8e9ca54deb5a50e1ef7035857c`  
		Last Modified: Wed, 14 Feb 2024 21:27:14 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f0b7658ba93600fbb3d46955c4030818eab0d9ee14ac0f2e17afd2728e1ea8`  
		Last Modified: Wed, 14 Feb 2024 21:27:14 GMT  
		Size: 1.7 MB (1666295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ffc354f7064866e9a01cd793241fe9fb0e6c82dc2388b1ed8ca9c0c70428b3`  
		Last Modified: Wed, 14 Feb 2024 21:27:13 GMT  
		Size: 1.3 KB (1320 bytes)  
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
$ docker pull caddy@sha256:52b96e26a80a1694b7195f1be152643f7a27b85d1b809e38f7b4d2def10a03a1
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
$ docker pull caddy@sha256:8fee3614a6b6cabdab16312c9ec1062982ef3d655b99bcc8e983cbc777572fa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76972175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2decac0840cd748d459d2f76eebc64754108ee601a66e06fca48c6880efcdb02`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 20:10:42 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 20:10:42 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 20:10:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 20:10:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 20:10:43 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 20:10:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 20:10:44 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 20:10:44 GMT
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
	-	`sha256:d18ba8e8dd02491f11cea93df354c71628a2360674a625c205e213ef6fd82127`  
		Last Modified: Tue, 06 Feb 2024 23:56:58 GMT  
		Size: 67.0 MB (67009643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8daf023d266d667210cf5767c01f2f4f68e40c297e0bdecf73799744ddac1026`  
		Last Modified: Tue, 06 Feb 2024 23:56:47 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23298fdc181f9cc9b4b9e297a84c2ff9119ed9ccef7ee4188033e1e62b835a71`  
		Last Modified: Wed, 07 Feb 2024 20:11:02 GMT  
		Size: 5.0 MB (4972450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2716cf52013dbd506ec1fae43d30c4339d959e635e237a5f6b1e8311fba51b4a`  
		Last Modified: Wed, 07 Feb 2024 20:11:02 GMT  
		Size: 1.3 MB (1302239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1a06d10c122c1efe42b77b107513d80c320d5adadaeeaec6ffe0235d8738c1`  
		Last Modified: Wed, 07 Feb 2024 20:11:02 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:89493aa84b348e455d5d5d3dd0f050644d7e3a9400cdc1a09d07545d95e85fd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75415278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921e0138a2eb31837973f479ce9117ffd13a871b9e3c1e3332f0689b85ec2e5d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 07:28:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 07:28:02 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 07:28:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 07:28:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 07:28:03 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 07:28:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 07:28:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 07:28:04 GMT
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
	-	`sha256:fa53b2f66831ea2a6a71d6469b90663284dc2a4ce3cb48320dd55896f9cd8d84`  
		Last Modified: Tue, 06 Feb 2024 23:32:01 GMT  
		Size: 65.8 MB (65767452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6d1ac72f2f91d206a9c3fa198f2e45b1f18fcfd8da385ab8c5e3288262790`  
		Last Modified: Tue, 06 Feb 2024 23:31:47 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6fbc6c4773d705c6048f1330050fc6200a9ae262d156ab7492ac01fc483010`  
		Last Modified: Wed, 07 Feb 2024 07:28:17 GMT  
		Size: 5.0 MB (4966629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cdc84144fd70dfac8f705109ec0a92dc10a7dfc50838c6af32b442b918fcc6`  
		Last Modified: Wed, 07 Feb 2024 07:28:17 GMT  
		Size: 1.2 MB (1248656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78e6ef661fee931920aa3236f1af661d851378c52b31aa87ffc8558da5e48a5`  
		Last Modified: Wed, 07 Feb 2024 07:28:16 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ff0b3bb63b15b33debf9aea993bd84f4b246b7c7d4484db77832556ef074ca51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c07a4329692996a3988717e0eba3652501b15f09abc9597e4ad3b87250cb63d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 02:48:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 02:48:33 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 02:48:33 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 02:48:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 02:48:34 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 02:48:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 02:48:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 02:48:38 GMT
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
	-	`sha256:7113cf104f60011eb6444102f15ef72cdd45fcb4c9caf77828b5fbc38dab492e`  
		Last Modified: Wed, 07 Feb 2024 02:23:31 GMT  
		Size: 65.8 MB (65767658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a6e0f5354f83f214823ce1d03ea8a7eab56425405c4ca69940f2f3dde97a80`  
		Last Modified: Wed, 07 Feb 2024 02:23:15 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f390b29274db9c266f41d8708269d5dda362068060acd663c445ce335597d742`  
		Last Modified: Wed, 07 Feb 2024 02:49:00 GMT  
		Size: 4.5 MB (4514221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399e806721f760b662ba77d6b0d28a03a0c91cfb57e9d60a85f9016392605507`  
		Last Modified: Wed, 07 Feb 2024 02:48:59 GMT  
		Size: 1.2 MB (1246089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5225c4821fb8eb5d3c9024e1b8b00504669f1ced491c2e93b97b5400673970c2`  
		Last Modified: Wed, 07 Feb 2024 02:48:59 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:bee0d79c6d83f0f253201d3c21afebe471923903c79a57fc165382018992582b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73998590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43afba92f6c2f26ccd2d5a34a29409424cb5d7437f186994917fd86a2a330c21`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 03:27:19 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 03:27:19 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 03:27:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 03:27:21 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 03:27:21 GMT
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
	-	`sha256:49ff1670edc3c20a6a9614ecb3f794095053b0a2bc5c3d8a27ffb6771b4e8de5`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 5.1 MB (5070614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6bfbf28b1c962164432ab027c42dcb68debdd9c90fe50d3fdec0bac01a2a1b`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 1.2 MB (1198449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dec8839aa12d34c5fc6d220df303a7b58562c777e2281fb6b912cabcb3b808`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:ff608ed0346698200d108d948d192f9d9977f35b9ee6dba5dc437eecb95eff13
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74213050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3961610a4cc67151079da941b2fa3b5f9e84fdbadf7ddfc2345914f2e7d34270`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 02:38:42 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 02:38:43 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 02:38:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 02:38:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 02:38:44 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 02:38:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 02:38:47 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 02:38:48 GMT
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
	-	`sha256:189f1d64ec6387010de82030584f95d2f1cb77480534f720a6c8051e1c053202`  
		Last Modified: Wed, 07 Feb 2024 02:39:06 GMT  
		Size: 5.3 MB (5270668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439fb1dfa6333e4624dc554a68c980b15bda052268ac48be84e477697d3fa5fc`  
		Last Modified: Wed, 07 Feb 2024 02:39:05 GMT  
		Size: 1.2 MB (1186180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b46e2bfe6d57573d777ff909c837b014c894d5f5c65212804d738620cb252e2`  
		Last Modified: Wed, 07 Feb 2024 02:39:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - linux; s390x

```console
$ docker pull caddy@sha256:fad88c033e71179f3df4bf1a5b2e9d0d0264bcbaa498b911238fc07787bbace2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76100380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914aa8aec00e9a7014cfcc15953ecea9afcc02ceae16b98a5643c211c018e323`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 03:55:22 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 03:55:23 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 03:55:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 03:55:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 03:55:24 GMT
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
	-	`sha256:667df4a2c04946a51104abaa6f5ed310f5428e8423a5229c6a93e33a7bfd3afa`  
		Last Modified: Tue, 06 Feb 2024 22:15:10 GMT  
		Size: 66.2 MB (66217776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed37103477a46e4048ca49195fde1e764f57b71cb5abadd05970bee2e2f29cc`  
		Last Modified: Tue, 06 Feb 2024 22:14:59 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d511e031e1b91b289c43c1a2190ee22aa5f38fe22568e3b6e23cdf96db48b`  
		Last Modified: Wed, 07 Feb 2024 03:56:50 GMT  
		Size: 5.1 MB (5116980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255f032cffa62a5bea76ec237a6dfe24caf125994ad6151aed12f4ae30860c02`  
		Last Modified: Wed, 07 Feb 2024 03:56:50 GMT  
		Size: 1.3 MB (1262391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8b53fd06bb1ce493aa5cc33297d87b8edfe9fd834896df28185e9c3f9b8480`  
		Last Modified: Wed, 07 Feb 2024 03:56:49 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:f21fcacb51baed792b0310844331fa37b39b4235d5cbb8274b453b4abdbeb68b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2007478332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfd7236ef3ba33c49b0293ddeaed24ed8f1a4a4be50d73bb5daf279ed0d1067`
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
# Wed, 14 Feb 2024 20:43:58 GMT
ENV GOLANG_VERSION=1.21.7
# Wed, 14 Feb 2024 20:46:14 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:46:15 GMT
WORKDIR C:\go
# Wed, 14 Feb 2024 21:25:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:25:03 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 14 Feb 2024 21:25:04 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:25:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Feb 2024 21:25:28 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Feb 2024 21:25:29 GMT
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
	-	`sha256:6a320e20304175d59e4aee6ec77d02f07509c042e71352229d992e5a71178266`  
		Last Modified: Wed, 14 Feb 2024 21:00:19 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70d6b39cc331fef21be1e6e1e4f8a09002d3e8c2cbe5510f9b576f73a103a11`  
		Last Modified: Wed, 14 Feb 2024 21:00:38 GMT  
		Size: 69.3 MB (69339697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e925967ba6e0e9ec84f4892a901f9137d074b01da5967f3f02cca1d17c55401`  
		Last Modified: Wed, 14 Feb 2024 21:00:18 GMT  
		Size: 1.5 KB (1465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5be391477771ac6ef063dfff5f60c2bf3720c4c3e438914ad4f83d4186dd419`  
		Last Modified: Wed, 14 Feb 2024 21:27:15 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8040861524a92cd1ef40205f09edcc78fca950bc460c86dabddb5b7c9d207e1`  
		Last Modified: Wed, 14 Feb 2024 21:27:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146989057ff74f0c65231a30d9ae96ef9aca638ac186e5133ab6e62f60daa4e4`  
		Last Modified: Wed, 14 Feb 2024 21:27:13 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a1e9fdf12fec3886fbcf530321f59f401f9a8e9ca54deb5a50e1ef7035857c`  
		Last Modified: Wed, 14 Feb 2024 21:27:14 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f0b7658ba93600fbb3d46955c4030818eab0d9ee14ac0f2e17afd2728e1ea8`  
		Last Modified: Wed, 14 Feb 2024 21:27:14 GMT  
		Size: 1.7 MB (1666295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ffc354f7064866e9a01cd793241fe9fb0e6c82dc2388b1ed8ca9c0c70428b3`  
		Last Modified: Wed, 14 Feb 2024 21:27:13 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:536798cc04c493719ee143f8570a8ce2c06929deaefd229e15de08e0ad26d554
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2177347938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1022bc7754872a576d582646d52e18dcb896332104dc5ae6edbb3c7130f6fe10`
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
# Wed, 14 Feb 2024 20:46:27 GMT
ENV GOLANG_VERSION=1.21.7
# Wed, 14 Feb 2024 20:49:46 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:49:47 GMT
WORKDIR C:\go
# Wed, 14 Feb 2024 21:23:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:23:35 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 14 Feb 2024 21:23:36 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:23:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Feb 2024 21:24:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Feb 2024 21:24:54 GMT
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
	-	`sha256:fc4a495babb42867e41e9e0341672d9c3dc4342d7d1ca2089393548a9394712c`  
		Last Modified: Wed, 14 Feb 2024 21:00:48 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88628d70e4f0b09c4b4d93d847ecc1af2c6287a6ee7f2c02f8574d79323b7e94`  
		Last Modified: Wed, 14 Feb 2024 21:01:08 GMT  
		Size: 69.4 MB (69351914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9c7605984ae14daab7f947cbb370c489f648caa2436563473651ccbd225379`  
		Last Modified: Wed, 14 Feb 2024 21:00:48 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7d44e23d90802e1136be2c8be711e41683f02e6106a295dc7cc9e3567c3a79`  
		Last Modified: Wed, 14 Feb 2024 21:26:56 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b8bb132d080a4d6cdfdac7bc8d37ba32d8e594b8117bee0a7149d2e0e10a59`  
		Last Modified: Wed, 14 Feb 2024 21:26:54 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0da4afa5ca0ec4b0e5f6e0ba7198a70aebf33635612ae7f8538cd3b623178c`  
		Last Modified: Wed, 14 Feb 2024 21:26:53 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b40cba54a5386a0889184fc68012a0626b7585c728882c037f3c0778a0c5365`  
		Last Modified: Wed, 14 Feb 2024 21:26:54 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9a8a348cc99b33e0367f75baaa076f55305110bd2f991bf2ca49cdde949ea6`  
		Last Modified: Wed, 14 Feb 2024 21:26:54 GMT  
		Size: 1.7 MB (1683480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f900898726315c327700e5fd8845b66a9965afeafa8abbe836093c700afe897d`  
		Last Modified: Wed, 14 Feb 2024 21:26:53 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-alpine`

```console
$ docker pull caddy@sha256:33a92d10027f0a21785908d646f81c6c23b4abd130fc123200f00a9381693be9
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
$ docker pull caddy@sha256:8fee3614a6b6cabdab16312c9ec1062982ef3d655b99bcc8e983cbc777572fa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76972175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2decac0840cd748d459d2f76eebc64754108ee601a66e06fca48c6880efcdb02`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 20:10:42 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 20:10:42 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 20:10:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 20:10:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 20:10:43 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 20:10:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 20:10:44 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 20:10:44 GMT
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
	-	`sha256:d18ba8e8dd02491f11cea93df354c71628a2360674a625c205e213ef6fd82127`  
		Last Modified: Tue, 06 Feb 2024 23:56:58 GMT  
		Size: 67.0 MB (67009643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8daf023d266d667210cf5767c01f2f4f68e40c297e0bdecf73799744ddac1026`  
		Last Modified: Tue, 06 Feb 2024 23:56:47 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23298fdc181f9cc9b4b9e297a84c2ff9119ed9ccef7ee4188033e1e62b835a71`  
		Last Modified: Wed, 07 Feb 2024 20:11:02 GMT  
		Size: 5.0 MB (4972450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2716cf52013dbd506ec1fae43d30c4339d959e635e237a5f6b1e8311fba51b4a`  
		Last Modified: Wed, 07 Feb 2024 20:11:02 GMT  
		Size: 1.3 MB (1302239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1a06d10c122c1efe42b77b107513d80c320d5adadaeeaec6ffe0235d8738c1`  
		Last Modified: Wed, 07 Feb 2024 20:11:02 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:89493aa84b348e455d5d5d3dd0f050644d7e3a9400cdc1a09d07545d95e85fd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75415278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921e0138a2eb31837973f479ce9117ffd13a871b9e3c1e3332f0689b85ec2e5d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 07:28:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 07:28:02 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 07:28:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 07:28:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 07:28:03 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 07:28:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 07:28:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 07:28:04 GMT
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
	-	`sha256:fa53b2f66831ea2a6a71d6469b90663284dc2a4ce3cb48320dd55896f9cd8d84`  
		Last Modified: Tue, 06 Feb 2024 23:32:01 GMT  
		Size: 65.8 MB (65767452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6d1ac72f2f91d206a9c3fa198f2e45b1f18fcfd8da385ab8c5e3288262790`  
		Last Modified: Tue, 06 Feb 2024 23:31:47 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6fbc6c4773d705c6048f1330050fc6200a9ae262d156ab7492ac01fc483010`  
		Last Modified: Wed, 07 Feb 2024 07:28:17 GMT  
		Size: 5.0 MB (4966629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cdc84144fd70dfac8f705109ec0a92dc10a7dfc50838c6af32b442b918fcc6`  
		Last Modified: Wed, 07 Feb 2024 07:28:17 GMT  
		Size: 1.2 MB (1248656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78e6ef661fee931920aa3236f1af661d851378c52b31aa87ffc8558da5e48a5`  
		Last Modified: Wed, 07 Feb 2024 07:28:16 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ff0b3bb63b15b33debf9aea993bd84f4b246b7c7d4484db77832556ef074ca51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c07a4329692996a3988717e0eba3652501b15f09abc9597e4ad3b87250cb63d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 02:48:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 02:48:33 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 02:48:33 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 02:48:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 02:48:34 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 02:48:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 02:48:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 02:48:38 GMT
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
	-	`sha256:7113cf104f60011eb6444102f15ef72cdd45fcb4c9caf77828b5fbc38dab492e`  
		Last Modified: Wed, 07 Feb 2024 02:23:31 GMT  
		Size: 65.8 MB (65767658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a6e0f5354f83f214823ce1d03ea8a7eab56425405c4ca69940f2f3dde97a80`  
		Last Modified: Wed, 07 Feb 2024 02:23:15 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f390b29274db9c266f41d8708269d5dda362068060acd663c445ce335597d742`  
		Last Modified: Wed, 07 Feb 2024 02:49:00 GMT  
		Size: 4.5 MB (4514221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399e806721f760b662ba77d6b0d28a03a0c91cfb57e9d60a85f9016392605507`  
		Last Modified: Wed, 07 Feb 2024 02:48:59 GMT  
		Size: 1.2 MB (1246089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5225c4821fb8eb5d3c9024e1b8b00504669f1ced491c2e93b97b5400673970c2`  
		Last Modified: Wed, 07 Feb 2024 02:48:59 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:bee0d79c6d83f0f253201d3c21afebe471923903c79a57fc165382018992582b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73998590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43afba92f6c2f26ccd2d5a34a29409424cb5d7437f186994917fd86a2a330c21`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 03:27:19 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 03:27:19 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 03:27:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 03:27:21 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 03:27:21 GMT
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
	-	`sha256:49ff1670edc3c20a6a9614ecb3f794095053b0a2bc5c3d8a27ffb6771b4e8de5`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 5.1 MB (5070614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6bfbf28b1c962164432ab027c42dcb68debdd9c90fe50d3fdec0bac01a2a1b`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 1.2 MB (1198449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dec8839aa12d34c5fc6d220df303a7b58562c777e2281fb6b912cabcb3b808`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:ff608ed0346698200d108d948d192f9d9977f35b9ee6dba5dc437eecb95eff13
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74213050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3961610a4cc67151079da941b2fa3b5f9e84fdbadf7ddfc2345914f2e7d34270`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 02:38:42 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 02:38:43 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 02:38:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 02:38:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 02:38:44 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 02:38:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 02:38:47 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 02:38:48 GMT
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
	-	`sha256:189f1d64ec6387010de82030584f95d2f1cb77480534f720a6c8051e1c053202`  
		Last Modified: Wed, 07 Feb 2024 02:39:06 GMT  
		Size: 5.3 MB (5270668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439fb1dfa6333e4624dc554a68c980b15bda052268ac48be84e477697d3fa5fc`  
		Last Modified: Wed, 07 Feb 2024 02:39:05 GMT  
		Size: 1.2 MB (1186180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b46e2bfe6d57573d777ff909c837b014c894d5f5c65212804d738620cb252e2`  
		Last Modified: Wed, 07 Feb 2024 02:39:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:fad88c033e71179f3df4bf1a5b2e9d0d0264bcbaa498b911238fc07787bbace2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76100380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914aa8aec00e9a7014cfcc15953ecea9afcc02ceae16b98a5643c211c018e323`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 03:55:22 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 03:55:23 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 03:55:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 03:55:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 03:55:24 GMT
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
	-	`sha256:667df4a2c04946a51104abaa6f5ed310f5428e8423a5229c6a93e33a7bfd3afa`  
		Last Modified: Tue, 06 Feb 2024 22:15:10 GMT  
		Size: 66.2 MB (66217776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed37103477a46e4048ca49195fde1e764f57b71cb5abadd05970bee2e2f29cc`  
		Last Modified: Tue, 06 Feb 2024 22:14:59 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d511e031e1b91b289c43c1a2190ee22aa5f38fe22568e3b6e23cdf96db48b`  
		Last Modified: Wed, 07 Feb 2024 03:56:50 GMT  
		Size: 5.1 MB (5116980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255f032cffa62a5bea76ec237a6dfe24caf125994ad6151aed12f4ae30860c02`  
		Last Modified: Wed, 07 Feb 2024 03:56:50 GMT  
		Size: 1.3 MB (1262391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8b53fd06bb1ce493aa5cc33297d87b8edfe9fd834896df28185e9c3f9b8480`  
		Last Modified: Wed, 07 Feb 2024 03:56:49 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:3f8db6e8a2fe203d75df858bb7930fe4be2c30c957a28c2bcf5c21302a39c66d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `caddy:2.7-builder-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:536798cc04c493719ee143f8570a8ce2c06929deaefd229e15de08e0ad26d554
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2177347938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1022bc7754872a576d582646d52e18dcb896332104dc5ae6edbb3c7130f6fe10`
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
# Wed, 14 Feb 2024 20:46:27 GMT
ENV GOLANG_VERSION=1.21.7
# Wed, 14 Feb 2024 20:49:46 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:49:47 GMT
WORKDIR C:\go
# Wed, 14 Feb 2024 21:23:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:23:35 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 14 Feb 2024 21:23:36 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:23:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Feb 2024 21:24:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Feb 2024 21:24:54 GMT
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
	-	`sha256:fc4a495babb42867e41e9e0341672d9c3dc4342d7d1ca2089393548a9394712c`  
		Last Modified: Wed, 14 Feb 2024 21:00:48 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88628d70e4f0b09c4b4d93d847ecc1af2c6287a6ee7f2c02f8574d79323b7e94`  
		Last Modified: Wed, 14 Feb 2024 21:01:08 GMT  
		Size: 69.4 MB (69351914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9c7605984ae14daab7f947cbb370c489f648caa2436563473651ccbd225379`  
		Last Modified: Wed, 14 Feb 2024 21:00:48 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7d44e23d90802e1136be2c8be711e41683f02e6106a295dc7cc9e3567c3a79`  
		Last Modified: Wed, 14 Feb 2024 21:26:56 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b8bb132d080a4d6cdfdac7bc8d37ba32d8e594b8117bee0a7149d2e0e10a59`  
		Last Modified: Wed, 14 Feb 2024 21:26:54 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0da4afa5ca0ec4b0e5f6e0ba7198a70aebf33635612ae7f8538cd3b623178c`  
		Last Modified: Wed, 14 Feb 2024 21:26:53 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b40cba54a5386a0889184fc68012a0626b7585c728882c037f3c0778a0c5365`  
		Last Modified: Wed, 14 Feb 2024 21:26:54 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9a8a348cc99b33e0367f75baaa076f55305110bd2f991bf2ca49cdde949ea6`  
		Last Modified: Wed, 14 Feb 2024 21:26:54 GMT  
		Size: 1.7 MB (1683480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f900898726315c327700e5fd8845b66a9965afeafa8abbe836093c700afe897d`  
		Last Modified: Wed, 14 Feb 2024 21:26:53 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:c902b48fcec4254e6ed5eeb752b75d08e42bbd1bbd67398e45da91dcfa46a841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `caddy:2.7-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:f21fcacb51baed792b0310844331fa37b39b4235d5cbb8274b453b4abdbeb68b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2007478332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfd7236ef3ba33c49b0293ddeaed24ed8f1a4a4be50d73bb5daf279ed0d1067`
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
# Wed, 14 Feb 2024 20:43:58 GMT
ENV GOLANG_VERSION=1.21.7
# Wed, 14 Feb 2024 20:46:14 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:46:15 GMT
WORKDIR C:\go
# Wed, 14 Feb 2024 21:25:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:25:03 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 14 Feb 2024 21:25:04 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:25:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Feb 2024 21:25:28 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Feb 2024 21:25:29 GMT
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
	-	`sha256:6a320e20304175d59e4aee6ec77d02f07509c042e71352229d992e5a71178266`  
		Last Modified: Wed, 14 Feb 2024 21:00:19 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70d6b39cc331fef21be1e6e1e4f8a09002d3e8c2cbe5510f9b576f73a103a11`  
		Last Modified: Wed, 14 Feb 2024 21:00:38 GMT  
		Size: 69.3 MB (69339697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e925967ba6e0e9ec84f4892a901f9137d074b01da5967f3f02cca1d17c55401`  
		Last Modified: Wed, 14 Feb 2024 21:00:18 GMT  
		Size: 1.5 KB (1465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5be391477771ac6ef063dfff5f60c2bf3720c4c3e438914ad4f83d4186dd419`  
		Last Modified: Wed, 14 Feb 2024 21:27:15 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8040861524a92cd1ef40205f09edcc78fca950bc460c86dabddb5b7c9d207e1`  
		Last Modified: Wed, 14 Feb 2024 21:27:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146989057ff74f0c65231a30d9ae96ef9aca638ac186e5133ab6e62f60daa4e4`  
		Last Modified: Wed, 14 Feb 2024 21:27:13 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a1e9fdf12fec3886fbcf530321f59f401f9a8e9ca54deb5a50e1ef7035857c`  
		Last Modified: Wed, 14 Feb 2024 21:27:14 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f0b7658ba93600fbb3d46955c4030818eab0d9ee14ac0f2e17afd2728e1ea8`  
		Last Modified: Wed, 14 Feb 2024 21:27:14 GMT  
		Size: 1.7 MB (1666295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ffc354f7064866e9a01cd793241fe9fb0e6c82dc2388b1ed8ca9c0c70428b3`  
		Last Modified: Wed, 14 Feb 2024 21:27:13 GMT  
		Size: 1.3 KB (1320 bytes)  
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
$ docker pull caddy@sha256:52b96e26a80a1694b7195f1be152643f7a27b85d1b809e38f7b4d2def10a03a1
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
$ docker pull caddy@sha256:8fee3614a6b6cabdab16312c9ec1062982ef3d655b99bcc8e983cbc777572fa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76972175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2decac0840cd748d459d2f76eebc64754108ee601a66e06fca48c6880efcdb02`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 20:10:42 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 20:10:42 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 20:10:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 20:10:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 20:10:43 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 20:10:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 20:10:44 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 20:10:44 GMT
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
	-	`sha256:d18ba8e8dd02491f11cea93df354c71628a2360674a625c205e213ef6fd82127`  
		Last Modified: Tue, 06 Feb 2024 23:56:58 GMT  
		Size: 67.0 MB (67009643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8daf023d266d667210cf5767c01f2f4f68e40c297e0bdecf73799744ddac1026`  
		Last Modified: Tue, 06 Feb 2024 23:56:47 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23298fdc181f9cc9b4b9e297a84c2ff9119ed9ccef7ee4188033e1e62b835a71`  
		Last Modified: Wed, 07 Feb 2024 20:11:02 GMT  
		Size: 5.0 MB (4972450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2716cf52013dbd506ec1fae43d30c4339d959e635e237a5f6b1e8311fba51b4a`  
		Last Modified: Wed, 07 Feb 2024 20:11:02 GMT  
		Size: 1.3 MB (1302239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1a06d10c122c1efe42b77b107513d80c320d5adadaeeaec6ffe0235d8738c1`  
		Last Modified: Wed, 07 Feb 2024 20:11:02 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:89493aa84b348e455d5d5d3dd0f050644d7e3a9400cdc1a09d07545d95e85fd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75415278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921e0138a2eb31837973f479ce9117ffd13a871b9e3c1e3332f0689b85ec2e5d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 07:28:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 07:28:02 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 07:28:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 07:28:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 07:28:03 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 07:28:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 07:28:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 07:28:04 GMT
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
	-	`sha256:fa53b2f66831ea2a6a71d6469b90663284dc2a4ce3cb48320dd55896f9cd8d84`  
		Last Modified: Tue, 06 Feb 2024 23:32:01 GMT  
		Size: 65.8 MB (65767452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6d1ac72f2f91d206a9c3fa198f2e45b1f18fcfd8da385ab8c5e3288262790`  
		Last Modified: Tue, 06 Feb 2024 23:31:47 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6fbc6c4773d705c6048f1330050fc6200a9ae262d156ab7492ac01fc483010`  
		Last Modified: Wed, 07 Feb 2024 07:28:17 GMT  
		Size: 5.0 MB (4966629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cdc84144fd70dfac8f705109ec0a92dc10a7dfc50838c6af32b442b918fcc6`  
		Last Modified: Wed, 07 Feb 2024 07:28:17 GMT  
		Size: 1.2 MB (1248656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78e6ef661fee931920aa3236f1af661d851378c52b31aa87ffc8558da5e48a5`  
		Last Modified: Wed, 07 Feb 2024 07:28:16 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ff0b3bb63b15b33debf9aea993bd84f4b246b7c7d4484db77832556ef074ca51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c07a4329692996a3988717e0eba3652501b15f09abc9597e4ad3b87250cb63d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 02:48:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 02:48:33 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 02:48:33 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 02:48:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 02:48:34 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 02:48:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 02:48:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 02:48:38 GMT
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
	-	`sha256:7113cf104f60011eb6444102f15ef72cdd45fcb4c9caf77828b5fbc38dab492e`  
		Last Modified: Wed, 07 Feb 2024 02:23:31 GMT  
		Size: 65.8 MB (65767658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a6e0f5354f83f214823ce1d03ea8a7eab56425405c4ca69940f2f3dde97a80`  
		Last Modified: Wed, 07 Feb 2024 02:23:15 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f390b29274db9c266f41d8708269d5dda362068060acd663c445ce335597d742`  
		Last Modified: Wed, 07 Feb 2024 02:49:00 GMT  
		Size: 4.5 MB (4514221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399e806721f760b662ba77d6b0d28a03a0c91cfb57e9d60a85f9016392605507`  
		Last Modified: Wed, 07 Feb 2024 02:48:59 GMT  
		Size: 1.2 MB (1246089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5225c4821fb8eb5d3c9024e1b8b00504669f1ced491c2e93b97b5400673970c2`  
		Last Modified: Wed, 07 Feb 2024 02:48:59 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:bee0d79c6d83f0f253201d3c21afebe471923903c79a57fc165382018992582b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73998590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43afba92f6c2f26ccd2d5a34a29409424cb5d7437f186994917fd86a2a330c21`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 03:27:19 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 03:27:19 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 03:27:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 03:27:21 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 03:27:21 GMT
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
	-	`sha256:49ff1670edc3c20a6a9614ecb3f794095053b0a2bc5c3d8a27ffb6771b4e8de5`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 5.1 MB (5070614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6bfbf28b1c962164432ab027c42dcb68debdd9c90fe50d3fdec0bac01a2a1b`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 1.2 MB (1198449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dec8839aa12d34c5fc6d220df303a7b58562c777e2281fb6b912cabcb3b808`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:ff608ed0346698200d108d948d192f9d9977f35b9ee6dba5dc437eecb95eff13
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74213050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3961610a4cc67151079da941b2fa3b5f9e84fdbadf7ddfc2345914f2e7d34270`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 02:38:42 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 02:38:43 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 02:38:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 02:38:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 02:38:44 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 02:38:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 02:38:47 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 02:38:48 GMT
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
	-	`sha256:189f1d64ec6387010de82030584f95d2f1cb77480534f720a6c8051e1c053202`  
		Last Modified: Wed, 07 Feb 2024 02:39:06 GMT  
		Size: 5.3 MB (5270668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439fb1dfa6333e4624dc554a68c980b15bda052268ac48be84e477697d3fa5fc`  
		Last Modified: Wed, 07 Feb 2024 02:39:05 GMT  
		Size: 1.2 MB (1186180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b46e2bfe6d57573d777ff909c837b014c894d5f5c65212804d738620cb252e2`  
		Last Modified: Wed, 07 Feb 2024 02:39:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - linux; s390x

```console
$ docker pull caddy@sha256:fad88c033e71179f3df4bf1a5b2e9d0d0264bcbaa498b911238fc07787bbace2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76100380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914aa8aec00e9a7014cfcc15953ecea9afcc02ceae16b98a5643c211c018e323`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 03:55:22 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 03:55:23 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 03:55:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 03:55:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 03:55:24 GMT
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
	-	`sha256:667df4a2c04946a51104abaa6f5ed310f5428e8423a5229c6a93e33a7bfd3afa`  
		Last Modified: Tue, 06 Feb 2024 22:15:10 GMT  
		Size: 66.2 MB (66217776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed37103477a46e4048ca49195fde1e764f57b71cb5abadd05970bee2e2f29cc`  
		Last Modified: Tue, 06 Feb 2024 22:14:59 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d511e031e1b91b289c43c1a2190ee22aa5f38fe22568e3b6e23cdf96db48b`  
		Last Modified: Wed, 07 Feb 2024 03:56:50 GMT  
		Size: 5.1 MB (5116980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255f032cffa62a5bea76ec237a6dfe24caf125994ad6151aed12f4ae30860c02`  
		Last Modified: Wed, 07 Feb 2024 03:56:50 GMT  
		Size: 1.3 MB (1262391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8b53fd06bb1ce493aa5cc33297d87b8edfe9fd834896df28185e9c3f9b8480`  
		Last Modified: Wed, 07 Feb 2024 03:56:49 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:f21fcacb51baed792b0310844331fa37b39b4235d5cbb8274b453b4abdbeb68b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2007478332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfd7236ef3ba33c49b0293ddeaed24ed8f1a4a4be50d73bb5daf279ed0d1067`
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
# Wed, 14 Feb 2024 20:43:58 GMT
ENV GOLANG_VERSION=1.21.7
# Wed, 14 Feb 2024 20:46:14 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:46:15 GMT
WORKDIR C:\go
# Wed, 14 Feb 2024 21:25:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:25:03 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 14 Feb 2024 21:25:04 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:25:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Feb 2024 21:25:28 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Feb 2024 21:25:29 GMT
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
	-	`sha256:6a320e20304175d59e4aee6ec77d02f07509c042e71352229d992e5a71178266`  
		Last Modified: Wed, 14 Feb 2024 21:00:19 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70d6b39cc331fef21be1e6e1e4f8a09002d3e8c2cbe5510f9b576f73a103a11`  
		Last Modified: Wed, 14 Feb 2024 21:00:38 GMT  
		Size: 69.3 MB (69339697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e925967ba6e0e9ec84f4892a901f9137d074b01da5967f3f02cca1d17c55401`  
		Last Modified: Wed, 14 Feb 2024 21:00:18 GMT  
		Size: 1.5 KB (1465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5be391477771ac6ef063dfff5f60c2bf3720c4c3e438914ad4f83d4186dd419`  
		Last Modified: Wed, 14 Feb 2024 21:27:15 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8040861524a92cd1ef40205f09edcc78fca950bc460c86dabddb5b7c9d207e1`  
		Last Modified: Wed, 14 Feb 2024 21:27:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146989057ff74f0c65231a30d9ae96ef9aca638ac186e5133ab6e62f60daa4e4`  
		Last Modified: Wed, 14 Feb 2024 21:27:13 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a1e9fdf12fec3886fbcf530321f59f401f9a8e9ca54deb5a50e1ef7035857c`  
		Last Modified: Wed, 14 Feb 2024 21:27:14 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f0b7658ba93600fbb3d46955c4030818eab0d9ee14ac0f2e17afd2728e1ea8`  
		Last Modified: Wed, 14 Feb 2024 21:27:14 GMT  
		Size: 1.7 MB (1666295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ffc354f7064866e9a01cd793241fe9fb0e6c82dc2388b1ed8ca9c0c70428b3`  
		Last Modified: Wed, 14 Feb 2024 21:27:13 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:536798cc04c493719ee143f8570a8ce2c06929deaefd229e15de08e0ad26d554
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2177347938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1022bc7754872a576d582646d52e18dcb896332104dc5ae6edbb3c7130f6fe10`
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
# Wed, 14 Feb 2024 20:46:27 GMT
ENV GOLANG_VERSION=1.21.7
# Wed, 14 Feb 2024 20:49:46 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:49:47 GMT
WORKDIR C:\go
# Wed, 14 Feb 2024 21:23:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:23:35 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 14 Feb 2024 21:23:36 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:23:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Feb 2024 21:24:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Feb 2024 21:24:54 GMT
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
	-	`sha256:fc4a495babb42867e41e9e0341672d9c3dc4342d7d1ca2089393548a9394712c`  
		Last Modified: Wed, 14 Feb 2024 21:00:48 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88628d70e4f0b09c4b4d93d847ecc1af2c6287a6ee7f2c02f8574d79323b7e94`  
		Last Modified: Wed, 14 Feb 2024 21:01:08 GMT  
		Size: 69.4 MB (69351914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9c7605984ae14daab7f947cbb370c489f648caa2436563473651ccbd225379`  
		Last Modified: Wed, 14 Feb 2024 21:00:48 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7d44e23d90802e1136be2c8be711e41683f02e6106a295dc7cc9e3567c3a79`  
		Last Modified: Wed, 14 Feb 2024 21:26:56 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b8bb132d080a4d6cdfdac7bc8d37ba32d8e594b8117bee0a7149d2e0e10a59`  
		Last Modified: Wed, 14 Feb 2024 21:26:54 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0da4afa5ca0ec4b0e5f6e0ba7198a70aebf33635612ae7f8538cd3b623178c`  
		Last Modified: Wed, 14 Feb 2024 21:26:53 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b40cba54a5386a0889184fc68012a0626b7585c728882c037f3c0778a0c5365`  
		Last Modified: Wed, 14 Feb 2024 21:26:54 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9a8a348cc99b33e0367f75baaa076f55305110bd2f991bf2ca49cdde949ea6`  
		Last Modified: Wed, 14 Feb 2024 21:26:54 GMT  
		Size: 1.7 MB (1683480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f900898726315c327700e5fd8845b66a9965afeafa8abbe836093c700afe897d`  
		Last Modified: Wed, 14 Feb 2024 21:26:53 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder-alpine`

```console
$ docker pull caddy@sha256:33a92d10027f0a21785908d646f81c6c23b4abd130fc123200f00a9381693be9
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
$ docker pull caddy@sha256:8fee3614a6b6cabdab16312c9ec1062982ef3d655b99bcc8e983cbc777572fa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76972175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2decac0840cd748d459d2f76eebc64754108ee601a66e06fca48c6880efcdb02`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 20:10:42 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 20:10:42 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 20:10:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 20:10:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 20:10:43 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 20:10:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 20:10:44 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 20:10:44 GMT
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
	-	`sha256:d18ba8e8dd02491f11cea93df354c71628a2360674a625c205e213ef6fd82127`  
		Last Modified: Tue, 06 Feb 2024 23:56:58 GMT  
		Size: 67.0 MB (67009643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8daf023d266d667210cf5767c01f2f4f68e40c297e0bdecf73799744ddac1026`  
		Last Modified: Tue, 06 Feb 2024 23:56:47 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23298fdc181f9cc9b4b9e297a84c2ff9119ed9ccef7ee4188033e1e62b835a71`  
		Last Modified: Wed, 07 Feb 2024 20:11:02 GMT  
		Size: 5.0 MB (4972450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2716cf52013dbd506ec1fae43d30c4339d959e635e237a5f6b1e8311fba51b4a`  
		Last Modified: Wed, 07 Feb 2024 20:11:02 GMT  
		Size: 1.3 MB (1302239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1a06d10c122c1efe42b77b107513d80c320d5adadaeeaec6ffe0235d8738c1`  
		Last Modified: Wed, 07 Feb 2024 20:11:02 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:89493aa84b348e455d5d5d3dd0f050644d7e3a9400cdc1a09d07545d95e85fd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75415278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921e0138a2eb31837973f479ce9117ffd13a871b9e3c1e3332f0689b85ec2e5d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 07:28:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 07:28:02 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 07:28:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 07:28:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 07:28:03 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 07:28:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 07:28:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 07:28:04 GMT
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
	-	`sha256:fa53b2f66831ea2a6a71d6469b90663284dc2a4ce3cb48320dd55896f9cd8d84`  
		Last Modified: Tue, 06 Feb 2024 23:32:01 GMT  
		Size: 65.8 MB (65767452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6d1ac72f2f91d206a9c3fa198f2e45b1f18fcfd8da385ab8c5e3288262790`  
		Last Modified: Tue, 06 Feb 2024 23:31:47 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6fbc6c4773d705c6048f1330050fc6200a9ae262d156ab7492ac01fc483010`  
		Last Modified: Wed, 07 Feb 2024 07:28:17 GMT  
		Size: 5.0 MB (4966629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cdc84144fd70dfac8f705109ec0a92dc10a7dfc50838c6af32b442b918fcc6`  
		Last Modified: Wed, 07 Feb 2024 07:28:17 GMT  
		Size: 1.2 MB (1248656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78e6ef661fee931920aa3236f1af661d851378c52b31aa87ffc8558da5e48a5`  
		Last Modified: Wed, 07 Feb 2024 07:28:16 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ff0b3bb63b15b33debf9aea993bd84f4b246b7c7d4484db77832556ef074ca51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c07a4329692996a3988717e0eba3652501b15f09abc9597e4ad3b87250cb63d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 02:48:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 02:48:33 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 02:48:33 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 02:48:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 02:48:34 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 02:48:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 02:48:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 02:48:38 GMT
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
	-	`sha256:7113cf104f60011eb6444102f15ef72cdd45fcb4c9caf77828b5fbc38dab492e`  
		Last Modified: Wed, 07 Feb 2024 02:23:31 GMT  
		Size: 65.8 MB (65767658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a6e0f5354f83f214823ce1d03ea8a7eab56425405c4ca69940f2f3dde97a80`  
		Last Modified: Wed, 07 Feb 2024 02:23:15 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f390b29274db9c266f41d8708269d5dda362068060acd663c445ce335597d742`  
		Last Modified: Wed, 07 Feb 2024 02:49:00 GMT  
		Size: 4.5 MB (4514221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399e806721f760b662ba77d6b0d28a03a0c91cfb57e9d60a85f9016392605507`  
		Last Modified: Wed, 07 Feb 2024 02:48:59 GMT  
		Size: 1.2 MB (1246089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5225c4821fb8eb5d3c9024e1b8b00504669f1ced491c2e93b97b5400673970c2`  
		Last Modified: Wed, 07 Feb 2024 02:48:59 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:bee0d79c6d83f0f253201d3c21afebe471923903c79a57fc165382018992582b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73998590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43afba92f6c2f26ccd2d5a34a29409424cb5d7437f186994917fd86a2a330c21`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 03:27:19 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 03:27:19 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 03:27:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 03:27:21 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 03:27:21 GMT
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
	-	`sha256:49ff1670edc3c20a6a9614ecb3f794095053b0a2bc5c3d8a27ffb6771b4e8de5`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 5.1 MB (5070614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6bfbf28b1c962164432ab027c42dcb68debdd9c90fe50d3fdec0bac01a2a1b`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 1.2 MB (1198449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dec8839aa12d34c5fc6d220df303a7b58562c777e2281fb6b912cabcb3b808`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:ff608ed0346698200d108d948d192f9d9977f35b9ee6dba5dc437eecb95eff13
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74213050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3961610a4cc67151079da941b2fa3b5f9e84fdbadf7ddfc2345914f2e7d34270`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 02:38:42 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 02:38:43 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 02:38:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 02:38:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 02:38:44 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 02:38:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 02:38:47 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 02:38:48 GMT
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
	-	`sha256:189f1d64ec6387010de82030584f95d2f1cb77480534f720a6c8051e1c053202`  
		Last Modified: Wed, 07 Feb 2024 02:39:06 GMT  
		Size: 5.3 MB (5270668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439fb1dfa6333e4624dc554a68c980b15bda052268ac48be84e477697d3fa5fc`  
		Last Modified: Wed, 07 Feb 2024 02:39:05 GMT  
		Size: 1.2 MB (1186180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b46e2bfe6d57573d777ff909c837b014c894d5f5c65212804d738620cb252e2`  
		Last Modified: Wed, 07 Feb 2024 02:39:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2.7.6-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:fad88c033e71179f3df4bf1a5b2e9d0d0264bcbaa498b911238fc07787bbace2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76100380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914aa8aec00e9a7014cfcc15953ecea9afcc02ceae16b98a5643c211c018e323`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 03:55:22 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 03:55:23 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 03:55:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 03:55:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 03:55:24 GMT
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
	-	`sha256:667df4a2c04946a51104abaa6f5ed310f5428e8423a5229c6a93e33a7bfd3afa`  
		Last Modified: Tue, 06 Feb 2024 22:15:10 GMT  
		Size: 66.2 MB (66217776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed37103477a46e4048ca49195fde1e764f57b71cb5abadd05970bee2e2f29cc`  
		Last Modified: Tue, 06 Feb 2024 22:14:59 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d511e031e1b91b289c43c1a2190ee22aa5f38fe22568e3b6e23cdf96db48b`  
		Last Modified: Wed, 07 Feb 2024 03:56:50 GMT  
		Size: 5.1 MB (5116980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255f032cffa62a5bea76ec237a6dfe24caf125994ad6151aed12f4ae30860c02`  
		Last Modified: Wed, 07 Feb 2024 03:56:50 GMT  
		Size: 1.3 MB (1262391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8b53fd06bb1ce493aa5cc33297d87b8edfe9fd834896df28185e9c3f9b8480`  
		Last Modified: Wed, 07 Feb 2024 03:56:49 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:3f8db6e8a2fe203d75df858bb7930fe4be2c30c957a28c2bcf5c21302a39c66d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `caddy:2.7.6-builder-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:536798cc04c493719ee143f8570a8ce2c06929deaefd229e15de08e0ad26d554
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2177347938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1022bc7754872a576d582646d52e18dcb896332104dc5ae6edbb3c7130f6fe10`
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
# Wed, 14 Feb 2024 20:46:27 GMT
ENV GOLANG_VERSION=1.21.7
# Wed, 14 Feb 2024 20:49:46 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:49:47 GMT
WORKDIR C:\go
# Wed, 14 Feb 2024 21:23:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:23:35 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 14 Feb 2024 21:23:36 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:23:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Feb 2024 21:24:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Feb 2024 21:24:54 GMT
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
	-	`sha256:fc4a495babb42867e41e9e0341672d9c3dc4342d7d1ca2089393548a9394712c`  
		Last Modified: Wed, 14 Feb 2024 21:00:48 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88628d70e4f0b09c4b4d93d847ecc1af2c6287a6ee7f2c02f8574d79323b7e94`  
		Last Modified: Wed, 14 Feb 2024 21:01:08 GMT  
		Size: 69.4 MB (69351914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9c7605984ae14daab7f947cbb370c489f648caa2436563473651ccbd225379`  
		Last Modified: Wed, 14 Feb 2024 21:00:48 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7d44e23d90802e1136be2c8be711e41683f02e6106a295dc7cc9e3567c3a79`  
		Last Modified: Wed, 14 Feb 2024 21:26:56 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b8bb132d080a4d6cdfdac7bc8d37ba32d8e594b8117bee0a7149d2e0e10a59`  
		Last Modified: Wed, 14 Feb 2024 21:26:54 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0da4afa5ca0ec4b0e5f6e0ba7198a70aebf33635612ae7f8538cd3b623178c`  
		Last Modified: Wed, 14 Feb 2024 21:26:53 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b40cba54a5386a0889184fc68012a0626b7585c728882c037f3c0778a0c5365`  
		Last Modified: Wed, 14 Feb 2024 21:26:54 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9a8a348cc99b33e0367f75baaa076f55305110bd2f991bf2ca49cdde949ea6`  
		Last Modified: Wed, 14 Feb 2024 21:26:54 GMT  
		Size: 1.7 MB (1683480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f900898726315c327700e5fd8845b66a9965afeafa8abbe836093c700afe897d`  
		Last Modified: Wed, 14 Feb 2024 21:26:53 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:2.7.6-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:c902b48fcec4254e6ed5eeb752b75d08e42bbd1bbd67398e45da91dcfa46a841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `caddy:2.7.6-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:f21fcacb51baed792b0310844331fa37b39b4235d5cbb8274b453b4abdbeb68b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2007478332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfd7236ef3ba33c49b0293ddeaed24ed8f1a4a4be50d73bb5daf279ed0d1067`
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
# Wed, 14 Feb 2024 20:43:58 GMT
ENV GOLANG_VERSION=1.21.7
# Wed, 14 Feb 2024 20:46:14 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:46:15 GMT
WORKDIR C:\go
# Wed, 14 Feb 2024 21:25:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:25:03 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 14 Feb 2024 21:25:04 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:25:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Feb 2024 21:25:28 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Feb 2024 21:25:29 GMT
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
	-	`sha256:6a320e20304175d59e4aee6ec77d02f07509c042e71352229d992e5a71178266`  
		Last Modified: Wed, 14 Feb 2024 21:00:19 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70d6b39cc331fef21be1e6e1e4f8a09002d3e8c2cbe5510f9b576f73a103a11`  
		Last Modified: Wed, 14 Feb 2024 21:00:38 GMT  
		Size: 69.3 MB (69339697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e925967ba6e0e9ec84f4892a901f9137d074b01da5967f3f02cca1d17c55401`  
		Last Modified: Wed, 14 Feb 2024 21:00:18 GMT  
		Size: 1.5 KB (1465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5be391477771ac6ef063dfff5f60c2bf3720c4c3e438914ad4f83d4186dd419`  
		Last Modified: Wed, 14 Feb 2024 21:27:15 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8040861524a92cd1ef40205f09edcc78fca950bc460c86dabddb5b7c9d207e1`  
		Last Modified: Wed, 14 Feb 2024 21:27:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146989057ff74f0c65231a30d9ae96ef9aca638ac186e5133ab6e62f60daa4e4`  
		Last Modified: Wed, 14 Feb 2024 21:27:13 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a1e9fdf12fec3886fbcf530321f59f401f9a8e9ca54deb5a50e1ef7035857c`  
		Last Modified: Wed, 14 Feb 2024 21:27:14 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f0b7658ba93600fbb3d46955c4030818eab0d9ee14ac0f2e17afd2728e1ea8`  
		Last Modified: Wed, 14 Feb 2024 21:27:14 GMT  
		Size: 1.7 MB (1666295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ffc354f7064866e9a01cd793241fe9fb0e6c82dc2388b1ed8ca9c0c70428b3`  
		Last Modified: Wed, 14 Feb 2024 21:27:13 GMT  
		Size: 1.3 KB (1320 bytes)  
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
$ docker pull caddy@sha256:52b96e26a80a1694b7195f1be152643f7a27b85d1b809e38f7b4d2def10a03a1
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
$ docker pull caddy@sha256:8fee3614a6b6cabdab16312c9ec1062982ef3d655b99bcc8e983cbc777572fa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76972175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2decac0840cd748d459d2f76eebc64754108ee601a66e06fca48c6880efcdb02`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 20:10:42 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 20:10:42 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 20:10:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 20:10:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 20:10:43 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 20:10:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 20:10:44 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 20:10:44 GMT
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
	-	`sha256:d18ba8e8dd02491f11cea93df354c71628a2360674a625c205e213ef6fd82127`  
		Last Modified: Tue, 06 Feb 2024 23:56:58 GMT  
		Size: 67.0 MB (67009643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8daf023d266d667210cf5767c01f2f4f68e40c297e0bdecf73799744ddac1026`  
		Last Modified: Tue, 06 Feb 2024 23:56:47 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23298fdc181f9cc9b4b9e297a84c2ff9119ed9ccef7ee4188033e1e62b835a71`  
		Last Modified: Wed, 07 Feb 2024 20:11:02 GMT  
		Size: 5.0 MB (4972450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2716cf52013dbd506ec1fae43d30c4339d959e635e237a5f6b1e8311fba51b4a`  
		Last Modified: Wed, 07 Feb 2024 20:11:02 GMT  
		Size: 1.3 MB (1302239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1a06d10c122c1efe42b77b107513d80c320d5adadaeeaec6ffe0235d8738c1`  
		Last Modified: Wed, 07 Feb 2024 20:11:02 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:89493aa84b348e455d5d5d3dd0f050644d7e3a9400cdc1a09d07545d95e85fd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75415278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921e0138a2eb31837973f479ce9117ffd13a871b9e3c1e3332f0689b85ec2e5d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 07:28:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 07:28:02 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 07:28:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 07:28:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 07:28:03 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 07:28:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 07:28:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 07:28:04 GMT
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
	-	`sha256:fa53b2f66831ea2a6a71d6469b90663284dc2a4ce3cb48320dd55896f9cd8d84`  
		Last Modified: Tue, 06 Feb 2024 23:32:01 GMT  
		Size: 65.8 MB (65767452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6d1ac72f2f91d206a9c3fa198f2e45b1f18fcfd8da385ab8c5e3288262790`  
		Last Modified: Tue, 06 Feb 2024 23:31:47 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6fbc6c4773d705c6048f1330050fc6200a9ae262d156ab7492ac01fc483010`  
		Last Modified: Wed, 07 Feb 2024 07:28:17 GMT  
		Size: 5.0 MB (4966629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cdc84144fd70dfac8f705109ec0a92dc10a7dfc50838c6af32b442b918fcc6`  
		Last Modified: Wed, 07 Feb 2024 07:28:17 GMT  
		Size: 1.2 MB (1248656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78e6ef661fee931920aa3236f1af661d851378c52b31aa87ffc8558da5e48a5`  
		Last Modified: Wed, 07 Feb 2024 07:28:16 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ff0b3bb63b15b33debf9aea993bd84f4b246b7c7d4484db77832556ef074ca51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c07a4329692996a3988717e0eba3652501b15f09abc9597e4ad3b87250cb63d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 02:48:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 02:48:33 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 02:48:33 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 02:48:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 02:48:34 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 02:48:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 02:48:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 02:48:38 GMT
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
	-	`sha256:7113cf104f60011eb6444102f15ef72cdd45fcb4c9caf77828b5fbc38dab492e`  
		Last Modified: Wed, 07 Feb 2024 02:23:31 GMT  
		Size: 65.8 MB (65767658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a6e0f5354f83f214823ce1d03ea8a7eab56425405c4ca69940f2f3dde97a80`  
		Last Modified: Wed, 07 Feb 2024 02:23:15 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f390b29274db9c266f41d8708269d5dda362068060acd663c445ce335597d742`  
		Last Modified: Wed, 07 Feb 2024 02:49:00 GMT  
		Size: 4.5 MB (4514221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399e806721f760b662ba77d6b0d28a03a0c91cfb57e9d60a85f9016392605507`  
		Last Modified: Wed, 07 Feb 2024 02:48:59 GMT  
		Size: 1.2 MB (1246089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5225c4821fb8eb5d3c9024e1b8b00504669f1ced491c2e93b97b5400673970c2`  
		Last Modified: Wed, 07 Feb 2024 02:48:59 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:bee0d79c6d83f0f253201d3c21afebe471923903c79a57fc165382018992582b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73998590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43afba92f6c2f26ccd2d5a34a29409424cb5d7437f186994917fd86a2a330c21`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 03:27:19 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 03:27:19 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 03:27:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 03:27:21 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 03:27:21 GMT
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
	-	`sha256:49ff1670edc3c20a6a9614ecb3f794095053b0a2bc5c3d8a27ffb6771b4e8de5`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 5.1 MB (5070614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6bfbf28b1c962164432ab027c42dcb68debdd9c90fe50d3fdec0bac01a2a1b`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 1.2 MB (1198449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dec8839aa12d34c5fc6d220df303a7b58562c777e2281fb6b912cabcb3b808`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:ff608ed0346698200d108d948d192f9d9977f35b9ee6dba5dc437eecb95eff13
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74213050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3961610a4cc67151079da941b2fa3b5f9e84fdbadf7ddfc2345914f2e7d34270`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 02:38:42 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 02:38:43 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 02:38:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 02:38:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 02:38:44 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 02:38:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 02:38:47 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 02:38:48 GMT
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
	-	`sha256:189f1d64ec6387010de82030584f95d2f1cb77480534f720a6c8051e1c053202`  
		Last Modified: Wed, 07 Feb 2024 02:39:06 GMT  
		Size: 5.3 MB (5270668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439fb1dfa6333e4624dc554a68c980b15bda052268ac48be84e477697d3fa5fc`  
		Last Modified: Wed, 07 Feb 2024 02:39:05 GMT  
		Size: 1.2 MB (1186180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b46e2bfe6d57573d777ff909c837b014c894d5f5c65212804d738620cb252e2`  
		Last Modified: Wed, 07 Feb 2024 02:39:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:fad88c033e71179f3df4bf1a5b2e9d0d0264bcbaa498b911238fc07787bbace2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76100380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914aa8aec00e9a7014cfcc15953ecea9afcc02ceae16b98a5643c211c018e323`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 03:55:22 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 03:55:23 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 03:55:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 03:55:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 03:55:24 GMT
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
	-	`sha256:667df4a2c04946a51104abaa6f5ed310f5428e8423a5229c6a93e33a7bfd3afa`  
		Last Modified: Tue, 06 Feb 2024 22:15:10 GMT  
		Size: 66.2 MB (66217776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed37103477a46e4048ca49195fde1e764f57b71cb5abadd05970bee2e2f29cc`  
		Last Modified: Tue, 06 Feb 2024 22:14:59 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d511e031e1b91b289c43c1a2190ee22aa5f38fe22568e3b6e23cdf96db48b`  
		Last Modified: Wed, 07 Feb 2024 03:56:50 GMT  
		Size: 5.1 MB (5116980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255f032cffa62a5bea76ec237a6dfe24caf125994ad6151aed12f4ae30860c02`  
		Last Modified: Wed, 07 Feb 2024 03:56:50 GMT  
		Size: 1.3 MB (1262391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8b53fd06bb1ce493aa5cc33297d87b8edfe9fd834896df28185e9c3f9b8480`  
		Last Modified: Wed, 07 Feb 2024 03:56:49 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:f21fcacb51baed792b0310844331fa37b39b4235d5cbb8274b453b4abdbeb68b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2007478332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfd7236ef3ba33c49b0293ddeaed24ed8f1a4a4be50d73bb5daf279ed0d1067`
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
# Wed, 14 Feb 2024 20:43:58 GMT
ENV GOLANG_VERSION=1.21.7
# Wed, 14 Feb 2024 20:46:14 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:46:15 GMT
WORKDIR C:\go
# Wed, 14 Feb 2024 21:25:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:25:03 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 14 Feb 2024 21:25:04 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:25:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Feb 2024 21:25:28 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Feb 2024 21:25:29 GMT
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
	-	`sha256:6a320e20304175d59e4aee6ec77d02f07509c042e71352229d992e5a71178266`  
		Last Modified: Wed, 14 Feb 2024 21:00:19 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70d6b39cc331fef21be1e6e1e4f8a09002d3e8c2cbe5510f9b576f73a103a11`  
		Last Modified: Wed, 14 Feb 2024 21:00:38 GMT  
		Size: 69.3 MB (69339697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e925967ba6e0e9ec84f4892a901f9137d074b01da5967f3f02cca1d17c55401`  
		Last Modified: Wed, 14 Feb 2024 21:00:18 GMT  
		Size: 1.5 KB (1465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5be391477771ac6ef063dfff5f60c2bf3720c4c3e438914ad4f83d4186dd419`  
		Last Modified: Wed, 14 Feb 2024 21:27:15 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8040861524a92cd1ef40205f09edcc78fca950bc460c86dabddb5b7c9d207e1`  
		Last Modified: Wed, 14 Feb 2024 21:27:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146989057ff74f0c65231a30d9ae96ef9aca638ac186e5133ab6e62f60daa4e4`  
		Last Modified: Wed, 14 Feb 2024 21:27:13 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a1e9fdf12fec3886fbcf530321f59f401f9a8e9ca54deb5a50e1ef7035857c`  
		Last Modified: Wed, 14 Feb 2024 21:27:14 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f0b7658ba93600fbb3d46955c4030818eab0d9ee14ac0f2e17afd2728e1ea8`  
		Last Modified: Wed, 14 Feb 2024 21:27:14 GMT  
		Size: 1.7 MB (1666295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ffc354f7064866e9a01cd793241fe9fb0e6c82dc2388b1ed8ca9c0c70428b3`  
		Last Modified: Wed, 14 Feb 2024 21:27:13 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:536798cc04c493719ee143f8570a8ce2c06929deaefd229e15de08e0ad26d554
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2177347938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1022bc7754872a576d582646d52e18dcb896332104dc5ae6edbb3c7130f6fe10`
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
# Wed, 14 Feb 2024 20:46:27 GMT
ENV GOLANG_VERSION=1.21.7
# Wed, 14 Feb 2024 20:49:46 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:49:47 GMT
WORKDIR C:\go
# Wed, 14 Feb 2024 21:23:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:23:35 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 14 Feb 2024 21:23:36 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:23:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Feb 2024 21:24:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Feb 2024 21:24:54 GMT
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
	-	`sha256:fc4a495babb42867e41e9e0341672d9c3dc4342d7d1ca2089393548a9394712c`  
		Last Modified: Wed, 14 Feb 2024 21:00:48 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88628d70e4f0b09c4b4d93d847ecc1af2c6287a6ee7f2c02f8574d79323b7e94`  
		Last Modified: Wed, 14 Feb 2024 21:01:08 GMT  
		Size: 69.4 MB (69351914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9c7605984ae14daab7f947cbb370c489f648caa2436563473651ccbd225379`  
		Last Modified: Wed, 14 Feb 2024 21:00:48 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7d44e23d90802e1136be2c8be711e41683f02e6106a295dc7cc9e3567c3a79`  
		Last Modified: Wed, 14 Feb 2024 21:26:56 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b8bb132d080a4d6cdfdac7bc8d37ba32d8e594b8117bee0a7149d2e0e10a59`  
		Last Modified: Wed, 14 Feb 2024 21:26:54 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0da4afa5ca0ec4b0e5f6e0ba7198a70aebf33635612ae7f8538cd3b623178c`  
		Last Modified: Wed, 14 Feb 2024 21:26:53 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b40cba54a5386a0889184fc68012a0626b7585c728882c037f3c0778a0c5365`  
		Last Modified: Wed, 14 Feb 2024 21:26:54 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9a8a348cc99b33e0367f75baaa076f55305110bd2f991bf2ca49cdde949ea6`  
		Last Modified: Wed, 14 Feb 2024 21:26:54 GMT  
		Size: 1.7 MB (1683480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f900898726315c327700e5fd8845b66a9965afeafa8abbe836093c700afe897d`  
		Last Modified: Wed, 14 Feb 2024 21:26:53 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:33a92d10027f0a21785908d646f81c6c23b4abd130fc123200f00a9381693be9
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
$ docker pull caddy@sha256:8fee3614a6b6cabdab16312c9ec1062982ef3d655b99bcc8e983cbc777572fa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76972175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2decac0840cd748d459d2f76eebc64754108ee601a66e06fca48c6880efcdb02`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 20:10:42 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 20:10:42 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 20:10:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 20:10:43 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 20:10:43 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 20:10:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 20:10:44 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 20:10:44 GMT
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
	-	`sha256:d18ba8e8dd02491f11cea93df354c71628a2360674a625c205e213ef6fd82127`  
		Last Modified: Tue, 06 Feb 2024 23:56:58 GMT  
		Size: 67.0 MB (67009643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8daf023d266d667210cf5767c01f2f4f68e40c297e0bdecf73799744ddac1026`  
		Last Modified: Tue, 06 Feb 2024 23:56:47 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23298fdc181f9cc9b4b9e297a84c2ff9119ed9ccef7ee4188033e1e62b835a71`  
		Last Modified: Wed, 07 Feb 2024 20:11:02 GMT  
		Size: 5.0 MB (4972450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2716cf52013dbd506ec1fae43d30c4339d959e635e237a5f6b1e8311fba51b4a`  
		Last Modified: Wed, 07 Feb 2024 20:11:02 GMT  
		Size: 1.3 MB (1302239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1a06d10c122c1efe42b77b107513d80c320d5adadaeeaec6ffe0235d8738c1`  
		Last Modified: Wed, 07 Feb 2024 20:11:02 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:89493aa84b348e455d5d5d3dd0f050644d7e3a9400cdc1a09d07545d95e85fd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75415278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921e0138a2eb31837973f479ce9117ffd13a871b9e3c1e3332f0689b85ec2e5d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 07:28:02 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 07:28:02 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 07:28:02 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 07:28:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 07:28:03 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 07:28:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 07:28:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 07:28:04 GMT
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
	-	`sha256:fa53b2f66831ea2a6a71d6469b90663284dc2a4ce3cb48320dd55896f9cd8d84`  
		Last Modified: Tue, 06 Feb 2024 23:32:01 GMT  
		Size: 65.8 MB (65767452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6d1ac72f2f91d206a9c3fa198f2e45b1f18fcfd8da385ab8c5e3288262790`  
		Last Modified: Tue, 06 Feb 2024 23:31:47 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6fbc6c4773d705c6048f1330050fc6200a9ae262d156ab7492ac01fc483010`  
		Last Modified: Wed, 07 Feb 2024 07:28:17 GMT  
		Size: 5.0 MB (4966629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cdc84144fd70dfac8f705109ec0a92dc10a7dfc50838c6af32b442b918fcc6`  
		Last Modified: Wed, 07 Feb 2024 07:28:17 GMT  
		Size: 1.2 MB (1248656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78e6ef661fee931920aa3236f1af661d851378c52b31aa87ffc8558da5e48a5`  
		Last Modified: Wed, 07 Feb 2024 07:28:16 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:ff0b3bb63b15b33debf9aea993bd84f4b246b7c7d4484db77832556ef074ca51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74714053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c07a4329692996a3988717e0eba3652501b15f09abc9597e4ad3b87250cb63d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 02:48:33 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 02:48:33 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 02:48:33 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 02:48:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 02:48:34 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 02:48:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 02:48:37 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 02:48:38 GMT
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
	-	`sha256:7113cf104f60011eb6444102f15ef72cdd45fcb4c9caf77828b5fbc38dab492e`  
		Last Modified: Wed, 07 Feb 2024 02:23:31 GMT  
		Size: 65.8 MB (65767658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a6e0f5354f83f214823ce1d03ea8a7eab56425405c4ca69940f2f3dde97a80`  
		Last Modified: Wed, 07 Feb 2024 02:23:15 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f390b29274db9c266f41d8708269d5dda362068060acd663c445ce335597d742`  
		Last Modified: Wed, 07 Feb 2024 02:49:00 GMT  
		Size: 4.5 MB (4514221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399e806721f760b662ba77d6b0d28a03a0c91cfb57e9d60a85f9016392605507`  
		Last Modified: Wed, 07 Feb 2024 02:48:59 GMT  
		Size: 1.2 MB (1246089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5225c4821fb8eb5d3c9024e1b8b00504669f1ced491c2e93b97b5400673970c2`  
		Last Modified: Wed, 07 Feb 2024 02:48:59 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:bee0d79c6d83f0f253201d3c21afebe471923903c79a57fc165382018992582b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73998590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43afba92f6c2f26ccd2d5a34a29409424cb5d7437f186994917fd86a2a330c21`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 03:27:19 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 03:27:19 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 03:27:19 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 03:27:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 03:27:21 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 03:27:21 GMT
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
	-	`sha256:49ff1670edc3c20a6a9614ecb3f794095053b0a2bc5c3d8a27ffb6771b4e8de5`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 5.1 MB (5070614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6bfbf28b1c962164432ab027c42dcb68debdd9c90fe50d3fdec0bac01a2a1b`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 1.2 MB (1198449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dec8839aa12d34c5fc6d220df303a7b58562c777e2281fb6b912cabcb3b808`  
		Last Modified: Wed, 07 Feb 2024 03:27:34 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:ff608ed0346698200d108d948d192f9d9977f35b9ee6dba5dc437eecb95eff13
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74213050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3961610a4cc67151079da941b2fa3b5f9e84fdbadf7ddfc2345914f2e7d34270`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 02:38:42 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 02:38:43 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 02:38:43 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 02:38:44 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 02:38:44 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 02:38:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 02:38:47 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 02:38:48 GMT
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
	-	`sha256:189f1d64ec6387010de82030584f95d2f1cb77480534f720a6c8051e1c053202`  
		Last Modified: Wed, 07 Feb 2024 02:39:06 GMT  
		Size: 5.3 MB (5270668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439fb1dfa6333e4624dc554a68c980b15bda052268ac48be84e477697d3fa5fc`  
		Last Modified: Wed, 07 Feb 2024 02:39:05 GMT  
		Size: 1.2 MB (1186180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b46e2bfe6d57573d777ff909c837b014c894d5f5c65212804d738620cb252e2`  
		Last Modified: Wed, 07 Feb 2024 02:39:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:fad88c033e71179f3df4bf1a5b2e9d0d0264bcbaa498b911238fc07787bbace2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76100380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914aa8aec00e9a7014cfcc15953ecea9afcc02ceae16b98a5643c211c018e323`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 23:26:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOLANG_VERSION=1.21.7
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Feb 2024 23:26:32 GMT
ENV GOPATH=/go
# Tue, 06 Feb 2024 23:26:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 23:26:32 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Feb 2024 23:26:32 GMT
WORKDIR /go
# Wed, 07 Feb 2024 03:55:22 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 07 Feb 2024 03:55:23 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 07 Feb 2024 03:55:23 GMT
ENV XCADDY_SETCAP=1
# Wed, 07 Feb 2024 03:55:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='9e87261a4ca4144bf25105e0cb3b3eb0fb0b8564fe4fa5c126e25a926baea2d16868cb4e88cafc419dc69db3e692894bc7ebcb25434c0bbb74362c2f3a696db5' ;; 		armhf)   binArch='armv6'; checksum='e327445263f3c4ceacae92f88417ef9d2f559bd01ea53230c38529295f2c29da45a0f9c436a71dafc85009a4ead7acdde832971479fccde7839228f0fc2153f1' ;; 		armv7)   binArch='armv7'; checksum='c46e12f1750ea1c99a80cf0ab2115541957f2791257176df2dbf2b25869c552b3108ff7c9d6854081dcf843548e6ec3b1e5451944bd7b6b9527dfe63f849f01b' ;; 		aarch64) binArch='arm64'; checksum='a4b1caf438326e0dcb58830701993d514b11fd86b4880c9c013c230031dfa68efa339be186662f586ce848d5a2841a2e6513f41ada9a05c04a297433df3f2a52' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='b9c79ec1ddd1f7606d7f1263cf4ebad8c03154e78e301db27cb1554723b1f12ae886dd4be682a9decd3dbc189d6e90c51879ae160696db00e0d32dced2df8991' ;; 		s390x)   binArch='s390x'; checksum='658f3d85e751e3e43906e55b9f915c35c1e87c6cdeb606263147804520fe4cf3afdf295882c7bab2e9c932a7c12d1759275fa1c0b611d5b770c940e9ec13ec43' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 07 Feb 2024 03:55:24 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 07 Feb 2024 03:55:24 GMT
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
	-	`sha256:667df4a2c04946a51104abaa6f5ed310f5428e8423a5229c6a93e33a7bfd3afa`  
		Last Modified: Tue, 06 Feb 2024 22:15:10 GMT  
		Size: 66.2 MB (66217776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed37103477a46e4048ca49195fde1e764f57b71cb5abadd05970bee2e2f29cc`  
		Last Modified: Tue, 06 Feb 2024 22:14:59 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d511e031e1b91b289c43c1a2190ee22aa5f38fe22568e3b6e23cdf96db48b`  
		Last Modified: Wed, 07 Feb 2024 03:56:50 GMT  
		Size: 5.1 MB (5116980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255f032cffa62a5bea76ec237a6dfe24caf125994ad6151aed12f4ae30860c02`  
		Last Modified: Wed, 07 Feb 2024 03:56:50 GMT  
		Size: 1.3 MB (1262391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8b53fd06bb1ce493aa5cc33297d87b8edfe9fd834896df28185e9c3f9b8480`  
		Last Modified: Wed, 07 Feb 2024 03:56:49 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:3f8db6e8a2fe203d75df858bb7930fe4be2c30c957a28c2bcf5c21302a39c66d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull caddy@sha256:536798cc04c493719ee143f8570a8ce2c06929deaefd229e15de08e0ad26d554
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2177347938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1022bc7754872a576d582646d52e18dcb896332104dc5ae6edbb3c7130f6fe10`
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
# Wed, 14 Feb 2024 20:46:27 GMT
ENV GOLANG_VERSION=1.21.7
# Wed, 14 Feb 2024 20:49:46 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:49:47 GMT
WORKDIR C:\go
# Wed, 14 Feb 2024 21:23:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:23:35 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 14 Feb 2024 21:23:36 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:23:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Feb 2024 21:24:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Feb 2024 21:24:54 GMT
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
	-	`sha256:fc4a495babb42867e41e9e0341672d9c3dc4342d7d1ca2089393548a9394712c`  
		Last Modified: Wed, 14 Feb 2024 21:00:48 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88628d70e4f0b09c4b4d93d847ecc1af2c6287a6ee7f2c02f8574d79323b7e94`  
		Last Modified: Wed, 14 Feb 2024 21:01:08 GMT  
		Size: 69.4 MB (69351914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9c7605984ae14daab7f947cbb370c489f648caa2436563473651ccbd225379`  
		Last Modified: Wed, 14 Feb 2024 21:00:48 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7d44e23d90802e1136be2c8be711e41683f02e6106a295dc7cc9e3567c3a79`  
		Last Modified: Wed, 14 Feb 2024 21:26:56 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b8bb132d080a4d6cdfdac7bc8d37ba32d8e594b8117bee0a7149d2e0e10a59`  
		Last Modified: Wed, 14 Feb 2024 21:26:54 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0da4afa5ca0ec4b0e5f6e0ba7198a70aebf33635612ae7f8538cd3b623178c`  
		Last Modified: Wed, 14 Feb 2024 21:26:53 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b40cba54a5386a0889184fc68012a0626b7585c728882c037f3c0778a0c5365`  
		Last Modified: Wed, 14 Feb 2024 21:26:54 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9a8a348cc99b33e0367f75baaa076f55305110bd2f991bf2ca49cdde949ea6`  
		Last Modified: Wed, 14 Feb 2024 21:26:54 GMT  
		Size: 1.7 MB (1683480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f900898726315c327700e5fd8845b66a9965afeafa8abbe836093c700afe897d`  
		Last Modified: Wed, 14 Feb 2024 21:26:53 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:c902b48fcec4254e6ed5eeb752b75d08e42bbd1bbd67398e45da91dcfa46a841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull caddy@sha256:f21fcacb51baed792b0310844331fa37b39b4235d5cbb8274b453b4abdbeb68b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2007478332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfd7236ef3ba33c49b0293ddeaed24ed8f1a4a4be50d73bb5daf279ed0d1067`
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
# Wed, 14 Feb 2024 20:43:58 GMT
ENV GOLANG_VERSION=1.21.7
# Wed, 14 Feb 2024 20:46:14 GMT
RUN $url = 'https://dl.google.com/go/go1.21.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9ba8652778baded6e9a758c3129aae73393b4b75b230933bb0cf3ab65b19be35'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:46:15 GMT
WORKDIR C:\go
# Wed, 14 Feb 2024 21:25:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 21:25:03 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 14 Feb 2024 21:25:04 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 14 Feb 2024 21:25:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 Feb 2024 21:25:28 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 Feb 2024 21:25:29 GMT
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
	-	`sha256:6a320e20304175d59e4aee6ec77d02f07509c042e71352229d992e5a71178266`  
		Last Modified: Wed, 14 Feb 2024 21:00:19 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70d6b39cc331fef21be1e6e1e4f8a09002d3e8c2cbe5510f9b576f73a103a11`  
		Last Modified: Wed, 14 Feb 2024 21:00:38 GMT  
		Size: 69.3 MB (69339697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e925967ba6e0e9ec84f4892a901f9137d074b01da5967f3f02cca1d17c55401`  
		Last Modified: Wed, 14 Feb 2024 21:00:18 GMT  
		Size: 1.5 KB (1465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5be391477771ac6ef063dfff5f60c2bf3720c4c3e438914ad4f83d4186dd419`  
		Last Modified: Wed, 14 Feb 2024 21:27:15 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8040861524a92cd1ef40205f09edcc78fca950bc460c86dabddb5b7c9d207e1`  
		Last Modified: Wed, 14 Feb 2024 21:27:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146989057ff74f0c65231a30d9ae96ef9aca638ac186e5133ab6e62f60daa4e4`  
		Last Modified: Wed, 14 Feb 2024 21:27:13 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a1e9fdf12fec3886fbcf530321f59f401f9a8e9ca54deb5a50e1ef7035857c`  
		Last Modified: Wed, 14 Feb 2024 21:27:14 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f0b7658ba93600fbb3d46955c4030818eab0d9ee14ac0f2e17afd2728e1ea8`  
		Last Modified: Wed, 14 Feb 2024 21:27:14 GMT  
		Size: 1.7 MB (1666295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ffc354f7064866e9a01cd793241fe9fb0e6c82dc2388b1ed8ca9c0c70428b3`  
		Last Modified: Wed, 14 Feb 2024 21:27:13 GMT  
		Size: 1.3 KB (1320 bytes)  
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
