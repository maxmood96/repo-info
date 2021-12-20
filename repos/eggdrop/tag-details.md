<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.9`](#eggdrop19)
-	[`eggdrop:1.9.1`](#eggdrop191)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.9`

```console
$ docker pull eggdrop@sha256:ab65ba14de91293c02bc2a9909a3b27423e967daee0be8e884be85c7d41c3ad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9` - linux; amd64

```console
$ docker pull eggdrop@sha256:a59e974d59389e831ecae043d9231947218922df96c69901407b54511feb5dd7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8300231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3320c64a32dcb8d52b6b690ac0f5917c83ea68f23f0275f7a3307697731a4f1`
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
# Mon, 20 Dec 2021 18:26:07 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 20 Dec 2021 18:26:07 GMT
ENV NICK=
# Mon, 20 Dec 2021 18:26:07 GMT
ENV SERVER=
# Mon, 20 Dec 2021 18:26:07 GMT
ENV LISTEN=3333
# Mon, 20 Dec 2021 18:26:08 GMT
ENV OWNER=
# Mon, 20 Dec 2021 18:26:08 GMT
ENV USERFILE=eggdrop.user
# Mon, 20 Dec 2021 18:26:08 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 20 Dec 2021 18:26:08 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 20 Dec 2021 18:26:08 GMT
EXPOSE 3333
# Mon, 20 Dec 2021 18:26:09 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 20 Dec 2021 18:26:09 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 20 Dec 2021 18:26:09 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 20 Dec 2021 18:26:09 GMT
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
	-	`sha256:75453781d4ba6ab72c3aa76672d386b7bd980708060f020d4fd08af05644a688`  
		Last Modified: Mon, 20 Dec 2021 18:26:38 GMT  
		Size: 2.7 MB (2737657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e13c3189e960a2bdfa5a6d758cc8f13bfda93e6b0933f8135ae0ac206c002ff`  
		Last Modified: Mon, 20 Dec 2021 18:26:36 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9055f41d8d3e77c6f2e7821bf6ca5401ddfaf636a71f4e22ad2b987bed41e8`  
		Last Modified: Mon, 20 Dec 2021 18:26:36 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:aa2faecba35703de5960df23dd3f431bfff6b4699cdfb667b87187fc13787f29
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7995863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e5d9d81dcebbb3a85f2db2707f030bae36b3502c80b220d5055f4449899e12`
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
# Mon, 20 Dec 2021 18:55:07 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 20 Dec 2021 18:55:07 GMT
ENV NICK=
# Mon, 20 Dec 2021 18:55:07 GMT
ENV SERVER=
# Mon, 20 Dec 2021 18:55:08 GMT
ENV LISTEN=3333
# Mon, 20 Dec 2021 18:55:08 GMT
ENV OWNER=
# Mon, 20 Dec 2021 18:55:09 GMT
ENV USERFILE=eggdrop.user
# Mon, 20 Dec 2021 18:55:09 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 20 Dec 2021 18:55:10 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 20 Dec 2021 18:55:10 GMT
EXPOSE 3333
# Mon, 20 Dec 2021 18:55:10 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 20 Dec 2021 18:55:11 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 20 Dec 2021 18:55:11 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 20 Dec 2021 18:55:12 GMT
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
	-	`sha256:b78b5f406903a04bda7bbb459bb5b33b3a60aba062803f5460126fefad1a1b2c`  
		Last Modified: Mon, 20 Dec 2021 18:56:12 GMT  
		Size: 2.7 MB (2695671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93cae81e90ad647a7108d367010b12e9cb7ddf701ca120ef8e424709c74508f`  
		Last Modified: Mon, 20 Dec 2021 18:56:10 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daec29e788a27f42decfeda136b0c42f7ddb53529432c3bc0a936bf44dd016a5`  
		Last Modified: Mon, 20 Dec 2021 18:56:10 GMT  
		Size: 708.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:c8605c08e15d161ef475826cfe46d635b05970a3b77fce7532c9e3b686da6e03
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8217797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e11d3b171a49920bc2eac46a8bf5452e4fda3b2b43cd0b65cb5420fca95a5f3a`
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
# Mon, 20 Dec 2021 18:42:31 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 20 Dec 2021 18:42:32 GMT
ENV NICK=
# Mon, 20 Dec 2021 18:42:33 GMT
ENV SERVER=
# Mon, 20 Dec 2021 18:42:34 GMT
ENV LISTEN=3333
# Mon, 20 Dec 2021 18:42:35 GMT
ENV OWNER=
# Mon, 20 Dec 2021 18:42:36 GMT
ENV USERFILE=eggdrop.user
# Mon, 20 Dec 2021 18:42:37 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 20 Dec 2021 18:42:38 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 20 Dec 2021 18:42:39 GMT
EXPOSE 3333
# Mon, 20 Dec 2021 18:42:41 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 20 Dec 2021 18:42:42 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 20 Dec 2021 18:42:42 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 20 Dec 2021 18:42:43 GMT
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
	-	`sha256:4816c252e168170e0db2232d41191587363aaf8b8ea56e571ae047c8e2c92337`  
		Last Modified: Mon, 20 Dec 2021 18:43:25 GMT  
		Size: 2.7 MB (2731721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89aac700a86c40f4c26139bbb988bf1307c15fb842cc38cb82434dc2775d6bae`  
		Last Modified: Mon, 20 Dec 2021 18:43:24 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71eabf20c514a598b9e44d51cd05e0828b4dec6c2080f2e8267c405c653e448f`  
		Last Modified: Mon, 20 Dec 2021 18:43:24 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.9.1`

```console
$ docker pull eggdrop@sha256:ab65ba14de91293c02bc2a9909a3b27423e967daee0be8e884be85c7d41c3ad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9.1` - linux; amd64

```console
$ docker pull eggdrop@sha256:a59e974d59389e831ecae043d9231947218922df96c69901407b54511feb5dd7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8300231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3320c64a32dcb8d52b6b690ac0f5917c83ea68f23f0275f7a3307697731a4f1`
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
# Mon, 20 Dec 2021 18:26:07 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 20 Dec 2021 18:26:07 GMT
ENV NICK=
# Mon, 20 Dec 2021 18:26:07 GMT
ENV SERVER=
# Mon, 20 Dec 2021 18:26:07 GMT
ENV LISTEN=3333
# Mon, 20 Dec 2021 18:26:08 GMT
ENV OWNER=
# Mon, 20 Dec 2021 18:26:08 GMT
ENV USERFILE=eggdrop.user
# Mon, 20 Dec 2021 18:26:08 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 20 Dec 2021 18:26:08 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 20 Dec 2021 18:26:08 GMT
EXPOSE 3333
# Mon, 20 Dec 2021 18:26:09 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 20 Dec 2021 18:26:09 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 20 Dec 2021 18:26:09 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 20 Dec 2021 18:26:09 GMT
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
	-	`sha256:75453781d4ba6ab72c3aa76672d386b7bd980708060f020d4fd08af05644a688`  
		Last Modified: Mon, 20 Dec 2021 18:26:38 GMT  
		Size: 2.7 MB (2737657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e13c3189e960a2bdfa5a6d758cc8f13bfda93e6b0933f8135ae0ac206c002ff`  
		Last Modified: Mon, 20 Dec 2021 18:26:36 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9055f41d8d3e77c6f2e7821bf6ca5401ddfaf636a71f4e22ad2b987bed41e8`  
		Last Modified: Mon, 20 Dec 2021 18:26:36 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.1` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:aa2faecba35703de5960df23dd3f431bfff6b4699cdfb667b87187fc13787f29
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7995863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e5d9d81dcebbb3a85f2db2707f030bae36b3502c80b220d5055f4449899e12`
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
# Mon, 20 Dec 2021 18:55:07 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 20 Dec 2021 18:55:07 GMT
ENV NICK=
# Mon, 20 Dec 2021 18:55:07 GMT
ENV SERVER=
# Mon, 20 Dec 2021 18:55:08 GMT
ENV LISTEN=3333
# Mon, 20 Dec 2021 18:55:08 GMT
ENV OWNER=
# Mon, 20 Dec 2021 18:55:09 GMT
ENV USERFILE=eggdrop.user
# Mon, 20 Dec 2021 18:55:09 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 20 Dec 2021 18:55:10 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 20 Dec 2021 18:55:10 GMT
EXPOSE 3333
# Mon, 20 Dec 2021 18:55:10 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 20 Dec 2021 18:55:11 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 20 Dec 2021 18:55:11 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 20 Dec 2021 18:55:12 GMT
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
	-	`sha256:b78b5f406903a04bda7bbb459bb5b33b3a60aba062803f5460126fefad1a1b2c`  
		Last Modified: Mon, 20 Dec 2021 18:56:12 GMT  
		Size: 2.7 MB (2695671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93cae81e90ad647a7108d367010b12e9cb7ddf701ca120ef8e424709c74508f`  
		Last Modified: Mon, 20 Dec 2021 18:56:10 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daec29e788a27f42decfeda136b0c42f7ddb53529432c3bc0a936bf44dd016a5`  
		Last Modified: Mon, 20 Dec 2021 18:56:10 GMT  
		Size: 708.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.1` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:c8605c08e15d161ef475826cfe46d635b05970a3b77fce7532c9e3b686da6e03
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8217797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e11d3b171a49920bc2eac46a8bf5452e4fda3b2b43cd0b65cb5420fca95a5f3a`
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
# Mon, 20 Dec 2021 18:42:31 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 20 Dec 2021 18:42:32 GMT
ENV NICK=
# Mon, 20 Dec 2021 18:42:33 GMT
ENV SERVER=
# Mon, 20 Dec 2021 18:42:34 GMT
ENV LISTEN=3333
# Mon, 20 Dec 2021 18:42:35 GMT
ENV OWNER=
# Mon, 20 Dec 2021 18:42:36 GMT
ENV USERFILE=eggdrop.user
# Mon, 20 Dec 2021 18:42:37 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 20 Dec 2021 18:42:38 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 20 Dec 2021 18:42:39 GMT
EXPOSE 3333
# Mon, 20 Dec 2021 18:42:41 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 20 Dec 2021 18:42:42 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 20 Dec 2021 18:42:42 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 20 Dec 2021 18:42:43 GMT
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
	-	`sha256:4816c252e168170e0db2232d41191587363aaf8b8ea56e571ae047c8e2c92337`  
		Last Modified: Mon, 20 Dec 2021 18:43:25 GMT  
		Size: 2.7 MB (2731721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89aac700a86c40f4c26139bbb988bf1307c15fb842cc38cb82434dc2775d6bae`  
		Last Modified: Mon, 20 Dec 2021 18:43:24 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71eabf20c514a598b9e44d51cd05e0828b4dec6c2080f2e8267c405c653e448f`  
		Last Modified: Mon, 20 Dec 2021 18:43:24 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:0998c8aa6ff2df82ca2bd270e7c5e9347c9dc6292bf1985f4ad641b538cbeeb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:5fa809fa292d7563a397f722d123cc0f0f33a5d5019f8c10f75cb997702b5327
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14546697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8509dcb7bf17c5e92a49f940061c5cd01f229697c27c47b5be1182c07b5e0546`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Mon, 20 Dec 2021 18:24:00 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 20 Dec 2021 18:24:01 GMT
RUN adduser -S eggdrop
# Mon, 20 Dec 2021 18:24:02 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 20 Dec 2021 18:24:02 GMT
ENV EGGDROP_SHA256=65274734d14e9c8e4e42eb6eb2644cfad4e7bc8277dc5043c92ac4e8865c8862
# Mon, 20 Dec 2021 18:24:02 GMT
ENV EGGDROP_COMMIT=003b270a52db0a61c6ce17b460fe2af5f555e89c
# Mon, 20 Dec 2021 18:24:04 GMT
RUN apk --update add --no-cache tcl bash openssl
# Mon, 20 Dec 2021 18:25:01 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 20 Dec 2021 18:25:01 GMT
ENV NICK=
# Mon, 20 Dec 2021 18:25:01 GMT
ENV SERVER=
# Mon, 20 Dec 2021 18:25:01 GMT
ENV LISTEN=3333
# Mon, 20 Dec 2021 18:25:01 GMT
ENV OWNER=
# Mon, 20 Dec 2021 18:25:02 GMT
ENV USERFILE=eggdrop.user
# Mon, 20 Dec 2021 18:25:02 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 20 Dec 2021 18:25:02 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 20 Dec 2021 18:25:02 GMT
EXPOSE 3333
# Mon, 20 Dec 2021 18:25:03 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Mon, 20 Dec 2021 18:25:03 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 20 Dec 2021 18:25:03 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 20 Dec 2021 18:25:03 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed713bd6cbbd9be3b021bc6066c7ac35c629a6fe92ac700c27d569b3b15a121`  
		Last Modified: Mon, 20 Dec 2021 18:26:29 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031e84c3563ff6eca3bb11888ea34a407de531b6024b4410d33b0a155fef00f0`  
		Last Modified: Mon, 20 Dec 2021 18:26:27 GMT  
		Size: 10.9 KB (10913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed79ad9efcfd3de21e086839c1546d351d79fce81505f902da55c77b4d0d36a`  
		Last Modified: Mon, 20 Dec 2021 18:26:27 GMT  
		Size: 2.7 MB (2738314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18874a8ac67e67a317f79ee91f8682a199445d460e260c0f7db062325fc37641`  
		Last Modified: Mon, 20 Dec 2021 18:26:28 GMT  
		Size: 9.0 MB (8975227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7928ec0389478720e7642dbeb02ad57af7e1d9e24d0f9e85ce05c16485876910`  
		Last Modified: Mon, 20 Dec 2021 18:26:27 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f8fe1cac2c55e3e202ecb0e03f8109f52d6806cdfe5198653c3721d189aa08`  
		Last Modified: Mon, 20 Dec 2021 18:26:27 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:8648626f062ff23b25a0ecd6d9e908239e865609f9ff9c066fc40460ffb80686
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13992744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c480b89ca2daa9b778a449239398bf98c956b548cbf4e9481fdc62496f7d00f3`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Mon, 20 Dec 2021 18:49:34 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 20 Dec 2021 18:49:36 GMT
RUN adduser -S eggdrop
# Mon, 20 Dec 2021 18:49:38 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 20 Dec 2021 18:49:38 GMT
ENV EGGDROP_SHA256=65274734d14e9c8e4e42eb6eb2644cfad4e7bc8277dc5043c92ac4e8865c8862
# Mon, 20 Dec 2021 18:49:39 GMT
ENV EGGDROP_COMMIT=003b270a52db0a61c6ce17b460fe2af5f555e89c
# Mon, 20 Dec 2021 18:49:42 GMT
RUN apk --update add --no-cache tcl bash openssl
# Mon, 20 Dec 2021 18:52:18 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 20 Dec 2021 18:52:19 GMT
ENV NICK=
# Mon, 20 Dec 2021 18:52:19 GMT
ENV SERVER=
# Mon, 20 Dec 2021 18:52:19 GMT
ENV LISTEN=3333
# Mon, 20 Dec 2021 18:52:20 GMT
ENV OWNER=
# Mon, 20 Dec 2021 18:52:20 GMT
ENV USERFILE=eggdrop.user
# Mon, 20 Dec 2021 18:52:21 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 20 Dec 2021 18:52:21 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 20 Dec 2021 18:52:21 GMT
EXPOSE 3333
# Mon, 20 Dec 2021 18:52:22 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Mon, 20 Dec 2021 18:52:22 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 20 Dec 2021 18:52:23 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 20 Dec 2021 18:52:23 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc243557409786368279d787d8157e50ed7a007e916632a31ee21a604785c0ef`  
		Last Modified: Mon, 20 Dec 2021 18:55:55 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97acb3857a4d39a676d6a2a8f98aeba3a39129bed1a060d7f954bf8f7d0e1733`  
		Last Modified: Mon, 20 Dec 2021 18:55:53 GMT  
		Size: 10.6 KB (10618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6419e11e5e4ea688e729f84e69e5116d60c13981d1e6c9d6be8cd142123b69fa`  
		Last Modified: Mon, 20 Dec 2021 18:55:55 GMT  
		Size: 2.7 MB (2661986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb25918e07d9a24a4264a342948b8761ec73d070cd9542415ed22b030595019`  
		Last Modified: Mon, 20 Dec 2021 18:55:59 GMT  
		Size: 8.7 MB (8684875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c846ef6c2c86f3b24194a2fb926a0f4f2710d005deec7260c825f76864114af`  
		Last Modified: Mon, 20 Dec 2021 18:55:53 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe8e44ac1c464aa633fa2741a402b4f14fe9dd20fc1bed3726b8e162b646dda`  
		Last Modified: Mon, 20 Dec 2021 18:55:53 GMT  
		Size: 697.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:453be3b25365252d87cd56d2b50b1b809899ab86546d3900a0fcf7058893f8e8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14371904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155555288203b4f4db7b4faa3d05ae2923cdb35531ca04362e6652ad659a2984`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Mon, 20 Dec 2021 18:39:37 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 20 Dec 2021 18:39:38 GMT
RUN adduser -S eggdrop
# Mon, 20 Dec 2021 18:39:40 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 20 Dec 2021 18:39:41 GMT
ENV EGGDROP_SHA256=65274734d14e9c8e4e42eb6eb2644cfad4e7bc8277dc5043c92ac4e8865c8862
# Mon, 20 Dec 2021 18:39:42 GMT
ENV EGGDROP_COMMIT=003b270a52db0a61c6ce17b460fe2af5f555e89c
# Mon, 20 Dec 2021 18:39:44 GMT
RUN apk --update add --no-cache tcl bash openssl
# Mon, 20 Dec 2021 18:40:51 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 20 Dec 2021 18:40:52 GMT
ENV NICK=
# Mon, 20 Dec 2021 18:40:53 GMT
ENV SERVER=
# Mon, 20 Dec 2021 18:40:54 GMT
ENV LISTEN=3333
# Mon, 20 Dec 2021 18:40:55 GMT
ENV OWNER=
# Mon, 20 Dec 2021 18:40:56 GMT
ENV USERFILE=eggdrop.user
# Mon, 20 Dec 2021 18:40:57 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 20 Dec 2021 18:40:58 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 20 Dec 2021 18:40:59 GMT
EXPOSE 3333
# Mon, 20 Dec 2021 18:41:01 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Mon, 20 Dec 2021 18:41:02 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 20 Dec 2021 18:41:02 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 20 Dec 2021 18:41:03 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef35c2d5191ae20bb33e02c716cac04dc521bd3fc7fa3b3ec52d63c00fc228b6`  
		Last Modified: Mon, 20 Dec 2021 18:43:16 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1bf5d9fa6f3fa5c52d4b6af2c9b368bfe6ba40b1f28e7749fefff4c26aa7385`  
		Last Modified: Mon, 20 Dec 2021 18:43:14 GMT  
		Size: 10.6 KB (10635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91efd1708ab90d1aa6639116d9c94a82a402e3b8832f7040cf64b2395ba51e52`  
		Last Modified: Mon, 20 Dec 2021 18:43:15 GMT  
		Size: 2.8 MB (2760056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c7629429a379f749c19fbe4991ad1a72e3ae4668c2b9e3468cba5b6d814a62`  
		Last Modified: Mon, 20 Dec 2021 18:43:16 GMT  
		Size: 8.9 MB (8881953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaea4e16ede473bf02e8d483411b1fb3c61159d12063ec0f1f686cccf8be7c3b`  
		Last Modified: Mon, 20 Dec 2021 18:43:14 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e97b5c44e0414d19e12f15457f2492bb6ea4177d5e249185b763843da8a812`  
		Last Modified: Mon, 20 Dec 2021 18:43:14 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:ab65ba14de91293c02bc2a9909a3b27423e967daee0be8e884be85c7d41c3ad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:a59e974d59389e831ecae043d9231947218922df96c69901407b54511feb5dd7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8300231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3320c64a32dcb8d52b6b690ac0f5917c83ea68f23f0275f7a3307697731a4f1`
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
# Mon, 20 Dec 2021 18:26:07 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 20 Dec 2021 18:26:07 GMT
ENV NICK=
# Mon, 20 Dec 2021 18:26:07 GMT
ENV SERVER=
# Mon, 20 Dec 2021 18:26:07 GMT
ENV LISTEN=3333
# Mon, 20 Dec 2021 18:26:08 GMT
ENV OWNER=
# Mon, 20 Dec 2021 18:26:08 GMT
ENV USERFILE=eggdrop.user
# Mon, 20 Dec 2021 18:26:08 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 20 Dec 2021 18:26:08 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 20 Dec 2021 18:26:08 GMT
EXPOSE 3333
# Mon, 20 Dec 2021 18:26:09 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 20 Dec 2021 18:26:09 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 20 Dec 2021 18:26:09 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 20 Dec 2021 18:26:09 GMT
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
	-	`sha256:75453781d4ba6ab72c3aa76672d386b7bd980708060f020d4fd08af05644a688`  
		Last Modified: Mon, 20 Dec 2021 18:26:38 GMT  
		Size: 2.7 MB (2737657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e13c3189e960a2bdfa5a6d758cc8f13bfda93e6b0933f8135ae0ac206c002ff`  
		Last Modified: Mon, 20 Dec 2021 18:26:36 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9055f41d8d3e77c6f2e7821bf6ca5401ddfaf636a71f4e22ad2b987bed41e8`  
		Last Modified: Mon, 20 Dec 2021 18:26:36 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:aa2faecba35703de5960df23dd3f431bfff6b4699cdfb667b87187fc13787f29
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7995863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e5d9d81dcebbb3a85f2db2707f030bae36b3502c80b220d5055f4449899e12`
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
# Mon, 20 Dec 2021 18:55:07 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 20 Dec 2021 18:55:07 GMT
ENV NICK=
# Mon, 20 Dec 2021 18:55:07 GMT
ENV SERVER=
# Mon, 20 Dec 2021 18:55:08 GMT
ENV LISTEN=3333
# Mon, 20 Dec 2021 18:55:08 GMT
ENV OWNER=
# Mon, 20 Dec 2021 18:55:09 GMT
ENV USERFILE=eggdrop.user
# Mon, 20 Dec 2021 18:55:09 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 20 Dec 2021 18:55:10 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 20 Dec 2021 18:55:10 GMT
EXPOSE 3333
# Mon, 20 Dec 2021 18:55:10 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 20 Dec 2021 18:55:11 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 20 Dec 2021 18:55:11 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 20 Dec 2021 18:55:12 GMT
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
	-	`sha256:b78b5f406903a04bda7bbb459bb5b33b3a60aba062803f5460126fefad1a1b2c`  
		Last Modified: Mon, 20 Dec 2021 18:56:12 GMT  
		Size: 2.7 MB (2695671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93cae81e90ad647a7108d367010b12e9cb7ddf701ca120ef8e424709c74508f`  
		Last Modified: Mon, 20 Dec 2021 18:56:10 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daec29e788a27f42decfeda136b0c42f7ddb53529432c3bc0a936bf44dd016a5`  
		Last Modified: Mon, 20 Dec 2021 18:56:10 GMT  
		Size: 708.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:c8605c08e15d161ef475826cfe46d635b05970a3b77fce7532c9e3b686da6e03
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8217797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e11d3b171a49920bc2eac46a8bf5452e4fda3b2b43cd0b65cb5420fca95a5f3a`
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
# Mon, 20 Dec 2021 18:42:31 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 20 Dec 2021 18:42:32 GMT
ENV NICK=
# Mon, 20 Dec 2021 18:42:33 GMT
ENV SERVER=
# Mon, 20 Dec 2021 18:42:34 GMT
ENV LISTEN=3333
# Mon, 20 Dec 2021 18:42:35 GMT
ENV OWNER=
# Mon, 20 Dec 2021 18:42:36 GMT
ENV USERFILE=eggdrop.user
# Mon, 20 Dec 2021 18:42:37 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 20 Dec 2021 18:42:38 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 20 Dec 2021 18:42:39 GMT
EXPOSE 3333
# Mon, 20 Dec 2021 18:42:41 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 20 Dec 2021 18:42:42 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 20 Dec 2021 18:42:42 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 20 Dec 2021 18:42:43 GMT
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
	-	`sha256:4816c252e168170e0db2232d41191587363aaf8b8ea56e571ae047c8e2c92337`  
		Last Modified: Mon, 20 Dec 2021 18:43:25 GMT  
		Size: 2.7 MB (2731721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89aac700a86c40f4c26139bbb988bf1307c15fb842cc38cb82434dc2775d6bae`  
		Last Modified: Mon, 20 Dec 2021 18:43:24 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71eabf20c514a598b9e44d51cd05e0828b4dec6c2080f2e8267c405c653e448f`  
		Last Modified: Mon, 20 Dec 2021 18:43:24 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:ab65ba14de91293c02bc2a9909a3b27423e967daee0be8e884be85c7d41c3ad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:a59e974d59389e831ecae043d9231947218922df96c69901407b54511feb5dd7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8300231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3320c64a32dcb8d52b6b690ac0f5917c83ea68f23f0275f7a3307697731a4f1`
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
# Mon, 20 Dec 2021 18:26:07 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 20 Dec 2021 18:26:07 GMT
ENV NICK=
# Mon, 20 Dec 2021 18:26:07 GMT
ENV SERVER=
# Mon, 20 Dec 2021 18:26:07 GMT
ENV LISTEN=3333
# Mon, 20 Dec 2021 18:26:08 GMT
ENV OWNER=
# Mon, 20 Dec 2021 18:26:08 GMT
ENV USERFILE=eggdrop.user
# Mon, 20 Dec 2021 18:26:08 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 20 Dec 2021 18:26:08 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 20 Dec 2021 18:26:08 GMT
EXPOSE 3333
# Mon, 20 Dec 2021 18:26:09 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 20 Dec 2021 18:26:09 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 20 Dec 2021 18:26:09 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 20 Dec 2021 18:26:09 GMT
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
	-	`sha256:75453781d4ba6ab72c3aa76672d386b7bd980708060f020d4fd08af05644a688`  
		Last Modified: Mon, 20 Dec 2021 18:26:38 GMT  
		Size: 2.7 MB (2737657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e13c3189e960a2bdfa5a6d758cc8f13bfda93e6b0933f8135ae0ac206c002ff`  
		Last Modified: Mon, 20 Dec 2021 18:26:36 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9055f41d8d3e77c6f2e7821bf6ca5401ddfaf636a71f4e22ad2b987bed41e8`  
		Last Modified: Mon, 20 Dec 2021 18:26:36 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:aa2faecba35703de5960df23dd3f431bfff6b4699cdfb667b87187fc13787f29
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7995863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e5d9d81dcebbb3a85f2db2707f030bae36b3502c80b220d5055f4449899e12`
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
# Mon, 20 Dec 2021 18:55:07 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 20 Dec 2021 18:55:07 GMT
ENV NICK=
# Mon, 20 Dec 2021 18:55:07 GMT
ENV SERVER=
# Mon, 20 Dec 2021 18:55:08 GMT
ENV LISTEN=3333
# Mon, 20 Dec 2021 18:55:08 GMT
ENV OWNER=
# Mon, 20 Dec 2021 18:55:09 GMT
ENV USERFILE=eggdrop.user
# Mon, 20 Dec 2021 18:55:09 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 20 Dec 2021 18:55:10 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 20 Dec 2021 18:55:10 GMT
EXPOSE 3333
# Mon, 20 Dec 2021 18:55:10 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 20 Dec 2021 18:55:11 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 20 Dec 2021 18:55:11 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 20 Dec 2021 18:55:12 GMT
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
	-	`sha256:b78b5f406903a04bda7bbb459bb5b33b3a60aba062803f5460126fefad1a1b2c`  
		Last Modified: Mon, 20 Dec 2021 18:56:12 GMT  
		Size: 2.7 MB (2695671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93cae81e90ad647a7108d367010b12e9cb7ddf701ca120ef8e424709c74508f`  
		Last Modified: Mon, 20 Dec 2021 18:56:10 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daec29e788a27f42decfeda136b0c42f7ddb53529432c3bc0a936bf44dd016a5`  
		Last Modified: Mon, 20 Dec 2021 18:56:10 GMT  
		Size: 708.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:c8605c08e15d161ef475826cfe46d635b05970a3b77fce7532c9e3b686da6e03
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8217797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e11d3b171a49920bc2eac46a8bf5452e4fda3b2b43cd0b65cb5420fca95a5f3a`
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
# Mon, 20 Dec 2021 18:42:31 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 20 Dec 2021 18:42:32 GMT
ENV NICK=
# Mon, 20 Dec 2021 18:42:33 GMT
ENV SERVER=
# Mon, 20 Dec 2021 18:42:34 GMT
ENV LISTEN=3333
# Mon, 20 Dec 2021 18:42:35 GMT
ENV OWNER=
# Mon, 20 Dec 2021 18:42:36 GMT
ENV USERFILE=eggdrop.user
# Mon, 20 Dec 2021 18:42:37 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 20 Dec 2021 18:42:38 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 20 Dec 2021 18:42:39 GMT
EXPOSE 3333
# Mon, 20 Dec 2021 18:42:41 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 20 Dec 2021 18:42:42 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 20 Dec 2021 18:42:42 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 20 Dec 2021 18:42:43 GMT
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
	-	`sha256:4816c252e168170e0db2232d41191587363aaf8b8ea56e571ae047c8e2c92337`  
		Last Modified: Mon, 20 Dec 2021 18:43:25 GMT  
		Size: 2.7 MB (2731721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89aac700a86c40f4c26139bbb988bf1307c15fb842cc38cb82434dc2775d6bae`  
		Last Modified: Mon, 20 Dec 2021 18:43:24 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71eabf20c514a598b9e44d51cd05e0828b4dec6c2080f2e8267c405c653e448f`  
		Last Modified: Mon, 20 Dec 2021 18:43:24 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
