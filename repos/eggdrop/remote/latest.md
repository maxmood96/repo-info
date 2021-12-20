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
