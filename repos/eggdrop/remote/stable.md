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
