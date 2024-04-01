<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.9`](#eggdrop19)
-	[`eggdrop:1.9.5`](#eggdrop195)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.9`

```console
$ docker pull eggdrop@sha256:80cb83320a4382fe26261bd37bc3775605583ef7fe7af4a2613b93e00a1d59fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9` - linux; amd64

```console
$ docker pull eggdrop@sha256:34a38b278b4fe46c1b431fcf7dfa6cbac1615246172272129b9208d0d2fa8bd4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680b372bebae349d2d30d7d1885053541c90be76f8b4cc32415f7d940836dc13`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:14:11 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 16 Mar 2024 06:14:11 GMT
RUN adduser -S eggdrop
# Sat, 16 Mar 2024 06:14:13 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 16 Mar 2024 06:14:14 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 16 Mar 2024 06:18:03 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 16 Mar 2024 06:18:03 GMT
ENV NICK=
# Sat, 16 Mar 2024 06:18:03 GMT
ENV SERVER=
# Sat, 16 Mar 2024 06:18:03 GMT
ENV LISTEN=3333
# Sat, 16 Mar 2024 06:18:03 GMT
ENV OWNER=
# Sat, 16 Mar 2024 06:18:03 GMT
ENV USERFILE=eggdrop.user
# Sat, 16 Mar 2024 06:18:03 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 16 Mar 2024 06:18:03 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 16 Mar 2024 06:18:03 GMT
EXPOSE 3333
# Sat, 16 Mar 2024 06:18:04 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 16 Mar 2024 06:18:04 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 16 Mar 2024 06:18:04 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 16 Mar 2024 06:18:04 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c630ff352121cf34896e97408532ee11e27a42505c86d429d155280ccb8002`  
		Last Modified: Sat, 16 Mar 2024 06:18:34 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb419fa2bf132049b023b1393209d0b8836e6a7598b618c2dbee91036dc922f7`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 11.0 KB (10954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b4a85b3c8cbd4a52ab562b3e5909758273e37b541cdc144e2a07fc4a329f84`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 2.8 MB (2758094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91429a382ad8f8d515a3269ac11d856c4a69a1062217035b56747b603c5fd9b3`  
		Last Modified: Sat, 16 Mar 2024 06:18:34 GMT  
		Size: 6.1 MB (6146820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c61fc1b45ec89476a85feefd5ae3515f358e5255fc53b9611732f34f49355`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe2aee5f06911bbd805d8dc9d6beedd17ff7a25f96fbb1dc1ba70732675d433`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:dd6d6710745b8807a747a3131d778c60522010d6bfb6dfb87c8e3269e16b94d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11364455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b737f04cfea3721350fa28d59e56750a460811baeaa4a3d4f64fa878a7e9396`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:26 GMT
ADD file:66e93ac5159ebc95b5c9f4e0de97aae75eccd84ab8d5a6f9fac4dba891685e5c in / 
# Fri, 26 Jan 2024 23:49:26 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 01:17:49 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 16 Mar 2024 01:17:50 GMT
RUN adduser -S eggdrop
# Sat, 16 Mar 2024 01:17:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 16 Mar 2024 01:17:55 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 16 Mar 2024 01:23:51 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 16 Mar 2024 01:23:51 GMT
ENV NICK=
# Sat, 16 Mar 2024 01:23:51 GMT
ENV SERVER=
# Sat, 16 Mar 2024 01:23:51 GMT
ENV LISTEN=3333
# Sat, 16 Mar 2024 01:23:52 GMT
ENV OWNER=
# Sat, 16 Mar 2024 01:23:52 GMT
ENV USERFILE=eggdrop.user
# Sat, 16 Mar 2024 01:23:52 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 16 Mar 2024 01:23:52 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 16 Mar 2024 01:23:53 GMT
EXPOSE 3333
# Sat, 16 Mar 2024 01:23:53 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 16 Mar 2024 01:23:53 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 16 Mar 2024 01:23:53 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 16 Mar 2024 01:23:54 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:fb7463fbd2413e7d062aba6aa29a656d8ab69e3219cc8790148f3a6f6127f241`  
		Last Modified: Fri, 26 Jan 2024 23:50:09 GMT  
		Size: 2.6 MB (2615845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affcee25bef02b5cba26102707e223e662132304327f74b1d03a0a80b021419e`  
		Last Modified: Sat, 16 Mar 2024 01:24:17 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb1334c9b8bbb16b6b41546d71c45fa883fd8c114011e7788bfd28e197694c4`  
		Last Modified: Sat, 16 Mar 2024 01:24:15 GMT  
		Size: 10.6 KB (10632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37bdb64459c3fc20ac99747c2f88b2476a7add515e08772c2e13b1d0779b50d1`  
		Last Modified: Sat, 16 Mar 2024 01:24:16 GMT  
		Size: 2.7 MB (2679963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dab88836f957381aafea6ed7b022ae07f98fc726a3da5559bf403838c4c4b6`  
		Last Modified: Sat, 16 Mar 2024 01:24:17 GMT  
		Size: 6.1 MB (6054195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a83c1c85c5ff7a3a94b1eb51df9c444b720a5b195b36d2e4e6e51ca657cd32`  
		Last Modified: Sat, 16 Mar 2024 01:24:15 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337ebff1ed4221f79babe930a7d26bd64b04886592773c37fbde29cd78ef6b33`  
		Last Modified: Sat, 16 Mar 2024 01:24:15 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:ec4247483ebd32d7d44ebbcbd3ab79395804c27127923d824301f8e13e82930a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11686612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a90801751b5098ab1a3e25d54522b32ba1d10b3f41d856b48128cfeba3de7de`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:08:16 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 16 Mar 2024 03:08:17 GMT
RUN adduser -S eggdrop
# Sat, 16 Mar 2024 03:08:18 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 16 Mar 2024 03:08:19 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 16 Mar 2024 03:12:35 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 16 Mar 2024 03:12:36 GMT
ENV NICK=
# Sat, 16 Mar 2024 03:12:36 GMT
ENV SERVER=
# Sat, 16 Mar 2024 03:12:36 GMT
ENV LISTEN=3333
# Sat, 16 Mar 2024 03:12:36 GMT
ENV OWNER=
# Sat, 16 Mar 2024 03:12:36 GMT
ENV USERFILE=eggdrop.user
# Sat, 16 Mar 2024 03:12:36 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 16 Mar 2024 03:12:36 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 16 Mar 2024 03:12:36 GMT
EXPOSE 3333
# Sat, 16 Mar 2024 03:12:36 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 16 Mar 2024 03:12:36 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 16 Mar 2024 03:12:36 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 16 Mar 2024 03:12:36 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d92ce36709d975e7bb125a902ca25b8572e1c2893090abf8672386ac0a9186`  
		Last Modified: Sat, 16 Mar 2024 03:12:56 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9277c10b9391cd692deafe7cfa17ca0c81e41e7381551232f258c79fed2ad313`  
		Last Modified: Sat, 16 Mar 2024 03:12:55 GMT  
		Size: 10.7 KB (10745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffeb931ccb1f3206342817d97aff9406b2f22aed54d89a6e52ee0c84450e977`  
		Last Modified: Sat, 16 Mar 2024 03:12:55 GMT  
		Size: 2.8 MB (2776574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4181939fa22881ffff419922aa82e06d5d0221f1cfb200040aa24f9007fe3951`  
		Last Modified: Sat, 16 Mar 2024 03:12:56 GMT  
		Size: 6.2 MB (6187205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b5b85db5291f7e557bcbb3b8454967469cb3d8e359aaca6310e4612c0b165d`  
		Last Modified: Sat, 16 Mar 2024 03:12:55 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7611b67f18902787b2989033ac14356ced6c8e9f8aa9a757c19ce4e2017207`  
		Last Modified: Sat, 16 Mar 2024 03:12:55 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.9.5`

```console
$ docker pull eggdrop@sha256:80cb83320a4382fe26261bd37bc3775605583ef7fe7af4a2613b93e00a1d59fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9.5` - linux; amd64

```console
$ docker pull eggdrop@sha256:34a38b278b4fe46c1b431fcf7dfa6cbac1615246172272129b9208d0d2fa8bd4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680b372bebae349d2d30d7d1885053541c90be76f8b4cc32415f7d940836dc13`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:14:11 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 16 Mar 2024 06:14:11 GMT
RUN adduser -S eggdrop
# Sat, 16 Mar 2024 06:14:13 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 16 Mar 2024 06:14:14 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 16 Mar 2024 06:18:03 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 16 Mar 2024 06:18:03 GMT
ENV NICK=
# Sat, 16 Mar 2024 06:18:03 GMT
ENV SERVER=
# Sat, 16 Mar 2024 06:18:03 GMT
ENV LISTEN=3333
# Sat, 16 Mar 2024 06:18:03 GMT
ENV OWNER=
# Sat, 16 Mar 2024 06:18:03 GMT
ENV USERFILE=eggdrop.user
# Sat, 16 Mar 2024 06:18:03 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 16 Mar 2024 06:18:03 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 16 Mar 2024 06:18:03 GMT
EXPOSE 3333
# Sat, 16 Mar 2024 06:18:04 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 16 Mar 2024 06:18:04 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 16 Mar 2024 06:18:04 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 16 Mar 2024 06:18:04 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c630ff352121cf34896e97408532ee11e27a42505c86d429d155280ccb8002`  
		Last Modified: Sat, 16 Mar 2024 06:18:34 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb419fa2bf132049b023b1393209d0b8836e6a7598b618c2dbee91036dc922f7`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 11.0 KB (10954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b4a85b3c8cbd4a52ab562b3e5909758273e37b541cdc144e2a07fc4a329f84`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 2.8 MB (2758094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91429a382ad8f8d515a3269ac11d856c4a69a1062217035b56747b603c5fd9b3`  
		Last Modified: Sat, 16 Mar 2024 06:18:34 GMT  
		Size: 6.1 MB (6146820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c61fc1b45ec89476a85feefd5ae3515f358e5255fc53b9611732f34f49355`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe2aee5f06911bbd805d8dc9d6beedd17ff7a25f96fbb1dc1ba70732675d433`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.5` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:dd6d6710745b8807a747a3131d778c60522010d6bfb6dfb87c8e3269e16b94d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11364455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b737f04cfea3721350fa28d59e56750a460811baeaa4a3d4f64fa878a7e9396`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:26 GMT
ADD file:66e93ac5159ebc95b5c9f4e0de97aae75eccd84ab8d5a6f9fac4dba891685e5c in / 
# Fri, 26 Jan 2024 23:49:26 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 01:17:49 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 16 Mar 2024 01:17:50 GMT
RUN adduser -S eggdrop
# Sat, 16 Mar 2024 01:17:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 16 Mar 2024 01:17:55 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 16 Mar 2024 01:23:51 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 16 Mar 2024 01:23:51 GMT
ENV NICK=
# Sat, 16 Mar 2024 01:23:51 GMT
ENV SERVER=
# Sat, 16 Mar 2024 01:23:51 GMT
ENV LISTEN=3333
# Sat, 16 Mar 2024 01:23:52 GMT
ENV OWNER=
# Sat, 16 Mar 2024 01:23:52 GMT
ENV USERFILE=eggdrop.user
# Sat, 16 Mar 2024 01:23:52 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 16 Mar 2024 01:23:52 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 16 Mar 2024 01:23:53 GMT
EXPOSE 3333
# Sat, 16 Mar 2024 01:23:53 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 16 Mar 2024 01:23:53 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 16 Mar 2024 01:23:53 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 16 Mar 2024 01:23:54 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:fb7463fbd2413e7d062aba6aa29a656d8ab69e3219cc8790148f3a6f6127f241`  
		Last Modified: Fri, 26 Jan 2024 23:50:09 GMT  
		Size: 2.6 MB (2615845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affcee25bef02b5cba26102707e223e662132304327f74b1d03a0a80b021419e`  
		Last Modified: Sat, 16 Mar 2024 01:24:17 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb1334c9b8bbb16b6b41546d71c45fa883fd8c114011e7788bfd28e197694c4`  
		Last Modified: Sat, 16 Mar 2024 01:24:15 GMT  
		Size: 10.6 KB (10632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37bdb64459c3fc20ac99747c2f88b2476a7add515e08772c2e13b1d0779b50d1`  
		Last Modified: Sat, 16 Mar 2024 01:24:16 GMT  
		Size: 2.7 MB (2679963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dab88836f957381aafea6ed7b022ae07f98fc726a3da5559bf403838c4c4b6`  
		Last Modified: Sat, 16 Mar 2024 01:24:17 GMT  
		Size: 6.1 MB (6054195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a83c1c85c5ff7a3a94b1eb51df9c444b720a5b195b36d2e4e6e51ca657cd32`  
		Last Modified: Sat, 16 Mar 2024 01:24:15 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337ebff1ed4221f79babe930a7d26bd64b04886592773c37fbde29cd78ef6b33`  
		Last Modified: Sat, 16 Mar 2024 01:24:15 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.5` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:ec4247483ebd32d7d44ebbcbd3ab79395804c27127923d824301f8e13e82930a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11686612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a90801751b5098ab1a3e25d54522b32ba1d10b3f41d856b48128cfeba3de7de`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:08:16 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 16 Mar 2024 03:08:17 GMT
RUN adduser -S eggdrop
# Sat, 16 Mar 2024 03:08:18 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 16 Mar 2024 03:08:19 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 16 Mar 2024 03:12:35 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 16 Mar 2024 03:12:36 GMT
ENV NICK=
# Sat, 16 Mar 2024 03:12:36 GMT
ENV SERVER=
# Sat, 16 Mar 2024 03:12:36 GMT
ENV LISTEN=3333
# Sat, 16 Mar 2024 03:12:36 GMT
ENV OWNER=
# Sat, 16 Mar 2024 03:12:36 GMT
ENV USERFILE=eggdrop.user
# Sat, 16 Mar 2024 03:12:36 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 16 Mar 2024 03:12:36 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 16 Mar 2024 03:12:36 GMT
EXPOSE 3333
# Sat, 16 Mar 2024 03:12:36 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 16 Mar 2024 03:12:36 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 16 Mar 2024 03:12:36 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 16 Mar 2024 03:12:36 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d92ce36709d975e7bb125a902ca25b8572e1c2893090abf8672386ac0a9186`  
		Last Modified: Sat, 16 Mar 2024 03:12:56 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9277c10b9391cd692deafe7cfa17ca0c81e41e7381551232f258c79fed2ad313`  
		Last Modified: Sat, 16 Mar 2024 03:12:55 GMT  
		Size: 10.7 KB (10745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffeb931ccb1f3206342817d97aff9406b2f22aed54d89a6e52ee0c84450e977`  
		Last Modified: Sat, 16 Mar 2024 03:12:55 GMT  
		Size: 2.8 MB (2776574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4181939fa22881ffff419922aa82e06d5d0221f1cfb200040aa24f9007fe3951`  
		Last Modified: Sat, 16 Mar 2024 03:12:56 GMT  
		Size: 6.2 MB (6187205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b5b85db5291f7e557bcbb3b8454967469cb3d8e359aaca6310e4612c0b165d`  
		Last Modified: Sat, 16 Mar 2024 03:12:55 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7611b67f18902787b2989033ac14356ced6c8e9f8aa9a757c19ce4e2017207`  
		Last Modified: Sat, 16 Mar 2024 03:12:55 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:abee8790ee3c8af88afc778597b995f7b311d37a5b3c1e0da8322c23a1775ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:d3bf47606c9fb02fe7c32997b1c93d6cfb04b04057c0c3a957439e8949766587
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16095231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85193ba96e72cff112ca0e132f55e78289189987ae101f4cfb087d04295df91a`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 01 Apr 2024 17:53:55 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Mon, 01 Apr 2024 17:53:55 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Mon, 01 Apr 2024 17:53:57 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Mon, 01 Apr 2024 17:53:57 GMT
ENV EGGDROP_SHA256=a46bf0e77ed2af907fe6e15b77bddf0c55706258070a05c92810e0bd40a1fe3b
# Mon, 01 Apr 2024 17:53:57 GMT
ENV EGGDROP_COMMIT=4703f71067437c361ca8d5c8c4a09d41561a7a20
# Mon, 01 Apr 2024 17:56:24 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Mon, 01 Apr 2024 17:56:24 GMT
ENV NICK=
# Mon, 01 Apr 2024 17:56:24 GMT
ENV SERVER=
# Mon, 01 Apr 2024 17:56:24 GMT
ENV LISTEN=3333
# Mon, 01 Apr 2024 17:56:24 GMT
ENV USERFILE=eggdrop.user
# Mon, 01 Apr 2024 17:56:25 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 01 Apr 2024 17:56:25 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 01 Apr 2024 17:56:25 GMT
EXPOSE 3333
# Mon, 01 Apr 2024 17:56:25 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Mon, 01 Apr 2024 17:56:25 GMT
COPY file:61da6bdf6e84c41c8486cddfad6cc1d25ced9bbeaa056bab87034428f2134436 in ./scripts/ 
# Mon, 01 Apr 2024 17:56:25 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 01 Apr 2024 17:56:25 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc8a36fd2fdee81c9926e705a41740df18a69d30586b6bfe4c840cad14b851a`  
		Last Modified: Mon, 01 Apr 2024 17:56:42 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687be1d96a29a2b29dd5902cb3870e479175969b487a68c5a8251ec369f76426`  
		Last Modified: Mon, 01 Apr 2024 17:56:42 GMT  
		Size: 1.1 MB (1093055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14db582761e32b97e1892ffe514d06d1688a9489460315a330540429e180b4ab`  
		Last Modified: Mon, 01 Apr 2024 17:56:43 GMT  
		Size: 11.6 MB (11589088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e632c154f9ab04f67d438a081878d472929ba6343314831ce4b51678da241b94`  
		Last Modified: Mon, 01 Apr 2024 17:56:42 GMT  
		Size: 2.0 KB (1954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f62eed83eb06910486ca6d6a74d3a516a38dca697b3d64099693f1b1c75058`  
		Last Modified: Mon, 01 Apr 2024 17:56:42 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:d206a27b4ef580b531a88fd3592278490926e86d05156509d99213d701010625
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15746602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4449e8b4e016503983749d263693857edf4916511d115a0a65ab09416fff4b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:23 GMT
ADD file:ef699a4b52d87def9be5a058091005e5e3f0bb9fb7bf5c9fe3053ba85d79d7af in / 
# Fri, 26 Jan 2024 23:49:23 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 01:13:56 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sat, 16 Mar 2024 01:13:58 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Sat, 16 Mar 2024 01:14:01 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Sat, 16 Mar 2024 01:14:01 GMT
ENV EGGDROP_SHA256=a155625d2ac3a0673e69c9d0149293910583c1623cd1f90f38ad2bcba7b2b766
# Sat, 16 Mar 2024 01:14:02 GMT
ENV EGGDROP_COMMIT=322bddbd102d58cdb00864a3a335b086beaf042c
# Sat, 16 Mar 2024 01:17:33 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Sat, 16 Mar 2024 01:17:33 GMT
ENV NICK=
# Sat, 16 Mar 2024 01:17:33 GMT
ENV SERVER=
# Sat, 16 Mar 2024 01:17:33 GMT
ENV LISTEN=3333
# Sat, 16 Mar 2024 01:17:34 GMT
ENV USERFILE=eggdrop.user
# Sat, 16 Mar 2024 01:17:34 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 16 Mar 2024 01:17:34 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 16 Mar 2024 01:17:34 GMT
EXPOSE 3333
# Sat, 16 Mar 2024 01:17:35 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Sat, 16 Mar 2024 01:17:35 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in ./scripts/ 
# Sat, 16 Mar 2024 01:17:35 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 16 Mar 2024 01:17:36 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:dded572f39df01b407585bbbda3ae89a2d14042e68184c8b3f6af6ac7fe5b86b`  
		Last Modified: Fri, 26 Jan 2024 23:50:01 GMT  
		Size: 3.1 MB (3113120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb82302311f51ac466878a742622f0992f0cb2e8734d1e5857294a462e4c82ff`  
		Last Modified: Sat, 16 Mar 2024 01:24:06 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed3d696d75625936ab9b40d2810cf75477e315eaca22ce53203d1d4c3a349df`  
		Last Modified: Sat, 16 Mar 2024 01:24:06 GMT  
		Size: 1.2 MB (1190273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892b372f1d1f865f5375fbaec12fbb261bb9617cc75f962666c379b149291df4`  
		Last Modified: Sat, 16 Mar 2024 01:24:08 GMT  
		Size: 11.4 MB (11438917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b34938e2ca15c56cc5e2f9cb44eda473eda38d7d204464939500b029fa55bd`  
		Last Modified: Sat, 16 Mar 2024 01:24:06 GMT  
		Size: 2.0 KB (1955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f368ca5d92dee70dac9f2ab26bf6afe912e953c6f9ffaa77eeca31a83d18d7`  
		Last Modified: Sat, 16 Mar 2024 01:24:06 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:e5108c49b6ad5de2f90b6e4a0f91ac1acfcc1b9a3ba4d0f10a6d143b0c71f53d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16218902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab0459b69ae5de28ddb6f95c206d82fde68860df20509fa4affef53a8e3e4c1`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 01 Apr 2024 18:09:16 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Mon, 01 Apr 2024 18:09:16 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Mon, 01 Apr 2024 18:09:17 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Mon, 01 Apr 2024 18:09:17 GMT
ENV EGGDROP_SHA256=a46bf0e77ed2af907fe6e15b77bddf0c55706258070a05c92810e0bd40a1fe3b
# Mon, 01 Apr 2024 18:09:17 GMT
ENV EGGDROP_COMMIT=4703f71067437c361ca8d5c8c4a09d41561a7a20
# Mon, 01 Apr 2024 18:11:14 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Mon, 01 Apr 2024 18:11:15 GMT
ENV NICK=
# Mon, 01 Apr 2024 18:11:15 GMT
ENV SERVER=
# Mon, 01 Apr 2024 18:11:15 GMT
ENV LISTEN=3333
# Mon, 01 Apr 2024 18:11:15 GMT
ENV USERFILE=eggdrop.user
# Mon, 01 Apr 2024 18:11:15 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 01 Apr 2024 18:11:15 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 01 Apr 2024 18:11:15 GMT
EXPOSE 3333
# Mon, 01 Apr 2024 18:11:15 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Mon, 01 Apr 2024 18:11:15 GMT
COPY file:61da6bdf6e84c41c8486cddfad6cc1d25ced9bbeaa056bab87034428f2134436 in ./scripts/ 
# Mon, 01 Apr 2024 18:11:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 01 Apr 2024 18:11:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0324dc57ab492c18add828859dfe3b783b32671cab482a484a29d4948ce56e08`  
		Last Modified: Mon, 01 Apr 2024 18:11:31 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35ebfbd2ee49804d05022386da852ade6ef72ef87853762a12a59565e07fb79`  
		Last Modified: Mon, 01 Apr 2024 18:11:31 GMT  
		Size: 1.2 MB (1188152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5935cf17256ca211b6e5413117b6b0739376ad97e9689919ff49480cfc4cebe2`  
		Last Modified: Mon, 01 Apr 2024 18:11:33 GMT  
		Size: 11.7 MB (11678686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f44d4fe85a03bee8781b17511c95cd3606888a995df7f89633aef2c6a65881`  
		Last Modified: Mon, 01 Apr 2024 18:11:31 GMT  
		Size: 2.0 KB (1951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d408ab23b63e971991a9852e06d4b55c0ef0674b8df740d1f98413f9365ea3`  
		Last Modified: Mon, 01 Apr 2024 18:11:31 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:80cb83320a4382fe26261bd37bc3775605583ef7fe7af4a2613b93e00a1d59fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:34a38b278b4fe46c1b431fcf7dfa6cbac1615246172272129b9208d0d2fa8bd4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680b372bebae349d2d30d7d1885053541c90be76f8b4cc32415f7d940836dc13`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:14:11 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 16 Mar 2024 06:14:11 GMT
RUN adduser -S eggdrop
# Sat, 16 Mar 2024 06:14:13 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 16 Mar 2024 06:14:14 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 16 Mar 2024 06:18:03 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 16 Mar 2024 06:18:03 GMT
ENV NICK=
# Sat, 16 Mar 2024 06:18:03 GMT
ENV SERVER=
# Sat, 16 Mar 2024 06:18:03 GMT
ENV LISTEN=3333
# Sat, 16 Mar 2024 06:18:03 GMT
ENV OWNER=
# Sat, 16 Mar 2024 06:18:03 GMT
ENV USERFILE=eggdrop.user
# Sat, 16 Mar 2024 06:18:03 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 16 Mar 2024 06:18:03 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 16 Mar 2024 06:18:03 GMT
EXPOSE 3333
# Sat, 16 Mar 2024 06:18:04 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 16 Mar 2024 06:18:04 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 16 Mar 2024 06:18:04 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 16 Mar 2024 06:18:04 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c630ff352121cf34896e97408532ee11e27a42505c86d429d155280ccb8002`  
		Last Modified: Sat, 16 Mar 2024 06:18:34 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb419fa2bf132049b023b1393209d0b8836e6a7598b618c2dbee91036dc922f7`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 11.0 KB (10954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b4a85b3c8cbd4a52ab562b3e5909758273e37b541cdc144e2a07fc4a329f84`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 2.8 MB (2758094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91429a382ad8f8d515a3269ac11d856c4a69a1062217035b56747b603c5fd9b3`  
		Last Modified: Sat, 16 Mar 2024 06:18:34 GMT  
		Size: 6.1 MB (6146820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c61fc1b45ec89476a85feefd5ae3515f358e5255fc53b9611732f34f49355`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe2aee5f06911bbd805d8dc9d6beedd17ff7a25f96fbb1dc1ba70732675d433`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:dd6d6710745b8807a747a3131d778c60522010d6bfb6dfb87c8e3269e16b94d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11364455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b737f04cfea3721350fa28d59e56750a460811baeaa4a3d4f64fa878a7e9396`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:26 GMT
ADD file:66e93ac5159ebc95b5c9f4e0de97aae75eccd84ab8d5a6f9fac4dba891685e5c in / 
# Fri, 26 Jan 2024 23:49:26 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 01:17:49 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 16 Mar 2024 01:17:50 GMT
RUN adduser -S eggdrop
# Sat, 16 Mar 2024 01:17:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 16 Mar 2024 01:17:55 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 16 Mar 2024 01:23:51 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 16 Mar 2024 01:23:51 GMT
ENV NICK=
# Sat, 16 Mar 2024 01:23:51 GMT
ENV SERVER=
# Sat, 16 Mar 2024 01:23:51 GMT
ENV LISTEN=3333
# Sat, 16 Mar 2024 01:23:52 GMT
ENV OWNER=
# Sat, 16 Mar 2024 01:23:52 GMT
ENV USERFILE=eggdrop.user
# Sat, 16 Mar 2024 01:23:52 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 16 Mar 2024 01:23:52 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 16 Mar 2024 01:23:53 GMT
EXPOSE 3333
# Sat, 16 Mar 2024 01:23:53 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 16 Mar 2024 01:23:53 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 16 Mar 2024 01:23:53 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 16 Mar 2024 01:23:54 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:fb7463fbd2413e7d062aba6aa29a656d8ab69e3219cc8790148f3a6f6127f241`  
		Last Modified: Fri, 26 Jan 2024 23:50:09 GMT  
		Size: 2.6 MB (2615845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affcee25bef02b5cba26102707e223e662132304327f74b1d03a0a80b021419e`  
		Last Modified: Sat, 16 Mar 2024 01:24:17 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb1334c9b8bbb16b6b41546d71c45fa883fd8c114011e7788bfd28e197694c4`  
		Last Modified: Sat, 16 Mar 2024 01:24:15 GMT  
		Size: 10.6 KB (10632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37bdb64459c3fc20ac99747c2f88b2476a7add515e08772c2e13b1d0779b50d1`  
		Last Modified: Sat, 16 Mar 2024 01:24:16 GMT  
		Size: 2.7 MB (2679963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dab88836f957381aafea6ed7b022ae07f98fc726a3da5559bf403838c4c4b6`  
		Last Modified: Sat, 16 Mar 2024 01:24:17 GMT  
		Size: 6.1 MB (6054195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a83c1c85c5ff7a3a94b1eb51df9c444b720a5b195b36d2e4e6e51ca657cd32`  
		Last Modified: Sat, 16 Mar 2024 01:24:15 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337ebff1ed4221f79babe930a7d26bd64b04886592773c37fbde29cd78ef6b33`  
		Last Modified: Sat, 16 Mar 2024 01:24:15 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:ec4247483ebd32d7d44ebbcbd3ab79395804c27127923d824301f8e13e82930a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11686612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a90801751b5098ab1a3e25d54522b32ba1d10b3f41d856b48128cfeba3de7de`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:08:16 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 16 Mar 2024 03:08:17 GMT
RUN adduser -S eggdrop
# Sat, 16 Mar 2024 03:08:18 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 16 Mar 2024 03:08:19 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 16 Mar 2024 03:12:35 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 16 Mar 2024 03:12:36 GMT
ENV NICK=
# Sat, 16 Mar 2024 03:12:36 GMT
ENV SERVER=
# Sat, 16 Mar 2024 03:12:36 GMT
ENV LISTEN=3333
# Sat, 16 Mar 2024 03:12:36 GMT
ENV OWNER=
# Sat, 16 Mar 2024 03:12:36 GMT
ENV USERFILE=eggdrop.user
# Sat, 16 Mar 2024 03:12:36 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 16 Mar 2024 03:12:36 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 16 Mar 2024 03:12:36 GMT
EXPOSE 3333
# Sat, 16 Mar 2024 03:12:36 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 16 Mar 2024 03:12:36 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 16 Mar 2024 03:12:36 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 16 Mar 2024 03:12:36 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d92ce36709d975e7bb125a902ca25b8572e1c2893090abf8672386ac0a9186`  
		Last Modified: Sat, 16 Mar 2024 03:12:56 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9277c10b9391cd692deafe7cfa17ca0c81e41e7381551232f258c79fed2ad313`  
		Last Modified: Sat, 16 Mar 2024 03:12:55 GMT  
		Size: 10.7 KB (10745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffeb931ccb1f3206342817d97aff9406b2f22aed54d89a6e52ee0c84450e977`  
		Last Modified: Sat, 16 Mar 2024 03:12:55 GMT  
		Size: 2.8 MB (2776574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4181939fa22881ffff419922aa82e06d5d0221f1cfb200040aa24f9007fe3951`  
		Last Modified: Sat, 16 Mar 2024 03:12:56 GMT  
		Size: 6.2 MB (6187205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b5b85db5291f7e557bcbb3b8454967469cb3d8e359aaca6310e4612c0b165d`  
		Last Modified: Sat, 16 Mar 2024 03:12:55 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7611b67f18902787b2989033ac14356ced6c8e9f8aa9a757c19ce4e2017207`  
		Last Modified: Sat, 16 Mar 2024 03:12:55 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:80cb83320a4382fe26261bd37bc3775605583ef7fe7af4a2613b93e00a1d59fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:34a38b278b4fe46c1b431fcf7dfa6cbac1615246172272129b9208d0d2fa8bd4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680b372bebae349d2d30d7d1885053541c90be76f8b4cc32415f7d940836dc13`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:14:11 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 16 Mar 2024 06:14:11 GMT
RUN adduser -S eggdrop
# Sat, 16 Mar 2024 06:14:13 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 16 Mar 2024 06:14:14 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 16 Mar 2024 06:18:03 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 16 Mar 2024 06:18:03 GMT
ENV NICK=
# Sat, 16 Mar 2024 06:18:03 GMT
ENV SERVER=
# Sat, 16 Mar 2024 06:18:03 GMT
ENV LISTEN=3333
# Sat, 16 Mar 2024 06:18:03 GMT
ENV OWNER=
# Sat, 16 Mar 2024 06:18:03 GMT
ENV USERFILE=eggdrop.user
# Sat, 16 Mar 2024 06:18:03 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 16 Mar 2024 06:18:03 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 16 Mar 2024 06:18:03 GMT
EXPOSE 3333
# Sat, 16 Mar 2024 06:18:04 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 16 Mar 2024 06:18:04 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 16 Mar 2024 06:18:04 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 16 Mar 2024 06:18:04 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c630ff352121cf34896e97408532ee11e27a42505c86d429d155280ccb8002`  
		Last Modified: Sat, 16 Mar 2024 06:18:34 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb419fa2bf132049b023b1393209d0b8836e6a7598b618c2dbee91036dc922f7`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 11.0 KB (10954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b4a85b3c8cbd4a52ab562b3e5909758273e37b541cdc144e2a07fc4a329f84`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 2.8 MB (2758094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91429a382ad8f8d515a3269ac11d856c4a69a1062217035b56747b603c5fd9b3`  
		Last Modified: Sat, 16 Mar 2024 06:18:34 GMT  
		Size: 6.1 MB (6146820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c61fc1b45ec89476a85feefd5ae3515f358e5255fc53b9611732f34f49355`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe2aee5f06911bbd805d8dc9d6beedd17ff7a25f96fbb1dc1ba70732675d433`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:dd6d6710745b8807a747a3131d778c60522010d6bfb6dfb87c8e3269e16b94d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11364455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b737f04cfea3721350fa28d59e56750a460811baeaa4a3d4f64fa878a7e9396`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:26 GMT
ADD file:66e93ac5159ebc95b5c9f4e0de97aae75eccd84ab8d5a6f9fac4dba891685e5c in / 
# Fri, 26 Jan 2024 23:49:26 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 01:17:49 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 16 Mar 2024 01:17:50 GMT
RUN adduser -S eggdrop
# Sat, 16 Mar 2024 01:17:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 16 Mar 2024 01:17:55 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 16 Mar 2024 01:23:51 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 16 Mar 2024 01:23:51 GMT
ENV NICK=
# Sat, 16 Mar 2024 01:23:51 GMT
ENV SERVER=
# Sat, 16 Mar 2024 01:23:51 GMT
ENV LISTEN=3333
# Sat, 16 Mar 2024 01:23:52 GMT
ENV OWNER=
# Sat, 16 Mar 2024 01:23:52 GMT
ENV USERFILE=eggdrop.user
# Sat, 16 Mar 2024 01:23:52 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 16 Mar 2024 01:23:52 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 16 Mar 2024 01:23:53 GMT
EXPOSE 3333
# Sat, 16 Mar 2024 01:23:53 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 16 Mar 2024 01:23:53 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 16 Mar 2024 01:23:53 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 16 Mar 2024 01:23:54 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:fb7463fbd2413e7d062aba6aa29a656d8ab69e3219cc8790148f3a6f6127f241`  
		Last Modified: Fri, 26 Jan 2024 23:50:09 GMT  
		Size: 2.6 MB (2615845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affcee25bef02b5cba26102707e223e662132304327f74b1d03a0a80b021419e`  
		Last Modified: Sat, 16 Mar 2024 01:24:17 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb1334c9b8bbb16b6b41546d71c45fa883fd8c114011e7788bfd28e197694c4`  
		Last Modified: Sat, 16 Mar 2024 01:24:15 GMT  
		Size: 10.6 KB (10632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37bdb64459c3fc20ac99747c2f88b2476a7add515e08772c2e13b1d0779b50d1`  
		Last Modified: Sat, 16 Mar 2024 01:24:16 GMT  
		Size: 2.7 MB (2679963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dab88836f957381aafea6ed7b022ae07f98fc726a3da5559bf403838c4c4b6`  
		Last Modified: Sat, 16 Mar 2024 01:24:17 GMT  
		Size: 6.1 MB (6054195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a83c1c85c5ff7a3a94b1eb51df9c444b720a5b195b36d2e4e6e51ca657cd32`  
		Last Modified: Sat, 16 Mar 2024 01:24:15 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337ebff1ed4221f79babe930a7d26bd64b04886592773c37fbde29cd78ef6b33`  
		Last Modified: Sat, 16 Mar 2024 01:24:15 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:ec4247483ebd32d7d44ebbcbd3ab79395804c27127923d824301f8e13e82930a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11686612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a90801751b5098ab1a3e25d54522b32ba1d10b3f41d856b48128cfeba3de7de`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:08:16 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 16 Mar 2024 03:08:17 GMT
RUN adduser -S eggdrop
# Sat, 16 Mar 2024 03:08:18 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 16 Mar 2024 03:08:19 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 16 Mar 2024 03:12:35 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 16 Mar 2024 03:12:36 GMT
ENV NICK=
# Sat, 16 Mar 2024 03:12:36 GMT
ENV SERVER=
# Sat, 16 Mar 2024 03:12:36 GMT
ENV LISTEN=3333
# Sat, 16 Mar 2024 03:12:36 GMT
ENV OWNER=
# Sat, 16 Mar 2024 03:12:36 GMT
ENV USERFILE=eggdrop.user
# Sat, 16 Mar 2024 03:12:36 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 16 Mar 2024 03:12:36 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 16 Mar 2024 03:12:36 GMT
EXPOSE 3333
# Sat, 16 Mar 2024 03:12:36 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 16 Mar 2024 03:12:36 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 16 Mar 2024 03:12:36 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 16 Mar 2024 03:12:36 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d92ce36709d975e7bb125a902ca25b8572e1c2893090abf8672386ac0a9186`  
		Last Modified: Sat, 16 Mar 2024 03:12:56 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9277c10b9391cd692deafe7cfa17ca0c81e41e7381551232f258c79fed2ad313`  
		Last Modified: Sat, 16 Mar 2024 03:12:55 GMT  
		Size: 10.7 KB (10745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffeb931ccb1f3206342817d97aff9406b2f22aed54d89a6e52ee0c84450e977`  
		Last Modified: Sat, 16 Mar 2024 03:12:55 GMT  
		Size: 2.8 MB (2776574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4181939fa22881ffff419922aa82e06d5d0221f1cfb200040aa24f9007fe3951`  
		Last Modified: Sat, 16 Mar 2024 03:12:56 GMT  
		Size: 6.2 MB (6187205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b5b85db5291f7e557bcbb3b8454967469cb3d8e359aaca6310e4612c0b165d`  
		Last Modified: Sat, 16 Mar 2024 03:12:55 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7611b67f18902787b2989033ac14356ced6c8e9f8aa9a757c19ce4e2017207`  
		Last Modified: Sat, 16 Mar 2024 03:12:55 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
