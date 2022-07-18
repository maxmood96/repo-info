<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.9`](#eggdrop19)
-	[`eggdrop:1.9.2`](#eggdrop192)
-	[`eggdrop:1.9.3rc1`](#eggdrop193rc1)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.9`

```console
$ docker pull eggdrop@sha256:faa227d56547d3820922135762c6ab1f39d5b25f6566848bf9a8bd7439571e7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9` - linux; amd64

```console
$ docker pull eggdrop@sha256:3b8f3d6d8d54caf3481cfa1460600229fc8c6da8e910fdbb99e39a74e56d020c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8284963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7e75710541da8025bad1f0029c3ca1af5388a757b7d20e89aca2a003e65400`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:14 GMT
ADD file:0f80c1db9ba5535d5020662b1c880624848316637bf3f9c189f459ab31f365d0 in / 
# Tue, 05 Apr 2022 00:20:14 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:16:32 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 11:16:33 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 11:16:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 11:16:35 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 05 Apr 2022 11:17:25 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 05 Apr 2022 11:17:26 GMT
ENV NICK=
# Tue, 05 Apr 2022 11:17:26 GMT
ENV SERVER=
# Tue, 05 Apr 2022 11:17:26 GMT
ENV LISTEN=3333
# Tue, 05 Apr 2022 11:17:26 GMT
ENV OWNER=
# Tue, 05 Apr 2022 11:17:26 GMT
ENV USERFILE=eggdrop.user
# Tue, 05 Apr 2022 11:17:26 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 05 Apr 2022 11:17:26 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 05 Apr 2022 11:17:26 GMT
EXPOSE 3333
# Tue, 05 Apr 2022 11:17:26 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 05 Apr 2022 11:17:26 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 05 Apr 2022 11:17:27 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 05 Apr 2022 11:17:27 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:6097bfa160c13665f946cea95b206a812a795d2517d7690a0a0796d64ec5f817`  
		Last Modified: Tue, 05 Apr 2022 00:21:00 GMT  
		Size: 2.8 MB (2819312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af7270901fcd1dae05f35973cd7825724dbc1bd998e39f5d71450e974a3153`  
		Last Modified: Tue, 05 Apr 2022 11:17:53 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa006e8c5e3fd9de6d58e77396feb8a3bc4a41181f023dfaaa0ff5ea2394ae7`  
		Last Modified: Tue, 05 Apr 2022 11:17:51 GMT  
		Size: 10.7 KB (10703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2356ac0c96e4675ed17f71ab61eb3b7302184d902b4c8b03940a9455937005aa`  
		Last Modified: Tue, 05 Apr 2022 11:17:51 GMT  
		Size: 2.7 MB (2726450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa54252a0927aac784047d4bb711cdb2300cf0ab2cb717b6a6c39d5f09d16274`  
		Last Modified: Tue, 05 Apr 2022 11:17:51 GMT  
		Size: 2.7 MB (2724699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefa2626779fae87079a5346e23ce3c837754cf74b4480391cc1fab89653b435`  
		Last Modified: Tue, 05 Apr 2022 11:17:51 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65c0dcfa91e1ea98c3a706cdb4c1caa0529339cc39fea214f12d278212eda12`  
		Last Modified: Tue, 05 Apr 2022 11:17:51 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:5f612a73564453d842b4d792dc9ae6e4242412b5b7a032b475c5be472d28e6d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7975642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf5abfb1dcefa42801e88040dbbcf28f1a958831415925b1b8f6be8fffc8808`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:50:07 GMT
ADD file:9e96de1fefc4e9efba26e76103eca5f1495f00a66a8d8207d493fa9eabed19c0 in / 
# Mon, 04 Apr 2022 23:50:07 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:42:42 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 03:42:43 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 03:42:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 03:42:49 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 05 Apr 2022 03:45:10 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 05 Apr 2022 03:45:10 GMT
ENV NICK=
# Tue, 05 Apr 2022 03:45:11 GMT
ENV SERVER=
# Tue, 05 Apr 2022 03:45:11 GMT
ENV LISTEN=3333
# Tue, 05 Apr 2022 03:45:12 GMT
ENV OWNER=
# Tue, 05 Apr 2022 03:45:12 GMT
ENV USERFILE=eggdrop.user
# Tue, 05 Apr 2022 03:45:12 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 05 Apr 2022 03:45:13 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 05 Apr 2022 03:45:13 GMT
EXPOSE 3333
# Tue, 05 Apr 2022 03:45:14 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 05 Apr 2022 03:45:14 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 05 Apr 2022 03:45:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 05 Apr 2022 03:45:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:83a39d5693a8029bb5246b7d72205357bcd5d8306489b586abf44bc8659dfc1e`  
		Last Modified: Mon, 04 Apr 2022 23:51:58 GMT  
		Size: 2.6 MB (2625144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216d0875ece6437b7759f658b19a743c65d8a0209dd6959b89006f06a7d4632d`  
		Last Modified: Tue, 05 Apr 2022 03:46:25 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb2483aeba1bc6bf4edfd57deb0a196f319c5338bf1032faa780a5f7d392477`  
		Last Modified: Tue, 05 Apr 2022 03:46:24 GMT  
		Size: 10.4 KB (10403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7883dd4bb4066fb7e7baa70d4271a40c7d91977982d50cc6b30892462da59f8b`  
		Last Modified: Tue, 05 Apr 2022 03:46:26 GMT  
		Size: 2.7 MB (2653002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c32b092000a7f5deeebdd19f48bf387342a0106dd81e475ba6110f073171679`  
		Last Modified: Tue, 05 Apr 2022 03:46:26 GMT  
		Size: 2.7 MB (2683288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45089181a50f12a8dcd62efc9ad43f63605aece6c118eddafefa51dfb361fc4`  
		Last Modified: Tue, 05 Apr 2022 03:46:24 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43385cdd604f9bac361f23a6a138a6e0e979410600f0c9a4d4fc9f564b16e1a`  
		Last Modified: Tue, 05 Apr 2022 03:46:24 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:a63be8915ecee00600434fbae83c83b8826ccf9163773af37a6529e5a9b4e5f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8206988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef7a72401b0431e568de59619be3e4194fd339d58d0312252354c864238658e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:46 GMT
ADD file:535e6f58c2cf7520c1824c8a290dc38c5519485470ed49587748a27c0113d586 in / 
# Mon, 04 Apr 2022 23:39:46 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:08:50 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 04:08:51 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 04:08:53 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 04:08:55 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 05 Apr 2022 04:10:00 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 05 Apr 2022 04:10:01 GMT
ENV NICK=
# Tue, 05 Apr 2022 04:10:02 GMT
ENV SERVER=
# Tue, 05 Apr 2022 04:10:03 GMT
ENV LISTEN=3333
# Tue, 05 Apr 2022 04:10:04 GMT
ENV OWNER=
# Tue, 05 Apr 2022 04:10:05 GMT
ENV USERFILE=eggdrop.user
# Tue, 05 Apr 2022 04:10:06 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 05 Apr 2022 04:10:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 05 Apr 2022 04:10:08 GMT
EXPOSE 3333
# Tue, 05 Apr 2022 04:10:10 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 05 Apr 2022 04:10:11 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 05 Apr 2022 04:10:11 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 05 Apr 2022 04:10:12 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:edd30f0f17040c7b292e0960fa771cf3ea45f994d7a2577a14fe02ae7ce727e9`  
		Last Modified: Mon, 04 Apr 2022 23:40:51 GMT  
		Size: 2.7 MB (2720895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad29698dd37ab923ffb59ccb8a25101399ae72afc52716f7abef24b92f50f6f8`  
		Last Modified: Tue, 05 Apr 2022 04:10:46 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8e549fca9947f4bb9b0c7445e2dec0e1372dcfcf71a2845b36869e8b5213a1`  
		Last Modified: Tue, 05 Apr 2022 04:10:44 GMT  
		Size: 10.5 KB (10481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019a83cb70204edfbb029b1bf19a37c13268c06f97b77a3e4a687d3ebdd9ba3f`  
		Last Modified: Tue, 05 Apr 2022 04:10:44 GMT  
		Size: 2.8 MB (2752068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1050eba79944e68ab2dec5b7978af9ef6ee179979ad364e1c6c8a578bc5ba17`  
		Last Modified: Tue, 05 Apr 2022 04:10:44 GMT  
		Size: 2.7 MB (2719773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec4e36daf9711164139c38e07f155b97f78ed76f76927146f1a8d483a1979e8`  
		Last Modified: Tue, 05 Apr 2022 04:10:44 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:035e6d3d5202a896ef25b0b1b67b32e046ec78a3f72d91637944160d57abff50`  
		Last Modified: Tue, 05 Apr 2022 04:10:44 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.9.2`

```console
$ docker pull eggdrop@sha256:faa227d56547d3820922135762c6ab1f39d5b25f6566848bf9a8bd7439571e7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9.2` - linux; amd64

```console
$ docker pull eggdrop@sha256:3b8f3d6d8d54caf3481cfa1460600229fc8c6da8e910fdbb99e39a74e56d020c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8284963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7e75710541da8025bad1f0029c3ca1af5388a757b7d20e89aca2a003e65400`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:14 GMT
ADD file:0f80c1db9ba5535d5020662b1c880624848316637bf3f9c189f459ab31f365d0 in / 
# Tue, 05 Apr 2022 00:20:14 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:16:32 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 11:16:33 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 11:16:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 11:16:35 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 05 Apr 2022 11:17:25 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 05 Apr 2022 11:17:26 GMT
ENV NICK=
# Tue, 05 Apr 2022 11:17:26 GMT
ENV SERVER=
# Tue, 05 Apr 2022 11:17:26 GMT
ENV LISTEN=3333
# Tue, 05 Apr 2022 11:17:26 GMT
ENV OWNER=
# Tue, 05 Apr 2022 11:17:26 GMT
ENV USERFILE=eggdrop.user
# Tue, 05 Apr 2022 11:17:26 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 05 Apr 2022 11:17:26 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 05 Apr 2022 11:17:26 GMT
EXPOSE 3333
# Tue, 05 Apr 2022 11:17:26 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 05 Apr 2022 11:17:26 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 05 Apr 2022 11:17:27 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 05 Apr 2022 11:17:27 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:6097bfa160c13665f946cea95b206a812a795d2517d7690a0a0796d64ec5f817`  
		Last Modified: Tue, 05 Apr 2022 00:21:00 GMT  
		Size: 2.8 MB (2819312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af7270901fcd1dae05f35973cd7825724dbc1bd998e39f5d71450e974a3153`  
		Last Modified: Tue, 05 Apr 2022 11:17:53 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa006e8c5e3fd9de6d58e77396feb8a3bc4a41181f023dfaaa0ff5ea2394ae7`  
		Last Modified: Tue, 05 Apr 2022 11:17:51 GMT  
		Size: 10.7 KB (10703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2356ac0c96e4675ed17f71ab61eb3b7302184d902b4c8b03940a9455937005aa`  
		Last Modified: Tue, 05 Apr 2022 11:17:51 GMT  
		Size: 2.7 MB (2726450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa54252a0927aac784047d4bb711cdb2300cf0ab2cb717b6a6c39d5f09d16274`  
		Last Modified: Tue, 05 Apr 2022 11:17:51 GMT  
		Size: 2.7 MB (2724699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefa2626779fae87079a5346e23ce3c837754cf74b4480391cc1fab89653b435`  
		Last Modified: Tue, 05 Apr 2022 11:17:51 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65c0dcfa91e1ea98c3a706cdb4c1caa0529339cc39fea214f12d278212eda12`  
		Last Modified: Tue, 05 Apr 2022 11:17:51 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.2` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:5f612a73564453d842b4d792dc9ae6e4242412b5b7a032b475c5be472d28e6d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7975642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf5abfb1dcefa42801e88040dbbcf28f1a958831415925b1b8f6be8fffc8808`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:50:07 GMT
ADD file:9e96de1fefc4e9efba26e76103eca5f1495f00a66a8d8207d493fa9eabed19c0 in / 
# Mon, 04 Apr 2022 23:50:07 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:42:42 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 03:42:43 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 03:42:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 03:42:49 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 05 Apr 2022 03:45:10 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 05 Apr 2022 03:45:10 GMT
ENV NICK=
# Tue, 05 Apr 2022 03:45:11 GMT
ENV SERVER=
# Tue, 05 Apr 2022 03:45:11 GMT
ENV LISTEN=3333
# Tue, 05 Apr 2022 03:45:12 GMT
ENV OWNER=
# Tue, 05 Apr 2022 03:45:12 GMT
ENV USERFILE=eggdrop.user
# Tue, 05 Apr 2022 03:45:12 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 05 Apr 2022 03:45:13 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 05 Apr 2022 03:45:13 GMT
EXPOSE 3333
# Tue, 05 Apr 2022 03:45:14 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 05 Apr 2022 03:45:14 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 05 Apr 2022 03:45:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 05 Apr 2022 03:45:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:83a39d5693a8029bb5246b7d72205357bcd5d8306489b586abf44bc8659dfc1e`  
		Last Modified: Mon, 04 Apr 2022 23:51:58 GMT  
		Size: 2.6 MB (2625144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216d0875ece6437b7759f658b19a743c65d8a0209dd6959b89006f06a7d4632d`  
		Last Modified: Tue, 05 Apr 2022 03:46:25 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb2483aeba1bc6bf4edfd57deb0a196f319c5338bf1032faa780a5f7d392477`  
		Last Modified: Tue, 05 Apr 2022 03:46:24 GMT  
		Size: 10.4 KB (10403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7883dd4bb4066fb7e7baa70d4271a40c7d91977982d50cc6b30892462da59f8b`  
		Last Modified: Tue, 05 Apr 2022 03:46:26 GMT  
		Size: 2.7 MB (2653002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c32b092000a7f5deeebdd19f48bf387342a0106dd81e475ba6110f073171679`  
		Last Modified: Tue, 05 Apr 2022 03:46:26 GMT  
		Size: 2.7 MB (2683288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45089181a50f12a8dcd62efc9ad43f63605aece6c118eddafefa51dfb361fc4`  
		Last Modified: Tue, 05 Apr 2022 03:46:24 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43385cdd604f9bac361f23a6a138a6e0e979410600f0c9a4d4fc9f564b16e1a`  
		Last Modified: Tue, 05 Apr 2022 03:46:24 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.2` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:a63be8915ecee00600434fbae83c83b8826ccf9163773af37a6529e5a9b4e5f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8206988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef7a72401b0431e568de59619be3e4194fd339d58d0312252354c864238658e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:46 GMT
ADD file:535e6f58c2cf7520c1824c8a290dc38c5519485470ed49587748a27c0113d586 in / 
# Mon, 04 Apr 2022 23:39:46 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:08:50 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 04:08:51 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 04:08:53 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 04:08:55 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 05 Apr 2022 04:10:00 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 05 Apr 2022 04:10:01 GMT
ENV NICK=
# Tue, 05 Apr 2022 04:10:02 GMT
ENV SERVER=
# Tue, 05 Apr 2022 04:10:03 GMT
ENV LISTEN=3333
# Tue, 05 Apr 2022 04:10:04 GMT
ENV OWNER=
# Tue, 05 Apr 2022 04:10:05 GMT
ENV USERFILE=eggdrop.user
# Tue, 05 Apr 2022 04:10:06 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 05 Apr 2022 04:10:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 05 Apr 2022 04:10:08 GMT
EXPOSE 3333
# Tue, 05 Apr 2022 04:10:10 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 05 Apr 2022 04:10:11 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 05 Apr 2022 04:10:11 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 05 Apr 2022 04:10:12 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:edd30f0f17040c7b292e0960fa771cf3ea45f994d7a2577a14fe02ae7ce727e9`  
		Last Modified: Mon, 04 Apr 2022 23:40:51 GMT  
		Size: 2.7 MB (2720895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad29698dd37ab923ffb59ccb8a25101399ae72afc52716f7abef24b92f50f6f8`  
		Last Modified: Tue, 05 Apr 2022 04:10:46 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8e549fca9947f4bb9b0c7445e2dec0e1372dcfcf71a2845b36869e8b5213a1`  
		Last Modified: Tue, 05 Apr 2022 04:10:44 GMT  
		Size: 10.5 KB (10481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019a83cb70204edfbb029b1bf19a37c13268c06f97b77a3e4a687d3ebdd9ba3f`  
		Last Modified: Tue, 05 Apr 2022 04:10:44 GMT  
		Size: 2.8 MB (2752068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1050eba79944e68ab2dec5b7978af9ef6ee179979ad364e1c6c8a578bc5ba17`  
		Last Modified: Tue, 05 Apr 2022 04:10:44 GMT  
		Size: 2.7 MB (2719773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec4e36daf9711164139c38e07f155b97f78ed76f76927146f1a8d483a1979e8`  
		Last Modified: Tue, 05 Apr 2022 04:10:44 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:035e6d3d5202a896ef25b0b1b67b32e046ec78a3f72d91637944160d57abff50`  
		Last Modified: Tue, 05 Apr 2022 04:10:44 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.9.3rc1`

```console
$ docker pull eggdrop@sha256:4e3c7d6135a98b79616a3f4defb4c34631ef7bb371d000ea3be3ff56fcd66a07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9.3rc1` - linux; amd64

```console
$ docker pull eggdrop@sha256:dad3de2ceae1edc30c94a020e51b8f117fe88687a4b90a5b0fae73a1dc062c87
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8171743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02efe040da836aa57f0fc9d953b58dc8d4e971cf1cf9aea1fc6d513dacf57619`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 21:01:24 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 18 Jul 2022 21:01:24 GMT
RUN adduser -S eggdrop
# Mon, 18 Jul 2022 21:01:25 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 18 Jul 2022 21:01:27 GMT
RUN apk add --no-cache tcl bash openssl
# Mon, 18 Jul 2022 21:02:24 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3rc1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3rc1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.3rc1.tar.gz.asc eggdrop-1.9.3rc1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.3rc1.tar.gz.asc   && tar -zxvf eggdrop-1.9.3rc1.tar.gz   && rm eggdrop-1.9.3rc1.tar.gz   && ( cd eggdrop-1.9.3rc1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.3rc1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 18 Jul 2022 21:02:24 GMT
ENV NICK=
# Mon, 18 Jul 2022 21:02:24 GMT
ENV SERVER=
# Mon, 18 Jul 2022 21:02:25 GMT
ENV LISTEN=3333
# Mon, 18 Jul 2022 21:02:25 GMT
ENV OWNER=
# Mon, 18 Jul 2022 21:02:25 GMT
ENV USERFILE=eggdrop.user
# Mon, 18 Jul 2022 21:02:25 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 18 Jul 2022 21:02:25 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 18 Jul 2022 21:02:25 GMT
EXPOSE 3333
# Mon, 18 Jul 2022 21:02:25 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 18 Jul 2022 21:02:25 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 18 Jul 2022 21:02:25 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 18 Jul 2022 21:02:26 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12dc67a7e62653d3846f08f84471b9d69a994cbb65f61425bbb86789475917dd`  
		Last Modified: Mon, 18 Jul 2022 21:02:47 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44665cacec565984be192fed4481df67032270ff87621de84494750202fe6c2b`  
		Last Modified: Mon, 18 Jul 2022 21:02:45 GMT  
		Size: 10.9 KB (10908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8ac8c6454f50c944d90e0d8d14c98a98f9a1fe4809a9b1ec66b8e17d566baf`  
		Last Modified: Mon, 18 Jul 2022 21:02:45 GMT  
		Size: 2.8 MB (2757814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43094664a37e2581a99fc1d530a8ad5568f27fe1f27d3093190647d2a762d648`  
		Last Modified: Mon, 18 Jul 2022 21:02:45 GMT  
		Size: 2.6 MB (2600417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1abda0d4645ea0f771a0113ecd80da64e140385c5eb2b174a4a55e4e85b1fec6`  
		Last Modified: Mon, 18 Jul 2022 21:02:45 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3611e0f5adbbc773b05f65982e3c0ac7412efabeb0553de5dbe6f6af2e0f163`  
		Last Modified: Mon, 18 Jul 2022 21:02:45 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.3rc1` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:3fdfbb48bef53ae668389c730f5c3374d7bfa5f21df8f0d537ae937e9fbc3888
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7915385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ff1592841c57427e2cc36617955b8692957eb7dd6426138ee2af26166ce1ec`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 18 Jul 2022 19:49:37 GMT
ADD file:7a20333469e71664904a0cb8f61613250f2bd092b4a27bfa7bbae1dc7e21b7ed in / 
# Mon, 18 Jul 2022 19:49:37 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 20:20:26 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 18 Jul 2022 20:20:27 GMT
RUN adduser -S eggdrop
# Mon, 18 Jul 2022 20:20:29 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 18 Jul 2022 20:20:33 GMT
RUN apk add --no-cache tcl bash openssl
# Mon, 18 Jul 2022 20:23:10 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3rc1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3rc1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.3rc1.tar.gz.asc eggdrop-1.9.3rc1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.3rc1.tar.gz.asc   && tar -zxvf eggdrop-1.9.3rc1.tar.gz   && rm eggdrop-1.9.3rc1.tar.gz   && ( cd eggdrop-1.9.3rc1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.3rc1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 18 Jul 2022 20:23:11 GMT
ENV NICK=
# Mon, 18 Jul 2022 20:23:11 GMT
ENV SERVER=
# Mon, 18 Jul 2022 20:23:12 GMT
ENV LISTEN=3333
# Mon, 18 Jul 2022 20:23:12 GMT
ENV OWNER=
# Mon, 18 Jul 2022 20:23:12 GMT
ENV USERFILE=eggdrop.user
# Mon, 18 Jul 2022 20:23:13 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 18 Jul 2022 20:23:13 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 18 Jul 2022 20:23:14 GMT
EXPOSE 3333
# Mon, 18 Jul 2022 20:23:14 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 18 Jul 2022 20:23:15 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 18 Jul 2022 20:23:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 18 Jul 2022 20:23:16 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:b7885075fcd06a866d12dfd56eb704045eaadbd22dc03a224cd98715be566677`  
		Last Modified: Mon, 18 Jul 2022 19:08:42 GMT  
		Size: 2.6 MB (2606431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4bf358da359bc34c989093c8a871f385d0b108bcf3fce18cdac4d543bd07da0`  
		Last Modified: Mon, 18 Jul 2022 20:24:12 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655d344c5652d10ea25461fe0aac12fa4820915b1dad8c306d3d481a01e8ba84`  
		Last Modified: Mon, 18 Jul 2022 20:24:10 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be3cf31cfdee484cf0e9f19889179f59587f5820afc365d5c921112ccbcad75`  
		Last Modified: Mon, 18 Jul 2022 20:24:12 GMT  
		Size: 2.7 MB (2679937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8741adee0ec9c7ad2d0f393d15a09cdb10d3771bb7dc910291696770356442f3`  
		Last Modified: Mon, 18 Jul 2022 20:24:12 GMT  
		Size: 2.6 MB (2614606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7150238cd34be8f321787abb7669f6b2de34281b317ea63d6ac52bdd333a77d`  
		Last Modified: Mon, 18 Jul 2022 20:24:10 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f06965c294b5f1246fb6700d2fac17ddc7b58475ced817eee9bf8c7358e84f`  
		Last Modified: Mon, 18 Jul 2022 20:24:10 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.3rc1` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:b8d38cd02babe304e81e8ffa8b0fcb87bb09f63f529835de821d6999cea7de24
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9469502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371d0bfb38b5426517ae43d7e5c2b960d451ca097173af04f1e3f302f6a94e7f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 23 May 2022 19:39:22 GMT
ADD file:3ae36c6c4a1fc43157692da97c6c4fa6c3d0189ba82e2bef7f5aaf4a5e083f18 in / 
# Mon, 23 May 2022 19:39:22 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 19:09:02 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 18 Jul 2022 19:09:03 GMT
RUN adduser -S eggdrop
# Mon, 18 Jul 2022 19:09:04 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 18 Jul 2022 19:09:06 GMT
RUN apk add --no-cache tcl bash openssl
# Mon, 18 Jul 2022 19:10:15 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3rc1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3rc1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.3rc1.tar.gz.asc eggdrop-1.9.3rc1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.3rc1.tar.gz.asc   && tar -zxvf eggdrop-1.9.3rc1.tar.gz   && rm eggdrop-1.9.3rc1.tar.gz   && ( cd eggdrop-1.9.3rc1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.3rc1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 18 Jul 2022 19:10:15 GMT
ENV NICK=
# Mon, 18 Jul 2022 19:10:16 GMT
ENV SERVER=
# Mon, 18 Jul 2022 19:10:17 GMT
ENV LISTEN=3333
# Mon, 18 Jul 2022 19:10:18 GMT
ENV OWNER=
# Mon, 18 Jul 2022 19:10:19 GMT
ENV USERFILE=eggdrop.user
# Mon, 18 Jul 2022 19:10:20 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 18 Jul 2022 19:10:21 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 18 Jul 2022 19:10:22 GMT
EXPOSE 3333
# Mon, 18 Jul 2022 19:10:24 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 18 Jul 2022 19:10:25 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 18 Jul 2022 19:10:25 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 18 Jul 2022 19:10:26 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:b3c136eddcbf2003d3180787cef00f39d46b9fd9e4623178282ad6a8d63ad3b0`  
		Last Modified: Mon, 23 May 2022 19:08:34 GMT  
		Size: 2.7 MB (2694464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01be248cb50723182b1e28f592c3632ed457405cdb9ba145862500914c9c43bd`  
		Last Modified: Mon, 18 Jul 2022 19:11:17 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b7a5c9a1c0e8f1626452df209844f62c68cb24c4e0738ce618a0036d36ca74`  
		Last Modified: Mon, 18 Jul 2022 19:11:15 GMT  
		Size: 10.6 KB (10615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ac00fc8b8873103dd5a9a8a3845d77a89c94344db9f39937bc7c5a2443ffe4`  
		Last Modified: Mon, 18 Jul 2022 19:11:15 GMT  
		Size: 2.8 MB (2775849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113bc41d743c6544ad59d989f905481a989405979c0ef3d9ed0609a3db9881b1`  
		Last Modified: Mon, 18 Jul 2022 19:11:15 GMT  
		Size: 4.0 MB (3984785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e5ed4e9da173123c02d12cf5e7576898a3c1f96697c002ba33f65746907810`  
		Last Modified: Mon, 18 Jul 2022 19:11:15 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36cf9bb51638f8a357baf161162a30662327e4d86bebbeb457257fb3db9045e`  
		Last Modified: Mon, 18 Jul 2022 19:11:15 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:1119f9826d82b78c5c45fe0378d6ad03482f1b7a3e768b7ae96dfe60f8ff5cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:fd04d974fd1c59c3b4b00aaebd1d423bbc8282e08f4fdd8511d1da02ee7e358b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41162459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b700906d1f334863ac63c56310df99794fa9b300cc8e2d62731f818b71cff6c`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:12:25 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 11:12:25 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 11:12:26 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 18 Jul 2022 20:04:56 GMT
ENV EGGDROP_SHA256=34915a9bf1870bb3759c68520df62443ba45e01558a53c991d2fb03db9b4ec72
# Mon, 18 Jul 2022 20:04:56 GMT
ENV EGGDROP_COMMIT=47962f7f15a1840b3f3c9ad1a6c247647d16de56
# Mon, 18 Jul 2022 20:04:57 GMT
RUN apk --update add --no-cache bash openssl
# Mon, 18 Jul 2022 20:09:08 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 18 Jul 2022 20:09:09 GMT
ENV NICK=
# Mon, 18 Jul 2022 20:09:09 GMT
ENV SERVER=
# Mon, 18 Jul 2022 20:09:09 GMT
ENV LISTEN=3333
# Mon, 18 Jul 2022 20:09:09 GMT
ENV OWNER=
# Mon, 18 Jul 2022 20:09:09 GMT
ENV USERFILE=eggdrop.user
# Mon, 18 Jul 2022 20:09:09 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 18 Jul 2022 20:09:09 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 18 Jul 2022 20:09:09 GMT
EXPOSE 3333
# Mon, 18 Jul 2022 20:09:09 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Mon, 18 Jul 2022 20:09:10 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 18 Jul 2022 20:09:10 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 18 Jul 2022 20:09:10 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5afb7ebc822c4005d25f15d49dada11e4a41876f643351d04feea9b2b22840cc`  
		Last Modified: Tue, 05 Apr 2022 11:17:40 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e7bd2972241b11e355dd2e732c2f4dbcbe0a9624d7b8c43e68e1b891810d4a`  
		Last Modified: Tue, 05 Apr 2022 11:17:38 GMT  
		Size: 10.9 KB (10946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d60371653cbbb6a799e42cb68c55b92664ae5911ef01810663a723143150e5`  
		Last Modified: Mon, 18 Jul 2022 20:10:40 GMT  
		Size: 1.1 MB (1089973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d2d24c077be4de74a52f909f02afcfc69d58682843febf251086770019f322`  
		Last Modified: Mon, 18 Jul 2022 20:10:46 GMT  
		Size: 37.2 MB (37243117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783f43bb535cfc33101e684d42ec7aa469226106f327c2b257dbd55c4b49876c`  
		Last Modified: Mon, 18 Jul 2022 20:10:40 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da194030311da981b6b28720ea05b81e3c14deea5af6f40ee0b6274ff0c839ee`  
		Last Modified: Mon, 18 Jul 2022 20:10:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:c9e126616745f437a1316d309084832d58151fafeb28b07c662db54fad03cf70
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40314778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545abc69ab2eef92b2edbf01cbdd08740e6842bd1e6b477d8e6047b6b96f7fe4`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:31:44 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 03:31:46 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 03:31:48 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 18 Jul 2022 18:49:45 GMT
ENV EGGDROP_SHA256=34915a9bf1870bb3759c68520df62443ba45e01558a53c991d2fb03db9b4ec72
# Mon, 18 Jul 2022 18:49:45 GMT
ENV EGGDROP_COMMIT=47962f7f15a1840b3f3c9ad1a6c247647d16de56
# Mon, 18 Jul 2022 18:49:48 GMT
RUN apk --update add --no-cache bash openssl
# Mon, 18 Jul 2022 19:00:28 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 18 Jul 2022 19:00:29 GMT
ENV NICK=
# Mon, 18 Jul 2022 19:00:29 GMT
ENV SERVER=
# Mon, 18 Jul 2022 19:00:29 GMT
ENV LISTEN=3333
# Mon, 18 Jul 2022 19:00:30 GMT
ENV OWNER=
# Mon, 18 Jul 2022 19:00:30 GMT
ENV USERFILE=eggdrop.user
# Mon, 18 Jul 2022 19:00:31 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 18 Jul 2022 19:00:31 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 18 Jul 2022 19:00:31 GMT
EXPOSE 3333
# Mon, 18 Jul 2022 19:00:32 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Mon, 18 Jul 2022 19:00:32 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 18 Jul 2022 19:00:33 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 18 Jul 2022 19:00:33 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f46acd206d1b9854dd7a69f3dd94d51ffb03228b347337d6755524e938f848d`  
		Last Modified: Tue, 05 Apr 2022 03:45:57 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ab9123d31326e4f773e35061abb57883ec6b6221e6df8719354fc8598c9123`  
		Last Modified: Tue, 05 Apr 2022 03:45:55 GMT  
		Size: 10.6 KB (10643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f36aa237eb1d5a61f87401541fbc3b6b7c9fa196207eeb0fa78f126ff9145e`  
		Last Modified: Mon, 18 Jul 2022 19:04:34 GMT  
		Size: 1.0 MB (1032591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad3257c3ec35772168580fe6515ac2a515576ab7e6ea173ee9db5868c50f2c8`  
		Last Modified: Mon, 18 Jul 2022 19:04:58 GMT  
		Size: 36.6 MB (36645704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bd986b36f8bae82826097ae809bd11ee15f40d48ba1753fc9a8309e4bc9772`  
		Last Modified: Mon, 18 Jul 2022 19:04:33 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ac6a5f8fc7f345fdc59052ce1153c7fc0f3c4e559a2ec14f6baaf732376285`  
		Last Modified: Mon, 18 Jul 2022 19:04:33 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:d83678d2eb7f05433e3077b917f5ae5d9bb3e0d04bcd2d3d50f0cdf65f59b77e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41105869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed5f47239adf5ad860a32263105693ed8520f07de6df888326210c8a4ce267e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:03:36 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 04:03:37 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 04:03:38 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 18 Jul 2022 19:04:00 GMT
ENV EGGDROP_SHA256=34915a9bf1870bb3759c68520df62443ba45e01558a53c991d2fb03db9b4ec72
# Mon, 18 Jul 2022 19:04:01 GMT
ENV EGGDROP_COMMIT=47962f7f15a1840b3f3c9ad1a6c247647d16de56
# Mon, 18 Jul 2022 19:04:03 GMT
RUN apk --update add --no-cache bash openssl
# Mon, 18 Jul 2022 19:08:41 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 18 Jul 2022 19:08:41 GMT
ENV NICK=
# Mon, 18 Jul 2022 19:08:42 GMT
ENV SERVER=
# Mon, 18 Jul 2022 19:08:43 GMT
ENV LISTEN=3333
# Mon, 18 Jul 2022 19:08:44 GMT
ENV OWNER=
# Mon, 18 Jul 2022 19:08:45 GMT
ENV USERFILE=eggdrop.user
# Mon, 18 Jul 2022 19:08:46 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 18 Jul 2022 19:08:47 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 18 Jul 2022 19:08:48 GMT
EXPOSE 3333
# Mon, 18 Jul 2022 19:08:50 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Mon, 18 Jul 2022 19:08:51 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 18 Jul 2022 19:08:51 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 18 Jul 2022 19:08:52 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687fbd14cec7fbb8ee2d3dfd1bedd832165c780a579635649359ea5d966007c3`  
		Last Modified: Tue, 05 Apr 2022 04:10:33 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778e0ebd563495b9fbda0eb57ed55b539e2a45c085cbb1dc1866b09b01007cb8`  
		Last Modified: Tue, 05 Apr 2022 04:10:31 GMT  
		Size: 10.7 KB (10674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52078216c257b43f5ec723592db0ef148d021477c2a3ae869e13b3c1b17540b7`  
		Last Modified: Mon, 18 Jul 2022 19:10:59 GMT  
		Size: 1.1 MB (1087601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b594dd26f8aef28728f4732d32d9b40b251de22d12f1aaae6fac53ec8c919954`  
		Last Modified: Mon, 18 Jul 2022 19:11:04 GMT  
		Size: 37.3 MB (37287276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d475a701cf7af470e6f914a72b4eecca7163c657883e7574156a121155d2486e`  
		Last Modified: Mon, 18 Jul 2022 19:10:58 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2599fbdb93451279b9f84ff9e86c8a93f494ef785aa457560446d3e9763fb3`  
		Last Modified: Mon, 18 Jul 2022 19:10:58 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:faa227d56547d3820922135762c6ab1f39d5b25f6566848bf9a8bd7439571e7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:3b8f3d6d8d54caf3481cfa1460600229fc8c6da8e910fdbb99e39a74e56d020c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8284963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7e75710541da8025bad1f0029c3ca1af5388a757b7d20e89aca2a003e65400`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:14 GMT
ADD file:0f80c1db9ba5535d5020662b1c880624848316637bf3f9c189f459ab31f365d0 in / 
# Tue, 05 Apr 2022 00:20:14 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:16:32 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 11:16:33 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 11:16:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 11:16:35 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 05 Apr 2022 11:17:25 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 05 Apr 2022 11:17:26 GMT
ENV NICK=
# Tue, 05 Apr 2022 11:17:26 GMT
ENV SERVER=
# Tue, 05 Apr 2022 11:17:26 GMT
ENV LISTEN=3333
# Tue, 05 Apr 2022 11:17:26 GMT
ENV OWNER=
# Tue, 05 Apr 2022 11:17:26 GMT
ENV USERFILE=eggdrop.user
# Tue, 05 Apr 2022 11:17:26 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 05 Apr 2022 11:17:26 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 05 Apr 2022 11:17:26 GMT
EXPOSE 3333
# Tue, 05 Apr 2022 11:17:26 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 05 Apr 2022 11:17:26 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 05 Apr 2022 11:17:27 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 05 Apr 2022 11:17:27 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:6097bfa160c13665f946cea95b206a812a795d2517d7690a0a0796d64ec5f817`  
		Last Modified: Tue, 05 Apr 2022 00:21:00 GMT  
		Size: 2.8 MB (2819312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af7270901fcd1dae05f35973cd7825724dbc1bd998e39f5d71450e974a3153`  
		Last Modified: Tue, 05 Apr 2022 11:17:53 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa006e8c5e3fd9de6d58e77396feb8a3bc4a41181f023dfaaa0ff5ea2394ae7`  
		Last Modified: Tue, 05 Apr 2022 11:17:51 GMT  
		Size: 10.7 KB (10703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2356ac0c96e4675ed17f71ab61eb3b7302184d902b4c8b03940a9455937005aa`  
		Last Modified: Tue, 05 Apr 2022 11:17:51 GMT  
		Size: 2.7 MB (2726450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa54252a0927aac784047d4bb711cdb2300cf0ab2cb717b6a6c39d5f09d16274`  
		Last Modified: Tue, 05 Apr 2022 11:17:51 GMT  
		Size: 2.7 MB (2724699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefa2626779fae87079a5346e23ce3c837754cf74b4480391cc1fab89653b435`  
		Last Modified: Tue, 05 Apr 2022 11:17:51 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65c0dcfa91e1ea98c3a706cdb4c1caa0529339cc39fea214f12d278212eda12`  
		Last Modified: Tue, 05 Apr 2022 11:17:51 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:5f612a73564453d842b4d792dc9ae6e4242412b5b7a032b475c5be472d28e6d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7975642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf5abfb1dcefa42801e88040dbbcf28f1a958831415925b1b8f6be8fffc8808`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:50:07 GMT
ADD file:9e96de1fefc4e9efba26e76103eca5f1495f00a66a8d8207d493fa9eabed19c0 in / 
# Mon, 04 Apr 2022 23:50:07 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:42:42 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 03:42:43 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 03:42:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 03:42:49 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 05 Apr 2022 03:45:10 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 05 Apr 2022 03:45:10 GMT
ENV NICK=
# Tue, 05 Apr 2022 03:45:11 GMT
ENV SERVER=
# Tue, 05 Apr 2022 03:45:11 GMT
ENV LISTEN=3333
# Tue, 05 Apr 2022 03:45:12 GMT
ENV OWNER=
# Tue, 05 Apr 2022 03:45:12 GMT
ENV USERFILE=eggdrop.user
# Tue, 05 Apr 2022 03:45:12 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 05 Apr 2022 03:45:13 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 05 Apr 2022 03:45:13 GMT
EXPOSE 3333
# Tue, 05 Apr 2022 03:45:14 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 05 Apr 2022 03:45:14 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 05 Apr 2022 03:45:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 05 Apr 2022 03:45:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:83a39d5693a8029bb5246b7d72205357bcd5d8306489b586abf44bc8659dfc1e`  
		Last Modified: Mon, 04 Apr 2022 23:51:58 GMT  
		Size: 2.6 MB (2625144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216d0875ece6437b7759f658b19a743c65d8a0209dd6959b89006f06a7d4632d`  
		Last Modified: Tue, 05 Apr 2022 03:46:25 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb2483aeba1bc6bf4edfd57deb0a196f319c5338bf1032faa780a5f7d392477`  
		Last Modified: Tue, 05 Apr 2022 03:46:24 GMT  
		Size: 10.4 KB (10403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7883dd4bb4066fb7e7baa70d4271a40c7d91977982d50cc6b30892462da59f8b`  
		Last Modified: Tue, 05 Apr 2022 03:46:26 GMT  
		Size: 2.7 MB (2653002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c32b092000a7f5deeebdd19f48bf387342a0106dd81e475ba6110f073171679`  
		Last Modified: Tue, 05 Apr 2022 03:46:26 GMT  
		Size: 2.7 MB (2683288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45089181a50f12a8dcd62efc9ad43f63605aece6c118eddafefa51dfb361fc4`  
		Last Modified: Tue, 05 Apr 2022 03:46:24 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43385cdd604f9bac361f23a6a138a6e0e979410600f0c9a4d4fc9f564b16e1a`  
		Last Modified: Tue, 05 Apr 2022 03:46:24 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:a63be8915ecee00600434fbae83c83b8826ccf9163773af37a6529e5a9b4e5f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8206988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef7a72401b0431e568de59619be3e4194fd339d58d0312252354c864238658e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:46 GMT
ADD file:535e6f58c2cf7520c1824c8a290dc38c5519485470ed49587748a27c0113d586 in / 
# Mon, 04 Apr 2022 23:39:46 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:08:50 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 04:08:51 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 04:08:53 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 04:08:55 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 05 Apr 2022 04:10:00 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 05 Apr 2022 04:10:01 GMT
ENV NICK=
# Tue, 05 Apr 2022 04:10:02 GMT
ENV SERVER=
# Tue, 05 Apr 2022 04:10:03 GMT
ENV LISTEN=3333
# Tue, 05 Apr 2022 04:10:04 GMT
ENV OWNER=
# Tue, 05 Apr 2022 04:10:05 GMT
ENV USERFILE=eggdrop.user
# Tue, 05 Apr 2022 04:10:06 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 05 Apr 2022 04:10:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 05 Apr 2022 04:10:08 GMT
EXPOSE 3333
# Tue, 05 Apr 2022 04:10:10 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 05 Apr 2022 04:10:11 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 05 Apr 2022 04:10:11 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 05 Apr 2022 04:10:12 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:edd30f0f17040c7b292e0960fa771cf3ea45f994d7a2577a14fe02ae7ce727e9`  
		Last Modified: Mon, 04 Apr 2022 23:40:51 GMT  
		Size: 2.7 MB (2720895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad29698dd37ab923ffb59ccb8a25101399ae72afc52716f7abef24b92f50f6f8`  
		Last Modified: Tue, 05 Apr 2022 04:10:46 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8e549fca9947f4bb9b0c7445e2dec0e1372dcfcf71a2845b36869e8b5213a1`  
		Last Modified: Tue, 05 Apr 2022 04:10:44 GMT  
		Size: 10.5 KB (10481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019a83cb70204edfbb029b1bf19a37c13268c06f97b77a3e4a687d3ebdd9ba3f`  
		Last Modified: Tue, 05 Apr 2022 04:10:44 GMT  
		Size: 2.8 MB (2752068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1050eba79944e68ab2dec5b7978af9ef6ee179979ad364e1c6c8a578bc5ba17`  
		Last Modified: Tue, 05 Apr 2022 04:10:44 GMT  
		Size: 2.7 MB (2719773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec4e36daf9711164139c38e07f155b97f78ed76f76927146f1a8d483a1979e8`  
		Last Modified: Tue, 05 Apr 2022 04:10:44 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:035e6d3d5202a896ef25b0b1b67b32e046ec78a3f72d91637944160d57abff50`  
		Last Modified: Tue, 05 Apr 2022 04:10:44 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:faa227d56547d3820922135762c6ab1f39d5b25f6566848bf9a8bd7439571e7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:3b8f3d6d8d54caf3481cfa1460600229fc8c6da8e910fdbb99e39a74e56d020c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8284963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7e75710541da8025bad1f0029c3ca1af5388a757b7d20e89aca2a003e65400`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:14 GMT
ADD file:0f80c1db9ba5535d5020662b1c880624848316637bf3f9c189f459ab31f365d0 in / 
# Tue, 05 Apr 2022 00:20:14 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:16:32 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 11:16:33 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 11:16:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 11:16:35 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 05 Apr 2022 11:17:25 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 05 Apr 2022 11:17:26 GMT
ENV NICK=
# Tue, 05 Apr 2022 11:17:26 GMT
ENV SERVER=
# Tue, 05 Apr 2022 11:17:26 GMT
ENV LISTEN=3333
# Tue, 05 Apr 2022 11:17:26 GMT
ENV OWNER=
# Tue, 05 Apr 2022 11:17:26 GMT
ENV USERFILE=eggdrop.user
# Tue, 05 Apr 2022 11:17:26 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 05 Apr 2022 11:17:26 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 05 Apr 2022 11:17:26 GMT
EXPOSE 3333
# Tue, 05 Apr 2022 11:17:26 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 05 Apr 2022 11:17:26 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 05 Apr 2022 11:17:27 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 05 Apr 2022 11:17:27 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:6097bfa160c13665f946cea95b206a812a795d2517d7690a0a0796d64ec5f817`  
		Last Modified: Tue, 05 Apr 2022 00:21:00 GMT  
		Size: 2.8 MB (2819312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af7270901fcd1dae05f35973cd7825724dbc1bd998e39f5d71450e974a3153`  
		Last Modified: Tue, 05 Apr 2022 11:17:53 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa006e8c5e3fd9de6d58e77396feb8a3bc4a41181f023dfaaa0ff5ea2394ae7`  
		Last Modified: Tue, 05 Apr 2022 11:17:51 GMT  
		Size: 10.7 KB (10703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2356ac0c96e4675ed17f71ab61eb3b7302184d902b4c8b03940a9455937005aa`  
		Last Modified: Tue, 05 Apr 2022 11:17:51 GMT  
		Size: 2.7 MB (2726450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa54252a0927aac784047d4bb711cdb2300cf0ab2cb717b6a6c39d5f09d16274`  
		Last Modified: Tue, 05 Apr 2022 11:17:51 GMT  
		Size: 2.7 MB (2724699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefa2626779fae87079a5346e23ce3c837754cf74b4480391cc1fab89653b435`  
		Last Modified: Tue, 05 Apr 2022 11:17:51 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65c0dcfa91e1ea98c3a706cdb4c1caa0529339cc39fea214f12d278212eda12`  
		Last Modified: Tue, 05 Apr 2022 11:17:51 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:5f612a73564453d842b4d792dc9ae6e4242412b5b7a032b475c5be472d28e6d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7975642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf5abfb1dcefa42801e88040dbbcf28f1a958831415925b1b8f6be8fffc8808`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:50:07 GMT
ADD file:9e96de1fefc4e9efba26e76103eca5f1495f00a66a8d8207d493fa9eabed19c0 in / 
# Mon, 04 Apr 2022 23:50:07 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:42:42 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 03:42:43 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 03:42:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 03:42:49 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 05 Apr 2022 03:45:10 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 05 Apr 2022 03:45:10 GMT
ENV NICK=
# Tue, 05 Apr 2022 03:45:11 GMT
ENV SERVER=
# Tue, 05 Apr 2022 03:45:11 GMT
ENV LISTEN=3333
# Tue, 05 Apr 2022 03:45:12 GMT
ENV OWNER=
# Tue, 05 Apr 2022 03:45:12 GMT
ENV USERFILE=eggdrop.user
# Tue, 05 Apr 2022 03:45:12 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 05 Apr 2022 03:45:13 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 05 Apr 2022 03:45:13 GMT
EXPOSE 3333
# Tue, 05 Apr 2022 03:45:14 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 05 Apr 2022 03:45:14 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 05 Apr 2022 03:45:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 05 Apr 2022 03:45:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:83a39d5693a8029bb5246b7d72205357bcd5d8306489b586abf44bc8659dfc1e`  
		Last Modified: Mon, 04 Apr 2022 23:51:58 GMT  
		Size: 2.6 MB (2625144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216d0875ece6437b7759f658b19a743c65d8a0209dd6959b89006f06a7d4632d`  
		Last Modified: Tue, 05 Apr 2022 03:46:25 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb2483aeba1bc6bf4edfd57deb0a196f319c5338bf1032faa780a5f7d392477`  
		Last Modified: Tue, 05 Apr 2022 03:46:24 GMT  
		Size: 10.4 KB (10403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7883dd4bb4066fb7e7baa70d4271a40c7d91977982d50cc6b30892462da59f8b`  
		Last Modified: Tue, 05 Apr 2022 03:46:26 GMT  
		Size: 2.7 MB (2653002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c32b092000a7f5deeebdd19f48bf387342a0106dd81e475ba6110f073171679`  
		Last Modified: Tue, 05 Apr 2022 03:46:26 GMT  
		Size: 2.7 MB (2683288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45089181a50f12a8dcd62efc9ad43f63605aece6c118eddafefa51dfb361fc4`  
		Last Modified: Tue, 05 Apr 2022 03:46:24 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43385cdd604f9bac361f23a6a138a6e0e979410600f0c9a4d4fc9f564b16e1a`  
		Last Modified: Tue, 05 Apr 2022 03:46:24 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:a63be8915ecee00600434fbae83c83b8826ccf9163773af37a6529e5a9b4e5f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8206988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef7a72401b0431e568de59619be3e4194fd339d58d0312252354c864238658e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:46 GMT
ADD file:535e6f58c2cf7520c1824c8a290dc38c5519485470ed49587748a27c0113d586 in / 
# Mon, 04 Apr 2022 23:39:46 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:08:50 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 04:08:51 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 04:08:53 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 04:08:55 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 05 Apr 2022 04:10:00 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 05 Apr 2022 04:10:01 GMT
ENV NICK=
# Tue, 05 Apr 2022 04:10:02 GMT
ENV SERVER=
# Tue, 05 Apr 2022 04:10:03 GMT
ENV LISTEN=3333
# Tue, 05 Apr 2022 04:10:04 GMT
ENV OWNER=
# Tue, 05 Apr 2022 04:10:05 GMT
ENV USERFILE=eggdrop.user
# Tue, 05 Apr 2022 04:10:06 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 05 Apr 2022 04:10:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 05 Apr 2022 04:10:08 GMT
EXPOSE 3333
# Tue, 05 Apr 2022 04:10:10 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 05 Apr 2022 04:10:11 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 05 Apr 2022 04:10:11 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 05 Apr 2022 04:10:12 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:edd30f0f17040c7b292e0960fa771cf3ea45f994d7a2577a14fe02ae7ce727e9`  
		Last Modified: Mon, 04 Apr 2022 23:40:51 GMT  
		Size: 2.7 MB (2720895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad29698dd37ab923ffb59ccb8a25101399ae72afc52716f7abef24b92f50f6f8`  
		Last Modified: Tue, 05 Apr 2022 04:10:46 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8e549fca9947f4bb9b0c7445e2dec0e1372dcfcf71a2845b36869e8b5213a1`  
		Last Modified: Tue, 05 Apr 2022 04:10:44 GMT  
		Size: 10.5 KB (10481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019a83cb70204edfbb029b1bf19a37c13268c06f97b77a3e4a687d3ebdd9ba3f`  
		Last Modified: Tue, 05 Apr 2022 04:10:44 GMT  
		Size: 2.8 MB (2752068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1050eba79944e68ab2dec5b7978af9ef6ee179979ad364e1c6c8a578bc5ba17`  
		Last Modified: Tue, 05 Apr 2022 04:10:44 GMT  
		Size: 2.7 MB (2719773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec4e36daf9711164139c38e07f155b97f78ed76f76927146f1a8d483a1979e8`  
		Last Modified: Tue, 05 Apr 2022 04:10:44 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:035e6d3d5202a896ef25b0b1b67b32e046ec78a3f72d91637944160d57abff50`  
		Last Modified: Tue, 05 Apr 2022 04:10:44 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
