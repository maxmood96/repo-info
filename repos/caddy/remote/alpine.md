## `caddy:alpine`

```console
$ docker pull caddy@sha256:1d90f85249439ec8c0774aa417fb23d13d7b8d9e38df29517838ae56d4034627
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
