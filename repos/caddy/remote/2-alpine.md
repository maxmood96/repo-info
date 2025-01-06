## `caddy:2-alpine`

```console
$ docker pull caddy@sha256:e97e0e3f8f51be708a9d5fadbbd75e3398c22fc0eecd4b26d48561e3f7daa9eb
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

### `caddy:2-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:69f9a2cd92221b45258a5728b3f08c9b03ba03ed27e0ac791b4343400c3e7385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 MB (18625819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa9a2c5676288c88ffa3ae9812dd7eb5ddeed8c06245b3f8fa181e9dfcf6601`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		riscv64) binArch='riscv64'; checksum='67ce559ca785f05b54b587f91f12f8c4c46a7d14e3f72772f14922b672417473b4e76ab61dd939b9b710889ca3a0604cd7f4c78ccba8e6dbfd5fd5193d9bf719' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /srv
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f2636bb565977eac2181eb6f095824febc32cfb1fa8b5f2b74dbd664031638`  
		Last Modified: Tue, 12 Nov 2024 02:21:50 GMT  
		Size: 355.5 KB (355496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b667dcdaab274461f78f562875abc47be7e3db2dcf2c9f5a2b331a3754fb35e4`  
		Last Modified: Tue, 12 Nov 2024 02:21:50 GMT  
		Size: 7.5 KB (7453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e24303ace2224cc9aabb3349ff7a08bea09f9bab509b5cc86553dcb11490e9`  
		Last Modified: Tue, 12 Nov 2024 02:21:51 GMT  
		Size: 14.6 MB (14638934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:644c2f11ab9a3b3499fa695684f277415ed28c7b74f5525f8b9a91d2133e8193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.7 KB (303690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac594f95c8e790a75fc91ef1bfab300375535ae99fcf0618ea6eef4192604eec`

```dockerfile
```

-	Layers:
	-	`sha256:f86a078fd51d204d2ae50c52e6742d0b03910bfe031b414bd9bfbcc156769dd3`  
		Last Modified: Tue, 12 Nov 2024 02:21:50 GMT  
		Size: 285.4 KB (285433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1a269ce835318d2dd271cf4d4bed82c31002cf2f4896aa122e3235c4c4ffd71`  
		Last Modified: Tue, 12 Nov 2024 02:21:50 GMT  
		Size: 18.3 KB (18257 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:3a64bb7b5d8eb7c416d4bcd6f66d9ded73dbb4b9c4b45267fd9f37bedaa9a998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17495861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4746d29e08c14ce3f7fd6f3ea506514ac529a698e910fcd7e621ceb4341c9e5`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		riscv64) binArch='riscv64'; checksum='67ce559ca785f05b54b587f91f12f8c4c46a7d14e3f72772f14922b672417473b4e76ab61dd939b9b710889ca3a0604cd7f4c78ccba8e6dbfd5fd5193d9bf719' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /srv
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d2c38b04a4e560f4869ada6c37157d2529e07c40a29776b57eb947e96ecf6a`  
		Last Modified: Tue, 12 Nov 2024 15:32:45 GMT  
		Size: 355.9 KB (355945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb82bddddfab59bc95946f732ef9fb231160b144905f27579ca01a77124245cc`  
		Last Modified: Tue, 12 Nov 2024 15:33:17 GMT  
		Size: 7.5 KB (7453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e64cdd2a6d4fd28b7d6fa6a34b700a7eee93b4cc5d58cf9e43e99ea2f417152`  
		Last Modified: Tue, 12 Nov 2024 15:33:18 GMT  
		Size: 13.8 MB (13765835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:20b38ff7b51dc8ec5af08b97c18f812d8e494cddb19ba14a9b36616c9c4490a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc79bc952f90c80f7b4587c1dc6743ff00c8a9ff08bb03d581c5429625315e1e`

```dockerfile
```

-	Layers:
	-	`sha256:fca633f1c79da144c783d39f60c4314684df27ab0084c54bf541e47ca3e9306f`  
		Last Modified: Tue, 12 Nov 2024 15:33:17 GMT  
		Size: 18.2 KB (18176 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:96a6944c60115111f417652a087cf4df604e4568812784ee7260665a537bc723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17195015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6117083d1946ceab06ef9f4e6cfc88fb1399ff6bba36af846fe6b3caf5637a48`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		riscv64) binArch='riscv64'; checksum='67ce559ca785f05b54b587f91f12f8c4c46a7d14e3f72772f14922b672417473b4e76ab61dd939b9b710889ca3a0604cd7f4c78ccba8e6dbfd5fd5193d9bf719' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /srv
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfacd796f78a14b4e1122ff5265c27fa560747234674711f9d2ad0db9cc28c6`  
		Size: 352.2 KB (352193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb7bf0a26cc070f0e5bcc4c2bfd4f46e378b9ecca58d751d3f5178cb68e5428`  
		Last Modified: Wed, 13 Nov 2024 06:48:14 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1c4e0ee85189c75ae49cff932f7647130de97aefbfc61dbaa99c635a43c273`  
		Last Modified: Wed, 13 Nov 2024 06:48:15 GMT  
		Size: 13.7 MB (13739851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:4cc512e129ded702130868aaeac9670c5e3ad4bbf129bc1f59cf5a4f46841fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 KB (303892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26550c53e5312ce1d479b1ab7877ffcd8dc8d2cd21cfb96e463137ff9b2866fc`

```dockerfile
```

-	Layers:
	-	`sha256:ac4b63888007f61d55d9e90a004f2b90df672dfa97a6f56744a0c3d95e50e2e0`  
		Last Modified: Wed, 13 Nov 2024 06:48:14 GMT  
		Size: 285.5 KB (285501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fed2da771b610ba8728ae4ffeb48280f8ca090ba8b7aff674dd1225775f0442`  
		Last Modified: Wed, 13 Nov 2024 06:48:14 GMT  
		Size: 18.4 KB (18391 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:b2899a6a0eed5aa536ba82869581dde4b5063325dd94ab06b104f4d01999895e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18014037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a41ccd1eab8d9f8b7b72a26735725c0378c4465406acf1f07c6f444bafa5a4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		riscv64) binArch='riscv64'; checksum='67ce559ca785f05b54b587f91f12f8c4c46a7d14e3f72772f14922b672417473b4e76ab61dd939b9b710889ca3a0604cd7f4c78ccba8e6dbfd5fd5193d9bf719' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /srv
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ba1ff97d794a97638e1c38050d57a8f3e8673e8298c948f95a9ec6d88fe4a6`  
		Last Modified: Wed, 13 Nov 2024 00:58:06 GMT  
		Size: 367.8 KB (367760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad30cb28148d1e71b958324ef05b28a78912322d3becd97ab643b8d4a596073`  
		Last Modified: Wed, 13 Nov 2024 00:58:38 GMT  
		Size: 7.5 KB (7454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c043e1630daf678b2ba41744e50eb188364bc49cd8bccf6afadf12c8a3736e7b`  
		Last Modified: Wed, 13 Nov 2024 00:58:38 GMT  
		Size: 13.6 MB (13551065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:0906aa813e0af867c083c755bb42a6af9febe0dded2881bff1a798594523692b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 KB (303976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157f32854719be2567338b54af678862fe37295d61301bec497e80f59c4bc9b2`

```dockerfile
```

-	Layers:
	-	`sha256:8631c8053b80dba8f51c6f2b9ce3c527a6734fa8ce78c1cc729f26ab2749b846`  
		Last Modified: Wed, 13 Nov 2024 00:58:38 GMT  
		Size: 285.5 KB (285537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ff78a68e7f0c0f09ea385d456ca273c7f1870bcda959d5aa7c8fc71c5efbfe3`  
		Last Modified: Wed, 13 Nov 2024 00:58:38 GMT  
		Size: 18.4 KB (18439 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:766758e8a8e4b583451e1a20975cbc8ed4c0c525745e40cbbe1b81fea3017c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17241025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b9a5e094aaaa8af04dcfcdebe15e7dd08305ff1ec63d0e3d8e94ae2decd563`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		riscv64) binArch='riscv64'; checksum='67ce559ca785f05b54b587f91f12f8c4c46a7d14e3f72772f14922b672417473b4e76ab61dd939b9b710889ca3a0604cd7f4c78ccba8e6dbfd5fd5193d9bf719' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /srv
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1caca72f7c01a6c3a145f50a8b3384f294c2cfd49724ffa40b62a7e2c26fd1ac`  
		Last Modified: Tue, 12 Nov 2024 14:56:23 GMT  
		Size: 369.0 KB (369046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a9c5a43d085eb5400fc8ff0269f07bda1e0217d4d2dc9744f184fe5e454b47`  
		Last Modified: Tue, 12 Nov 2024 14:57:11 GMT  
		Size: 7.5 KB (7453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b74b926ef92ceb8fa8e5de4ece9e33fde7fd28e78acfe72d448b7193c88739`  
		Last Modified: Tue, 12 Nov 2024 14:57:12 GMT  
		Size: 13.3 MB (13292035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:b13b77e473ecc507a6970bc27eb60e8b225e2b9bae0547df14bad9617757f00e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.9 KB (301866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8955ece544861ac917b562b15a1207c513481eed800ef6d24f249fc648b094c8`

```dockerfile
```

-	Layers:
	-	`sha256:01f31ec9b803ec964376d0de06e3d82e7291a78ac37e79f898a3671442f312d9`  
		Last Modified: Tue, 12 Nov 2024 14:57:11 GMT  
		Size: 283.5 KB (283537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90db314f14eb56a16e3c71bf34934752f3ea694992cc6e9937bda5a9cb39969b`  
		Last Modified: Tue, 12 Nov 2024 14:57:11 GMT  
		Size: 18.3 KB (18329 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:f70704a0c9b4084b305b581c3a123df1e333782a5724a474a82fca9e223f4656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17597056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3e0caf24dfdbb872ea87925f2f2939d4653769cae723611b072bb9814a13c0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		riscv64) binArch='riscv64'; checksum='67ce559ca785f05b54b587f91f12f8c4c46a7d14e3f72772f14922b672417473b4e76ab61dd939b9b710889ca3a0604cd7f4c78ccba8e6dbfd5fd5193d9bf719' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /srv
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e4791757fafc8d5ec76994945b7f221ee3a7f72dce5e8491588396b4fd14a`  
		Last Modified: Wed, 13 Nov 2024 11:39:51 GMT  
		Size: 359.1 KB (359083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc9a07b9f1eb5b75ed09670e492ddfe159df28c722bc5037b4baa2b69a079a4`  
		Last Modified: Wed, 13 Nov 2024 11:41:05 GMT  
		Size: 7.5 KB (7452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f20d0a82f11dde912d4a6d263412df88a3100e9cbc82d72f893baae5f5de6c1`  
		Last Modified: Wed, 13 Nov 2024 11:41:08 GMT  
		Size: 13.9 MB (13859007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e512d9e3dcfdfc8eaefc5fd9e4d36efc271021f1f32f26df279c06c42cb45341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.9 KB (301862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11891f5e5a63f816a6c4a701994757464a3dd559545082ca5a0327bc2adf4fcf`

```dockerfile
```

-	Layers:
	-	`sha256:a54c64a9e3f6af4b319410f1ab337d6211aff9d5544b7a7f05bddd04002d169e`  
		Size: 283.5 KB (283533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fa2b6c9c4d6cedf08e5cf26aa83277da3d69b5368c604ef630a28b87d692d86`  
		Last Modified: Wed, 13 Nov 2024 11:41:05 GMT  
		Size: 18.3 KB (18329 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:066a7da46f473ef6fb5f4f6009a5ab208f0887469566dffbf9fb09c108182df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17988412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce116b5826a93ea4cb2fa6f1fdeb2be35af77cb70e28160a19da961cad80e76`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	libcap 	mailcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	mkdir -p 		/config/caddy 		/data/caddy 		/etc/caddy 		/usr/share/caddy 	; 	wget -O /etc/caddy/Caddyfile "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"; 	wget -O /usr/share/caddy/index.html "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='b8bec15d14fb033562af9f207850027bcbaa1f891edc9efe00d38bf39e1bf9944f8b6b8eba041ddd4c171cd70c905174c704d705be2f23bc678fe1eaf37a2485' ;; 		armhf)   binArch='armv6'; checksum='640536eee0645342a8cb3bfe6ca3ad5bce8a22fee371eb295192d4e95971802a4f4dbe3a188d2be577762547f713e8ac708f8e9b6acf4806cdf509ce54954eac' ;; 		armv7)   binArch='armv7'; checksum='8aecf8866a6dbdc46d550d2d957afc26dd262a8fa1fd6feb122df961ef57d2301b720556e6ff180f1ea0ae19e13f1cc6ea9935eae58efb68b8821aebffe989f1' ;; 		aarch64) binArch='arm64'; checksum='5466234be3e988071cef937aedbdd94c15b6f75cf7307397e67c2641219ac9bfe2c2bb3b31fc05bc68d3b6398bbe50abfa16ccf3b127318ccac31115ad26507c' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='90c4a779f52b86d4b615a15acdec01db986a88fb606ca11145c21cfc4e64b417296fe0a54416f2c295600f8a2994a073a40028b1b1583403b416464bf39de173' ;; 		riscv64) binArch='riscv64'; checksum='67ce559ca785f05b54b587f91f12f8c4c46a7d14e3f72772f14922b672417473b4e76ab61dd939b9b710889ca3a0604cd7f4c78ccba8e6dbfd5fd5193d9bf719' ;; 		s390x)   binArch='s390x'; checksum='ed67cecdb9f50379d75805ebeb687183f096d3206cef053b768e87eceb4472fd568f47ef8fe0939f019f38e298a3a41243ba9caa193f57e7b29e4daa700898bc' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/caddy.tar.gz "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/caddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/caddy.tar.gz -C /usr/bin caddy; 	rm -f /tmp/caddy.tar.gz; 	setcap cap_net_bind_service=+ep /usr/bin/caddy; 	chmod +x /usr/bin/caddy; 	caddy version # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_CONFIG_HOME=/config
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XDG_DATA_HOME=/data
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.title=Caddy
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 04 Jun 2024 22:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[443/udp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
EXPOSE map[2019/tcp:{}]
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /srv
# Tue, 04 Jun 2024 22:12:59 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853e6c2d77b7ec3a04a5632cc1fcc559f0ef74dcd2a80e3afd3e5c2b58f8e2ba`  
		Last Modified: Tue, 12 Nov 2024 22:28:45 GMT  
		Size: 363.2 KB (363179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda79e51805cc63db21e2ed55562117dc70dbe97261dc2148de03ea54c9dc07a`  
		Last Modified: Tue, 12 Nov 2024 22:29:40 GMT  
		Size: 7.5 KB (7453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d3ee0f58d8bd3a64030d86ffb52bad170d1d4cfbeb34c195e6a0e0245f0a66`  
		Last Modified: Tue, 12 Nov 2024 22:29:40 GMT  
		Size: 14.2 MB (14156140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:5e7234ff7832023859c8b95397f424924067f4d346780cf3ea1011ef9f44ba91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 KB (301736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6508353f081e66048325e60213999c0ddff0ae89431bbcc611bde9698b883332`

```dockerfile
```

-	Layers:
	-	`sha256:325b9ca3f5d091d24df1eb0e89d09585f4eaf2f6850f6be08e8c3eec7f11a112`  
		Last Modified: Tue, 12 Nov 2024 22:29:40 GMT  
		Size: 283.5 KB (283479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32883847cc6c6714b7b758e87098c85fe3afbbe5f86495abd902f815fdf4a6c`  
		Last Modified: Tue, 12 Nov 2024 22:29:40 GMT  
		Size: 18.3 KB (18257 bytes)  
		MIME: application/vnd.in-toto+json
