<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.10`](#eggdrop110)
-	[`eggdrop:1.10.0`](#eggdrop1100)
-	[`eggdrop:1.9`](#eggdrop19)
-	[`eggdrop:1.9.5`](#eggdrop195)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.10`

```console
$ docker pull eggdrop@sha256:570dd216d64c15b27c2366a02b116a485ae5ee028776eb39a4cbf1a2778fdda6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:1.10` - linux; amd64

```console
$ docker pull eggdrop@sha256:820390da349548b8337d027e2000a1bdc308c62846bfebe9125722405fb9f39d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17468949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c172d56253fb7af7a3b6b9f46833e567e9ca3b97206620053138b88ac075b1f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba2ed38a951eb3af32798f4d632878bfc543836ccdfc2a299b726d2ffa8af85`  
		Last Modified: Wed, 08 Jan 2025 18:01:40 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf4724448b76a36bb76ea1cd392295fd5cbb512c33b2a9b8744af84634e3666`  
		Last Modified: Wed, 08 Jan 2025 18:01:41 GMT  
		Size: 1.1 MB (1115390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0cd364521d7ca48a805725251ca95989e8ff839bdaa2e323608e7e949d7181`  
		Last Modified: Wed, 08 Jan 2025 18:01:41 GMT  
		Size: 12.7 MB (12723237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20c8212b54ec5591eacc689e1d3613b7394d54130c90ff3abca14efb6d58de`  
		Last Modified: Wed, 08 Jan 2025 18:01:41 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbd7f44f61763e498f90f16c646aec872fb647c583e46d78fec5dc0e1be0dd2`  
		Last Modified: Wed, 08 Jan 2025 18:01:41 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10` - unknown; unknown

```console
$ docker pull eggdrop@sha256:953774f40b106af1fb32fc5840952957544cc328a8c873875ad1ed8c84ee4d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 KB (157534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3267f0d8d58865a7a4b11dc973db9b5bdffdc32767e819d14c98fee65f8445`

```dockerfile
```

-	Layers:
	-	`sha256:a6c1711e8758aff9f23949489545f3eb136bd7336e552527b890e876610cda6d`  
		Last Modified: Wed, 08 Jan 2025 18:01:41 GMT  
		Size: 138.8 KB (138764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:461222170f6bcc43f749f025f1ddbafbaba23c1082414c82b3009f504e75b31a`  
		Last Modified: Wed, 08 Jan 2025 18:01:40 GMT  
		Size: 18.8 KB (18770 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:f83091be92b257d32fbf9c6fbed21ddcbacfd84e543ef17e291fb35d93a67ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17076901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5298cdfde50ed0b9ad37404d68d023aa2e6618976d7fd155e9ccbb491b7b4ed`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Wed, 08 Jan 2025 17:23:56 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e221ba7d901e5b2e4c8a1cc65e81852346141765a956648846f7d2049f8aaaf2`  
		Last Modified: Wed, 08 Jan 2025 18:27:42 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b64f124a8a5d0a4109f8450d26288172a7a8b83e46c5133671247535a592e9`  
		Last Modified: Wed, 08 Jan 2025 18:27:43 GMT  
		Size: 1.1 MB (1129563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56747594a231ad7e35932c7a593d8e8be6665e62b0846cb767b09851fc0a5b16`  
		Last Modified: Wed, 08 Jan 2025 18:35:15 GMT  
		Size: 12.6 MB (12571789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabdbac5ec70e76518d884961bf2de5ab29bc374211dcac4dd125c9a174aea11`  
		Last Modified: Wed, 08 Jan 2025 18:35:15 GMT  
		Size: 2.0 KB (1954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1f1bc39af4850d7724b277099c16b2106b9c52eb5b3e56cf1c9cc7047ab1cf`  
		Last Modified: Wed, 08 Jan 2025 18:35:15 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10` - unknown; unknown

```console
$ docker pull eggdrop@sha256:62366f69b54d5b7ee6b5ea97eac8b06acb3f22f0700e45dbafc32fb1204dc1c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e93ea81bc9ef8cc048bc0d811b744e45a3afee33ba7bf52edf66531a84f0e4`

```dockerfile
```

-	Layers:
	-	`sha256:c3336b8b867d566db0bc930345a3f0de1c70268b7323313acb1e1bc84c4e228f`  
		Last Modified: Wed, 08 Jan 2025 18:35:14 GMT  
		Size: 18.7 KB (18658 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:1e3e94175c6136b2956448a704ce185695b7ab4729803be8e617363dcfd848c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18162740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c2704a4b05e703b2b23b81be75bf14fe7a146b79e8021878d3b411e8b68b8e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dc5771b4cb21ae2a2bab536d6a359970cd3a34e970a8a0be98e54d192f0664`  
		Last Modified: Wed, 08 Jan 2025 18:27:31 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8917a57a55679bb3082cea769355873fc8ae45ab8caf5e990029718b232ebe0c`  
		Last Modified: Wed, 08 Jan 2025 18:27:31 GMT  
		Size: 1.2 MB (1210974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00fc1a13bfd6d68eac9dd7761eac4c9317710affb065542d15c60aa69086a0a`  
		Last Modified: Wed, 08 Jan 2025 18:33:30 GMT  
		Size: 12.9 MB (12856924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46884e96140c161c4efa5d4cab995e341b9592400c3db5132d42137071b8da65`  
		Last Modified: Wed, 08 Jan 2025 18:33:29 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b7d440051ff64a186a5311fc066136cb5ebe2e2a06cd80619f0e966f75f949`  
		Last Modified: Wed, 08 Jan 2025 18:33:29 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10` - unknown; unknown

```console
$ docker pull eggdrop@sha256:2d3191ee6478001199b48d737e375c8b2c545afd95c27da9f3811e7c62a02069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 KB (157725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9fcd7346d6d369651db6daa73a39ff635ebdb30d0ab64e80e7b5c5376a41a6f`

```dockerfile
```

-	Layers:
	-	`sha256:cd130b0889db81d55044ee726aef57927b6ecd401b41b4a8d123884204ae76b5`  
		Last Modified: Wed, 08 Jan 2025 18:33:29 GMT  
		Size: 138.8 KB (138820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b175d71afcc8d14c978a6331b8d3e56ea315b810c7207d64a01644920795c0`  
		Last Modified: Wed, 08 Jan 2025 18:33:29 GMT  
		Size: 18.9 KB (18905 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:1.10.0`

```console
$ docker pull eggdrop@sha256:570dd216d64c15b27c2366a02b116a485ae5ee028776eb39a4cbf1a2778fdda6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:1.10.0` - linux; amd64

```console
$ docker pull eggdrop@sha256:820390da349548b8337d027e2000a1bdc308c62846bfebe9125722405fb9f39d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17468949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c172d56253fb7af7a3b6b9f46833e567e9ca3b97206620053138b88ac075b1f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba2ed38a951eb3af32798f4d632878bfc543836ccdfc2a299b726d2ffa8af85`  
		Last Modified: Wed, 08 Jan 2025 18:01:40 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf4724448b76a36bb76ea1cd392295fd5cbb512c33b2a9b8744af84634e3666`  
		Last Modified: Wed, 08 Jan 2025 18:01:41 GMT  
		Size: 1.1 MB (1115390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0cd364521d7ca48a805725251ca95989e8ff839bdaa2e323608e7e949d7181`  
		Last Modified: Wed, 08 Jan 2025 18:01:41 GMT  
		Size: 12.7 MB (12723237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20c8212b54ec5591eacc689e1d3613b7394d54130c90ff3abca14efb6d58de`  
		Last Modified: Wed, 08 Jan 2025 18:01:41 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbd7f44f61763e498f90f16c646aec872fb647c583e46d78fec5dc0e1be0dd2`  
		Last Modified: Wed, 08 Jan 2025 18:01:41 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.0` - unknown; unknown

```console
$ docker pull eggdrop@sha256:953774f40b106af1fb32fc5840952957544cc328a8c873875ad1ed8c84ee4d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 KB (157534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3267f0d8d58865a7a4b11dc973db9b5bdffdc32767e819d14c98fee65f8445`

```dockerfile
```

-	Layers:
	-	`sha256:a6c1711e8758aff9f23949489545f3eb136bd7336e552527b890e876610cda6d`  
		Last Modified: Wed, 08 Jan 2025 18:01:41 GMT  
		Size: 138.8 KB (138764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:461222170f6bcc43f749f025f1ddbafbaba23c1082414c82b3009f504e75b31a`  
		Last Modified: Wed, 08 Jan 2025 18:01:40 GMT  
		Size: 18.8 KB (18770 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10.0` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:f83091be92b257d32fbf9c6fbed21ddcbacfd84e543ef17e291fb35d93a67ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17076901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5298cdfde50ed0b9ad37404d68d023aa2e6618976d7fd155e9ccbb491b7b4ed`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Wed, 08 Jan 2025 17:23:56 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e221ba7d901e5b2e4c8a1cc65e81852346141765a956648846f7d2049f8aaaf2`  
		Last Modified: Wed, 08 Jan 2025 18:27:42 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b64f124a8a5d0a4109f8450d26288172a7a8b83e46c5133671247535a592e9`  
		Last Modified: Wed, 08 Jan 2025 18:27:43 GMT  
		Size: 1.1 MB (1129563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56747594a231ad7e35932c7a593d8e8be6665e62b0846cb767b09851fc0a5b16`  
		Last Modified: Wed, 08 Jan 2025 18:35:15 GMT  
		Size: 12.6 MB (12571789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabdbac5ec70e76518d884961bf2de5ab29bc374211dcac4dd125c9a174aea11`  
		Last Modified: Wed, 08 Jan 2025 18:35:15 GMT  
		Size: 2.0 KB (1954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1f1bc39af4850d7724b277099c16b2106b9c52eb5b3e56cf1c9cc7047ab1cf`  
		Last Modified: Wed, 08 Jan 2025 18:35:15 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.0` - unknown; unknown

```console
$ docker pull eggdrop@sha256:62366f69b54d5b7ee6b5ea97eac8b06acb3f22f0700e45dbafc32fb1204dc1c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e93ea81bc9ef8cc048bc0d811b744e45a3afee33ba7bf52edf66531a84f0e4`

```dockerfile
```

-	Layers:
	-	`sha256:c3336b8b867d566db0bc930345a3f0de1c70268b7323313acb1e1bc84c4e228f`  
		Last Modified: Wed, 08 Jan 2025 18:35:14 GMT  
		Size: 18.7 KB (18658 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10.0` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:1e3e94175c6136b2956448a704ce185695b7ab4729803be8e617363dcfd848c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18162740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c2704a4b05e703b2b23b81be75bf14fe7a146b79e8021878d3b411e8b68b8e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dc5771b4cb21ae2a2bab536d6a359970cd3a34e970a8a0be98e54d192f0664`  
		Last Modified: Wed, 08 Jan 2025 18:27:31 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8917a57a55679bb3082cea769355873fc8ae45ab8caf5e990029718b232ebe0c`  
		Last Modified: Wed, 08 Jan 2025 18:27:31 GMT  
		Size: 1.2 MB (1210974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00fc1a13bfd6d68eac9dd7761eac4c9317710affb065542d15c60aa69086a0a`  
		Last Modified: Wed, 08 Jan 2025 18:33:30 GMT  
		Size: 12.9 MB (12856924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46884e96140c161c4efa5d4cab995e341b9592400c3db5132d42137071b8da65`  
		Last Modified: Wed, 08 Jan 2025 18:33:29 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b7d440051ff64a186a5311fc066136cb5ebe2e2a06cd80619f0e966f75f949`  
		Last Modified: Wed, 08 Jan 2025 18:33:29 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.0` - unknown; unknown

```console
$ docker pull eggdrop@sha256:2d3191ee6478001199b48d737e375c8b2c545afd95c27da9f3811e7c62a02069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 KB (157725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9fcd7346d6d369651db6daa73a39ff635ebdb30d0ab64e80e7b5c5376a41a6f`

```dockerfile
```

-	Layers:
	-	`sha256:cd130b0889db81d55044ee726aef57927b6ecd401b41b4a8d123884204ae76b5`  
		Last Modified: Wed, 08 Jan 2025 18:33:29 GMT  
		Size: 138.8 KB (138820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b175d71afcc8d14c978a6331b8d3e56ea315b810c7207d64a01644920795c0`  
		Last Modified: Wed, 08 Jan 2025 18:33:29 GMT  
		Size: 18.9 KB (18905 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:1.9`

```console
$ docker pull eggdrop@sha256:35805191134f5fdbbea8b5c2e33060d079b1c504c4b9b04dbbd3bfb1c72b827d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:1.9` - linux; amd64

```console
$ docker pull eggdrop@sha256:18010ff34267435ece22921511c072f362e499fb1139be5a00386abd256a2202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12285296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702c1bdd52b4b377889e7b0e9c29040afe0cfb233a550cff2f8828063a80247c`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 15:14:19 GMT
RUN adduser -S eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache tcl bash openssl # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:14:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:14:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:14:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:14:19 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:14:19 GMT
COPY entrypoint.sh /home/eggdrop/eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
COPY docker.tcl /home/eggdrop/eggdrop/scripts/ # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ff7ee5a95c455915fb1fbbb11b9b4d02b120ee128c9208ee5d816be1348b90`  
		Last Modified: Wed, 08 Jan 2025 18:02:25 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f7943a30c406824a5c967253b593622addd3ef529d0776e1f9a6c4578dc917`  
		Last Modified: Wed, 08 Jan 2025 18:02:25 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbac46b60b34452978aa607da72b295b333dc06881c24847a9a9065e47083913`  
		Last Modified: Wed, 08 Jan 2025 18:02:25 GMT  
		Size: 2.9 MB (2886343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd269a60e7f25046f13363305d3db9e0fc0ec5f9848d25d0d91152ce178d1f0`  
		Last Modified: Wed, 08 Jan 2025 18:02:25 GMT  
		Size: 6.0 MB (5964075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53aa1a98d14557559aa069805873f0890809e623669b4008fb6823ab38fa9664`  
		Last Modified: Wed, 08 Jan 2025 18:02:26 GMT  
		Size: 1.8 KB (1828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0727f149e66b0e76fbda20fe8f063a3fa6a5b7ad18de19e17acae904f9c3afc0`  
		Last Modified: Wed, 08 Jan 2025 18:02:26 GMT  
		Size: 697.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9` - unknown; unknown

```console
$ docker pull eggdrop@sha256:493b85ac76da1bcc95193717c82e0875db62866c4db9d613a22cf5ccbd217607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1062538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf4d82d7ad2da3002f92e99b0e939dee3dac6777419f370e1bbeda0cf86c336`

```dockerfile
```

-	Layers:
	-	`sha256:473cb128e980cf6fd88ea4f6bcf56a729db68d465e3f67ec3207990faf5ed600`  
		Last Modified: Wed, 08 Jan 2025 18:02:25 GMT  
		Size: 1.0 MB (1043182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f52ffe3e57422c2bbe9d7f8034c9064b1a3e5a615d54f062bb835181863f8d43`  
		Last Modified: Wed, 08 Jan 2025 18:02:25 GMT  
		Size: 19.4 KB (19356 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:a60f5adceeb4522e0ccdf30292032eca3eb516a9cdf0aa616976835e20db0cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11940483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b360698b8a9eb90311e0b210f2554a3ed7ab36f1b64c722a8def98bab6cd28`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.6-armhf.tar.gz / # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 15:14:19 GMT
RUN adduser -S eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache tcl bash openssl # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:14:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:14:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:14:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:14:19 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:14:19 GMT
COPY entrypoint.sh /home/eggdrop/eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
COPY docker.tcl /home/eggdrop/eggdrop/scripts/ # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:bfff14c232517ab149a6524fba444f7b5a336feab49d08abd27455f12ceb2efc`  
		Last Modified: Wed, 08 Jan 2025 17:24:09 GMT  
		Size: 3.2 MB (3176999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1943658bb1f5aa40f8fb6a5a2d03bed28a28a4c2ca25515867ddd8e91a708f`  
		Last Modified: Wed, 08 Jan 2025 18:32:18 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4901e5ef91acfad3b9b49b7efd5ea010d98368973c1246ba49d70c3d746e2d`  
		Last Modified: Wed, 08 Jan 2025 18:32:18 GMT  
		Size: 11.0 KB (10964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50db5a6d0511046c91accd10af4cd56efe341f1294ba452a9958e502fa5037d6`  
		Last Modified: Wed, 08 Jan 2025 18:32:18 GMT  
		Size: 2.9 MB (2889091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef9badf636f5ee159fe3ff62bba8df1f27567145299049d92db505871afa32b`  
		Last Modified: Wed, 08 Jan 2025 18:32:19 GMT  
		Size: 5.9 MB (5859616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84d9215cd3b358f1614835943a80c85bfae214d11d10a0fd5aaab412b61bb97`  
		Last Modified: Wed, 08 Jan 2025 18:32:19 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5a79c20f9a4d5398a70916006a7072635de2ff930aa82abd78dabc001a1ba7`  
		Last Modified: Wed, 08 Jan 2025 18:32:19 GMT  
		Size: 701.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9` - unknown; unknown

```console
$ docker pull eggdrop@sha256:75091d6520884aacfd27531393d793fd9bac148cde39092f8abf21539385b66d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6547df7c2f273d686f5a4035607c4991f4b7a774d933c5ea7345620b77c7799`

```dockerfile
```

-	Layers:
	-	`sha256:7121465d4eb29da0a7a93530351da79ec1d3a020b31bb8ababfb4e79c647cc85`  
		Last Modified: Wed, 08 Jan 2025 18:32:18 GMT  
		Size: 19.2 KB (19240 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.9` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:5610f135bd127953fe6f706d4439d556429d00fdb160332bb2c1318f29e1d85b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12412480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce64ec01302097cc50a0deeaca22ed8dd142866d945e7e7dbe6f3cbdb9971630`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 15:14:19 GMT
RUN adduser -S eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache tcl bash openssl # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:14:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:14:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:14:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:14:19 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:14:19 GMT
COPY entrypoint.sh /home/eggdrop/eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
COPY docker.tcl /home/eggdrop/eggdrop/scripts/ # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Wed, 08 Jan 2025 17:24:18 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47bfaca725747041c04ef1167aa50d2f257273f3cc6611b25e3ebce979c3f1d`  
		Last Modified: Wed, 08 Jan 2025 18:31:15 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b59e2be77d1625e509771c4af6bdadd99bc0cdddd655f66b087b0699064c56`  
		Last Modified: Wed, 08 Jan 2025 18:31:15 GMT  
		Size: 11.4 KB (11357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fd549be4e37dd227f8730272a4cbd1503a4af2d47d7144f1efa5d054ee67f6`  
		Last Modified: Wed, 08 Jan 2025 18:31:15 GMT  
		Size: 3.0 MB (3020982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72131c69e4a90397290762eb3291cc6c2f161f1746cebadb084bc184cde44b5`  
		Last Modified: Wed, 08 Jan 2025 18:31:16 GMT  
		Size: 6.0 MB (6015801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a474e53b7ce1a6907eb3e8b3d75b1603467ea01bc958acdbf1947535c7178830`  
		Last Modified: Wed, 08 Jan 2025 18:31:16 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15803245b4e7d441711dd06f9c265cb3f27ed0d26dddb5254306ecc0bd5bf7dc`  
		Last Modified: Wed, 08 Jan 2025 18:31:16 GMT  
		Size: 700.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9` - unknown; unknown

```console
$ docker pull eggdrop@sha256:a8acb84e8b09b9b4d0008e2467ec6f5f7cc04f76a04c606c01e1bfc012eab269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1062695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976f97d274b1fe513b3cef4b93d39c80bcf6740e70e869607b027a829db71f69`

```dockerfile
```

-	Layers:
	-	`sha256:4c082c9c08d3e26d2c5ff19030c9c387b45af131547bc357d6afe7dd833e2964`  
		Last Modified: Wed, 08 Jan 2025 18:31:15 GMT  
		Size: 1.0 MB (1043214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c04cf3a6c835d8c3f0e3177b391c107a8e16a312d8df8a54f59702ebcc0e64a`  
		Last Modified: Wed, 08 Jan 2025 18:31:15 GMT  
		Size: 19.5 KB (19481 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:1.9.5`

```console
$ docker pull eggdrop@sha256:35805191134f5fdbbea8b5c2e33060d079b1c504c4b9b04dbbd3bfb1c72b827d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:1.9.5` - linux; amd64

```console
$ docker pull eggdrop@sha256:18010ff34267435ece22921511c072f362e499fb1139be5a00386abd256a2202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12285296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702c1bdd52b4b377889e7b0e9c29040afe0cfb233a550cff2f8828063a80247c`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 15:14:19 GMT
RUN adduser -S eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache tcl bash openssl # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:14:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:14:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:14:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:14:19 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:14:19 GMT
COPY entrypoint.sh /home/eggdrop/eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
COPY docker.tcl /home/eggdrop/eggdrop/scripts/ # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ff7ee5a95c455915fb1fbbb11b9b4d02b120ee128c9208ee5d816be1348b90`  
		Last Modified: Wed, 08 Jan 2025 18:02:25 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f7943a30c406824a5c967253b593622addd3ef529d0776e1f9a6c4578dc917`  
		Last Modified: Wed, 08 Jan 2025 18:02:25 GMT  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbac46b60b34452978aa607da72b295b333dc06881c24847a9a9065e47083913`  
		Last Modified: Wed, 08 Jan 2025 18:02:25 GMT  
		Size: 2.9 MB (2886343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd269a60e7f25046f13363305d3db9e0fc0ec5f9848d25d0d91152ce178d1f0`  
		Last Modified: Wed, 08 Jan 2025 18:02:25 GMT  
		Size: 6.0 MB (5964075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53aa1a98d14557559aa069805873f0890809e623669b4008fb6823ab38fa9664`  
		Last Modified: Wed, 08 Jan 2025 18:02:26 GMT  
		Size: 1.8 KB (1828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0727f149e66b0e76fbda20fe8f063a3fa6a5b7ad18de19e17acae904f9c3afc0`  
		Last Modified: Wed, 08 Jan 2025 18:02:26 GMT  
		Size: 697.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9.5` - unknown; unknown

```console
$ docker pull eggdrop@sha256:493b85ac76da1bcc95193717c82e0875db62866c4db9d613a22cf5ccbd217607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1062538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf4d82d7ad2da3002f92e99b0e939dee3dac6777419f370e1bbeda0cf86c336`

```dockerfile
```

-	Layers:
	-	`sha256:473cb128e980cf6fd88ea4f6bcf56a729db68d465e3f67ec3207990faf5ed600`  
		Last Modified: Wed, 08 Jan 2025 18:02:25 GMT  
		Size: 1.0 MB (1043182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f52ffe3e57422c2bbe9d7f8034c9064b1a3e5a615d54f062bb835181863f8d43`  
		Last Modified: Wed, 08 Jan 2025 18:02:25 GMT  
		Size: 19.4 KB (19356 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.9.5` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:a60f5adceeb4522e0ccdf30292032eca3eb516a9cdf0aa616976835e20db0cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11940483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b360698b8a9eb90311e0b210f2554a3ed7ab36f1b64c722a8def98bab6cd28`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.6-armhf.tar.gz / # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 15:14:19 GMT
RUN adduser -S eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache tcl bash openssl # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:14:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:14:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:14:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:14:19 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:14:19 GMT
COPY entrypoint.sh /home/eggdrop/eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
COPY docker.tcl /home/eggdrop/eggdrop/scripts/ # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:bfff14c232517ab149a6524fba444f7b5a336feab49d08abd27455f12ceb2efc`  
		Last Modified: Wed, 08 Jan 2025 17:24:09 GMT  
		Size: 3.2 MB (3176999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1943658bb1f5aa40f8fb6a5a2d03bed28a28a4c2ca25515867ddd8e91a708f`  
		Last Modified: Wed, 08 Jan 2025 18:32:18 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4901e5ef91acfad3b9b49b7efd5ea010d98368973c1246ba49d70c3d746e2d`  
		Last Modified: Wed, 08 Jan 2025 18:32:18 GMT  
		Size: 11.0 KB (10964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50db5a6d0511046c91accd10af4cd56efe341f1294ba452a9958e502fa5037d6`  
		Last Modified: Wed, 08 Jan 2025 18:32:18 GMT  
		Size: 2.9 MB (2889091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef9badf636f5ee159fe3ff62bba8df1f27567145299049d92db505871afa32b`  
		Last Modified: Wed, 08 Jan 2025 18:32:19 GMT  
		Size: 5.9 MB (5859616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84d9215cd3b358f1614835943a80c85bfae214d11d10a0fd5aaab412b61bb97`  
		Last Modified: Wed, 08 Jan 2025 18:32:19 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5a79c20f9a4d5398a70916006a7072635de2ff930aa82abd78dabc001a1ba7`  
		Last Modified: Wed, 08 Jan 2025 18:32:19 GMT  
		Size: 701.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9.5` - unknown; unknown

```console
$ docker pull eggdrop@sha256:75091d6520884aacfd27531393d793fd9bac148cde39092f8abf21539385b66d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6547df7c2f273d686f5a4035607c4991f4b7a774d933c5ea7345620b77c7799`

```dockerfile
```

-	Layers:
	-	`sha256:7121465d4eb29da0a7a93530351da79ec1d3a020b31bb8ababfb4e79c647cc85`  
		Last Modified: Wed, 08 Jan 2025 18:32:18 GMT  
		Size: 19.2 KB (19240 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.9.5` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:5610f135bd127953fe6f706d4439d556429d00fdb160332bb2c1318f29e1d85b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12412480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce64ec01302097cc50a0deeaca22ed8dd142866d945e7e7dbe6f3cbdb9971630`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 15:14:19 GMT
RUN adduser -S eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache tcl bash openssl # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:14:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:14:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:14:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:14:19 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:14:19 GMT
COPY entrypoint.sh /home/eggdrop/eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
COPY docker.tcl /home/eggdrop/eggdrop/scripts/ # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Wed, 08 Jan 2025 17:24:18 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47bfaca725747041c04ef1167aa50d2f257273f3cc6611b25e3ebce979c3f1d`  
		Last Modified: Wed, 08 Jan 2025 18:31:15 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b59e2be77d1625e509771c4af6bdadd99bc0cdddd655f66b087b0699064c56`  
		Last Modified: Wed, 08 Jan 2025 18:31:15 GMT  
		Size: 11.4 KB (11357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fd549be4e37dd227f8730272a4cbd1503a4af2d47d7144f1efa5d054ee67f6`  
		Last Modified: Wed, 08 Jan 2025 18:31:15 GMT  
		Size: 3.0 MB (3020982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72131c69e4a90397290762eb3291cc6c2f161f1746cebadb084bc184cde44b5`  
		Last Modified: Wed, 08 Jan 2025 18:31:16 GMT  
		Size: 6.0 MB (6015801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a474e53b7ce1a6907eb3e8b3d75b1603467ea01bc958acdbf1947535c7178830`  
		Last Modified: Wed, 08 Jan 2025 18:31:16 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15803245b4e7d441711dd06f9c265cb3f27ed0d26dddb5254306ecc0bd5bf7dc`  
		Last Modified: Wed, 08 Jan 2025 18:31:16 GMT  
		Size: 700.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9.5` - unknown; unknown

```console
$ docker pull eggdrop@sha256:a8acb84e8b09b9b4d0008e2467ec6f5f7cc04f76a04c606c01e1bfc012eab269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1062695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976f97d274b1fe513b3cef4b93d39c80bcf6740e70e869607b027a829db71f69`

```dockerfile
```

-	Layers:
	-	`sha256:4c082c9c08d3e26d2c5ff19030c9c387b45af131547bc357d6afe7dd833e2964`  
		Last Modified: Wed, 08 Jan 2025 18:31:15 GMT  
		Size: 1.0 MB (1043214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c04cf3a6c835d8c3f0e3177b391c107a8e16a312d8df8a54f59702ebcc0e64a`  
		Last Modified: Wed, 08 Jan 2025 18:31:15 GMT  
		Size: 19.5 KB (19481 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:5ecef503547b119fcf74cf2b6ea0fbf37ee13edd0b7db7b4ef8c4930a048f44d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:dabfcf059c265dce23afcf0c50c74d50885f34e80ef2e479c8341a7f29947132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12783005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:635ee8f865d9b80af29f2b6e0bd723d6223902e8ec9cf3317a40bbe5a507d5fd`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 03 Feb 2025 02:59:38 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Mon, 03 Feb 2025 02:59:38 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENV EGGDROP_SHA256=e42668f102c1446901b066d13fe0bf39622afca8d723f356ac2390d5faaf6e5e
# Mon, 03 Feb 2025 02:59:38 GMT
ENV EGGDROP_COMMIT=541e8ac17e549a40e177b5eea54e4abf24629a33
# Mon, 03 Feb 2025 02:59:38 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENV NICK=
# Mon, 03 Feb 2025 02:59:38 GMT
ENV SERVER=
# Mon, 03 Feb 2025 02:59:38 GMT
ENV LISTEN=3333
# Mon, 03 Feb 2025 02:59:38 GMT
ENV USERFILE=eggdrop.user
# Mon, 03 Feb 2025 02:59:38 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 03 Feb 2025 02:59:38 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 03 Feb 2025 02:59:38 GMT
EXPOSE map[3333/tcp:{}]
# Mon, 03 Feb 2025 02:59:38 GMT
COPY entrypoint.sh ./ # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
COPY docker.tcl ./scripts/ # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 03 Feb 2025 02:59:38 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122c69717639f8f256364490094110a9b1d7df56ceeb8b13a8d1b39f244d6f0c`  
		Last Modified: Mon, 03 Feb 2025 21:31:41 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8bde30c3b94071f7844cf5bb2e2274e51f5cceb7ef5f197a271fa8c83a24de`  
		Last Modified: Mon, 03 Feb 2025 21:31:40 GMT  
		Size: 1.1 MB (1115812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec388b64790efbb9db340f4dc80ff4899a6b71a814c8a2168c0234e8f3d0cbd`  
		Last Modified: Mon, 03 Feb 2025 21:31:41 GMT  
		Size: 8.0 MB (8021396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c05351390994af83d27d0cba64c41501ae8fcf9416e81e1b1b55b59e2d6dce0`  
		Last Modified: Mon, 03 Feb 2025 21:31:41 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bf7b3a5bc3a95ed12410f09561e43d7e4988b7f1d4c1eb977f77c40ac144bb`  
		Last Modified: Mon, 03 Feb 2025 21:31:41 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:d7733f68b9587cc8ddd5d0a5e87d4ae804c4f8fadef4db20b2e83f1fb595d6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 KB (157998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8375dc6928b79c66f37f6fd0966f5576446a8176af47e4ddf851b92e3a5e100c`

```dockerfile
```

-	Layers:
	-	`sha256:f6e3eac3c72850023dd63fa450bacdeda03c45f90b1e71b8592b5eb3b99d0b32`  
		Last Modified: Mon, 03 Feb 2025 21:31:40 GMT  
		Size: 140.9 KB (140907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caaf4736ea1b75742ee2d3123aba3def171951d2e2bf457400e8fe104a48574d`  
		Last Modified: Mon, 03 Feb 2025 21:31:40 GMT  
		Size: 17.1 KB (17091 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:1cdf139a4989d2ad5ffd7ed840d1697d4ffb35cf76e617d89c6bb3ad12ff8d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12335343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:465ec1c7e929eb858e0c6bf6914b06ac69ca9fec1f8948ff74f8d539d0240dc1`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 03 Feb 2025 02:59:38 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Mon, 03 Feb 2025 02:59:38 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENV EGGDROP_SHA256=e42668f102c1446901b066d13fe0bf39622afca8d723f356ac2390d5faaf6e5e
# Mon, 03 Feb 2025 02:59:38 GMT
ENV EGGDROP_COMMIT=541e8ac17e549a40e177b5eea54e4abf24629a33
# Mon, 03 Feb 2025 02:59:38 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENV NICK=
# Mon, 03 Feb 2025 02:59:38 GMT
ENV SERVER=
# Mon, 03 Feb 2025 02:59:38 GMT
ENV LISTEN=3333
# Mon, 03 Feb 2025 02:59:38 GMT
ENV USERFILE=eggdrop.user
# Mon, 03 Feb 2025 02:59:38 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 03 Feb 2025 02:59:38 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 03 Feb 2025 02:59:38 GMT
EXPOSE map[3333/tcp:{}]
# Mon, 03 Feb 2025 02:59:38 GMT
COPY entrypoint.sh ./ # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
COPY docker.tcl ./scripts/ # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 03 Feb 2025 02:59:38 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8f92d7debdb4d79633eeee7d89d5ec7468cde32925a38203f69b85781f316c`  
		Last Modified: Mon, 03 Feb 2025 21:32:10 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15725b51278e03d3c324719d25c1799bd692ea6b3b003c819fb6d28a8893325`  
		Last Modified: Mon, 03 Feb 2025 21:32:11 GMT  
		Size: 1.1 MB (1128397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a804f50c83cd24a866317a2805d790c695557d5e51454e82b1f2ff6ca44d58`  
		Last Modified: Mon, 03 Feb 2025 21:32:11 GMT  
		Size: 7.8 MB (7838980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0603e1c6d079da7203b313e2436309b43dac0c1e80b5d16cc4ad992f099526dc`  
		Last Modified: Mon, 03 Feb 2025 21:32:10 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5395b5804db45aeffd996b34b5d4aada3319ae0e66fd60bbd416b8e010d8269d`  
		Last Modified: Mon, 03 Feb 2025 21:32:11 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:b751bbe2e315c71ea63cbac948079d70650b5bb5ef935c5ae90b66dca64f1c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (16954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd816744d1b75356db445fe3e76d4067145ac6730d2bb7c8b78a36ef0a724ce`

```dockerfile
```

-	Layers:
	-	`sha256:2893f80852f7c4cfcb5dfb30ebe9bfda73be170ef50f0e8b619914742f940594`  
		Last Modified: Mon, 03 Feb 2025 21:32:10 GMT  
		Size: 17.0 KB (16954 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:50d1d13c591a6216d72854f73613b558524d8bafc2546b227efbda6676ea0f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13234211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fee526bbe500fb6844da3a7e43ee8483a0177f94d0e2d9b70b71bdc43fe4f59`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 03 Feb 2025 02:59:38 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Mon, 03 Feb 2025 02:59:38 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENV EGGDROP_SHA256=e42668f102c1446901b066d13fe0bf39622afca8d723f356ac2390d5faaf6e5e
# Mon, 03 Feb 2025 02:59:38 GMT
ENV EGGDROP_COMMIT=541e8ac17e549a40e177b5eea54e4abf24629a33
# Mon, 03 Feb 2025 02:59:38 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENV NICK=
# Mon, 03 Feb 2025 02:59:38 GMT
ENV SERVER=
# Mon, 03 Feb 2025 02:59:38 GMT
ENV LISTEN=3333
# Mon, 03 Feb 2025 02:59:38 GMT
ENV USERFILE=eggdrop.user
# Mon, 03 Feb 2025 02:59:38 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 03 Feb 2025 02:59:38 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 03 Feb 2025 02:59:38 GMT
EXPOSE map[3333/tcp:{}]
# Mon, 03 Feb 2025 02:59:38 GMT
COPY entrypoint.sh ./ # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
COPY docker.tcl ./scripts/ # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 03 Feb 2025 02:59:38 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51e44dcc35225de03a01a04dd3e872ead2ffb431dc6ea6c1ba4642baad081cb`  
		Last Modified: Mon, 03 Feb 2025 21:31:20 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374bceaeb5647a8e79c93eb68141d61aef47d1ec39c4b5e070cbc625038eb685`  
		Last Modified: Mon, 03 Feb 2025 21:31:20 GMT  
		Size: 1.2 MB (1169751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d19e42b835cfdd5d7e7d74a70e38e8da5b9cf7d88f72c2abc258b9bf27ffbf`  
		Last Modified: Mon, 03 Feb 2025 21:31:20 GMT  
		Size: 8.1 MB (8068017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891218d2ab450d92507655dc2bb8596d02036d1d381bab3f4a91c9c7ed164e77`  
		Last Modified: Mon, 03 Feb 2025 21:31:20 GMT  
		Size: 2.0 KB (1965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481bb921d265f236b4768010107ea10865418f0cc106017acc03c6d2dc445352`  
		Last Modified: Mon, 03 Feb 2025 21:31:21 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:ef72f33e2126e4aa7cd68ce36a068846df8f098681e61771ce8762068d97bc3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 KB (158116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5b370b58af939337011efb63acac525614c4b3b8864b23af1462e04fea6edc`

```dockerfile
```

-	Layers:
	-	`sha256:4a4c3057aea11e609e871a2c9333907c8d57d60e1d21cc1ad69ee12ff99c0ebd`  
		Last Modified: Mon, 03 Feb 2025 21:31:20 GMT  
		Size: 140.9 KB (140927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dffef19ea40c320b1ea56d51134fea4040cb324076b72d92c2b1b21c93aa9dba`  
		Last Modified: Mon, 03 Feb 2025 21:31:20 GMT  
		Size: 17.2 KB (17189 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:570dd216d64c15b27c2366a02b116a485ae5ee028776eb39a4cbf1a2778fdda6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:820390da349548b8337d027e2000a1bdc308c62846bfebe9125722405fb9f39d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17468949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c172d56253fb7af7a3b6b9f46833e567e9ca3b97206620053138b88ac075b1f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba2ed38a951eb3af32798f4d632878bfc543836ccdfc2a299b726d2ffa8af85`  
		Last Modified: Wed, 08 Jan 2025 18:01:40 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf4724448b76a36bb76ea1cd392295fd5cbb512c33b2a9b8744af84634e3666`  
		Last Modified: Wed, 08 Jan 2025 18:01:41 GMT  
		Size: 1.1 MB (1115390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0cd364521d7ca48a805725251ca95989e8ff839bdaa2e323608e7e949d7181`  
		Last Modified: Wed, 08 Jan 2025 18:01:41 GMT  
		Size: 12.7 MB (12723237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20c8212b54ec5591eacc689e1d3613b7394d54130c90ff3abca14efb6d58de`  
		Last Modified: Wed, 08 Jan 2025 18:01:41 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbd7f44f61763e498f90f16c646aec872fb647c583e46d78fec5dc0e1be0dd2`  
		Last Modified: Wed, 08 Jan 2025 18:01:41 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:953774f40b106af1fb32fc5840952957544cc328a8c873875ad1ed8c84ee4d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 KB (157534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3267f0d8d58865a7a4b11dc973db9b5bdffdc32767e819d14c98fee65f8445`

```dockerfile
```

-	Layers:
	-	`sha256:a6c1711e8758aff9f23949489545f3eb136bd7336e552527b890e876610cda6d`  
		Last Modified: Wed, 08 Jan 2025 18:01:41 GMT  
		Size: 138.8 KB (138764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:461222170f6bcc43f749f025f1ddbafbaba23c1082414c82b3009f504e75b31a`  
		Last Modified: Wed, 08 Jan 2025 18:01:40 GMT  
		Size: 18.8 KB (18770 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:f83091be92b257d32fbf9c6fbed21ddcbacfd84e543ef17e291fb35d93a67ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17076901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5298cdfde50ed0b9ad37404d68d023aa2e6618976d7fd155e9ccbb491b7b4ed`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Wed, 08 Jan 2025 17:23:56 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e221ba7d901e5b2e4c8a1cc65e81852346141765a956648846f7d2049f8aaaf2`  
		Last Modified: Wed, 08 Jan 2025 18:27:42 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b64f124a8a5d0a4109f8450d26288172a7a8b83e46c5133671247535a592e9`  
		Last Modified: Wed, 08 Jan 2025 18:27:43 GMT  
		Size: 1.1 MB (1129563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56747594a231ad7e35932c7a593d8e8be6665e62b0846cb767b09851fc0a5b16`  
		Last Modified: Wed, 08 Jan 2025 18:35:15 GMT  
		Size: 12.6 MB (12571789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabdbac5ec70e76518d884961bf2de5ab29bc374211dcac4dd125c9a174aea11`  
		Last Modified: Wed, 08 Jan 2025 18:35:15 GMT  
		Size: 2.0 KB (1954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1f1bc39af4850d7724b277099c16b2106b9c52eb5b3e56cf1c9cc7047ab1cf`  
		Last Modified: Wed, 08 Jan 2025 18:35:15 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:62366f69b54d5b7ee6b5ea97eac8b06acb3f22f0700e45dbafc32fb1204dc1c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e93ea81bc9ef8cc048bc0d811b744e45a3afee33ba7bf52edf66531a84f0e4`

```dockerfile
```

-	Layers:
	-	`sha256:c3336b8b867d566db0bc930345a3f0de1c70268b7323313acb1e1bc84c4e228f`  
		Last Modified: Wed, 08 Jan 2025 18:35:14 GMT  
		Size: 18.7 KB (18658 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:1e3e94175c6136b2956448a704ce185695b7ab4729803be8e617363dcfd848c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18162740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c2704a4b05e703b2b23b81be75bf14fe7a146b79e8021878d3b411e8b68b8e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dc5771b4cb21ae2a2bab536d6a359970cd3a34e970a8a0be98e54d192f0664`  
		Last Modified: Wed, 08 Jan 2025 18:27:31 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8917a57a55679bb3082cea769355873fc8ae45ab8caf5e990029718b232ebe0c`  
		Last Modified: Wed, 08 Jan 2025 18:27:31 GMT  
		Size: 1.2 MB (1210974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00fc1a13bfd6d68eac9dd7761eac4c9317710affb065542d15c60aa69086a0a`  
		Last Modified: Wed, 08 Jan 2025 18:33:30 GMT  
		Size: 12.9 MB (12856924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46884e96140c161c4efa5d4cab995e341b9592400c3db5132d42137071b8da65`  
		Last Modified: Wed, 08 Jan 2025 18:33:29 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b7d440051ff64a186a5311fc066136cb5ebe2e2a06cd80619f0e966f75f949`  
		Last Modified: Wed, 08 Jan 2025 18:33:29 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:2d3191ee6478001199b48d737e375c8b2c545afd95c27da9f3811e7c62a02069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 KB (157725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9fcd7346d6d369651db6daa73a39ff635ebdb30d0ab64e80e7b5c5376a41a6f`

```dockerfile
```

-	Layers:
	-	`sha256:cd130b0889db81d55044ee726aef57927b6ecd401b41b4a8d123884204ae76b5`  
		Last Modified: Wed, 08 Jan 2025 18:33:29 GMT  
		Size: 138.8 KB (138820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b175d71afcc8d14c978a6331b8d3e56ea315b810c7207d64a01644920795c0`  
		Last Modified: Wed, 08 Jan 2025 18:33:29 GMT  
		Size: 18.9 KB (18905 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:570dd216d64c15b27c2366a02b116a485ae5ee028776eb39a4cbf1a2778fdda6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:820390da349548b8337d027e2000a1bdc308c62846bfebe9125722405fb9f39d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17468949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c172d56253fb7af7a3b6b9f46833e567e9ca3b97206620053138b88ac075b1f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba2ed38a951eb3af32798f4d632878bfc543836ccdfc2a299b726d2ffa8af85`  
		Last Modified: Wed, 08 Jan 2025 18:01:40 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf4724448b76a36bb76ea1cd392295fd5cbb512c33b2a9b8744af84634e3666`  
		Last Modified: Wed, 08 Jan 2025 18:01:41 GMT  
		Size: 1.1 MB (1115390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0cd364521d7ca48a805725251ca95989e8ff839bdaa2e323608e7e949d7181`  
		Last Modified: Wed, 08 Jan 2025 18:01:41 GMT  
		Size: 12.7 MB (12723237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20c8212b54ec5591eacc689e1d3613b7394d54130c90ff3abca14efb6d58de`  
		Last Modified: Wed, 08 Jan 2025 18:01:41 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbd7f44f61763e498f90f16c646aec872fb647c583e46d78fec5dc0e1be0dd2`  
		Last Modified: Wed, 08 Jan 2025 18:01:41 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:953774f40b106af1fb32fc5840952957544cc328a8c873875ad1ed8c84ee4d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 KB (157534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3267f0d8d58865a7a4b11dc973db9b5bdffdc32767e819d14c98fee65f8445`

```dockerfile
```

-	Layers:
	-	`sha256:a6c1711e8758aff9f23949489545f3eb136bd7336e552527b890e876610cda6d`  
		Last Modified: Wed, 08 Jan 2025 18:01:41 GMT  
		Size: 138.8 KB (138764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:461222170f6bcc43f749f025f1ddbafbaba23c1082414c82b3009f504e75b31a`  
		Last Modified: Wed, 08 Jan 2025 18:01:40 GMT  
		Size: 18.8 KB (18770 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:f83091be92b257d32fbf9c6fbed21ddcbacfd84e543ef17e291fb35d93a67ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17076901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5298cdfde50ed0b9ad37404d68d023aa2e6618976d7fd155e9ccbb491b7b4ed`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Wed, 08 Jan 2025 17:23:56 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e221ba7d901e5b2e4c8a1cc65e81852346141765a956648846f7d2049f8aaaf2`  
		Last Modified: Wed, 08 Jan 2025 18:27:42 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b64f124a8a5d0a4109f8450d26288172a7a8b83e46c5133671247535a592e9`  
		Last Modified: Wed, 08 Jan 2025 18:27:43 GMT  
		Size: 1.1 MB (1129563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56747594a231ad7e35932c7a593d8e8be6665e62b0846cb767b09851fc0a5b16`  
		Last Modified: Wed, 08 Jan 2025 18:35:15 GMT  
		Size: 12.6 MB (12571789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabdbac5ec70e76518d884961bf2de5ab29bc374211dcac4dd125c9a174aea11`  
		Last Modified: Wed, 08 Jan 2025 18:35:15 GMT  
		Size: 2.0 KB (1954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1f1bc39af4850d7724b277099c16b2106b9c52eb5b3e56cf1c9cc7047ab1cf`  
		Last Modified: Wed, 08 Jan 2025 18:35:15 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:62366f69b54d5b7ee6b5ea97eac8b06acb3f22f0700e45dbafc32fb1204dc1c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e93ea81bc9ef8cc048bc0d811b744e45a3afee33ba7bf52edf66531a84f0e4`

```dockerfile
```

-	Layers:
	-	`sha256:c3336b8b867d566db0bc930345a3f0de1c70268b7323313acb1e1bc84c4e228f`  
		Last Modified: Wed, 08 Jan 2025 18:35:14 GMT  
		Size: 18.7 KB (18658 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:1e3e94175c6136b2956448a704ce185695b7ab4729803be8e617363dcfd848c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18162740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c2704a4b05e703b2b23b81be75bf14fe7a146b79e8021878d3b411e8b68b8e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dc5771b4cb21ae2a2bab536d6a359970cd3a34e970a8a0be98e54d192f0664`  
		Last Modified: Wed, 08 Jan 2025 18:27:31 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8917a57a55679bb3082cea769355873fc8ae45ab8caf5e990029718b232ebe0c`  
		Last Modified: Wed, 08 Jan 2025 18:27:31 GMT  
		Size: 1.2 MB (1210974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00fc1a13bfd6d68eac9dd7761eac4c9317710affb065542d15c60aa69086a0a`  
		Last Modified: Wed, 08 Jan 2025 18:33:30 GMT  
		Size: 12.9 MB (12856924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46884e96140c161c4efa5d4cab995e341b9592400c3db5132d42137071b8da65`  
		Last Modified: Wed, 08 Jan 2025 18:33:29 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b7d440051ff64a186a5311fc066136cb5ebe2e2a06cd80619f0e966f75f949`  
		Last Modified: Wed, 08 Jan 2025 18:33:29 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:2d3191ee6478001199b48d737e375c8b2c545afd95c27da9f3811e7c62a02069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 KB (157725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9fcd7346d6d369651db6daa73a39ff635ebdb30d0ab64e80e7b5c5376a41a6f`

```dockerfile
```

-	Layers:
	-	`sha256:cd130b0889db81d55044ee726aef57927b6ecd401b41b4a8d123884204ae76b5`  
		Last Modified: Wed, 08 Jan 2025 18:33:29 GMT  
		Size: 138.8 KB (138820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b175d71afcc8d14c978a6331b8d3e56ea315b810c7207d64a01644920795c0`  
		Last Modified: Wed, 08 Jan 2025 18:33:29 GMT  
		Size: 18.9 KB (18905 bytes)  
		MIME: application/vnd.in-toto+json
