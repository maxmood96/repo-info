<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.8`](#eggdrop18)
-	[`eggdrop:1.8.4`](#eggdrop184)
-	[`eggdrop:1.9`](#eggdrop19)
-	[`eggdrop:1.9.1`](#eggdrop191)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.8`

```console
$ docker pull eggdrop@sha256:9cd4a0b8fee593cecf08c504fdda01e5c5059bac191ae3d93d000300c743b98b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eggdrop:1.8` - linux; amd64

```console
$ docker pull eggdrop@sha256:22fd38405c2ac3cdf8a68bd99b6373b4ca3ef22326dc55a9040d27cdb6759c30
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8800819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3205dc38d4bd88d8222c7146b241df75126c7c0e31c216683e9c3997b88d99b8`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:26:38 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 20:26:39 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 20:26:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 20:27:40 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 20:28:41 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.8.4.tar.gz.asc eggdrop-1.8.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.8.4.tar.gz.asc   && tar -zxvf eggdrop-1.8.4.tar.gz   && rm eggdrop-1.8.4.tar.gz   && ( cd eggdrop-1.8.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.8.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 20:28:42 GMT
ENV NICK=
# Wed, 14 Apr 2021 20:28:42 GMT
ENV SERVER=
# Wed, 14 Apr 2021 20:28:43 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 20:28:43 GMT
ENV OWNER=
# Wed, 14 Apr 2021 20:28:43 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 20:28:44 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 20:28:44 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 20:28:45 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 20:28:45 GMT
COPY file:f8d85155d39ecdefdd2ce710ca8c1211edaffb7c3fbbde0877da166dd3aaa579 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 20:28:45 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 20:28:46 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 20:28:46 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9b60f543dd32d2ac2d7575d5ad495a35a0796146dbf47fd6c76f083f30d599`  
		Last Modified: Wed, 14 Apr 2021 20:31:00 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1714e89337f555b15f73058aa485a830db0f4a0bd40a36eccd6e66bf949c0259`  
		Last Modified: Wed, 14 Apr 2021 20:30:58 GMT  
		Size: 9.6 KB (9603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9644dcb11463fdb7414f818b0e825bcf15eaa953f86758ed75844357ebc346a2`  
		Last Modified: Wed, 14 Apr 2021 20:31:10 GMT  
		Size: 2.7 MB (2685300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7baaf014b27977624d9dd6472d3430a5910795933ad31bd1af3b311726094f6`  
		Last Modified: Wed, 14 Apr 2021 20:31:10 GMT  
		Size: 3.3 MB (3285828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558533a61e7e9393619d8477302e7a4ceff2107098c41d808f7ed16746c16d25`  
		Last Modified: Wed, 14 Apr 2021 20:31:09 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7459735fb3d77e7827bdbc52771965f821916df4851f7e0295c2717958bac34`  
		Last Modified: Wed, 14 Apr 2021 20:31:09 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.8.4`

```console
$ docker pull eggdrop@sha256:9cd4a0b8fee593cecf08c504fdda01e5c5059bac191ae3d93d000300c743b98b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eggdrop:1.8.4` - linux; amd64

```console
$ docker pull eggdrop@sha256:22fd38405c2ac3cdf8a68bd99b6373b4ca3ef22326dc55a9040d27cdb6759c30
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8800819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3205dc38d4bd88d8222c7146b241df75126c7c0e31c216683e9c3997b88d99b8`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:26:38 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 20:26:39 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 20:26:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 20:27:40 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 20:28:41 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.8.4.tar.gz.asc eggdrop-1.8.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.8.4.tar.gz.asc   && tar -zxvf eggdrop-1.8.4.tar.gz   && rm eggdrop-1.8.4.tar.gz   && ( cd eggdrop-1.8.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.8.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 20:28:42 GMT
ENV NICK=
# Wed, 14 Apr 2021 20:28:42 GMT
ENV SERVER=
# Wed, 14 Apr 2021 20:28:43 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 20:28:43 GMT
ENV OWNER=
# Wed, 14 Apr 2021 20:28:43 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 20:28:44 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 20:28:44 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 20:28:45 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 20:28:45 GMT
COPY file:f8d85155d39ecdefdd2ce710ca8c1211edaffb7c3fbbde0877da166dd3aaa579 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 20:28:45 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 20:28:46 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 20:28:46 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9b60f543dd32d2ac2d7575d5ad495a35a0796146dbf47fd6c76f083f30d599`  
		Last Modified: Wed, 14 Apr 2021 20:31:00 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1714e89337f555b15f73058aa485a830db0f4a0bd40a36eccd6e66bf949c0259`  
		Last Modified: Wed, 14 Apr 2021 20:30:58 GMT  
		Size: 9.6 KB (9603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9644dcb11463fdb7414f818b0e825bcf15eaa953f86758ed75844357ebc346a2`  
		Last Modified: Wed, 14 Apr 2021 20:31:10 GMT  
		Size: 2.7 MB (2685300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7baaf014b27977624d9dd6472d3430a5910795933ad31bd1af3b311726094f6`  
		Last Modified: Wed, 14 Apr 2021 20:31:10 GMT  
		Size: 3.3 MB (3285828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558533a61e7e9393619d8477302e7a4ceff2107098c41d808f7ed16746c16d25`  
		Last Modified: Wed, 14 Apr 2021 20:31:09 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7459735fb3d77e7827bdbc52771965f821916df4851f7e0295c2717958bac34`  
		Last Modified: Wed, 14 Apr 2021 20:31:09 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.9`

```console
$ docker pull eggdrop@sha256:c1bfc6d7635fb78eb5b3ebfcb48186d0c17c2b3b0691af075b0557a864da06b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9` - linux; amd64

```console
$ docker pull eggdrop@sha256:51b3ef47ca8b09e0a8670e81741a7db345f341ccae1d55aae151313ebfa5b365
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8676697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09112261a150b58dcde08ca4b1b9c9903ec3d35ac6ec7578443847dd4a61a851`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:28:52 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 20:28:54 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 20:28:57 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 20:29:00 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 02 Jul 2021 17:21:38 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 02 Jul 2021 17:21:38 GMT
ENV NICK=
# Fri, 02 Jul 2021 17:21:38 GMT
ENV SERVER=
# Fri, 02 Jul 2021 17:21:38 GMT
ENV LISTEN=3333
# Fri, 02 Jul 2021 17:21:39 GMT
ENV OWNER=
# Fri, 02 Jul 2021 17:21:39 GMT
ENV USERFILE=eggdrop.user
# Fri, 02 Jul 2021 17:21:39 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 02 Jul 2021 17:21:39 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 02 Jul 2021 17:21:40 GMT
EXPOSE 3333
# Fri, 02 Jul 2021 17:21:40 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 02 Jul 2021 17:21:40 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 02 Jul 2021 17:21:40 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 02 Jul 2021 17:21:40 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac1d9ab058af7106893a1ba77f9ca0b3a58052b9ae5066905c6f7ae26c94434`  
		Last Modified: Wed, 14 Apr 2021 20:31:26 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76394ca5ad9f94b4ac3d2cb72f4bcd6e7eb23df13adb36a6b732b4e11bf4e9a3`  
		Last Modified: Wed, 14 Apr 2021 20:31:23 GMT  
		Size: 10.1 KB (10113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb74bc16f4c16d3b897fd84478f8df97a60b755eee63f8202139c5e4937537d`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 2.7 MB (2724472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c114180b4ff20542b47e87dddd4e279a6a1c5b93a5fdb4657bda142baa1ef6`  
		Last Modified: Fri, 02 Jul 2021 17:22:07 GMT  
		Size: 3.1 MB (3126334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5184da22eb5974602eeb414a05aa7e2c7b32d466f6737b6bd24b920345229d35`  
		Last Modified: Fri, 02 Jul 2021 17:22:07 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938251404b7a9828161193fdee8efa6acbb84fd990876aeb173ffe1b9bfc259e`  
		Last Modified: Fri, 02 Jul 2021 17:22:07 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:cb2857b4f08efcdc1fe4c3453e4f2681c370cc986a4aa90d75feff218e2b879f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8374923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8231bbbcc5827a63173e69ca178c549755fb7bb7f25c379925c3ea7789b017b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Fri, 02 Jul 2021 17:52:27 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 02 Jul 2021 17:52:29 GMT
RUN adduser -S eggdrop
# Fri, 02 Jul 2021 17:52:31 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 02 Jul 2021 17:52:35 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 02 Jul 2021 17:54:56 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 02 Jul 2021 17:54:56 GMT
ENV NICK=
# Fri, 02 Jul 2021 17:54:57 GMT
ENV SERVER=
# Fri, 02 Jul 2021 17:54:57 GMT
ENV LISTEN=3333
# Fri, 02 Jul 2021 17:54:58 GMT
ENV OWNER=
# Fri, 02 Jul 2021 17:54:58 GMT
ENV USERFILE=eggdrop.user
# Fri, 02 Jul 2021 17:54:59 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 02 Jul 2021 17:55:00 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 02 Jul 2021 17:55:00 GMT
EXPOSE 3333
# Fri, 02 Jul 2021 17:55:01 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 02 Jul 2021 17:55:01 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 02 Jul 2021 17:55:02 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 02 Jul 2021 17:55:02 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde3d0442928db4e3f1dc1a2010597a09612b4f1eb31218ef74cfc446970579f`  
		Last Modified: Fri, 02 Jul 2021 17:55:54 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cabc0f0341eb96eca7c7ecd27e3c208cc939745bedad90ed4513d11be419b4bd`  
		Last Modified: Fri, 02 Jul 2021 17:55:52 GMT  
		Size: 9.8 KB (9833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c0b9d868b661bfa23dd60b3676248d157e8431770bbae4677d622e2680c1db`  
		Last Modified: Fri, 02 Jul 2021 17:55:55 GMT  
		Size: 2.7 MB (2652125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe78ec41b27bf431ccc00eff90efc248d26ad67423e09b418211f5d53cd3e742`  
		Last Modified: Fri, 02 Jul 2021 17:55:55 GMT  
		Size: 3.1 MB (3087038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9bd7137c26119576b933cf2679217767e61f3b3cf60813c85108a34f8e8073`  
		Last Modified: Fri, 02 Jul 2021 17:55:52 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43999f10c3c2695ace77755e1632d119b78f8b54b257f3b632b434c02635bbb`  
		Last Modified: Fri, 02 Jul 2021 17:55:52 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:7b36070ed17d1cf8345ae28df628c1f4e503f7fa363c3920bfc3594fd8ffdada
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8609230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1598a06a352e8e3bd10b91634ce2a1258cfc4a386bfd693f6428850636862c86`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:30:49 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 15 Jun 2021 23:30:50 GMT
RUN adduser -S eggdrop
# Tue, 15 Jun 2021 23:30:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 15 Jun 2021 23:30:53 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 02 Jul 2021 17:42:07 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 02 Jul 2021 17:42:07 GMT
ENV NICK=
# Fri, 02 Jul 2021 17:42:07 GMT
ENV SERVER=
# Fri, 02 Jul 2021 17:42:08 GMT
ENV LISTEN=3333
# Fri, 02 Jul 2021 17:42:08 GMT
ENV OWNER=
# Fri, 02 Jul 2021 17:42:08 GMT
ENV USERFILE=eggdrop.user
# Fri, 02 Jul 2021 17:42:08 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 02 Jul 2021 17:42:08 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 02 Jul 2021 17:42:09 GMT
EXPOSE 3333
# Fri, 02 Jul 2021 17:42:09 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 02 Jul 2021 17:42:09 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 02 Jul 2021 17:42:09 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 02 Jul 2021 17:42:09 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3db2720b6273728863ce64bb67670c4aae649525cf85a5bc0834bd557c60028`  
		Last Modified: Tue, 15 Jun 2021 23:32:42 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5960848fa3748666f162fe523f04c331adba985f24d63933d5aaf1e2a0e75c5b`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 10.0 KB (9996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1ebe6949c44b5c5569f8ee4c4dfe8132fc69db2ae59ed92a76bdcbbc5e5784`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 2.8 MB (2752462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fa19ca3b45bab88854e50ddd795bed53f87dc0bff57b2a313377aa740f0f12`  
		Last Modified: Fri, 02 Jul 2021 17:42:39 GMT  
		Size: 3.1 MB (3130930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71fa519e4578f3ab87690779bc55cb283cecaaed9cb745e64661de22660e341`  
		Last Modified: Fri, 02 Jul 2021 17:42:38 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350e82783e7834ea302f5f705d827daedd7ef7ceff73bb2382d25f2eadeca8dd`  
		Last Modified: Fri, 02 Jul 2021 17:42:38 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.9.1`

```console
$ docker pull eggdrop@sha256:c1bfc6d7635fb78eb5b3ebfcb48186d0c17c2b3b0691af075b0557a864da06b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9.1` - linux; amd64

```console
$ docker pull eggdrop@sha256:51b3ef47ca8b09e0a8670e81741a7db345f341ccae1d55aae151313ebfa5b365
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8676697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09112261a150b58dcde08ca4b1b9c9903ec3d35ac6ec7578443847dd4a61a851`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:28:52 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 20:28:54 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 20:28:57 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 20:29:00 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 02 Jul 2021 17:21:38 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 02 Jul 2021 17:21:38 GMT
ENV NICK=
# Fri, 02 Jul 2021 17:21:38 GMT
ENV SERVER=
# Fri, 02 Jul 2021 17:21:38 GMT
ENV LISTEN=3333
# Fri, 02 Jul 2021 17:21:39 GMT
ENV OWNER=
# Fri, 02 Jul 2021 17:21:39 GMT
ENV USERFILE=eggdrop.user
# Fri, 02 Jul 2021 17:21:39 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 02 Jul 2021 17:21:39 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 02 Jul 2021 17:21:40 GMT
EXPOSE 3333
# Fri, 02 Jul 2021 17:21:40 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 02 Jul 2021 17:21:40 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 02 Jul 2021 17:21:40 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 02 Jul 2021 17:21:40 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac1d9ab058af7106893a1ba77f9ca0b3a58052b9ae5066905c6f7ae26c94434`  
		Last Modified: Wed, 14 Apr 2021 20:31:26 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76394ca5ad9f94b4ac3d2cb72f4bcd6e7eb23df13adb36a6b732b4e11bf4e9a3`  
		Last Modified: Wed, 14 Apr 2021 20:31:23 GMT  
		Size: 10.1 KB (10113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb74bc16f4c16d3b897fd84478f8df97a60b755eee63f8202139c5e4937537d`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 2.7 MB (2724472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c114180b4ff20542b47e87dddd4e279a6a1c5b93a5fdb4657bda142baa1ef6`  
		Last Modified: Fri, 02 Jul 2021 17:22:07 GMT  
		Size: 3.1 MB (3126334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5184da22eb5974602eeb414a05aa7e2c7b32d466f6737b6bd24b920345229d35`  
		Last Modified: Fri, 02 Jul 2021 17:22:07 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938251404b7a9828161193fdee8efa6acbb84fd990876aeb173ffe1b9bfc259e`  
		Last Modified: Fri, 02 Jul 2021 17:22:07 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.1` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:cb2857b4f08efcdc1fe4c3453e4f2681c370cc986a4aa90d75feff218e2b879f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8374923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8231bbbcc5827a63173e69ca178c549755fb7bb7f25c379925c3ea7789b017b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Fri, 02 Jul 2021 17:52:27 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 02 Jul 2021 17:52:29 GMT
RUN adduser -S eggdrop
# Fri, 02 Jul 2021 17:52:31 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 02 Jul 2021 17:52:35 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 02 Jul 2021 17:54:56 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 02 Jul 2021 17:54:56 GMT
ENV NICK=
# Fri, 02 Jul 2021 17:54:57 GMT
ENV SERVER=
# Fri, 02 Jul 2021 17:54:57 GMT
ENV LISTEN=3333
# Fri, 02 Jul 2021 17:54:58 GMT
ENV OWNER=
# Fri, 02 Jul 2021 17:54:58 GMT
ENV USERFILE=eggdrop.user
# Fri, 02 Jul 2021 17:54:59 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 02 Jul 2021 17:55:00 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 02 Jul 2021 17:55:00 GMT
EXPOSE 3333
# Fri, 02 Jul 2021 17:55:01 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 02 Jul 2021 17:55:01 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 02 Jul 2021 17:55:02 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 02 Jul 2021 17:55:02 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde3d0442928db4e3f1dc1a2010597a09612b4f1eb31218ef74cfc446970579f`  
		Last Modified: Fri, 02 Jul 2021 17:55:54 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cabc0f0341eb96eca7c7ecd27e3c208cc939745bedad90ed4513d11be419b4bd`  
		Last Modified: Fri, 02 Jul 2021 17:55:52 GMT  
		Size: 9.8 KB (9833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c0b9d868b661bfa23dd60b3676248d157e8431770bbae4677d622e2680c1db`  
		Last Modified: Fri, 02 Jul 2021 17:55:55 GMT  
		Size: 2.7 MB (2652125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe78ec41b27bf431ccc00eff90efc248d26ad67423e09b418211f5d53cd3e742`  
		Last Modified: Fri, 02 Jul 2021 17:55:55 GMT  
		Size: 3.1 MB (3087038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9bd7137c26119576b933cf2679217767e61f3b3cf60813c85108a34f8e8073`  
		Last Modified: Fri, 02 Jul 2021 17:55:52 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43999f10c3c2695ace77755e1632d119b78f8b54b257f3b632b434c02635bbb`  
		Last Modified: Fri, 02 Jul 2021 17:55:52 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.1` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:7b36070ed17d1cf8345ae28df628c1f4e503f7fa363c3920bfc3594fd8ffdada
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8609230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1598a06a352e8e3bd10b91634ce2a1258cfc4a386bfd693f6428850636862c86`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:30:49 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 15 Jun 2021 23:30:50 GMT
RUN adduser -S eggdrop
# Tue, 15 Jun 2021 23:30:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 15 Jun 2021 23:30:53 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 02 Jul 2021 17:42:07 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 02 Jul 2021 17:42:07 GMT
ENV NICK=
# Fri, 02 Jul 2021 17:42:07 GMT
ENV SERVER=
# Fri, 02 Jul 2021 17:42:08 GMT
ENV LISTEN=3333
# Fri, 02 Jul 2021 17:42:08 GMT
ENV OWNER=
# Fri, 02 Jul 2021 17:42:08 GMT
ENV USERFILE=eggdrop.user
# Fri, 02 Jul 2021 17:42:08 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 02 Jul 2021 17:42:08 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 02 Jul 2021 17:42:09 GMT
EXPOSE 3333
# Fri, 02 Jul 2021 17:42:09 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 02 Jul 2021 17:42:09 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 02 Jul 2021 17:42:09 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 02 Jul 2021 17:42:09 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3db2720b6273728863ce64bb67670c4aae649525cf85a5bc0834bd557c60028`  
		Last Modified: Tue, 15 Jun 2021 23:32:42 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5960848fa3748666f162fe523f04c331adba985f24d63933d5aaf1e2a0e75c5b`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 10.0 KB (9996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1ebe6949c44b5c5569f8ee4c4dfe8132fc69db2ae59ed92a76bdcbbc5e5784`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 2.8 MB (2752462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fa19ca3b45bab88854e50ddd795bed53f87dc0bff57b2a313377aa740f0f12`  
		Last Modified: Fri, 02 Jul 2021 17:42:39 GMT  
		Size: 3.1 MB (3130930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71fa519e4578f3ab87690779bc55cb283cecaaed9cb745e64661de22660e341`  
		Last Modified: Fri, 02 Jul 2021 17:42:38 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350e82783e7834ea302f5f705d827daedd7ef7ceff73bb2382d25f2eadeca8dd`  
		Last Modified: Fri, 02 Jul 2021 17:42:38 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:78170f6417446248d6f84fb23b6cf56a11a8195d51e70343a09094f90298e220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:2ab816999da538e9f94ca9d61a1d9eb7217dc8f2c9208716e4fafea284284a9f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13967159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708829750388821816f955df9e88872264718c0b8692ac727d6f7600f71ef45f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:26:38 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 20:26:39 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 20:26:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 02 Jul 2021 17:19:42 GMT
ENV EGGDROP_SHA256=f977f8f586d1b65d2bae581b5b5828d79193a29a217f617c4c74d1868a566c7f
# Fri, 02 Jul 2021 17:19:42 GMT
ENV EGGDROP_COMMIT=886c2ff6f943952018000c16cb48c08b8ab99127
# Fri, 02 Jul 2021 17:19:45 GMT
RUN apk --update add --no-cache tcl bash openssl
# Fri, 02 Jul 2021 17:20:35 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 02 Jul 2021 17:20:35 GMT
ENV NICK=
# Fri, 02 Jul 2021 17:20:36 GMT
ENV SERVER=
# Fri, 02 Jul 2021 17:20:36 GMT
ENV LISTEN=3333
# Fri, 02 Jul 2021 17:20:36 GMT
ENV OWNER=
# Fri, 02 Jul 2021 17:20:36 GMT
ENV USERFILE=eggdrop.user
# Fri, 02 Jul 2021 17:20:36 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 02 Jul 2021 17:20:37 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 02 Jul 2021 17:20:37 GMT
EXPOSE 3333
# Fri, 02 Jul 2021 17:20:37 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Fri, 02 Jul 2021 17:20:37 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 02 Jul 2021 17:20:37 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 02 Jul 2021 17:20:38 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9b60f543dd32d2ac2d7575d5ad495a35a0796146dbf47fd6c76f083f30d599`  
		Last Modified: Wed, 14 Apr 2021 20:31:00 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1714e89337f555b15f73058aa485a830db0f4a0bd40a36eccd6e66bf949c0259`  
		Last Modified: Wed, 14 Apr 2021 20:30:58 GMT  
		Size: 9.6 KB (9603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd72365e83b32d0746f4c0050d60fe8a0facbe94088cf5b589e82b40202bae1`  
		Last Modified: Fri, 02 Jul 2021 17:21:57 GMT  
		Size: 2.7 MB (2685326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312819311fd72def7d8d65cdeb2fae083b1d64371f456d40d94a658afe094ad7`  
		Last Modified: Fri, 02 Jul 2021 17:21:58 GMT  
		Size: 8.5 MB (8452134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d3c5febc67a911d07cb73a9fc366d56581bdb0b744a222709c596ae9b3119c`  
		Last Modified: Fri, 02 Jul 2021 17:21:56 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2f081372a6166ad1ce90579062dc37c4e687a49c2b854d79da9ecafcd2fca5`  
		Last Modified: Fri, 02 Jul 2021 17:21:56 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:349e68f9d8b74146ff745e0f0cc3a21e5c52a083c528e37f89c8abd3a2eb25fb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13626210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1e85ffc7a8e21b7bf572ba96e3f188e8c47887230b499edc5d84ebfe768333`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:47 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Tue, 15 Jun 2021 22:57:47 GMT
CMD ["/bin/sh"]
# Fri, 02 Jul 2021 17:49:40 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 02 Jul 2021 17:49:42 GMT
RUN adduser -S eggdrop
# Fri, 02 Jul 2021 17:49:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 02 Jul 2021 17:49:46 GMT
ENV EGGDROP_SHA256=f977f8f586d1b65d2bae581b5b5828d79193a29a217f617c4c74d1868a566c7f
# Fri, 02 Jul 2021 17:49:47 GMT
ENV EGGDROP_COMMIT=886c2ff6f943952018000c16cb48c08b8ab99127
# Fri, 02 Jul 2021 17:49:51 GMT
RUN apk --update add --no-cache tcl bash openssl
# Fri, 02 Jul 2021 17:52:11 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 02 Jul 2021 17:52:11 GMT
ENV NICK=
# Fri, 02 Jul 2021 17:52:12 GMT
ENV SERVER=
# Fri, 02 Jul 2021 17:52:12 GMT
ENV LISTEN=3333
# Fri, 02 Jul 2021 17:52:13 GMT
ENV OWNER=
# Fri, 02 Jul 2021 17:52:13 GMT
ENV USERFILE=eggdrop.user
# Fri, 02 Jul 2021 17:52:14 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 02 Jul 2021 17:52:14 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 02 Jul 2021 17:52:15 GMT
EXPOSE 3333
# Fri, 02 Jul 2021 17:52:15 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Fri, 02 Jul 2021 17:52:16 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 02 Jul 2021 17:52:16 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 02 Jul 2021 17:52:16 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a19728eec432014213ee2238d2d2987f76b1aedf389f3d48ec0a81c426e913`  
		Last Modified: Fri, 02 Jul 2021 17:55:41 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0051ea1d18bb74c8ef22d384ba405fa2b858271ef119d0e7903d31c72fdfda68`  
		Last Modified: Fri, 02 Jul 2021 17:55:39 GMT  
		Size: 9.4 KB (9404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbff33951f6cd1cfd2db6ba353068d028c0c5c3865fae1bac1c434a9b9e70816`  
		Last Modified: Fri, 02 Jul 2021 17:55:41 GMT  
		Size: 2.6 MB (2608755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd4c1a1643b6116ec93916f92c9d9d7b0f2173db2dd8b63caa5eb6fd9504ed3`  
		Last Modified: Fri, 02 Jul 2021 17:55:44 GMT  
		Size: 8.4 MB (8382295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928dc582c0585d29dd4b646801e06d99732873c6d11b4b224044fd6b9dc382ad`  
		Last Modified: Fri, 02 Jul 2021 17:55:39 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08997fdb04a278dafdd7f2c2d1332d473c61ced42b9daceccf3a702b581a13d6`  
		Last Modified: Fri, 02 Jul 2021 17:55:39 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:c70ac0a13f955edd79ed236bca0dbdc36e97187f05a9354f7c94ef52fda6a006
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13931532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa5d0df8630f3024bd782a7f72e9e5b4fa6b68003b9f8265f3681cf9cacdae4`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:29:36 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 15 Jun 2021 23:29:37 GMT
RUN adduser -S eggdrop
# Tue, 15 Jun 2021 23:29:38 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 02 Jul 2021 17:39:48 GMT
ENV EGGDROP_SHA256=f977f8f586d1b65d2bae581b5b5828d79193a29a217f617c4c74d1868a566c7f
# Fri, 02 Jul 2021 17:39:48 GMT
ENV EGGDROP_COMMIT=886c2ff6f943952018000c16cb48c08b8ab99127
# Fri, 02 Jul 2021 17:39:50 GMT
RUN apk --update add --no-cache tcl bash openssl
# Fri, 02 Jul 2021 17:40:53 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 02 Jul 2021 17:40:53 GMT
ENV NICK=
# Fri, 02 Jul 2021 17:40:53 GMT
ENV SERVER=
# Fri, 02 Jul 2021 17:40:53 GMT
ENV LISTEN=3333
# Fri, 02 Jul 2021 17:40:54 GMT
ENV OWNER=
# Fri, 02 Jul 2021 17:40:54 GMT
ENV USERFILE=eggdrop.user
# Fri, 02 Jul 2021 17:40:54 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 02 Jul 2021 17:40:54 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 02 Jul 2021 17:40:54 GMT
EXPOSE 3333
# Fri, 02 Jul 2021 17:40:55 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Fri, 02 Jul 2021 17:40:55 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 02 Jul 2021 17:40:55 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 02 Jul 2021 17:40:55 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c7539bf8879d1a52593f00c732dcc06de9183953717c4b4951f6b8d29cbbc1`  
		Last Modified: Tue, 15 Jun 2021 23:32:32 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7414aa2d3258c5ce8af602a09967cff2107fdb7e678a330b48e092a0cfca4a44`  
		Last Modified: Tue, 15 Jun 2021 23:32:29 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5b09a183e39b602bd66f2775c80e61270e350bfb739fc1dd6263c5410a5ced`  
		Last Modified: Fri, 02 Jul 2021 17:42:30 GMT  
		Size: 2.7 MB (2722582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fda6c805fe8d9feb0a57de280acfb2501a580dcd55c37fec52394d2732bfde4`  
		Last Modified: Fri, 02 Jul 2021 17:42:30 GMT  
		Size: 8.5 MB (8468643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed23ead9fb4f46dd5c0c877ce2f44670feea4fd533bf5f89b0f04ef62581426`  
		Last Modified: Fri, 02 Jul 2021 17:42:29 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05ba0af66353010b8adc3027934e3e8c6fd0bcb8ace7841ec086de17864bd5b`  
		Last Modified: Fri, 02 Jul 2021 17:42:29 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:c1bfc6d7635fb78eb5b3ebfcb48186d0c17c2b3b0691af075b0557a864da06b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:51b3ef47ca8b09e0a8670e81741a7db345f341ccae1d55aae151313ebfa5b365
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8676697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09112261a150b58dcde08ca4b1b9c9903ec3d35ac6ec7578443847dd4a61a851`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:28:52 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 20:28:54 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 20:28:57 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 20:29:00 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 02 Jul 2021 17:21:38 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 02 Jul 2021 17:21:38 GMT
ENV NICK=
# Fri, 02 Jul 2021 17:21:38 GMT
ENV SERVER=
# Fri, 02 Jul 2021 17:21:38 GMT
ENV LISTEN=3333
# Fri, 02 Jul 2021 17:21:39 GMT
ENV OWNER=
# Fri, 02 Jul 2021 17:21:39 GMT
ENV USERFILE=eggdrop.user
# Fri, 02 Jul 2021 17:21:39 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 02 Jul 2021 17:21:39 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 02 Jul 2021 17:21:40 GMT
EXPOSE 3333
# Fri, 02 Jul 2021 17:21:40 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 02 Jul 2021 17:21:40 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 02 Jul 2021 17:21:40 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 02 Jul 2021 17:21:40 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac1d9ab058af7106893a1ba77f9ca0b3a58052b9ae5066905c6f7ae26c94434`  
		Last Modified: Wed, 14 Apr 2021 20:31:26 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76394ca5ad9f94b4ac3d2cb72f4bcd6e7eb23df13adb36a6b732b4e11bf4e9a3`  
		Last Modified: Wed, 14 Apr 2021 20:31:23 GMT  
		Size: 10.1 KB (10113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb74bc16f4c16d3b897fd84478f8df97a60b755eee63f8202139c5e4937537d`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 2.7 MB (2724472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c114180b4ff20542b47e87dddd4e279a6a1c5b93a5fdb4657bda142baa1ef6`  
		Last Modified: Fri, 02 Jul 2021 17:22:07 GMT  
		Size: 3.1 MB (3126334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5184da22eb5974602eeb414a05aa7e2c7b32d466f6737b6bd24b920345229d35`  
		Last Modified: Fri, 02 Jul 2021 17:22:07 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938251404b7a9828161193fdee8efa6acbb84fd990876aeb173ffe1b9bfc259e`  
		Last Modified: Fri, 02 Jul 2021 17:22:07 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:cb2857b4f08efcdc1fe4c3453e4f2681c370cc986a4aa90d75feff218e2b879f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8374923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8231bbbcc5827a63173e69ca178c549755fb7bb7f25c379925c3ea7789b017b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Fri, 02 Jul 2021 17:52:27 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 02 Jul 2021 17:52:29 GMT
RUN adduser -S eggdrop
# Fri, 02 Jul 2021 17:52:31 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 02 Jul 2021 17:52:35 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 02 Jul 2021 17:54:56 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 02 Jul 2021 17:54:56 GMT
ENV NICK=
# Fri, 02 Jul 2021 17:54:57 GMT
ENV SERVER=
# Fri, 02 Jul 2021 17:54:57 GMT
ENV LISTEN=3333
# Fri, 02 Jul 2021 17:54:58 GMT
ENV OWNER=
# Fri, 02 Jul 2021 17:54:58 GMT
ENV USERFILE=eggdrop.user
# Fri, 02 Jul 2021 17:54:59 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 02 Jul 2021 17:55:00 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 02 Jul 2021 17:55:00 GMT
EXPOSE 3333
# Fri, 02 Jul 2021 17:55:01 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 02 Jul 2021 17:55:01 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 02 Jul 2021 17:55:02 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 02 Jul 2021 17:55:02 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde3d0442928db4e3f1dc1a2010597a09612b4f1eb31218ef74cfc446970579f`  
		Last Modified: Fri, 02 Jul 2021 17:55:54 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cabc0f0341eb96eca7c7ecd27e3c208cc939745bedad90ed4513d11be419b4bd`  
		Last Modified: Fri, 02 Jul 2021 17:55:52 GMT  
		Size: 9.8 KB (9833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c0b9d868b661bfa23dd60b3676248d157e8431770bbae4677d622e2680c1db`  
		Last Modified: Fri, 02 Jul 2021 17:55:55 GMT  
		Size: 2.7 MB (2652125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe78ec41b27bf431ccc00eff90efc248d26ad67423e09b418211f5d53cd3e742`  
		Last Modified: Fri, 02 Jul 2021 17:55:55 GMT  
		Size: 3.1 MB (3087038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9bd7137c26119576b933cf2679217767e61f3b3cf60813c85108a34f8e8073`  
		Last Modified: Fri, 02 Jul 2021 17:55:52 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43999f10c3c2695ace77755e1632d119b78f8b54b257f3b632b434c02635bbb`  
		Last Modified: Fri, 02 Jul 2021 17:55:52 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:7b36070ed17d1cf8345ae28df628c1f4e503f7fa363c3920bfc3594fd8ffdada
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8609230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1598a06a352e8e3bd10b91634ce2a1258cfc4a386bfd693f6428850636862c86`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:30:49 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 15 Jun 2021 23:30:50 GMT
RUN adduser -S eggdrop
# Tue, 15 Jun 2021 23:30:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 15 Jun 2021 23:30:53 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 02 Jul 2021 17:42:07 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 02 Jul 2021 17:42:07 GMT
ENV NICK=
# Fri, 02 Jul 2021 17:42:07 GMT
ENV SERVER=
# Fri, 02 Jul 2021 17:42:08 GMT
ENV LISTEN=3333
# Fri, 02 Jul 2021 17:42:08 GMT
ENV OWNER=
# Fri, 02 Jul 2021 17:42:08 GMT
ENV USERFILE=eggdrop.user
# Fri, 02 Jul 2021 17:42:08 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 02 Jul 2021 17:42:08 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 02 Jul 2021 17:42:09 GMT
EXPOSE 3333
# Fri, 02 Jul 2021 17:42:09 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 02 Jul 2021 17:42:09 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 02 Jul 2021 17:42:09 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 02 Jul 2021 17:42:09 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3db2720b6273728863ce64bb67670c4aae649525cf85a5bc0834bd557c60028`  
		Last Modified: Tue, 15 Jun 2021 23:32:42 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5960848fa3748666f162fe523f04c331adba985f24d63933d5aaf1e2a0e75c5b`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 10.0 KB (9996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1ebe6949c44b5c5569f8ee4c4dfe8132fc69db2ae59ed92a76bdcbbc5e5784`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 2.8 MB (2752462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fa19ca3b45bab88854e50ddd795bed53f87dc0bff57b2a313377aa740f0f12`  
		Last Modified: Fri, 02 Jul 2021 17:42:39 GMT  
		Size: 3.1 MB (3130930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71fa519e4578f3ab87690779bc55cb283cecaaed9cb745e64661de22660e341`  
		Last Modified: Fri, 02 Jul 2021 17:42:38 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350e82783e7834ea302f5f705d827daedd7ef7ceff73bb2382d25f2eadeca8dd`  
		Last Modified: Fri, 02 Jul 2021 17:42:38 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:c1bfc6d7635fb78eb5b3ebfcb48186d0c17c2b3b0691af075b0557a864da06b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:51b3ef47ca8b09e0a8670e81741a7db345f341ccae1d55aae151313ebfa5b365
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8676697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09112261a150b58dcde08ca4b1b9c9903ec3d35ac6ec7578443847dd4a61a851`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:28:52 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 20:28:54 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 20:28:57 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 20:29:00 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 02 Jul 2021 17:21:38 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 02 Jul 2021 17:21:38 GMT
ENV NICK=
# Fri, 02 Jul 2021 17:21:38 GMT
ENV SERVER=
# Fri, 02 Jul 2021 17:21:38 GMT
ENV LISTEN=3333
# Fri, 02 Jul 2021 17:21:39 GMT
ENV OWNER=
# Fri, 02 Jul 2021 17:21:39 GMT
ENV USERFILE=eggdrop.user
# Fri, 02 Jul 2021 17:21:39 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 02 Jul 2021 17:21:39 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 02 Jul 2021 17:21:40 GMT
EXPOSE 3333
# Fri, 02 Jul 2021 17:21:40 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 02 Jul 2021 17:21:40 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 02 Jul 2021 17:21:40 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 02 Jul 2021 17:21:40 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac1d9ab058af7106893a1ba77f9ca0b3a58052b9ae5066905c6f7ae26c94434`  
		Last Modified: Wed, 14 Apr 2021 20:31:26 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76394ca5ad9f94b4ac3d2cb72f4bcd6e7eb23df13adb36a6b732b4e11bf4e9a3`  
		Last Modified: Wed, 14 Apr 2021 20:31:23 GMT  
		Size: 10.1 KB (10113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb74bc16f4c16d3b897fd84478f8df97a60b755eee63f8202139c5e4937537d`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 2.7 MB (2724472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c114180b4ff20542b47e87dddd4e279a6a1c5b93a5fdb4657bda142baa1ef6`  
		Last Modified: Fri, 02 Jul 2021 17:22:07 GMT  
		Size: 3.1 MB (3126334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5184da22eb5974602eeb414a05aa7e2c7b32d466f6737b6bd24b920345229d35`  
		Last Modified: Fri, 02 Jul 2021 17:22:07 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938251404b7a9828161193fdee8efa6acbb84fd990876aeb173ffe1b9bfc259e`  
		Last Modified: Fri, 02 Jul 2021 17:22:07 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:cb2857b4f08efcdc1fe4c3453e4f2681c370cc986a4aa90d75feff218e2b879f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8374923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8231bbbcc5827a63173e69ca178c549755fb7bb7f25c379925c3ea7789b017b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Fri, 02 Jul 2021 17:52:27 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 02 Jul 2021 17:52:29 GMT
RUN adduser -S eggdrop
# Fri, 02 Jul 2021 17:52:31 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 02 Jul 2021 17:52:35 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 02 Jul 2021 17:54:56 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 02 Jul 2021 17:54:56 GMT
ENV NICK=
# Fri, 02 Jul 2021 17:54:57 GMT
ENV SERVER=
# Fri, 02 Jul 2021 17:54:57 GMT
ENV LISTEN=3333
# Fri, 02 Jul 2021 17:54:58 GMT
ENV OWNER=
# Fri, 02 Jul 2021 17:54:58 GMT
ENV USERFILE=eggdrop.user
# Fri, 02 Jul 2021 17:54:59 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 02 Jul 2021 17:55:00 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 02 Jul 2021 17:55:00 GMT
EXPOSE 3333
# Fri, 02 Jul 2021 17:55:01 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 02 Jul 2021 17:55:01 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 02 Jul 2021 17:55:02 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 02 Jul 2021 17:55:02 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde3d0442928db4e3f1dc1a2010597a09612b4f1eb31218ef74cfc446970579f`  
		Last Modified: Fri, 02 Jul 2021 17:55:54 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cabc0f0341eb96eca7c7ecd27e3c208cc939745bedad90ed4513d11be419b4bd`  
		Last Modified: Fri, 02 Jul 2021 17:55:52 GMT  
		Size: 9.8 KB (9833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c0b9d868b661bfa23dd60b3676248d157e8431770bbae4677d622e2680c1db`  
		Last Modified: Fri, 02 Jul 2021 17:55:55 GMT  
		Size: 2.7 MB (2652125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe78ec41b27bf431ccc00eff90efc248d26ad67423e09b418211f5d53cd3e742`  
		Last Modified: Fri, 02 Jul 2021 17:55:55 GMT  
		Size: 3.1 MB (3087038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9bd7137c26119576b933cf2679217767e61f3b3cf60813c85108a34f8e8073`  
		Last Modified: Fri, 02 Jul 2021 17:55:52 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43999f10c3c2695ace77755e1632d119b78f8b54b257f3b632b434c02635bbb`  
		Last Modified: Fri, 02 Jul 2021 17:55:52 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:7b36070ed17d1cf8345ae28df628c1f4e503f7fa363c3920bfc3594fd8ffdada
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8609230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1598a06a352e8e3bd10b91634ce2a1258cfc4a386bfd693f6428850636862c86`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:30:49 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 15 Jun 2021 23:30:50 GMT
RUN adduser -S eggdrop
# Tue, 15 Jun 2021 23:30:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 15 Jun 2021 23:30:53 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 02 Jul 2021 17:42:07 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 02 Jul 2021 17:42:07 GMT
ENV NICK=
# Fri, 02 Jul 2021 17:42:07 GMT
ENV SERVER=
# Fri, 02 Jul 2021 17:42:08 GMT
ENV LISTEN=3333
# Fri, 02 Jul 2021 17:42:08 GMT
ENV OWNER=
# Fri, 02 Jul 2021 17:42:08 GMT
ENV USERFILE=eggdrop.user
# Fri, 02 Jul 2021 17:42:08 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 02 Jul 2021 17:42:08 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 02 Jul 2021 17:42:09 GMT
EXPOSE 3333
# Fri, 02 Jul 2021 17:42:09 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 02 Jul 2021 17:42:09 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 02 Jul 2021 17:42:09 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 02 Jul 2021 17:42:09 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3db2720b6273728863ce64bb67670c4aae649525cf85a5bc0834bd557c60028`  
		Last Modified: Tue, 15 Jun 2021 23:32:42 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5960848fa3748666f162fe523f04c331adba985f24d63933d5aaf1e2a0e75c5b`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 10.0 KB (9996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1ebe6949c44b5c5569f8ee4c4dfe8132fc69db2ae59ed92a76bdcbbc5e5784`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 2.8 MB (2752462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fa19ca3b45bab88854e50ddd795bed53f87dc0bff57b2a313377aa740f0f12`  
		Last Modified: Fri, 02 Jul 2021 17:42:39 GMT  
		Size: 3.1 MB (3130930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71fa519e4578f3ab87690779bc55cb283cecaaed9cb745e64661de22660e341`  
		Last Modified: Fri, 02 Jul 2021 17:42:38 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350e82783e7834ea302f5f705d827daedd7ef7ceff73bb2382d25f2eadeca8dd`  
		Last Modified: Fri, 02 Jul 2021 17:42:38 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
