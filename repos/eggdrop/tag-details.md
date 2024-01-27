<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.9`](#eggdrop19)
-	[`eggdrop:1.9.5`](#eggdrop195)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.9`

```console
$ docker pull eggdrop@sha256:16e07e25600986dcd40d63230d758a00bbaac798ebb8aa64bfd2c4ce46e5f592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9` - linux; amd64

```console
$ docker pull eggdrop@sha256:545f3c6b3fae1eee3b82dad78bca7bb4933e3fc361df31c835fede32aa8af3e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e96a60c235c0c85131c4b9d9a0a9ad05a0c59a71f8d3aa00d390cef0e6cc9ef`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:05 GMT
ADD file:282274bb02b29182f35c732f021f3dab6de9f16a1ae24460061ad1abdca6444a in / 
# Thu, 30 Nov 2023 23:23:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:41:07 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 01 Dec 2023 06:41:08 GMT
RUN adduser -S eggdrop
# Fri, 01 Dec 2023 06:41:09 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 01 Dec 2023 06:41:10 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 01 Dec 2023 06:45:03 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 01 Dec 2023 06:45:04 GMT
ENV NICK=
# Fri, 01 Dec 2023 06:45:04 GMT
ENV SERVER=
# Fri, 01 Dec 2023 06:45:04 GMT
ENV LISTEN=3333
# Fri, 01 Dec 2023 06:45:04 GMT
ENV OWNER=
# Fri, 01 Dec 2023 06:45:04 GMT
ENV USERFILE=eggdrop.user
# Fri, 01 Dec 2023 06:45:04 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 01 Dec 2023 06:45:04 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 01 Dec 2023 06:45:04 GMT
EXPOSE 3333
# Fri, 01 Dec 2023 06:45:04 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 01 Dec 2023 06:45:04 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 01 Dec 2023 06:45:04 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 01 Dec 2023 06:45:05 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:070eb51debd997eca763a31532c01e2579afe94e43b110d84282a81cb576e342`  
		Last Modified: Thu, 30 Nov 2023 23:23:49 GMT  
		Size: 2.8 MB (2807782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:629cf89d5d7e8f97725ff6746082a65b9ae73d314af7a682674c162c9baa0cf8`  
		Last Modified: Fri, 01 Dec 2023 06:45:31 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330a312f95a82e55d4dd1236ad4e70fd752cb23843c89c4b3e5be9b9261b9fd8`  
		Last Modified: Fri, 01 Dec 2023 06:45:29 GMT  
		Size: 10.9 KB (10938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a7e20c17b706565d917aa75b08be6f910828fbd9ac1b964688e7224b727a4f`  
		Last Modified: Fri, 01 Dec 2023 06:45:30 GMT  
		Size: 2.8 MB (2758055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc22440dc807cdaf75d421e92b484931faac1aab57ed26dcd95723a659dadf8`  
		Last Modified: Fri, 01 Dec 2023 06:45:30 GMT  
		Size: 6.1 MB (6146883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7c72d37935ecf627e3519642da6a3653885d7b7ca29055c31023c0f55b608c`  
		Last Modified: Fri, 01 Dec 2023 06:45:29 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da7deba64091e866346a47f2c19a0d3208458a55ebab3f56d56996d0bbb6cc48`  
		Last Modified: Fri, 01 Dec 2023 06:45:29 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:5303975fe3a74d1daa741fa4833543309463f7f6116cd57def0ece9c8befae3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11364118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9787af832df0f155290c28d70bb881ae4e58e303089025b9a5fff48deeba855b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:26 GMT
ADD file:66e93ac5159ebc95b5c9f4e0de97aae75eccd84ab8d5a6f9fac4dba891685e5c in / 
# Fri, 26 Jan 2024 23:49:26 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:11:39 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 27 Jan 2024 00:11:39 GMT
RUN adduser -S eggdrop
# Sat, 27 Jan 2024 00:11:40 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 27 Jan 2024 00:11:43 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 27 Jan 2024 00:16:20 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 27 Jan 2024 00:16:21 GMT
ENV NICK=
# Sat, 27 Jan 2024 00:16:21 GMT
ENV SERVER=
# Sat, 27 Jan 2024 00:16:21 GMT
ENV LISTEN=3333
# Sat, 27 Jan 2024 00:16:21 GMT
ENV OWNER=
# Sat, 27 Jan 2024 00:16:21 GMT
ENV USERFILE=eggdrop.user
# Sat, 27 Jan 2024 00:16:21 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 27 Jan 2024 00:16:21 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 27 Jan 2024 00:16:21 GMT
EXPOSE 3333
# Sat, 27 Jan 2024 00:16:21 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 27 Jan 2024 00:16:22 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 27 Jan 2024 00:16:22 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 27 Jan 2024 00:16:22 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:fb7463fbd2413e7d062aba6aa29a656d8ab69e3219cc8790148f3a6f6127f241`  
		Last Modified: Fri, 26 Jan 2024 23:50:09 GMT  
		Size: 2.6 MB (2615845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222100f0ff57112043cac39b6a2a04f0863bafb7e5894e54e0da2d45ae25b935`  
		Last Modified: Sat, 27 Jan 2024 00:16:50 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2cd0363e95908a579e318c5a21d6b1ddcef7104d565d050073f6954418e8609`  
		Last Modified: Sat, 27 Jan 2024 00:16:48 GMT  
		Size: 10.6 KB (10631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ae25495d96c88f3e52e101244ba154d4787605ea2cbe29239daeb44a44f0a1`  
		Last Modified: Sat, 27 Jan 2024 00:16:49 GMT  
		Size: 2.7 MB (2679969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4494d68e80ca72eac17be0d1feadc6a8d9b7992ed047cb91451c1e78c8cd0844`  
		Last Modified: Sat, 27 Jan 2024 00:16:49 GMT  
		Size: 6.1 MB (6053861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec39e78d7577eb2910c0774d0cc51bd2b672585698e4070189a6e93477aedd`  
		Last Modified: Sat, 27 Jan 2024 00:16:48 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce4469b4088a2b550e6a624884c7d7744bb28687afeafb8dd25f67385fa789a`  
		Last Modified: Sat, 27 Jan 2024 00:16:48 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:9db60674c0f1dd59645d4b6c37cb5d254a2e5c663f8e56149819134d1bb8344b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11686667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b0985cdd9ea5832e1c552759ed321fe961b0f9e480baa8292f7c9b166a7c41`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:11 GMT
ADD file:1efd26ad638f3c262f37eb81a32e3f026121dcd60479e91c42097bfc8329ed3b in / 
# Thu, 30 Nov 2023 23:11:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:14:01 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 01 Dec 2023 03:14:01 GMT
RUN adduser -S eggdrop
# Fri, 01 Dec 2023 03:14:02 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 01 Dec 2023 03:14:04 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 01 Dec 2023 03:17:49 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 01 Dec 2023 03:17:50 GMT
ENV NICK=
# Fri, 01 Dec 2023 03:17:50 GMT
ENV SERVER=
# Fri, 01 Dec 2023 03:17:50 GMT
ENV LISTEN=3333
# Fri, 01 Dec 2023 03:17:50 GMT
ENV OWNER=
# Fri, 01 Dec 2023 03:17:50 GMT
ENV USERFILE=eggdrop.user
# Fri, 01 Dec 2023 03:17:50 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 01 Dec 2023 03:17:50 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 01 Dec 2023 03:17:50 GMT
EXPOSE 3333
# Fri, 01 Dec 2023 03:17:50 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 01 Dec 2023 03:17:50 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 01 Dec 2023 03:17:50 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 01 Dec 2023 03:17:50 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:5362b5901f8a9898f2bcc8eb6c3e6990364aa058617afaae388bdb9f437d3d7e`  
		Last Modified: Thu, 30 Nov 2023 23:11:54 GMT  
		Size: 2.7 MB (2708293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff2069577d157e1182b8b6c04eae6d55712f498b88436f60b4b0a15affb689e`  
		Last Modified: Fri, 01 Dec 2023 03:18:09 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271862d0747f28c19eeeead041d6a2933d36380bfc78a5f44b65094796dcb652`  
		Last Modified: Fri, 01 Dec 2023 03:18:07 GMT  
		Size: 10.7 KB (10745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff489cf648bef12337965e6f858aac0cbf7d48eea86491cb226bd40281d7f73`  
		Last Modified: Fri, 01 Dec 2023 03:18:08 GMT  
		Size: 2.8 MB (2776579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11838f196153b1d83372eb3761df0cba739e83eeefefbfd4865c4f497fedf818`  
		Last Modified: Fri, 01 Dec 2023 03:18:08 GMT  
		Size: 6.2 MB (6187239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601b0134851d1b731ab53e63f85c17817015a8e38f5795e3106a064c97932cef`  
		Last Modified: Fri, 01 Dec 2023 03:18:07 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc987ed7913f661d6b04b54c4c1b0161de75b2aed618c493c4a97f751c0c8865`  
		Last Modified: Fri, 01 Dec 2023 03:18:07 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.9.5`

```console
$ docker pull eggdrop@sha256:16e07e25600986dcd40d63230d758a00bbaac798ebb8aa64bfd2c4ce46e5f592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9.5` - linux; amd64

```console
$ docker pull eggdrop@sha256:545f3c6b3fae1eee3b82dad78bca7bb4933e3fc361df31c835fede32aa8af3e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e96a60c235c0c85131c4b9d9a0a9ad05a0c59a71f8d3aa00d390cef0e6cc9ef`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:05 GMT
ADD file:282274bb02b29182f35c732f021f3dab6de9f16a1ae24460061ad1abdca6444a in / 
# Thu, 30 Nov 2023 23:23:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:41:07 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 01 Dec 2023 06:41:08 GMT
RUN adduser -S eggdrop
# Fri, 01 Dec 2023 06:41:09 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 01 Dec 2023 06:41:10 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 01 Dec 2023 06:45:03 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 01 Dec 2023 06:45:04 GMT
ENV NICK=
# Fri, 01 Dec 2023 06:45:04 GMT
ENV SERVER=
# Fri, 01 Dec 2023 06:45:04 GMT
ENV LISTEN=3333
# Fri, 01 Dec 2023 06:45:04 GMT
ENV OWNER=
# Fri, 01 Dec 2023 06:45:04 GMT
ENV USERFILE=eggdrop.user
# Fri, 01 Dec 2023 06:45:04 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 01 Dec 2023 06:45:04 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 01 Dec 2023 06:45:04 GMT
EXPOSE 3333
# Fri, 01 Dec 2023 06:45:04 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 01 Dec 2023 06:45:04 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 01 Dec 2023 06:45:04 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 01 Dec 2023 06:45:05 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:070eb51debd997eca763a31532c01e2579afe94e43b110d84282a81cb576e342`  
		Last Modified: Thu, 30 Nov 2023 23:23:49 GMT  
		Size: 2.8 MB (2807782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:629cf89d5d7e8f97725ff6746082a65b9ae73d314af7a682674c162c9baa0cf8`  
		Last Modified: Fri, 01 Dec 2023 06:45:31 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330a312f95a82e55d4dd1236ad4e70fd752cb23843c89c4b3e5be9b9261b9fd8`  
		Last Modified: Fri, 01 Dec 2023 06:45:29 GMT  
		Size: 10.9 KB (10938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a7e20c17b706565d917aa75b08be6f910828fbd9ac1b964688e7224b727a4f`  
		Last Modified: Fri, 01 Dec 2023 06:45:30 GMT  
		Size: 2.8 MB (2758055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc22440dc807cdaf75d421e92b484931faac1aab57ed26dcd95723a659dadf8`  
		Last Modified: Fri, 01 Dec 2023 06:45:30 GMT  
		Size: 6.1 MB (6146883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7c72d37935ecf627e3519642da6a3653885d7b7ca29055c31023c0f55b608c`  
		Last Modified: Fri, 01 Dec 2023 06:45:29 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da7deba64091e866346a47f2c19a0d3208458a55ebab3f56d56996d0bbb6cc48`  
		Last Modified: Fri, 01 Dec 2023 06:45:29 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.5` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:5303975fe3a74d1daa741fa4833543309463f7f6116cd57def0ece9c8befae3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11364118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9787af832df0f155290c28d70bb881ae4e58e303089025b9a5fff48deeba855b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:26 GMT
ADD file:66e93ac5159ebc95b5c9f4e0de97aae75eccd84ab8d5a6f9fac4dba891685e5c in / 
# Fri, 26 Jan 2024 23:49:26 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:11:39 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 27 Jan 2024 00:11:39 GMT
RUN adduser -S eggdrop
# Sat, 27 Jan 2024 00:11:40 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 27 Jan 2024 00:11:43 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 27 Jan 2024 00:16:20 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 27 Jan 2024 00:16:21 GMT
ENV NICK=
# Sat, 27 Jan 2024 00:16:21 GMT
ENV SERVER=
# Sat, 27 Jan 2024 00:16:21 GMT
ENV LISTEN=3333
# Sat, 27 Jan 2024 00:16:21 GMT
ENV OWNER=
# Sat, 27 Jan 2024 00:16:21 GMT
ENV USERFILE=eggdrop.user
# Sat, 27 Jan 2024 00:16:21 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 27 Jan 2024 00:16:21 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 27 Jan 2024 00:16:21 GMT
EXPOSE 3333
# Sat, 27 Jan 2024 00:16:21 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 27 Jan 2024 00:16:22 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 27 Jan 2024 00:16:22 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 27 Jan 2024 00:16:22 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:fb7463fbd2413e7d062aba6aa29a656d8ab69e3219cc8790148f3a6f6127f241`  
		Last Modified: Fri, 26 Jan 2024 23:50:09 GMT  
		Size: 2.6 MB (2615845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222100f0ff57112043cac39b6a2a04f0863bafb7e5894e54e0da2d45ae25b935`  
		Last Modified: Sat, 27 Jan 2024 00:16:50 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2cd0363e95908a579e318c5a21d6b1ddcef7104d565d050073f6954418e8609`  
		Last Modified: Sat, 27 Jan 2024 00:16:48 GMT  
		Size: 10.6 KB (10631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ae25495d96c88f3e52e101244ba154d4787605ea2cbe29239daeb44a44f0a1`  
		Last Modified: Sat, 27 Jan 2024 00:16:49 GMT  
		Size: 2.7 MB (2679969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4494d68e80ca72eac17be0d1feadc6a8d9b7992ed047cb91451c1e78c8cd0844`  
		Last Modified: Sat, 27 Jan 2024 00:16:49 GMT  
		Size: 6.1 MB (6053861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec39e78d7577eb2910c0774d0cc51bd2b672585698e4070189a6e93477aedd`  
		Last Modified: Sat, 27 Jan 2024 00:16:48 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce4469b4088a2b550e6a624884c7d7744bb28687afeafb8dd25f67385fa789a`  
		Last Modified: Sat, 27 Jan 2024 00:16:48 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.5` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:9db60674c0f1dd59645d4b6c37cb5d254a2e5c663f8e56149819134d1bb8344b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11686667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b0985cdd9ea5832e1c552759ed321fe961b0f9e480baa8292f7c9b166a7c41`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:11 GMT
ADD file:1efd26ad638f3c262f37eb81a32e3f026121dcd60479e91c42097bfc8329ed3b in / 
# Thu, 30 Nov 2023 23:11:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:14:01 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 01 Dec 2023 03:14:01 GMT
RUN adduser -S eggdrop
# Fri, 01 Dec 2023 03:14:02 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 01 Dec 2023 03:14:04 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 01 Dec 2023 03:17:49 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 01 Dec 2023 03:17:50 GMT
ENV NICK=
# Fri, 01 Dec 2023 03:17:50 GMT
ENV SERVER=
# Fri, 01 Dec 2023 03:17:50 GMT
ENV LISTEN=3333
# Fri, 01 Dec 2023 03:17:50 GMT
ENV OWNER=
# Fri, 01 Dec 2023 03:17:50 GMT
ENV USERFILE=eggdrop.user
# Fri, 01 Dec 2023 03:17:50 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 01 Dec 2023 03:17:50 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 01 Dec 2023 03:17:50 GMT
EXPOSE 3333
# Fri, 01 Dec 2023 03:17:50 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 01 Dec 2023 03:17:50 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 01 Dec 2023 03:17:50 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 01 Dec 2023 03:17:50 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:5362b5901f8a9898f2bcc8eb6c3e6990364aa058617afaae388bdb9f437d3d7e`  
		Last Modified: Thu, 30 Nov 2023 23:11:54 GMT  
		Size: 2.7 MB (2708293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff2069577d157e1182b8b6c04eae6d55712f498b88436f60b4b0a15affb689e`  
		Last Modified: Fri, 01 Dec 2023 03:18:09 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271862d0747f28c19eeeead041d6a2933d36380bfc78a5f44b65094796dcb652`  
		Last Modified: Fri, 01 Dec 2023 03:18:07 GMT  
		Size: 10.7 KB (10745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff489cf648bef12337965e6f858aac0cbf7d48eea86491cb226bd40281d7f73`  
		Last Modified: Fri, 01 Dec 2023 03:18:08 GMT  
		Size: 2.8 MB (2776579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11838f196153b1d83372eb3761df0cba739e83eeefefbfd4865c4f497fedf818`  
		Last Modified: Fri, 01 Dec 2023 03:18:08 GMT  
		Size: 6.2 MB (6187239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601b0134851d1b731ab53e63f85c17817015a8e38f5795e3106a064c97932cef`  
		Last Modified: Fri, 01 Dec 2023 03:18:07 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc987ed7913f661d6b04b54c4c1b0161de75b2aed618c493c4a97f751c0c8865`  
		Last Modified: Fri, 01 Dec 2023 03:18:07 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:087969a2ccfbfa9c667492c0869d42087d0a702096534e86794e8438dbf90140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:0dbae2bcb5c0afd85aeb02ecb33593d552ee8eade082997d60ee456b82360bbf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16146288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43a30c2649a2e91dcfd939f8d0c20f89f38b9c5ca0237b606bd16b87e1f78ff`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:38:43 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Fri, 01 Dec 2023 06:38:44 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Fri, 01 Dec 2023 06:38:45 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Fri, 01 Dec 2023 06:38:45 GMT
ENV EGGDROP_SHA256=a155625d2ac3a0673e69c9d0149293910583c1623cd1f90f38ad2bcba7b2b766
# Fri, 01 Dec 2023 06:38:45 GMT
ENV EGGDROP_COMMIT=322bddbd102d58cdb00864a3a335b086beaf042c
# Fri, 01 Dec 2023 06:40:53 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Fri, 01 Dec 2023 06:40:53 GMT
ENV NICK=
# Fri, 01 Dec 2023 06:40:53 GMT
ENV SERVER=
# Fri, 01 Dec 2023 06:40:53 GMT
ENV LISTEN=3333
# Fri, 01 Dec 2023 06:40:53 GMT
ENV USERFILE=eggdrop.user
# Fri, 01 Dec 2023 06:40:53 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 01 Dec 2023 06:40:53 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 01 Dec 2023 06:40:53 GMT
EXPOSE 3333
# Fri, 01 Dec 2023 06:40:53 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Fri, 01 Dec 2023 06:40:54 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in ./scripts/ 
# Fri, 01 Dec 2023 06:40:54 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 01 Dec 2023 06:40:54 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8d4286230b4d5d95213c19d08015e2d35beb2cffa862992135f0c6a48ba37d`  
		Last Modified: Fri, 01 Dec 2023 06:45:22 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0abd1b087ea616c57c07d1fd242635b591f81b010064f6743f66f46eea39562`  
		Last Modified: Fri, 01 Dec 2023 06:45:22 GMT  
		Size: 1.2 MB (1208548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6afb6802bb96586ab96437c600cdb4a8b9bd5abc46c015bf0f65030badd2d71`  
		Last Modified: Fri, 01 Dec 2023 06:45:24 GMT  
		Size: 11.6 MB (11554131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751ec9b32617d65b3a17cbcd4ce853093b934cafd61065d9e45e88efa26f6918`  
		Last Modified: Fri, 01 Dec 2023 06:45:22 GMT  
		Size: 2.0 KB (1951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7f8e4e30612777c2e9f1478c6164967167c7b009f21d33947e3f5c036dde95`  
		Last Modified: Fri, 01 Dec 2023 06:45:22 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:b3ecac186624c1ef1b49aad7f380a515e6e2f25f91e91b8d615c6dae1973249d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15746026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25421f279ac8fc30422f8881081113aafa2ee33ea87fff891592d21835e962db`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:23 GMT
ADD file:ef699a4b52d87def9be5a058091005e5e3f0bb9fb7bf5c9fe3053ba85d79d7af in / 
# Fri, 26 Jan 2024 23:49:23 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:09:01 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sat, 27 Jan 2024 00:09:01 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Sat, 27 Jan 2024 00:09:02 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Sat, 27 Jan 2024 00:09:03 GMT
ENV EGGDROP_SHA256=a155625d2ac3a0673e69c9d0149293910583c1623cd1f90f38ad2bcba7b2b766
# Sat, 27 Jan 2024 00:09:03 GMT
ENV EGGDROP_COMMIT=322bddbd102d58cdb00864a3a335b086beaf042c
# Sat, 27 Jan 2024 00:11:23 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Sat, 27 Jan 2024 00:11:24 GMT
ENV NICK=
# Sat, 27 Jan 2024 00:11:25 GMT
ENV SERVER=
# Sat, 27 Jan 2024 00:11:25 GMT
ENV LISTEN=3333
# Sat, 27 Jan 2024 00:11:26 GMT
ENV USERFILE=eggdrop.user
# Sat, 27 Jan 2024 00:11:26 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 27 Jan 2024 00:11:26 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 27 Jan 2024 00:11:27 GMT
EXPOSE 3333
# Sat, 27 Jan 2024 00:11:27 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Sat, 27 Jan 2024 00:11:27 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in ./scripts/ 
# Sat, 27 Jan 2024 00:11:27 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 27 Jan 2024 00:11:28 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:dded572f39df01b407585bbbda3ae89a2d14042e68184c8b3f6af6ac7fe5b86b`  
		Last Modified: Fri, 26 Jan 2024 23:50:01 GMT  
		Size: 3.1 MB (3113120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75dd35fe984c1393584176440a5ed0aec30992543f588166b548ae990510046`  
		Last Modified: Sat, 27 Jan 2024 00:16:40 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6775dc99ffe22e0b73ac70f33605d475963df8c0a891ad13a5762e1dc138a4d2`  
		Last Modified: Sat, 27 Jan 2024 00:16:40 GMT  
		Size: 1.2 MB (1190278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53664391843e0d5e89fabb7a56de6bd693548b3d81f306013b605de8e7afe74`  
		Last Modified: Sat, 27 Jan 2024 00:16:42 GMT  
		Size: 11.4 MB (11438337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4035e62368521afe30a21e1006a6a11241b3b86a09ed514e2c9ae37089805e`  
		Last Modified: Sat, 27 Jan 2024 00:16:40 GMT  
		Size: 2.0 KB (1954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5428857012f80c08173542a5357700d977f774b1bd660dccdac14cc14e2ff6b1`  
		Last Modified: Sat, 27 Jan 2024 00:16:40 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:70c32e454aca8c3516627dcde5ed95984bd6101e20fa8af37bf0cc0e2f8f7e93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16114076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f0456d051e5a6a9382948a1fbc291bed7d971febf90183ba72e2096acf1870`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:07 GMT
ADD file:e5c66967d6570e36da50c9d42dd8f8f55e6c6a65b92c79601ea9e750c076fa2a in / 
# Thu, 30 Nov 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:11:53 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Fri, 01 Dec 2023 03:11:53 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Fri, 01 Dec 2023 03:11:55 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Fri, 01 Dec 2023 03:11:55 GMT
ENV EGGDROP_SHA256=a155625d2ac3a0673e69c9d0149293910583c1623cd1f90f38ad2bcba7b2b766
# Fri, 01 Dec 2023 03:11:55 GMT
ENV EGGDROP_COMMIT=322bddbd102d58cdb00864a3a335b086beaf042c
# Fri, 01 Dec 2023 03:13:43 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Fri, 01 Dec 2023 03:13:44 GMT
ENV NICK=
# Fri, 01 Dec 2023 03:13:44 GMT
ENV SERVER=
# Fri, 01 Dec 2023 03:13:44 GMT
ENV LISTEN=3333
# Fri, 01 Dec 2023 03:13:44 GMT
ENV USERFILE=eggdrop.user
# Fri, 01 Dec 2023 03:13:44 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 01 Dec 2023 03:13:44 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 01 Dec 2023 03:13:44 GMT
EXPOSE 3333
# Fri, 01 Dec 2023 03:13:44 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Fri, 01 Dec 2023 03:13:44 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in ./scripts/ 
# Fri, 01 Dec 2023 03:13:44 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 01 Dec 2023 03:13:44 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:b8180c93b172865af87a7c0e7e3c8bcb139e0d0c92e19c96467ff2cd4c8919ad`  
		Last Modified: Thu, 30 Nov 2023 23:11:45 GMT  
		Size: 3.3 MB (3258348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85bacdc4b43589aef43c1d2c353fd54809834e48f4c5df7638a530b51b9c6673`  
		Last Modified: Fri, 01 Dec 2023 03:17:59 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff546a7c3f3fd3c5b3d6deb4fd081a3d899c9c0e34e88598d3ea87de5945259`  
		Last Modified: Fri, 01 Dec 2023 03:18:00 GMT  
		Size: 1.2 MB (1235871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0eca6e881ad2d151b651e87f832ed570e938a42fd3458ff262c735ac05d924`  
		Last Modified: Fri, 01 Dec 2023 03:18:01 GMT  
		Size: 11.6 MB (11615569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317b5fc59491b349f7f90bdcbf66f6a91bcea032b81c0656612af288d30fb380`  
		Last Modified: Fri, 01 Dec 2023 03:17:59 GMT  
		Size: 2.0 KB (1953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39617066b3ff6192087a015914df6009055915d33a4311aff0536537a161d1ae`  
		Last Modified: Fri, 01 Dec 2023 03:17:59 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:16e07e25600986dcd40d63230d758a00bbaac798ebb8aa64bfd2c4ce46e5f592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:545f3c6b3fae1eee3b82dad78bca7bb4933e3fc361df31c835fede32aa8af3e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e96a60c235c0c85131c4b9d9a0a9ad05a0c59a71f8d3aa00d390cef0e6cc9ef`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:05 GMT
ADD file:282274bb02b29182f35c732f021f3dab6de9f16a1ae24460061ad1abdca6444a in / 
# Thu, 30 Nov 2023 23:23:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:41:07 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 01 Dec 2023 06:41:08 GMT
RUN adduser -S eggdrop
# Fri, 01 Dec 2023 06:41:09 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 01 Dec 2023 06:41:10 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 01 Dec 2023 06:45:03 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 01 Dec 2023 06:45:04 GMT
ENV NICK=
# Fri, 01 Dec 2023 06:45:04 GMT
ENV SERVER=
# Fri, 01 Dec 2023 06:45:04 GMT
ENV LISTEN=3333
# Fri, 01 Dec 2023 06:45:04 GMT
ENV OWNER=
# Fri, 01 Dec 2023 06:45:04 GMT
ENV USERFILE=eggdrop.user
# Fri, 01 Dec 2023 06:45:04 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 01 Dec 2023 06:45:04 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 01 Dec 2023 06:45:04 GMT
EXPOSE 3333
# Fri, 01 Dec 2023 06:45:04 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 01 Dec 2023 06:45:04 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 01 Dec 2023 06:45:04 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 01 Dec 2023 06:45:05 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:070eb51debd997eca763a31532c01e2579afe94e43b110d84282a81cb576e342`  
		Last Modified: Thu, 30 Nov 2023 23:23:49 GMT  
		Size: 2.8 MB (2807782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:629cf89d5d7e8f97725ff6746082a65b9ae73d314af7a682674c162c9baa0cf8`  
		Last Modified: Fri, 01 Dec 2023 06:45:31 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330a312f95a82e55d4dd1236ad4e70fd752cb23843c89c4b3e5be9b9261b9fd8`  
		Last Modified: Fri, 01 Dec 2023 06:45:29 GMT  
		Size: 10.9 KB (10938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a7e20c17b706565d917aa75b08be6f910828fbd9ac1b964688e7224b727a4f`  
		Last Modified: Fri, 01 Dec 2023 06:45:30 GMT  
		Size: 2.8 MB (2758055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc22440dc807cdaf75d421e92b484931faac1aab57ed26dcd95723a659dadf8`  
		Last Modified: Fri, 01 Dec 2023 06:45:30 GMT  
		Size: 6.1 MB (6146883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7c72d37935ecf627e3519642da6a3653885d7b7ca29055c31023c0f55b608c`  
		Last Modified: Fri, 01 Dec 2023 06:45:29 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da7deba64091e866346a47f2c19a0d3208458a55ebab3f56d56996d0bbb6cc48`  
		Last Modified: Fri, 01 Dec 2023 06:45:29 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:5303975fe3a74d1daa741fa4833543309463f7f6116cd57def0ece9c8befae3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11364118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9787af832df0f155290c28d70bb881ae4e58e303089025b9a5fff48deeba855b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:26 GMT
ADD file:66e93ac5159ebc95b5c9f4e0de97aae75eccd84ab8d5a6f9fac4dba891685e5c in / 
# Fri, 26 Jan 2024 23:49:26 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:11:39 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 27 Jan 2024 00:11:39 GMT
RUN adduser -S eggdrop
# Sat, 27 Jan 2024 00:11:40 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 27 Jan 2024 00:11:43 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 27 Jan 2024 00:16:20 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 27 Jan 2024 00:16:21 GMT
ENV NICK=
# Sat, 27 Jan 2024 00:16:21 GMT
ENV SERVER=
# Sat, 27 Jan 2024 00:16:21 GMT
ENV LISTEN=3333
# Sat, 27 Jan 2024 00:16:21 GMT
ENV OWNER=
# Sat, 27 Jan 2024 00:16:21 GMT
ENV USERFILE=eggdrop.user
# Sat, 27 Jan 2024 00:16:21 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 27 Jan 2024 00:16:21 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 27 Jan 2024 00:16:21 GMT
EXPOSE 3333
# Sat, 27 Jan 2024 00:16:21 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 27 Jan 2024 00:16:22 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 27 Jan 2024 00:16:22 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 27 Jan 2024 00:16:22 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:fb7463fbd2413e7d062aba6aa29a656d8ab69e3219cc8790148f3a6f6127f241`  
		Last Modified: Fri, 26 Jan 2024 23:50:09 GMT  
		Size: 2.6 MB (2615845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222100f0ff57112043cac39b6a2a04f0863bafb7e5894e54e0da2d45ae25b935`  
		Last Modified: Sat, 27 Jan 2024 00:16:50 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2cd0363e95908a579e318c5a21d6b1ddcef7104d565d050073f6954418e8609`  
		Last Modified: Sat, 27 Jan 2024 00:16:48 GMT  
		Size: 10.6 KB (10631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ae25495d96c88f3e52e101244ba154d4787605ea2cbe29239daeb44a44f0a1`  
		Last Modified: Sat, 27 Jan 2024 00:16:49 GMT  
		Size: 2.7 MB (2679969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4494d68e80ca72eac17be0d1feadc6a8d9b7992ed047cb91451c1e78c8cd0844`  
		Last Modified: Sat, 27 Jan 2024 00:16:49 GMT  
		Size: 6.1 MB (6053861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec39e78d7577eb2910c0774d0cc51bd2b672585698e4070189a6e93477aedd`  
		Last Modified: Sat, 27 Jan 2024 00:16:48 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce4469b4088a2b550e6a624884c7d7744bb28687afeafb8dd25f67385fa789a`  
		Last Modified: Sat, 27 Jan 2024 00:16:48 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:9db60674c0f1dd59645d4b6c37cb5d254a2e5c663f8e56149819134d1bb8344b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11686667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b0985cdd9ea5832e1c552759ed321fe961b0f9e480baa8292f7c9b166a7c41`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:11 GMT
ADD file:1efd26ad638f3c262f37eb81a32e3f026121dcd60479e91c42097bfc8329ed3b in / 
# Thu, 30 Nov 2023 23:11:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:14:01 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 01 Dec 2023 03:14:01 GMT
RUN adduser -S eggdrop
# Fri, 01 Dec 2023 03:14:02 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 01 Dec 2023 03:14:04 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 01 Dec 2023 03:17:49 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 01 Dec 2023 03:17:50 GMT
ENV NICK=
# Fri, 01 Dec 2023 03:17:50 GMT
ENV SERVER=
# Fri, 01 Dec 2023 03:17:50 GMT
ENV LISTEN=3333
# Fri, 01 Dec 2023 03:17:50 GMT
ENV OWNER=
# Fri, 01 Dec 2023 03:17:50 GMT
ENV USERFILE=eggdrop.user
# Fri, 01 Dec 2023 03:17:50 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 01 Dec 2023 03:17:50 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 01 Dec 2023 03:17:50 GMT
EXPOSE 3333
# Fri, 01 Dec 2023 03:17:50 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 01 Dec 2023 03:17:50 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 01 Dec 2023 03:17:50 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 01 Dec 2023 03:17:50 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:5362b5901f8a9898f2bcc8eb6c3e6990364aa058617afaae388bdb9f437d3d7e`  
		Last Modified: Thu, 30 Nov 2023 23:11:54 GMT  
		Size: 2.7 MB (2708293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff2069577d157e1182b8b6c04eae6d55712f498b88436f60b4b0a15affb689e`  
		Last Modified: Fri, 01 Dec 2023 03:18:09 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271862d0747f28c19eeeead041d6a2933d36380bfc78a5f44b65094796dcb652`  
		Last Modified: Fri, 01 Dec 2023 03:18:07 GMT  
		Size: 10.7 KB (10745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff489cf648bef12337965e6f858aac0cbf7d48eea86491cb226bd40281d7f73`  
		Last Modified: Fri, 01 Dec 2023 03:18:08 GMT  
		Size: 2.8 MB (2776579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11838f196153b1d83372eb3761df0cba739e83eeefefbfd4865c4f497fedf818`  
		Last Modified: Fri, 01 Dec 2023 03:18:08 GMT  
		Size: 6.2 MB (6187239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601b0134851d1b731ab53e63f85c17817015a8e38f5795e3106a064c97932cef`  
		Last Modified: Fri, 01 Dec 2023 03:18:07 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc987ed7913f661d6b04b54c4c1b0161de75b2aed618c493c4a97f751c0c8865`  
		Last Modified: Fri, 01 Dec 2023 03:18:07 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:16e07e25600986dcd40d63230d758a00bbaac798ebb8aa64bfd2c4ce46e5f592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:545f3c6b3fae1eee3b82dad78bca7bb4933e3fc361df31c835fede32aa8af3e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e96a60c235c0c85131c4b9d9a0a9ad05a0c59a71f8d3aa00d390cef0e6cc9ef`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:05 GMT
ADD file:282274bb02b29182f35c732f021f3dab6de9f16a1ae24460061ad1abdca6444a in / 
# Thu, 30 Nov 2023 23:23:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:41:07 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 01 Dec 2023 06:41:08 GMT
RUN adduser -S eggdrop
# Fri, 01 Dec 2023 06:41:09 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 01 Dec 2023 06:41:10 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 01 Dec 2023 06:45:03 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 01 Dec 2023 06:45:04 GMT
ENV NICK=
# Fri, 01 Dec 2023 06:45:04 GMT
ENV SERVER=
# Fri, 01 Dec 2023 06:45:04 GMT
ENV LISTEN=3333
# Fri, 01 Dec 2023 06:45:04 GMT
ENV OWNER=
# Fri, 01 Dec 2023 06:45:04 GMT
ENV USERFILE=eggdrop.user
# Fri, 01 Dec 2023 06:45:04 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 01 Dec 2023 06:45:04 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 01 Dec 2023 06:45:04 GMT
EXPOSE 3333
# Fri, 01 Dec 2023 06:45:04 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 01 Dec 2023 06:45:04 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 01 Dec 2023 06:45:04 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 01 Dec 2023 06:45:05 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:070eb51debd997eca763a31532c01e2579afe94e43b110d84282a81cb576e342`  
		Last Modified: Thu, 30 Nov 2023 23:23:49 GMT  
		Size: 2.8 MB (2807782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:629cf89d5d7e8f97725ff6746082a65b9ae73d314af7a682674c162c9baa0cf8`  
		Last Modified: Fri, 01 Dec 2023 06:45:31 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330a312f95a82e55d4dd1236ad4e70fd752cb23843c89c4b3e5be9b9261b9fd8`  
		Last Modified: Fri, 01 Dec 2023 06:45:29 GMT  
		Size: 10.9 KB (10938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a7e20c17b706565d917aa75b08be6f910828fbd9ac1b964688e7224b727a4f`  
		Last Modified: Fri, 01 Dec 2023 06:45:30 GMT  
		Size: 2.8 MB (2758055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc22440dc807cdaf75d421e92b484931faac1aab57ed26dcd95723a659dadf8`  
		Last Modified: Fri, 01 Dec 2023 06:45:30 GMT  
		Size: 6.1 MB (6146883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7c72d37935ecf627e3519642da6a3653885d7b7ca29055c31023c0f55b608c`  
		Last Modified: Fri, 01 Dec 2023 06:45:29 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da7deba64091e866346a47f2c19a0d3208458a55ebab3f56d56996d0bbb6cc48`  
		Last Modified: Fri, 01 Dec 2023 06:45:29 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:5303975fe3a74d1daa741fa4833543309463f7f6116cd57def0ece9c8befae3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11364118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9787af832df0f155290c28d70bb881ae4e58e303089025b9a5fff48deeba855b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:26 GMT
ADD file:66e93ac5159ebc95b5c9f4e0de97aae75eccd84ab8d5a6f9fac4dba891685e5c in / 
# Fri, 26 Jan 2024 23:49:26 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:11:39 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 27 Jan 2024 00:11:39 GMT
RUN adduser -S eggdrop
# Sat, 27 Jan 2024 00:11:40 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 27 Jan 2024 00:11:43 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 27 Jan 2024 00:16:20 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 27 Jan 2024 00:16:21 GMT
ENV NICK=
# Sat, 27 Jan 2024 00:16:21 GMT
ENV SERVER=
# Sat, 27 Jan 2024 00:16:21 GMT
ENV LISTEN=3333
# Sat, 27 Jan 2024 00:16:21 GMT
ENV OWNER=
# Sat, 27 Jan 2024 00:16:21 GMT
ENV USERFILE=eggdrop.user
# Sat, 27 Jan 2024 00:16:21 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 27 Jan 2024 00:16:21 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 27 Jan 2024 00:16:21 GMT
EXPOSE 3333
# Sat, 27 Jan 2024 00:16:21 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 27 Jan 2024 00:16:22 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 27 Jan 2024 00:16:22 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 27 Jan 2024 00:16:22 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:fb7463fbd2413e7d062aba6aa29a656d8ab69e3219cc8790148f3a6f6127f241`  
		Last Modified: Fri, 26 Jan 2024 23:50:09 GMT  
		Size: 2.6 MB (2615845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222100f0ff57112043cac39b6a2a04f0863bafb7e5894e54e0da2d45ae25b935`  
		Last Modified: Sat, 27 Jan 2024 00:16:50 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2cd0363e95908a579e318c5a21d6b1ddcef7104d565d050073f6954418e8609`  
		Last Modified: Sat, 27 Jan 2024 00:16:48 GMT  
		Size: 10.6 KB (10631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ae25495d96c88f3e52e101244ba154d4787605ea2cbe29239daeb44a44f0a1`  
		Last Modified: Sat, 27 Jan 2024 00:16:49 GMT  
		Size: 2.7 MB (2679969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4494d68e80ca72eac17be0d1feadc6a8d9b7992ed047cb91451c1e78c8cd0844`  
		Last Modified: Sat, 27 Jan 2024 00:16:49 GMT  
		Size: 6.1 MB (6053861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bec39e78d7577eb2910c0774d0cc51bd2b672585698e4070189a6e93477aedd`  
		Last Modified: Sat, 27 Jan 2024 00:16:48 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce4469b4088a2b550e6a624884c7d7744bb28687afeafb8dd25f67385fa789a`  
		Last Modified: Sat, 27 Jan 2024 00:16:48 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:9db60674c0f1dd59645d4b6c37cb5d254a2e5c663f8e56149819134d1bb8344b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11686667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b0985cdd9ea5832e1c552759ed321fe961b0f9e480baa8292f7c9b166a7c41`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:11 GMT
ADD file:1efd26ad638f3c262f37eb81a32e3f026121dcd60479e91c42097bfc8329ed3b in / 
# Thu, 30 Nov 2023 23:11:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:14:01 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 01 Dec 2023 03:14:01 GMT
RUN adduser -S eggdrop
# Fri, 01 Dec 2023 03:14:02 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 01 Dec 2023 03:14:04 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 01 Dec 2023 03:17:49 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 01 Dec 2023 03:17:50 GMT
ENV NICK=
# Fri, 01 Dec 2023 03:17:50 GMT
ENV SERVER=
# Fri, 01 Dec 2023 03:17:50 GMT
ENV LISTEN=3333
# Fri, 01 Dec 2023 03:17:50 GMT
ENV OWNER=
# Fri, 01 Dec 2023 03:17:50 GMT
ENV USERFILE=eggdrop.user
# Fri, 01 Dec 2023 03:17:50 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 01 Dec 2023 03:17:50 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 01 Dec 2023 03:17:50 GMT
EXPOSE 3333
# Fri, 01 Dec 2023 03:17:50 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 01 Dec 2023 03:17:50 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 01 Dec 2023 03:17:50 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 01 Dec 2023 03:17:50 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:5362b5901f8a9898f2bcc8eb6c3e6990364aa058617afaae388bdb9f437d3d7e`  
		Last Modified: Thu, 30 Nov 2023 23:11:54 GMT  
		Size: 2.7 MB (2708293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff2069577d157e1182b8b6c04eae6d55712f498b88436f60b4b0a15affb689e`  
		Last Modified: Fri, 01 Dec 2023 03:18:09 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271862d0747f28c19eeeead041d6a2933d36380bfc78a5f44b65094796dcb652`  
		Last Modified: Fri, 01 Dec 2023 03:18:07 GMT  
		Size: 10.7 KB (10745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff489cf648bef12337965e6f858aac0cbf7d48eea86491cb226bd40281d7f73`  
		Last Modified: Fri, 01 Dec 2023 03:18:08 GMT  
		Size: 2.8 MB (2776579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11838f196153b1d83372eb3761df0cba739e83eeefefbfd4865c4f497fedf818`  
		Last Modified: Fri, 01 Dec 2023 03:18:08 GMT  
		Size: 6.2 MB (6187239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601b0134851d1b731ab53e63f85c17817015a8e38f5795e3106a064c97932cef`  
		Last Modified: Fri, 01 Dec 2023 03:18:07 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc987ed7913f661d6b04b54c4c1b0161de75b2aed618c493c4a97f751c0c8865`  
		Last Modified: Fri, 01 Dec 2023 03:18:07 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
