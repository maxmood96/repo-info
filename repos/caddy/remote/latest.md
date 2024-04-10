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
