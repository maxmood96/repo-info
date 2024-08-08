<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.10.0rc1`](#eggdrop1100rc1)
-	[`eggdrop:1.9`](#eggdrop19)
-	[`eggdrop:1.9.5`](#eggdrop195)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.10.0rc1`

```console
$ docker pull eggdrop@sha256:046e23d30dc8de769ddd24160927f6f123786d1f0b641139ebdbafd9d3cde772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.10.0rc1` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:4a11af1dd3659cbafdb8247eda2d12ed54f07e2564e6906b97a701121bc39655
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17053042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4d1f52936e7aafc2a71864bc756ce4b682a067d528b40f2a21f2a2e743b9bf`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 19:51:31 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Thu, 08 Aug 2024 19:51:33 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Thu, 08 Aug 2024 19:51:35 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Thu, 08 Aug 2024 20:02:36 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0rc1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0rc1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0rc1.tar.gz.asc eggdrop-1.10.0rc1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0rc1.tar.gz.asc   && tar -zxvf eggdrop-1.10.0rc1.tar.gz   && rm eggdrop-1.10.0rc1.tar.gz   && ( cd eggdrop-1.10.0rc1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10rc1.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Thu, 08 Aug 2024 20:02:37 GMT
ENV NICK=
# Thu, 08 Aug 2024 20:02:37 GMT
ENV SERVER=
# Thu, 08 Aug 2024 20:02:37 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 20:02:37 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 20:02:37 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 20:02:37 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 20:02:37 GMT
EXPOSE 3333
# Thu, 08 Aug 2024 20:02:38 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Thu, 08 Aug 2024 20:02:38 GMT
COPY file:61da6bdf6e84c41c8486cddfad6cc1d25ced9bbeaa056bab87034428f2134436 in ./scripts/ 
# Thu, 08 Aug 2024 20:02:38 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 20:02:38 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade96c498913dfb986e395fa5b382c7643627c76acf91dc28bfd94b61bfdbda1`  
		Last Modified: Thu, 08 Aug 2024 20:02:47 GMT  
		Size: 967.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db39b8b10cbe820079ef063c33200dfba1b45391bc84208ff5290cfca48a06ed`  
		Last Modified: Thu, 08 Aug 2024 20:02:47 GMT  
		Size: 1.1 MB (1129499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6ebeff96c99f90f244ad65113302001ada6d5d2a8bc8b520555e6f94644820`  
		Last Modified: Thu, 08 Aug 2024 20:03:11 GMT  
		Size: 12.6 MB (12554301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd74c5485ba67f2a17d6399db89b6d5a622a4a1aa0e53a9cc5632699f67eec9b`  
		Last Modified: Thu, 08 Aug 2024 20:03:08 GMT  
		Size: 2.0 KB (1957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ef357e10730167ee4890d8d16c3bc831e811fb331cba6a7220f3003b45595a`  
		Last Modified: Thu, 08 Aug 2024 20:03:08 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.10.0rc1` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:46ea6d2c159b3b9bc6f3128655a67bc7fd717768635c20eca2842de432d6057c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18151504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea179d9eee100a0012f2ef16e8dc6728b333f11c4d67256b4641d13a177238f7`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 19:43:37 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Thu, 08 Aug 2024 19:43:38 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Thu, 08 Aug 2024 19:43:39 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Thu, 08 Aug 2024 19:51:30 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0rc1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0rc1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0rc1.tar.gz.asc eggdrop-1.10.0rc1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0rc1.tar.gz.asc   && tar -zxvf eggdrop-1.10.0rc1.tar.gz   && rm eggdrop-1.10.0rc1.tar.gz   && ( cd eggdrop-1.10.0rc1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10rc1.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Thu, 08 Aug 2024 19:51:30 GMT
ENV NICK=
# Thu, 08 Aug 2024 19:51:30 GMT
ENV SERVER=
# Thu, 08 Aug 2024 19:51:30 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 19:51:30 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 19:51:30 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 19:51:30 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 19:51:31 GMT
EXPOSE 3333
# Thu, 08 Aug 2024 19:51:31 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Thu, 08 Aug 2024 19:51:31 GMT
COPY file:61da6bdf6e84c41c8486cddfad6cc1d25ced9bbeaa056bab87034428f2134436 in ./scripts/ 
# Thu, 08 Aug 2024 19:51:31 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 19:51:31 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df1fbd90925124f99f470d0e8fb64bb807608c5c0bbe563414aaec386a6b0ca`  
		Last Modified: Thu, 08 Aug 2024 19:51:52 GMT  
		Size: 966.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1131de528037c7182c2a886926b7114abcc3062bddced8c87d376e2afe96a63`  
		Last Modified: Thu, 08 Aug 2024 19:51:53 GMT  
		Size: 1.2 MB (1210745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be04448f413a85c8ce43c1d1c20b472d29e43641fce6d89a581cef503000c96`  
		Last Modified: Thu, 08 Aug 2024 19:52:17 GMT  
		Size: 12.8 MB (12849778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15eef4afabf88334bfa97a962b51f53fa76289169d4482bedb76dab3204718f`  
		Last Modified: Thu, 08 Aug 2024 19:52:15 GMT  
		Size: 2.0 KB (1954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b21e083e2d9b1229a3690ffa8d4c5a42ac50664a7dd6bfd72c10e09033a83f7`  
		Last Modified: Thu, 08 Aug 2024 19:52:15 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.9`

```console
$ docker pull eggdrop@sha256:e1a0ca3770caa65b8a9e485546599c450760c1365374fb7e1cb416557e25db80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9` - linux; amd64

```console
$ docker pull eggdrop@sha256:34a38b278b4fe46c1b431fcf7dfa6cbac1615246172272129b9208d0d2fa8bd4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680b372bebae349d2d30d7d1885053541c90be76f8b4cc32415f7d940836dc13`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:14:11 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 16 Mar 2024 06:14:11 GMT
RUN adduser -S eggdrop
# Sat, 16 Mar 2024 06:14:13 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 16 Mar 2024 06:14:14 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 16 Mar 2024 06:18:03 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 16 Mar 2024 06:18:03 GMT
ENV NICK=
# Sat, 16 Mar 2024 06:18:03 GMT
ENV SERVER=
# Sat, 16 Mar 2024 06:18:03 GMT
ENV LISTEN=3333
# Sat, 16 Mar 2024 06:18:03 GMT
ENV OWNER=
# Sat, 16 Mar 2024 06:18:03 GMT
ENV USERFILE=eggdrop.user
# Sat, 16 Mar 2024 06:18:03 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 16 Mar 2024 06:18:03 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 16 Mar 2024 06:18:03 GMT
EXPOSE 3333
# Sat, 16 Mar 2024 06:18:04 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 16 Mar 2024 06:18:04 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 16 Mar 2024 06:18:04 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 16 Mar 2024 06:18:04 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c630ff352121cf34896e97408532ee11e27a42505c86d429d155280ccb8002`  
		Last Modified: Sat, 16 Mar 2024 06:18:34 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb419fa2bf132049b023b1393209d0b8836e6a7598b618c2dbee91036dc922f7`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 11.0 KB (10954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b4a85b3c8cbd4a52ab562b3e5909758273e37b541cdc144e2a07fc4a329f84`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 2.8 MB (2758094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91429a382ad8f8d515a3269ac11d856c4a69a1062217035b56747b603c5fd9b3`  
		Last Modified: Sat, 16 Mar 2024 06:18:34 GMT  
		Size: 6.1 MB (6146820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c61fc1b45ec89476a85feefd5ae3515f358e5255fc53b9611732f34f49355`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe2aee5f06911bbd805d8dc9d6beedd17ff7a25f96fbb1dc1ba70732675d433`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:d54fdfd8b26fb5b0f8b7500a4d1ad7c3ffa2e42c22a13803a8211a7471885a04
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11954276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f378228fee0077f2c893c1a7f54eb600597161946e443375418ce0b6cc299f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:22 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
# Mon, 22 Jul 2024 21:49:22 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 19:54:54 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 19:54:55 GMT
RUN adduser -S eggdrop
# Thu, 08 Aug 2024 19:54:56 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 08 Aug 2024 19:54:58 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 08 Aug 2024 19:59:38 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 08 Aug 2024 19:59:38 GMT
ENV NICK=
# Thu, 08 Aug 2024 19:59:38 GMT
ENV SERVER=
# Thu, 08 Aug 2024 19:59:39 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 19:59:39 GMT
ENV OWNER=
# Thu, 08 Aug 2024 19:59:39 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 19:59:39 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 19:59:39 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 19:59:39 GMT
EXPOSE 3333
# Thu, 08 Aug 2024 19:59:39 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 08 Aug 2024 19:59:39 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 08 Aug 2024 19:59:40 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 19:59:40 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:25b28a78657effc87fccb3820a41450134ddcdbea210294d5b989ee0f09c0563`  
		Last Modified: Mon, 22 Jul 2024 21:49:53 GMT  
		Size: 3.2 MB (3175673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce1736469a094d3fea3178e545181d8c90b7f519a24e40834d20196aeecf493`  
		Last Modified: Thu, 08 Aug 2024 20:02:56 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b0bd5169afbdebbcbe59c1a8999d4f702e7c96753a8a9224271038b0efc5f4`  
		Last Modified: Thu, 08 Aug 2024 20:02:54 GMT  
		Size: 11.0 KB (11009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f753a90e840abe1598071e0e8575bfb9a56d4b638e492a9d533a787764424715`  
		Last Modified: Thu, 08 Aug 2024 20:02:55 GMT  
		Size: 2.9 MB (2904462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8dfcdf07d0444df1253fdec5e3655f16380890afb4f20871122d88ed855b77e`  
		Last Modified: Thu, 08 Aug 2024 20:02:55 GMT  
		Size: 5.9 MB (5859352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805e6d65553da001602486202abb7c08f1b23065651b0b09095d997694e2354c`  
		Last Modified: Thu, 08 Aug 2024 20:02:54 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b47463063d2c9865c7a9c41b59750bddb780891be5947eb3f0a73318cadfc9`  
		Last Modified: Thu, 08 Aug 2024 20:02:54 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:64166b3cf2df01a17e431db880b621810acda5b0fd0ddbba6ba59105e2b82fd8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12424083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d293d71c94643df7ec3252594eca670575e13b9d2d9c0bf18a71aea03b02a8d`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 19:45:45 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 19:45:45 GMT
RUN adduser -S eggdrop
# Thu, 08 Aug 2024 19:45:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 08 Aug 2024 19:45:48 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 08 Aug 2024 19:49:18 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 08 Aug 2024 19:49:18 GMT
ENV NICK=
# Thu, 08 Aug 2024 19:49:18 GMT
ENV SERVER=
# Thu, 08 Aug 2024 19:49:18 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 19:49:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 19:49:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 19:49:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 19:49:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 19:49:19 GMT
EXPOSE 3333
# Thu, 08 Aug 2024 19:49:19 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 08 Aug 2024 19:49:19 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 08 Aug 2024 19:49:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 19:49:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3af4066f123f44c2fb98e2f28964f982bc14db4ba15906ad8cc3887a867266`  
		Last Modified: Thu, 08 Aug 2024 19:52:03 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ccffd445d45c37456f285a0ce2105caf980a691a88a750da9d0b219b008a86`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 11.4 KB (11395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0587e228beafa54aa50b93967977861c70914e0ddedcd401e31b42fd0c0e733`  
		Last Modified: Thu, 08 Aug 2024 19:52:02 GMT  
		Size: 3.0 MB (3034852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0dfbf35befd934b3269c7f9f9c391974da4d1dca33f36515bd2dfa7352f5d1e`  
		Last Modified: Thu, 08 Aug 2024 19:52:02 GMT  
		Size: 6.0 MB (6015601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d6a4d43f2f43e12cbd85ae7f616403e0c64a507c111410e4fa39fb99153592`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae77733354b0d53d2c6134cf545bf14ed540dec92c819344b15a4ab36c0a228c`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.9.5`

```console
$ docker pull eggdrop@sha256:e1a0ca3770caa65b8a9e485546599c450760c1365374fb7e1cb416557e25db80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9.5` - linux; amd64

```console
$ docker pull eggdrop@sha256:34a38b278b4fe46c1b431fcf7dfa6cbac1615246172272129b9208d0d2fa8bd4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680b372bebae349d2d30d7d1885053541c90be76f8b4cc32415f7d940836dc13`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:14:11 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 16 Mar 2024 06:14:11 GMT
RUN adduser -S eggdrop
# Sat, 16 Mar 2024 06:14:13 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 16 Mar 2024 06:14:14 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 16 Mar 2024 06:18:03 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 16 Mar 2024 06:18:03 GMT
ENV NICK=
# Sat, 16 Mar 2024 06:18:03 GMT
ENV SERVER=
# Sat, 16 Mar 2024 06:18:03 GMT
ENV LISTEN=3333
# Sat, 16 Mar 2024 06:18:03 GMT
ENV OWNER=
# Sat, 16 Mar 2024 06:18:03 GMT
ENV USERFILE=eggdrop.user
# Sat, 16 Mar 2024 06:18:03 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 16 Mar 2024 06:18:03 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 16 Mar 2024 06:18:03 GMT
EXPOSE 3333
# Sat, 16 Mar 2024 06:18:04 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 16 Mar 2024 06:18:04 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 16 Mar 2024 06:18:04 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 16 Mar 2024 06:18:04 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c630ff352121cf34896e97408532ee11e27a42505c86d429d155280ccb8002`  
		Last Modified: Sat, 16 Mar 2024 06:18:34 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb419fa2bf132049b023b1393209d0b8836e6a7598b618c2dbee91036dc922f7`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 11.0 KB (10954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b4a85b3c8cbd4a52ab562b3e5909758273e37b541cdc144e2a07fc4a329f84`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 2.8 MB (2758094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91429a382ad8f8d515a3269ac11d856c4a69a1062217035b56747b603c5fd9b3`  
		Last Modified: Sat, 16 Mar 2024 06:18:34 GMT  
		Size: 6.1 MB (6146820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c61fc1b45ec89476a85feefd5ae3515f358e5255fc53b9611732f34f49355`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe2aee5f06911bbd805d8dc9d6beedd17ff7a25f96fbb1dc1ba70732675d433`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.5` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:d54fdfd8b26fb5b0f8b7500a4d1ad7c3ffa2e42c22a13803a8211a7471885a04
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11954276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f378228fee0077f2c893c1a7f54eb600597161946e443375418ce0b6cc299f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:22 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
# Mon, 22 Jul 2024 21:49:22 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 19:54:54 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 19:54:55 GMT
RUN adduser -S eggdrop
# Thu, 08 Aug 2024 19:54:56 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 08 Aug 2024 19:54:58 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 08 Aug 2024 19:59:38 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 08 Aug 2024 19:59:38 GMT
ENV NICK=
# Thu, 08 Aug 2024 19:59:38 GMT
ENV SERVER=
# Thu, 08 Aug 2024 19:59:39 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 19:59:39 GMT
ENV OWNER=
# Thu, 08 Aug 2024 19:59:39 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 19:59:39 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 19:59:39 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 19:59:39 GMT
EXPOSE 3333
# Thu, 08 Aug 2024 19:59:39 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 08 Aug 2024 19:59:39 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 08 Aug 2024 19:59:40 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 19:59:40 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:25b28a78657effc87fccb3820a41450134ddcdbea210294d5b989ee0f09c0563`  
		Last Modified: Mon, 22 Jul 2024 21:49:53 GMT  
		Size: 3.2 MB (3175673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce1736469a094d3fea3178e545181d8c90b7f519a24e40834d20196aeecf493`  
		Last Modified: Thu, 08 Aug 2024 20:02:56 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b0bd5169afbdebbcbe59c1a8999d4f702e7c96753a8a9224271038b0efc5f4`  
		Last Modified: Thu, 08 Aug 2024 20:02:54 GMT  
		Size: 11.0 KB (11009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f753a90e840abe1598071e0e8575bfb9a56d4b638e492a9d533a787764424715`  
		Last Modified: Thu, 08 Aug 2024 20:02:55 GMT  
		Size: 2.9 MB (2904462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8dfcdf07d0444df1253fdec5e3655f16380890afb4f20871122d88ed855b77e`  
		Last Modified: Thu, 08 Aug 2024 20:02:55 GMT  
		Size: 5.9 MB (5859352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805e6d65553da001602486202abb7c08f1b23065651b0b09095d997694e2354c`  
		Last Modified: Thu, 08 Aug 2024 20:02:54 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b47463063d2c9865c7a9c41b59750bddb780891be5947eb3f0a73318cadfc9`  
		Last Modified: Thu, 08 Aug 2024 20:02:54 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.5` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:64166b3cf2df01a17e431db880b621810acda5b0fd0ddbba6ba59105e2b82fd8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12424083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d293d71c94643df7ec3252594eca670575e13b9d2d9c0bf18a71aea03b02a8d`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 19:45:45 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 19:45:45 GMT
RUN adduser -S eggdrop
# Thu, 08 Aug 2024 19:45:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 08 Aug 2024 19:45:48 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 08 Aug 2024 19:49:18 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 08 Aug 2024 19:49:18 GMT
ENV NICK=
# Thu, 08 Aug 2024 19:49:18 GMT
ENV SERVER=
# Thu, 08 Aug 2024 19:49:18 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 19:49:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 19:49:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 19:49:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 19:49:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 19:49:19 GMT
EXPOSE 3333
# Thu, 08 Aug 2024 19:49:19 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 08 Aug 2024 19:49:19 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 08 Aug 2024 19:49:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 19:49:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3af4066f123f44c2fb98e2f28964f982bc14db4ba15906ad8cc3887a867266`  
		Last Modified: Thu, 08 Aug 2024 19:52:03 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ccffd445d45c37456f285a0ce2105caf980a691a88a750da9d0b219b008a86`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 11.4 KB (11395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0587e228beafa54aa50b93967977861c70914e0ddedcd401e31b42fd0c0e733`  
		Last Modified: Thu, 08 Aug 2024 19:52:02 GMT  
		Size: 3.0 MB (3034852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0dfbf35befd934b3269c7f9f9c391974da4d1dca33f36515bd2dfa7352f5d1e`  
		Last Modified: Thu, 08 Aug 2024 19:52:02 GMT  
		Size: 6.0 MB (6015601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d6a4d43f2f43e12cbd85ae7f616403e0c64a507c111410e4fa39fb99153592`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae77733354b0d53d2c6134cf545bf14ed540dec92c819344b15a4ab36c0a228c`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:bbcf5479a48fc70107616ffc0edbfd529efddd55ef0bb4ec2255808f321b66ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:4ff039e7347479155dcbb356e60ccee0969d191c1aee7ea36a727ef625b59808
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16108085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739666adc38b1d5874afc1e79543c1c2ce1d0a2e61b3868a3df5d13e65c25846`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:14:34 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Tue, 23 Jul 2024 01:14:34 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Tue, 23 Jul 2024 01:14:35 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Tue, 23 Jul 2024 01:14:35 GMT
ENV EGGDROP_SHA256=a46bf0e77ed2af907fe6e15b77bddf0c55706258070a05c92810e0bd40a1fe3b
# Tue, 23 Jul 2024 01:14:36 GMT
ENV EGGDROP_COMMIT=4703f71067437c361ca8d5c8c4a09d41561a7a20
# Tue, 23 Jul 2024 01:17:04 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Tue, 23 Jul 2024 01:17:04 GMT
ENV NICK=
# Tue, 23 Jul 2024 01:17:04 GMT
ENV SERVER=
# Tue, 23 Jul 2024 01:17:04 GMT
ENV LISTEN=3333
# Tue, 23 Jul 2024 01:17:04 GMT
ENV USERFILE=eggdrop.user
# Tue, 23 Jul 2024 01:17:04 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 23 Jul 2024 01:17:04 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 23 Jul 2024 01:17:05 GMT
EXPOSE 3333
# Tue, 23 Jul 2024 01:17:05 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Tue, 23 Jul 2024 01:17:05 GMT
COPY file:61da6bdf6e84c41c8486cddfad6cc1d25ced9bbeaa056bab87034428f2134436 in ./scripts/ 
# Tue, 23 Jul 2024 01:17:05 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 23 Jul 2024 01:17:05 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76676b69518c6efca4698061dd85921fa4b82abfd718819b2379346874576504`  
		Last Modified: Tue, 23 Jul 2024 01:17:20 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b8fb66c352b36ad7b77b0db44b347f8586829c1a847a2b6cab6d45ef8f15ea`  
		Last Modified: Tue, 23 Jul 2024 01:17:21 GMT  
		Size: 1.1 MB (1093083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2facaf68288bb827b3dd056e411ecada7bbf8353497fb54cc48147632ac6483f`  
		Last Modified: Tue, 23 Jul 2024 01:17:22 GMT  
		Size: 11.6 MB (11591634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b435550e9b2c8c56169fc934af485352e493d666f43ca8796888f96d73a0d698`  
		Last Modified: Tue, 23 Jul 2024 01:17:20 GMT  
		Size: 2.0 KB (1955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d7620cb520a2ef6258d1834d3a13f182e710cc3cb5c0a6454556310ea5f446`  
		Last Modified: Tue, 23 Jul 2024 01:17:20 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:f286c4877ad2d20067287ce7737eff999faaacd2b5f588b39762aa0eb6b43cfa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15979212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e04801fecad6c737092d0126e52640454b7851bdd7d185f260f0be85fd49b53e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 19:51:31 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Thu, 08 Aug 2024 19:51:33 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Thu, 08 Aug 2024 19:51:35 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Thu, 08 Aug 2024 19:51:35 GMT
ENV EGGDROP_SHA256=d185512ad282aeee49a75328e847f604c762e94be19fb1e01a7e8a4f927730b8
# Thu, 08 Aug 2024 19:51:36 GMT
ENV EGGDROP_COMMIT=f80f8ae468fd7bcec83407134ef5941225131104
# Thu, 08 Aug 2024 19:54:50 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Thu, 08 Aug 2024 19:54:50 GMT
ENV NICK=
# Thu, 08 Aug 2024 19:54:51 GMT
ENV SERVER=
# Thu, 08 Aug 2024 19:54:51 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 19:54:51 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 19:54:51 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 19:54:51 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 19:54:51 GMT
EXPOSE 3333
# Thu, 08 Aug 2024 19:54:51 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Thu, 08 Aug 2024 19:54:51 GMT
COPY file:61da6bdf6e84c41c8486cddfad6cc1d25ced9bbeaa056bab87034428f2134436 in ./scripts/ 
# Thu, 08 Aug 2024 19:54:51 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 19:54:52 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade96c498913dfb986e395fa5b382c7643627c76acf91dc28bfd94b61bfdbda1`  
		Last Modified: Thu, 08 Aug 2024 20:02:47 GMT  
		Size: 967.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db39b8b10cbe820079ef063c33200dfba1b45391bc84208ff5290cfca48a06ed`  
		Last Modified: Thu, 08 Aug 2024 20:02:47 GMT  
		Size: 1.1 MB (1129499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8b508fe0cf020d7ecc788220ea62cc0fa523c49656cc03cf25b55c88aefbcf`  
		Last Modified: Thu, 08 Aug 2024 20:02:49 GMT  
		Size: 11.5 MB (11480475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592ce2f158695962f3c8d126daed3dc572fe2f2ed3204945d45160b830d010ba`  
		Last Modified: Thu, 08 Aug 2024 20:02:47 GMT  
		Size: 2.0 KB (1955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121ef4537f6329562260380c3b604f446f433e3219a4c446565041b45c5804db`  
		Last Modified: Thu, 08 Aug 2024 20:02:47 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:1bde69ebc16112c43db8461ea3bc2cf30733f3eba70de7c41b33b5e1a03bee8c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17001287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e8ef8aaf5fbaf76e979d266a2e91750a75987f53ff256e440f1006fddad8e6`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 19:43:37 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Thu, 08 Aug 2024 19:43:38 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Thu, 08 Aug 2024 19:43:39 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Thu, 08 Aug 2024 19:43:39 GMT
ENV EGGDROP_SHA256=d185512ad282aeee49a75328e847f604c762e94be19fb1e01a7e8a4f927730b8
# Thu, 08 Aug 2024 19:43:39 GMT
ENV EGGDROP_COMMIT=f80f8ae468fd7bcec83407134ef5941225131104
# Thu, 08 Aug 2024 19:45:35 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Thu, 08 Aug 2024 19:45:35 GMT
ENV NICK=
# Thu, 08 Aug 2024 19:45:35 GMT
ENV SERVER=
# Thu, 08 Aug 2024 19:45:35 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 19:45:35 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 19:45:36 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 19:45:36 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 19:45:36 GMT
EXPOSE 3333
# Thu, 08 Aug 2024 19:45:36 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Thu, 08 Aug 2024 19:45:36 GMT
COPY file:61da6bdf6e84c41c8486cddfad6cc1d25ced9bbeaa056bab87034428f2134436 in ./scripts/ 
# Thu, 08 Aug 2024 19:45:36 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 19:45:36 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df1fbd90925124f99f470d0e8fb64bb807608c5c0bbe563414aaec386a6b0ca`  
		Last Modified: Thu, 08 Aug 2024 19:51:52 GMT  
		Size: 966.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1131de528037c7182c2a886926b7114abcc3062bddced8c87d376e2afe96a63`  
		Last Modified: Thu, 08 Aug 2024 19:51:53 GMT  
		Size: 1.2 MB (1210745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbb79da626c1f3ac029f6f510202afe3435f1ad9e5dd1d6f6b18fa19486b1e7`  
		Last Modified: Thu, 08 Aug 2024 19:51:54 GMT  
		Size: 11.7 MB (11699558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdcfdbffa5694231ca240b034fe2db03102fe20212c6622321f33a630af3b03`  
		Last Modified: Thu, 08 Aug 2024 19:51:52 GMT  
		Size: 2.0 KB (1956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7806ead3de8a9b031855581e4f6c95dc82835fc6dce8e32eb5f07e9f3ceae506`  
		Last Modified: Thu, 08 Aug 2024 19:51:52 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:e1a0ca3770caa65b8a9e485546599c450760c1365374fb7e1cb416557e25db80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:34a38b278b4fe46c1b431fcf7dfa6cbac1615246172272129b9208d0d2fa8bd4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680b372bebae349d2d30d7d1885053541c90be76f8b4cc32415f7d940836dc13`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:14:11 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 16 Mar 2024 06:14:11 GMT
RUN adduser -S eggdrop
# Sat, 16 Mar 2024 06:14:13 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 16 Mar 2024 06:14:14 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 16 Mar 2024 06:18:03 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 16 Mar 2024 06:18:03 GMT
ENV NICK=
# Sat, 16 Mar 2024 06:18:03 GMT
ENV SERVER=
# Sat, 16 Mar 2024 06:18:03 GMT
ENV LISTEN=3333
# Sat, 16 Mar 2024 06:18:03 GMT
ENV OWNER=
# Sat, 16 Mar 2024 06:18:03 GMT
ENV USERFILE=eggdrop.user
# Sat, 16 Mar 2024 06:18:03 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 16 Mar 2024 06:18:03 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 16 Mar 2024 06:18:03 GMT
EXPOSE 3333
# Sat, 16 Mar 2024 06:18:04 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 16 Mar 2024 06:18:04 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 16 Mar 2024 06:18:04 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 16 Mar 2024 06:18:04 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c630ff352121cf34896e97408532ee11e27a42505c86d429d155280ccb8002`  
		Last Modified: Sat, 16 Mar 2024 06:18:34 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb419fa2bf132049b023b1393209d0b8836e6a7598b618c2dbee91036dc922f7`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 11.0 KB (10954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b4a85b3c8cbd4a52ab562b3e5909758273e37b541cdc144e2a07fc4a329f84`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 2.8 MB (2758094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91429a382ad8f8d515a3269ac11d856c4a69a1062217035b56747b603c5fd9b3`  
		Last Modified: Sat, 16 Mar 2024 06:18:34 GMT  
		Size: 6.1 MB (6146820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c61fc1b45ec89476a85feefd5ae3515f358e5255fc53b9611732f34f49355`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe2aee5f06911bbd805d8dc9d6beedd17ff7a25f96fbb1dc1ba70732675d433`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:d54fdfd8b26fb5b0f8b7500a4d1ad7c3ffa2e42c22a13803a8211a7471885a04
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11954276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f378228fee0077f2c893c1a7f54eb600597161946e443375418ce0b6cc299f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:22 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
# Mon, 22 Jul 2024 21:49:22 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 19:54:54 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 19:54:55 GMT
RUN adduser -S eggdrop
# Thu, 08 Aug 2024 19:54:56 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 08 Aug 2024 19:54:58 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 08 Aug 2024 19:59:38 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 08 Aug 2024 19:59:38 GMT
ENV NICK=
# Thu, 08 Aug 2024 19:59:38 GMT
ENV SERVER=
# Thu, 08 Aug 2024 19:59:39 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 19:59:39 GMT
ENV OWNER=
# Thu, 08 Aug 2024 19:59:39 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 19:59:39 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 19:59:39 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 19:59:39 GMT
EXPOSE 3333
# Thu, 08 Aug 2024 19:59:39 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 08 Aug 2024 19:59:39 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 08 Aug 2024 19:59:40 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 19:59:40 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:25b28a78657effc87fccb3820a41450134ddcdbea210294d5b989ee0f09c0563`  
		Last Modified: Mon, 22 Jul 2024 21:49:53 GMT  
		Size: 3.2 MB (3175673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce1736469a094d3fea3178e545181d8c90b7f519a24e40834d20196aeecf493`  
		Last Modified: Thu, 08 Aug 2024 20:02:56 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b0bd5169afbdebbcbe59c1a8999d4f702e7c96753a8a9224271038b0efc5f4`  
		Last Modified: Thu, 08 Aug 2024 20:02:54 GMT  
		Size: 11.0 KB (11009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f753a90e840abe1598071e0e8575bfb9a56d4b638e492a9d533a787764424715`  
		Last Modified: Thu, 08 Aug 2024 20:02:55 GMT  
		Size: 2.9 MB (2904462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8dfcdf07d0444df1253fdec5e3655f16380890afb4f20871122d88ed855b77e`  
		Last Modified: Thu, 08 Aug 2024 20:02:55 GMT  
		Size: 5.9 MB (5859352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805e6d65553da001602486202abb7c08f1b23065651b0b09095d997694e2354c`  
		Last Modified: Thu, 08 Aug 2024 20:02:54 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b47463063d2c9865c7a9c41b59750bddb780891be5947eb3f0a73318cadfc9`  
		Last Modified: Thu, 08 Aug 2024 20:02:54 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:64166b3cf2df01a17e431db880b621810acda5b0fd0ddbba6ba59105e2b82fd8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12424083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d293d71c94643df7ec3252594eca670575e13b9d2d9c0bf18a71aea03b02a8d`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 19:45:45 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 19:45:45 GMT
RUN adduser -S eggdrop
# Thu, 08 Aug 2024 19:45:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 08 Aug 2024 19:45:48 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 08 Aug 2024 19:49:18 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 08 Aug 2024 19:49:18 GMT
ENV NICK=
# Thu, 08 Aug 2024 19:49:18 GMT
ENV SERVER=
# Thu, 08 Aug 2024 19:49:18 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 19:49:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 19:49:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 19:49:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 19:49:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 19:49:19 GMT
EXPOSE 3333
# Thu, 08 Aug 2024 19:49:19 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 08 Aug 2024 19:49:19 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 08 Aug 2024 19:49:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 19:49:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3af4066f123f44c2fb98e2f28964f982bc14db4ba15906ad8cc3887a867266`  
		Last Modified: Thu, 08 Aug 2024 19:52:03 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ccffd445d45c37456f285a0ce2105caf980a691a88a750da9d0b219b008a86`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 11.4 KB (11395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0587e228beafa54aa50b93967977861c70914e0ddedcd401e31b42fd0c0e733`  
		Last Modified: Thu, 08 Aug 2024 19:52:02 GMT  
		Size: 3.0 MB (3034852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0dfbf35befd934b3269c7f9f9c391974da4d1dca33f36515bd2dfa7352f5d1e`  
		Last Modified: Thu, 08 Aug 2024 19:52:02 GMT  
		Size: 6.0 MB (6015601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d6a4d43f2f43e12cbd85ae7f616403e0c64a507c111410e4fa39fb99153592`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae77733354b0d53d2c6134cf545bf14ed540dec92c819344b15a4ab36c0a228c`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:e1a0ca3770caa65b8a9e485546599c450760c1365374fb7e1cb416557e25db80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:34a38b278b4fe46c1b431fcf7dfa6cbac1615246172272129b9208d0d2fa8bd4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680b372bebae349d2d30d7d1885053541c90be76f8b4cc32415f7d940836dc13`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:14:11 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 16 Mar 2024 06:14:11 GMT
RUN adduser -S eggdrop
# Sat, 16 Mar 2024 06:14:13 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 16 Mar 2024 06:14:14 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 16 Mar 2024 06:18:03 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 16 Mar 2024 06:18:03 GMT
ENV NICK=
# Sat, 16 Mar 2024 06:18:03 GMT
ENV SERVER=
# Sat, 16 Mar 2024 06:18:03 GMT
ENV LISTEN=3333
# Sat, 16 Mar 2024 06:18:03 GMT
ENV OWNER=
# Sat, 16 Mar 2024 06:18:03 GMT
ENV USERFILE=eggdrop.user
# Sat, 16 Mar 2024 06:18:03 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 16 Mar 2024 06:18:03 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 16 Mar 2024 06:18:03 GMT
EXPOSE 3333
# Sat, 16 Mar 2024 06:18:04 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 16 Mar 2024 06:18:04 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 16 Mar 2024 06:18:04 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 16 Mar 2024 06:18:04 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c630ff352121cf34896e97408532ee11e27a42505c86d429d155280ccb8002`  
		Last Modified: Sat, 16 Mar 2024 06:18:34 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb419fa2bf132049b023b1393209d0b8836e6a7598b618c2dbee91036dc922f7`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 11.0 KB (10954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b4a85b3c8cbd4a52ab562b3e5909758273e37b541cdc144e2a07fc4a329f84`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 2.8 MB (2758094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91429a382ad8f8d515a3269ac11d856c4a69a1062217035b56747b603c5fd9b3`  
		Last Modified: Sat, 16 Mar 2024 06:18:34 GMT  
		Size: 6.1 MB (6146820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865c61fc1b45ec89476a85feefd5ae3515f358e5255fc53b9611732f34f49355`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe2aee5f06911bbd805d8dc9d6beedd17ff7a25f96fbb1dc1ba70732675d433`  
		Last Modified: Sat, 16 Mar 2024 06:18:33 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:d54fdfd8b26fb5b0f8b7500a4d1ad7c3ffa2e42c22a13803a8211a7471885a04
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11954276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f378228fee0077f2c893c1a7f54eb600597161946e443375418ce0b6cc299f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:22 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
# Mon, 22 Jul 2024 21:49:22 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 19:54:54 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 19:54:55 GMT
RUN adduser -S eggdrop
# Thu, 08 Aug 2024 19:54:56 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 08 Aug 2024 19:54:58 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 08 Aug 2024 19:59:38 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 08 Aug 2024 19:59:38 GMT
ENV NICK=
# Thu, 08 Aug 2024 19:59:38 GMT
ENV SERVER=
# Thu, 08 Aug 2024 19:59:39 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 19:59:39 GMT
ENV OWNER=
# Thu, 08 Aug 2024 19:59:39 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 19:59:39 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 19:59:39 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 19:59:39 GMT
EXPOSE 3333
# Thu, 08 Aug 2024 19:59:39 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 08 Aug 2024 19:59:39 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 08 Aug 2024 19:59:40 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 19:59:40 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:25b28a78657effc87fccb3820a41450134ddcdbea210294d5b989ee0f09c0563`  
		Last Modified: Mon, 22 Jul 2024 21:49:53 GMT  
		Size: 3.2 MB (3175673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce1736469a094d3fea3178e545181d8c90b7f519a24e40834d20196aeecf493`  
		Last Modified: Thu, 08 Aug 2024 20:02:56 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b0bd5169afbdebbcbe59c1a8999d4f702e7c96753a8a9224271038b0efc5f4`  
		Last Modified: Thu, 08 Aug 2024 20:02:54 GMT  
		Size: 11.0 KB (11009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f753a90e840abe1598071e0e8575bfb9a56d4b638e492a9d533a787764424715`  
		Last Modified: Thu, 08 Aug 2024 20:02:55 GMT  
		Size: 2.9 MB (2904462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8dfcdf07d0444df1253fdec5e3655f16380890afb4f20871122d88ed855b77e`  
		Last Modified: Thu, 08 Aug 2024 20:02:55 GMT  
		Size: 5.9 MB (5859352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805e6d65553da001602486202abb7c08f1b23065651b0b09095d997694e2354c`  
		Last Modified: Thu, 08 Aug 2024 20:02:54 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b47463063d2c9865c7a9c41b59750bddb780891be5947eb3f0a73318cadfc9`  
		Last Modified: Thu, 08 Aug 2024 20:02:54 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:64166b3cf2df01a17e431db880b621810acda5b0fd0ddbba6ba59105e2b82fd8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12424083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d293d71c94643df7ec3252594eca670575e13b9d2d9c0bf18a71aea03b02a8d`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 19:45:45 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 19:45:45 GMT
RUN adduser -S eggdrop
# Thu, 08 Aug 2024 19:45:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 08 Aug 2024 19:45:48 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 08 Aug 2024 19:49:18 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 08 Aug 2024 19:49:18 GMT
ENV NICK=
# Thu, 08 Aug 2024 19:49:18 GMT
ENV SERVER=
# Thu, 08 Aug 2024 19:49:18 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 19:49:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 19:49:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 19:49:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 19:49:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 19:49:19 GMT
EXPOSE 3333
# Thu, 08 Aug 2024 19:49:19 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 08 Aug 2024 19:49:19 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 08 Aug 2024 19:49:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 19:49:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3af4066f123f44c2fb98e2f28964f982bc14db4ba15906ad8cc3887a867266`  
		Last Modified: Thu, 08 Aug 2024 19:52:03 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ccffd445d45c37456f285a0ce2105caf980a691a88a750da9d0b219b008a86`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 11.4 KB (11395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0587e228beafa54aa50b93967977861c70914e0ddedcd401e31b42fd0c0e733`  
		Last Modified: Thu, 08 Aug 2024 19:52:02 GMT  
		Size: 3.0 MB (3034852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0dfbf35befd934b3269c7f9f9c391974da4d1dca33f36515bd2dfa7352f5d1e`  
		Last Modified: Thu, 08 Aug 2024 19:52:02 GMT  
		Size: 6.0 MB (6015601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d6a4d43f2f43e12cbd85ae7f616403e0c64a507c111410e4fa39fb99153592`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae77733354b0d53d2c6134cf545bf14ed540dec92c819344b15a4ab36c0a228c`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
