## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:c0a0a8c1094a7c1d77df3667305a128dff4596efac6686bb572f15e38aa68835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:77ebf946c594e59e3084e75386d79c850c909e4dd67ee7bb8366db1fd8e2665c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4648b668050242dd18c9efec9b9d8f748df6c9f3b9a12aa49712160c42149a40`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:44:58 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 27 Jan 2024 03:44:58 GMT
RUN adduser -S eggdrop
# Sat, 27 Jan 2024 03:44:59 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 27 Jan 2024 03:45:01 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 27 Jan 2024 03:48:56 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 27 Jan 2024 03:48:56 GMT
ENV NICK=
# Sat, 27 Jan 2024 03:48:56 GMT
ENV SERVER=
# Sat, 27 Jan 2024 03:48:56 GMT
ENV LISTEN=3333
# Sat, 27 Jan 2024 03:48:56 GMT
ENV OWNER=
# Sat, 27 Jan 2024 03:48:56 GMT
ENV USERFILE=eggdrop.user
# Sat, 27 Jan 2024 03:48:56 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 27 Jan 2024 03:48:56 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 27 Jan 2024 03:48:56 GMT
EXPOSE 3333
# Sat, 27 Jan 2024 03:48:57 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 27 Jan 2024 03:48:57 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 27 Jan 2024 03:48:57 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 27 Jan 2024 03:48:57 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30290942be9dec4671ce9d5d9c43c27b35600303a1921d99536b11072bc8e521`  
		Last Modified: Sat, 27 Jan 2024 03:49:21 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4fd988df37cd156061d1a860db35e02648e52a84a6f92f6c1984749c416ae1`  
		Last Modified: Sat, 27 Jan 2024 03:49:19 GMT  
		Size: 11.0 KB (10951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cee24ac298d2150d59391957a1214239790330f0b4f363ad568c24ab74b661`  
		Last Modified: Sat, 27 Jan 2024 03:49:20 GMT  
		Size: 2.8 MB (2758079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717b80ca6c579effa32e7a902fe3494e06f52bde29f54169bed47f73ed2cc874`  
		Last Modified: Sat, 27 Jan 2024 03:49:20 GMT  
		Size: 6.1 MB (6146940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1ff45460ba880593639da82b3d7ce0c09eba17ff292a9230c0f060bc19c0f7`  
		Last Modified: Sat, 27 Jan 2024 03:49:19 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9072f5d1f3939cc1e56fa8e284ede2c7fbc295200daebe5ee14fe544290967`  
		Last Modified: Sat, 27 Jan 2024 03:49:19 GMT  
		Size: 698.0 B  
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
$ docker pull eggdrop@sha256:62e4b24ec30ef13a8cd11076a9c7dd8cf121b181735238b2459ce487c3957ace
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11686720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4792066db6cb4debc078da0759e3f3fb2a373decacfb840c4004feae4cee534`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:50:49 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 27 Jan 2024 03:50:49 GMT
RUN adduser -S eggdrop
# Sat, 27 Jan 2024 03:50:50 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 27 Jan 2024 03:50:53 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 27 Jan 2024 03:54:30 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 27 Jan 2024 03:54:30 GMT
ENV NICK=
# Sat, 27 Jan 2024 03:54:30 GMT
ENV SERVER=
# Sat, 27 Jan 2024 03:54:30 GMT
ENV LISTEN=3333
# Sat, 27 Jan 2024 03:54:30 GMT
ENV OWNER=
# Sat, 27 Jan 2024 03:54:30 GMT
ENV USERFILE=eggdrop.user
# Sat, 27 Jan 2024 03:54:30 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 27 Jan 2024 03:54:31 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 27 Jan 2024 03:54:31 GMT
EXPOSE 3333
# Sat, 27 Jan 2024 03:54:31 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 27 Jan 2024 03:54:31 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 27 Jan 2024 03:54:31 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 27 Jan 2024 03:54:31 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0272fcfcf15f29db40f572756748e118f5a6ba81f38f31c01b054fa1e4999087`  
		Last Modified: Sat, 27 Jan 2024 03:54:58 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b447779f460c686693a6bd3233568f27e5aaf6fab6f671b289f170bbeb7dd7a`  
		Last Modified: Sat, 27 Jan 2024 03:54:56 GMT  
		Size: 10.7 KB (10742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8985411ea0e26dff2de983b53fb744ef6df6a0f736d11692eabdd6f25dfd98b`  
		Last Modified: Sat, 27 Jan 2024 03:54:57 GMT  
		Size: 2.8 MB (2776590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99254a032c360cf19ad47233eb68c29bf2c278e1425010569523c577d2a10509`  
		Last Modified: Sat, 27 Jan 2024 03:54:57 GMT  
		Size: 6.2 MB (6187296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1094c7c6f3e107032b021701e7d4f3ab7aa255ded479c7d606a72da437c5e79`  
		Last Modified: Sat, 27 Jan 2024 03:54:56 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71ef382dfe0f85038573cb288532de8f1530491f29c7d69de49b61e445e5714`  
		Last Modified: Sat, 27 Jan 2024 03:54:56 GMT  
		Size: 697.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
