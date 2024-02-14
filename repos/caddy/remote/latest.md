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
