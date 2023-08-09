<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.9`](#eggdrop19)
-	[`eggdrop:1.9.5`](#eggdrop195)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.9`

```console
$ docker pull eggdrop@sha256:ce2d5608e40789dfceafed599ff7987d3e2ca5ced336e29882656a4273653ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9` - linux; amd64

```console
$ docker pull eggdrop@sha256:067001b49b16e7b2843450085e133de7119fea0ea83ece8a1fa1e228d7c60b64
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7869f72da560a9be174f98cf0682f54ae7aec597d597e57ca55596f73c1668`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:41:07 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 08 Aug 2023 23:41:07 GMT
RUN adduser -S eggdrop
# Tue, 08 Aug 2023 23:41:08 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 08 Aug 2023 23:41:09 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 08 Aug 2023 23:45:02 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 08 Aug 2023 23:45:02 GMT
ENV NICK=
# Tue, 08 Aug 2023 23:45:02 GMT
ENV SERVER=
# Tue, 08 Aug 2023 23:45:02 GMT
ENV LISTEN=3333
# Tue, 08 Aug 2023 23:45:02 GMT
ENV OWNER=
# Tue, 08 Aug 2023 23:45:02 GMT
ENV USERFILE=eggdrop.user
# Tue, 08 Aug 2023 23:45:02 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 08 Aug 2023 23:45:02 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 08 Aug 2023 23:45:03 GMT
EXPOSE 3333
# Tue, 08 Aug 2023 23:45:03 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 08 Aug 2023 23:45:03 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 08 Aug 2023 23:45:03 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 08 Aug 2023 23:45:03 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4acb10f80f9f6279e3de61139d3c6811cad56af40f95b49b65dc9f93f87916`  
		Last Modified: Tue, 08 Aug 2023 23:45:31 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f039073aec9e1300ad97f4ba8443ef0f261977135eb1c907a9c02d44b8795a7f`  
		Last Modified: Tue, 08 Aug 2023 23:45:29 GMT  
		Size: 10.9 KB (10941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fe6012fe71d2ad532da09cc225006fa5ebd6ce40673870ad2847d8cc6a9a65`  
		Last Modified: Tue, 08 Aug 2023 23:45:30 GMT  
		Size: 2.8 MB (2758095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e415f33afb0f4b927816a6df8a833544d7d23bde202f2fb405eedd7086920c32`  
		Last Modified: Tue, 08 Aug 2023 23:45:30 GMT  
		Size: 6.1 MB (6146727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2836a59010f1e0c892f072d6cb6077f8fe5439f216144ca41feb1ce9745e5b7f`  
		Last Modified: Tue, 08 Aug 2023 23:45:29 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0216508c10c8057645f42bae6e9f9f60d66c81009004994b998548a88d9903`  
		Last Modified: Tue, 08 Aug 2023 23:45:29 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:f515853a8633cc2acb2f7b272809c99fcced45d052a2e1a4abb0c3a8ba6f5832
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11363784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd681812c870f1a0dad0a33ac5d324e13e9c199c05d2b0b48c40ffd1f06541b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:20 GMT
ADD file:321b24cc0fbd39caa2d7672a740d2cd2030ba99cab16f50c22db9955bd99350b in / 
# Mon, 07 Aug 2023 19:49:20 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 22:07:45 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 07 Aug 2023 22:07:45 GMT
RUN adduser -S eggdrop
# Mon, 07 Aug 2023 22:07:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 07 Aug 2023 22:07:48 GMT
RUN apk add --no-cache tcl bash openssl
# Mon, 07 Aug 2023 22:12:58 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 07 Aug 2023 22:12:58 GMT
ENV NICK=
# Mon, 07 Aug 2023 22:12:58 GMT
ENV SERVER=
# Mon, 07 Aug 2023 22:12:58 GMT
ENV LISTEN=3333
# Mon, 07 Aug 2023 22:12:58 GMT
ENV OWNER=
# Mon, 07 Aug 2023 22:12:58 GMT
ENV USERFILE=eggdrop.user
# Mon, 07 Aug 2023 22:12:58 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 07 Aug 2023 22:12:58 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 07 Aug 2023 22:12:58 GMT
EXPOSE 3333
# Mon, 07 Aug 2023 22:12:58 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 07 Aug 2023 22:12:59 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 07 Aug 2023 22:12:59 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 07 Aug 2023 22:12:59 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:dffa980f71c953938bb194a457aa62e7f1885137331eef8bf7f9403c075f711c`  
		Last Modified: Mon, 07 Aug 2023 19:50:02 GMT  
		Size: 2.6 MB (2615553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b720555f5994efe82d1f8fa1a831f681243dab05b37ca283b93588190b20c8`  
		Last Modified: Mon, 07 Aug 2023 22:13:28 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f700305957831109bfaa5a699e5e743a7e76daf177c8f4b821ef1a3a6ab0d5cb`  
		Last Modified: Mon, 07 Aug 2023 22:13:26 GMT  
		Size: 10.6 KB (10629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01fa1c3b77ab4e8fb787f9c731ec1b11637eac08644c829fb22295bf912da747`  
		Last Modified: Mon, 07 Aug 2023 22:13:28 GMT  
		Size: 2.7 MB (2679936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7454d49e1110383afbfe9a1d9c3aa7bb95bb2394f687d3daf288d1efe2f2078e`  
		Last Modified: Mon, 07 Aug 2023 22:13:28 GMT  
		Size: 6.1 MB (6053856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab34a30dd387b3045fc7447b49799e52ed88561de2d3f56ca91a72bd3a1139d8`  
		Last Modified: Mon, 07 Aug 2023 22:13:26 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd0f9c22b9cf4325e32b32b208cb3f28946ce5eedd2346c4da6367fd436b484`  
		Last Modified: Mon, 07 Aug 2023 22:13:26 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:206d9da498c45c71109b9dd23adfc9d77d9f704f95b90da2118edf61f783ee02
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11686461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbce1c0975c3fede1fda10cf32063453feecca60130a785ebf655e6ece8197af`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:26 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 07 Aug 2023 19:39:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:05:35 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 08 Aug 2023 23:05:36 GMT
RUN adduser -S eggdrop
# Tue, 08 Aug 2023 23:05:37 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 08 Aug 2023 23:05:38 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 08 Aug 2023 23:09:15 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 08 Aug 2023 23:09:15 GMT
ENV NICK=
# Tue, 08 Aug 2023 23:09:15 GMT
ENV SERVER=
# Tue, 08 Aug 2023 23:09:15 GMT
ENV LISTEN=3333
# Tue, 08 Aug 2023 23:09:15 GMT
ENV OWNER=
# Tue, 08 Aug 2023 23:09:15 GMT
ENV USERFILE=eggdrop.user
# Tue, 08 Aug 2023 23:09:15 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 08 Aug 2023 23:09:15 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 08 Aug 2023 23:09:15 GMT
EXPOSE 3333
# Tue, 08 Aug 2023 23:09:16 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 08 Aug 2023 23:09:16 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 08 Aug 2023 23:09:16 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 08 Aug 2023 23:09:16 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6cc73b6a504f251379d7d25b533cb1b15e55ffaa00346fcffd270abbaccdf7`  
		Last Modified: Tue, 08 Aug 2023 23:09:43 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0429d00c2602fa6069fd322fc19ce26692da176bfc289d68b71a57b2ff2769`  
		Last Modified: Tue, 08 Aug 2023 23:09:41 GMT  
		Size: 10.7 KB (10748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b334d21e87707297512e175e343dd92de9023742868e23d085f1322b776adc`  
		Last Modified: Tue, 08 Aug 2023 23:09:42 GMT  
		Size: 2.8 MB (2776573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe6df62b68fb22fabd8c2ccdb8fa6025c5493621650e31cdc3f191593e631fe`  
		Last Modified: Tue, 08 Aug 2023 23:09:42 GMT  
		Size: 6.2 MB (6187306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b530eb3732a3031c16ca294daba836e6c8ae5cf0dab82e1115da5fce03ddd67`  
		Last Modified: Tue, 08 Aug 2023 23:09:41 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e69277efb4953ec23569199945650d356c677b05bb61fdbaf710a42c1c1dc2c`  
		Last Modified: Tue, 08 Aug 2023 23:09:41 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.9.5`

```console
$ docker pull eggdrop@sha256:ce2d5608e40789dfceafed599ff7987d3e2ca5ced336e29882656a4273653ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9.5` - linux; amd64

```console
$ docker pull eggdrop@sha256:067001b49b16e7b2843450085e133de7119fea0ea83ece8a1fa1e228d7c60b64
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7869f72da560a9be174f98cf0682f54ae7aec597d597e57ca55596f73c1668`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:41:07 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 08 Aug 2023 23:41:07 GMT
RUN adduser -S eggdrop
# Tue, 08 Aug 2023 23:41:08 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 08 Aug 2023 23:41:09 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 08 Aug 2023 23:45:02 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 08 Aug 2023 23:45:02 GMT
ENV NICK=
# Tue, 08 Aug 2023 23:45:02 GMT
ENV SERVER=
# Tue, 08 Aug 2023 23:45:02 GMT
ENV LISTEN=3333
# Tue, 08 Aug 2023 23:45:02 GMT
ENV OWNER=
# Tue, 08 Aug 2023 23:45:02 GMT
ENV USERFILE=eggdrop.user
# Tue, 08 Aug 2023 23:45:02 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 08 Aug 2023 23:45:02 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 08 Aug 2023 23:45:03 GMT
EXPOSE 3333
# Tue, 08 Aug 2023 23:45:03 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 08 Aug 2023 23:45:03 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 08 Aug 2023 23:45:03 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 08 Aug 2023 23:45:03 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4acb10f80f9f6279e3de61139d3c6811cad56af40f95b49b65dc9f93f87916`  
		Last Modified: Tue, 08 Aug 2023 23:45:31 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f039073aec9e1300ad97f4ba8443ef0f261977135eb1c907a9c02d44b8795a7f`  
		Last Modified: Tue, 08 Aug 2023 23:45:29 GMT  
		Size: 10.9 KB (10941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fe6012fe71d2ad532da09cc225006fa5ebd6ce40673870ad2847d8cc6a9a65`  
		Last Modified: Tue, 08 Aug 2023 23:45:30 GMT  
		Size: 2.8 MB (2758095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e415f33afb0f4b927816a6df8a833544d7d23bde202f2fb405eedd7086920c32`  
		Last Modified: Tue, 08 Aug 2023 23:45:30 GMT  
		Size: 6.1 MB (6146727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2836a59010f1e0c892f072d6cb6077f8fe5439f216144ca41feb1ce9745e5b7f`  
		Last Modified: Tue, 08 Aug 2023 23:45:29 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0216508c10c8057645f42bae6e9f9f60d66c81009004994b998548a88d9903`  
		Last Modified: Tue, 08 Aug 2023 23:45:29 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.5` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:f515853a8633cc2acb2f7b272809c99fcced45d052a2e1a4abb0c3a8ba6f5832
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11363784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd681812c870f1a0dad0a33ac5d324e13e9c199c05d2b0b48c40ffd1f06541b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:20 GMT
ADD file:321b24cc0fbd39caa2d7672a740d2cd2030ba99cab16f50c22db9955bd99350b in / 
# Mon, 07 Aug 2023 19:49:20 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 22:07:45 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 07 Aug 2023 22:07:45 GMT
RUN adduser -S eggdrop
# Mon, 07 Aug 2023 22:07:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 07 Aug 2023 22:07:48 GMT
RUN apk add --no-cache tcl bash openssl
# Mon, 07 Aug 2023 22:12:58 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 07 Aug 2023 22:12:58 GMT
ENV NICK=
# Mon, 07 Aug 2023 22:12:58 GMT
ENV SERVER=
# Mon, 07 Aug 2023 22:12:58 GMT
ENV LISTEN=3333
# Mon, 07 Aug 2023 22:12:58 GMT
ENV OWNER=
# Mon, 07 Aug 2023 22:12:58 GMT
ENV USERFILE=eggdrop.user
# Mon, 07 Aug 2023 22:12:58 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 07 Aug 2023 22:12:58 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 07 Aug 2023 22:12:58 GMT
EXPOSE 3333
# Mon, 07 Aug 2023 22:12:58 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 07 Aug 2023 22:12:59 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 07 Aug 2023 22:12:59 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 07 Aug 2023 22:12:59 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:dffa980f71c953938bb194a457aa62e7f1885137331eef8bf7f9403c075f711c`  
		Last Modified: Mon, 07 Aug 2023 19:50:02 GMT  
		Size: 2.6 MB (2615553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b720555f5994efe82d1f8fa1a831f681243dab05b37ca283b93588190b20c8`  
		Last Modified: Mon, 07 Aug 2023 22:13:28 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f700305957831109bfaa5a699e5e743a7e76daf177c8f4b821ef1a3a6ab0d5cb`  
		Last Modified: Mon, 07 Aug 2023 22:13:26 GMT  
		Size: 10.6 KB (10629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01fa1c3b77ab4e8fb787f9c731ec1b11637eac08644c829fb22295bf912da747`  
		Last Modified: Mon, 07 Aug 2023 22:13:28 GMT  
		Size: 2.7 MB (2679936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7454d49e1110383afbfe9a1d9c3aa7bb95bb2394f687d3daf288d1efe2f2078e`  
		Last Modified: Mon, 07 Aug 2023 22:13:28 GMT  
		Size: 6.1 MB (6053856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab34a30dd387b3045fc7447b49799e52ed88561de2d3f56ca91a72bd3a1139d8`  
		Last Modified: Mon, 07 Aug 2023 22:13:26 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd0f9c22b9cf4325e32b32b208cb3f28946ce5eedd2346c4da6367fd436b484`  
		Last Modified: Mon, 07 Aug 2023 22:13:26 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.5` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:206d9da498c45c71109b9dd23adfc9d77d9f704f95b90da2118edf61f783ee02
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11686461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbce1c0975c3fede1fda10cf32063453feecca60130a785ebf655e6ece8197af`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:26 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 07 Aug 2023 19:39:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:05:35 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 08 Aug 2023 23:05:36 GMT
RUN adduser -S eggdrop
# Tue, 08 Aug 2023 23:05:37 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 08 Aug 2023 23:05:38 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 08 Aug 2023 23:09:15 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 08 Aug 2023 23:09:15 GMT
ENV NICK=
# Tue, 08 Aug 2023 23:09:15 GMT
ENV SERVER=
# Tue, 08 Aug 2023 23:09:15 GMT
ENV LISTEN=3333
# Tue, 08 Aug 2023 23:09:15 GMT
ENV OWNER=
# Tue, 08 Aug 2023 23:09:15 GMT
ENV USERFILE=eggdrop.user
# Tue, 08 Aug 2023 23:09:15 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 08 Aug 2023 23:09:15 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 08 Aug 2023 23:09:15 GMT
EXPOSE 3333
# Tue, 08 Aug 2023 23:09:16 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 08 Aug 2023 23:09:16 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 08 Aug 2023 23:09:16 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 08 Aug 2023 23:09:16 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6cc73b6a504f251379d7d25b533cb1b15e55ffaa00346fcffd270abbaccdf7`  
		Last Modified: Tue, 08 Aug 2023 23:09:43 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0429d00c2602fa6069fd322fc19ce26692da176bfc289d68b71a57b2ff2769`  
		Last Modified: Tue, 08 Aug 2023 23:09:41 GMT  
		Size: 10.7 KB (10748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b334d21e87707297512e175e343dd92de9023742868e23d085f1322b776adc`  
		Last Modified: Tue, 08 Aug 2023 23:09:42 GMT  
		Size: 2.8 MB (2776573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe6df62b68fb22fabd8c2ccdb8fa6025c5493621650e31cdc3f191593e631fe`  
		Last Modified: Tue, 08 Aug 2023 23:09:42 GMT  
		Size: 6.2 MB (6187306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b530eb3732a3031c16ca294daba836e6c8ae5cf0dab82e1115da5fce03ddd67`  
		Last Modified: Tue, 08 Aug 2023 23:09:41 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e69277efb4953ec23569199945650d356c677b05bb61fdbaf710a42c1c1dc2c`  
		Last Modified: Tue, 08 Aug 2023 23:09:41 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:e787f2fe83af76f1390474465c965e0d991427eb8880a0add2387df80ba4a991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:efda885301af66513774188f4e3f0b2913f63aaabfdc179425e9969a340942a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16132112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9417ba1287905d0241856d3a71d726f88ed396dd3902270009ceae49a373676`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:37:13 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 08 Aug 2023 23:37:13 GMT
RUN adduser -S eggdrop
# Tue, 08 Aug 2023 23:37:14 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 08 Aug 2023 23:37:14 GMT
ENV EGGDROP_SHA256=cc7936ee427959081651319119ac0b8f3581a18d7be7b20f71023954f1f69a91
# Tue, 08 Aug 2023 23:37:14 GMT
ENV EGGDROP_COMMIT=26ecf0921ee84c5bf61cb31014a75f02670b1af4
# Tue, 08 Aug 2023 23:37:15 GMT
RUN apk --update add --no-cache bash openssl
# Tue, 08 Aug 2023 23:40:49 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 08 Aug 2023 23:40:49 GMT
ENV NICK=
# Tue, 08 Aug 2023 23:40:49 GMT
ENV SERVER=
# Tue, 08 Aug 2023 23:40:49 GMT
ENV LISTEN=3333
# Tue, 08 Aug 2023 23:40:49 GMT
ENV OWNER=
# Tue, 08 Aug 2023 23:40:49 GMT
ENV USERFILE=eggdrop.user
# Tue, 08 Aug 2023 23:40:49 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 08 Aug 2023 23:40:49 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 08 Aug 2023 23:40:50 GMT
EXPOSE 3333
# Tue, 08 Aug 2023 23:40:50 GMT
COPY file:35e05bb72116a1848ec779e3fbc4ea6bbcd95ceb11059751f608c8543e18cde7 in /home/eggdrop/eggdrop 
# Tue, 08 Aug 2023 23:40:50 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 08 Aug 2023 23:40:50 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 08 Aug 2023 23:40:50 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9aaeede874a10e7e24ee2c9685d7e8ecf762e6f7f9c3f999981af88510503d`  
		Last Modified: Tue, 08 Aug 2023 23:45:24 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f01e1410e6ccfe040fad10b90d5a18fbab52d604ee706f7f575ce708db73a6`  
		Last Modified: Tue, 08 Aug 2023 23:45:22 GMT  
		Size: 11.0 KB (10988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedb685615707e672c8cd6ca665ce8752a8f01afd159f1cd26d7e1b345b67fec`  
		Last Modified: Tue, 08 Aug 2023 23:45:22 GMT  
		Size: 1.2 MB (1203723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c844047a9b86ff8f985b01076671a69e3b5b0c3cbbfa29f9567418929e892660`  
		Last Modified: Tue, 08 Aug 2023 23:45:23 GMT  
		Size: 11.5 MB (11534569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f2073b9fd5b72b79ad87269659239fac4e3f2e70f6962469f8d72c903436f6`  
		Last Modified: Tue, 08 Aug 2023 23:45:22 GMT  
		Size: 1.9 KB (1890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5d7be0d8185b0b5c085c7ed6caa8d50445e0b28c8c7afea88130dfdd792e7c`  
		Last Modified: Tue, 08 Aug 2023 23:45:22 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:41e4e5df35d60a72f85c544b912fa003b25efd34da4bf8967db15c5d1ddbd4ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15730774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d179768c437120e8fbec88d356cb32ee59335f2faebae1bfa5b4f4a61b86d9`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:17 GMT
ADD file:cb3f59b0f701cb6ef552e7f8ada1707cf82747c95b69759924061ff9ac6dbe72 in / 
# Mon, 07 Aug 2023 19:49:18 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 22:03:22 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 07 Aug 2023 22:03:24 GMT
RUN adduser -S eggdrop
# Mon, 07 Aug 2023 22:03:26 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 07 Aug 2023 22:03:26 GMT
ENV EGGDROP_SHA256=cc7936ee427959081651319119ac0b8f3581a18d7be7b20f71023954f1f69a91
# Mon, 07 Aug 2023 22:03:26 GMT
ENV EGGDROP_COMMIT=26ecf0921ee84c5bf61cb31014a75f02670b1af4
# Mon, 07 Aug 2023 22:03:28 GMT
RUN apk --update add --no-cache bash openssl
# Mon, 07 Aug 2023 22:07:38 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 07 Aug 2023 22:07:38 GMT
ENV NICK=
# Mon, 07 Aug 2023 22:07:39 GMT
ENV SERVER=
# Mon, 07 Aug 2023 22:07:39 GMT
ENV LISTEN=3333
# Mon, 07 Aug 2023 22:07:39 GMT
ENV OWNER=
# Mon, 07 Aug 2023 22:07:39 GMT
ENV USERFILE=eggdrop.user
# Mon, 07 Aug 2023 22:07:39 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 07 Aug 2023 22:07:39 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 07 Aug 2023 22:07:39 GMT
EXPOSE 3333
# Mon, 07 Aug 2023 22:07:39 GMT
COPY file:35e05bb72116a1848ec779e3fbc4ea6bbcd95ceb11059751f608c8543e18cde7 in /home/eggdrop/eggdrop 
# Mon, 07 Aug 2023 22:07:39 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 07 Aug 2023 22:07:39 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 07 Aug 2023 22:07:40 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:342323bc858ed9706f7953ab06cbf6785b678c55ef2317577af748533d11165b`  
		Last Modified: Mon, 07 Aug 2023 19:49:53 GMT  
		Size: 3.1 MB (3112450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73efea92f6e8a5f90afe9fc6a05239a509d094c1f0b975e0218680c6c03ec5dc`  
		Last Modified: Mon, 07 Aug 2023 22:13:20 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731ba4f78dc39cdc49dcf4ee65cd93fb5b9baa662666c73d260b66b50076c639`  
		Last Modified: Mon, 07 Aug 2023 22:13:19 GMT  
		Size: 11.1 KB (11131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5149941d019a09e5ecbdeb9a8343d555097697df7fa8b2efda1f55f5f538ab75`  
		Last Modified: Mon, 07 Aug 2023 22:13:18 GMT  
		Size: 1.2 MB (1187637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911ac50cb3fe192c2eaee197dbea75fbcbaa060bb9a4fe60ea31d2f55d308b9f`  
		Last Modified: Mon, 07 Aug 2023 22:13:20 GMT  
		Size: 11.4 MB (11415326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10a8ce890dcd5d203ad1fd377d38c3d19108b5f5bbcacb68c10f03d0d55315a`  
		Last Modified: Mon, 07 Aug 2023 22:13:17 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:869cf83ebf990e2439ae4298998dbcf95f88378a5b2171b14fdd695d515b60d5`  
		Last Modified: Mon, 07 Aug 2023 22:13:18 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:21407a762f0acde4d12e90ba79a9b19779f5c7f847acc5012f3e0bb57990dbf9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16100880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d62e5cb19347bb2751ee766017d10f10e5b909ea2d27323150097427802b803`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:22 GMT
ADD file:9e054a25c83111adc857a7f988336ee40eea5e1794ed30a80d465e8d472342e2 in / 
# Mon, 07 Aug 2023 19:39:22 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:02:13 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 08 Aug 2023 23:02:13 GMT
RUN adduser -S eggdrop
# Tue, 08 Aug 2023 23:02:14 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 08 Aug 2023 23:02:14 GMT
ENV EGGDROP_SHA256=cc7936ee427959081651319119ac0b8f3581a18d7be7b20f71023954f1f69a91
# Tue, 08 Aug 2023 23:02:14 GMT
ENV EGGDROP_COMMIT=26ecf0921ee84c5bf61cb31014a75f02670b1af4
# Tue, 08 Aug 2023 23:02:15 GMT
RUN apk --update add --no-cache bash openssl
# Tue, 08 Aug 2023 23:05:26 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 08 Aug 2023 23:05:26 GMT
ENV NICK=
# Tue, 08 Aug 2023 23:05:26 GMT
ENV SERVER=
# Tue, 08 Aug 2023 23:05:26 GMT
ENV LISTEN=3333
# Tue, 08 Aug 2023 23:05:26 GMT
ENV OWNER=
# Tue, 08 Aug 2023 23:05:27 GMT
ENV USERFILE=eggdrop.user
# Tue, 08 Aug 2023 23:05:27 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 08 Aug 2023 23:05:27 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 08 Aug 2023 23:05:27 GMT
EXPOSE 3333
# Tue, 08 Aug 2023 23:05:27 GMT
COPY file:35e05bb72116a1848ec779e3fbc4ea6bbcd95ceb11059751f608c8543e18cde7 in /home/eggdrop/eggdrop 
# Tue, 08 Aug 2023 23:05:27 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 08 Aug 2023 23:05:27 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 08 Aug 2023 23:05:27 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:4060ece20d7ac783f52cbe28a35fd5b06f90f7b4d773bae0d956024e85ff35b6`  
		Last Modified: Mon, 07 Aug 2023 19:39:59 GMT  
		Size: 3.3 MB (3258290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a033905739de3b7f3a960fb5ba45fb664750e12faba0a28944f42e59c3ab8f`  
		Last Modified: Tue, 08 Aug 2023 23:09:36 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7204aa9f82607e7cc6d0ab3821040f278ae14a1330a50a40ced101ca0d16cde9`  
		Last Modified: Tue, 08 Aug 2023 23:09:34 GMT  
		Size: 11.2 KB (11192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79cc5940d404cd9dba22236d3b275a36b7fde7b1187a47ffc199baa89c64e43a`  
		Last Modified: Tue, 08 Aug 2023 23:09:35 GMT  
		Size: 1.2 MB (1234263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca645c9eed2eb8ca552ee696043b4462616f5a9f404cda5a6427f69c0b94f75`  
		Last Modified: Tue, 08 Aug 2023 23:09:36 GMT  
		Size: 11.6 MB (11592912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28d4237d5934878cbf5b7827479778730b4496b1030f308a1b4dcabfacc4849`  
		Last Modified: Tue, 08 Aug 2023 23:09:34 GMT  
		Size: 1.9 KB (1890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769d4e10682bff165ddc930d3824c3c4923ebc9075305f76392fba3f8a061c0f`  
		Last Modified: Tue, 08 Aug 2023 23:09:34 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:ce2d5608e40789dfceafed599ff7987d3e2ca5ced336e29882656a4273653ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:067001b49b16e7b2843450085e133de7119fea0ea83ece8a1fa1e228d7c60b64
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7869f72da560a9be174f98cf0682f54ae7aec597d597e57ca55596f73c1668`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:41:07 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 08 Aug 2023 23:41:07 GMT
RUN adduser -S eggdrop
# Tue, 08 Aug 2023 23:41:08 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 08 Aug 2023 23:41:09 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 08 Aug 2023 23:45:02 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 08 Aug 2023 23:45:02 GMT
ENV NICK=
# Tue, 08 Aug 2023 23:45:02 GMT
ENV SERVER=
# Tue, 08 Aug 2023 23:45:02 GMT
ENV LISTEN=3333
# Tue, 08 Aug 2023 23:45:02 GMT
ENV OWNER=
# Tue, 08 Aug 2023 23:45:02 GMT
ENV USERFILE=eggdrop.user
# Tue, 08 Aug 2023 23:45:02 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 08 Aug 2023 23:45:02 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 08 Aug 2023 23:45:03 GMT
EXPOSE 3333
# Tue, 08 Aug 2023 23:45:03 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 08 Aug 2023 23:45:03 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 08 Aug 2023 23:45:03 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 08 Aug 2023 23:45:03 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4acb10f80f9f6279e3de61139d3c6811cad56af40f95b49b65dc9f93f87916`  
		Last Modified: Tue, 08 Aug 2023 23:45:31 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f039073aec9e1300ad97f4ba8443ef0f261977135eb1c907a9c02d44b8795a7f`  
		Last Modified: Tue, 08 Aug 2023 23:45:29 GMT  
		Size: 10.9 KB (10941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fe6012fe71d2ad532da09cc225006fa5ebd6ce40673870ad2847d8cc6a9a65`  
		Last Modified: Tue, 08 Aug 2023 23:45:30 GMT  
		Size: 2.8 MB (2758095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e415f33afb0f4b927816a6df8a833544d7d23bde202f2fb405eedd7086920c32`  
		Last Modified: Tue, 08 Aug 2023 23:45:30 GMT  
		Size: 6.1 MB (6146727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2836a59010f1e0c892f072d6cb6077f8fe5439f216144ca41feb1ce9745e5b7f`  
		Last Modified: Tue, 08 Aug 2023 23:45:29 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0216508c10c8057645f42bae6e9f9f60d66c81009004994b998548a88d9903`  
		Last Modified: Tue, 08 Aug 2023 23:45:29 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:f515853a8633cc2acb2f7b272809c99fcced45d052a2e1a4abb0c3a8ba6f5832
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11363784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd681812c870f1a0dad0a33ac5d324e13e9c199c05d2b0b48c40ffd1f06541b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:20 GMT
ADD file:321b24cc0fbd39caa2d7672a740d2cd2030ba99cab16f50c22db9955bd99350b in / 
# Mon, 07 Aug 2023 19:49:20 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 22:07:45 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 07 Aug 2023 22:07:45 GMT
RUN adduser -S eggdrop
# Mon, 07 Aug 2023 22:07:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 07 Aug 2023 22:07:48 GMT
RUN apk add --no-cache tcl bash openssl
# Mon, 07 Aug 2023 22:12:58 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 07 Aug 2023 22:12:58 GMT
ENV NICK=
# Mon, 07 Aug 2023 22:12:58 GMT
ENV SERVER=
# Mon, 07 Aug 2023 22:12:58 GMT
ENV LISTEN=3333
# Mon, 07 Aug 2023 22:12:58 GMT
ENV OWNER=
# Mon, 07 Aug 2023 22:12:58 GMT
ENV USERFILE=eggdrop.user
# Mon, 07 Aug 2023 22:12:58 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 07 Aug 2023 22:12:58 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 07 Aug 2023 22:12:58 GMT
EXPOSE 3333
# Mon, 07 Aug 2023 22:12:58 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 07 Aug 2023 22:12:59 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 07 Aug 2023 22:12:59 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 07 Aug 2023 22:12:59 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:dffa980f71c953938bb194a457aa62e7f1885137331eef8bf7f9403c075f711c`  
		Last Modified: Mon, 07 Aug 2023 19:50:02 GMT  
		Size: 2.6 MB (2615553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b720555f5994efe82d1f8fa1a831f681243dab05b37ca283b93588190b20c8`  
		Last Modified: Mon, 07 Aug 2023 22:13:28 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f700305957831109bfaa5a699e5e743a7e76daf177c8f4b821ef1a3a6ab0d5cb`  
		Last Modified: Mon, 07 Aug 2023 22:13:26 GMT  
		Size: 10.6 KB (10629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01fa1c3b77ab4e8fb787f9c731ec1b11637eac08644c829fb22295bf912da747`  
		Last Modified: Mon, 07 Aug 2023 22:13:28 GMT  
		Size: 2.7 MB (2679936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7454d49e1110383afbfe9a1d9c3aa7bb95bb2394f687d3daf288d1efe2f2078e`  
		Last Modified: Mon, 07 Aug 2023 22:13:28 GMT  
		Size: 6.1 MB (6053856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab34a30dd387b3045fc7447b49799e52ed88561de2d3f56ca91a72bd3a1139d8`  
		Last Modified: Mon, 07 Aug 2023 22:13:26 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd0f9c22b9cf4325e32b32b208cb3f28946ce5eedd2346c4da6367fd436b484`  
		Last Modified: Mon, 07 Aug 2023 22:13:26 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:206d9da498c45c71109b9dd23adfc9d77d9f704f95b90da2118edf61f783ee02
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11686461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbce1c0975c3fede1fda10cf32063453feecca60130a785ebf655e6ece8197af`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:26 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 07 Aug 2023 19:39:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:05:35 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 08 Aug 2023 23:05:36 GMT
RUN adduser -S eggdrop
# Tue, 08 Aug 2023 23:05:37 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 08 Aug 2023 23:05:38 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 08 Aug 2023 23:09:15 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 08 Aug 2023 23:09:15 GMT
ENV NICK=
# Tue, 08 Aug 2023 23:09:15 GMT
ENV SERVER=
# Tue, 08 Aug 2023 23:09:15 GMT
ENV LISTEN=3333
# Tue, 08 Aug 2023 23:09:15 GMT
ENV OWNER=
# Tue, 08 Aug 2023 23:09:15 GMT
ENV USERFILE=eggdrop.user
# Tue, 08 Aug 2023 23:09:15 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 08 Aug 2023 23:09:15 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 08 Aug 2023 23:09:15 GMT
EXPOSE 3333
# Tue, 08 Aug 2023 23:09:16 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 08 Aug 2023 23:09:16 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 08 Aug 2023 23:09:16 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 08 Aug 2023 23:09:16 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6cc73b6a504f251379d7d25b533cb1b15e55ffaa00346fcffd270abbaccdf7`  
		Last Modified: Tue, 08 Aug 2023 23:09:43 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0429d00c2602fa6069fd322fc19ce26692da176bfc289d68b71a57b2ff2769`  
		Last Modified: Tue, 08 Aug 2023 23:09:41 GMT  
		Size: 10.7 KB (10748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b334d21e87707297512e175e343dd92de9023742868e23d085f1322b776adc`  
		Last Modified: Tue, 08 Aug 2023 23:09:42 GMT  
		Size: 2.8 MB (2776573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe6df62b68fb22fabd8c2ccdb8fa6025c5493621650e31cdc3f191593e631fe`  
		Last Modified: Tue, 08 Aug 2023 23:09:42 GMT  
		Size: 6.2 MB (6187306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b530eb3732a3031c16ca294daba836e6c8ae5cf0dab82e1115da5fce03ddd67`  
		Last Modified: Tue, 08 Aug 2023 23:09:41 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e69277efb4953ec23569199945650d356c677b05bb61fdbaf710a42c1c1dc2c`  
		Last Modified: Tue, 08 Aug 2023 23:09:41 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:ce2d5608e40789dfceafed599ff7987d3e2ca5ced336e29882656a4273653ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:067001b49b16e7b2843450085e133de7119fea0ea83ece8a1fa1e228d7c60b64
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7869f72da560a9be174f98cf0682f54ae7aec597d597e57ca55596f73c1668`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:41:07 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 08 Aug 2023 23:41:07 GMT
RUN adduser -S eggdrop
# Tue, 08 Aug 2023 23:41:08 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 08 Aug 2023 23:41:09 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 08 Aug 2023 23:45:02 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 08 Aug 2023 23:45:02 GMT
ENV NICK=
# Tue, 08 Aug 2023 23:45:02 GMT
ENV SERVER=
# Tue, 08 Aug 2023 23:45:02 GMT
ENV LISTEN=3333
# Tue, 08 Aug 2023 23:45:02 GMT
ENV OWNER=
# Tue, 08 Aug 2023 23:45:02 GMT
ENV USERFILE=eggdrop.user
# Tue, 08 Aug 2023 23:45:02 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 08 Aug 2023 23:45:02 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 08 Aug 2023 23:45:03 GMT
EXPOSE 3333
# Tue, 08 Aug 2023 23:45:03 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 08 Aug 2023 23:45:03 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 08 Aug 2023 23:45:03 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 08 Aug 2023 23:45:03 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4acb10f80f9f6279e3de61139d3c6811cad56af40f95b49b65dc9f93f87916`  
		Last Modified: Tue, 08 Aug 2023 23:45:31 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f039073aec9e1300ad97f4ba8443ef0f261977135eb1c907a9c02d44b8795a7f`  
		Last Modified: Tue, 08 Aug 2023 23:45:29 GMT  
		Size: 10.9 KB (10941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fe6012fe71d2ad532da09cc225006fa5ebd6ce40673870ad2847d8cc6a9a65`  
		Last Modified: Tue, 08 Aug 2023 23:45:30 GMT  
		Size: 2.8 MB (2758095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e415f33afb0f4b927816a6df8a833544d7d23bde202f2fb405eedd7086920c32`  
		Last Modified: Tue, 08 Aug 2023 23:45:30 GMT  
		Size: 6.1 MB (6146727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2836a59010f1e0c892f072d6cb6077f8fe5439f216144ca41feb1ce9745e5b7f`  
		Last Modified: Tue, 08 Aug 2023 23:45:29 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0216508c10c8057645f42bae6e9f9f60d66c81009004994b998548a88d9903`  
		Last Modified: Tue, 08 Aug 2023 23:45:29 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:f515853a8633cc2acb2f7b272809c99fcced45d052a2e1a4abb0c3a8ba6f5832
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11363784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd681812c870f1a0dad0a33ac5d324e13e9c199c05d2b0b48c40ffd1f06541b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:20 GMT
ADD file:321b24cc0fbd39caa2d7672a740d2cd2030ba99cab16f50c22db9955bd99350b in / 
# Mon, 07 Aug 2023 19:49:20 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 22:07:45 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Mon, 07 Aug 2023 22:07:45 GMT
RUN adduser -S eggdrop
# Mon, 07 Aug 2023 22:07:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 07 Aug 2023 22:07:48 GMT
RUN apk add --no-cache tcl bash openssl
# Mon, 07 Aug 2023 22:12:58 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Mon, 07 Aug 2023 22:12:58 GMT
ENV NICK=
# Mon, 07 Aug 2023 22:12:58 GMT
ENV SERVER=
# Mon, 07 Aug 2023 22:12:58 GMT
ENV LISTEN=3333
# Mon, 07 Aug 2023 22:12:58 GMT
ENV OWNER=
# Mon, 07 Aug 2023 22:12:58 GMT
ENV USERFILE=eggdrop.user
# Mon, 07 Aug 2023 22:12:58 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 07 Aug 2023 22:12:58 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 07 Aug 2023 22:12:58 GMT
EXPOSE 3333
# Mon, 07 Aug 2023 22:12:58 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Mon, 07 Aug 2023 22:12:59 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Mon, 07 Aug 2023 22:12:59 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 07 Aug 2023 22:12:59 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:dffa980f71c953938bb194a457aa62e7f1885137331eef8bf7f9403c075f711c`  
		Last Modified: Mon, 07 Aug 2023 19:50:02 GMT  
		Size: 2.6 MB (2615553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b720555f5994efe82d1f8fa1a831f681243dab05b37ca283b93588190b20c8`  
		Last Modified: Mon, 07 Aug 2023 22:13:28 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f700305957831109bfaa5a699e5e743a7e76daf177c8f4b821ef1a3a6ab0d5cb`  
		Last Modified: Mon, 07 Aug 2023 22:13:26 GMT  
		Size: 10.6 KB (10629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01fa1c3b77ab4e8fb787f9c731ec1b11637eac08644c829fb22295bf912da747`  
		Last Modified: Mon, 07 Aug 2023 22:13:28 GMT  
		Size: 2.7 MB (2679936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7454d49e1110383afbfe9a1d9c3aa7bb95bb2394f687d3daf288d1efe2f2078e`  
		Last Modified: Mon, 07 Aug 2023 22:13:28 GMT  
		Size: 6.1 MB (6053856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab34a30dd387b3045fc7447b49799e52ed88561de2d3f56ca91a72bd3a1139d8`  
		Last Modified: Mon, 07 Aug 2023 22:13:26 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd0f9c22b9cf4325e32b32b208cb3f28946ce5eedd2346c4da6367fd436b484`  
		Last Modified: Mon, 07 Aug 2023 22:13:26 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:206d9da498c45c71109b9dd23adfc9d77d9f704f95b90da2118edf61f783ee02
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11686461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbce1c0975c3fede1fda10cf32063453feecca60130a785ebf655e6ece8197af`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:26 GMT
ADD file:cf85500a1f5b87a88587b279c8b8018eebeb3092f402b7e2cc4ad3873e078580 in / 
# Mon, 07 Aug 2023 19:39:26 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:05:35 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 08 Aug 2023 23:05:36 GMT
RUN adduser -S eggdrop
# Tue, 08 Aug 2023 23:05:37 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 08 Aug 2023 23:05:38 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 08 Aug 2023 23:09:15 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 08 Aug 2023 23:09:15 GMT
ENV NICK=
# Tue, 08 Aug 2023 23:09:15 GMT
ENV SERVER=
# Tue, 08 Aug 2023 23:09:15 GMT
ENV LISTEN=3333
# Tue, 08 Aug 2023 23:09:15 GMT
ENV OWNER=
# Tue, 08 Aug 2023 23:09:15 GMT
ENV USERFILE=eggdrop.user
# Tue, 08 Aug 2023 23:09:15 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 08 Aug 2023 23:09:15 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 08 Aug 2023 23:09:15 GMT
EXPOSE 3333
# Tue, 08 Aug 2023 23:09:16 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 08 Aug 2023 23:09:16 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 08 Aug 2023 23:09:16 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 08 Aug 2023 23:09:16 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:bdb2de7ba06c3a4e10b98f439a8c70afd63eee492c2ddc32342331a8e9ef4ff7`  
		Last Modified: Mon, 07 Aug 2023 19:40:08 GMT  
		Size: 2.7 MB (2708023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6cc73b6a504f251379d7d25b533cb1b15e55ffaa00346fcffd270abbaccdf7`  
		Last Modified: Tue, 08 Aug 2023 23:09:43 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0429d00c2602fa6069fd322fc19ce26692da176bfc289d68b71a57b2ff2769`  
		Last Modified: Tue, 08 Aug 2023 23:09:41 GMT  
		Size: 10.7 KB (10748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b334d21e87707297512e175e343dd92de9023742868e23d085f1322b776adc`  
		Last Modified: Tue, 08 Aug 2023 23:09:42 GMT  
		Size: 2.8 MB (2776573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe6df62b68fb22fabd8c2ccdb8fa6025c5493621650e31cdc3f191593e631fe`  
		Last Modified: Tue, 08 Aug 2023 23:09:42 GMT  
		Size: 6.2 MB (6187306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b530eb3732a3031c16ca294daba836e6c8ae5cf0dab82e1115da5fce03ddd67`  
		Last Modified: Tue, 08 Aug 2023 23:09:41 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e69277efb4953ec23569199945650d356c677b05bb61fdbaf710a42c1c1dc2c`  
		Last Modified: Tue, 08 Aug 2023 23:09:41 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
