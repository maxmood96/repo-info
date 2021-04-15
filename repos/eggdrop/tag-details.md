<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.8`](#eggdrop18)
-	[`eggdrop:1.8.4`](#eggdrop184)
-	[`eggdrop:1.9`](#eggdrop19)
-	[`eggdrop:1.9.0`](#eggdrop190)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.8`

```console
$ docker pull eggdrop@sha256:9cd4a0b8fee593cecf08c504fdda01e5c5059bac191ae3d93d000300c743b98b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
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
-	Platforms:
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
$ docker pull eggdrop@sha256:9ef9b503970e8c35f157896867aa1c5e81b1bf7064ee9b736e1aa9d5f665d9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9` - linux; amd64

```console
$ docker pull eggdrop@sha256:e8c3fe57ff5964dd97a8d2a2a506f6a40031e625afb25bdb5b1ec22988823d56
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8224211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b387e204eb1200e349577df42c08c9953800908b336091be2e20c92a264a611`
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
# Wed, 14 Apr 2021 20:30:27 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 20:30:28 GMT
ENV NICK=
# Wed, 14 Apr 2021 20:30:28 GMT
ENV SERVER=
# Wed, 14 Apr 2021 20:30:28 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 20:30:28 GMT
ENV OWNER=
# Wed, 14 Apr 2021 20:30:28 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 20:30:28 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 20:30:29 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 20:30:29 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 20:30:29 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 20:30:29 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 20:30:29 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 20:30:30 GMT
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
	-	`sha256:bee19a14cecf7a9a8b0e86b924d4aa1db06886f93b75039bac7d4d5eaa83bdbc`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 2.7 MB (2673860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5976395ecd64a6b14179cdbc52fceecb422cac42f1f9ed9cb4880fe7b563ed58`  
		Last Modified: Wed, 14 Apr 2021 20:31:23 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa43e66c459b027e8b1e3088b3b265682a436283838f3687b2f71c18be678e8`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:78d4ef27cb29911685f18cdb92cfa41270f510f6e8d3592cb6be006bb87fd2b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7921449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52238f34cb3a55328a8ec63d83fbf69536f22afc05543942adae191aa86b4d4f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:56:54 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 19:57:05 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 19:57:10 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 19:57:16 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 19:59:12 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 19:59:13 GMT
ENV NICK=
# Wed, 14 Apr 2021 19:59:14 GMT
ENV SERVER=
# Wed, 14 Apr 2021 19:59:15 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 19:59:16 GMT
ENV OWNER=
# Wed, 14 Apr 2021 19:59:17 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 19:59:18 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 19:59:20 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 19:59:25 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 19:59:30 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 19:59:33 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 19:59:35 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 19:59:35 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e231f03afe8c29e8696ea3a9a12fa671d754a62a9c635382104d12dec2757072`  
		Last Modified: Wed, 14 Apr 2021 20:00:13 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbf18f1d89826a83b49120673b77422238266894b80701441d516f79823588`  
		Last Modified: Wed, 14 Apr 2021 20:00:11 GMT  
		Size: 9.8 KB (9830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34e9e82dddc9b362ff5bb8a7f2a880e794e14e3d8e734ef0d6614f14bf56ffb`  
		Last Modified: Wed, 14 Apr 2021 20:00:14 GMT  
		Size: 2.7 MB (2652131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef3b98fe7b74dd2000c22edd32faf39f1067b9fa39efb1e59eb3ab209205275`  
		Last Modified: Wed, 14 Apr 2021 20:00:12 GMT  
		Size: 2.6 MB (2633547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01b6a123b9dd6f23ecf8478d53dddf1407060d2f980725386ca54df4afca2c9`  
		Last Modified: Wed, 14 Apr 2021 20:00:11 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05a75460f30a5e4255854c4a9f16faf02f30eee88b4615b3fba025dbc0b2852`  
		Last Modified: Wed, 14 Apr 2021 20:00:11 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:18e95f9cc4efe1ed898089618a720936ad3b67e99700067783048d1444eb1eb6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8146707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24cf1212f8c98ae441c5b7e4268d8e90712302713c3d69d40eed73326b5258b0`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:39:04 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 19:39:07 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 19:39:10 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 19:39:14 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 19:41:19 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 19:41:20 GMT
ENV NICK=
# Wed, 14 Apr 2021 19:41:21 GMT
ENV SERVER=
# Wed, 14 Apr 2021 19:41:22 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 19:41:23 GMT
ENV OWNER=
# Wed, 14 Apr 2021 19:41:24 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 19:41:25 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 19:41:26 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 19:41:27 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 19:41:28 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 19:41:29 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 19:41:30 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 19:41:31 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2a603a165935de32f72822852ae214ae654fcc73afa86fcda5b6db51806d7e`  
		Last Modified: Wed, 14 Apr 2021 19:41:59 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26eb9792575074457b28da2f91d83deecd2bd7358e2afbc4acfb526e5e222d1`  
		Last Modified: Wed, 14 Apr 2021 19:41:59 GMT  
		Size: 10.0 KB (9999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819655b9b18f5b196e9022502b52c797a056085e06350876d9a1df2e036dcc8f`  
		Last Modified: Wed, 14 Apr 2021 19:41:59 GMT  
		Size: 2.8 MB (2752494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cac466ffc40facce85904fbed06e49d4c92e412a9badc2f1958e9ba051b630f`  
		Last Modified: Wed, 14 Apr 2021 19:41:56 GMT  
		Size: 2.7 MB (2668385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991a1d03455a6fa9804bfad777e237e49ade17ae6eee71827b63f855b4ca550f`  
		Last Modified: Wed, 14 Apr 2021 19:41:55 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b1dec8c8e3b2dcf2a8b5120983cd74369e46e79d18a5bbaaf70c34eb6e5529`  
		Last Modified: Wed, 14 Apr 2021 19:41:56 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.9.0`

```console
$ docker pull eggdrop@sha256:9ef9b503970e8c35f157896867aa1c5e81b1bf7064ee9b736e1aa9d5f665d9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9.0` - linux; amd64

```console
$ docker pull eggdrop@sha256:e8c3fe57ff5964dd97a8d2a2a506f6a40031e625afb25bdb5b1ec22988823d56
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8224211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b387e204eb1200e349577df42c08c9953800908b336091be2e20c92a264a611`
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
# Wed, 14 Apr 2021 20:30:27 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 20:30:28 GMT
ENV NICK=
# Wed, 14 Apr 2021 20:30:28 GMT
ENV SERVER=
# Wed, 14 Apr 2021 20:30:28 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 20:30:28 GMT
ENV OWNER=
# Wed, 14 Apr 2021 20:30:28 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 20:30:28 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 20:30:29 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 20:30:29 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 20:30:29 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 20:30:29 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 20:30:29 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 20:30:30 GMT
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
	-	`sha256:bee19a14cecf7a9a8b0e86b924d4aa1db06886f93b75039bac7d4d5eaa83bdbc`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 2.7 MB (2673860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5976395ecd64a6b14179cdbc52fceecb422cac42f1f9ed9cb4880fe7b563ed58`  
		Last Modified: Wed, 14 Apr 2021 20:31:23 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa43e66c459b027e8b1e3088b3b265682a436283838f3687b2f71c18be678e8`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.0` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:78d4ef27cb29911685f18cdb92cfa41270f510f6e8d3592cb6be006bb87fd2b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7921449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52238f34cb3a55328a8ec63d83fbf69536f22afc05543942adae191aa86b4d4f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:56:54 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 19:57:05 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 19:57:10 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 19:57:16 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 19:59:12 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 19:59:13 GMT
ENV NICK=
# Wed, 14 Apr 2021 19:59:14 GMT
ENV SERVER=
# Wed, 14 Apr 2021 19:59:15 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 19:59:16 GMT
ENV OWNER=
# Wed, 14 Apr 2021 19:59:17 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 19:59:18 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 19:59:20 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 19:59:25 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 19:59:30 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 19:59:33 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 19:59:35 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 19:59:35 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e231f03afe8c29e8696ea3a9a12fa671d754a62a9c635382104d12dec2757072`  
		Last Modified: Wed, 14 Apr 2021 20:00:13 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbf18f1d89826a83b49120673b77422238266894b80701441d516f79823588`  
		Last Modified: Wed, 14 Apr 2021 20:00:11 GMT  
		Size: 9.8 KB (9830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34e9e82dddc9b362ff5bb8a7f2a880e794e14e3d8e734ef0d6614f14bf56ffb`  
		Last Modified: Wed, 14 Apr 2021 20:00:14 GMT  
		Size: 2.7 MB (2652131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef3b98fe7b74dd2000c22edd32faf39f1067b9fa39efb1e59eb3ab209205275`  
		Last Modified: Wed, 14 Apr 2021 20:00:12 GMT  
		Size: 2.6 MB (2633547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01b6a123b9dd6f23ecf8478d53dddf1407060d2f980725386ca54df4afca2c9`  
		Last Modified: Wed, 14 Apr 2021 20:00:11 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05a75460f30a5e4255854c4a9f16faf02f30eee88b4615b3fba025dbc0b2852`  
		Last Modified: Wed, 14 Apr 2021 20:00:11 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.0` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:18e95f9cc4efe1ed898089618a720936ad3b67e99700067783048d1444eb1eb6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8146707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24cf1212f8c98ae441c5b7e4268d8e90712302713c3d69d40eed73326b5258b0`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:39:04 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 19:39:07 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 19:39:10 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 19:39:14 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 19:41:19 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 19:41:20 GMT
ENV NICK=
# Wed, 14 Apr 2021 19:41:21 GMT
ENV SERVER=
# Wed, 14 Apr 2021 19:41:22 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 19:41:23 GMT
ENV OWNER=
# Wed, 14 Apr 2021 19:41:24 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 19:41:25 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 19:41:26 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 19:41:27 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 19:41:28 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 19:41:29 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 19:41:30 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 19:41:31 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2a603a165935de32f72822852ae214ae654fcc73afa86fcda5b6db51806d7e`  
		Last Modified: Wed, 14 Apr 2021 19:41:59 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26eb9792575074457b28da2f91d83deecd2bd7358e2afbc4acfb526e5e222d1`  
		Last Modified: Wed, 14 Apr 2021 19:41:59 GMT  
		Size: 10.0 KB (9999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819655b9b18f5b196e9022502b52c797a056085e06350876d9a1df2e036dcc8f`  
		Last Modified: Wed, 14 Apr 2021 19:41:59 GMT  
		Size: 2.8 MB (2752494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cac466ffc40facce85904fbed06e49d4c92e412a9badc2f1958e9ba051b630f`  
		Last Modified: Wed, 14 Apr 2021 19:41:56 GMT  
		Size: 2.7 MB (2668385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991a1d03455a6fa9804bfad777e237e49ade17ae6eee71827b63f855b4ca550f`  
		Last Modified: Wed, 14 Apr 2021 19:41:55 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b1dec8c8e3b2dcf2a8b5120983cd74369e46e79d18a5bbaaf70c34eb6e5529`  
		Last Modified: Wed, 14 Apr 2021 19:41:56 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:26370f2980837f6755712d00d80e6e98734619faf418b07ae443555763485e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:863a1dca7315a511d83332073aacfa18fac03397358b5fe5ba2e7b8a75a276e5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13903044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576dc66e6ec6201c1e65dcb5da0e0c2fa11511e7a1501fbe397e97153707e91c`
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
# Wed, 14 Apr 2021 20:26:41 GMT
ENV EGGDROP_SHA256=ef482116819630aa65127d1c3d04e3762cbf45827bc66d7d505d481960209448
# Wed, 14 Apr 2021 20:26:41 GMT
ENV EGGDROP_COMMIT=d7729c4bbfb30e831e879da3985832e1db503dff
# Wed, 14 Apr 2021 20:26:42 GMT
RUN apk --update add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 20:27:33 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 20:27:33 GMT
ENV NICK=
# Wed, 14 Apr 2021 20:27:34 GMT
ENV SERVER=
# Wed, 14 Apr 2021 20:27:34 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 20:27:34 GMT
ENV OWNER=
# Wed, 14 Apr 2021 20:27:34 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 20:27:34 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 20:27:35 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 20:27:35 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 20:27:35 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 20:27:35 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 20:27:35 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 20:27:36 GMT
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
	-	`sha256:3e603a0c1dc60f9e4445917bed7c38bd060a3e336da983bab83ed39e1d071ec3`  
		Last Modified: Wed, 14 Apr 2021 20:31:00 GMT  
		Size: 2.7 MB (2685312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43656001cc97fbe42d47f6244dd22e9dc0d4091492bd2a44536fcb0aa27a7f4`  
		Last Modified: Wed, 14 Apr 2021 20:30:59 GMT  
		Size: 8.4 MB (8388045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6b5e043a85370cf7210f1f8531dbc218be306517c005b8eae5be566056b7f6`  
		Last Modified: Wed, 14 Apr 2021 20:30:58 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3914a952f41a10e7c83dd041fa5773f3c6328b582d6ea304077875cb445d9d06`  
		Last Modified: Wed, 14 Apr 2021 20:31:00 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:c3bf9c2cdda221f8f156f3057dd408719ef78bff09878a6c82205fd7b26d7d76
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13560543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e08412b7b45976542614516e11642429bae78a720cfd2198019236710aa3dc69`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:58 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Wed, 14 Apr 2021 18:49:59 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:53:23 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 19:53:38 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 19:53:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 19:53:49 GMT
ENV EGGDROP_SHA256=ef482116819630aa65127d1c3d04e3762cbf45827bc66d7d505d481960209448
# Wed, 14 Apr 2021 19:53:52 GMT
ENV EGGDROP_COMMIT=d7729c4bbfb30e831e879da3985832e1db503dff
# Wed, 14 Apr 2021 19:54:07 GMT
RUN apk --update add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 19:56:19 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 19:56:21 GMT
ENV NICK=
# Wed, 14 Apr 2021 19:56:24 GMT
ENV SERVER=
# Wed, 14 Apr 2021 19:56:26 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 19:56:27 GMT
ENV OWNER=
# Wed, 14 Apr 2021 19:56:29 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 19:56:31 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 19:56:32 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 19:56:34 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 19:56:36 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 19:56:39 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 19:56:40 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 19:56:41 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22d78ffb0e230408fd608629b875c877407afeedd0a45af9c9ed2169117984a`  
		Last Modified: Wed, 14 Apr 2021 20:00:04 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c9123ad8d661005614f22f8c8a3d8e82e151f2596a6b93ce83809a14465b9b`  
		Last Modified: Wed, 14 Apr 2021 20:00:02 GMT  
		Size: 9.4 KB (9404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d2497d083ecbb0cc42823a3ca7c0f6ad3b17b85d126e8bd66a9fdac142d9a3`  
		Last Modified: Wed, 14 Apr 2021 20:00:04 GMT  
		Size: 2.6 MB (2608740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca996bb7fde0998b70d0a1136b7178cce6ed3fe68b18596b71e73446dc5aa649`  
		Last Modified: Wed, 14 Apr 2021 20:00:05 GMT  
		Size: 8.3 MB (8316642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd72ae776e770eebcfd03df0c40615a2bdcc024cfe43b8e8e08c4ed405c121`  
		Last Modified: Wed, 14 Apr 2021 20:00:02 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78dc612d9cb44bd8c9252e2c38ca1cc514123fa1a8af2c91306702bd2b6e3680`  
		Last Modified: Wed, 14 Apr 2021 20:00:02 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:850252afe44da6dab30835de33df0e0272f31a8e27faa61b07eb6fa95da1e050
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13869702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f40ebf6796d89015db913a8e3ef2b45e2aa1c4c6d58221f8aa89338eadf4d3`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:05 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Wed, 14 Apr 2021 18:43:06 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:36:29 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 19:36:31 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 19:36:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 19:36:34 GMT
ENV EGGDROP_SHA256=ef482116819630aa65127d1c3d04e3762cbf45827bc66d7d505d481960209448
# Wed, 14 Apr 2021 19:36:35 GMT
ENV EGGDROP_COMMIT=d7729c4bbfb30e831e879da3985832e1db503dff
# Wed, 14 Apr 2021 19:36:39 GMT
RUN apk --update add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 19:38:32 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 19:38:33 GMT
ENV NICK=
# Wed, 14 Apr 2021 19:38:35 GMT
ENV SERVER=
# Wed, 14 Apr 2021 19:38:36 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 19:38:37 GMT
ENV OWNER=
# Wed, 14 Apr 2021 19:38:38 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 19:38:39 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 19:38:40 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 19:38:41 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 19:38:42 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 19:38:43 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 19:38:44 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 19:38:45 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b997aad343dbd28650ee0bcb299c642ad54a09abb3b0cf217846adcdee4a68`  
		Last Modified: Wed, 14 Apr 2021 19:41:47 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45ce3889961128acbf24016684d8ea750fc7b4f4b7896eda664f96033f0f11f`  
		Last Modified: Wed, 14 Apr 2021 19:41:45 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a607909297e6f6a696926e7263bf92de9005af01c3bac0e8039bcd663d5e92`  
		Last Modified: Wed, 14 Apr 2021 19:41:46 GMT  
		Size: 2.7 MB (2722578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f5323a1ed5b8a53964900fa41cbaab40682b4315811604f7ce33e64e176290`  
		Last Modified: Wed, 14 Apr 2021 19:41:47 GMT  
		Size: 8.4 MB (8406817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f9df699f58db3c3d1f9926c52a6a610e80b1a751e60a18976d7aa4945a21ad`  
		Last Modified: Wed, 14 Apr 2021 19:41:45 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f056d5429942f9902fa6ce8c9b6858ff7cc00d8238c6fd694ad28f2a20ae65f8`  
		Last Modified: Wed, 14 Apr 2021 19:41:45 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:9ef9b503970e8c35f157896867aa1c5e81b1bf7064ee9b736e1aa9d5f665d9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:e8c3fe57ff5964dd97a8d2a2a506f6a40031e625afb25bdb5b1ec22988823d56
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8224211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b387e204eb1200e349577df42c08c9953800908b336091be2e20c92a264a611`
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
# Wed, 14 Apr 2021 20:30:27 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 20:30:28 GMT
ENV NICK=
# Wed, 14 Apr 2021 20:30:28 GMT
ENV SERVER=
# Wed, 14 Apr 2021 20:30:28 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 20:30:28 GMT
ENV OWNER=
# Wed, 14 Apr 2021 20:30:28 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 20:30:28 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 20:30:29 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 20:30:29 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 20:30:29 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 20:30:29 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 20:30:29 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 20:30:30 GMT
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
	-	`sha256:bee19a14cecf7a9a8b0e86b924d4aa1db06886f93b75039bac7d4d5eaa83bdbc`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 2.7 MB (2673860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5976395ecd64a6b14179cdbc52fceecb422cac42f1f9ed9cb4880fe7b563ed58`  
		Last Modified: Wed, 14 Apr 2021 20:31:23 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa43e66c459b027e8b1e3088b3b265682a436283838f3687b2f71c18be678e8`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:78d4ef27cb29911685f18cdb92cfa41270f510f6e8d3592cb6be006bb87fd2b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7921449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52238f34cb3a55328a8ec63d83fbf69536f22afc05543942adae191aa86b4d4f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:56:54 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 19:57:05 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 19:57:10 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 19:57:16 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 19:59:12 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 19:59:13 GMT
ENV NICK=
# Wed, 14 Apr 2021 19:59:14 GMT
ENV SERVER=
# Wed, 14 Apr 2021 19:59:15 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 19:59:16 GMT
ENV OWNER=
# Wed, 14 Apr 2021 19:59:17 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 19:59:18 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 19:59:20 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 19:59:25 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 19:59:30 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 19:59:33 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 19:59:35 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 19:59:35 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e231f03afe8c29e8696ea3a9a12fa671d754a62a9c635382104d12dec2757072`  
		Last Modified: Wed, 14 Apr 2021 20:00:13 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbf18f1d89826a83b49120673b77422238266894b80701441d516f79823588`  
		Last Modified: Wed, 14 Apr 2021 20:00:11 GMT  
		Size: 9.8 KB (9830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34e9e82dddc9b362ff5bb8a7f2a880e794e14e3d8e734ef0d6614f14bf56ffb`  
		Last Modified: Wed, 14 Apr 2021 20:00:14 GMT  
		Size: 2.7 MB (2652131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef3b98fe7b74dd2000c22edd32faf39f1067b9fa39efb1e59eb3ab209205275`  
		Last Modified: Wed, 14 Apr 2021 20:00:12 GMT  
		Size: 2.6 MB (2633547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01b6a123b9dd6f23ecf8478d53dddf1407060d2f980725386ca54df4afca2c9`  
		Last Modified: Wed, 14 Apr 2021 20:00:11 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05a75460f30a5e4255854c4a9f16faf02f30eee88b4615b3fba025dbc0b2852`  
		Last Modified: Wed, 14 Apr 2021 20:00:11 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:18e95f9cc4efe1ed898089618a720936ad3b67e99700067783048d1444eb1eb6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8146707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24cf1212f8c98ae441c5b7e4268d8e90712302713c3d69d40eed73326b5258b0`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:39:04 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 19:39:07 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 19:39:10 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 19:39:14 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 19:41:19 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 19:41:20 GMT
ENV NICK=
# Wed, 14 Apr 2021 19:41:21 GMT
ENV SERVER=
# Wed, 14 Apr 2021 19:41:22 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 19:41:23 GMT
ENV OWNER=
# Wed, 14 Apr 2021 19:41:24 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 19:41:25 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 19:41:26 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 19:41:27 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 19:41:28 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 19:41:29 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 19:41:30 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 19:41:31 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2a603a165935de32f72822852ae214ae654fcc73afa86fcda5b6db51806d7e`  
		Last Modified: Wed, 14 Apr 2021 19:41:59 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26eb9792575074457b28da2f91d83deecd2bd7358e2afbc4acfb526e5e222d1`  
		Last Modified: Wed, 14 Apr 2021 19:41:59 GMT  
		Size: 10.0 KB (9999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819655b9b18f5b196e9022502b52c797a056085e06350876d9a1df2e036dcc8f`  
		Last Modified: Wed, 14 Apr 2021 19:41:59 GMT  
		Size: 2.8 MB (2752494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cac466ffc40facce85904fbed06e49d4c92e412a9badc2f1958e9ba051b630f`  
		Last Modified: Wed, 14 Apr 2021 19:41:56 GMT  
		Size: 2.7 MB (2668385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991a1d03455a6fa9804bfad777e237e49ade17ae6eee71827b63f855b4ca550f`  
		Last Modified: Wed, 14 Apr 2021 19:41:55 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b1dec8c8e3b2dcf2a8b5120983cd74369e46e79d18a5bbaaf70c34eb6e5529`  
		Last Modified: Wed, 14 Apr 2021 19:41:56 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:9ef9b503970e8c35f157896867aa1c5e81b1bf7064ee9b736e1aa9d5f665d9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:e8c3fe57ff5964dd97a8d2a2a506f6a40031e625afb25bdb5b1ec22988823d56
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8224211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b387e204eb1200e349577df42c08c9953800908b336091be2e20c92a264a611`
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
# Wed, 14 Apr 2021 20:30:27 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 20:30:28 GMT
ENV NICK=
# Wed, 14 Apr 2021 20:30:28 GMT
ENV SERVER=
# Wed, 14 Apr 2021 20:30:28 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 20:30:28 GMT
ENV OWNER=
# Wed, 14 Apr 2021 20:30:28 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 20:30:28 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 20:30:29 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 20:30:29 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 20:30:29 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 20:30:29 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 20:30:29 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 20:30:30 GMT
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
	-	`sha256:bee19a14cecf7a9a8b0e86b924d4aa1db06886f93b75039bac7d4d5eaa83bdbc`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 2.7 MB (2673860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5976395ecd64a6b14179cdbc52fceecb422cac42f1f9ed9cb4880fe7b563ed58`  
		Last Modified: Wed, 14 Apr 2021 20:31:23 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa43e66c459b027e8b1e3088b3b265682a436283838f3687b2f71c18be678e8`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:78d4ef27cb29911685f18cdb92cfa41270f510f6e8d3592cb6be006bb87fd2b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7921449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52238f34cb3a55328a8ec63d83fbf69536f22afc05543942adae191aa86b4d4f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:56:54 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 19:57:05 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 19:57:10 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 19:57:16 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 19:59:12 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 19:59:13 GMT
ENV NICK=
# Wed, 14 Apr 2021 19:59:14 GMT
ENV SERVER=
# Wed, 14 Apr 2021 19:59:15 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 19:59:16 GMT
ENV OWNER=
# Wed, 14 Apr 2021 19:59:17 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 19:59:18 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 19:59:20 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 19:59:25 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 19:59:30 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 19:59:33 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 19:59:35 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 19:59:35 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e231f03afe8c29e8696ea3a9a12fa671d754a62a9c635382104d12dec2757072`  
		Last Modified: Wed, 14 Apr 2021 20:00:13 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cbf18f1d89826a83b49120673b77422238266894b80701441d516f79823588`  
		Last Modified: Wed, 14 Apr 2021 20:00:11 GMT  
		Size: 9.8 KB (9830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34e9e82dddc9b362ff5bb8a7f2a880e794e14e3d8e734ef0d6614f14bf56ffb`  
		Last Modified: Wed, 14 Apr 2021 20:00:14 GMT  
		Size: 2.7 MB (2652131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef3b98fe7b74dd2000c22edd32faf39f1067b9fa39efb1e59eb3ab209205275`  
		Last Modified: Wed, 14 Apr 2021 20:00:12 GMT  
		Size: 2.6 MB (2633547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01b6a123b9dd6f23ecf8478d53dddf1407060d2f980725386ca54df4afca2c9`  
		Last Modified: Wed, 14 Apr 2021 20:00:11 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05a75460f30a5e4255854c4a9f16faf02f30eee88b4615b3fba025dbc0b2852`  
		Last Modified: Wed, 14 Apr 2021 20:00:11 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:18e95f9cc4efe1ed898089618a720936ad3b67e99700067783048d1444eb1eb6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8146707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24cf1212f8c98ae441c5b7e4268d8e90712302713c3d69d40eed73326b5258b0`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:39:04 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 19:39:07 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 19:39:10 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 19:39:14 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 19:41:19 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.0.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.0.tar.gz.asc eggdrop-1.9.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.0.tar.gz.asc   && tar -zxvf eggdrop-1.9.0.tar.gz   && rm eggdrop-1.9.0.tar.gz   && ( cd eggdrop-1.9.0     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 19:41:20 GMT
ENV NICK=
# Wed, 14 Apr 2021 19:41:21 GMT
ENV SERVER=
# Wed, 14 Apr 2021 19:41:22 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 19:41:23 GMT
ENV OWNER=
# Wed, 14 Apr 2021 19:41:24 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 19:41:25 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 19:41:26 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 19:41:27 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 19:41:28 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 19:41:29 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 19:41:30 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 19:41:31 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2a603a165935de32f72822852ae214ae654fcc73afa86fcda5b6db51806d7e`  
		Last Modified: Wed, 14 Apr 2021 19:41:59 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26eb9792575074457b28da2f91d83deecd2bd7358e2afbc4acfb526e5e222d1`  
		Last Modified: Wed, 14 Apr 2021 19:41:59 GMT  
		Size: 10.0 KB (9999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819655b9b18f5b196e9022502b52c797a056085e06350876d9a1df2e036dcc8f`  
		Last Modified: Wed, 14 Apr 2021 19:41:59 GMT  
		Size: 2.8 MB (2752494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cac466ffc40facce85904fbed06e49d4c92e412a9badc2f1958e9ba051b630f`  
		Last Modified: Wed, 14 Apr 2021 19:41:56 GMT  
		Size: 2.7 MB (2668385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991a1d03455a6fa9804bfad777e237e49ade17ae6eee71827b63f855b4ca550f`  
		Last Modified: Wed, 14 Apr 2021 19:41:55 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b1dec8c8e3b2dcf2a8b5120983cd74369e46e79d18a5bbaaf70c34eb6e5529`  
		Last Modified: Wed, 14 Apr 2021 19:41:56 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
