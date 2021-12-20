<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.9`](#eggdrop19)
-	[`eggdrop:1.9.1`](#eggdrop191)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.9`

```console
$ docker pull eggdrop@sha256:be0af413359c347d83cd90d038e2c47a72f287f6408bcf7ec4e5278c6fe6ac93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9` - linux; amd64

```console
$ docker pull eggdrop@sha256:9c6596f5f82d72853c41a1ff2ab0dde99cf183a9360c3e81d2aa04adc1aff31d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8300228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7461ee69238d0e483760f24b0e8f8105ede4967b89e9aecfb2019359c4c9877a`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 02:14:10 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 19 Nov 2021 02:14:11 GMT
RUN adduser -S eggdrop
# Fri, 19 Nov 2021 02:14:12 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 19 Nov 2021 02:14:14 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 19 Nov 2021 02:15:32 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 19 Nov 2021 02:15:33 GMT
ENV NICK=
# Fri, 19 Nov 2021 02:15:33 GMT
ENV SERVER=
# Fri, 19 Nov 2021 02:15:33 GMT
ENV LISTEN=3333
# Fri, 19 Nov 2021 02:15:33 GMT
ENV OWNER=
# Fri, 19 Nov 2021 02:15:34 GMT
ENV USERFILE=eggdrop.user
# Fri, 19 Nov 2021 02:15:34 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 19 Nov 2021 02:15:34 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 19 Nov 2021 02:15:34 GMT
EXPOSE 3333
# Fri, 19 Nov 2021 02:15:34 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 19 Nov 2021 02:15:35 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 19 Nov 2021 02:15:35 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 19 Nov 2021 02:15:35 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3241c16fd16e3a139d141166ed22612842968854446255731cfe12791acfc269`  
		Last Modified: Fri, 19 Nov 2021 02:16:18 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281a017ba637452218499fca2a22d724cdc72571a4475255c1ab054b41b12a67`  
		Last Modified: Fri, 19 Nov 2021 02:16:15 GMT  
		Size: 10.7 KB (10696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb699dbe31b3a2a61d0a1d77320a2b8498026a801e89a6120867ce22e17fcbfa`  
		Last Modified: Fri, 19 Nov 2021 02:16:16 GMT  
		Size: 2.7 MB (2725635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c578fe6ec65c61bb7d4b9d0fb9e95bad41dc21eb0a367b41a08514c0f45629`  
		Last Modified: Fri, 19 Nov 2021 02:16:16 GMT  
		Size: 2.7 MB (2737667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd855de544c861d806abe4adce8d076181eadebcbaf72087ec9d8d3208b4b0b8`  
		Last Modified: Fri, 19 Nov 2021 02:16:16 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff4bd4f3812e83ee5267d745bcab933481aaba47d0b044b213e019342ddb2e0`  
		Last Modified: Fri, 19 Nov 2021 02:16:15 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:5690f691d5aebfd87054f27e1f6899a78266fcb4a229ea0bd0a86b9e29e36736
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7995875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4247b2ce077a62a9cfe5151f7e7ce8b36363656a7cfd58f72927c809f85b47ff`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 02:14:56 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 19 Nov 2021 02:14:58 GMT
RUN adduser -S eggdrop
# Fri, 19 Nov 2021 02:15:00 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 19 Nov 2021 02:15:03 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 19 Nov 2021 02:17:29 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 19 Nov 2021 02:17:29 GMT
ENV NICK=
# Fri, 19 Nov 2021 02:17:29 GMT
ENV SERVER=
# Fri, 19 Nov 2021 02:17:30 GMT
ENV LISTEN=3333
# Fri, 19 Nov 2021 02:17:30 GMT
ENV OWNER=
# Fri, 19 Nov 2021 02:17:31 GMT
ENV USERFILE=eggdrop.user
# Fri, 19 Nov 2021 02:17:31 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 19 Nov 2021 02:17:32 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 19 Nov 2021 02:17:32 GMT
EXPOSE 3333
# Fri, 19 Nov 2021 02:17:33 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 19 Nov 2021 02:17:33 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 19 Nov 2021 02:17:34 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 19 Nov 2021 02:17:34 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2309fcfaf1ca362756bec339b48f126b6ec0f5fa3fb744e9434fb293ed0d3c24`  
		Last Modified: Fri, 19 Nov 2021 02:18:12 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b5e954defc4ce697425f8522b59169b4279c8711007be88b712f4a9a2a9e54`  
		Last Modified: Fri, 19 Nov 2021 02:18:10 GMT  
		Size: 10.4 KB (10419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1517d2175902598848fc6b7e2ffe3003fa8d8c51d595eea621210dd1081c2f8`  
		Last Modified: Fri, 19 Nov 2021 02:18:13 GMT  
		Size: 2.7 MB (2652614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8d9a09ecea5272d582e8e12e809f68ce11347a033f0ff0aa4e462983d6c2ed`  
		Last Modified: Fri, 19 Nov 2021 02:18:12 GMT  
		Size: 2.7 MB (2695694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b958bd4e892235910ef2726bc08dde37dc2a05c3c22df21299546bc681f2bef`  
		Last Modified: Fri, 19 Nov 2021 02:18:10 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da7b19f145d2e7edbcf311aa83e2fb8a4b7a2414d6ae9e0275296627d6ede250`  
		Last Modified: Fri, 19 Nov 2021 02:18:10 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:cce2af596f43a71f3de7c879b8e8cebc3fd854ef89894ee49b673988036c5147
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8217633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d52838b63670883cfec07a7586170da2288a4506bef5bf0c02fa411731b2e97`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 08:52:44 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 13 Nov 2021 08:52:45 GMT
RUN adduser -S eggdrop
# Sat, 13 Nov 2021 08:52:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 13 Nov 2021 08:52:49 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 19 Nov 2021 01:37:42 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 19 Nov 2021 01:37:42 GMT
ENV NICK=
# Fri, 19 Nov 2021 01:37:43 GMT
ENV SERVER=
# Fri, 19 Nov 2021 01:37:44 GMT
ENV LISTEN=3333
# Fri, 19 Nov 2021 01:37:45 GMT
ENV OWNER=
# Fri, 19 Nov 2021 01:37:46 GMT
ENV USERFILE=eggdrop.user
# Fri, 19 Nov 2021 01:37:47 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 19 Nov 2021 01:37:51 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 19 Nov 2021 01:37:52 GMT
EXPOSE 3333
# Fri, 19 Nov 2021 01:37:53 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 19 Nov 2021 01:37:56 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 19 Nov 2021 01:37:57 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 19 Nov 2021 01:37:59 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbc128b98804468eb07fa0b1f7b4085c18d55cce6ed2ee8f3b56142609072e2`  
		Last Modified: Fri, 19 Nov 2021 01:38:47 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74808eaa2e85c2f4828d5df25cdcc933b83b31a54fbe0a8f56b6aa7e44ddb722`  
		Last Modified: Fri, 19 Nov 2021 01:38:45 GMT  
		Size: 10.5 KB (10488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317e568dff660152611634a3956770f05f9e989c2b4510e6c43999867205c556`  
		Last Modified: Fri, 19 Nov 2021 01:38:45 GMT  
		Size: 2.8 MB (2752158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c739270eb14b17b8b35df6c081e3781bae52f8d48a5e6c70787b4cde16ae80e`  
		Last Modified: Fri, 19 Nov 2021 01:38:45 GMT  
		Size: 2.7 MB (2731563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fcc42b9556809184e4b06fc5dd03a84ca43734db824db1b99538be54debdc6`  
		Last Modified: Fri, 19 Nov 2021 01:38:44 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27268c13af41e5b69d74afc62083d6832c3dc5f7f2dd4debc9b8abd32de1040`  
		Last Modified: Fri, 19 Nov 2021 01:38:44 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.9.1`

```console
$ docker pull eggdrop@sha256:be0af413359c347d83cd90d038e2c47a72f287f6408bcf7ec4e5278c6fe6ac93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9.1` - linux; amd64

```console
$ docker pull eggdrop@sha256:9c6596f5f82d72853c41a1ff2ab0dde99cf183a9360c3e81d2aa04adc1aff31d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8300228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7461ee69238d0e483760f24b0e8f8105ede4967b89e9aecfb2019359c4c9877a`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 02:14:10 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 19 Nov 2021 02:14:11 GMT
RUN adduser -S eggdrop
# Fri, 19 Nov 2021 02:14:12 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 19 Nov 2021 02:14:14 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 19 Nov 2021 02:15:32 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 19 Nov 2021 02:15:33 GMT
ENV NICK=
# Fri, 19 Nov 2021 02:15:33 GMT
ENV SERVER=
# Fri, 19 Nov 2021 02:15:33 GMT
ENV LISTEN=3333
# Fri, 19 Nov 2021 02:15:33 GMT
ENV OWNER=
# Fri, 19 Nov 2021 02:15:34 GMT
ENV USERFILE=eggdrop.user
# Fri, 19 Nov 2021 02:15:34 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 19 Nov 2021 02:15:34 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 19 Nov 2021 02:15:34 GMT
EXPOSE 3333
# Fri, 19 Nov 2021 02:15:34 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 19 Nov 2021 02:15:35 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 19 Nov 2021 02:15:35 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 19 Nov 2021 02:15:35 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3241c16fd16e3a139d141166ed22612842968854446255731cfe12791acfc269`  
		Last Modified: Fri, 19 Nov 2021 02:16:18 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281a017ba637452218499fca2a22d724cdc72571a4475255c1ab054b41b12a67`  
		Last Modified: Fri, 19 Nov 2021 02:16:15 GMT  
		Size: 10.7 KB (10696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb699dbe31b3a2a61d0a1d77320a2b8498026a801e89a6120867ce22e17fcbfa`  
		Last Modified: Fri, 19 Nov 2021 02:16:16 GMT  
		Size: 2.7 MB (2725635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c578fe6ec65c61bb7d4b9d0fb9e95bad41dc21eb0a367b41a08514c0f45629`  
		Last Modified: Fri, 19 Nov 2021 02:16:16 GMT  
		Size: 2.7 MB (2737667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd855de544c861d806abe4adce8d076181eadebcbaf72087ec9d8d3208b4b0b8`  
		Last Modified: Fri, 19 Nov 2021 02:16:16 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff4bd4f3812e83ee5267d745bcab933481aaba47d0b044b213e019342ddb2e0`  
		Last Modified: Fri, 19 Nov 2021 02:16:15 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.1` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:5690f691d5aebfd87054f27e1f6899a78266fcb4a229ea0bd0a86b9e29e36736
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7995875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4247b2ce077a62a9cfe5151f7e7ce8b36363656a7cfd58f72927c809f85b47ff`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 02:14:56 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 19 Nov 2021 02:14:58 GMT
RUN adduser -S eggdrop
# Fri, 19 Nov 2021 02:15:00 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 19 Nov 2021 02:15:03 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 19 Nov 2021 02:17:29 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 19 Nov 2021 02:17:29 GMT
ENV NICK=
# Fri, 19 Nov 2021 02:17:29 GMT
ENV SERVER=
# Fri, 19 Nov 2021 02:17:30 GMT
ENV LISTEN=3333
# Fri, 19 Nov 2021 02:17:30 GMT
ENV OWNER=
# Fri, 19 Nov 2021 02:17:31 GMT
ENV USERFILE=eggdrop.user
# Fri, 19 Nov 2021 02:17:31 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 19 Nov 2021 02:17:32 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 19 Nov 2021 02:17:32 GMT
EXPOSE 3333
# Fri, 19 Nov 2021 02:17:33 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 19 Nov 2021 02:17:33 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 19 Nov 2021 02:17:34 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 19 Nov 2021 02:17:34 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2309fcfaf1ca362756bec339b48f126b6ec0f5fa3fb744e9434fb293ed0d3c24`  
		Last Modified: Fri, 19 Nov 2021 02:18:12 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b5e954defc4ce697425f8522b59169b4279c8711007be88b712f4a9a2a9e54`  
		Last Modified: Fri, 19 Nov 2021 02:18:10 GMT  
		Size: 10.4 KB (10419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1517d2175902598848fc6b7e2ffe3003fa8d8c51d595eea621210dd1081c2f8`  
		Last Modified: Fri, 19 Nov 2021 02:18:13 GMT  
		Size: 2.7 MB (2652614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8d9a09ecea5272d582e8e12e809f68ce11347a033f0ff0aa4e462983d6c2ed`  
		Last Modified: Fri, 19 Nov 2021 02:18:12 GMT  
		Size: 2.7 MB (2695694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b958bd4e892235910ef2726bc08dde37dc2a05c3c22df21299546bc681f2bef`  
		Last Modified: Fri, 19 Nov 2021 02:18:10 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da7b19f145d2e7edbcf311aa83e2fb8a4b7a2414d6ae9e0275296627d6ede250`  
		Last Modified: Fri, 19 Nov 2021 02:18:10 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.1` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:cce2af596f43a71f3de7c879b8e8cebc3fd854ef89894ee49b673988036c5147
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8217633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d52838b63670883cfec07a7586170da2288a4506bef5bf0c02fa411731b2e97`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 08:52:44 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 13 Nov 2021 08:52:45 GMT
RUN adduser -S eggdrop
# Sat, 13 Nov 2021 08:52:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 13 Nov 2021 08:52:49 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 19 Nov 2021 01:37:42 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 19 Nov 2021 01:37:42 GMT
ENV NICK=
# Fri, 19 Nov 2021 01:37:43 GMT
ENV SERVER=
# Fri, 19 Nov 2021 01:37:44 GMT
ENV LISTEN=3333
# Fri, 19 Nov 2021 01:37:45 GMT
ENV OWNER=
# Fri, 19 Nov 2021 01:37:46 GMT
ENV USERFILE=eggdrop.user
# Fri, 19 Nov 2021 01:37:47 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 19 Nov 2021 01:37:51 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 19 Nov 2021 01:37:52 GMT
EXPOSE 3333
# Fri, 19 Nov 2021 01:37:53 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 19 Nov 2021 01:37:56 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 19 Nov 2021 01:37:57 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 19 Nov 2021 01:37:59 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbc128b98804468eb07fa0b1f7b4085c18d55cce6ed2ee8f3b56142609072e2`  
		Last Modified: Fri, 19 Nov 2021 01:38:47 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74808eaa2e85c2f4828d5df25cdcc933b83b31a54fbe0a8f56b6aa7e44ddb722`  
		Last Modified: Fri, 19 Nov 2021 01:38:45 GMT  
		Size: 10.5 KB (10488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317e568dff660152611634a3956770f05f9e989c2b4510e6c43999867205c556`  
		Last Modified: Fri, 19 Nov 2021 01:38:45 GMT  
		Size: 2.8 MB (2752158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c739270eb14b17b8b35df6c081e3781bae52f8d48a5e6c70787b4cde16ae80e`  
		Last Modified: Fri, 19 Nov 2021 01:38:45 GMT  
		Size: 2.7 MB (2731563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fcc42b9556809184e4b06fc5dd03a84ca43734db824db1b99538be54debdc6`  
		Last Modified: Fri, 19 Nov 2021 01:38:44 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27268c13af41e5b69d74afc62083d6832c3dc5f7f2dd4debc9b8abd32de1040`  
		Last Modified: Fri, 19 Nov 2021 01:38:44 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:9a6eb9a85e0b7a37587d595fe990ea3e04d060d587603d9ade07c3b0ece8dbae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:ac51c0945714354a18de779773d2a06aea0eba1a5db4f39a59afa998af0f2d54
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13971126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18f8406444915774df8bc7fde6cb77d2d7cfdb1f8efbd11c34dfcd931fa42e4`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:17 GMT
ADD file:efe2d94a88cdbbd01c3ef095f0a2473cec9e74804b49cd6fb9b837d362631409 in / 
# Fri, 12 Nov 2021 17:20:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:16:40 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 12 Nov 2021 22:16:42 GMT
RUN adduser -S eggdrop
# Fri, 12 Nov 2021 22:16:44 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 12 Nov 2021 22:16:44 GMT
ENV EGGDROP_SHA256=f977f8f586d1b65d2bae581b5b5828d79193a29a217f617c4c74d1868a566c7f
# Fri, 12 Nov 2021 22:16:45 GMT
ENV EGGDROP_COMMIT=886c2ff6f943952018000c16cb48c08b8ab99127
# Fri, 12 Nov 2021 22:16:48 GMT
RUN apk --update add --no-cache tcl bash openssl
# Fri, 12 Nov 2021 22:18:15 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 12 Nov 2021 22:18:15 GMT
ENV NICK=
# Fri, 12 Nov 2021 22:18:15 GMT
ENV SERVER=
# Fri, 12 Nov 2021 22:18:16 GMT
ENV LISTEN=3333
# Fri, 12 Nov 2021 22:18:16 GMT
ENV OWNER=
# Fri, 12 Nov 2021 22:18:16 GMT
ENV USERFILE=eggdrop.user
# Fri, 12 Nov 2021 22:18:16 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 12 Nov 2021 22:18:17 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 12 Nov 2021 22:18:17 GMT
EXPOSE 3333
# Fri, 12 Nov 2021 22:18:17 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Fri, 12 Nov 2021 22:18:17 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 12 Nov 2021 22:18:17 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 12 Nov 2021 22:18:18 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:79e9f2f55bf5465a02ee6a6170e66005b20c7aa6b115af6fcd04fad706ea651a`  
		Last Modified: Fri, 12 Nov 2021 17:21:24 GMT  
		Size: 2.8 MB (2817409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81adda6e9eba444737eb924c547e315175df5a0ce22872ddefa8d3e84e6d8426`  
		Last Modified: Fri, 12 Nov 2021 23:38:59 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c6691f36cfa95bda1f875a9e50901e42545817a24e6fd9cb8463d931f68075`  
		Last Modified: Fri, 12 Nov 2021 23:38:57 GMT  
		Size: 9.6 KB (9592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1745cf1ed4da7a73fcd90fbf3034e047ac1ddcfc9cafd47e6bec219875fd02b9`  
		Last Modified: Fri, 12 Nov 2021 23:38:57 GMT  
		Size: 2.7 MB (2685370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df75c7a1bacde78f2df7ea75d7a042759a70bdc1a2e64625cf00980990a9b4da`  
		Last Modified: Fri, 12 Nov 2021 23:38:58 GMT  
		Size: 8.5 MB (8454906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3a328dd9ff12c659f26cf5675153e3f8cfd0d2b31419e4d27dac84638dc1cd`  
		Last Modified: Fri, 12 Nov 2021 23:38:57 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb35aaa19b161c31605b0557e35b5f89b077501a6006bf5d840e6cfc255fa07e`  
		Last Modified: Fri, 12 Nov 2021 23:38:56 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:04f5da1f8d9cfe9b4de20d07b8aaf6580c423e499b7aa1f92c3efd19ce804d9e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13629131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5248e64648b70dd2a8aecf181dad16c62e9d8e29e1a0c849d51461bd31028895`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:50:22 GMT
ADD file:c219ee7662a2b29c4e06be5bf332f2f53b326937277057af61516f5cf5abce1e in / 
# Fri, 12 Nov 2021 16:50:23 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 03:30:49 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 13 Nov 2021 03:30:51 GMT
RUN adduser -S eggdrop
# Sat, 13 Nov 2021 03:30:53 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 13 Nov 2021 03:30:53 GMT
ENV EGGDROP_SHA256=f977f8f586d1b65d2bae581b5b5828d79193a29a217f617c4c74d1868a566c7f
# Sat, 13 Nov 2021 03:30:54 GMT
ENV EGGDROP_COMMIT=886c2ff6f943952018000c16cb48c08b8ab99127
# Sat, 13 Nov 2021 03:30:57 GMT
RUN apk --update add --no-cache tcl bash openssl
# Sat, 13 Nov 2021 03:33:19 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 13 Nov 2021 03:33:19 GMT
ENV NICK=
# Sat, 13 Nov 2021 03:33:20 GMT
ENV SERVER=
# Sat, 13 Nov 2021 03:33:20 GMT
ENV LISTEN=3333
# Sat, 13 Nov 2021 03:33:21 GMT
ENV OWNER=
# Sat, 13 Nov 2021 03:33:21 GMT
ENV USERFILE=eggdrop.user
# Sat, 13 Nov 2021 03:33:21 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 13 Nov 2021 03:33:22 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 13 Nov 2021 03:33:22 GMT
EXPOSE 3333
# Sat, 13 Nov 2021 03:33:23 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Sat, 13 Nov 2021 03:33:23 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 13 Nov 2021 03:33:24 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 13 Nov 2021 03:33:24 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:5cb8b15578b20b3c847454a0e0743b923ddea3e4f22ffa95f6f41b0c551a391e`  
		Last Modified: Fri, 12 Nov 2021 16:52:20 GMT  
		Size: 2.6 MB (2623510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c9647b4c3050e47077e5c8d9edce7ae926c3eefafc735a6d81ae469a024c07`  
		Last Modified: Sat, 13 Nov 2021 05:53:01 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c37ba58553c63fd2ebdb5da2016f7c19934d0142773987afbdcf01d6ab27b8`  
		Last Modified: Sat, 13 Nov 2021 05:52:59 GMT  
		Size: 9.4 KB (9401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8db5f2e7b2aaa5174a81b283f2169f8b8bdb1541e83f9627eac970e7d131e4`  
		Last Modified: Sat, 13 Nov 2021 05:53:01 GMT  
		Size: 2.6 MB (2608749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d2918d67befd1ef0a53c4a262000402dc37d2319db48ac355ea31e3329d37c`  
		Last Modified: Sat, 13 Nov 2021 05:53:03 GMT  
		Size: 8.4 MB (8383622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03c6c6a8ac6c10a942eac56504eafae00725f92eb42b53619939705d3e43ddb`  
		Last Modified: Sat, 13 Nov 2021 05:52:59 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ddd2315eb1df07d63a69e2844cb7573ea7737fa3222e8f4fb6943a11ddf4e21`  
		Last Modified: Sat, 13 Nov 2021 05:52:59 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:b082575f3b7776a35592d8b1e4fc81b7e46d43715fb16bf1667d4240b8bbddcd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13933506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709c2cd43aab5d0a0aef27eaf5ed741a05accc39b4127c91f1f572013ae33b80`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:19 GMT
ADD file:bffb4828c6bba0115b766f72c49407938059b204ac9edf130d023af34871d3d0 in / 
# Fri, 12 Nov 2021 16:40:19 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 08:51:17 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 13 Nov 2021 08:51:18 GMT
RUN adduser -S eggdrop
# Sat, 13 Nov 2021 08:51:19 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 13 Nov 2021 08:51:20 GMT
ENV EGGDROP_SHA256=f977f8f586d1b65d2bae581b5b5828d79193a29a217f617c4c74d1868a566c7f
# Sat, 13 Nov 2021 08:51:21 GMT
ENV EGGDROP_COMMIT=886c2ff6f943952018000c16cb48c08b8ab99127
# Sat, 13 Nov 2021 08:51:23 GMT
RUN apk --update add --no-cache tcl bash openssl
# Sat, 13 Nov 2021 08:52:22 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 13 Nov 2021 08:52:22 GMT
ENV NICK=
# Sat, 13 Nov 2021 08:52:23 GMT
ENV SERVER=
# Sat, 13 Nov 2021 08:52:24 GMT
ENV LISTEN=3333
# Sat, 13 Nov 2021 08:52:25 GMT
ENV OWNER=
# Sat, 13 Nov 2021 08:52:26 GMT
ENV USERFILE=eggdrop.user
# Sat, 13 Nov 2021 08:52:27 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 13 Nov 2021 08:52:28 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 13 Nov 2021 08:52:29 GMT
EXPOSE 3333
# Sat, 13 Nov 2021 08:52:31 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Sat, 13 Nov 2021 08:52:32 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 13 Nov 2021 08:52:32 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 13 Nov 2021 08:52:33 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:b48a9fe99aba73065302163e59c82a1b0054810c7b9ef85eee6f1b495b162461`  
		Last Modified: Fri, 12 Nov 2021 16:41:35 GMT  
		Size: 2.7 MB (2728748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5e043b67ff2353188b91df7f18b9d6303a74dfab8ddbb4db3728b472d64f8a`  
		Last Modified: Sat, 13 Nov 2021 11:11:50 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0405e4fb852476c00df2b9492fe26cb8808a4289859d547bf3fa6d64c7bbad`  
		Last Modified: Sat, 13 Nov 2021 11:11:48 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98322a765eb39902765567678e96d10de88f46f9b891d05f35d9bd23e82b0657`  
		Last Modified: Sat, 13 Nov 2021 11:11:48 GMT  
		Size: 2.7 MB (2721970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bdda7ca8a68c3ef9b15288227172a8bec3ad3c17a25bbae6c87a3b130b62a5`  
		Last Modified: Sat, 13 Nov 2021 11:11:49 GMT  
		Size: 8.5 MB (8469526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c09ac811e036ac0a4b650e3babedf24d7a9b7181704c67a3ba8e9c6603f39cc`  
		Last Modified: Sat, 13 Nov 2021 11:11:47 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dea7d298717e7a3a2673a17ac32f21709df757929cf0e6a1254849b81b2cba`  
		Last Modified: Sat, 13 Nov 2021 11:11:47 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:be0af413359c347d83cd90d038e2c47a72f287f6408bcf7ec4e5278c6fe6ac93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:9c6596f5f82d72853c41a1ff2ab0dde99cf183a9360c3e81d2aa04adc1aff31d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8300228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7461ee69238d0e483760f24b0e8f8105ede4967b89e9aecfb2019359c4c9877a`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 02:14:10 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 19 Nov 2021 02:14:11 GMT
RUN adduser -S eggdrop
# Fri, 19 Nov 2021 02:14:12 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 19 Nov 2021 02:14:14 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 19 Nov 2021 02:15:32 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 19 Nov 2021 02:15:33 GMT
ENV NICK=
# Fri, 19 Nov 2021 02:15:33 GMT
ENV SERVER=
# Fri, 19 Nov 2021 02:15:33 GMT
ENV LISTEN=3333
# Fri, 19 Nov 2021 02:15:33 GMT
ENV OWNER=
# Fri, 19 Nov 2021 02:15:34 GMT
ENV USERFILE=eggdrop.user
# Fri, 19 Nov 2021 02:15:34 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 19 Nov 2021 02:15:34 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 19 Nov 2021 02:15:34 GMT
EXPOSE 3333
# Fri, 19 Nov 2021 02:15:34 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 19 Nov 2021 02:15:35 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 19 Nov 2021 02:15:35 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 19 Nov 2021 02:15:35 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3241c16fd16e3a139d141166ed22612842968854446255731cfe12791acfc269`  
		Last Modified: Fri, 19 Nov 2021 02:16:18 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281a017ba637452218499fca2a22d724cdc72571a4475255c1ab054b41b12a67`  
		Last Modified: Fri, 19 Nov 2021 02:16:15 GMT  
		Size: 10.7 KB (10696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb699dbe31b3a2a61d0a1d77320a2b8498026a801e89a6120867ce22e17fcbfa`  
		Last Modified: Fri, 19 Nov 2021 02:16:16 GMT  
		Size: 2.7 MB (2725635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c578fe6ec65c61bb7d4b9d0fb9e95bad41dc21eb0a367b41a08514c0f45629`  
		Last Modified: Fri, 19 Nov 2021 02:16:16 GMT  
		Size: 2.7 MB (2737667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd855de544c861d806abe4adce8d076181eadebcbaf72087ec9d8d3208b4b0b8`  
		Last Modified: Fri, 19 Nov 2021 02:16:16 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff4bd4f3812e83ee5267d745bcab933481aaba47d0b044b213e019342ddb2e0`  
		Last Modified: Fri, 19 Nov 2021 02:16:15 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:5690f691d5aebfd87054f27e1f6899a78266fcb4a229ea0bd0a86b9e29e36736
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7995875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4247b2ce077a62a9cfe5151f7e7ce8b36363656a7cfd58f72927c809f85b47ff`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 02:14:56 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 19 Nov 2021 02:14:58 GMT
RUN adduser -S eggdrop
# Fri, 19 Nov 2021 02:15:00 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 19 Nov 2021 02:15:03 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 19 Nov 2021 02:17:29 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 19 Nov 2021 02:17:29 GMT
ENV NICK=
# Fri, 19 Nov 2021 02:17:29 GMT
ENV SERVER=
# Fri, 19 Nov 2021 02:17:30 GMT
ENV LISTEN=3333
# Fri, 19 Nov 2021 02:17:30 GMT
ENV OWNER=
# Fri, 19 Nov 2021 02:17:31 GMT
ENV USERFILE=eggdrop.user
# Fri, 19 Nov 2021 02:17:31 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 19 Nov 2021 02:17:32 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 19 Nov 2021 02:17:32 GMT
EXPOSE 3333
# Fri, 19 Nov 2021 02:17:33 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 19 Nov 2021 02:17:33 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 19 Nov 2021 02:17:34 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 19 Nov 2021 02:17:34 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2309fcfaf1ca362756bec339b48f126b6ec0f5fa3fb744e9434fb293ed0d3c24`  
		Last Modified: Fri, 19 Nov 2021 02:18:12 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b5e954defc4ce697425f8522b59169b4279c8711007be88b712f4a9a2a9e54`  
		Last Modified: Fri, 19 Nov 2021 02:18:10 GMT  
		Size: 10.4 KB (10419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1517d2175902598848fc6b7e2ffe3003fa8d8c51d595eea621210dd1081c2f8`  
		Last Modified: Fri, 19 Nov 2021 02:18:13 GMT  
		Size: 2.7 MB (2652614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8d9a09ecea5272d582e8e12e809f68ce11347a033f0ff0aa4e462983d6c2ed`  
		Last Modified: Fri, 19 Nov 2021 02:18:12 GMT  
		Size: 2.7 MB (2695694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b958bd4e892235910ef2726bc08dde37dc2a05c3c22df21299546bc681f2bef`  
		Last Modified: Fri, 19 Nov 2021 02:18:10 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da7b19f145d2e7edbcf311aa83e2fb8a4b7a2414d6ae9e0275296627d6ede250`  
		Last Modified: Fri, 19 Nov 2021 02:18:10 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:cce2af596f43a71f3de7c879b8e8cebc3fd854ef89894ee49b673988036c5147
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8217633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d52838b63670883cfec07a7586170da2288a4506bef5bf0c02fa411731b2e97`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 08:52:44 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 13 Nov 2021 08:52:45 GMT
RUN adduser -S eggdrop
# Sat, 13 Nov 2021 08:52:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 13 Nov 2021 08:52:49 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 19 Nov 2021 01:37:42 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 19 Nov 2021 01:37:42 GMT
ENV NICK=
# Fri, 19 Nov 2021 01:37:43 GMT
ENV SERVER=
# Fri, 19 Nov 2021 01:37:44 GMT
ENV LISTEN=3333
# Fri, 19 Nov 2021 01:37:45 GMT
ENV OWNER=
# Fri, 19 Nov 2021 01:37:46 GMT
ENV USERFILE=eggdrop.user
# Fri, 19 Nov 2021 01:37:47 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 19 Nov 2021 01:37:51 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 19 Nov 2021 01:37:52 GMT
EXPOSE 3333
# Fri, 19 Nov 2021 01:37:53 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 19 Nov 2021 01:37:56 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 19 Nov 2021 01:37:57 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 19 Nov 2021 01:37:59 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbc128b98804468eb07fa0b1f7b4085c18d55cce6ed2ee8f3b56142609072e2`  
		Last Modified: Fri, 19 Nov 2021 01:38:47 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74808eaa2e85c2f4828d5df25cdcc933b83b31a54fbe0a8f56b6aa7e44ddb722`  
		Last Modified: Fri, 19 Nov 2021 01:38:45 GMT  
		Size: 10.5 KB (10488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317e568dff660152611634a3956770f05f9e989c2b4510e6c43999867205c556`  
		Last Modified: Fri, 19 Nov 2021 01:38:45 GMT  
		Size: 2.8 MB (2752158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c739270eb14b17b8b35df6c081e3781bae52f8d48a5e6c70787b4cde16ae80e`  
		Last Modified: Fri, 19 Nov 2021 01:38:45 GMT  
		Size: 2.7 MB (2731563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fcc42b9556809184e4b06fc5dd03a84ca43734db824db1b99538be54debdc6`  
		Last Modified: Fri, 19 Nov 2021 01:38:44 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27268c13af41e5b69d74afc62083d6832c3dc5f7f2dd4debc9b8abd32de1040`  
		Last Modified: Fri, 19 Nov 2021 01:38:44 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:be0af413359c347d83cd90d038e2c47a72f287f6408bcf7ec4e5278c6fe6ac93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:9c6596f5f82d72853c41a1ff2ab0dde99cf183a9360c3e81d2aa04adc1aff31d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8300228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7461ee69238d0e483760f24b0e8f8105ede4967b89e9aecfb2019359c4c9877a`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 02:14:10 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 19 Nov 2021 02:14:11 GMT
RUN adduser -S eggdrop
# Fri, 19 Nov 2021 02:14:12 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 19 Nov 2021 02:14:14 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 19 Nov 2021 02:15:32 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 19 Nov 2021 02:15:33 GMT
ENV NICK=
# Fri, 19 Nov 2021 02:15:33 GMT
ENV SERVER=
# Fri, 19 Nov 2021 02:15:33 GMT
ENV LISTEN=3333
# Fri, 19 Nov 2021 02:15:33 GMT
ENV OWNER=
# Fri, 19 Nov 2021 02:15:34 GMT
ENV USERFILE=eggdrop.user
# Fri, 19 Nov 2021 02:15:34 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 19 Nov 2021 02:15:34 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 19 Nov 2021 02:15:34 GMT
EXPOSE 3333
# Fri, 19 Nov 2021 02:15:34 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 19 Nov 2021 02:15:35 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 19 Nov 2021 02:15:35 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 19 Nov 2021 02:15:35 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3241c16fd16e3a139d141166ed22612842968854446255731cfe12791acfc269`  
		Last Modified: Fri, 19 Nov 2021 02:16:18 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281a017ba637452218499fca2a22d724cdc72571a4475255c1ab054b41b12a67`  
		Last Modified: Fri, 19 Nov 2021 02:16:15 GMT  
		Size: 10.7 KB (10696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb699dbe31b3a2a61d0a1d77320a2b8498026a801e89a6120867ce22e17fcbfa`  
		Last Modified: Fri, 19 Nov 2021 02:16:16 GMT  
		Size: 2.7 MB (2725635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c578fe6ec65c61bb7d4b9d0fb9e95bad41dc21eb0a367b41a08514c0f45629`  
		Last Modified: Fri, 19 Nov 2021 02:16:16 GMT  
		Size: 2.7 MB (2737667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd855de544c861d806abe4adce8d076181eadebcbaf72087ec9d8d3208b4b0b8`  
		Last Modified: Fri, 19 Nov 2021 02:16:16 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff4bd4f3812e83ee5267d745bcab933481aaba47d0b044b213e019342ddb2e0`  
		Last Modified: Fri, 19 Nov 2021 02:16:15 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:5690f691d5aebfd87054f27e1f6899a78266fcb4a229ea0bd0a86b9e29e36736
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7995875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4247b2ce077a62a9cfe5151f7e7ce8b36363656a7cfd58f72927c809f85b47ff`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Nov 2021 02:14:56 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 19 Nov 2021 02:14:58 GMT
RUN adduser -S eggdrop
# Fri, 19 Nov 2021 02:15:00 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 19 Nov 2021 02:15:03 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 19 Nov 2021 02:17:29 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 19 Nov 2021 02:17:29 GMT
ENV NICK=
# Fri, 19 Nov 2021 02:17:29 GMT
ENV SERVER=
# Fri, 19 Nov 2021 02:17:30 GMT
ENV LISTEN=3333
# Fri, 19 Nov 2021 02:17:30 GMT
ENV OWNER=
# Fri, 19 Nov 2021 02:17:31 GMT
ENV USERFILE=eggdrop.user
# Fri, 19 Nov 2021 02:17:31 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 19 Nov 2021 02:17:32 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 19 Nov 2021 02:17:32 GMT
EXPOSE 3333
# Fri, 19 Nov 2021 02:17:33 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 19 Nov 2021 02:17:33 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 19 Nov 2021 02:17:34 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 19 Nov 2021 02:17:34 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2309fcfaf1ca362756bec339b48f126b6ec0f5fa3fb744e9434fb293ed0d3c24`  
		Last Modified: Fri, 19 Nov 2021 02:18:12 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b5e954defc4ce697425f8522b59169b4279c8711007be88b712f4a9a2a9e54`  
		Last Modified: Fri, 19 Nov 2021 02:18:10 GMT  
		Size: 10.4 KB (10419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1517d2175902598848fc6b7e2ffe3003fa8d8c51d595eea621210dd1081c2f8`  
		Last Modified: Fri, 19 Nov 2021 02:18:13 GMT  
		Size: 2.7 MB (2652614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8d9a09ecea5272d582e8e12e809f68ce11347a033f0ff0aa4e462983d6c2ed`  
		Last Modified: Fri, 19 Nov 2021 02:18:12 GMT  
		Size: 2.7 MB (2695694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b958bd4e892235910ef2726bc08dde37dc2a05c3c22df21299546bc681f2bef`  
		Last Modified: Fri, 19 Nov 2021 02:18:10 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da7b19f145d2e7edbcf311aa83e2fb8a4b7a2414d6ae9e0275296627d6ede250`  
		Last Modified: Fri, 19 Nov 2021 02:18:10 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:cce2af596f43a71f3de7c879b8e8cebc3fd854ef89894ee49b673988036c5147
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8217633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d52838b63670883cfec07a7586170da2288a4506bef5bf0c02fa411731b2e97`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 08:52:44 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 13 Nov 2021 08:52:45 GMT
RUN adduser -S eggdrop
# Sat, 13 Nov 2021 08:52:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 13 Nov 2021 08:52:49 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 19 Nov 2021 01:37:42 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 19 Nov 2021 01:37:42 GMT
ENV NICK=
# Fri, 19 Nov 2021 01:37:43 GMT
ENV SERVER=
# Fri, 19 Nov 2021 01:37:44 GMT
ENV LISTEN=3333
# Fri, 19 Nov 2021 01:37:45 GMT
ENV OWNER=
# Fri, 19 Nov 2021 01:37:46 GMT
ENV USERFILE=eggdrop.user
# Fri, 19 Nov 2021 01:37:47 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 19 Nov 2021 01:37:51 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 19 Nov 2021 01:37:52 GMT
EXPOSE 3333
# Fri, 19 Nov 2021 01:37:53 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 19 Nov 2021 01:37:56 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 19 Nov 2021 01:37:57 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 19 Nov 2021 01:37:59 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbc128b98804468eb07fa0b1f7b4085c18d55cce6ed2ee8f3b56142609072e2`  
		Last Modified: Fri, 19 Nov 2021 01:38:47 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74808eaa2e85c2f4828d5df25cdcc933b83b31a54fbe0a8f56b6aa7e44ddb722`  
		Last Modified: Fri, 19 Nov 2021 01:38:45 GMT  
		Size: 10.5 KB (10488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317e568dff660152611634a3956770f05f9e989c2b4510e6c43999867205c556`  
		Last Modified: Fri, 19 Nov 2021 01:38:45 GMT  
		Size: 2.8 MB (2752158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c739270eb14b17b8b35df6c081e3781bae52f8d48a5e6c70787b4cde16ae80e`  
		Last Modified: Fri, 19 Nov 2021 01:38:45 GMT  
		Size: 2.7 MB (2731563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fcc42b9556809184e4b06fc5dd03a84ca43734db824db1b99538be54debdc6`  
		Last Modified: Fri, 19 Nov 2021 01:38:44 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27268c13af41e5b69d74afc62083d6832c3dc5f7f2dd4debc9b8abd32de1040`  
		Last Modified: Fri, 19 Nov 2021 01:38:44 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
