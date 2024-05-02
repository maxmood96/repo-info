## `caddy:latest`

```console
$ docker pull caddy@sha256:90276aa213f7833cdf256df77c0eabfd5b3a438e245d17766381c423b522401f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `caddy:latest` - linux; amd64

```console
$ docker pull caddy@sha256:82e3a05828100969bec64fb84f387ece979c66875ca8b3033ac98cc304ea8f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18476994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbd4302afb8cb196ff48423af4508320dbeab653faf279da0c93e8bb47141e7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 08 Dec 2023 02:23:07 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Fri, 08 Dec 2023 02:23:07 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 02:23:07 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html" # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 02:23:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 02:23:07 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 Dec 2023 02:23:07 GMT
EXPOSE map[443/tcp:{}]
# Fri, 08 Dec 2023 02:23:07 GMT
EXPOSE map[443/udp:{}]
# Fri, 08 Dec 2023 02:23:07 GMT
EXPOSE map[2019/tcp:{}]
# Fri, 08 Dec 2023 02:23:07 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 02:23:07 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e62bf88daf5db8b319b21f28d8defeb9b7a914c77dade4ffb63aca21e00d15c`  
		Last Modified: Wed, 01 May 2024 21:52:03 GMT  
		Size: 360.6 KB (360576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d5dfd14a592fc46e7f050ef4ea9b6095578bc7d625012974ed493f06330511`  
		Last Modified: Wed, 01 May 2024 21:52:03 GMT  
		Size: 7.5 KB (7454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a56a6ec555c97b63313c8b1e344f021051b6ff6a646c1639d5813a55b9ba74`  
		Last Modified: Wed, 01 May 2024 21:52:05 GMT  
		Size: 14.7 MB (14706390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:285b1e8fc3497532a5f92155f9c5fa94e44fb4124073701c25f9ebb59e131676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 KB (286599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b122fff4bb37e9e23e8e4410b0d5c9de63688487226a7f5bfb4876baee9f0f32`

```dockerfile
```

-	Layers:
	-	`sha256:9be4da22ba3af3e0a07118e91b2058c88275179acbc7b8be4a3bccecb0865bc4`  
		Last Modified: Wed, 01 May 2024 21:52:04 GMT  
		Size: 268.9 KB (268899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd44b8aaf991209719c5f05ec748b9e05fb898179cafe8e12b1067334f130200`  
		Last Modified: Wed, 01 May 2024 21:52:03 GMT  
		Size: 17.7 KB (17700 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v6

```console
$ docker pull caddy@sha256:6fff56910d5aa8323635d87b8f1ff797fab25eb26b596de490a06910edbd4364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17432793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1205613dbc921cd8260cf9e1251b12d757b4e97473acb1565bc78a14651c6b2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 08 Dec 2023 02:23:07 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 08 Dec 2023 02:23:07 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 02:23:07 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html" # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 02:23:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 02:23:07 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 Dec 2023 02:23:07 GMT
EXPOSE map[443/tcp:{}]
# Fri, 08 Dec 2023 02:23:07 GMT
EXPOSE map[443/udp:{}]
# Fri, 08 Dec 2023 02:23:07 GMT
EXPOSE map[2019/tcp:{}]
# Fri, 08 Dec 2023 02:23:07 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 02:23:07 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320944b9d89ce73b5dbd09f5e7a6041004d85f4bef04eb1417a27e8a24f13f5b`  
		Last Modified: Wed, 01 May 2024 21:56:04 GMT  
		Size: 357.3 KB (357340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f8b47308b9a41e174547c5e8fdd49d007deee8cf0cb35c433f0c372392466d`  
		Last Modified: Wed, 01 May 2024 21:56:04 GMT  
		Size: 7.5 KB (7450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ac9a8374eed44354154877d4bf28fb1cfa5ca1bbdbccc4195e6fb20fc139c5`  
		Last Modified: Wed, 01 May 2024 21:56:05 GMT  
		Size: 13.9 MB (13920912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:a446eae20b567c7735af3884318feba446830c2821c086ac28e706b7c15b3d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66bc5869e952a01318c6172942e57e8d1c1a5d3060237cd3e6b261ff801955d`

```dockerfile
```

-	Layers:
	-	`sha256:70b4ead65e1d8ffc6a707fc6aa20674e0dd4a0d957700027d6035cb3c7e146cf`  
		Last Modified: Wed, 01 May 2024 21:56:05 GMT  
		Size: 17.4 KB (17441 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm variant v7

```console
$ docker pull caddy@sha256:472661646590f10b0746f9426e59e59744963a5bb683e3157b3ce9d3e227303f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17156263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9b784e37e6307fa4d5283771fd63fda49d202619955136907d32715ced8818`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 08 Dec 2023 02:23:07 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Fri, 08 Dec 2023 02:23:07 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 02:23:07 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html" # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 02:23:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 02:23:07 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 Dec 2023 02:23:07 GMT
EXPOSE map[443/tcp:{}]
# Fri, 08 Dec 2023 02:23:07 GMT
EXPOSE map[443/udp:{}]
# Fri, 08 Dec 2023 02:23:07 GMT
EXPOSE map[2019/tcp:{}]
# Fri, 08 Dec 2023 02:23:07 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 02:23:07 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b527911aa0f8852117f57452d522fb961c184d105b0818cb4a87109b08272643`  
		Last Modified: Wed, 01 May 2024 22:05:53 GMT  
		Size: 353.7 KB (353705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c2b2e6aa4512d9656ee88bcaa7b5c45f2403fc5f66a9e56148ff4f4f55c605`  
		Last Modified: Wed, 01 May 2024 22:05:52 GMT  
		Size: 7.5 KB (7450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666c1622df85e816a23209fde59fd3224312ce0f36c4c533187a670eb1f4c3a8`  
		Last Modified: Wed, 01 May 2024 22:05:53 GMT  
		Size: 13.9 MB (13893684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:f4b884df09ab35a3d390ea752dc8ee52dc5eaa746d3be863e8c583954d01e358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 KB (286629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc20ba5a5c17189776982aaa4395fd70b220cfca7f35870b76964f0ff6451444`

```dockerfile
```

-	Layers:
	-	`sha256:008d006848d30e18f047716e28ab9b8541ec816adca9355ebafb57d13fc63634`  
		Last Modified: Wed, 01 May 2024 22:05:53 GMT  
		Size: 269.0 KB (268967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f525a65babfb454ba9b0c6d045a1cd5705c157d3d6e386b38dd6dd4425275502`  
		Last Modified: Wed, 01 May 2024 22:05:52 GMT  
		Size: 17.7 KB (17662 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:f949d6da3de94ce1c161ffe466639f43a630085821e9a8a161f619b5075a4982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17278622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0716abea5022ab80b7696d173dfd0b40b961e73be069f37a974c9e8885169932`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 08 Dec 2023 02:23:07 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 08 Dec 2023 02:23:07 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 02:23:07 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html" # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 02:23:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 02:23:07 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 Dec 2023 02:23:07 GMT
EXPOSE map[443/tcp:{}]
# Fri, 08 Dec 2023 02:23:07 GMT
EXPOSE map[443/udp:{}]
# Fri, 08 Dec 2023 02:23:07 GMT
EXPOSE map[2019/tcp:{}]
# Fri, 08 Dec 2023 02:23:07 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 02:23:07 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f50788699932589070b139144f3b1440a2948fa84be4ca81ecdc1d1a54e4e69`  
		Last Modified: Wed, 01 May 2024 22:12:04 GMT  
		Size: 368.8 KB (368765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc4192edeba6f7c45fe77039c759ecaae17e5f77e471ff65bdab32cfe198576`  
		Last Modified: Wed, 01 May 2024 22:12:04 GMT  
		Size: 7.5 KB (7454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d8a1e96952f0422e0056c8f04d690a4ffdbe808f868b6566f2ae1fdb0d2369`  
		Last Modified: Wed, 01 May 2024 22:12:04 GMT  
		Size: 13.6 MB (13569010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:530358cafe446226047be397de275e20ccff7d1bf7b2a0978f1ed38825834ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 KB (286469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30434a273e547ad166ea7d5237320a5a509ef619469c02a94ffd399852b19cb5`

```dockerfile
```

-	Layers:
	-	`sha256:3920f3a14066cda2d0c0516bbcf735add437556c946c1634f5135dadbf90fe77`  
		Last Modified: Wed, 01 May 2024 22:12:04 GMT  
		Size: 268.9 KB (268918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55f5ce4dd53b403f48dd6870abe91c2e5e8f2b978e60c1fe237a1669522871b7`  
		Last Modified: Wed, 01 May 2024 22:12:04 GMT  
		Size: 17.6 KB (17551 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; ppc64le

```console
$ docker pull caddy@sha256:b023c1ec5e136ebfc786d405504c91b39fd23ff93a64b7db15997f480ec6aa0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17060085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aae07509494a977317f079d09c8ee42c8db977e41845d7519086db222b43f3f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 08 Dec 2023 02:23:07 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Fri, 08 Dec 2023 02:23:07 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 02:23:07 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html" # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 02:23:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 02:23:07 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 Dec 2023 02:23:07 GMT
EXPOSE map[443/tcp:{}]
# Fri, 08 Dec 2023 02:23:07 GMT
EXPOSE map[443/udp:{}]
# Fri, 08 Dec 2023 02:23:07 GMT
EXPOSE map[2019/tcp:{}]
# Fri, 08 Dec 2023 02:23:07 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 02:23:07 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0550c488b324bf74512534b8af77dc0690e94dd12f1286c76669cb03c733692`  
		Last Modified: Wed, 01 May 2024 22:06:02 GMT  
		Size: 370.3 KB (370278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9459a3c9a5a45e4f7379e5baf3d6a8c88d9a93558d32e306fd5796552b6b45`  
		Last Modified: Wed, 01 May 2024 22:06:02 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22c0a754cc2f8dba05b0ed6b3730b2d133514ef4da2f3a7d54f090034e276cd`  
		Last Modified: Wed, 01 May 2024 22:06:03 GMT  
		Size: 13.3 MB (13333836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:706ebf17e0b6ca1499ff9ad480f57e73a47d41f8d0e47a51e06cac4a992cbe94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 KB (284603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed42091e5f60b3b18b4c588d9c2e73182167a450fe93d706a690491a93d4a8a`

```dockerfile
```

-	Layers:
	-	`sha256:eb91db6d479fca8f480ebff834b13d1dfa6abbf79a3c29792466a901a69feacf`  
		Last Modified: Wed, 01 May 2024 22:06:02 GMT  
		Size: 267.0 KB (267003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00916c70996a9c642d7f479522cad912e074caabf44586ff779fe0a04bc504dd`  
		Last Modified: Wed, 01 May 2024 22:06:02 GMT  
		Size: 17.6 KB (17600 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - linux; s390x

```console
$ docker pull caddy@sha256:cfb2d8f56ac1224957fc7aaf1a2c1c07b79c71ade237810679092ee401a44341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17828010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037390288ab18ea66f20920f176a99b498527495815672b105c023f85fad56c1`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 08 Dec 2023 02:23:07 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Fri, 08 Dec 2023 02:23:07 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 02:23:07 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html" # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
ENV CADDY_VERSION=v2.7.6
# Fri, 08 Dec 2023 02:23:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b74311ec8263f30f6d36e5c8be151e8bc092b377789a55300d5671238b9043de5bd6db2bcefae32aa1e6fe94c47bbf02982c44a7871e5777b2596fdb20907cbf' ;; 		armhf)   binArch='armv6'; checksum='88756642ca412db3a8da7a40b518861a6f524a8ac704021e8451d3cb38746f24243b1e561f4eec07e1575200d06bfd098783d2b7ee7ee07a971aed1c677da6e6' ;; 		armv7)   binArch='armv7'; checksum='118776e879c280556abb7c03ff7c0081eda23c2aee0472aef176f733785e9501defaeaf334cd2443e31294809beafaea831d2e695aa68045160082aa3a966e2f' ;; 		aarch64) binArch='arm64'; checksum='62252ade5e8dcec13a66154ee1978d959370be049cce52e7c4edefff14ef70bbb21630e3735092719bc3c31214e89dff99e55970ff0adec8ac0a94c6415b059a' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='65d27fe53f5e4fa79f3476f8902071c907aab74db1a2616342be3714d4252219fbb53b174ef588e20c51e7cfac84376c7a0a608091c2fe83b31dbf59dabeb237' ;; 		s390x)   binArch='s390x'; checksum='c562190962a2db0248a4190616dd2ebaa02df2cf62f1a2c71f9d9de18af2a297df8000a06a11e8d3929dfd64f0c081d1e61961687ca220007459f2dbd0be2c81' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XDG_CONFIG_HOME=/config
# Fri, 08 Dec 2023 02:23:07 GMT
ENV XDG_DATA_HOME=/data
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.title=Caddy
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 Dec 2023 02:23:07 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 08 Dec 2023 02:23:07 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 Dec 2023 02:23:07 GMT
EXPOSE map[443/tcp:{}]
# Fri, 08 Dec 2023 02:23:07 GMT
EXPOSE map[443/udp:{}]
# Fri, 08 Dec 2023 02:23:07 GMT
EXPOSE map[2019/tcp:{}]
# Fri, 08 Dec 2023 02:23:07 GMT
WORKDIR /srv
# Fri, 08 Dec 2023 02:23:07 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7649425a6a944a0c8c4f452b8bc1e2874e0e99c7e097d2aec191fb8ac784fd6d`  
		Last Modified: Wed, 01 May 2024 22:05:37 GMT  
		Size: 364.7 KB (364696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642b451d8ec761431d2cabb8e470c10726a97928fb52f2e0f9503b2d24b58649`  
		Last Modified: Wed, 01 May 2024 22:05:37 GMT  
		Size: 7.5 KB (7453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a978fa315c2a7ea88b68e4d42f35d8b08c33cc1cf729c6b5f7d5858e20cf121d`  
		Last Modified: Wed, 01 May 2024 22:05:37 GMT  
		Size: 14.2 MB (14238299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:latest` - unknown; unknown

```console
$ docker pull caddy@sha256:76704cb6574cecb755d7505b0baa788e6078bd32cf98e150cff96c42095fad21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 KB (284475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881fd2799c806dc84a4c0cc614fef65071b5e776a542b43850a352dcc42ead93`

```dockerfile
```

-	Layers:
	-	`sha256:94f4f546c040f162d6340b723bd25083f301deda2c4771ca75f931b16d361103`  
		Last Modified: Wed, 01 May 2024 22:05:38 GMT  
		Size: 266.9 KB (266941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da9f11093451e41806cfe341a80e8d07331c9e7731dba417abb6a42fe35678ec`  
		Last Modified: Wed, 01 May 2024 22:05:37 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:latest` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:db2ca936588a88f8cb1f1ac281665623ae6cff49aa03938f153f61368a5cc56b
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2015565479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df45dc5c85ef1b67aa9ac39373f5d31666a1fc45364c803bbcedc13b41167ece`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Wed, 01 May 2024 21:52:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 01 May 2024 21:53:35 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 01 May 2024 21:53:36 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 21:53:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 01 May 2024 21:53:51 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 01 May 2024 21:53:52 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 01 May 2024 21:53:53 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 21:53:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 21:53:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 21:53:55 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 21:53:56 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 21:53:57 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 21:53:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 21:53:58 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 21:53:59 GMT
EXPOSE 80
# Wed, 01 May 2024 21:54:00 GMT
EXPOSE 443
# Wed, 01 May 2024 21:54:00 GMT
EXPOSE 443/udp
# Wed, 01 May 2024 21:54:01 GMT
EXPOSE 2019
# Wed, 01 May 2024 21:54:11 GMT
RUN caddy version
# Wed, 01 May 2024 21:54:12 GMT
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
	-	`sha256:0010899e99c47859b14feb3007a937573303de68076ec99117119ab57fdd57c1`  
		Last Modified: Wed, 01 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c890145d7d363f973edd90b4ffdcc5d20b5b1260bb3bbeb325dbcf0e9009a3`  
		Last Modified: Wed, 01 May 2024 21:54:18 GMT  
		Size: 512.1 KB (512100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8422e5e19e084131580873257c6f2625df71a8745e2c1595ded7c16ba475a0`  
		Last Modified: Wed, 01 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ef736991f48e994e25aeb590132bea5f19d8b42fa8d1180d315f2f73495fa0`  
		Last Modified: Wed, 01 May 2024 21:54:20 GMT  
		Size: 15.3 MB (15323389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef601d3fe6409725e550af59a5ba123c5702c2fbd40b326cc940c084d5f0785`  
		Last Modified: Wed, 01 May 2024 21:54:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3df3db726e1e0a5a13fec3c8248a22c2d9e07471c0b95a3ba2f0e4cc95b304`  
		Last Modified: Wed, 01 May 2024 21:54:17 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3cdb261531e719d2bc6b975c0f53b29040dbe568c1303af740b2ae6ea41b85`  
		Last Modified: Wed, 01 May 2024 21:54:17 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff5c5e04007ac6458d1ea04660e383c43b99803f43e2a668701b18941736838`  
		Last Modified: Wed, 01 May 2024 21:54:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84de06b1d99a5017a815393d6265dc38221ccec44af3c08e6c2ff648892b34b2`  
		Last Modified: Wed, 01 May 2024 21:54:17 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6def0c5665fae6a5f2f264ed2da99bab0ecd84fef2046f839b3b401056847`  
		Last Modified: Wed, 01 May 2024 21:54:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4fe393b3e7b4c6b6456a1973667f020b2302bb22dfe798cdc05b944a97769e`  
		Last Modified: Wed, 01 May 2024 21:54:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71ec2469f82bfb83af1bfb0fded85a95bfd2712cb32d862af3b7129c6211fec`  
		Last Modified: Wed, 01 May 2024 21:54:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd104668c0fec173f2d4d176447ae55e00a317704f13f2f0e6b88c962dfef1c8`  
		Last Modified: Wed, 01 May 2024 21:54:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5409a5e8b2cdefd2116ef7002f18fa0f8dc654c94ce9d998e8b249893c495bc2`  
		Last Modified: Wed, 01 May 2024 21:54:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23f0af2fa993eebe78fa6f22654d8c4b0a0ac855f974f10f4f541eee1477bd8`  
		Last Modified: Wed, 01 May 2024 21:54:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a8d145e66895c555fa5ee89b4deeb8f1e72d45cdbaa91f0b2ddd9337a404df`  
		Last Modified: Wed, 01 May 2024 21:54:15 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1491cf2c5b446d7e52a6a7a07c7929a86546c4d6e88c807abf9117cde973bdfb`  
		Last Modified: Wed, 01 May 2024 21:54:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdc06d71f3b6a91dfd3cc874ed8e93b0c646b7e6e1efdd7825dc8a7e3d45db0`  
		Last Modified: Wed, 01 May 2024 21:54:14 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91eb21f53b513606014145f4ab50fc401c21276b52680592c2dce492250d5cc`  
		Last Modified: Wed, 01 May 2024 21:54:15 GMT  
		Size: 334.3 KB (334339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2799cd914dadb04d5be8ac47754e967df5574ac518aecabdf69ee7e83575ef3c`  
		Last Modified: Wed, 01 May 2024 21:54:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:latest` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:58b302755f654da481f0b65cb8a754c0682320d6d1d67983df3fe8dfd2519292
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2180627792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8709e36c6a33d54655556e49964ded05c8cf7bac9dfccf3155b88388bc5b9c6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Wed, 01 May 2024 21:52:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 01 May 2024 21:52:49 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 01 May 2024 21:52:49 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 21:53:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 01 May 2024 21:53:19 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 01 May 2024 21:53:19 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 01 May 2024 21:53:20 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 21:53:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 21:53:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 21:53:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 21:53:22 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 21:53:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 21:53:23 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 21:53:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 21:53:24 GMT
EXPOSE 80
# Wed, 01 May 2024 21:53:25 GMT
EXPOSE 443
# Wed, 01 May 2024 21:53:25 GMT
EXPOSE 443/udp
# Wed, 01 May 2024 21:53:26 GMT
EXPOSE 2019
# Wed, 01 May 2024 21:53:48 GMT
RUN caddy version
# Wed, 01 May 2024 21:53:49 GMT
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
	-	`sha256:a11f8f0ed706dd088e2964a1db4c196eab427d3ebcd72a94bc601bc71f0edd66`  
		Last Modified: Wed, 01 May 2024 21:53:59 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7867e31171e68f8934ada5c219f4c6f382d53aef22408ff4303e828a83ad0246`  
		Last Modified: Wed, 01 May 2024 21:54:00 GMT  
		Size: 497.1 KB (497053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953f416cfa31c18fc5a61bc98c96d8637a1cde627f2f5394d0a515489411040f`  
		Last Modified: Wed, 01 May 2024 21:53:59 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a76666bffc803defd63fa816e852588ae58756e61b07006c09b7722e9648474`  
		Last Modified: Wed, 01 May 2024 21:54:01 GMT  
		Size: 15.3 MB (15344008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1605fdc91841c5519f821acf15e6b1c23522f51bf72c2136541550a7c5a1aff3`  
		Last Modified: Wed, 01 May 2024 21:53:58 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24774db8845fdc637df149345943184e1f4c523ea2b4dd00407788369e0d7cc`  
		Last Modified: Wed, 01 May 2024 21:53:58 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6051ca70f9a3d922809a1676bc4a00f1c9cc43020c18a765905660bd4e36e087`  
		Last Modified: Wed, 01 May 2024 21:53:57 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a03e682933b577dc860b4314b7947c0873cd968ec09c4c6d851878589ff446`  
		Last Modified: Wed, 01 May 2024 21:53:57 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105b73d8a840e890b5605d1ece6adeb212e32e17f31f70c6f206778d2c07c866`  
		Last Modified: Wed, 01 May 2024 21:53:57 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489b6f22087ae5eb9b3131ea68a1e13033cdb0dfca64abbc4d5761cc7eadda91`  
		Last Modified: Wed, 01 May 2024 21:53:57 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154e4875860ebfccacb938b6d0169c810e3398d544960b97b3df96872f5f14c3`  
		Last Modified: Wed, 01 May 2024 21:53:55 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56dd5e69cfe7d2e118eb318eb0701125025185cffa40dd2be33c622068d5ace3`  
		Last Modified: Wed, 01 May 2024 21:53:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c8b0d6c3ac77c9af55159666d49dfbea38d01f17f4824fa8738a6f9bdaea4d`  
		Last Modified: Wed, 01 May 2024 21:53:55 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847710ca1f0cdda84e9d48d0d0577c8924de4d1b4ee1dc5e72d62b99a57a9cbb`  
		Last Modified: Wed, 01 May 2024 21:53:55 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802477541d228fe5a3dfd3d067b89afc39171fa056f56821b08ece8f94552108`  
		Last Modified: Wed, 01 May 2024 21:53:55 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a562cce4903e8ede1483531b0412cd0610454f6a21cc33b4bb228d5306013300`  
		Last Modified: Wed, 01 May 2024 21:53:53 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4b04e85bdb051c214ae0c76191bc498513f5198158d22fb4f386fccb7b1f98`  
		Last Modified: Wed, 01 May 2024 21:53:53 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce63a1f1784f21f621d3199572beda3b3d0cffd4c5cb9c858e6e3ef55014d1`  
		Last Modified: Wed, 01 May 2024 21:53:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77523f1e3d4709dc2fed1ebfbd39c17444f56c74ef4a6a29bdfbd50c9ae38859`  
		Last Modified: Wed, 01 May 2024 21:53:53 GMT  
		Size: 336.7 KB (336665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38d02c65e08275d3374291aa34d44d250c91bb6254851098389c338efd91592`  
		Last Modified: Wed, 01 May 2024 21:53:53 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
