<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.9`](#eggdrop19)
-	[`eggdrop:1.9.5`](#eggdrop195)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.9`

```console
$ docker pull eggdrop@sha256:a747b89bb44438ff60e4361de08897eefb6867d44c1f8681e86a4203df9a097f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9` - linux; amd64

```console
$ docker pull eggdrop@sha256:57a147a5cf2a4f194b2b76353a0dfaf454ebb27cb7393fcebd437cf8d5d21b79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edcf45b10d05687f622222d595cc7c6c9f41fe6442416119b8f63be2cc69ffc`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:58:51 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 29 Mar 2023 19:58:51 GMT
RUN adduser -S eggdrop
# Wed, 29 Mar 2023 19:58:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 29 Mar 2023 19:58:53 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 29 Mar 2023 20:02:50 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 29 Mar 2023 20:02:50 GMT
ENV NICK=
# Wed, 29 Mar 2023 20:02:50 GMT
ENV SERVER=
# Wed, 29 Mar 2023 20:02:50 GMT
ENV LISTEN=3333
# Wed, 29 Mar 2023 20:02:50 GMT
ENV OWNER=
# Wed, 29 Mar 2023 20:02:50 GMT
ENV USERFILE=eggdrop.user
# Wed, 29 Mar 2023 20:02:50 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 29 Mar 2023 20:02:50 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 29 Mar 2023 20:02:51 GMT
EXPOSE 3333
# Wed, 29 Mar 2023 20:02:51 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 29 Mar 2023 20:02:51 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 29 Mar 2023 20:02:51 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 29 Mar 2023 20:02:51 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23976c3f784517befc2fad73f932254ab2c35b19a8c57a33699f7111ce63fce2`  
		Last Modified: Wed, 29 Mar 2023 20:03:15 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbeecf4fb1af393b47260e06a8839c6be72f28aa2d067870cb1095f1dde69982`  
		Last Modified: Wed, 29 Mar 2023 20:03:13 GMT  
		Size: 10.9 KB (10941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5427267142d57e33be6fcd6b03cfa5043b2dee85068a32a0d2759f433a0a5c4`  
		Last Modified: Wed, 29 Mar 2023 20:03:14 GMT  
		Size: 2.8 MB (2757962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43cd3de0b8fab51b1167597c6a99c9e3c08d396a2dde5809da6b2baf305d05a`  
		Last Modified: Wed, 29 Mar 2023 20:03:15 GMT  
		Size: 6.1 MB (6146955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a860fb2bfe9d6a3fdea128401a5b55a39013c35429561c9920a892710a980d5b`  
		Last Modified: Wed, 29 Mar 2023 20:03:13 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ddc2bae137f2434cd1023385e46a65c72fd99ea1937038e767b0fbc4adcb1c`  
		Last Modified: Wed, 29 Mar 2023 20:03:13 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:b8f18f32c6f50d3d622b687a62a98063626c1ebaad90b88615b01cce14c94f6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11363954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1faba54e962f458cbc99783a3c0429a3bdf9b487dfd87861c7e32eaaf592ac`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:28 GMT
ADD file:41a85835978e4acba9d92833f0d5e20084da50779e52d8832d576b003a7aa1bb in / 
# Wed, 14 Jun 2023 18:49:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 19:50:56 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Jun 2023 19:50:57 GMT
RUN adduser -S eggdrop
# Wed, 14 Jun 2023 19:51:00 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Jun 2023 19:51:03 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Jun 2023 19:56:08 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Jun 2023 19:56:08 GMT
ENV NICK=
# Wed, 14 Jun 2023 19:56:09 GMT
ENV SERVER=
# Wed, 14 Jun 2023 19:56:09 GMT
ENV LISTEN=3333
# Wed, 14 Jun 2023 19:56:09 GMT
ENV OWNER=
# Wed, 14 Jun 2023 19:56:09 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Jun 2023 19:56:09 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Jun 2023 19:56:09 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Jun 2023 19:56:09 GMT
EXPOSE 3333
# Wed, 14 Jun 2023 19:56:09 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Jun 2023 19:56:09 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Jun 2023 19:56:09 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Jun 2023 19:56:09 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:053f9b31dd2e619ba14dc3733515fcd65e92851f612b94453db88ea1d27ab0ea`  
		Last Modified: Wed, 14 Jun 2023 18:50:10 GMT  
		Size: 2.6 MB (2615570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59edb5f625f9baba9a7ea41967538ecb65f8f3a2c21dbaac52c1cebdda71f4c5`  
		Last Modified: Wed, 14 Jun 2023 19:56:37 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d91c589e5b4c6197aed20876f69cbd4e6c2b756d05e459b7ac6bbcabe136c7`  
		Last Modified: Wed, 14 Jun 2023 19:56:35 GMT  
		Size: 10.6 KB (10631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fdffc7323d45dd58aa0359aab7e2d9f9f375fddb9958fcd64fd770c94daf83`  
		Last Modified: Wed, 14 Jun 2023 19:56:36 GMT  
		Size: 2.7 MB (2679963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2d7b4abdc31f67a9db93623090b78267d3fea57aef5ce525ffa72866261ccd`  
		Last Modified: Wed, 14 Jun 2023 19:56:37 GMT  
		Size: 6.1 MB (6053977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114272a2dc638a3349674767d3512c750bc67c2aa58ab072006c0c343c129aa8`  
		Last Modified: Wed, 14 Jun 2023 19:56:35 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f4afb0fc779b33a25070697e8911beeae28c81d7400a42941eee76a2e95ba1`  
		Last Modified: Wed, 14 Jun 2023 19:56:35 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:30e1a07d96fd6931347842b9e336e3406c69a22af5a30ee3a6c6eede82c759db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11686144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95261f7f791cadf51418239f765292865cfdb39a9c8ac55c55c2addba62a289f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:51:05 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Jun 2023 22:51:05 GMT
RUN adduser -S eggdrop
# Wed, 14 Jun 2023 22:51:06 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Jun 2023 22:51:08 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Jun 2023 22:54:57 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Jun 2023 22:54:57 GMT
ENV NICK=
# Wed, 14 Jun 2023 22:54:57 GMT
ENV SERVER=
# Wed, 14 Jun 2023 22:54:57 GMT
ENV LISTEN=3333
# Wed, 14 Jun 2023 22:54:57 GMT
ENV OWNER=
# Wed, 14 Jun 2023 22:54:57 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Jun 2023 22:54:57 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Jun 2023 22:54:57 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Jun 2023 22:54:57 GMT
EXPOSE 3333
# Wed, 14 Jun 2023 22:54:57 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Jun 2023 22:54:58 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Jun 2023 22:54:58 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Jun 2023 22:54:58 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099eb2c394b0d326d520fdcc5f18a8fc772045d738fe77a2f240efab118e0d9b`  
		Last Modified: Wed, 14 Jun 2023 22:55:28 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbc96b3f897fdcd18e5cda5ebe64ec173bbfd8da96d5d790e9b0fd73cefc79d`  
		Last Modified: Wed, 14 Jun 2023 22:55:26 GMT  
		Size: 10.7 KB (10747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e509faecac222671b3dd4d55f72a002ca5a682a47d68f82faf0510bd4537e5`  
		Last Modified: Wed, 14 Jun 2023 22:55:26 GMT  
		Size: 2.8 MB (2776563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778ae48ae48085b17498690a77e4e6048a2ccf947f9a36640cecba18111a1b55`  
		Last Modified: Wed, 14 Jun 2023 22:55:27 GMT  
		Size: 6.2 MB (6187134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351a0886d9b67a435b0ad05bc1102cca13f87d0b00c9acea9271dbde6f057284`  
		Last Modified: Wed, 14 Jun 2023 22:55:26 GMT  
		Size: 1.8 KB (1828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457742eaec2ef43d65da8e6c10a538032d2d076549399118c397804c11c2ed72`  
		Last Modified: Wed, 14 Jun 2023 22:55:26 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.9.5`

```console
$ docker pull eggdrop@sha256:a747b89bb44438ff60e4361de08897eefb6867d44c1f8681e86a4203df9a097f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9.5` - linux; amd64

```console
$ docker pull eggdrop@sha256:57a147a5cf2a4f194b2b76353a0dfaf454ebb27cb7393fcebd437cf8d5d21b79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edcf45b10d05687f622222d595cc7c6c9f41fe6442416119b8f63be2cc69ffc`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:58:51 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 29 Mar 2023 19:58:51 GMT
RUN adduser -S eggdrop
# Wed, 29 Mar 2023 19:58:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 29 Mar 2023 19:58:53 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 29 Mar 2023 20:02:50 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 29 Mar 2023 20:02:50 GMT
ENV NICK=
# Wed, 29 Mar 2023 20:02:50 GMT
ENV SERVER=
# Wed, 29 Mar 2023 20:02:50 GMT
ENV LISTEN=3333
# Wed, 29 Mar 2023 20:02:50 GMT
ENV OWNER=
# Wed, 29 Mar 2023 20:02:50 GMT
ENV USERFILE=eggdrop.user
# Wed, 29 Mar 2023 20:02:50 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 29 Mar 2023 20:02:50 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 29 Mar 2023 20:02:51 GMT
EXPOSE 3333
# Wed, 29 Mar 2023 20:02:51 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 29 Mar 2023 20:02:51 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 29 Mar 2023 20:02:51 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 29 Mar 2023 20:02:51 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23976c3f784517befc2fad73f932254ab2c35b19a8c57a33699f7111ce63fce2`  
		Last Modified: Wed, 29 Mar 2023 20:03:15 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbeecf4fb1af393b47260e06a8839c6be72f28aa2d067870cb1095f1dde69982`  
		Last Modified: Wed, 29 Mar 2023 20:03:13 GMT  
		Size: 10.9 KB (10941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5427267142d57e33be6fcd6b03cfa5043b2dee85068a32a0d2759f433a0a5c4`  
		Last Modified: Wed, 29 Mar 2023 20:03:14 GMT  
		Size: 2.8 MB (2757962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43cd3de0b8fab51b1167597c6a99c9e3c08d396a2dde5809da6b2baf305d05a`  
		Last Modified: Wed, 29 Mar 2023 20:03:15 GMT  
		Size: 6.1 MB (6146955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a860fb2bfe9d6a3fdea128401a5b55a39013c35429561c9920a892710a980d5b`  
		Last Modified: Wed, 29 Mar 2023 20:03:13 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ddc2bae137f2434cd1023385e46a65c72fd99ea1937038e767b0fbc4adcb1c`  
		Last Modified: Wed, 29 Mar 2023 20:03:13 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.5` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:b8f18f32c6f50d3d622b687a62a98063626c1ebaad90b88615b01cce14c94f6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11363954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1faba54e962f458cbc99783a3c0429a3bdf9b487dfd87861c7e32eaaf592ac`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:28 GMT
ADD file:41a85835978e4acba9d92833f0d5e20084da50779e52d8832d576b003a7aa1bb in / 
# Wed, 14 Jun 2023 18:49:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 19:50:56 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Jun 2023 19:50:57 GMT
RUN adduser -S eggdrop
# Wed, 14 Jun 2023 19:51:00 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Jun 2023 19:51:03 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Jun 2023 19:56:08 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Jun 2023 19:56:08 GMT
ENV NICK=
# Wed, 14 Jun 2023 19:56:09 GMT
ENV SERVER=
# Wed, 14 Jun 2023 19:56:09 GMT
ENV LISTEN=3333
# Wed, 14 Jun 2023 19:56:09 GMT
ENV OWNER=
# Wed, 14 Jun 2023 19:56:09 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Jun 2023 19:56:09 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Jun 2023 19:56:09 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Jun 2023 19:56:09 GMT
EXPOSE 3333
# Wed, 14 Jun 2023 19:56:09 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Jun 2023 19:56:09 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Jun 2023 19:56:09 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Jun 2023 19:56:09 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:053f9b31dd2e619ba14dc3733515fcd65e92851f612b94453db88ea1d27ab0ea`  
		Last Modified: Wed, 14 Jun 2023 18:50:10 GMT  
		Size: 2.6 MB (2615570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59edb5f625f9baba9a7ea41967538ecb65f8f3a2c21dbaac52c1cebdda71f4c5`  
		Last Modified: Wed, 14 Jun 2023 19:56:37 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d91c589e5b4c6197aed20876f69cbd4e6c2b756d05e459b7ac6bbcabe136c7`  
		Last Modified: Wed, 14 Jun 2023 19:56:35 GMT  
		Size: 10.6 KB (10631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fdffc7323d45dd58aa0359aab7e2d9f9f375fddb9958fcd64fd770c94daf83`  
		Last Modified: Wed, 14 Jun 2023 19:56:36 GMT  
		Size: 2.7 MB (2679963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2d7b4abdc31f67a9db93623090b78267d3fea57aef5ce525ffa72866261ccd`  
		Last Modified: Wed, 14 Jun 2023 19:56:37 GMT  
		Size: 6.1 MB (6053977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114272a2dc638a3349674767d3512c750bc67c2aa58ab072006c0c343c129aa8`  
		Last Modified: Wed, 14 Jun 2023 19:56:35 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f4afb0fc779b33a25070697e8911beeae28c81d7400a42941eee76a2e95ba1`  
		Last Modified: Wed, 14 Jun 2023 19:56:35 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.5` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:30e1a07d96fd6931347842b9e336e3406c69a22af5a30ee3a6c6eede82c759db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11686144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95261f7f791cadf51418239f765292865cfdb39a9c8ac55c55c2addba62a289f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:51:05 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Jun 2023 22:51:05 GMT
RUN adduser -S eggdrop
# Wed, 14 Jun 2023 22:51:06 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Jun 2023 22:51:08 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Jun 2023 22:54:57 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Jun 2023 22:54:57 GMT
ENV NICK=
# Wed, 14 Jun 2023 22:54:57 GMT
ENV SERVER=
# Wed, 14 Jun 2023 22:54:57 GMT
ENV LISTEN=3333
# Wed, 14 Jun 2023 22:54:57 GMT
ENV OWNER=
# Wed, 14 Jun 2023 22:54:57 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Jun 2023 22:54:57 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Jun 2023 22:54:57 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Jun 2023 22:54:57 GMT
EXPOSE 3333
# Wed, 14 Jun 2023 22:54:57 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Jun 2023 22:54:58 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Jun 2023 22:54:58 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Jun 2023 22:54:58 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099eb2c394b0d326d520fdcc5f18a8fc772045d738fe77a2f240efab118e0d9b`  
		Last Modified: Wed, 14 Jun 2023 22:55:28 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbc96b3f897fdcd18e5cda5ebe64ec173bbfd8da96d5d790e9b0fd73cefc79d`  
		Last Modified: Wed, 14 Jun 2023 22:55:26 GMT  
		Size: 10.7 KB (10747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e509faecac222671b3dd4d55f72a002ca5a682a47d68f82faf0510bd4537e5`  
		Last Modified: Wed, 14 Jun 2023 22:55:26 GMT  
		Size: 2.8 MB (2776563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778ae48ae48085b17498690a77e4e6048a2ccf947f9a36640cecba18111a1b55`  
		Last Modified: Wed, 14 Jun 2023 22:55:27 GMT  
		Size: 6.2 MB (6187134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351a0886d9b67a435b0ad05bc1102cca13f87d0b00c9acea9271dbde6f057284`  
		Last Modified: Wed, 14 Jun 2023 22:55:26 GMT  
		Size: 1.8 KB (1828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457742eaec2ef43d65da8e6c10a538032d2d076549399118c397804c11c2ed72`  
		Last Modified: Wed, 14 Jun 2023 22:55:26 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:e7db6844ac96a8e5c8b03ebe4f33c3146d9df1be88fe7733e2ad1ba4fc70f2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:bc541fc728b554e4f7640cbdb9a68229aaac76d45b1aa6730ad08d7f32df484b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16124690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84396e5cb68862bf935730f66e5c1f08a3dcc09477841b3bdfe3e3d5a3f107f1`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:54:57 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 29 Mar 2023 19:54:58 GMT
RUN adduser -S eggdrop
# Wed, 29 Mar 2023 19:54:59 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 29 Mar 2023 19:54:59 GMT
ENV EGGDROP_SHA256=cc7936ee427959081651319119ac0b8f3581a18d7be7b20f71023954f1f69a91
# Wed, 29 Mar 2023 19:54:59 GMT
ENV EGGDROP_COMMIT=26ecf0921ee84c5bf61cb31014a75f02670b1af4
# Wed, 29 Mar 2023 19:55:00 GMT
RUN apk --update add --no-cache bash openssl
# Wed, 29 Mar 2023 19:58:37 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 29 Mar 2023 19:58:37 GMT
ENV NICK=
# Wed, 29 Mar 2023 19:58:37 GMT
ENV SERVER=
# Wed, 29 Mar 2023 19:58:37 GMT
ENV LISTEN=3333
# Wed, 29 Mar 2023 19:58:37 GMT
ENV OWNER=
# Wed, 29 Mar 2023 19:58:37 GMT
ENV USERFILE=eggdrop.user
# Wed, 29 Mar 2023 19:58:37 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 29 Mar 2023 19:58:37 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 29 Mar 2023 19:58:37 GMT
EXPOSE 3333
# Wed, 29 Mar 2023 19:58:38 GMT
COPY file:35e05bb72116a1848ec779e3fbc4ea6bbcd95ceb11059751f608c8543e18cde7 in /home/eggdrop/eggdrop 
# Wed, 29 Mar 2023 19:58:38 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 29 Mar 2023 19:58:38 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 29 Mar 2023 19:58:38 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448baa775d700b6d963b98900648a2a828a6e33dc23c5b146e833095c826d3bf`  
		Last Modified: Wed, 29 Mar 2023 20:03:08 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1edddd715dda5d8ca68ed2c72ad665f4ba9a79f3b5d7a3e190d45d2e5cec66a3`  
		Last Modified: Wed, 29 Mar 2023 20:03:06 GMT  
		Size: 11.0 KB (10979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8f0c91f7f35c261be4b320d49652a14b869a7ea0ddc550b062742266c2779d`  
		Last Modified: Wed, 29 Mar 2023 20:03:06 GMT  
		Size: 1.2 MB (1202021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7296b3a61c4009b463590722a0e6080646f28e9e8f81c371a26cb41fc174bebe`  
		Last Modified: Wed, 29 Mar 2023 20:03:07 GMT  
		Size: 11.5 MB (11532897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a5973215293aa56051e3413de88292cd6608fe8809b7eb519bdd500bc4974f`  
		Last Modified: Wed, 29 Mar 2023 20:03:06 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641588a22b8e55ee2967e817b9dfaddea36bafe614336433770a692aaa136ca6`  
		Last Modified: Wed, 29 Mar 2023 20:03:06 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:b04c9ee90ae434c47a92e072bbe5b57531dbaa037afceaf1c681c13004a76b42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15727050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c20287fe40eb276e9686ef4bea510b90ebafc1975f35e844d5f9022befbd0b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:25 GMT
ADD file:07e668ef139dce7f076143a30b89ff57885c8539d8b5764ac1bd5277d9936702 in / 
# Wed, 14 Jun 2023 18:49:25 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 19:46:33 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Jun 2023 19:46:34 GMT
RUN adduser -S eggdrop
# Wed, 14 Jun 2023 19:46:36 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Jun 2023 19:46:36 GMT
ENV EGGDROP_SHA256=cc7936ee427959081651319119ac0b8f3581a18d7be7b20f71023954f1f69a91
# Wed, 14 Jun 2023 19:46:37 GMT
ENV EGGDROP_COMMIT=26ecf0921ee84c5bf61cb31014a75f02670b1af4
# Wed, 14 Jun 2023 19:46:38 GMT
RUN apk --update add --no-cache bash openssl
# Wed, 14 Jun 2023 19:50:44 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Jun 2023 19:50:44 GMT
ENV NICK=
# Wed, 14 Jun 2023 19:50:45 GMT
ENV SERVER=
# Wed, 14 Jun 2023 19:50:45 GMT
ENV LISTEN=3333
# Wed, 14 Jun 2023 19:50:45 GMT
ENV OWNER=
# Wed, 14 Jun 2023 19:50:45 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Jun 2023 19:50:45 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Jun 2023 19:50:45 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Jun 2023 19:50:45 GMT
EXPOSE 3333
# Wed, 14 Jun 2023 19:50:45 GMT
COPY file:35e05bb72116a1848ec779e3fbc4ea6bbcd95ceb11059751f608c8543e18cde7 in /home/eggdrop/eggdrop 
# Wed, 14 Jun 2023 19:50:45 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Jun 2023 19:50:45 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Jun 2023 19:50:45 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:33ec62e98ceea71d24212ee03e239c2d5538dbe7c98f41c42e8b2693fedf58fb`  
		Last Modified: Wed, 14 Jun 2023 18:50:00 GMT  
		Size: 3.1 MB (3110916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da662cf081eacecc880868556d58fefa681f5a85748f715fa018059fc3610b9`  
		Last Modified: Wed, 14 Jun 2023 19:56:28 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1adc81653025f97685e7c96ba9145ecf37d5eb688af5653e202542ce7aa0af4`  
		Last Modified: Wed, 14 Jun 2023 19:56:26 GMT  
		Size: 11.1 KB (11135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93b4e51f49c1a11557946eba1189df73b55efac200f2f9fdfcf88c4a2ccc789`  
		Last Modified: Wed, 14 Jun 2023 19:56:27 GMT  
		Size: 1.2 MB (1187432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b510499214f86b56fc84b2e8fce2d41a3c2ac6a01d3a339c5b6502e92f3968e8`  
		Last Modified: Wed, 14 Jun 2023 19:56:29 GMT  
		Size: 11.4 MB (11413335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6856ec7405ef9cab9d83cb843abb5b9880819c47362f0abd65c2adb821c61d33`  
		Last Modified: Wed, 14 Jun 2023 19:56:26 GMT  
		Size: 1.9 KB (1896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6058d001e9e054632a5c35775eaef1dc3e93a2b93e697f7d21e2d49ff024f6d0`  
		Last Modified: Wed, 14 Jun 2023 19:56:26 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:d6ee40eddcd6b4a135621b7b30c03b37126ea9caa8a0351ddabc3d3355e48154
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16104053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100ca47c5d29b68946c3c6b138af46476c2bb77c08d9c9829d9b71642a7cda37`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:04 GMT
ADD file:6f6c919dc1fe5a56c2664a26a702d77203039cdd4c91e39da57063ea5d3f3094 in / 
# Wed, 14 Jun 2023 20:49:04 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:47:42 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Jun 2023 22:47:42 GMT
RUN adduser -S eggdrop
# Wed, 14 Jun 2023 22:47:44 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Jun 2023 22:47:44 GMT
ENV EGGDROP_SHA256=cc7936ee427959081651319119ac0b8f3581a18d7be7b20f71023954f1f69a91
# Wed, 14 Jun 2023 22:47:44 GMT
ENV EGGDROP_COMMIT=26ecf0921ee84c5bf61cb31014a75f02670b1af4
# Wed, 14 Jun 2023 22:47:45 GMT
RUN apk --update add --no-cache bash openssl
# Wed, 14 Jun 2023 22:51:02 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Jun 2023 22:51:02 GMT
ENV NICK=
# Wed, 14 Jun 2023 22:51:02 GMT
ENV SERVER=
# Wed, 14 Jun 2023 22:51:02 GMT
ENV LISTEN=3333
# Wed, 14 Jun 2023 22:51:02 GMT
ENV OWNER=
# Wed, 14 Jun 2023 22:51:02 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Jun 2023 22:51:02 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Jun 2023 22:51:02 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Jun 2023 22:51:03 GMT
EXPOSE 3333
# Wed, 14 Jun 2023 22:51:03 GMT
COPY file:35e05bb72116a1848ec779e3fbc4ea6bbcd95ceb11059751f608c8543e18cde7 in /home/eggdrop/eggdrop 
# Wed, 14 Jun 2023 22:51:03 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Jun 2023 22:51:03 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Jun 2023 22:51:03 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:edb6bdbacee93be93e930669f43e2e922c8594676aa342a70e2221361fd1914d`  
		Last Modified: Wed, 14 Jun 2023 20:49:35 GMT  
		Size: 3.3 MB (3261139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab556bb27c3eeadbcc437904e4d024f7ab53548eb269e2f05babbd5d673b7f06`  
		Last Modified: Wed, 14 Jun 2023 22:55:21 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821fe5f3cdc578d1e7bf2c18f3185bd991b368062f1a7c6b6edf42d1d1bd2c9c`  
		Last Modified: Wed, 14 Jun 2023 22:55:19 GMT  
		Size: 11.2 KB (11189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c154146375088dd23f935a6db1f78af30a7913b4a60903db68641c8822f425bc`  
		Last Modified: Wed, 14 Jun 2023 22:55:19 GMT  
		Size: 1.2 MB (1234460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b9bf5d321b4c83ed35be7d9f12decc16635c4dd88fb9aa9a6192ac3b26b237`  
		Last Modified: Wed, 14 Jun 2023 22:55:20 GMT  
		Size: 11.6 MB (11593040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821f8b68fcae9339ef33904560aade133f4b38dae0fa947938aa1b094651f365`  
		Last Modified: Wed, 14 Jun 2023 22:55:19 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae53839769fce95bc4bcf305e8d8bbf34e1820445b05c558cc53dd2dafd53aff`  
		Last Modified: Wed, 14 Jun 2023 22:55:19 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:a747b89bb44438ff60e4361de08897eefb6867d44c1f8681e86a4203df9a097f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:57a147a5cf2a4f194b2b76353a0dfaf454ebb27cb7393fcebd437cf8d5d21b79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edcf45b10d05687f622222d595cc7c6c9f41fe6442416119b8f63be2cc69ffc`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:58:51 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 29 Mar 2023 19:58:51 GMT
RUN adduser -S eggdrop
# Wed, 29 Mar 2023 19:58:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 29 Mar 2023 19:58:53 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 29 Mar 2023 20:02:50 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 29 Mar 2023 20:02:50 GMT
ENV NICK=
# Wed, 29 Mar 2023 20:02:50 GMT
ENV SERVER=
# Wed, 29 Mar 2023 20:02:50 GMT
ENV LISTEN=3333
# Wed, 29 Mar 2023 20:02:50 GMT
ENV OWNER=
# Wed, 29 Mar 2023 20:02:50 GMT
ENV USERFILE=eggdrop.user
# Wed, 29 Mar 2023 20:02:50 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 29 Mar 2023 20:02:50 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 29 Mar 2023 20:02:51 GMT
EXPOSE 3333
# Wed, 29 Mar 2023 20:02:51 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 29 Mar 2023 20:02:51 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 29 Mar 2023 20:02:51 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 29 Mar 2023 20:02:51 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23976c3f784517befc2fad73f932254ab2c35b19a8c57a33699f7111ce63fce2`  
		Last Modified: Wed, 29 Mar 2023 20:03:15 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbeecf4fb1af393b47260e06a8839c6be72f28aa2d067870cb1095f1dde69982`  
		Last Modified: Wed, 29 Mar 2023 20:03:13 GMT  
		Size: 10.9 KB (10941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5427267142d57e33be6fcd6b03cfa5043b2dee85068a32a0d2759f433a0a5c4`  
		Last Modified: Wed, 29 Mar 2023 20:03:14 GMT  
		Size: 2.8 MB (2757962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43cd3de0b8fab51b1167597c6a99c9e3c08d396a2dde5809da6b2baf305d05a`  
		Last Modified: Wed, 29 Mar 2023 20:03:15 GMT  
		Size: 6.1 MB (6146955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a860fb2bfe9d6a3fdea128401a5b55a39013c35429561c9920a892710a980d5b`  
		Last Modified: Wed, 29 Mar 2023 20:03:13 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ddc2bae137f2434cd1023385e46a65c72fd99ea1937038e767b0fbc4adcb1c`  
		Last Modified: Wed, 29 Mar 2023 20:03:13 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:b8f18f32c6f50d3d622b687a62a98063626c1ebaad90b88615b01cce14c94f6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11363954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1faba54e962f458cbc99783a3c0429a3bdf9b487dfd87861c7e32eaaf592ac`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:28 GMT
ADD file:41a85835978e4acba9d92833f0d5e20084da50779e52d8832d576b003a7aa1bb in / 
# Wed, 14 Jun 2023 18:49:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 19:50:56 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Jun 2023 19:50:57 GMT
RUN adduser -S eggdrop
# Wed, 14 Jun 2023 19:51:00 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Jun 2023 19:51:03 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Jun 2023 19:56:08 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Jun 2023 19:56:08 GMT
ENV NICK=
# Wed, 14 Jun 2023 19:56:09 GMT
ENV SERVER=
# Wed, 14 Jun 2023 19:56:09 GMT
ENV LISTEN=3333
# Wed, 14 Jun 2023 19:56:09 GMT
ENV OWNER=
# Wed, 14 Jun 2023 19:56:09 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Jun 2023 19:56:09 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Jun 2023 19:56:09 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Jun 2023 19:56:09 GMT
EXPOSE 3333
# Wed, 14 Jun 2023 19:56:09 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Jun 2023 19:56:09 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Jun 2023 19:56:09 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Jun 2023 19:56:09 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:053f9b31dd2e619ba14dc3733515fcd65e92851f612b94453db88ea1d27ab0ea`  
		Last Modified: Wed, 14 Jun 2023 18:50:10 GMT  
		Size: 2.6 MB (2615570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59edb5f625f9baba9a7ea41967538ecb65f8f3a2c21dbaac52c1cebdda71f4c5`  
		Last Modified: Wed, 14 Jun 2023 19:56:37 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d91c589e5b4c6197aed20876f69cbd4e6c2b756d05e459b7ac6bbcabe136c7`  
		Last Modified: Wed, 14 Jun 2023 19:56:35 GMT  
		Size: 10.6 KB (10631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fdffc7323d45dd58aa0359aab7e2d9f9f375fddb9958fcd64fd770c94daf83`  
		Last Modified: Wed, 14 Jun 2023 19:56:36 GMT  
		Size: 2.7 MB (2679963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2d7b4abdc31f67a9db93623090b78267d3fea57aef5ce525ffa72866261ccd`  
		Last Modified: Wed, 14 Jun 2023 19:56:37 GMT  
		Size: 6.1 MB (6053977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114272a2dc638a3349674767d3512c750bc67c2aa58ab072006c0c343c129aa8`  
		Last Modified: Wed, 14 Jun 2023 19:56:35 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f4afb0fc779b33a25070697e8911beeae28c81d7400a42941eee76a2e95ba1`  
		Last Modified: Wed, 14 Jun 2023 19:56:35 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:30e1a07d96fd6931347842b9e336e3406c69a22af5a30ee3a6c6eede82c759db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11686144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95261f7f791cadf51418239f765292865cfdb39a9c8ac55c55c2addba62a289f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:51:05 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Jun 2023 22:51:05 GMT
RUN adduser -S eggdrop
# Wed, 14 Jun 2023 22:51:06 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Jun 2023 22:51:08 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Jun 2023 22:54:57 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Jun 2023 22:54:57 GMT
ENV NICK=
# Wed, 14 Jun 2023 22:54:57 GMT
ENV SERVER=
# Wed, 14 Jun 2023 22:54:57 GMT
ENV LISTEN=3333
# Wed, 14 Jun 2023 22:54:57 GMT
ENV OWNER=
# Wed, 14 Jun 2023 22:54:57 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Jun 2023 22:54:57 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Jun 2023 22:54:57 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Jun 2023 22:54:57 GMT
EXPOSE 3333
# Wed, 14 Jun 2023 22:54:57 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Jun 2023 22:54:58 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Jun 2023 22:54:58 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Jun 2023 22:54:58 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099eb2c394b0d326d520fdcc5f18a8fc772045d738fe77a2f240efab118e0d9b`  
		Last Modified: Wed, 14 Jun 2023 22:55:28 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbc96b3f897fdcd18e5cda5ebe64ec173bbfd8da96d5d790e9b0fd73cefc79d`  
		Last Modified: Wed, 14 Jun 2023 22:55:26 GMT  
		Size: 10.7 KB (10747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e509faecac222671b3dd4d55f72a002ca5a682a47d68f82faf0510bd4537e5`  
		Last Modified: Wed, 14 Jun 2023 22:55:26 GMT  
		Size: 2.8 MB (2776563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778ae48ae48085b17498690a77e4e6048a2ccf947f9a36640cecba18111a1b55`  
		Last Modified: Wed, 14 Jun 2023 22:55:27 GMT  
		Size: 6.2 MB (6187134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351a0886d9b67a435b0ad05bc1102cca13f87d0b00c9acea9271dbde6f057284`  
		Last Modified: Wed, 14 Jun 2023 22:55:26 GMT  
		Size: 1.8 KB (1828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457742eaec2ef43d65da8e6c10a538032d2d076549399118c397804c11c2ed72`  
		Last Modified: Wed, 14 Jun 2023 22:55:26 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:a747b89bb44438ff60e4361de08897eefb6867d44c1f8681e86a4203df9a097f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:57a147a5cf2a4f194b2b76353a0dfaf454ebb27cb7393fcebd437cf8d5d21b79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11727463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edcf45b10d05687f622222d595cc7c6c9f41fe6442416119b8f63be2cc69ffc`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:58:51 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 29 Mar 2023 19:58:51 GMT
RUN adduser -S eggdrop
# Wed, 29 Mar 2023 19:58:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 29 Mar 2023 19:58:53 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 29 Mar 2023 20:02:50 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 29 Mar 2023 20:02:50 GMT
ENV NICK=
# Wed, 29 Mar 2023 20:02:50 GMT
ENV SERVER=
# Wed, 29 Mar 2023 20:02:50 GMT
ENV LISTEN=3333
# Wed, 29 Mar 2023 20:02:50 GMT
ENV OWNER=
# Wed, 29 Mar 2023 20:02:50 GMT
ENV USERFILE=eggdrop.user
# Wed, 29 Mar 2023 20:02:50 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 29 Mar 2023 20:02:50 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 29 Mar 2023 20:02:51 GMT
EXPOSE 3333
# Wed, 29 Mar 2023 20:02:51 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 29 Mar 2023 20:02:51 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 29 Mar 2023 20:02:51 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 29 Mar 2023 20:02:51 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23976c3f784517befc2fad73f932254ab2c35b19a8c57a33699f7111ce63fce2`  
		Last Modified: Wed, 29 Mar 2023 20:03:15 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbeecf4fb1af393b47260e06a8839c6be72f28aa2d067870cb1095f1dde69982`  
		Last Modified: Wed, 29 Mar 2023 20:03:13 GMT  
		Size: 10.9 KB (10941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5427267142d57e33be6fcd6b03cfa5043b2dee85068a32a0d2759f433a0a5c4`  
		Last Modified: Wed, 29 Mar 2023 20:03:14 GMT  
		Size: 2.8 MB (2757962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43cd3de0b8fab51b1167597c6a99c9e3c08d396a2dde5809da6b2baf305d05a`  
		Last Modified: Wed, 29 Mar 2023 20:03:15 GMT  
		Size: 6.1 MB (6146955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a860fb2bfe9d6a3fdea128401a5b55a39013c35429561c9920a892710a980d5b`  
		Last Modified: Wed, 29 Mar 2023 20:03:13 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ddc2bae137f2434cd1023385e46a65c72fd99ea1937038e767b0fbc4adcb1c`  
		Last Modified: Wed, 29 Mar 2023 20:03:13 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:b8f18f32c6f50d3d622b687a62a98063626c1ebaad90b88615b01cce14c94f6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11363954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1faba54e962f458cbc99783a3c0429a3bdf9b487dfd87861c7e32eaaf592ac`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:28 GMT
ADD file:41a85835978e4acba9d92833f0d5e20084da50779e52d8832d576b003a7aa1bb in / 
# Wed, 14 Jun 2023 18:49:29 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 19:50:56 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Jun 2023 19:50:57 GMT
RUN adduser -S eggdrop
# Wed, 14 Jun 2023 19:51:00 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Jun 2023 19:51:03 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Jun 2023 19:56:08 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Jun 2023 19:56:08 GMT
ENV NICK=
# Wed, 14 Jun 2023 19:56:09 GMT
ENV SERVER=
# Wed, 14 Jun 2023 19:56:09 GMT
ENV LISTEN=3333
# Wed, 14 Jun 2023 19:56:09 GMT
ENV OWNER=
# Wed, 14 Jun 2023 19:56:09 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Jun 2023 19:56:09 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Jun 2023 19:56:09 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Jun 2023 19:56:09 GMT
EXPOSE 3333
# Wed, 14 Jun 2023 19:56:09 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Jun 2023 19:56:09 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Jun 2023 19:56:09 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Jun 2023 19:56:09 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:053f9b31dd2e619ba14dc3733515fcd65e92851f612b94453db88ea1d27ab0ea`  
		Last Modified: Wed, 14 Jun 2023 18:50:10 GMT  
		Size: 2.6 MB (2615570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59edb5f625f9baba9a7ea41967538ecb65f8f3a2c21dbaac52c1cebdda71f4c5`  
		Last Modified: Wed, 14 Jun 2023 19:56:37 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d91c589e5b4c6197aed20876f69cbd4e6c2b756d05e459b7ac6bbcabe136c7`  
		Last Modified: Wed, 14 Jun 2023 19:56:35 GMT  
		Size: 10.6 KB (10631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fdffc7323d45dd58aa0359aab7e2d9f9f375fddb9958fcd64fd770c94daf83`  
		Last Modified: Wed, 14 Jun 2023 19:56:36 GMT  
		Size: 2.7 MB (2679963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2d7b4abdc31f67a9db93623090b78267d3fea57aef5ce525ffa72866261ccd`  
		Last Modified: Wed, 14 Jun 2023 19:56:37 GMT  
		Size: 6.1 MB (6053977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114272a2dc638a3349674767d3512c750bc67c2aa58ab072006c0c343c129aa8`  
		Last Modified: Wed, 14 Jun 2023 19:56:35 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f4afb0fc779b33a25070697e8911beeae28c81d7400a42941eee76a2e95ba1`  
		Last Modified: Wed, 14 Jun 2023 19:56:35 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:30e1a07d96fd6931347842b9e336e3406c69a22af5a30ee3a6c6eede82c759db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11686144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95261f7f791cadf51418239f765292865cfdb39a9c8ac55c55c2addba62a289f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:51:05 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Jun 2023 22:51:05 GMT
RUN adduser -S eggdrop
# Wed, 14 Jun 2023 22:51:06 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Jun 2023 22:51:08 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 14 Jun 2023 22:54:57 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Jun 2023 22:54:57 GMT
ENV NICK=
# Wed, 14 Jun 2023 22:54:57 GMT
ENV SERVER=
# Wed, 14 Jun 2023 22:54:57 GMT
ENV LISTEN=3333
# Wed, 14 Jun 2023 22:54:57 GMT
ENV OWNER=
# Wed, 14 Jun 2023 22:54:57 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Jun 2023 22:54:57 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Jun 2023 22:54:57 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Jun 2023 22:54:57 GMT
EXPOSE 3333
# Wed, 14 Jun 2023 22:54:57 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 14 Jun 2023 22:54:58 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Jun 2023 22:54:58 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Jun 2023 22:54:58 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099eb2c394b0d326d520fdcc5f18a8fc772045d738fe77a2f240efab118e0d9b`  
		Last Modified: Wed, 14 Jun 2023 22:55:28 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbc96b3f897fdcd18e5cda5ebe64ec173bbfd8da96d5d790e9b0fd73cefc79d`  
		Last Modified: Wed, 14 Jun 2023 22:55:26 GMT  
		Size: 10.7 KB (10747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e509faecac222671b3dd4d55f72a002ca5a682a47d68f82faf0510bd4537e5`  
		Last Modified: Wed, 14 Jun 2023 22:55:26 GMT  
		Size: 2.8 MB (2776563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778ae48ae48085b17498690a77e4e6048a2ccf947f9a36640cecba18111a1b55`  
		Last Modified: Wed, 14 Jun 2023 22:55:27 GMT  
		Size: 6.2 MB (6187134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351a0886d9b67a435b0ad05bc1102cca13f87d0b00c9acea9271dbde6f057284`  
		Last Modified: Wed, 14 Jun 2023 22:55:26 GMT  
		Size: 1.8 KB (1828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457742eaec2ef43d65da8e6c10a538032d2d076549399118c397804c11c2ed72`  
		Last Modified: Wed, 14 Jun 2023 22:55:26 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
