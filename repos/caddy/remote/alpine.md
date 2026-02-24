## `caddy:alpine`

```console
$ docker pull caddy@sha256:3b2a0196e0687279c14c27adff9fc6b44acfa318dbb97eaebe385bdf99e5364c
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `caddy:alpine` - linux; amd64

```console
$ docker pull caddy@sha256:a4983e09003e598c28ef85197c16bb2fdd34da8b2526487c0d144f38fd3b2970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23730087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818bec5261db8072f732f941ed335d7f027b1657230c0f62479a4398683e911f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 20:03:56 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Mon, 23 Feb 2026 20:03:57 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Mon, 23 Feb 2026 20:03:58 GMT
ENV CADDY_VERSION=v2.11.1
# Mon, 23 Feb 2026 20:03:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='cd194db2a730db0dbb343e9b468725d6bc31d915d977ed3fc79ae88af83fd0ad259d3560976a28c51ec5d9fd23a79980e71763eda5239beb8232e5adfa0a9707' ;; 		armhf)   binArch='armv6'; checksum='e1165b9375507781d9fec1d5a1ccb179b252911b40bfcb654d19dade298d12e7fc67ef494d2bd9ff99649b23540f666d35a41b9489c690317145130acbf400d1' ;; 		armv7)   binArch='armv7'; checksum='7c2dbe9cdac73ba8a3de4ec551a594c4c645f819e8ce2cf55b12421cbd79402a9aa4b41c717812e71595077eba2da919de1eb7251daee55dfd5a5ae456555f38' ;; 		aarch64) binArch='arm64'; checksum='d7b1edfa08eb5576d468b44d4c0ad2c5273ba27de4fc9dd0acc58e7a7c66bd3729cbf78a79f421377f26180ad13fbba323b37f471ce5daf9332c393cb649f348' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c74b1fc8794370b4fe8145fc4355655be41e03bab52637bd1374d8e91bee697145abd0cf3aa52bfd4f2b6f72874e901f8e7d9516f3f2b22dded6d1e6dd07a429' ;; 		riscv64) binArch='riscv64'; checksum='26340ad3b323eec3e62d1827a9f369b532a8b001423fa4d2f9b5aa9f5431c8327d0aa18bfc5b215c957016d80f4a4a5083fd6df6ede30a921835a5538f6baba3' ;; 		s390x)   binArch='s390x'; checksum='f17945253167d26038524bda89c8bf0ddd05774fc8baf5a22da136b989dacf696a24710e84d8fe694802c8accf0b0dff383093be8dc61537ae0536689ba9c366' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.1/caddy_2.11.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 23 Feb 2026 20:03:58 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 23 Feb 2026 20:03:58 GMT
ENV XDG_DATA_HOME=/data
# Mon, 23 Feb 2026 20:03:58 GMT
LABEL org.opencontainers.image.version=v2.11.1
# Mon, 23 Feb 2026 20:03:58 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 23 Feb 2026 20:03:58 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 23 Feb 2026 20:03:58 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 23 Feb 2026 20:03:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 23 Feb 2026 20:03:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 23 Feb 2026 20:03:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 23 Feb 2026 20:03:58 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 23 Feb 2026 20:03:58 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 20:03:58 GMT
EXPOSE map[443/tcp:{}]
# Mon, 23 Feb 2026 20:03:58 GMT
EXPOSE map[443/udp:{}]
# Mon, 23 Feb 2026 20:03:58 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 23 Feb 2026 20:03:58 GMT
WORKDIR /srv
# Mon, 23 Feb 2026 20:03:58 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bad5e15d6f1895fe9a8e04c10ef1f1587625bde6f4a47f52db5cdae0f86874`  
		Last Modified: Mon, 23 Feb 2026 20:04:06 GMT  
		Size: 2.9 MB (2888400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a7ae11c8e3c52bfefd847437dfed4291282124e8d173aee3e4b885642909eb`  
		Last Modified: Mon, 23 Feb 2026 20:04:05 GMT  
		Size: 7.5 KB (7501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7ea5ae3091afb1f6c3d30b0d6c9d4bc76451ad2e01968b8ea24babd298f386`  
		Last Modified: Mon, 23 Feb 2026 20:04:06 GMT  
		Size: 17.0 MB (16972333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:2aa687b431b42d3dc793e0e2d5f9ce46be5ca1b2020d79b7a2b713983cfd6448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.4 KB (353402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce2664077f1f6cfce62355e5980ad73fe7fd84820237ec79a113629d5883263`

```dockerfile
```

-	Layers:
	-	`sha256:eb061fc2fe463baf20d04f582a42dc80d60d50e8351515429e9b763db941f7e4`  
		Last Modified: Mon, 23 Feb 2026 20:04:05 GMT  
		Size: 335.0 KB (334972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d46078793871adc1723edded2ff61d489a6e9acbd16a2141b7eaa84820ebdd7`  
		Last Modified: Mon, 23 Feb 2026 20:04:05 GMT  
		Size: 18.4 KB (18430 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:cda96db30750b0c29f2225b032d3877a13b9f08d266c436a0e75892ddc835b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22513437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430b24aefc5abef35d6e8193853e220ed4840271e3032dcf709ab7e07fd07af3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 20:03:44 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Mon, 23 Feb 2026 20:03:44 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Mon, 23 Feb 2026 20:03:46 GMT
ENV CADDY_VERSION=v2.11.1
# Mon, 23 Feb 2026 20:03:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='cd194db2a730db0dbb343e9b468725d6bc31d915d977ed3fc79ae88af83fd0ad259d3560976a28c51ec5d9fd23a79980e71763eda5239beb8232e5adfa0a9707' ;; 		armhf)   binArch='armv6'; checksum='e1165b9375507781d9fec1d5a1ccb179b252911b40bfcb654d19dade298d12e7fc67ef494d2bd9ff99649b23540f666d35a41b9489c690317145130acbf400d1' ;; 		armv7)   binArch='armv7'; checksum='7c2dbe9cdac73ba8a3de4ec551a594c4c645f819e8ce2cf55b12421cbd79402a9aa4b41c717812e71595077eba2da919de1eb7251daee55dfd5a5ae456555f38' ;; 		aarch64) binArch='arm64'; checksum='d7b1edfa08eb5576d468b44d4c0ad2c5273ba27de4fc9dd0acc58e7a7c66bd3729cbf78a79f421377f26180ad13fbba323b37f471ce5daf9332c393cb649f348' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c74b1fc8794370b4fe8145fc4355655be41e03bab52637bd1374d8e91bee697145abd0cf3aa52bfd4f2b6f72874e901f8e7d9516f3f2b22dded6d1e6dd07a429' ;; 		riscv64) binArch='riscv64'; checksum='26340ad3b323eec3e62d1827a9f369b532a8b001423fa4d2f9b5aa9f5431c8327d0aa18bfc5b215c957016d80f4a4a5083fd6df6ede30a921835a5538f6baba3' ;; 		s390x)   binArch='s390x'; checksum='f17945253167d26038524bda89c8bf0ddd05774fc8baf5a22da136b989dacf696a24710e84d8fe694802c8accf0b0dff383093be8dc61537ae0536689ba9c366' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.1/caddy_2.11.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 23 Feb 2026 20:03:46 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 23 Feb 2026 20:03:46 GMT
ENV XDG_DATA_HOME=/data
# Mon, 23 Feb 2026 20:03:46 GMT
LABEL org.opencontainers.image.version=v2.11.1
# Mon, 23 Feb 2026 20:03:46 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 23 Feb 2026 20:03:46 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 23 Feb 2026 20:03:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 23 Feb 2026 20:03:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 23 Feb 2026 20:03:46 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 23 Feb 2026 20:03:46 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 23 Feb 2026 20:03:46 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 23 Feb 2026 20:03:46 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 20:03:46 GMT
EXPOSE map[443/tcp:{}]
# Mon, 23 Feb 2026 20:03:46 GMT
EXPOSE map[443/udp:{}]
# Mon, 23 Feb 2026 20:03:46 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 23 Feb 2026 20:03:46 GMT
WORKDIR /srv
# Mon, 23 Feb 2026 20:03:46 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be2574b9e9ffd98bc74dfea81282ddb00dca7d061aad11917806bfe903c8ce3`  
		Last Modified: Mon, 23 Feb 2026 20:03:51 GMT  
		Size: 2.8 MB (2825011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ecb84f03081be6aea416c0a9d55f71c18d1bfef0ce18f4657c8fb5b185656ec`  
		Last Modified: Mon, 23 Feb 2026 20:03:51 GMT  
		Size: 7.5 KB (7499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbfaa4c27a9c0dd8ff2c6e77961e1a24a0d279c026f6029f62b2a82bbd780ed`  
		Last Modified: Mon, 23 Feb 2026 20:03:52 GMT  
		Size: 16.1 MB (16111074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:19303a729bc857f48c13bdaccfc2a621133f0fee72648b0e3a31661d7a1da4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0f43a6d0a8443f399eb7cadf5579996132c3fd3625e8d92e00613b460fc4c8`

```dockerfile
```

-	Layers:
	-	`sha256:c364f6be8743a3b0db542d8d37eb5d43f0fadf479dffb179c950219fcb1d4162`  
		Last Modified: Mon, 23 Feb 2026 20:03:51 GMT  
		Size: 18.4 KB (18353 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:62246c0792a054d0e8385b7f717b305fd450a70d989da06b1bbe81e5d967e2a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22071628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f617ead75112e5573f6cd2db78274152f140d33fbaf6488c2cbfd2102e02c5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 20:03:40 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Mon, 23 Feb 2026 20:03:41 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Mon, 23 Feb 2026 20:03:43 GMT
ENV CADDY_VERSION=v2.11.1
# Mon, 23 Feb 2026 20:03:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='cd194db2a730db0dbb343e9b468725d6bc31d915d977ed3fc79ae88af83fd0ad259d3560976a28c51ec5d9fd23a79980e71763eda5239beb8232e5adfa0a9707' ;; 		armhf)   binArch='armv6'; checksum='e1165b9375507781d9fec1d5a1ccb179b252911b40bfcb654d19dade298d12e7fc67ef494d2bd9ff99649b23540f666d35a41b9489c690317145130acbf400d1' ;; 		armv7)   binArch='armv7'; checksum='7c2dbe9cdac73ba8a3de4ec551a594c4c645f819e8ce2cf55b12421cbd79402a9aa4b41c717812e71595077eba2da919de1eb7251daee55dfd5a5ae456555f38' ;; 		aarch64) binArch='arm64'; checksum='d7b1edfa08eb5576d468b44d4c0ad2c5273ba27de4fc9dd0acc58e7a7c66bd3729cbf78a79f421377f26180ad13fbba323b37f471ce5daf9332c393cb649f348' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c74b1fc8794370b4fe8145fc4355655be41e03bab52637bd1374d8e91bee697145abd0cf3aa52bfd4f2b6f72874e901f8e7d9516f3f2b22dded6d1e6dd07a429' ;; 		riscv64) binArch='riscv64'; checksum='26340ad3b323eec3e62d1827a9f369b532a8b001423fa4d2f9b5aa9f5431c8327d0aa18bfc5b215c957016d80f4a4a5083fd6df6ede30a921835a5538f6baba3' ;; 		s390x)   binArch='s390x'; checksum='f17945253167d26038524bda89c8bf0ddd05774fc8baf5a22da136b989dacf696a24710e84d8fe694802c8accf0b0dff383093be8dc61537ae0536689ba9c366' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.1/caddy_2.11.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 23 Feb 2026 20:03:43 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 23 Feb 2026 20:03:43 GMT
ENV XDG_DATA_HOME=/data
# Mon, 23 Feb 2026 20:03:43 GMT
LABEL org.opencontainers.image.version=v2.11.1
# Mon, 23 Feb 2026 20:03:43 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 23 Feb 2026 20:03:43 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 23 Feb 2026 20:03:43 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 23 Feb 2026 20:03:43 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 23 Feb 2026 20:03:43 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 23 Feb 2026 20:03:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 23 Feb 2026 20:03:43 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 23 Feb 2026 20:03:43 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 20:03:43 GMT
EXPOSE map[443/tcp:{}]
# Mon, 23 Feb 2026 20:03:43 GMT
EXPOSE map[443/udp:{}]
# Mon, 23 Feb 2026 20:03:43 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 23 Feb 2026 20:03:43 GMT
WORKDIR /srv
# Mon, 23 Feb 2026 20:03:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e38ca6cf1dcde7ed75612343ebff3e940dbfd867462e8d21b0ea76023abfd03`  
		Last Modified: Mon, 23 Feb 2026 20:03:50 GMT  
		Size: 2.7 MB (2687991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a5636a06b5951d0a41b7b1ef579306bd8abf36564cdf9cb9e0da44736c66b1`  
		Last Modified: Mon, 23 Feb 2026 20:03:50 GMT  
		Size: 7.5 KB (7501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b32e1a2a655c173570f8e38431a6147ff931c9264727fec98a06bcff056c152`  
		Last Modified: Mon, 23 Feb 2026 20:03:50 GMT  
		Size: 16.1 MB (16094380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:ffe60882f7834b868ac7eaaa8c2ae11eb550528b19d76c77489084feb3fae7c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.0 KB (352958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d1cacaa29501393abef56b3dd7e13150ceac751e440bd9f6b742b0eec8659b`

```dockerfile
```

-	Layers:
	-	`sha256:2b60e9eee8b8014b4585b4e42057800b44cc8bbf9576eb807c3fe65ed2bea94a`  
		Last Modified: Mon, 23 Feb 2026 20:03:50 GMT  
		Size: 334.4 KB (334390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48f4371ff0769a0dc1f04f59db96020ea2c87fe11771bc5d645b93b06c9a1dd9`  
		Last Modified: Mon, 23 Feb 2026 20:03:50 GMT  
		Size: 18.6 KB (18568 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:04536d2f7743aece51c9f80888ff255762ca0a93323602b039bf7e45cf8a263e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22577114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa2217f6abcf03ab4e3dc0c9d01e6a44c688c3a422cb2632223f3548e0a757a4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 20:03:53 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Mon, 23 Feb 2026 20:03:54 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Mon, 23 Feb 2026 20:03:55 GMT
ENV CADDY_VERSION=v2.11.1
# Mon, 23 Feb 2026 20:03:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='cd194db2a730db0dbb343e9b468725d6bc31d915d977ed3fc79ae88af83fd0ad259d3560976a28c51ec5d9fd23a79980e71763eda5239beb8232e5adfa0a9707' ;; 		armhf)   binArch='armv6'; checksum='e1165b9375507781d9fec1d5a1ccb179b252911b40bfcb654d19dade298d12e7fc67ef494d2bd9ff99649b23540f666d35a41b9489c690317145130acbf400d1' ;; 		armv7)   binArch='armv7'; checksum='7c2dbe9cdac73ba8a3de4ec551a594c4c645f819e8ce2cf55b12421cbd79402a9aa4b41c717812e71595077eba2da919de1eb7251daee55dfd5a5ae456555f38' ;; 		aarch64) binArch='arm64'; checksum='d7b1edfa08eb5576d468b44d4c0ad2c5273ba27de4fc9dd0acc58e7a7c66bd3729cbf78a79f421377f26180ad13fbba323b37f471ce5daf9332c393cb649f348' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c74b1fc8794370b4fe8145fc4355655be41e03bab52637bd1374d8e91bee697145abd0cf3aa52bfd4f2b6f72874e901f8e7d9516f3f2b22dded6d1e6dd07a429' ;; 		riscv64) binArch='riscv64'; checksum='26340ad3b323eec3e62d1827a9f369b532a8b001423fa4d2f9b5aa9f5431c8327d0aa18bfc5b215c957016d80f4a4a5083fd6df6ede30a921835a5538f6baba3' ;; 		s390x)   binArch='s390x'; checksum='f17945253167d26038524bda89c8bf0ddd05774fc8baf5a22da136b989dacf696a24710e84d8fe694802c8accf0b0dff383093be8dc61537ae0536689ba9c366' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.1/caddy_2.11.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 23 Feb 2026 20:03:55 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 23 Feb 2026 20:03:55 GMT
ENV XDG_DATA_HOME=/data
# Mon, 23 Feb 2026 20:03:55 GMT
LABEL org.opencontainers.image.version=v2.11.1
# Mon, 23 Feb 2026 20:03:55 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 23 Feb 2026 20:03:55 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 23 Feb 2026 20:03:55 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 23 Feb 2026 20:03:55 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 23 Feb 2026 20:03:55 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 23 Feb 2026 20:03:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 23 Feb 2026 20:03:55 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 23 Feb 2026 20:03:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 20:03:55 GMT
EXPOSE map[443/tcp:{}]
# Mon, 23 Feb 2026 20:03:55 GMT
EXPOSE map[443/udp:{}]
# Mon, 23 Feb 2026 20:03:55 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 23 Feb 2026 20:03:55 GMT
WORKDIR /srv
# Mon, 23 Feb 2026 20:03:55 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38bb188f7127cfd8ab6b538de27e100d4279cc04a754763452431cbdfb73df5`  
		Last Modified: Mon, 23 Feb 2026 20:04:02 GMT  
		Size: 2.9 MB (2904361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86208d879c92c874fb5b0f3c556236132f4bdb0836d352748439a1865c9f537`  
		Last Modified: Mon, 23 Feb 2026 20:04:01 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e130f118fb4e318a957526bd72155cc8c96e5fe46df04a6ed0939c48b44b7c`  
		Last Modified: Mon, 23 Feb 2026 20:04:02 GMT  
		Size: 15.5 MB (15468127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:edf0448f995cc59512a08272fecc1bd4d07e94ce6cec48c925878841125ee82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.0 KB (353038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775e11b98c07e5b3bb7366d5b42e6cd7e94fc86d71e10c0f0e798993705e3117`

```dockerfile
```

-	Layers:
	-	`sha256:5c88aa9a0084693a1bd425b51232a6df12a1c03fcecc36e126dfdc380a48b9d9`  
		Last Modified: Mon, 23 Feb 2026 20:04:02 GMT  
		Size: 334.4 KB (334426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80f65cc5a8eda2485f5be86b278b1112609776db9ec00d2ece2e5a60b7edbd33`  
		Last Modified: Mon, 23 Feb 2026 20:04:01 GMT  
		Size: 18.6 KB (18612 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:abcb70fb265c36a8e013525cb3b6eb6bac9f340fdaa095ac77d519ba96f4a9e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22328635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b30c2c121c56098bc953dd891881d83b0e17c85b67191506369252080489242`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:26:19 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Wed, 11 Feb 2026 18:26:21 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Mon, 23 Feb 2026 20:03:18 GMT
ENV CADDY_VERSION=v2.11.1
# Mon, 23 Feb 2026 20:03:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='cd194db2a730db0dbb343e9b468725d6bc31d915d977ed3fc79ae88af83fd0ad259d3560976a28c51ec5d9fd23a79980e71763eda5239beb8232e5adfa0a9707' ;; 		armhf)   binArch='armv6'; checksum='e1165b9375507781d9fec1d5a1ccb179b252911b40bfcb654d19dade298d12e7fc67ef494d2bd9ff99649b23540f666d35a41b9489c690317145130acbf400d1' ;; 		armv7)   binArch='armv7'; checksum='7c2dbe9cdac73ba8a3de4ec551a594c4c645f819e8ce2cf55b12421cbd79402a9aa4b41c717812e71595077eba2da919de1eb7251daee55dfd5a5ae456555f38' ;; 		aarch64) binArch='arm64'; checksum='d7b1edfa08eb5576d468b44d4c0ad2c5273ba27de4fc9dd0acc58e7a7c66bd3729cbf78a79f421377f26180ad13fbba323b37f471ce5daf9332c393cb649f348' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c74b1fc8794370b4fe8145fc4355655be41e03bab52637bd1374d8e91bee697145abd0cf3aa52bfd4f2b6f72874e901f8e7d9516f3f2b22dded6d1e6dd07a429' ;; 		riscv64) binArch='riscv64'; checksum='26340ad3b323eec3e62d1827a9f369b532a8b001423fa4d2f9b5aa9f5431c8327d0aa18bfc5b215c957016d80f4a4a5083fd6df6ede30a921835a5538f6baba3' ;; 		s390x)   binArch='s390x'; checksum='f17945253167d26038524bda89c8bf0ddd05774fc8baf5a22da136b989dacf696a24710e84d8fe694802c8accf0b0dff383093be8dc61537ae0536689ba9c366' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.1/caddy_2.11.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 23 Feb 2026 20:03:18 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 23 Feb 2026 20:03:18 GMT
ENV XDG_DATA_HOME=/data
# Mon, 23 Feb 2026 20:03:18 GMT
LABEL org.opencontainers.image.version=v2.11.1
# Mon, 23 Feb 2026 20:03:18 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 23 Feb 2026 20:03:18 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 23 Feb 2026 20:03:18 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 23 Feb 2026 20:03:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 23 Feb 2026 20:03:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 23 Feb 2026 20:03:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 23 Feb 2026 20:03:18 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 23 Feb 2026 20:03:18 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 20:03:18 GMT
EXPOSE map[443/tcp:{}]
# Mon, 23 Feb 2026 20:03:18 GMT
EXPOSE map[443/udp:{}]
# Mon, 23 Feb 2026 20:03:18 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 23 Feb 2026 20:03:19 GMT
WORKDIR /srv
# Mon, 23 Feb 2026 20:03:19 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81709d7071fd127789b5207997f472bea24464f745bf287c5e2ae9b9c2180717`  
		Last Modified: Wed, 11 Feb 2026 18:26:45 GMT  
		Size: 3.0 MB (3028403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969730299b462827c9b93ff86f0faf2e1e3cf04a752eb1d2e086f75a5fc0a49e`  
		Last Modified: Wed, 11 Feb 2026 18:26:44 GMT  
		Size: 7.5 KB (7503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607b84945c74a5cbe7b4f544ab5d3ee01d979abe1b888c58dfe0ba61378304d`  
		Last Modified: Mon, 23 Feb 2026 20:03:36 GMT  
		Size: 15.5 MB (15463054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:4f6b8dd03e195cab0a95c6f66846d1f3f7c4b6e83f2fd4bae9b21e40d6b38fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.9 KB (352880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e00783e73be802a23e5a1c9dbe7283fd7862bc7f25f34617f92830d2a94146`

```dockerfile
```

-	Layers:
	-	`sha256:d7a1ff22972498a2ef0c85a17a237855f1dfe5da727615d7f3bf13a03a9594c8`  
		Last Modified: Mon, 23 Feb 2026 20:03:35 GMT  
		Size: 334.4 KB (334379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f2fb13dd0b8dd3051bc762f45582da11d1718e7ee7291947d0051f1e17f0072`  
		Last Modified: Mon, 23 Feb 2026 20:03:35 GMT  
		Size: 18.5 KB (18501 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:3ebe7ba0d3aa3d6e0ae75d40321f7a3a0d8f4f08c13305ab846df10c06d94be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22623947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e8280a35b58fb63b3f5d746de46554ff836cc50cfee2bb0e0178bfc8672b49`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 02:47:18 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Tue, 24 Feb 2026 02:47:20 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Tue, 24 Feb 2026 02:47:26 GMT
ENV CADDY_VERSION=v2.11.1
# Tue, 24 Feb 2026 02:47:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='cd194db2a730db0dbb343e9b468725d6bc31d915d977ed3fc79ae88af83fd0ad259d3560976a28c51ec5d9fd23a79980e71763eda5239beb8232e5adfa0a9707' ;; 		armhf)   binArch='armv6'; checksum='e1165b9375507781d9fec1d5a1ccb179b252911b40bfcb654d19dade298d12e7fc67ef494d2bd9ff99649b23540f666d35a41b9489c690317145130acbf400d1' ;; 		armv7)   binArch='armv7'; checksum='7c2dbe9cdac73ba8a3de4ec551a594c4c645f819e8ce2cf55b12421cbd79402a9aa4b41c717812e71595077eba2da919de1eb7251daee55dfd5a5ae456555f38' ;; 		aarch64) binArch='arm64'; checksum='d7b1edfa08eb5576d468b44d4c0ad2c5273ba27de4fc9dd0acc58e7a7c66bd3729cbf78a79f421377f26180ad13fbba323b37f471ce5daf9332c393cb649f348' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c74b1fc8794370b4fe8145fc4355655be41e03bab52637bd1374d8e91bee697145abd0cf3aa52bfd4f2b6f72874e901f8e7d9516f3f2b22dded6d1e6dd07a429' ;; 		riscv64) binArch='riscv64'; checksum='26340ad3b323eec3e62d1827a9f369b532a8b001423fa4d2f9b5aa9f5431c8327d0aa18bfc5b215c957016d80f4a4a5083fd6df6ede30a921835a5538f6baba3' ;; 		s390x)   binArch='s390x'; checksum='f17945253167d26038524bda89c8bf0ddd05774fc8baf5a22da136b989dacf696a24710e84d8fe694802c8accf0b0dff383093be8dc61537ae0536689ba9c366' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.1/caddy_2.11.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 24 Feb 2026 02:47:26 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 24 Feb 2026 02:47:26 GMT
ENV XDG_DATA_HOME=/data
# Tue, 24 Feb 2026 02:47:26 GMT
LABEL org.opencontainers.image.version=v2.11.1
# Tue, 24 Feb 2026 02:47:26 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 24 Feb 2026 02:47:26 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 24 Feb 2026 02:47:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 24 Feb 2026 02:47:26 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 24 Feb 2026 02:47:26 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 24 Feb 2026 02:47:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 24 Feb 2026 02:47:26 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 24 Feb 2026 02:47:26 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 02:47:26 GMT
EXPOSE map[443/tcp:{}]
# Tue, 24 Feb 2026 02:47:26 GMT
EXPOSE map[443/udp:{}]
# Tue, 24 Feb 2026 02:47:26 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 24 Feb 2026 02:47:26 GMT
WORKDIR /srv
# Tue, 24 Feb 2026 02:47:26 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9b2cc29851eabf70e0bfefee2736addb5021151f3b22cdaae94aabb6eb5f79`  
		Last Modified: Tue, 24 Feb 2026 02:48:13 GMT  
		Size: 3.0 MB (3029875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc045436bc64a22522ca8e688a83de035cc70998b5c626773a79a31369a3b86a`  
		Last Modified: Tue, 24 Feb 2026 02:48:12 GMT  
		Size: 7.5 KB (7505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386f24cffc6aa44cd3408b185040a40087cb289117bd27b269225a16aa29dcf4`  
		Last Modified: Tue, 24 Feb 2026 02:48:15 GMT  
		Size: 16.0 MB (16001248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:79d61831865218b4ca47d75f672ad8945181bf373681760b9d51ae4e6c66f49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.9 KB (352877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b6a322990bced393710c353316f4739b24085c24c929a9f9d747c9291777cd`

```dockerfile
```

-	Layers:
	-	`sha256:637e842aa837f9dad3184ae614bc30a66114e899f4d597a0376929daddb3371d`  
		Last Modified: Tue, 24 Feb 2026 02:48:13 GMT  
		Size: 334.4 KB (334375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e0094a29744ddc682ea37d3522788aae5093c4fae395a08c4508853259437df`  
		Last Modified: Tue, 24 Feb 2026 02:48:12 GMT  
		Size: 18.5 KB (18502 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:alpine` - linux; s390x

```console
$ docker pull caddy@sha256:8b1e029d20e5e1a7f0413885967028ad7f6fcb38f12dfa9b2b6af90fc1ac9aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23098427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:315903de5d2edcabf499e8fdf571f5aa6dd485c2c2c0428bf94758e7ab755a4f`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 20:03:33 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	libcap 	mailcap # buildkit
# Mon, 23 Feb 2026 20:03:35 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	chmod 1777 /config/caddy /data/caddy; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html" # buildkit
# Mon, 23 Feb 2026 20:03:39 GMT
ENV CADDY_VERSION=v2.11.1
# Mon, 23 Feb 2026 20:03:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='cd194db2a730db0dbb343e9b468725d6bc31d915d977ed3fc79ae88af83fd0ad259d3560976a28c51ec5d9fd23a79980e71763eda5239beb8232e5adfa0a9707' ;; 		armhf)   binArch='armv6'; checksum='e1165b9375507781d9fec1d5a1ccb179b252911b40bfcb654d19dade298d12e7fc67ef494d2bd9ff99649b23540f666d35a41b9489c690317145130acbf400d1' ;; 		armv7)   binArch='armv7'; checksum='7c2dbe9cdac73ba8a3de4ec551a594c4c645f819e8ce2cf55b12421cbd79402a9aa4b41c717812e71595077eba2da919de1eb7251daee55dfd5a5ae456555f38' ;; 		aarch64) binArch='arm64'; checksum='d7b1edfa08eb5576d468b44d4c0ad2c5273ba27de4fc9dd0acc58e7a7c66bd3729cbf78a79f421377f26180ad13fbba323b37f471ce5daf9332c393cb649f348' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='c74b1fc8794370b4fe8145fc4355655be41e03bab52637bd1374d8e91bee697145abd0cf3aa52bfd4f2b6f72874e901f8e7d9516f3f2b22dded6d1e6dd07a429' ;; 		riscv64) binArch='riscv64'; checksum='26340ad3b323eec3e62d1827a9f369b532a8b001423fa4d2f9b5aa9f5431c8327d0aa18bfc5b215c957016d80f4a4a5083fd6df6ede30a921835a5538f6baba3' ;; 		s390x)   binArch='s390x'; checksum='f17945253167d26038524bda89c8bf0ddd05774fc8baf5a22da136b989dacf696a24710e84d8fe694802c8accf0b0dff383093be8dc61537ae0536689ba9c366' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.11.1/caddy_2.11.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Mon, 23 Feb 2026 20:03:39 GMT
ENV XDG_CONFIG_HOME=/config
# Mon, 23 Feb 2026 20:03:39 GMT
ENV XDG_DATA_HOME=/data
# Mon, 23 Feb 2026 20:03:39 GMT
LABEL org.opencontainers.image.version=v2.11.1
# Mon, 23 Feb 2026 20:03:39 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 23 Feb 2026 20:03:39 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 23 Feb 2026 20:03:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 23 Feb 2026 20:03:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 23 Feb 2026 20:03:39 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 23 Feb 2026 20:03:39 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 23 Feb 2026 20:03:39 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 23 Feb 2026 20:03:39 GMT
EXPOSE map[80/tcp:{}]
# Mon, 23 Feb 2026 20:03:39 GMT
EXPOSE map[443/tcp:{}]
# Mon, 23 Feb 2026 20:03:39 GMT
EXPOSE map[443/udp:{}]
# Mon, 23 Feb 2026 20:03:39 GMT
EXPOSE map[2019/tcp:{}]
# Mon, 23 Feb 2026 20:03:40 GMT
WORKDIR /srv
# Mon, 23 Feb 2026 20:03:40 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe4bb2a906bef081b18638228108ebe9143313a3e23e97a6c339943b566d9aa`  
		Last Modified: Mon, 23 Feb 2026 20:04:02 GMT  
		Size: 3.0 MB (3017729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67681816d38a5021e6f5faf0b35fd0ebeb0bb60676596ce555a98b2155701564`  
		Last Modified: Mon, 23 Feb 2026 20:04:02 GMT  
		Size: 7.5 KB (7502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20ea3f1557a8ba1fefb67de16207b40038e7ff93ad93ba14fd673b8f98df42d`  
		Last Modified: Mon, 23 Feb 2026 20:04:02 GMT  
		Size: 16.3 MB (16347831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:93527caf7b7a98004ea1348b572100b7fa0848c1145807bf45aa4be24134649b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.8 KB (352751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5333e290db971eed81aff8995ab3931bc8deb760b36d880806d2e730e4a4413`

```dockerfile
```

-	Layers:
	-	`sha256:1d9993ef2a678417d917d154309aba5387ffdc2a68c0f2f329dd57954fa58e9f`  
		Last Modified: Mon, 23 Feb 2026 20:04:02 GMT  
		Size: 334.3 KB (334321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb472ad82d31bfa602a67ea397842217263cc20f166eb84edeeb3a8d5126b5d6`  
		Last Modified: Mon, 23 Feb 2026 20:04:02 GMT  
		Size: 18.4 KB (18430 bytes)  
		MIME: application/vnd.in-toto+json
