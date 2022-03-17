## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:e1fed67b11820c8f2406ce6234c16fafe956e876939c531312575326c110d491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:e49f298cb2e9e2f2e802edaa9a19cc482bcf74029faa98843994fe7aa98e6a9a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9767476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02576e601c28f1892b42557b2f916fcb832f175dd8b3cf2a85e582cd541c7a3b`
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
# Wed, 16 Mar 2022 17:25:25 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 16 Mar 2022 17:25:25 GMT
ENV NICK=
# Wed, 16 Mar 2022 17:25:25 GMT
ENV SERVER=
# Wed, 16 Mar 2022 17:25:25 GMT
ENV LISTEN=3333
# Wed, 16 Mar 2022 17:25:25 GMT
ENV OWNER=
# Wed, 16 Mar 2022 17:25:25 GMT
ENV USERFILE=eggdrop.user
# Wed, 16 Mar 2022 17:25:25 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 16 Mar 2022 17:25:25 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 16 Mar 2022 17:25:25 GMT
EXPOSE 3333
# Wed, 16 Mar 2022 17:25:26 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 16 Mar 2022 17:25:26 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 16 Mar 2022 17:25:26 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 16 Mar 2022 17:25:26 GMT
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
	-	`sha256:e042219553e908abc1c2cbb88b2deaf6800a593a292741d76f13002fc8d42776`  
		Last Modified: Wed, 16 Mar 2022 17:25:51 GMT  
		Size: 4.2 MB (4204907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e81597d040b7cdd032802ee42ff737f6d1fd6843ba0b21631dfec2df44ef80`  
		Last Modified: Wed, 16 Mar 2022 17:25:50 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1c4c2f9192430888a96251b7100c3ac53911e57ab2dd596520cd88e6aa955f`  
		Last Modified: Wed, 16 Mar 2022 17:25:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:c18551e5d206c1e9dcc67e60b763d9411c641408248d4b5bff370a8cec5301d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9220579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d62f3b1bea6b4320a2e8902d30c7b6f8bcc4732b78d63dfeb37b32bb0557c15`
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
# Wed, 16 Mar 2022 18:02:51 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 16 Mar 2022 18:02:51 GMT
ENV NICK=
# Wed, 16 Mar 2022 18:02:52 GMT
ENV SERVER=
# Wed, 16 Mar 2022 18:02:52 GMT
ENV LISTEN=3333
# Wed, 16 Mar 2022 18:02:53 GMT
ENV OWNER=
# Wed, 16 Mar 2022 18:02:53 GMT
ENV USERFILE=eggdrop.user
# Wed, 16 Mar 2022 18:02:53 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 16 Mar 2022 18:02:54 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 16 Mar 2022 18:02:54 GMT
EXPOSE 3333
# Wed, 16 Mar 2022 18:02:55 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 16 Mar 2022 18:02:55 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 16 Mar 2022 18:02:56 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 16 Mar 2022 18:02:56 GMT
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
	-	`sha256:67a28060f9975d86b954fc82dc2f2a09cd3a2f8d4fe1efc072b248fe80f15c19`  
		Last Modified: Wed, 16 Mar 2022 18:04:11 GMT  
		Size: 3.9 MB (3920385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f746b9c0006ed4e767dc9de5f4fa5d72aca33b9c0cdf1448b970ee41ccb05d`  
		Last Modified: Wed, 16 Mar 2022 18:04:08 GMT  
		Size: 1.8 KB (1846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9570c6f5cee84d0d068a74f7b9b5852438df136ddc5ef0fe3d2d2a7ba4da1eb1`  
		Last Modified: Wed, 16 Mar 2022 18:04:08 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:e3d07fc7d3d3e9edb80eea3045a2cf3a7d2e00c9129cc9c891ecd89130c9496c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9562984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ff212406fa2f4646697bc896f6a2b3e4d48da7ebd66ff3f97c5aba133ebf25`
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
# Wed, 16 Mar 2022 17:50:44 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 16 Mar 2022 17:50:45 GMT
ENV NICK=
# Wed, 16 Mar 2022 17:50:46 GMT
ENV SERVER=
# Wed, 16 Mar 2022 17:50:47 GMT
ENV LISTEN=3333
# Wed, 16 Mar 2022 17:50:48 GMT
ENV OWNER=
# Wed, 16 Mar 2022 17:50:49 GMT
ENV USERFILE=eggdrop.user
# Wed, 16 Mar 2022 17:50:50 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 16 Mar 2022 17:50:51 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 16 Mar 2022 17:50:52 GMT
EXPOSE 3333
# Wed, 16 Mar 2022 17:50:54 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 16 Mar 2022 17:50:55 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 16 Mar 2022 17:50:55 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 16 Mar 2022 17:50:56 GMT
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
	-	`sha256:8db202e82b0be9633674cb1ae3bf0d64527ed6d84552d2567e1c2d5fcfb61629`  
		Last Modified: Wed, 16 Mar 2022 17:51:30 GMT  
		Size: 4.1 MB (4076908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0960b0460f308b4db55f117594a0779d3fe56066e9862f0933a8443d47d6414`  
		Last Modified: Wed, 16 Mar 2022 17:51:30 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07313fee79ac5eeac7c17e483e9022c975b7f4c23fef10171ec9b1a51c6bf6b`  
		Last Modified: Wed, 16 Mar 2022 17:51:29 GMT  
		Size: 710.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
