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
$ docker pull eggdrop@sha256:93bd285c1d8a5b55d0bd152315e155556fb9dc49aa17fa12fa15a19186791dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:2f36a7f7c26559179d3bea4814207667f99797a14c8ed0f06565e2244753ae4f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16104405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a612b2e1157682c0bc7a87919745faed530abefaa04adb4f88d6a2739c6a256f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:04 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Thu, 20 Jun 2024 20:17:04 GMT
CMD ["/bin/sh"]
# Wed, 26 Jun 2024 16:51:05 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 26 Jun 2024 16:51:06 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Wed, 26 Jun 2024 16:51:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Wed, 26 Jun 2024 16:51:07 GMT
ENV EGGDROP_SHA256=a46bf0e77ed2af907fe6e15b77bddf0c55706258070a05c92810e0bd40a1fe3b
# Wed, 26 Jun 2024 16:51:07 GMT
ENV EGGDROP_COMMIT=4703f71067437c361ca8d5c8c4a09d41561a7a20
# Wed, 26 Jun 2024 16:53:37 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Wed, 26 Jun 2024 16:53:37 GMT
ENV NICK=
# Wed, 26 Jun 2024 16:53:37 GMT
ENV SERVER=
# Wed, 26 Jun 2024 16:53:37 GMT
ENV LISTEN=3333
# Wed, 26 Jun 2024 16:53:37 GMT
ENV USERFILE=eggdrop.user
# Wed, 26 Jun 2024 16:53:38 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 26 Jun 2024 16:53:38 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 26 Jun 2024 16:53:38 GMT
EXPOSE 3333
# Wed, 26 Jun 2024 16:53:38 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Wed, 26 Jun 2024 16:53:38 GMT
COPY file:61da6bdf6e84c41c8486cddfad6cc1d25ced9bbeaa056bab87034428f2134436 in ./scripts/ 
# Wed, 26 Jun 2024 16:53:38 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 26 Jun 2024 16:53:38 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e5cf294e09fd7f4effe5cff0c57a211f41aaee778ec6715750ac0c487107b3`  
		Last Modified: Wed, 26 Jun 2024 16:53:53 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e22a2e4f1c3c5db4af9dcd1caf769ae766cb7332ac61820c8ccf3ee07d4a537`  
		Last Modified: Wed, 26 Jun 2024 16:53:54 GMT  
		Size: 1.1 MB (1093051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1301de2282ecd4f73f7d4824169c9a3fbf390367d214c8b7c08b19ca720c7262`  
		Last Modified: Wed, 26 Jun 2024 16:53:55 GMT  
		Size: 11.6 MB (11589693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d502b23edb843965c5408a88dc3d3be7abb0b32367ea032d6453ff9b33be7e`  
		Last Modified: Wed, 26 Jun 2024 16:53:53 GMT  
		Size: 2.0 KB (1954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e486719c62d7526c8e13756a7207658a4ddf19438f0c72139825798c25c942f`  
		Last Modified: Wed, 26 Jun 2024 16:53:53 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:4481ab6bcbb7bd031f67f9c6b109abfb1339d0b22cc4bec06979da3959e23113
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15747991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d300d32b17c8f0a90cc3f938200c7fa38ff82e5c1234585b5ebdac12e9684e5e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 20 Jun 2024 17:49:18 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 21:58:59 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Thu, 20 Jun 2024 21:58:59 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Thu, 20 Jun 2024 21:59:01 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Thu, 20 Jun 2024 21:59:01 GMT
ENV EGGDROP_SHA256=a46bf0e77ed2af907fe6e15b77bddf0c55706258070a05c92810e0bd40a1fe3b
# Thu, 20 Jun 2024 21:59:01 GMT
ENV EGGDROP_COMMIT=4703f71067437c361ca8d5c8c4a09d41561a7a20
# Thu, 20 Jun 2024 22:01:47 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Thu, 20 Jun 2024 22:01:47 GMT
ENV NICK=
# Thu, 20 Jun 2024 22:01:48 GMT
ENV SERVER=
# Thu, 20 Jun 2024 22:01:48 GMT
ENV LISTEN=3333
# Thu, 20 Jun 2024 22:01:48 GMT
ENV USERFILE=eggdrop.user
# Thu, 20 Jun 2024 22:01:48 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 20 Jun 2024 22:01:49 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 20 Jun 2024 22:01:49 GMT
EXPOSE 3333
# Thu, 20 Jun 2024 22:01:49 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Thu, 20 Jun 2024 22:01:49 GMT
COPY file:61da6bdf6e84c41c8486cddfad6cc1d25ced9bbeaa056bab87034428f2134436 in ./scripts/ 
# Thu, 20 Jun 2024 22:01:50 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 20 Jun 2024 22:01:50 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913f9513ab76a3a95ae6b576ccf39e8e558a6516054bda4f721fbb960edeaf51`  
		Last Modified: Wed, 26 Jun 2024 16:50:52 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b44de2989ee023350dfc9e9ed0ec9ccd5c84f75c9fafe18ae2996a0c2ffb72`  
		Last Modified: Wed, 26 Jun 2024 16:50:53 GMT  
		Size: 1.1 MB (1106371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f3b025f175453607b3b5ceb048a894915f302210d25e79cd08283706f0656a`  
		Last Modified: Wed, 26 Jun 2024 16:50:55 GMT  
		Size: 11.5 MB (11463396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f802bb8ed38cf01ae8449ea8a11d7e124e3f906758fb56a963a27a3e8075c75`  
		Last Modified: Wed, 26 Jun 2024 16:50:52 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a409afe84a96f0f1572372501a67a30fd986ef7e33282ad2ff7ae8c7c965b66c`  
		Last Modified: Wed, 26 Jun 2024 16:50:52 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:f180f5f4265abff9d724182c01b48d1602efd6267895625a936c3e626a7effc1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16228680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19da4706ab1424bc52f258c5f4a0010feb3944cb05dcccd64442f75662f8d441`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 01:12:04 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Fri, 21 Jun 2024 01:12:06 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Fri, 21 Jun 2024 01:12:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Fri, 21 Jun 2024 01:12:07 GMT
ENV EGGDROP_SHA256=a46bf0e77ed2af907fe6e15b77bddf0c55706258070a05c92810e0bd40a1fe3b
# Fri, 21 Jun 2024 01:12:08 GMT
ENV EGGDROP_COMMIT=4703f71067437c361ca8d5c8c4a09d41561a7a20
# Fri, 21 Jun 2024 01:14:10 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Fri, 21 Jun 2024 01:14:10 GMT
ENV NICK=
# Fri, 21 Jun 2024 01:14:11 GMT
ENV SERVER=
# Fri, 21 Jun 2024 01:14:11 GMT
ENV LISTEN=3333
# Fri, 21 Jun 2024 01:14:11 GMT
ENV USERFILE=eggdrop.user
# Fri, 21 Jun 2024 01:14:11 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 21 Jun 2024 01:14:11 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 21 Jun 2024 01:14:11 GMT
EXPOSE 3333
# Fri, 21 Jun 2024 01:14:11 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Fri, 21 Jun 2024 01:14:11 GMT
COPY file:61da6bdf6e84c41c8486cddfad6cc1d25ced9bbeaa056bab87034428f2134436 in ./scripts/ 
# Fri, 21 Jun 2024 01:14:11 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 21 Jun 2024 01:14:11 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8066016b3afe20cf5aed256b3a40077cbbda7e66fbef5cf0dc8e4b38140ee0`  
		Last Modified: Fri, 21 Jun 2024 01:14:27 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57f43ce2d7f7b0f29e1d5669061a7d4b0d5574fb333ff7561c65f2ea6ad1a79`  
		Last Modified: Fri, 21 Jun 2024 01:14:27 GMT  
		Size: 1.2 MB (1188337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57709e356ded8f4924eb987405207c98c9f0fc1faa61721660b38a3cb9afa82d`  
		Last Modified: Fri, 21 Jun 2024 01:14:29 GMT  
		Size: 11.7 MB (11678814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a3a791501bdfa6a4feafd9cc4ddf12fbdf8784048e8e07160566843c70aadc`  
		Last Modified: Fri, 21 Jun 2024 01:14:27 GMT  
		Size: 2.0 KB (1954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec98f64a49f6633c0fc02b38e7a5aa13e0bcc7702c8056a6015ba5d66bd7dcc`  
		Last Modified: Fri, 21 Jun 2024 01:14:27 GMT  
		Size: 1.1 KB (1125 bytes)  
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
