<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.9`](#eggdrop19)
-	[`eggdrop:1.9.2`](#eggdrop192)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.9`

```console
$ docker pull eggdrop@sha256:be7b3b5f1d3ac12c3b479422e403c597966ec37f768a2d163667cba1b27bc9dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9` - linux; amd64

```console
$ docker pull eggdrop@sha256:f8959ecd7389c13f0b1c308a92909632723fed1a39a1e7e11be8967b339425dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8284831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a58c228898c4b45bd0873967892fc3c9f1ae67e216a9f6ab5176e530bf3973`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:46 GMT
ADD file:a2ef39a587aac85256b55bee81f17d73aaa7154b2a32a31527c7803fb889f2e7 in / 
# Tue, 29 Mar 2022 00:19:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:02:46 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 29 Mar 2022 12:02:46 GMT
RUN adduser -S eggdrop
# Tue, 29 Mar 2022 12:02:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 29 Mar 2022 12:02:49 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 29 Mar 2022 12:03:43 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 29 Mar 2022 12:03:43 GMT
ENV NICK=
# Tue, 29 Mar 2022 12:03:43 GMT
ENV SERVER=
# Tue, 29 Mar 2022 12:03:43 GMT
ENV LISTEN=3333
# Tue, 29 Mar 2022 12:03:43 GMT
ENV OWNER=
# Tue, 29 Mar 2022 12:03:44 GMT
ENV USERFILE=eggdrop.user
# Tue, 29 Mar 2022 12:03:44 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 29 Mar 2022 12:03:44 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 29 Mar 2022 12:03:44 GMT
EXPOSE 3333
# Tue, 29 Mar 2022 12:03:44 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 29 Mar 2022 12:03:44 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 29 Mar 2022 12:03:44 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 29 Mar 2022 12:03:44 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:b9c05db88786fd3c89b78787631257301391f898c03ba50553b556630046a741`  
		Last Modified: Tue, 29 Mar 2022 00:20:43 GMT  
		Size: 2.8 MB (2819223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9acac2e2c60780abd6b0e25869e85d9deb82a02ef2f59551172c88bea3f177d9`  
		Last Modified: Tue, 29 Mar 2022 12:04:19 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f63481626d334eabf1b3d8276a15c87932fcb09d476ae53aad900606e9dfaa`  
		Last Modified: Tue, 29 Mar 2022 12:04:16 GMT  
		Size: 10.7 KB (10693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc59cd14f7ab318b4cd643b4b21c2a2fbd9de695e06e6e9993f63bb9ef8c68`  
		Last Modified: Tue, 29 Mar 2022 12:04:17 GMT  
		Size: 2.7 MB (2726422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a787fa2eca8d7f7f9edcc027cc642019628754b70edf5bc41912f9246456d4`  
		Last Modified: Tue, 29 Mar 2022 12:04:17 GMT  
		Size: 2.7 MB (2724696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d69605e7aed6ad848eae6a5e270bb2ae5ab6cca147a7efa700bde818cca04ed`  
		Last Modified: Tue, 29 Mar 2022 12:04:16 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26a08d672007b6c13e248a18f5e3040cd0158213c2bebfb278f8a31d27d1c46`  
		Last Modified: Tue, 29 Mar 2022 12:04:16 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:fc709505f111fdbce3c7c2d010174e9ce05f8917cfa672a57bf3d684d12634d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7975684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027e12449683568173ac82fc9233610e76bcb8c122bc209ef6d05936dd92e684`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:56 GMT
ADD file:23d913551f75313e359a4e93592ea0a9655e1a7c2bec5fddd210717d70c3114b in / 
# Tue, 29 Mar 2022 00:49:57 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:35:03 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 29 Mar 2022 12:35:04 GMT
RUN adduser -S eggdrop
# Tue, 29 Mar 2022 12:35:06 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 29 Mar 2022 12:35:10 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 29 Mar 2022 12:37:33 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 29 Mar 2022 12:37:34 GMT
ENV NICK=
# Tue, 29 Mar 2022 12:37:34 GMT
ENV SERVER=
# Tue, 29 Mar 2022 12:37:35 GMT
ENV LISTEN=3333
# Tue, 29 Mar 2022 12:37:35 GMT
ENV OWNER=
# Tue, 29 Mar 2022 12:37:36 GMT
ENV USERFILE=eggdrop.user
# Tue, 29 Mar 2022 12:37:36 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 29 Mar 2022 12:37:37 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 29 Mar 2022 12:37:37 GMT
EXPOSE 3333
# Tue, 29 Mar 2022 12:37:38 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 29 Mar 2022 12:37:38 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 29 Mar 2022 12:37:39 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 29 Mar 2022 12:37:39 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:eba0847afba90891ea7dae672f5dadfa405a822df0bc9c00b9e3328fd5fd889c`  
		Last Modified: Tue, 29 Mar 2022 00:51:57 GMT  
		Size: 2.6 MB (2625139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47719ec1561d1e4862f2f9cfc89f920e35096fe46de845a2419822e784797b84`  
		Last Modified: Tue, 29 Mar 2022 12:38:47 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14771c9c03b4ccdbfd89671866cd4b954b4a1c64ce6357e27969542a72ab472`  
		Last Modified: Tue, 29 Mar 2022 12:38:45 GMT  
		Size: 10.4 KB (10405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78456caeb0d0f3345826024aee28dc462d3f732fca733f8b71bb3b687dab7bdf`  
		Last Modified: Tue, 29 Mar 2022 12:38:47 GMT  
		Size: 2.7 MB (2653026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d776a0092c26f0d42f45f1ccd7b14de0112d2b9e12a61bff28d59a01ba47d5fe`  
		Last Modified: Tue, 29 Mar 2022 12:38:47 GMT  
		Size: 2.7 MB (2683304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7a21c3e26575af12fd2822e1fbd2b11893a84dc339092de4ad09c4783d57fc`  
		Last Modified: Tue, 29 Mar 2022 12:38:46 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1553d7330f4de75064224e4485bf5c8c88cea6ec97e163d38b5fefa281b7680b`  
		Last Modified: Tue, 29 Mar 2022 12:38:45 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:cb0b62e745409481ea5ee7d094a40a023983befbb886255aa6dfd8dd64ff1c38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8206880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07c63ca9a05557355635ba09c2023e3a9c691e795cb5426bd5cf9b563e2fbe9`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:18 GMT
ADD file:3b8e0dac20ca40faf2aaf084b69476a222952f177c0e6ec90804a10c91a51feb in / 
# Tue, 29 Mar 2022 00:40:19 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:44:06 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 29 Mar 2022 08:44:07 GMT
RUN adduser -S eggdrop
# Tue, 29 Mar 2022 08:44:09 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 29 Mar 2022 08:44:11 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 29 Mar 2022 08:46:03 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 29 Mar 2022 08:46:04 GMT
ENV NICK=
# Tue, 29 Mar 2022 08:46:05 GMT
ENV SERVER=
# Tue, 29 Mar 2022 08:46:06 GMT
ENV LISTEN=3333
# Tue, 29 Mar 2022 08:46:07 GMT
ENV OWNER=
# Tue, 29 Mar 2022 08:46:08 GMT
ENV USERFILE=eggdrop.user
# Tue, 29 Mar 2022 08:46:09 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 29 Mar 2022 08:46:10 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 29 Mar 2022 08:46:11 GMT
EXPOSE 3333
# Tue, 29 Mar 2022 08:46:13 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 29 Mar 2022 08:46:14 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 29 Mar 2022 08:46:14 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 29 Mar 2022 08:46:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:4e7dd0becbc2dc968b69cba46c81a25fa500c88a644832ce17a5bb090925fa79`  
		Last Modified: Tue, 29 Mar 2022 00:41:37 GMT  
		Size: 2.7 MB (2720845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d8d6adaf5207ba27bf31cf8a052fd3227ef4bf57d8452bdae7e76abf78d4ab`  
		Last Modified: Tue, 29 Mar 2022 08:47:02 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0165d47b893704dcc5d6335a1073bfed26c1812d90b157b377f53a94a94df2`  
		Last Modified: Tue, 29 Mar 2022 08:47:00 GMT  
		Size: 10.5 KB (10484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eb57b1bdf04b5c6fd98f9075fe9a4136786078efc3f44ee2d8d89ac61ae3a3`  
		Last Modified: Tue, 29 Mar 2022 08:47:00 GMT  
		Size: 2.8 MB (2752095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e210cd6a352f10e15e5ffed220e2da94703f48ddf40639d629212a7d674832bc`  
		Last Modified: Tue, 29 Mar 2022 08:47:00 GMT  
		Size: 2.7 MB (2719683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e04e00273f225bcc569309d326a5b8040cef79755bb337be368e7eb969da9d`  
		Last Modified: Tue, 29 Mar 2022 08:47:00 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0abd5e1dc7453538deb3f86d5f1b45e5df7e988889c7ff574947f3ee22e9023`  
		Last Modified: Tue, 29 Mar 2022 08:47:00 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.9.2`

```console
$ docker pull eggdrop@sha256:be7b3b5f1d3ac12c3b479422e403c597966ec37f768a2d163667cba1b27bc9dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9.2` - linux; amd64

```console
$ docker pull eggdrop@sha256:f8959ecd7389c13f0b1c308a92909632723fed1a39a1e7e11be8967b339425dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8284831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a58c228898c4b45bd0873967892fc3c9f1ae67e216a9f6ab5176e530bf3973`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:46 GMT
ADD file:a2ef39a587aac85256b55bee81f17d73aaa7154b2a32a31527c7803fb889f2e7 in / 
# Tue, 29 Mar 2022 00:19:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:02:46 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 29 Mar 2022 12:02:46 GMT
RUN adduser -S eggdrop
# Tue, 29 Mar 2022 12:02:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 29 Mar 2022 12:02:49 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 29 Mar 2022 12:03:43 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 29 Mar 2022 12:03:43 GMT
ENV NICK=
# Tue, 29 Mar 2022 12:03:43 GMT
ENV SERVER=
# Tue, 29 Mar 2022 12:03:43 GMT
ENV LISTEN=3333
# Tue, 29 Mar 2022 12:03:43 GMT
ENV OWNER=
# Tue, 29 Mar 2022 12:03:44 GMT
ENV USERFILE=eggdrop.user
# Tue, 29 Mar 2022 12:03:44 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 29 Mar 2022 12:03:44 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 29 Mar 2022 12:03:44 GMT
EXPOSE 3333
# Tue, 29 Mar 2022 12:03:44 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 29 Mar 2022 12:03:44 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 29 Mar 2022 12:03:44 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 29 Mar 2022 12:03:44 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:b9c05db88786fd3c89b78787631257301391f898c03ba50553b556630046a741`  
		Last Modified: Tue, 29 Mar 2022 00:20:43 GMT  
		Size: 2.8 MB (2819223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9acac2e2c60780abd6b0e25869e85d9deb82a02ef2f59551172c88bea3f177d9`  
		Last Modified: Tue, 29 Mar 2022 12:04:19 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f63481626d334eabf1b3d8276a15c87932fcb09d476ae53aad900606e9dfaa`  
		Last Modified: Tue, 29 Mar 2022 12:04:16 GMT  
		Size: 10.7 KB (10693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc59cd14f7ab318b4cd643b4b21c2a2fbd9de695e06e6e9993f63bb9ef8c68`  
		Last Modified: Tue, 29 Mar 2022 12:04:17 GMT  
		Size: 2.7 MB (2726422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a787fa2eca8d7f7f9edcc027cc642019628754b70edf5bc41912f9246456d4`  
		Last Modified: Tue, 29 Mar 2022 12:04:17 GMT  
		Size: 2.7 MB (2724696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d69605e7aed6ad848eae6a5e270bb2ae5ab6cca147a7efa700bde818cca04ed`  
		Last Modified: Tue, 29 Mar 2022 12:04:16 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26a08d672007b6c13e248a18f5e3040cd0158213c2bebfb278f8a31d27d1c46`  
		Last Modified: Tue, 29 Mar 2022 12:04:16 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.2` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:fc709505f111fdbce3c7c2d010174e9ce05f8917cfa672a57bf3d684d12634d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7975684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027e12449683568173ac82fc9233610e76bcb8c122bc209ef6d05936dd92e684`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:56 GMT
ADD file:23d913551f75313e359a4e93592ea0a9655e1a7c2bec5fddd210717d70c3114b in / 
# Tue, 29 Mar 2022 00:49:57 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:35:03 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 29 Mar 2022 12:35:04 GMT
RUN adduser -S eggdrop
# Tue, 29 Mar 2022 12:35:06 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 29 Mar 2022 12:35:10 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 29 Mar 2022 12:37:33 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 29 Mar 2022 12:37:34 GMT
ENV NICK=
# Tue, 29 Mar 2022 12:37:34 GMT
ENV SERVER=
# Tue, 29 Mar 2022 12:37:35 GMT
ENV LISTEN=3333
# Tue, 29 Mar 2022 12:37:35 GMT
ENV OWNER=
# Tue, 29 Mar 2022 12:37:36 GMT
ENV USERFILE=eggdrop.user
# Tue, 29 Mar 2022 12:37:36 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 29 Mar 2022 12:37:37 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 29 Mar 2022 12:37:37 GMT
EXPOSE 3333
# Tue, 29 Mar 2022 12:37:38 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 29 Mar 2022 12:37:38 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 29 Mar 2022 12:37:39 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 29 Mar 2022 12:37:39 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:eba0847afba90891ea7dae672f5dadfa405a822df0bc9c00b9e3328fd5fd889c`  
		Last Modified: Tue, 29 Mar 2022 00:51:57 GMT  
		Size: 2.6 MB (2625139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47719ec1561d1e4862f2f9cfc89f920e35096fe46de845a2419822e784797b84`  
		Last Modified: Tue, 29 Mar 2022 12:38:47 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14771c9c03b4ccdbfd89671866cd4b954b4a1c64ce6357e27969542a72ab472`  
		Last Modified: Tue, 29 Mar 2022 12:38:45 GMT  
		Size: 10.4 KB (10405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78456caeb0d0f3345826024aee28dc462d3f732fca733f8b71bb3b687dab7bdf`  
		Last Modified: Tue, 29 Mar 2022 12:38:47 GMT  
		Size: 2.7 MB (2653026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d776a0092c26f0d42f45f1ccd7b14de0112d2b9e12a61bff28d59a01ba47d5fe`  
		Last Modified: Tue, 29 Mar 2022 12:38:47 GMT  
		Size: 2.7 MB (2683304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7a21c3e26575af12fd2822e1fbd2b11893a84dc339092de4ad09c4783d57fc`  
		Last Modified: Tue, 29 Mar 2022 12:38:46 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1553d7330f4de75064224e4485bf5c8c88cea6ec97e163d38b5fefa281b7680b`  
		Last Modified: Tue, 29 Mar 2022 12:38:45 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.2` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:cb0b62e745409481ea5ee7d094a40a023983befbb886255aa6dfd8dd64ff1c38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8206880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07c63ca9a05557355635ba09c2023e3a9c691e795cb5426bd5cf9b563e2fbe9`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:18 GMT
ADD file:3b8e0dac20ca40faf2aaf084b69476a222952f177c0e6ec90804a10c91a51feb in / 
# Tue, 29 Mar 2022 00:40:19 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:44:06 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 29 Mar 2022 08:44:07 GMT
RUN adduser -S eggdrop
# Tue, 29 Mar 2022 08:44:09 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 29 Mar 2022 08:44:11 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 29 Mar 2022 08:46:03 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 29 Mar 2022 08:46:04 GMT
ENV NICK=
# Tue, 29 Mar 2022 08:46:05 GMT
ENV SERVER=
# Tue, 29 Mar 2022 08:46:06 GMT
ENV LISTEN=3333
# Tue, 29 Mar 2022 08:46:07 GMT
ENV OWNER=
# Tue, 29 Mar 2022 08:46:08 GMT
ENV USERFILE=eggdrop.user
# Tue, 29 Mar 2022 08:46:09 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 29 Mar 2022 08:46:10 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 29 Mar 2022 08:46:11 GMT
EXPOSE 3333
# Tue, 29 Mar 2022 08:46:13 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 29 Mar 2022 08:46:14 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 29 Mar 2022 08:46:14 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 29 Mar 2022 08:46:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:4e7dd0becbc2dc968b69cba46c81a25fa500c88a644832ce17a5bb090925fa79`  
		Last Modified: Tue, 29 Mar 2022 00:41:37 GMT  
		Size: 2.7 MB (2720845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d8d6adaf5207ba27bf31cf8a052fd3227ef4bf57d8452bdae7e76abf78d4ab`  
		Last Modified: Tue, 29 Mar 2022 08:47:02 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0165d47b893704dcc5d6335a1073bfed26c1812d90b157b377f53a94a94df2`  
		Last Modified: Tue, 29 Mar 2022 08:47:00 GMT  
		Size: 10.5 KB (10484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eb57b1bdf04b5c6fd98f9075fe9a4136786078efc3f44ee2d8d89ac61ae3a3`  
		Last Modified: Tue, 29 Mar 2022 08:47:00 GMT  
		Size: 2.8 MB (2752095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e210cd6a352f10e15e5ffed220e2da94703f48ddf40639d629212a7d674832bc`  
		Last Modified: Tue, 29 Mar 2022 08:47:00 GMT  
		Size: 2.7 MB (2719683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e04e00273f225bcc569309d326a5b8040cef79755bb337be368e7eb969da9d`  
		Last Modified: Tue, 29 Mar 2022 08:47:00 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0abd5e1dc7453538deb3f86d5f1b45e5df7e988889c7ff574947f3ee22e9023`  
		Last Modified: Tue, 29 Mar 2022 08:47:00 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:5b10997c6073911238c5c8b8b353f5fe68bf0f4ef8e9c5ce92aa8fd402436fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:1aeebd57ae1707c3710b46b7e33409e2b0fbfe6493731ea692e380dba408e394
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39770851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4694c76ab607e85da34b92dae862739842f70ab6d675902bacd27bbab2b959`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 11:58:38 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 29 Mar 2022 11:58:39 GMT
RUN adduser -S eggdrop
# Tue, 29 Mar 2022 11:58:40 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 29 Mar 2022 11:58:40 GMT
ENV EGGDROP_SHA256=85700bdd1e5e709e7ac44fc4cac3bf06ab674ead4fb1df99f1ba8cb892c27a3c
# Tue, 29 Mar 2022 11:58:40 GMT
ENV EGGDROP_COMMIT=6959f1943659db6117b93262d18b27dd98313206
# Tue, 29 Mar 2022 11:58:41 GMT
RUN apk --update add --no-cache bash openssl
# Tue, 29 Mar 2022 12:02:29 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 29 Mar 2022 12:02:29 GMT
ENV NICK=
# Tue, 29 Mar 2022 12:02:29 GMT
ENV SERVER=
# Tue, 29 Mar 2022 12:02:29 GMT
ENV LISTEN=3333
# Tue, 29 Mar 2022 12:02:30 GMT
ENV OWNER=
# Tue, 29 Mar 2022 12:02:30 GMT
ENV USERFILE=eggdrop.user
# Tue, 29 Mar 2022 12:02:30 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 29 Mar 2022 12:02:30 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 29 Mar 2022 12:02:30 GMT
EXPOSE 3333
# Tue, 29 Mar 2022 12:02:30 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Tue, 29 Mar 2022 12:02:30 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 29 Mar 2022 12:02:30 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 29 Mar 2022 12:02:30 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fb61010abf5a69cbde6fef350ccb3f1cccdb738a529a130007939fb12aa7bc`  
		Last Modified: Tue, 29 Mar 2022 12:04:07 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ca98fe50b6a7460ca0403abdbdfe56f9f0f65ad028d0646a1c426a65a2af26`  
		Last Modified: Tue, 29 Mar 2022 12:04:04 GMT  
		Size: 10.9 KB (10947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f973893e5f0430443a84b87f5d35b80d20b2609e7a32d53ff3b71851430c41`  
		Last Modified: Tue, 29 Mar 2022 12:04:05 GMT  
		Size: 1.1 MB (1089643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dc78d5804f959f865916cd011afe1cf55cbd14a725b5559f15dbff9c3dffe9`  
		Last Modified: Tue, 29 Mar 2022 12:04:10 GMT  
		Size: 35.9 MB (35851903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf69ecc0001bcbe74f66625dd25d9afecaa67722bfbb0385c300e9d9363fb542`  
		Last Modified: Tue, 29 Mar 2022 12:04:04 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa21b18065fc4618ccc656606eb3a3bab4b10bafb95838f61fd9181e2aca745`  
		Last Modified: Tue, 29 Mar 2022 12:04:04 GMT  
		Size: 697.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:36f6b063b1ae647368fb44b152165fa6fc54a61c5224ba4e8f497bf28e086a36
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39165960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff18f6351921aba72532c6816d77b850e26a75f3e98ff7f99e50e4f3e09ad8d`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:32 GMT
ADD file:44acf536d487bec7f7bf16561f4ec90e60d4447b3cbabfeca66953c4491aabeb in / 
# Tue, 29 Mar 2022 00:49:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:24:20 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 29 Mar 2022 12:24:21 GMT
RUN adduser -S eggdrop
# Tue, 29 Mar 2022 12:24:24 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 29 Mar 2022 12:24:24 GMT
ENV EGGDROP_SHA256=85700bdd1e5e709e7ac44fc4cac3bf06ab674ead4fb1df99f1ba8cb892c27a3c
# Tue, 29 Mar 2022 12:24:25 GMT
ENV EGGDROP_COMMIT=6959f1943659db6117b93262d18b27dd98313206
# Tue, 29 Mar 2022 12:24:27 GMT
RUN apk --update add --no-cache bash openssl
# Tue, 29 Mar 2022 12:34:43 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 29 Mar 2022 12:34:44 GMT
ENV NICK=
# Tue, 29 Mar 2022 12:34:45 GMT
ENV SERVER=
# Tue, 29 Mar 2022 12:34:45 GMT
ENV LISTEN=3333
# Tue, 29 Mar 2022 12:34:45 GMT
ENV OWNER=
# Tue, 29 Mar 2022 12:34:46 GMT
ENV USERFILE=eggdrop.user
# Tue, 29 Mar 2022 12:34:46 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 29 Mar 2022 12:34:47 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 29 Mar 2022 12:34:47 GMT
EXPOSE 3333
# Tue, 29 Mar 2022 12:34:48 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Tue, 29 Mar 2022 12:34:48 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 29 Mar 2022 12:34:48 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 29 Mar 2022 12:34:49 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:84f033dabe5013c0dfae4263abd951011719d0a15adc3c7312c5be994deff030`  
		Last Modified: Tue, 29 Mar 2022 00:51:25 GMT  
		Size: 2.6 MB (2621943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63240a16b38668f610edc5128f225a877039b118ae7f255a574b811a91b15e92`  
		Last Modified: Tue, 29 Mar 2022 12:38:16 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc9e6b8e28e12fa0728973197f40a2838c284d504a3db2249220cbc7ef19c42`  
		Last Modified: Tue, 29 Mar 2022 12:38:15 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ffdfc75128ae9df071d1d654315e4d2ed9cd461e8c20b786ffbb24ec887cfe`  
		Last Modified: Tue, 29 Mar 2022 12:38:15 GMT  
		Size: 1.0 MB (1032375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed0edfb653bf36be23398e354e32830ee8a056d774e1bd208c0a2fa6dcbae01`  
		Last Modified: Tue, 29 Mar 2022 12:38:38 GMT  
		Size: 35.5 MB (35497132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a898162cb59c4690bd86db28d5e445f2d6495573c05c0e574ee4c9c269f50302`  
		Last Modified: Tue, 29 Mar 2022 12:38:15 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:166051ee680cb8f2fb7f955de719075cc4131997e69246cc7db6f22cd1babb34`  
		Last Modified: Tue, 29 Mar 2022 12:38:15 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:bc754a00e69a169738dffcf72c407b245523b362270176024c41263ad49c351b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39840405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df4ec45f1c8cb1603eacfbb9975b2cc0340b1725074f2c3fd4b1bdd6a013e66`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:35:52 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 29 Mar 2022 08:35:52 GMT
RUN adduser -S eggdrop
# Tue, 29 Mar 2022 08:35:54 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 29 Mar 2022 08:35:55 GMT
ENV EGGDROP_SHA256=85700bdd1e5e709e7ac44fc4cac3bf06ab674ead4fb1df99f1ba8cb892c27a3c
# Tue, 29 Mar 2022 08:35:56 GMT
ENV EGGDROP_COMMIT=6959f1943659db6117b93262d18b27dd98313206
# Tue, 29 Mar 2022 08:35:58 GMT
RUN apk --update add --no-cache bash openssl
# Tue, 29 Mar 2022 08:43:43 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 29 Mar 2022 08:43:43 GMT
ENV NICK=
# Tue, 29 Mar 2022 08:43:44 GMT
ENV SERVER=
# Tue, 29 Mar 2022 08:43:45 GMT
ENV LISTEN=3333
# Tue, 29 Mar 2022 08:43:46 GMT
ENV OWNER=
# Tue, 29 Mar 2022 08:43:47 GMT
ENV USERFILE=eggdrop.user
# Tue, 29 Mar 2022 08:43:48 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 29 Mar 2022 08:43:49 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 29 Mar 2022 08:43:50 GMT
EXPOSE 3333
# Tue, 29 Mar 2022 08:43:52 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Tue, 29 Mar 2022 08:43:53 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 29 Mar 2022 08:43:53 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 29 Mar 2022 08:43:54 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425a67c2147c2518b3b50438a8d7490f7866e871f0eb779610655a1b089bde1f`  
		Last Modified: Tue, 29 Mar 2022 08:46:49 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc043abf221001c0161e89995789abe1b76005b6060c22f369b6e9c530e41f8`  
		Last Modified: Tue, 29 Mar 2022 08:46:47 GMT  
		Size: 10.7 KB (10682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83de456a90a49bc3b5e97b1c59d545af8c85be9178b0ae791b3da36ebfcb3da9`  
		Last Modified: Tue, 29 Mar 2022 08:46:47 GMT  
		Size: 1.1 MB (1087187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a2b2d1d1dfc653139f172efdea79f3b49ea8d5474feb7534d100891a687a99`  
		Last Modified: Tue, 29 Mar 2022 08:46:52 GMT  
		Size: 36.0 MB (36022359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3dde69589821aa666fa837ac41c1393d1368181edb56005f1bb1d99f204bd5e`  
		Last Modified: Tue, 29 Mar 2022 08:46:47 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0fcaa949de0630a27dda0655eeb28a12857d10fbd1f08737550eddc03d691e`  
		Last Modified: Tue, 29 Mar 2022 08:46:47 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:be7b3b5f1d3ac12c3b479422e403c597966ec37f768a2d163667cba1b27bc9dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:f8959ecd7389c13f0b1c308a92909632723fed1a39a1e7e11be8967b339425dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8284831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a58c228898c4b45bd0873967892fc3c9f1ae67e216a9f6ab5176e530bf3973`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:46 GMT
ADD file:a2ef39a587aac85256b55bee81f17d73aaa7154b2a32a31527c7803fb889f2e7 in / 
# Tue, 29 Mar 2022 00:19:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:02:46 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 29 Mar 2022 12:02:46 GMT
RUN adduser -S eggdrop
# Tue, 29 Mar 2022 12:02:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 29 Mar 2022 12:02:49 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 29 Mar 2022 12:03:43 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 29 Mar 2022 12:03:43 GMT
ENV NICK=
# Tue, 29 Mar 2022 12:03:43 GMT
ENV SERVER=
# Tue, 29 Mar 2022 12:03:43 GMT
ENV LISTEN=3333
# Tue, 29 Mar 2022 12:03:43 GMT
ENV OWNER=
# Tue, 29 Mar 2022 12:03:44 GMT
ENV USERFILE=eggdrop.user
# Tue, 29 Mar 2022 12:03:44 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 29 Mar 2022 12:03:44 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 29 Mar 2022 12:03:44 GMT
EXPOSE 3333
# Tue, 29 Mar 2022 12:03:44 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 29 Mar 2022 12:03:44 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 29 Mar 2022 12:03:44 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 29 Mar 2022 12:03:44 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:b9c05db88786fd3c89b78787631257301391f898c03ba50553b556630046a741`  
		Last Modified: Tue, 29 Mar 2022 00:20:43 GMT  
		Size: 2.8 MB (2819223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9acac2e2c60780abd6b0e25869e85d9deb82a02ef2f59551172c88bea3f177d9`  
		Last Modified: Tue, 29 Mar 2022 12:04:19 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f63481626d334eabf1b3d8276a15c87932fcb09d476ae53aad900606e9dfaa`  
		Last Modified: Tue, 29 Mar 2022 12:04:16 GMT  
		Size: 10.7 KB (10693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc59cd14f7ab318b4cd643b4b21c2a2fbd9de695e06e6e9993f63bb9ef8c68`  
		Last Modified: Tue, 29 Mar 2022 12:04:17 GMT  
		Size: 2.7 MB (2726422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a787fa2eca8d7f7f9edcc027cc642019628754b70edf5bc41912f9246456d4`  
		Last Modified: Tue, 29 Mar 2022 12:04:17 GMT  
		Size: 2.7 MB (2724696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d69605e7aed6ad848eae6a5e270bb2ae5ab6cca147a7efa700bde818cca04ed`  
		Last Modified: Tue, 29 Mar 2022 12:04:16 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26a08d672007b6c13e248a18f5e3040cd0158213c2bebfb278f8a31d27d1c46`  
		Last Modified: Tue, 29 Mar 2022 12:04:16 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:fc709505f111fdbce3c7c2d010174e9ce05f8917cfa672a57bf3d684d12634d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7975684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027e12449683568173ac82fc9233610e76bcb8c122bc209ef6d05936dd92e684`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:56 GMT
ADD file:23d913551f75313e359a4e93592ea0a9655e1a7c2bec5fddd210717d70c3114b in / 
# Tue, 29 Mar 2022 00:49:57 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:35:03 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 29 Mar 2022 12:35:04 GMT
RUN adduser -S eggdrop
# Tue, 29 Mar 2022 12:35:06 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 29 Mar 2022 12:35:10 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 29 Mar 2022 12:37:33 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 29 Mar 2022 12:37:34 GMT
ENV NICK=
# Tue, 29 Mar 2022 12:37:34 GMT
ENV SERVER=
# Tue, 29 Mar 2022 12:37:35 GMT
ENV LISTEN=3333
# Tue, 29 Mar 2022 12:37:35 GMT
ENV OWNER=
# Tue, 29 Mar 2022 12:37:36 GMT
ENV USERFILE=eggdrop.user
# Tue, 29 Mar 2022 12:37:36 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 29 Mar 2022 12:37:37 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 29 Mar 2022 12:37:37 GMT
EXPOSE 3333
# Tue, 29 Mar 2022 12:37:38 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 29 Mar 2022 12:37:38 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 29 Mar 2022 12:37:39 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 29 Mar 2022 12:37:39 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:eba0847afba90891ea7dae672f5dadfa405a822df0bc9c00b9e3328fd5fd889c`  
		Last Modified: Tue, 29 Mar 2022 00:51:57 GMT  
		Size: 2.6 MB (2625139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47719ec1561d1e4862f2f9cfc89f920e35096fe46de845a2419822e784797b84`  
		Last Modified: Tue, 29 Mar 2022 12:38:47 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14771c9c03b4ccdbfd89671866cd4b954b4a1c64ce6357e27969542a72ab472`  
		Last Modified: Tue, 29 Mar 2022 12:38:45 GMT  
		Size: 10.4 KB (10405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78456caeb0d0f3345826024aee28dc462d3f732fca733f8b71bb3b687dab7bdf`  
		Last Modified: Tue, 29 Mar 2022 12:38:47 GMT  
		Size: 2.7 MB (2653026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d776a0092c26f0d42f45f1ccd7b14de0112d2b9e12a61bff28d59a01ba47d5fe`  
		Last Modified: Tue, 29 Mar 2022 12:38:47 GMT  
		Size: 2.7 MB (2683304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7a21c3e26575af12fd2822e1fbd2b11893a84dc339092de4ad09c4783d57fc`  
		Last Modified: Tue, 29 Mar 2022 12:38:46 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1553d7330f4de75064224e4485bf5c8c88cea6ec97e163d38b5fefa281b7680b`  
		Last Modified: Tue, 29 Mar 2022 12:38:45 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:cb0b62e745409481ea5ee7d094a40a023983befbb886255aa6dfd8dd64ff1c38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8206880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07c63ca9a05557355635ba09c2023e3a9c691e795cb5426bd5cf9b563e2fbe9`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:18 GMT
ADD file:3b8e0dac20ca40faf2aaf084b69476a222952f177c0e6ec90804a10c91a51feb in / 
# Tue, 29 Mar 2022 00:40:19 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:44:06 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 29 Mar 2022 08:44:07 GMT
RUN adduser -S eggdrop
# Tue, 29 Mar 2022 08:44:09 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 29 Mar 2022 08:44:11 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 29 Mar 2022 08:46:03 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 29 Mar 2022 08:46:04 GMT
ENV NICK=
# Tue, 29 Mar 2022 08:46:05 GMT
ENV SERVER=
# Tue, 29 Mar 2022 08:46:06 GMT
ENV LISTEN=3333
# Tue, 29 Mar 2022 08:46:07 GMT
ENV OWNER=
# Tue, 29 Mar 2022 08:46:08 GMT
ENV USERFILE=eggdrop.user
# Tue, 29 Mar 2022 08:46:09 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 29 Mar 2022 08:46:10 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 29 Mar 2022 08:46:11 GMT
EXPOSE 3333
# Tue, 29 Mar 2022 08:46:13 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 29 Mar 2022 08:46:14 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 29 Mar 2022 08:46:14 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 29 Mar 2022 08:46:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:4e7dd0becbc2dc968b69cba46c81a25fa500c88a644832ce17a5bb090925fa79`  
		Last Modified: Tue, 29 Mar 2022 00:41:37 GMT  
		Size: 2.7 MB (2720845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d8d6adaf5207ba27bf31cf8a052fd3227ef4bf57d8452bdae7e76abf78d4ab`  
		Last Modified: Tue, 29 Mar 2022 08:47:02 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0165d47b893704dcc5d6335a1073bfed26c1812d90b157b377f53a94a94df2`  
		Last Modified: Tue, 29 Mar 2022 08:47:00 GMT  
		Size: 10.5 KB (10484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eb57b1bdf04b5c6fd98f9075fe9a4136786078efc3f44ee2d8d89ac61ae3a3`  
		Last Modified: Tue, 29 Mar 2022 08:47:00 GMT  
		Size: 2.8 MB (2752095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e210cd6a352f10e15e5ffed220e2da94703f48ddf40639d629212a7d674832bc`  
		Last Modified: Tue, 29 Mar 2022 08:47:00 GMT  
		Size: 2.7 MB (2719683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e04e00273f225bcc569309d326a5b8040cef79755bb337be368e7eb969da9d`  
		Last Modified: Tue, 29 Mar 2022 08:47:00 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0abd5e1dc7453538deb3f86d5f1b45e5df7e988889c7ff574947f3ee22e9023`  
		Last Modified: Tue, 29 Mar 2022 08:47:00 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:be7b3b5f1d3ac12c3b479422e403c597966ec37f768a2d163667cba1b27bc9dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:f8959ecd7389c13f0b1c308a92909632723fed1a39a1e7e11be8967b339425dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8284831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a58c228898c4b45bd0873967892fc3c9f1ae67e216a9f6ab5176e530bf3973`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:46 GMT
ADD file:a2ef39a587aac85256b55bee81f17d73aaa7154b2a32a31527c7803fb889f2e7 in / 
# Tue, 29 Mar 2022 00:19:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:02:46 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 29 Mar 2022 12:02:46 GMT
RUN adduser -S eggdrop
# Tue, 29 Mar 2022 12:02:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 29 Mar 2022 12:02:49 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 29 Mar 2022 12:03:43 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 29 Mar 2022 12:03:43 GMT
ENV NICK=
# Tue, 29 Mar 2022 12:03:43 GMT
ENV SERVER=
# Tue, 29 Mar 2022 12:03:43 GMT
ENV LISTEN=3333
# Tue, 29 Mar 2022 12:03:43 GMT
ENV OWNER=
# Tue, 29 Mar 2022 12:03:44 GMT
ENV USERFILE=eggdrop.user
# Tue, 29 Mar 2022 12:03:44 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 29 Mar 2022 12:03:44 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 29 Mar 2022 12:03:44 GMT
EXPOSE 3333
# Tue, 29 Mar 2022 12:03:44 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 29 Mar 2022 12:03:44 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 29 Mar 2022 12:03:44 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 29 Mar 2022 12:03:44 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:b9c05db88786fd3c89b78787631257301391f898c03ba50553b556630046a741`  
		Last Modified: Tue, 29 Mar 2022 00:20:43 GMT  
		Size: 2.8 MB (2819223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9acac2e2c60780abd6b0e25869e85d9deb82a02ef2f59551172c88bea3f177d9`  
		Last Modified: Tue, 29 Mar 2022 12:04:19 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f63481626d334eabf1b3d8276a15c87932fcb09d476ae53aad900606e9dfaa`  
		Last Modified: Tue, 29 Mar 2022 12:04:16 GMT  
		Size: 10.7 KB (10693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcc59cd14f7ab318b4cd643b4b21c2a2fbd9de695e06e6e9993f63bb9ef8c68`  
		Last Modified: Tue, 29 Mar 2022 12:04:17 GMT  
		Size: 2.7 MB (2726422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a787fa2eca8d7f7f9edcc027cc642019628754b70edf5bc41912f9246456d4`  
		Last Modified: Tue, 29 Mar 2022 12:04:17 GMT  
		Size: 2.7 MB (2724696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d69605e7aed6ad848eae6a5e270bb2ae5ab6cca147a7efa700bde818cca04ed`  
		Last Modified: Tue, 29 Mar 2022 12:04:16 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26a08d672007b6c13e248a18f5e3040cd0158213c2bebfb278f8a31d27d1c46`  
		Last Modified: Tue, 29 Mar 2022 12:04:16 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:fc709505f111fdbce3c7c2d010174e9ce05f8917cfa672a57bf3d684d12634d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7975684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027e12449683568173ac82fc9233610e76bcb8c122bc209ef6d05936dd92e684`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:56 GMT
ADD file:23d913551f75313e359a4e93592ea0a9655e1a7c2bec5fddd210717d70c3114b in / 
# Tue, 29 Mar 2022 00:49:57 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:35:03 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 29 Mar 2022 12:35:04 GMT
RUN adduser -S eggdrop
# Tue, 29 Mar 2022 12:35:06 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 29 Mar 2022 12:35:10 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 29 Mar 2022 12:37:33 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 29 Mar 2022 12:37:34 GMT
ENV NICK=
# Tue, 29 Mar 2022 12:37:34 GMT
ENV SERVER=
# Tue, 29 Mar 2022 12:37:35 GMT
ENV LISTEN=3333
# Tue, 29 Mar 2022 12:37:35 GMT
ENV OWNER=
# Tue, 29 Mar 2022 12:37:36 GMT
ENV USERFILE=eggdrop.user
# Tue, 29 Mar 2022 12:37:36 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 29 Mar 2022 12:37:37 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 29 Mar 2022 12:37:37 GMT
EXPOSE 3333
# Tue, 29 Mar 2022 12:37:38 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 29 Mar 2022 12:37:38 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 29 Mar 2022 12:37:39 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 29 Mar 2022 12:37:39 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:eba0847afba90891ea7dae672f5dadfa405a822df0bc9c00b9e3328fd5fd889c`  
		Last Modified: Tue, 29 Mar 2022 00:51:57 GMT  
		Size: 2.6 MB (2625139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47719ec1561d1e4862f2f9cfc89f920e35096fe46de845a2419822e784797b84`  
		Last Modified: Tue, 29 Mar 2022 12:38:47 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14771c9c03b4ccdbfd89671866cd4b954b4a1c64ce6357e27969542a72ab472`  
		Last Modified: Tue, 29 Mar 2022 12:38:45 GMT  
		Size: 10.4 KB (10405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78456caeb0d0f3345826024aee28dc462d3f732fca733f8b71bb3b687dab7bdf`  
		Last Modified: Tue, 29 Mar 2022 12:38:47 GMT  
		Size: 2.7 MB (2653026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d776a0092c26f0d42f45f1ccd7b14de0112d2b9e12a61bff28d59a01ba47d5fe`  
		Last Modified: Tue, 29 Mar 2022 12:38:47 GMT  
		Size: 2.7 MB (2683304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7a21c3e26575af12fd2822e1fbd2b11893a84dc339092de4ad09c4783d57fc`  
		Last Modified: Tue, 29 Mar 2022 12:38:46 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1553d7330f4de75064224e4485bf5c8c88cea6ec97e163d38b5fefa281b7680b`  
		Last Modified: Tue, 29 Mar 2022 12:38:45 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:cb0b62e745409481ea5ee7d094a40a023983befbb886255aa6dfd8dd64ff1c38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8206880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07c63ca9a05557355635ba09c2023e3a9c691e795cb5426bd5cf9b563e2fbe9`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:18 GMT
ADD file:3b8e0dac20ca40faf2aaf084b69476a222952f177c0e6ec90804a10c91a51feb in / 
# Tue, 29 Mar 2022 00:40:19 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:44:06 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 29 Mar 2022 08:44:07 GMT
RUN adduser -S eggdrop
# Tue, 29 Mar 2022 08:44:09 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 29 Mar 2022 08:44:11 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 29 Mar 2022 08:46:03 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 29 Mar 2022 08:46:04 GMT
ENV NICK=
# Tue, 29 Mar 2022 08:46:05 GMT
ENV SERVER=
# Tue, 29 Mar 2022 08:46:06 GMT
ENV LISTEN=3333
# Tue, 29 Mar 2022 08:46:07 GMT
ENV OWNER=
# Tue, 29 Mar 2022 08:46:08 GMT
ENV USERFILE=eggdrop.user
# Tue, 29 Mar 2022 08:46:09 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 29 Mar 2022 08:46:10 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 29 Mar 2022 08:46:11 GMT
EXPOSE 3333
# Tue, 29 Mar 2022 08:46:13 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 29 Mar 2022 08:46:14 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 29 Mar 2022 08:46:14 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 29 Mar 2022 08:46:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:4e7dd0becbc2dc968b69cba46c81a25fa500c88a644832ce17a5bb090925fa79`  
		Last Modified: Tue, 29 Mar 2022 00:41:37 GMT  
		Size: 2.7 MB (2720845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d8d6adaf5207ba27bf31cf8a052fd3227ef4bf57d8452bdae7e76abf78d4ab`  
		Last Modified: Tue, 29 Mar 2022 08:47:02 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0165d47b893704dcc5d6335a1073bfed26c1812d90b157b377f53a94a94df2`  
		Last Modified: Tue, 29 Mar 2022 08:47:00 GMT  
		Size: 10.5 KB (10484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eb57b1bdf04b5c6fd98f9075fe9a4136786078efc3f44ee2d8d89ac61ae3a3`  
		Last Modified: Tue, 29 Mar 2022 08:47:00 GMT  
		Size: 2.8 MB (2752095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e210cd6a352f10e15e5ffed220e2da94703f48ddf40639d629212a7d674832bc`  
		Last Modified: Tue, 29 Mar 2022 08:47:00 GMT  
		Size: 2.7 MB (2719683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e04e00273f225bcc569309d326a5b8040cef79755bb337be368e7eb969da9d`  
		Last Modified: Tue, 29 Mar 2022 08:47:00 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0abd5e1dc7453538deb3f86d5f1b45e5df7e988889c7ff574947f3ee22e9023`  
		Last Modified: Tue, 29 Mar 2022 08:47:00 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
