<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.9`](#eggdrop19)
-	[`eggdrop:1.9.5`](#eggdrop195)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.9`

```console
$ docker pull eggdrop@sha256:b2b9cb9d518b42eb50ea7e2967dab39a2a56d5d8d3959b29d08ca0dd2219b67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9` - linux; amd64

```console
$ docker pull eggdrop@sha256:02687476be54e5db7a2f1d0148f0709a993091b7cb1db8df30f42309392a819a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8327b8ae1aa1dfccb1cd2d8163783cf913b444a2743d98c2a8777c98b775ab2`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:51:45 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 11 Feb 2023 07:51:46 GMT
RUN adduser -S eggdrop
# Sat, 11 Feb 2023 07:51:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 11 Feb 2023 07:51:48 GMT
RUN apk add --no-cache tcl bash openssl
# Mon, 13 Mar 2023 20:32:44 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 13 Mar 2023 20:32:44 GMT
ENV NICK=
# Mon, 13 Mar 2023 20:32:44 GMT
ENV SERVER=
# Mon, 13 Mar 2023 20:32:44 GMT
ENV LISTEN=3333
# Mon, 13 Mar 2023 20:32:44 GMT
ENV OWNER=
# Mon, 13 Mar 2023 20:32:44 GMT
ENV USERFILE=eggdrop.user
# Mon, 13 Mar 2023 20:32:44 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 13 Mar 2023 20:32:45 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 13 Mar 2023 20:32:45 GMT
EXPOSE 3333
# Mon, 13 Mar 2023 20:32:45 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 13 Mar 2023 20:32:45 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 13 Mar 2023 20:32:45 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 13 Mar 2023 20:32:45 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5929d6c17ae9e3c1785e747f2e1c9a4043d1271b0b4fa46fd3b5d69e688807c3`  
		Last Modified: Sat, 11 Feb 2023 07:56:10 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45534f8d250972e326ebb489c727bd241fe3ff4b1127eb39d1d672b0168cca9e`  
		Last Modified: Sat, 11 Feb 2023 07:56:08 GMT  
		Size: 10.9 KB (10932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c10f44dd07312e4c61cf11012690bfbb08c68a17c2cbd5e4c5bec99e2dcecf`  
		Last Modified: Sat, 11 Feb 2023 07:56:09 GMT  
		Size: 2.8 MB (2757983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f478db3e06ff2527da0c7d1abf834862607b2528acff445545f398d76b951c71`  
		Last Modified: Mon, 13 Mar 2023 20:33:13 GMT  
		Size: 6.1 MB (6147024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd801b0966b76d02345a09662ca6be954735c46303d03234760fefbb1c23e0fa`  
		Last Modified: Mon, 13 Mar 2023 20:33:12 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939b3f6e17c0e95865c3b20e9936556f6a8155b49736657cbbfe7b15fc9061ca`  
		Last Modified: Mon, 13 Mar 2023 20:33:12 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:09f505c393ffb684b29411666a5e77e765def0ec940fc3bfdf72e22642654aff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11364835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100b98ce3c42da7d035d94ea9abd968828c9e76870819676900cce9f8067bcc2`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:11 GMT
ADD file:c5e68ad58a515830d33f20488adffa6af47be2e332543c747b8931cab7444e59 in / 
# Wed, 29 Mar 2023 18:01:11 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:01:33 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 29 Mar 2023 19:01:33 GMT
RUN adduser -S eggdrop
# Wed, 29 Mar 2023 19:01:35 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 29 Mar 2023 19:01:36 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 29 Mar 2023 19:05:52 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 29 Mar 2023 19:05:52 GMT
ENV NICK=
# Wed, 29 Mar 2023 19:05:52 GMT
ENV SERVER=
# Wed, 29 Mar 2023 19:05:53 GMT
ENV LISTEN=3333
# Wed, 29 Mar 2023 19:05:53 GMT
ENV OWNER=
# Wed, 29 Mar 2023 19:05:53 GMT
ENV USERFILE=eggdrop.user
# Wed, 29 Mar 2023 19:05:53 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 29 Mar 2023 19:05:53 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 29 Mar 2023 19:05:53 GMT
EXPOSE 3333
# Wed, 29 Mar 2023 19:05:53 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 29 Mar 2023 19:05:53 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 29 Mar 2023 19:05:53 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 29 Mar 2023 19:05:53 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:c4ddbcc13e08e4ef30f810d8afad41fd6994bd8af7d37746d0ea33d8813968fc`  
		Last Modified: Wed, 29 Mar 2023 18:02:04 GMT  
		Size: 2.6 MB (2616846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d988c30b1bf105d6ce44505e097700f9503b8356db5d672c301501624c899658`  
		Last Modified: Wed, 29 Mar 2023 19:06:12 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5039a0196f82b73a0e0a65dcd779912da44a3a913894ac8432d52e105e1a85ab`  
		Last Modified: Wed, 29 Mar 2023 19:06:10 GMT  
		Size: 10.6 KB (10629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab88bbe9cd5465e6642f8e933b2933ec41511b0d257bc1f600d234214d150380`  
		Last Modified: Wed, 29 Mar 2023 19:06:14 GMT  
		Size: 2.7 MB (2679903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e071f86355c7c49f44cb4ef30f52b9ed29b25445bc12e8b31f00d735df4424bd`  
		Last Modified: Wed, 29 Mar 2023 19:06:11 GMT  
		Size: 6.1 MB (6053645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51930a8a6c57659f2214203f9bfdd1ca4790b56611c6955b3f07a251cc6be341`  
		Last Modified: Wed, 29 Mar 2023 19:06:10 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c23e3a8524a1e6240c31862047117a05df8f6c8e198822058c1d1c06687755f`  
		Last Modified: Wed, 29 Mar 2023 19:06:10 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:087798748e578aa2f07a9c8c0b984eaf308e03d9974d9ecefdf02c1ad4359344
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11687192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331e0178aa41967ad6c64d6eea6323083ac3c88c4fe617fd54851779ac8095f2`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:20 GMT
ADD file:a6a2f69b60d7d27bc6e2b9b7e9910dabdc3f5e3702c2345d26a7dc8c603ae595 in / 
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 18:02:16 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 29 Mar 2023 18:02:16 GMT
RUN adduser -S eggdrop
# Wed, 29 Mar 2023 18:02:17 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 29 Mar 2023 18:02:18 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 29 Mar 2023 18:06:03 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 29 Mar 2023 18:06:03 GMT
ENV NICK=
# Wed, 29 Mar 2023 18:06:03 GMT
ENV SERVER=
# Wed, 29 Mar 2023 18:06:04 GMT
ENV LISTEN=3333
# Wed, 29 Mar 2023 18:06:04 GMT
ENV OWNER=
# Wed, 29 Mar 2023 18:06:04 GMT
ENV USERFILE=eggdrop.user
# Wed, 29 Mar 2023 18:06:04 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 29 Mar 2023 18:06:04 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 29 Mar 2023 18:06:04 GMT
EXPOSE 3333
# Wed, 29 Mar 2023 18:06:04 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 29 Mar 2023 18:06:04 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 29 Mar 2023 18:06:04 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 29 Mar 2023 18:06:04 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:547446be3368f442c50ff95e2a2a9c85110b6b41bbb3c75b7e5ebb115f478b57`  
		Last Modified: Wed, 29 Mar 2023 17:39:56 GMT  
		Size: 2.7 MB (2709344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb69f3db113b0619a9372f4b7b70feb8f15fe4aa13ba9e5fa4a024ea95731f4c`  
		Last Modified: Wed, 29 Mar 2023 18:06:25 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e598031e523f6acd4c42bf753c34116e6204220d4a61ec11e62b13fb7f138160`  
		Last Modified: Wed, 29 Mar 2023 18:06:28 GMT  
		Size: 10.7 KB (10746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f2b000939306d443c2a1f2bffb5e73dbc192f7683d7b87fd89c2faedf32046`  
		Last Modified: Wed, 29 Mar 2023 18:06:24 GMT  
		Size: 2.8 MB (2776454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f270999340f5f5c78ba08b9cb807914c368554f21ed9bd0aba266124beb2d1`  
		Last Modified: Wed, 29 Mar 2023 18:06:24 GMT  
		Size: 6.2 MB (6186844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1940fe90811d6ce6c64f3eef4eb3b53d915db33644179d48f1b8e71b8ebe4f`  
		Last Modified: Wed, 29 Mar 2023 18:06:23 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c313b4dd4c0ec3851eb42e4665a8400813ddd7d0073c923616846cb98ca2982`  
		Last Modified: Wed, 29 Mar 2023 18:06:23 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.9.5`

```console
$ docker pull eggdrop@sha256:b2b9cb9d518b42eb50ea7e2967dab39a2a56d5d8d3959b29d08ca0dd2219b67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9.5` - linux; amd64

```console
$ docker pull eggdrop@sha256:02687476be54e5db7a2f1d0148f0709a993091b7cb1db8df30f42309392a819a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8327b8ae1aa1dfccb1cd2d8163783cf913b444a2743d98c2a8777c98b775ab2`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:51:45 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 11 Feb 2023 07:51:46 GMT
RUN adduser -S eggdrop
# Sat, 11 Feb 2023 07:51:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 11 Feb 2023 07:51:48 GMT
RUN apk add --no-cache tcl bash openssl
# Mon, 13 Mar 2023 20:32:44 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 13 Mar 2023 20:32:44 GMT
ENV NICK=
# Mon, 13 Mar 2023 20:32:44 GMT
ENV SERVER=
# Mon, 13 Mar 2023 20:32:44 GMT
ENV LISTEN=3333
# Mon, 13 Mar 2023 20:32:44 GMT
ENV OWNER=
# Mon, 13 Mar 2023 20:32:44 GMT
ENV USERFILE=eggdrop.user
# Mon, 13 Mar 2023 20:32:44 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 13 Mar 2023 20:32:45 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 13 Mar 2023 20:32:45 GMT
EXPOSE 3333
# Mon, 13 Mar 2023 20:32:45 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 13 Mar 2023 20:32:45 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 13 Mar 2023 20:32:45 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 13 Mar 2023 20:32:45 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5929d6c17ae9e3c1785e747f2e1c9a4043d1271b0b4fa46fd3b5d69e688807c3`  
		Last Modified: Sat, 11 Feb 2023 07:56:10 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45534f8d250972e326ebb489c727bd241fe3ff4b1127eb39d1d672b0168cca9e`  
		Last Modified: Sat, 11 Feb 2023 07:56:08 GMT  
		Size: 10.9 KB (10932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c10f44dd07312e4c61cf11012690bfbb08c68a17c2cbd5e4c5bec99e2dcecf`  
		Last Modified: Sat, 11 Feb 2023 07:56:09 GMT  
		Size: 2.8 MB (2757983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f478db3e06ff2527da0c7d1abf834862607b2528acff445545f398d76b951c71`  
		Last Modified: Mon, 13 Mar 2023 20:33:13 GMT  
		Size: 6.1 MB (6147024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd801b0966b76d02345a09662ca6be954735c46303d03234760fefbb1c23e0fa`  
		Last Modified: Mon, 13 Mar 2023 20:33:12 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939b3f6e17c0e95865c3b20e9936556f6a8155b49736657cbbfe7b15fc9061ca`  
		Last Modified: Mon, 13 Mar 2023 20:33:12 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.5` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:09f505c393ffb684b29411666a5e77e765def0ec940fc3bfdf72e22642654aff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11364835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100b98ce3c42da7d035d94ea9abd968828c9e76870819676900cce9f8067bcc2`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:11 GMT
ADD file:c5e68ad58a515830d33f20488adffa6af47be2e332543c747b8931cab7444e59 in / 
# Wed, 29 Mar 2023 18:01:11 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:01:33 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 29 Mar 2023 19:01:33 GMT
RUN adduser -S eggdrop
# Wed, 29 Mar 2023 19:01:35 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 29 Mar 2023 19:01:36 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 29 Mar 2023 19:05:52 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 29 Mar 2023 19:05:52 GMT
ENV NICK=
# Wed, 29 Mar 2023 19:05:52 GMT
ENV SERVER=
# Wed, 29 Mar 2023 19:05:53 GMT
ENV LISTEN=3333
# Wed, 29 Mar 2023 19:05:53 GMT
ENV OWNER=
# Wed, 29 Mar 2023 19:05:53 GMT
ENV USERFILE=eggdrop.user
# Wed, 29 Mar 2023 19:05:53 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 29 Mar 2023 19:05:53 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 29 Mar 2023 19:05:53 GMT
EXPOSE 3333
# Wed, 29 Mar 2023 19:05:53 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 29 Mar 2023 19:05:53 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 29 Mar 2023 19:05:53 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 29 Mar 2023 19:05:53 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:c4ddbcc13e08e4ef30f810d8afad41fd6994bd8af7d37746d0ea33d8813968fc`  
		Last Modified: Wed, 29 Mar 2023 18:02:04 GMT  
		Size: 2.6 MB (2616846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d988c30b1bf105d6ce44505e097700f9503b8356db5d672c301501624c899658`  
		Last Modified: Wed, 29 Mar 2023 19:06:12 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5039a0196f82b73a0e0a65dcd779912da44a3a913894ac8432d52e105e1a85ab`  
		Last Modified: Wed, 29 Mar 2023 19:06:10 GMT  
		Size: 10.6 KB (10629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab88bbe9cd5465e6642f8e933b2933ec41511b0d257bc1f600d234214d150380`  
		Last Modified: Wed, 29 Mar 2023 19:06:14 GMT  
		Size: 2.7 MB (2679903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e071f86355c7c49f44cb4ef30f52b9ed29b25445bc12e8b31f00d735df4424bd`  
		Last Modified: Wed, 29 Mar 2023 19:06:11 GMT  
		Size: 6.1 MB (6053645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51930a8a6c57659f2214203f9bfdd1ca4790b56611c6955b3f07a251cc6be341`  
		Last Modified: Wed, 29 Mar 2023 19:06:10 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c23e3a8524a1e6240c31862047117a05df8f6c8e198822058c1d1c06687755f`  
		Last Modified: Wed, 29 Mar 2023 19:06:10 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.5` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:087798748e578aa2f07a9c8c0b984eaf308e03d9974d9ecefdf02c1ad4359344
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11687192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331e0178aa41967ad6c64d6eea6323083ac3c88c4fe617fd54851779ac8095f2`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:20 GMT
ADD file:a6a2f69b60d7d27bc6e2b9b7e9910dabdc3f5e3702c2345d26a7dc8c603ae595 in / 
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 18:02:16 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 29 Mar 2023 18:02:16 GMT
RUN adduser -S eggdrop
# Wed, 29 Mar 2023 18:02:17 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 29 Mar 2023 18:02:18 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 29 Mar 2023 18:06:03 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 29 Mar 2023 18:06:03 GMT
ENV NICK=
# Wed, 29 Mar 2023 18:06:03 GMT
ENV SERVER=
# Wed, 29 Mar 2023 18:06:04 GMT
ENV LISTEN=3333
# Wed, 29 Mar 2023 18:06:04 GMT
ENV OWNER=
# Wed, 29 Mar 2023 18:06:04 GMT
ENV USERFILE=eggdrop.user
# Wed, 29 Mar 2023 18:06:04 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 29 Mar 2023 18:06:04 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 29 Mar 2023 18:06:04 GMT
EXPOSE 3333
# Wed, 29 Mar 2023 18:06:04 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 29 Mar 2023 18:06:04 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 29 Mar 2023 18:06:04 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 29 Mar 2023 18:06:04 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:547446be3368f442c50ff95e2a2a9c85110b6b41bbb3c75b7e5ebb115f478b57`  
		Last Modified: Wed, 29 Mar 2023 17:39:56 GMT  
		Size: 2.7 MB (2709344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb69f3db113b0619a9372f4b7b70feb8f15fe4aa13ba9e5fa4a024ea95731f4c`  
		Last Modified: Wed, 29 Mar 2023 18:06:25 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e598031e523f6acd4c42bf753c34116e6204220d4a61ec11e62b13fb7f138160`  
		Last Modified: Wed, 29 Mar 2023 18:06:28 GMT  
		Size: 10.7 KB (10746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f2b000939306d443c2a1f2bffb5e73dbc192f7683d7b87fd89c2faedf32046`  
		Last Modified: Wed, 29 Mar 2023 18:06:24 GMT  
		Size: 2.8 MB (2776454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f270999340f5f5c78ba08b9cb807914c368554f21ed9bd0aba266124beb2d1`  
		Last Modified: Wed, 29 Mar 2023 18:06:24 GMT  
		Size: 6.2 MB (6186844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1940fe90811d6ce6c64f3eef4eb3b53d915db33644179d48f1b8e71b8ebe4f`  
		Last Modified: Wed, 29 Mar 2023 18:06:23 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c313b4dd4c0ec3851eb42e4665a8400813ddd7d0073c923616846cb98ca2982`  
		Last Modified: Wed, 29 Mar 2023 18:06:23 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:375e9dc41561dfe792ee64f691e71e9463d0fa83051249f2957765565c45cf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:f4dda8dbfc8340afdb126c0060918804fce7479c781fea005f3bb8cb90a3e086
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16124763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae7b6f7479c5d54b5d4f907ec43ab5feb20c95f593915f87378b72b94a6efd4`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 20:24:51 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 13 Mar 2023 20:24:52 GMT
RUN adduser -S eggdrop
# Mon, 13 Mar 2023 20:24:53 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 13 Mar 2023 20:24:53 GMT
ENV EGGDROP_SHA256=cc7936ee427959081651319119ac0b8f3581a18d7be7b20f71023954f1f69a91
# Mon, 13 Mar 2023 20:24:53 GMT
ENV EGGDROP_COMMIT=26ecf0921ee84c5bf61cb31014a75f02670b1af4
# Mon, 13 Mar 2023 20:24:54 GMT
RUN apk --update add --no-cache bash openssl
# Mon, 13 Mar 2023 20:28:32 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 13 Mar 2023 20:28:32 GMT
ENV NICK=
# Mon, 13 Mar 2023 20:28:32 GMT
ENV SERVER=
# Mon, 13 Mar 2023 20:28:32 GMT
ENV LISTEN=3333
# Mon, 13 Mar 2023 20:28:33 GMT
ENV OWNER=
# Mon, 13 Mar 2023 20:28:33 GMT
ENV USERFILE=eggdrop.user
# Mon, 13 Mar 2023 20:28:33 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 13 Mar 2023 20:28:33 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 13 Mar 2023 20:28:33 GMT
EXPOSE 3333
# Mon, 13 Mar 2023 20:28:33 GMT
COPY file:35e05bb72116a1848ec779e3fbc4ea6bbcd95ceb11059751f608c8543e18cde7 in /home/eggdrop/eggdrop 
# Mon, 13 Mar 2023 20:28:33 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 13 Mar 2023 20:28:33 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 13 Mar 2023 20:28:33 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9266924772c11264278e8f7e9f3f47dcee1457bf7675615f5ea055188cf85f16`  
		Last Modified: Mon, 13 Mar 2023 20:33:03 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1250f5956177bcd3a38a3665961d74a6441095a6631b42607cb3b1bdc8e53cd`  
		Last Modified: Mon, 13 Mar 2023 20:33:01 GMT  
		Size: 11.0 KB (10987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f57101f337e18f728b8805f2c9c720b9eb2e51fcae646a64f79663025dc1146`  
		Last Modified: Mon, 13 Mar 2023 20:33:01 GMT  
		Size: 1.2 MB (1202022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cf3036a96c935256f63d8ddbd5c7f3ac6921566cef6753c6f06a3957765df1`  
		Last Modified: Mon, 13 Mar 2023 20:33:03 GMT  
		Size: 11.5 MB (11533076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc935cd2576555a7689ece02bcf0866b3f420389146b7f0db863abd0f5c87733`  
		Last Modified: Mon, 13 Mar 2023 20:33:01 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b2faffd8eedb0ba89d3d156d65a9712e4d488f2997630d6207476b6f075b38`  
		Last Modified: Mon, 13 Mar 2023 20:33:01 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:bc1143e737ab11d97f8021d27ba52c0e7dc25edf63a18b987f332acffc909c04
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15724291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d6bb195481c276efedaefc674e6331ae6877f727fa8c2ff0680ea7a0b7cdb3`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:09 GMT
ADD file:2dd294d20c0b500c8fed6b410b059429b36f51cd48a45eaf7a06ecbef9e2a3bb in / 
# Wed, 29 Mar 2023 18:01:09 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 18:56:59 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 29 Mar 2023 18:56:59 GMT
RUN adduser -S eggdrop
# Wed, 29 Mar 2023 18:57:00 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 29 Mar 2023 18:57:00 GMT
ENV EGGDROP_SHA256=cc7936ee427959081651319119ac0b8f3581a18d7be7b20f71023954f1f69a91
# Wed, 29 Mar 2023 18:57:00 GMT
ENV EGGDROP_COMMIT=26ecf0921ee84c5bf61cb31014a75f02670b1af4
# Wed, 29 Mar 2023 18:57:01 GMT
RUN apk --update add --no-cache bash openssl
# Wed, 29 Mar 2023 19:00:48 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 29 Mar 2023 19:00:49 GMT
ENV NICK=
# Wed, 29 Mar 2023 19:00:49 GMT
ENV SERVER=
# Wed, 29 Mar 2023 19:00:49 GMT
ENV LISTEN=3333
# Wed, 29 Mar 2023 19:00:49 GMT
ENV OWNER=
# Wed, 29 Mar 2023 19:00:49 GMT
ENV USERFILE=eggdrop.user
# Wed, 29 Mar 2023 19:00:49 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 29 Mar 2023 19:00:49 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 29 Mar 2023 19:00:49 GMT
EXPOSE 3333
# Wed, 29 Mar 2023 19:00:49 GMT
COPY file:35e05bb72116a1848ec779e3fbc4ea6bbcd95ceb11059751f608c8543e18cde7 in /home/eggdrop/eggdrop 
# Wed, 29 Mar 2023 19:00:49 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 29 Mar 2023 19:00:50 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 29 Mar 2023 19:00:50 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:75257e753735e4ff78fae2d44018022a6ac775290e02103713a70699ece7576e`  
		Last Modified: Wed, 29 Mar 2023 18:01:52 GMT  
		Size: 3.1 MB (3110802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb407c07d8a80384801109a46ef34303ea1639b89a3446233b33540b8e7fc22`  
		Last Modified: Wed, 29 Mar 2023 19:06:04 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410bfa5264cde2e4591afc9b76e9745b6aef7cf80955d901ef465a0c49852283`  
		Last Modified: Wed, 29 Mar 2023 19:06:02 GMT  
		Size: 11.1 KB (11125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787c620316ea18689bb4c924a98b9c71ed30fc44ce20a7f6d643b7408e6b5ff`  
		Last Modified: Wed, 29 Mar 2023 19:06:03 GMT  
		Size: 1.2 MB (1186209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbe0b9f9815dc70a838fc7afa04cdf2a2062a60cab93a094d780e7e819a7f8c`  
		Last Modified: Wed, 29 Mar 2023 19:06:05 GMT  
		Size: 11.4 MB (11411921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e4c3ec47877d7d80c8d5ba75986cb7526aecf878f02c0428b5ad86ac641726`  
		Last Modified: Wed, 29 Mar 2023 19:06:02 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4b8dfd93af9b0ea0c4122a88da0ad5fe6482c3ddd20bb63d37b26ade81ef8f`  
		Last Modified: Wed, 29 Mar 2023 19:06:03 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:02145b19b355da6bcb8d539238912b65ef4f4a01b951b517d35e46a28870fa83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16105068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13cb4c99c02b85a5b5e2c27e6801a193c19803d1da9747a1e1936f5df194fbe4`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:18 GMT
ADD file:e51d4089e73ad6dee52b31f0c8059a00c17df6e23f6741fe11b43bd84cc99008 in / 
# Wed, 29 Mar 2023 17:39:18 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 17:58:38 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 29 Mar 2023 17:58:39 GMT
RUN adduser -S eggdrop
# Wed, 29 Mar 2023 17:58:40 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 29 Mar 2023 17:58:40 GMT
ENV EGGDROP_SHA256=cc7936ee427959081651319119ac0b8f3581a18d7be7b20f71023954f1f69a91
# Wed, 29 Mar 2023 17:58:40 GMT
ENV EGGDROP_COMMIT=26ecf0921ee84c5bf61cb31014a75f02670b1af4
# Wed, 29 Mar 2023 17:58:41 GMT
RUN apk --update add --no-cache bash openssl
# Wed, 29 Mar 2023 18:02:00 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 29 Mar 2023 18:02:00 GMT
ENV NICK=
# Wed, 29 Mar 2023 18:02:00 GMT
ENV SERVER=
# Wed, 29 Mar 2023 18:02:00 GMT
ENV LISTEN=3333
# Wed, 29 Mar 2023 18:02:00 GMT
ENV OWNER=
# Wed, 29 Mar 2023 18:02:00 GMT
ENV USERFILE=eggdrop.user
# Wed, 29 Mar 2023 18:02:01 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 29 Mar 2023 18:02:01 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 29 Mar 2023 18:02:01 GMT
EXPOSE 3333
# Wed, 29 Mar 2023 18:02:01 GMT
COPY file:35e05bb72116a1848ec779e3fbc4ea6bbcd95ceb11059751f608c8543e18cde7 in /home/eggdrop/eggdrop 
# Wed, 29 Mar 2023 18:02:01 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 29 Mar 2023 18:02:01 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 29 Mar 2023 18:02:01 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:c41833b44d910632b415cd89a9cdaa4d62c9725dc56c99a7ddadafd6719960f9`  
		Last Modified: Wed, 29 Mar 2023 17:39:44 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91c2b5610b0ebf373765106488fc16d0eec5c20a499e88b30becdb08a9f9903`  
		Last Modified: Wed, 29 Mar 2023 18:06:17 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19ac67c8f11f17dc932ce797b534c6c348492ac2cbc8163ef410ecad15d3628`  
		Last Modified: Wed, 29 Mar 2023 18:06:16 GMT  
		Size: 11.2 KB (11184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473234a20c062f1e3b88a9cb43d551f41abf7f74a8da1e4fd7fb651f64430d82`  
		Last Modified: Wed, 29 Mar 2023 18:06:16 GMT  
		Size: 1.2 MB (1233181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3409786ba6676e4df657c0e9905cfbee6aeef0b9a035a348b451c9c87f29315e`  
		Last Modified: Wed, 29 Mar 2023 18:06:17 GMT  
		Size: 11.6 MB (11594624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9dcac42c924e970223b2dcccab46a8e2a2d918d55a704ad4bbb73a8591e7f05`  
		Last Modified: Wed, 29 Mar 2023 18:06:15 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3615e205be5683b484cb4927e849a95683d5f4e92040bdc1805b5dc881620d`  
		Last Modified: Wed, 29 Mar 2023 18:06:15 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:b2b9cb9d518b42eb50ea7e2967dab39a2a56d5d8d3959b29d08ca0dd2219b67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:02687476be54e5db7a2f1d0148f0709a993091b7cb1db8df30f42309392a819a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8327b8ae1aa1dfccb1cd2d8163783cf913b444a2743d98c2a8777c98b775ab2`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:51:45 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 11 Feb 2023 07:51:46 GMT
RUN adduser -S eggdrop
# Sat, 11 Feb 2023 07:51:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 11 Feb 2023 07:51:48 GMT
RUN apk add --no-cache tcl bash openssl
# Mon, 13 Mar 2023 20:32:44 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 13 Mar 2023 20:32:44 GMT
ENV NICK=
# Mon, 13 Mar 2023 20:32:44 GMT
ENV SERVER=
# Mon, 13 Mar 2023 20:32:44 GMT
ENV LISTEN=3333
# Mon, 13 Mar 2023 20:32:44 GMT
ENV OWNER=
# Mon, 13 Mar 2023 20:32:44 GMT
ENV USERFILE=eggdrop.user
# Mon, 13 Mar 2023 20:32:44 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 13 Mar 2023 20:32:45 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 13 Mar 2023 20:32:45 GMT
EXPOSE 3333
# Mon, 13 Mar 2023 20:32:45 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 13 Mar 2023 20:32:45 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 13 Mar 2023 20:32:45 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 13 Mar 2023 20:32:45 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5929d6c17ae9e3c1785e747f2e1c9a4043d1271b0b4fa46fd3b5d69e688807c3`  
		Last Modified: Sat, 11 Feb 2023 07:56:10 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45534f8d250972e326ebb489c727bd241fe3ff4b1127eb39d1d672b0168cca9e`  
		Last Modified: Sat, 11 Feb 2023 07:56:08 GMT  
		Size: 10.9 KB (10932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c10f44dd07312e4c61cf11012690bfbb08c68a17c2cbd5e4c5bec99e2dcecf`  
		Last Modified: Sat, 11 Feb 2023 07:56:09 GMT  
		Size: 2.8 MB (2757983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f478db3e06ff2527da0c7d1abf834862607b2528acff445545f398d76b951c71`  
		Last Modified: Mon, 13 Mar 2023 20:33:13 GMT  
		Size: 6.1 MB (6147024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd801b0966b76d02345a09662ca6be954735c46303d03234760fefbb1c23e0fa`  
		Last Modified: Mon, 13 Mar 2023 20:33:12 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939b3f6e17c0e95865c3b20e9936556f6a8155b49736657cbbfe7b15fc9061ca`  
		Last Modified: Mon, 13 Mar 2023 20:33:12 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:09f505c393ffb684b29411666a5e77e765def0ec940fc3bfdf72e22642654aff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11364835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100b98ce3c42da7d035d94ea9abd968828c9e76870819676900cce9f8067bcc2`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:11 GMT
ADD file:c5e68ad58a515830d33f20488adffa6af47be2e332543c747b8931cab7444e59 in / 
# Wed, 29 Mar 2023 18:01:11 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:01:33 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 29 Mar 2023 19:01:33 GMT
RUN adduser -S eggdrop
# Wed, 29 Mar 2023 19:01:35 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 29 Mar 2023 19:01:36 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 29 Mar 2023 19:05:52 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 29 Mar 2023 19:05:52 GMT
ENV NICK=
# Wed, 29 Mar 2023 19:05:52 GMT
ENV SERVER=
# Wed, 29 Mar 2023 19:05:53 GMT
ENV LISTEN=3333
# Wed, 29 Mar 2023 19:05:53 GMT
ENV OWNER=
# Wed, 29 Mar 2023 19:05:53 GMT
ENV USERFILE=eggdrop.user
# Wed, 29 Mar 2023 19:05:53 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 29 Mar 2023 19:05:53 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 29 Mar 2023 19:05:53 GMT
EXPOSE 3333
# Wed, 29 Mar 2023 19:05:53 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 29 Mar 2023 19:05:53 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 29 Mar 2023 19:05:53 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 29 Mar 2023 19:05:53 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:c4ddbcc13e08e4ef30f810d8afad41fd6994bd8af7d37746d0ea33d8813968fc`  
		Last Modified: Wed, 29 Mar 2023 18:02:04 GMT  
		Size: 2.6 MB (2616846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d988c30b1bf105d6ce44505e097700f9503b8356db5d672c301501624c899658`  
		Last Modified: Wed, 29 Mar 2023 19:06:12 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5039a0196f82b73a0e0a65dcd779912da44a3a913894ac8432d52e105e1a85ab`  
		Last Modified: Wed, 29 Mar 2023 19:06:10 GMT  
		Size: 10.6 KB (10629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab88bbe9cd5465e6642f8e933b2933ec41511b0d257bc1f600d234214d150380`  
		Last Modified: Wed, 29 Mar 2023 19:06:14 GMT  
		Size: 2.7 MB (2679903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e071f86355c7c49f44cb4ef30f52b9ed29b25445bc12e8b31f00d735df4424bd`  
		Last Modified: Wed, 29 Mar 2023 19:06:11 GMT  
		Size: 6.1 MB (6053645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51930a8a6c57659f2214203f9bfdd1ca4790b56611c6955b3f07a251cc6be341`  
		Last Modified: Wed, 29 Mar 2023 19:06:10 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c23e3a8524a1e6240c31862047117a05df8f6c8e198822058c1d1c06687755f`  
		Last Modified: Wed, 29 Mar 2023 19:06:10 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:087798748e578aa2f07a9c8c0b984eaf308e03d9974d9ecefdf02c1ad4359344
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11687192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331e0178aa41967ad6c64d6eea6323083ac3c88c4fe617fd54851779ac8095f2`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:20 GMT
ADD file:a6a2f69b60d7d27bc6e2b9b7e9910dabdc3f5e3702c2345d26a7dc8c603ae595 in / 
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 18:02:16 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 29 Mar 2023 18:02:16 GMT
RUN adduser -S eggdrop
# Wed, 29 Mar 2023 18:02:17 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 29 Mar 2023 18:02:18 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 29 Mar 2023 18:06:03 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 29 Mar 2023 18:06:03 GMT
ENV NICK=
# Wed, 29 Mar 2023 18:06:03 GMT
ENV SERVER=
# Wed, 29 Mar 2023 18:06:04 GMT
ENV LISTEN=3333
# Wed, 29 Mar 2023 18:06:04 GMT
ENV OWNER=
# Wed, 29 Mar 2023 18:06:04 GMT
ENV USERFILE=eggdrop.user
# Wed, 29 Mar 2023 18:06:04 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 29 Mar 2023 18:06:04 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 29 Mar 2023 18:06:04 GMT
EXPOSE 3333
# Wed, 29 Mar 2023 18:06:04 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 29 Mar 2023 18:06:04 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 29 Mar 2023 18:06:04 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 29 Mar 2023 18:06:04 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:547446be3368f442c50ff95e2a2a9c85110b6b41bbb3c75b7e5ebb115f478b57`  
		Last Modified: Wed, 29 Mar 2023 17:39:56 GMT  
		Size: 2.7 MB (2709344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb69f3db113b0619a9372f4b7b70feb8f15fe4aa13ba9e5fa4a024ea95731f4c`  
		Last Modified: Wed, 29 Mar 2023 18:06:25 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e598031e523f6acd4c42bf753c34116e6204220d4a61ec11e62b13fb7f138160`  
		Last Modified: Wed, 29 Mar 2023 18:06:28 GMT  
		Size: 10.7 KB (10746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f2b000939306d443c2a1f2bffb5e73dbc192f7683d7b87fd89c2faedf32046`  
		Last Modified: Wed, 29 Mar 2023 18:06:24 GMT  
		Size: 2.8 MB (2776454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f270999340f5f5c78ba08b9cb807914c368554f21ed9bd0aba266124beb2d1`  
		Last Modified: Wed, 29 Mar 2023 18:06:24 GMT  
		Size: 6.2 MB (6186844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1940fe90811d6ce6c64f3eef4eb3b53d915db33644179d48f1b8e71b8ebe4f`  
		Last Modified: Wed, 29 Mar 2023 18:06:23 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c313b4dd4c0ec3851eb42e4665a8400813ddd7d0073c923616846cb98ca2982`  
		Last Modified: Wed, 29 Mar 2023 18:06:23 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:b2b9cb9d518b42eb50ea7e2967dab39a2a56d5d8d3959b29d08ca0dd2219b67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:02687476be54e5db7a2f1d0148f0709a993091b7cb1db8df30f42309392a819a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8327b8ae1aa1dfccb1cd2d8163783cf913b444a2743d98c2a8777c98b775ab2`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:51:45 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 11 Feb 2023 07:51:46 GMT
RUN adduser -S eggdrop
# Sat, 11 Feb 2023 07:51:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 11 Feb 2023 07:51:48 GMT
RUN apk add --no-cache tcl bash openssl
# Mon, 13 Mar 2023 20:32:44 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 13 Mar 2023 20:32:44 GMT
ENV NICK=
# Mon, 13 Mar 2023 20:32:44 GMT
ENV SERVER=
# Mon, 13 Mar 2023 20:32:44 GMT
ENV LISTEN=3333
# Mon, 13 Mar 2023 20:32:44 GMT
ENV OWNER=
# Mon, 13 Mar 2023 20:32:44 GMT
ENV USERFILE=eggdrop.user
# Mon, 13 Mar 2023 20:32:44 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 13 Mar 2023 20:32:45 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 13 Mar 2023 20:32:45 GMT
EXPOSE 3333
# Mon, 13 Mar 2023 20:32:45 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 13 Mar 2023 20:32:45 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 13 Mar 2023 20:32:45 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 13 Mar 2023 20:32:45 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5929d6c17ae9e3c1785e747f2e1c9a4043d1271b0b4fa46fd3b5d69e688807c3`  
		Last Modified: Sat, 11 Feb 2023 07:56:10 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45534f8d250972e326ebb489c727bd241fe3ff4b1127eb39d1d672b0168cca9e`  
		Last Modified: Sat, 11 Feb 2023 07:56:08 GMT  
		Size: 10.9 KB (10932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c10f44dd07312e4c61cf11012690bfbb08c68a17c2cbd5e4c5bec99e2dcecf`  
		Last Modified: Sat, 11 Feb 2023 07:56:09 GMT  
		Size: 2.8 MB (2757983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f478db3e06ff2527da0c7d1abf834862607b2528acff445545f398d76b951c71`  
		Last Modified: Mon, 13 Mar 2023 20:33:13 GMT  
		Size: 6.1 MB (6147024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd801b0966b76d02345a09662ca6be954735c46303d03234760fefbb1c23e0fa`  
		Last Modified: Mon, 13 Mar 2023 20:33:12 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939b3f6e17c0e95865c3b20e9936556f6a8155b49736657cbbfe7b15fc9061ca`  
		Last Modified: Mon, 13 Mar 2023 20:33:12 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:09f505c393ffb684b29411666a5e77e765def0ec940fc3bfdf72e22642654aff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11364835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100b98ce3c42da7d035d94ea9abd968828c9e76870819676900cce9f8067bcc2`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:11 GMT
ADD file:c5e68ad58a515830d33f20488adffa6af47be2e332543c747b8931cab7444e59 in / 
# Wed, 29 Mar 2023 18:01:11 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:01:33 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 29 Mar 2023 19:01:33 GMT
RUN adduser -S eggdrop
# Wed, 29 Mar 2023 19:01:35 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 29 Mar 2023 19:01:36 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 29 Mar 2023 19:05:52 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 29 Mar 2023 19:05:52 GMT
ENV NICK=
# Wed, 29 Mar 2023 19:05:52 GMT
ENV SERVER=
# Wed, 29 Mar 2023 19:05:53 GMT
ENV LISTEN=3333
# Wed, 29 Mar 2023 19:05:53 GMT
ENV OWNER=
# Wed, 29 Mar 2023 19:05:53 GMT
ENV USERFILE=eggdrop.user
# Wed, 29 Mar 2023 19:05:53 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 29 Mar 2023 19:05:53 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 29 Mar 2023 19:05:53 GMT
EXPOSE 3333
# Wed, 29 Mar 2023 19:05:53 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 29 Mar 2023 19:05:53 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 29 Mar 2023 19:05:53 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 29 Mar 2023 19:05:53 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:c4ddbcc13e08e4ef30f810d8afad41fd6994bd8af7d37746d0ea33d8813968fc`  
		Last Modified: Wed, 29 Mar 2023 18:02:04 GMT  
		Size: 2.6 MB (2616846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d988c30b1bf105d6ce44505e097700f9503b8356db5d672c301501624c899658`  
		Last Modified: Wed, 29 Mar 2023 19:06:12 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5039a0196f82b73a0e0a65dcd779912da44a3a913894ac8432d52e105e1a85ab`  
		Last Modified: Wed, 29 Mar 2023 19:06:10 GMT  
		Size: 10.6 KB (10629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab88bbe9cd5465e6642f8e933b2933ec41511b0d257bc1f600d234214d150380`  
		Last Modified: Wed, 29 Mar 2023 19:06:14 GMT  
		Size: 2.7 MB (2679903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e071f86355c7c49f44cb4ef30f52b9ed29b25445bc12e8b31f00d735df4424bd`  
		Last Modified: Wed, 29 Mar 2023 19:06:11 GMT  
		Size: 6.1 MB (6053645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51930a8a6c57659f2214203f9bfdd1ca4790b56611c6955b3f07a251cc6be341`  
		Last Modified: Wed, 29 Mar 2023 19:06:10 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c23e3a8524a1e6240c31862047117a05df8f6c8e198822058c1d1c06687755f`  
		Last Modified: Wed, 29 Mar 2023 19:06:10 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:087798748e578aa2f07a9c8c0b984eaf308e03d9974d9ecefdf02c1ad4359344
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11687192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331e0178aa41967ad6c64d6eea6323083ac3c88c4fe617fd54851779ac8095f2`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:20 GMT
ADD file:a6a2f69b60d7d27bc6e2b9b7e9910dabdc3f5e3702c2345d26a7dc8c603ae595 in / 
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 18:02:16 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 29 Mar 2023 18:02:16 GMT
RUN adduser -S eggdrop
# Wed, 29 Mar 2023 18:02:17 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 29 Mar 2023 18:02:18 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 29 Mar 2023 18:06:03 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 29 Mar 2023 18:06:03 GMT
ENV NICK=
# Wed, 29 Mar 2023 18:06:03 GMT
ENV SERVER=
# Wed, 29 Mar 2023 18:06:04 GMT
ENV LISTEN=3333
# Wed, 29 Mar 2023 18:06:04 GMT
ENV OWNER=
# Wed, 29 Mar 2023 18:06:04 GMT
ENV USERFILE=eggdrop.user
# Wed, 29 Mar 2023 18:06:04 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 29 Mar 2023 18:06:04 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 29 Mar 2023 18:06:04 GMT
EXPOSE 3333
# Wed, 29 Mar 2023 18:06:04 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 29 Mar 2023 18:06:04 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 29 Mar 2023 18:06:04 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 29 Mar 2023 18:06:04 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:547446be3368f442c50ff95e2a2a9c85110b6b41bbb3c75b7e5ebb115f478b57`  
		Last Modified: Wed, 29 Mar 2023 17:39:56 GMT  
		Size: 2.7 MB (2709344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb69f3db113b0619a9372f4b7b70feb8f15fe4aa13ba9e5fa4a024ea95731f4c`  
		Last Modified: Wed, 29 Mar 2023 18:06:25 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e598031e523f6acd4c42bf753c34116e6204220d4a61ec11e62b13fb7f138160`  
		Last Modified: Wed, 29 Mar 2023 18:06:28 GMT  
		Size: 10.7 KB (10746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f2b000939306d443c2a1f2bffb5e73dbc192f7683d7b87fd89c2faedf32046`  
		Last Modified: Wed, 29 Mar 2023 18:06:24 GMT  
		Size: 2.8 MB (2776454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f270999340f5f5c78ba08b9cb807914c368554f21ed9bd0aba266124beb2d1`  
		Last Modified: Wed, 29 Mar 2023 18:06:24 GMT  
		Size: 6.2 MB (6186844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1940fe90811d6ce6c64f3eef4eb3b53d915db33644179d48f1b8e71b8ebe4f`  
		Last Modified: Wed, 29 Mar 2023 18:06:23 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c313b4dd4c0ec3851eb42e4665a8400813ddd7d0073c923616846cb98ca2982`  
		Last Modified: Wed, 29 Mar 2023 18:06:23 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
