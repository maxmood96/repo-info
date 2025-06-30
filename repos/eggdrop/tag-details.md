<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.10`](#eggdrop110)
-	[`eggdrop:1.10.0`](#eggdrop1100)
-	[`eggdrop:1.10.1rc1`](#eggdrop1101rc1)
-	[`eggdrop:1.9`](#eggdrop19)
-	[`eggdrop:1.9.5`](#eggdrop195)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.10`

```console
$ docker pull eggdrop@sha256:538cb8a3a26d486dbd78ebe4d1ab370e70973a1787fe56023aa1a5d57af318ab
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
$ docker pull eggdrop@sha256:31aba2be254a23fac1ca9df0ff7ed23c6f02cd9443e8a5d9126fef7d3c7bee18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17469999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d780465a6f218223949cbdd3131c8eccda6aaa5241371ad35bb98252c39c73e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b3444eeb09c629c9d3bcdbec5cf120853b2342308dfd0b5c460d5ba82a8622`  
		Last Modified: Fri, 14 Feb 2025 21:32:43 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8734443ac9c716799f545d89ccf8397a62a4f1f2af319a6aa04e85bceb4614`  
		Last Modified: Fri, 14 Feb 2025 21:32:43 GMT  
		Size: 1.1 MB (1115995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a208386598da099d59cdb929e35b8e54653564424b7e80bab5dc671ab1754d59`  
		Last Modified: Fri, 14 Feb 2025 21:32:44 GMT  
		Size: 12.7 MB (12723037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b2b70858cd562abe3c90891c3a80761170225aba0d29a6d6962363d2d56b22`  
		Last Modified: Fri, 14 Feb 2025 21:32:44 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba79086bb542341f7e4ffb7708cf8a107e8e8047abfd02d4b4878c24a317f46`  
		Last Modified: Fri, 14 Feb 2025 21:32:44 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10` - unknown; unknown

```console
$ docker pull eggdrop@sha256:3759dad3fd261cc3648714c96839890fbdd5f86a5b991c3ed9498ab08ae02dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 KB (157535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71faf331f37a788fdc348b5c53a68fb84db88b28a24a7c80e352c8c5eb6ad2e8`

```dockerfile
```

-	Layers:
	-	`sha256:d829d4c44533e372d3be0207c6b9adce61112450068b5e3e278eb043ddd6b4db`  
		Last Modified: Fri, 14 Feb 2025 21:30:21 GMT  
		Size: 138.8 KB (138764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56ebb2a93388b0529f8d2ed121d33bf2f35a8c376a332712e914d1a3d073384f`  
		Last Modified: Fri, 14 Feb 2025 21:30:21 GMT  
		Size: 18.8 KB (18771 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:c424dc7cc87f0fb02da042e36bc53a68d41237d871d583a4db7e9fa0a4e9a86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17078725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bb5d3553d651bd5cb523bbb122b336112f7e46312e75aa811231f8822d29d9`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
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
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 19:26:24 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5f5ebafbb9f2620b9c285aaede8b1c01410fa22db544ec4f8395ca66b6cd04`  
		Last Modified: Fri, 14 Feb 2025 21:30:32 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017b325b57e86dbac830719f76716817f84e81dad00dca0c78ecbc42ee10d704`  
		Last Modified: Fri, 14 Feb 2025 21:30:32 GMT  
		Size: 1.1 MB (1130373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5553baed849de0dced619d727239c90267a454e1d5082375d078bfedc1b65694`  
		Last Modified: Fri, 14 Feb 2025 21:30:33 GMT  
		Size: 12.6 MB (12571748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980845efd2922d60733f7e65dcfbb2556351dfb3591970c373d7bfd67798a65b`  
		Last Modified: Fri, 14 Feb 2025 21:30:32 GMT  
		Size: 2.0 KB (1951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30d6fc859cd8b7e9a6a4b46f6b7295071ba5c48ceb31a012a94caafc4507166`  
		Last Modified: Fri, 14 Feb 2025 21:30:32 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10` - unknown; unknown

```console
$ docker pull eggdrop@sha256:f54b495c9c22b0995def5f43ca925e63fd4b5854c332b06affb7245522809ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14913f8a5509822846bba45db715b832cc66b1f59b6de920c3d43bb3df359630`

```dockerfile
```

-	Layers:
	-	`sha256:aa90550c8b30a98ec74106530300ce5280cd706061d04406387bf47797628f97`  
		Last Modified: Fri, 14 Feb 2025 21:30:22 GMT  
		Size: 18.7 KB (18658 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:4035c5598844741674c04c76c922d8a7af24752fbc6788e8e9e6fbf59dd1b1d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18164152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7eb6d38e506b0c3ce3f15e5c7567ccad8fdff392d00179c87d4b2cc101445ef`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
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
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4f5e522137cc417a3f98ddcfca8b939a1bde2f1bfa06284389e632bd47f3dc`  
		Last Modified: Sat, 15 Feb 2025 02:01:23 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c5632ada7a032e4a40a385ac269d30d344dd48f333fa9490a2d9fddf33be97`  
		Last Modified: Sat, 15 Feb 2025 02:01:23 GMT  
		Size: 1.2 MB (1211974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16738349d7ac4181dbc287f636b71089e230b7b39a10bc59dbd3c275941d9b59`  
		Last Modified: Sat, 15 Feb 2025 02:01:24 GMT  
		Size: 12.9 MB (12856941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b878c75135710003b9e72ef4b408ab2f3c4ededfff0cf034a9351b9c3fdf74`  
		Last Modified: Sat, 15 Feb 2025 02:01:23 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d1412b27a55491a2489826aa90d806d17e53e4427a7f51f03086ebb8dd9304`  
		Last Modified: Sat, 15 Feb 2025 02:01:23 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10` - unknown; unknown

```console
$ docker pull eggdrop@sha256:7f123e51f800694ec3f3d2c2c46c6b1223181862a3c9b03ff4ed5fed4e051dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 KB (157724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c175b098b6ebbacf38438e2d9c1d4f6c6721baea7fb22b24ce757f60b5cc8f`

```dockerfile
```

-	Layers:
	-	`sha256:f4df0395fc7c5af9220eb15a11239d51fa69940e9ae3747f5f630e9f46edbbbc`  
		Last Modified: Sat, 15 Feb 2025 00:30:43 GMT  
		Size: 138.8 KB (138820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6f7123b133f1bbd79f1bb1a494afff036ed9f5373aa8f7dc72fa235be2e2f6d`  
		Last Modified: Sat, 15 Feb 2025 00:30:43 GMT  
		Size: 18.9 KB (18904 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:1.10.0`

```console
$ docker pull eggdrop@sha256:538cb8a3a26d486dbd78ebe4d1ab370e70973a1787fe56023aa1a5d57af318ab
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
$ docker pull eggdrop@sha256:31aba2be254a23fac1ca9df0ff7ed23c6f02cd9443e8a5d9126fef7d3c7bee18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17469999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d780465a6f218223949cbdd3131c8eccda6aaa5241371ad35bb98252c39c73e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b3444eeb09c629c9d3bcdbec5cf120853b2342308dfd0b5c460d5ba82a8622`  
		Last Modified: Fri, 14 Feb 2025 21:32:43 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8734443ac9c716799f545d89ccf8397a62a4f1f2af319a6aa04e85bceb4614`  
		Last Modified: Fri, 14 Feb 2025 21:32:43 GMT  
		Size: 1.1 MB (1115995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a208386598da099d59cdb929e35b8e54653564424b7e80bab5dc671ab1754d59`  
		Last Modified: Fri, 14 Feb 2025 21:32:44 GMT  
		Size: 12.7 MB (12723037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b2b70858cd562abe3c90891c3a80761170225aba0d29a6d6962363d2d56b22`  
		Last Modified: Fri, 14 Feb 2025 21:32:44 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba79086bb542341f7e4ffb7708cf8a107e8e8047abfd02d4b4878c24a317f46`  
		Last Modified: Fri, 14 Feb 2025 21:32:44 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.0` - unknown; unknown

```console
$ docker pull eggdrop@sha256:3759dad3fd261cc3648714c96839890fbdd5f86a5b991c3ed9498ab08ae02dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 KB (157535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71faf331f37a788fdc348b5c53a68fb84db88b28a24a7c80e352c8c5eb6ad2e8`

```dockerfile
```

-	Layers:
	-	`sha256:d829d4c44533e372d3be0207c6b9adce61112450068b5e3e278eb043ddd6b4db`  
		Last Modified: Fri, 14 Feb 2025 21:30:21 GMT  
		Size: 138.8 KB (138764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56ebb2a93388b0529f8d2ed121d33bf2f35a8c376a332712e914d1a3d073384f`  
		Last Modified: Fri, 14 Feb 2025 21:30:21 GMT  
		Size: 18.8 KB (18771 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10.0` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:c424dc7cc87f0fb02da042e36bc53a68d41237d871d583a4db7e9fa0a4e9a86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17078725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bb5d3553d651bd5cb523bbb122b336112f7e46312e75aa811231f8822d29d9`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
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
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 19:26:24 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5f5ebafbb9f2620b9c285aaede8b1c01410fa22db544ec4f8395ca66b6cd04`  
		Last Modified: Fri, 14 Feb 2025 21:30:32 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017b325b57e86dbac830719f76716817f84e81dad00dca0c78ecbc42ee10d704`  
		Last Modified: Fri, 14 Feb 2025 21:30:32 GMT  
		Size: 1.1 MB (1130373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5553baed849de0dced619d727239c90267a454e1d5082375d078bfedc1b65694`  
		Last Modified: Fri, 14 Feb 2025 21:30:33 GMT  
		Size: 12.6 MB (12571748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980845efd2922d60733f7e65dcfbb2556351dfb3591970c373d7bfd67798a65b`  
		Last Modified: Fri, 14 Feb 2025 21:30:32 GMT  
		Size: 2.0 KB (1951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30d6fc859cd8b7e9a6a4b46f6b7295071ba5c48ceb31a012a94caafc4507166`  
		Last Modified: Fri, 14 Feb 2025 21:30:32 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.0` - unknown; unknown

```console
$ docker pull eggdrop@sha256:f54b495c9c22b0995def5f43ca925e63fd4b5854c332b06affb7245522809ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14913f8a5509822846bba45db715b832cc66b1f59b6de920c3d43bb3df359630`

```dockerfile
```

-	Layers:
	-	`sha256:aa90550c8b30a98ec74106530300ce5280cd706061d04406387bf47797628f97`  
		Last Modified: Fri, 14 Feb 2025 21:30:22 GMT  
		Size: 18.7 KB (18658 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10.0` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:4035c5598844741674c04c76c922d8a7af24752fbc6788e8e9e6fbf59dd1b1d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18164152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7eb6d38e506b0c3ce3f15e5c7567ccad8fdff392d00179c87d4b2cc101445ef`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
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
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4f5e522137cc417a3f98ddcfca8b939a1bde2f1bfa06284389e632bd47f3dc`  
		Last Modified: Sat, 15 Feb 2025 02:01:23 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c5632ada7a032e4a40a385ac269d30d344dd48f333fa9490a2d9fddf33be97`  
		Last Modified: Sat, 15 Feb 2025 02:01:23 GMT  
		Size: 1.2 MB (1211974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16738349d7ac4181dbc287f636b71089e230b7b39a10bc59dbd3c275941d9b59`  
		Last Modified: Sat, 15 Feb 2025 02:01:24 GMT  
		Size: 12.9 MB (12856941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b878c75135710003b9e72ef4b408ab2f3c4ededfff0cf034a9351b9c3fdf74`  
		Last Modified: Sat, 15 Feb 2025 02:01:23 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d1412b27a55491a2489826aa90d806d17e53e4427a7f51f03086ebb8dd9304`  
		Last Modified: Sat, 15 Feb 2025 02:01:23 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.0` - unknown; unknown

```console
$ docker pull eggdrop@sha256:7f123e51f800694ec3f3d2c2c46c6b1223181862a3c9b03ff4ed5fed4e051dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 KB (157724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c175b098b6ebbacf38438e2d9c1d4f6c6721baea7fb22b24ce757f60b5cc8f`

```dockerfile
```

-	Layers:
	-	`sha256:f4df0395fc7c5af9220eb15a11239d51fa69940e9ae3747f5f630e9f46edbbbc`  
		Last Modified: Sat, 15 Feb 2025 00:30:43 GMT  
		Size: 138.8 KB (138820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6f7123b133f1bbd79f1bb1a494afff036ed9f5373aa8f7dc72fa235be2e2f6d`  
		Last Modified: Sat, 15 Feb 2025 00:30:43 GMT  
		Size: 18.9 KB (18904 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:1.10.1rc1`

```console
$ docker pull eggdrop@sha256:4e3f0a20c56fc31fede30a2e3375f5cabecef49b12a400326cadfad659155d5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:1.10.1rc1` - linux; amd64

```console
$ docker pull eggdrop@sha256:8985b83fb449798e5ed7a15f31c604b050257dd047478010ccadb6f997d5723c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12776225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ce477ac06bd37e542119ee5f6b28d4ebd0d8e8c007cb6525187502a74ca22c`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sun, 29 Jun 2025 14:54:46 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 29 Jun 2025 14:54:46 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 29 Jun 2025 14:54:46 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 29 Jun 2025 14:54:46 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1rc1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1rc1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1rc1.tar.gz.asc eggdrop-1.10.1rc1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.1rc1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1rc1.tar.gz   && rm eggdrop-1.10.1rc1.tar.gz   && ( cd eggdrop-1.10.1rc1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1rc1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 29 Jun 2025 14:54:46 GMT
ENV NICK=
# Sun, 29 Jun 2025 14:54:46 GMT
ENV SERVER=
# Sun, 29 Jun 2025 14:54:46 GMT
ENV LISTEN=3333
# Sun, 29 Jun 2025 14:54:46 GMT
ENV USERFILE=eggdrop.user
# Sun, 29 Jun 2025 14:54:46 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 29 Jun 2025 14:54:46 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 29 Jun 2025 14:54:46 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 29 Jun 2025 14:54:46 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 29 Jun 2025 14:54:46 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 29 Jun 2025 14:54:46 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 29 Jun 2025 14:54:46 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cdb6bb174e8810f69e54a475cfc17576c0103823588930f2b6f7813d76dd9ac`  
		Last Modified: Mon, 30 Jun 2025 17:30:27 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b0270297f1261f9dfdc90b518672581a1cd262f7cf68105b53eab0f8a63e0a`  
		Last Modified: Mon, 30 Jun 2025 17:30:27 GMT  
		Size: 1.1 MB (1116808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd4bfe2501474a799a240c1d4fca29c02c5059eaf7ed37d345e3611efae8151`  
		Last Modified: Mon, 30 Jun 2025 17:30:28 GMT  
		Size: 8.0 MB (8013080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f4f2c44bae8cd4a571432759d0a41e2a261f44157f5e611ccef5dd0dc7e010`  
		Last Modified: Mon, 30 Jun 2025 17:30:30 GMT  
		Size: 2.0 KB (1972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045038883a1b7740b3f41b482feab993c35b96c68b8e35edaa6f64a3438dce03`  
		Last Modified: Mon, 30 Jun 2025 17:30:27 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.1rc1` - unknown; unknown

```console
$ docker pull eggdrop@sha256:4d2884d7f34a2115aeae234b8271bee37e4d314b22a5b4cb298a93efddd8bd76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 KB (160568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8650ccba36411291f291140c97e6d5708891f6134b6ee4ef801a1ec7cbb94a37`

```dockerfile
```

-	Layers:
	-	`sha256:dd1b1be816145696ad0667acc57583c85833be681d9dd6e34ece282dde06f19a`  
		Last Modified: Mon, 30 Jun 2025 20:30:27 GMT  
		Size: 142.9 KB (142864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd97bbe4303c2d4c1bee1263d394af6c9f0840804b94656d8efd22e93efd9225`  
		Last Modified: Mon, 30 Jun 2025 20:30:28 GMT  
		Size: 17.7 KB (17704 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10.1rc1` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:d5c1aaddc36779b499ab2afed50b9c91b9b5d75034d0fabb8be346e752c0f66d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12330777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7610c88c80869dd68ce392082f60e4f15ac9de48e9015b7b7a1705aee183300`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sun, 29 Jun 2025 14:54:46 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 29 Jun 2025 14:54:46 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 29 Jun 2025 14:54:46 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 29 Jun 2025 14:54:46 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1rc1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1rc1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1rc1.tar.gz.asc eggdrop-1.10.1rc1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.1rc1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1rc1.tar.gz   && rm eggdrop-1.10.1rc1.tar.gz   && ( cd eggdrop-1.10.1rc1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1rc1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 29 Jun 2025 14:54:46 GMT
ENV NICK=
# Sun, 29 Jun 2025 14:54:46 GMT
ENV SERVER=
# Sun, 29 Jun 2025 14:54:46 GMT
ENV LISTEN=3333
# Sun, 29 Jun 2025 14:54:46 GMT
ENV USERFILE=eggdrop.user
# Sun, 29 Jun 2025 14:54:46 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 29 Jun 2025 14:54:46 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 29 Jun 2025 14:54:46 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 29 Jun 2025 14:54:46 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 29 Jun 2025 14:54:46 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 29 Jun 2025 14:54:46 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 29 Jun 2025 14:54:46 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc43811e2e53e4ae9b7973be733525f9c9ca18481dd12d34a7fd659226e9d7c`  
		Last Modified: Mon, 30 Jun 2025 17:30:56 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5493e76dae4e0ff11e5d72b6ac2f26a9996eade8680a566fb14d5ee19340f4`  
		Last Modified: Mon, 30 Jun 2025 17:30:57 GMT  
		Size: 1.1 MB (1129829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fa06515eab16b136963c2d61efadec391d698ab6f488fc402e5a95e4a2acce`  
		Last Modified: Mon, 30 Jun 2025 17:30:58 GMT  
		Size: 7.8 MB (7832138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b189ff4c237ea2345e5c0001842c597edb6e8731b7d9f12b3f3509e299b0131`  
		Last Modified: Mon, 30 Jun 2025 17:30:56 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5fe2df8fc8a2a1674e4dde518789bddc29eccdec29e9b0f52345e885225a71`  
		Last Modified: Mon, 30 Jun 2025 17:30:56 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.1rc1` - unknown; unknown

```console
$ docker pull eggdrop@sha256:9e4e943413e6f77e533e5e0b42cfaccc59e318043681a8f0cbac174d8ae1e616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 KB (17567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724d1c21bb62e94c30fb071b11c5da6cc031e6b073ead764edb60f8a1fa64ce4`

```dockerfile
```

-	Layers:
	-	`sha256:e14a32ff6be6de2c9879025263ab5a73700de3a4f70d5eeed6708402d4e5b5ed`  
		Last Modified: Mon, 30 Jun 2025 20:30:33 GMT  
		Size: 17.6 KB (17567 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10.1rc1` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:288a98b34c5144e049257ba511599d6acea83af72652520653e71640eca8b2f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13227206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031b1ca0c730d3e169d762c33aae45be674839baabd947314d8eb00f37082fc0`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sun, 29 Jun 2025 14:54:46 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 29 Jun 2025 14:54:46 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 29 Jun 2025 14:54:46 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 29 Jun 2025 14:54:46 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1rc1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1rc1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1rc1.tar.gz.asc eggdrop-1.10.1rc1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.1rc1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1rc1.tar.gz   && rm eggdrop-1.10.1rc1.tar.gz   && ( cd eggdrop-1.10.1rc1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1rc1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 29 Jun 2025 14:54:46 GMT
ENV NICK=
# Sun, 29 Jun 2025 14:54:46 GMT
ENV SERVER=
# Sun, 29 Jun 2025 14:54:46 GMT
ENV LISTEN=3333
# Sun, 29 Jun 2025 14:54:46 GMT
ENV USERFILE=eggdrop.user
# Sun, 29 Jun 2025 14:54:46 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 29 Jun 2025 14:54:46 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 29 Jun 2025 14:54:46 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 29 Jun 2025 14:54:46 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 29 Jun 2025 14:54:46 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 29 Jun 2025 14:54:46 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 29 Jun 2025 14:54:46 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a67b017a0ee37131e454a8b5f833c0d4cd87a3435da19d8f9f1fbee89a5e4e`  
		Last Modified: Mon, 30 Jun 2025 17:31:37 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d232aa641ee8beddf08ff91445200875942a158085b25c70f8ae5b0b727d55b1`  
		Last Modified: Mon, 30 Jun 2025 17:31:37 GMT  
		Size: 1.2 MB (1171079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244cb830c21448cd00b10fd2b9118e148fa1884daec61668329b0a6ceda31a5f`  
		Last Modified: Mon, 30 Jun 2025 17:31:41 GMT  
		Size: 8.1 MB (8059021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84daf522f4653650c7a10608894786e274d423542f28fe598e43040c7b97f638`  
		Last Modified: Mon, 30 Jun 2025 17:31:39 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e039efa44780e758e2152232c4f8dadacb2d91a43c53df1381995fb962dbf736`  
		Last Modified: Mon, 30 Jun 2025 17:31:39 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.1rc1` - unknown; unknown

```console
$ docker pull eggdrop@sha256:8f1c97fed287c1d18c016d3189e8310ef20dbff82fdc236dad6df16af65da666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 KB (160684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67380da602c17572b7a678de61e31293fa2e3ebac0fe641db44f71caf5e81f5b`

```dockerfile
```

-	Layers:
	-	`sha256:8d33120d3aefaa63c0dbd5765e8e9216ca08db4365fcfbe374e314c0e6c3cf6d`  
		Last Modified: Mon, 30 Jun 2025 20:30:37 GMT  
		Size: 142.9 KB (142884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad8e3881d90bdc5f57f136a6d2ead1a6e43988192fff9ed6b85af7c2ad87bed4`  
		Last Modified: Mon, 30 Jun 2025 20:30:37 GMT  
		Size: 17.8 KB (17800 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:1.9`

```console
$ docker pull eggdrop@sha256:972e5d56ee2deff8ddbf3c771725c066d58786819fc5b4244b58ee5e69f71aec
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
$ docker pull eggdrop@sha256:9f8684b61be46a4a4b4545cd374972b05cd850de670acbb04dfd7ba3ae4fb0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12286475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73364cea5c18f4f324ef30a2f0bac731b1290455117596176d1ddd9aa038cb70`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
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
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 14:30:10 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6c309dea210181dec5e17171108cdfb2333beb2405f141f0aa79d4fe36c906`  
		Last Modified: Sat, 15 Feb 2025 13:49:56 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dcc3df0ce6cb768c19a5022e397ff7cb0e0e695fffaacc5678d20a8d8a98b7`  
		Last Modified: Sat, 15 Feb 2025 13:49:55 GMT  
		Size: 10.8 KB (10826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209f6e4ea0aad39a14c57c7b865e0d480f4e7fc89d697ac756786b4449bb4247`  
		Last Modified: Sat, 15 Feb 2025 13:49:58 GMT  
		Size: 2.9 MB (2886703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854c6c8c83aeba9f53494777c719ea12835c6f942d3d605aa6fa9cf90a4c439c`  
		Last Modified: Sat, 15 Feb 2025 13:49:58 GMT  
		Size: 6.0 MB (5964271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413d8064b1b989db17fbebc9c81ca463d39a1b0847d84c9317cde54897103941`  
		Last Modified: Sat, 15 Feb 2025 13:49:58 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce68b2486e7a5448375bb0dd0846ea07c521b7d1581bd8b4ef2b550467fd3d7`  
		Last Modified: Sat, 15 Feb 2025 13:49:59 GMT  
		Size: 696.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9` - unknown; unknown

```console
$ docker pull eggdrop@sha256:41f352316b3cecc1dca2f0068c781af3551853f9a225f74db25023129cf4e3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1062538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eac3ea7cb823947a1ce58aad2b3843330fcf76548c7071da8648c757ccf01c7`

```dockerfile
```

-	Layers:
	-	`sha256:403d1051e657238e63a1b98c2c0986a62c90d8640ad20969ace3a8a36d435350`  
		Last Modified: Fri, 14 Feb 2025 21:30:30 GMT  
		Size: 1.0 MB (1043182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8c9a1ff32af0af5039728ae3a8a3618cf487898ebfcfeb9348c28caece5752c`  
		Last Modified: Fri, 14 Feb 2025 21:30:30 GMT  
		Size: 19.4 KB (19356 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:f10e1349bc98816a69d038ee688e24a87b1cdffda436b342793a6c6432df4424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11943848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894447f0f68cb4c271324608202415aea3bd42d6f1fb962849178f3e14a77e09`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.7-armhf.tar.gz / # buildkit
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
	-	`sha256:f5c2e5a96485e4eaf16caa456bdd06c183f55bf5a43c2e4532d5e8db8bfacaad`  
		Last Modified: Fri, 14 Feb 2025 19:25:37 GMT  
		Size: 3.2 MB (3177535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5a36525d0fcbba2920aa86c5064e7e1e14313fb5548ffc910085a5befd3dd7`  
		Last Modified: Fri, 14 Feb 2025 21:30:39 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3f904108af54640bea84ceddfd696a85893dd577db2afc08c8ea18af1dee6e`  
		Last Modified: Fri, 14 Feb 2025 21:30:39 GMT  
		Size: 11.0 KB (10956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94feb113c2bb41dd0efff24dd5d111680c7f8995c512221c5799d2beb1074c05`  
		Last Modified: Fri, 14 Feb 2025 21:30:39 GMT  
		Size: 2.9 MB (2891931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893117506eeb7e44af37eab08297f0c855c422b41d25f719daa9f15615489430`  
		Last Modified: Fri, 14 Feb 2025 21:30:40 GMT  
		Size: 5.9 MB (5859627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13555e9e4c43a47103ff3bc9f81263480912fb1cfa4ac9b8752f6d58e5fe0c0f`  
		Last Modified: Fri, 14 Feb 2025 21:30:40 GMT  
		Size: 1.8 KB (1829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a598dd8009a7496ba040c09d8b689adbc338567bb3cb2c349dcba041dfd50a94`  
		Last Modified: Fri, 14 Feb 2025 21:30:39 GMT  
		Size: 695.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9` - unknown; unknown

```console
$ docker pull eggdrop@sha256:2186239d930b0f7aba7d62f3ccf5d7b1d09ca043c6670ec8d83de5aa3f1590f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1baf361bc3b92bfff59c39ad039b269d10c12fe369749479b6fc380bbe0b58d9`

```dockerfile
```

-	Layers:
	-	`sha256:e5e4a6c5e4332277716397cf23fef0e3752776029e2f1abf19acf8715063c998`  
		Last Modified: Fri, 14 Feb 2025 21:30:32 GMT  
		Size: 19.2 KB (19240 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.9` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:71221b12a34f4afd052dec7a0ba6bac00f11d8f8d6d8b416bc6ab387a9eba32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12413682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06391f677a7f07b412e55209a4b0b3d0d9171d84baaae69193242fac6e5b9e78`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
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
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 14:31:17 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5e405d1b1d32ec2ea3cd7c4eaa746a0ad1a08bb9cb89ea1426833c906bc905`  
		Last Modified: Sat, 15 Feb 2025 03:30:14 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922022d41504f6d960abeb7ac90ea0f3165f03620c4c50ef7e69f5251ab4482c`  
		Last Modified: Sat, 15 Feb 2025 03:30:10 GMT  
		Size: 11.3 KB (11349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bb052d2efd871a6ab605c73a15f3623aaf5f0d395cef1b8e04656e75c676dd`  
		Last Modified: Sat, 15 Feb 2025 03:30:32 GMT  
		Size: 3.0 MB (3021436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee30b4ce5dc6de9512591fabfaa6761986b5e4a4d4219c00ff83badbaaef567`  
		Last Modified: Sat, 15 Feb 2025 03:30:34 GMT  
		Size: 6.0 MB (6015665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c7b229d78ea9859fb04eff273d89b99dc0df7ecad02c39985ba7bc84071a9`  
		Last Modified: Sat, 15 Feb 2025 03:30:30 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3f1cce52d7fa191ec3d160b9fc04bc18f59a5387a5208e966728c4960df1a0`  
		Last Modified: Sat, 15 Feb 2025 03:30:32 GMT  
		Size: 699.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9` - unknown; unknown

```console
$ docker pull eggdrop@sha256:9aa4cfa9ef03794d00ac4a43ad76be0ea5db78c20d8245434122fc66826bc1fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1062695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45cd0dd11840b8e339b7cb63b521dece5b2c27e6f454bbbef40a4c5caa6f62c8`

```dockerfile
```

-	Layers:
	-	`sha256:40c72dd854d99c91ef692d59d3d96dc7b6c0334a217cf2597910c95bf21cce76`  
		Last Modified: Sat, 15 Feb 2025 00:30:50 GMT  
		Size: 1.0 MB (1043214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f37e6ae2e1433c7e4c1faf9c13712dce853de3b0db13bae21736ed8aedea79c`  
		Last Modified: Sat, 15 Feb 2025 00:30:50 GMT  
		Size: 19.5 KB (19481 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:1.9.5`

```console
$ docker pull eggdrop@sha256:972e5d56ee2deff8ddbf3c771725c066d58786819fc5b4244b58ee5e69f71aec
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
$ docker pull eggdrop@sha256:9f8684b61be46a4a4b4545cd374972b05cd850de670acbb04dfd7ba3ae4fb0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12286475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73364cea5c18f4f324ef30a2f0bac731b1290455117596176d1ddd9aa038cb70`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
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
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 14:30:10 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6c309dea210181dec5e17171108cdfb2333beb2405f141f0aa79d4fe36c906`  
		Last Modified: Sat, 15 Feb 2025 13:49:56 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dcc3df0ce6cb768c19a5022e397ff7cb0e0e695fffaacc5678d20a8d8a98b7`  
		Last Modified: Sat, 15 Feb 2025 13:49:55 GMT  
		Size: 10.8 KB (10826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209f6e4ea0aad39a14c57c7b865e0d480f4e7fc89d697ac756786b4449bb4247`  
		Last Modified: Sat, 15 Feb 2025 13:49:58 GMT  
		Size: 2.9 MB (2886703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854c6c8c83aeba9f53494777c719ea12835c6f942d3d605aa6fa9cf90a4c439c`  
		Last Modified: Sat, 15 Feb 2025 13:49:58 GMT  
		Size: 6.0 MB (5964271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413d8064b1b989db17fbebc9c81ca463d39a1b0847d84c9317cde54897103941`  
		Last Modified: Sat, 15 Feb 2025 13:49:58 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce68b2486e7a5448375bb0dd0846ea07c521b7d1581bd8b4ef2b550467fd3d7`  
		Last Modified: Sat, 15 Feb 2025 13:49:59 GMT  
		Size: 696.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9.5` - unknown; unknown

```console
$ docker pull eggdrop@sha256:41f352316b3cecc1dca2f0068c781af3551853f9a225f74db25023129cf4e3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1062538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eac3ea7cb823947a1ce58aad2b3843330fcf76548c7071da8648c757ccf01c7`

```dockerfile
```

-	Layers:
	-	`sha256:403d1051e657238e63a1b98c2c0986a62c90d8640ad20969ace3a8a36d435350`  
		Last Modified: Fri, 14 Feb 2025 21:30:30 GMT  
		Size: 1.0 MB (1043182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8c9a1ff32af0af5039728ae3a8a3618cf487898ebfcfeb9348c28caece5752c`  
		Last Modified: Fri, 14 Feb 2025 21:30:30 GMT  
		Size: 19.4 KB (19356 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.9.5` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:f10e1349bc98816a69d038ee688e24a87b1cdffda436b342793a6c6432df4424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11943848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894447f0f68cb4c271324608202415aea3bd42d6f1fb962849178f3e14a77e09`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.7-armhf.tar.gz / # buildkit
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
	-	`sha256:f5c2e5a96485e4eaf16caa456bdd06c183f55bf5a43c2e4532d5e8db8bfacaad`  
		Last Modified: Fri, 14 Feb 2025 19:25:37 GMT  
		Size: 3.2 MB (3177535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5a36525d0fcbba2920aa86c5064e7e1e14313fb5548ffc910085a5befd3dd7`  
		Last Modified: Fri, 14 Feb 2025 21:30:39 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3f904108af54640bea84ceddfd696a85893dd577db2afc08c8ea18af1dee6e`  
		Last Modified: Fri, 14 Feb 2025 21:30:39 GMT  
		Size: 11.0 KB (10956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94feb113c2bb41dd0efff24dd5d111680c7f8995c512221c5799d2beb1074c05`  
		Last Modified: Fri, 14 Feb 2025 21:30:39 GMT  
		Size: 2.9 MB (2891931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893117506eeb7e44af37eab08297f0c855c422b41d25f719daa9f15615489430`  
		Last Modified: Fri, 14 Feb 2025 21:30:40 GMT  
		Size: 5.9 MB (5859627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13555e9e4c43a47103ff3bc9f81263480912fb1cfa4ac9b8752f6d58e5fe0c0f`  
		Last Modified: Fri, 14 Feb 2025 21:30:40 GMT  
		Size: 1.8 KB (1829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a598dd8009a7496ba040c09d8b689adbc338567bb3cb2c349dcba041dfd50a94`  
		Last Modified: Fri, 14 Feb 2025 21:30:39 GMT  
		Size: 695.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9.5` - unknown; unknown

```console
$ docker pull eggdrop@sha256:2186239d930b0f7aba7d62f3ccf5d7b1d09ca043c6670ec8d83de5aa3f1590f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1baf361bc3b92bfff59c39ad039b269d10c12fe369749479b6fc380bbe0b58d9`

```dockerfile
```

-	Layers:
	-	`sha256:e5e4a6c5e4332277716397cf23fef0e3752776029e2f1abf19acf8715063c998`  
		Last Modified: Fri, 14 Feb 2025 21:30:32 GMT  
		Size: 19.2 KB (19240 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.9.5` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:71221b12a34f4afd052dec7a0ba6bac00f11d8f8d6d8b416bc6ab387a9eba32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12413682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06391f677a7f07b412e55209a4b0b3d0d9171d84baaae69193242fac6e5b9e78`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
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
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 14:31:17 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5e405d1b1d32ec2ea3cd7c4eaa746a0ad1a08bb9cb89ea1426833c906bc905`  
		Last Modified: Sat, 15 Feb 2025 03:30:14 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922022d41504f6d960abeb7ac90ea0f3165f03620c4c50ef7e69f5251ab4482c`  
		Last Modified: Sat, 15 Feb 2025 03:30:10 GMT  
		Size: 11.3 KB (11349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bb052d2efd871a6ab605c73a15f3623aaf5f0d395cef1b8e04656e75c676dd`  
		Last Modified: Sat, 15 Feb 2025 03:30:32 GMT  
		Size: 3.0 MB (3021436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee30b4ce5dc6de9512591fabfaa6761986b5e4a4d4219c00ff83badbaaef567`  
		Last Modified: Sat, 15 Feb 2025 03:30:34 GMT  
		Size: 6.0 MB (6015665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c7b229d78ea9859fb04eff273d89b99dc0df7ecad02c39985ba7bc84071a9`  
		Last Modified: Sat, 15 Feb 2025 03:30:30 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3f1cce52d7fa191ec3d160b9fc04bc18f59a5387a5208e966728c4960df1a0`  
		Last Modified: Sat, 15 Feb 2025 03:30:32 GMT  
		Size: 699.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9.5` - unknown; unknown

```console
$ docker pull eggdrop@sha256:9aa4cfa9ef03794d00ac4a43ad76be0ea5db78c20d8245434122fc66826bc1fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1062695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45cd0dd11840b8e339b7cb63b521dece5b2c27e6f454bbbef40a4c5caa6f62c8`

```dockerfile
```

-	Layers:
	-	`sha256:40c72dd854d99c91ef692d59d3d96dc7b6c0334a217cf2597910c95bf21cce76`  
		Last Modified: Sat, 15 Feb 2025 00:30:50 GMT  
		Size: 1.0 MB (1043214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f37e6ae2e1433c7e4c1faf9c13712dce853de3b0db13bae21736ed8aedea79c`  
		Last Modified: Sat, 15 Feb 2025 00:30:50 GMT  
		Size: 19.5 KB (19481 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:a025c1e2e7a52e3169d23f1cebea3e5670243149527fee7be160778cdb63f886
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
$ docker pull eggdrop@sha256:df21871e938ff96b7e17da95b8c051200b3b12db4c614a6bd7df035dcedfcc0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12784523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770f61713e5e80316ae2d5b0ae85435afae0d5294e1a417dff4832b0603424a1`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 03 Feb 2025 02:59:38 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bae14b70df6a5152ffb6aa4f7db219a6b31a04aa96c0fbc6421213466fe505d`  
		Last Modified: Sat, 15 Feb 2025 09:24:37 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8468965d14c3b5811f6b6f22414aa4006bb76530265b4a0a44ed68b354f198c4`  
		Last Modified: Sat, 15 Feb 2025 09:24:37 GMT  
		Size: 1.1 MB (1116796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28a9e07b1c45a05b5327ed544bcb134f13487561af7f708adb3debda5f26d7a`  
		Last Modified: Sat, 15 Feb 2025 09:24:38 GMT  
		Size: 8.0 MB (8021402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab65ae290d1c04dcfaacc2f5b9d6489bb5e2c49ed4ad7bd47717c5bf21b0bba2`  
		Last Modified: Sat, 15 Feb 2025 09:24:39 GMT  
		Size: 2.0 KB (1968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7901c06000f20bd5c8fefe056f5364b2e8ec3293d9be7e0b3790c2ba6b95bf28`  
		Last Modified: Sat, 15 Feb 2025 09:24:39 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:609bbba498e08372a6d79197b054a03f8e92457a4a855ac160e4a0d0766752ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 KB (158002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4afd7a77190261d214db38069c0b1932df8fe8007f144e026192b7f822064de`

```dockerfile
```

-	Layers:
	-	`sha256:f3dabbfb5ca1f071c47d3f635a972252e30b351ce291d5f31f8204bf669bb29d`  
		Last Modified: Fri, 14 Feb 2025 21:30:38 GMT  
		Size: 140.9 KB (140913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fb4392449a57d73079aefb57d7332503d11c9402c4d6af7c4804986d8041866`  
		Last Modified: Fri, 14 Feb 2025 21:30:39 GMT  
		Size: 17.1 KB (17089 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:588903ec0d76b47ed168cb07c7f61af5e107cab666f6d9b296f6caed7c81ded5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12337800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539d5243968d0790b3f8ce68296eaf47468b5b5117a1820ec208a2a45647d5e5`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 03 Feb 2025 02:59:38 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243d2dc41e14c344d1a9f1cc74006025de32e9c01ef2676491ffb84c79f06b47`  
		Last Modified: Fri, 14 Feb 2025 21:30:47 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9eb9be78d7b5d67e744c97d659dd70efb8bdf1a929307d78e18e5a313cb0333`  
		Last Modified: Fri, 14 Feb 2025 21:30:47 GMT  
		Size: 1.1 MB (1129837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4180789d704a7ef80504849bf9c83b2971b6908782bfb14dcc5f488e0e67ad24`  
		Last Modified: Fri, 14 Feb 2025 21:30:47 GMT  
		Size: 7.8 MB (7839162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7675f0103f9c23aa055cd3ad661db2e2ffaff1be9f89f2c5a40f01b048c19b`  
		Last Modified: Fri, 14 Feb 2025 21:30:47 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7111a52f8e59611672091fd46afb7f5c39eff2e929cca6dc3b0aa7bff5a5a1cd`  
		Last Modified: Fri, 14 Feb 2025 21:30:47 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:71f90bc44a6ee8c3667e23c0a9c59706e3ddd5344c59ea566e908a1b4d7cbfd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (16954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20356f547d35628121e5070f13f79f4cac5a7f28f037af15c4aa1bb7383fcf5`

```dockerfile
```

-	Layers:
	-	`sha256:be5f9b3292abb44c643b1572249e55c45ece24fc3c8ab07e9cca14aa4db7ecfa`  
		Last Modified: Fri, 14 Feb 2025 21:30:40 GMT  
		Size: 17.0 KB (16954 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:edca286b7eeca981b0c6712bf0b88751668801c23ce50e0808a5d8ffe3895b49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13235872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2090c62b3a579a8265d6361edc8154f92b6f0763e0dc014efecc85f9904e04b8`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 03 Feb 2025 02:59:38 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f437ca58399a638057c62b2fec6ea27022c6ba14ca6b1e748e425dd004369d77`  
		Last Modified: Sun, 16 Feb 2025 17:21:18 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5ff23854b2cb7cc2af9ed9376082ad4ed0c2ffc31b68afedaea46db187d56c`  
		Last Modified: Sun, 16 Feb 2025 17:21:21 GMT  
		Size: 1.2 MB (1171028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958816378edfde5f40f73c6751957a2add2a47d5aced7436d57df71e6e356071`  
		Last Modified: Sun, 16 Feb 2025 17:21:22 GMT  
		Size: 8.1 MB (8067741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37103dd71102c1a0e5547fae2b66c5c50d5b2ca80e2fbfce46a4fdfdd5ac5643`  
		Last Modified: Sun, 16 Feb 2025 17:21:25 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8f56221f305640dc31f7b757db907f0d30c46c55af6451444bc6ffeb233b3b`  
		Last Modified: Sun, 16 Feb 2025 17:21:24 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:eea327f80f4be3a4bd0b35dbedac5a7e2df6b2e5fa651bc34bdb8215b986fa10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 KB (158122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7406f597f7c0749d07ab19b48840cdbb48e24db7f9e5a6f2bd6ae0cc50b2f2bf`

```dockerfile
```

-	Layers:
	-	`sha256:e07183601e9166b79501dc9273163739b8c5d6e7b176e262f4613e4fe9167d1a`  
		Last Modified: Sat, 15 Feb 2025 00:30:57 GMT  
		Size: 140.9 KB (140933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd7377e263547758e2047849e5452a8ac7c7be7aefd3bdb7fa45657ebf66708b`  
		Last Modified: Sat, 15 Feb 2025 00:30:57 GMT  
		Size: 17.2 KB (17189 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:538cb8a3a26d486dbd78ebe4d1ab370e70973a1787fe56023aa1a5d57af318ab
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
$ docker pull eggdrop@sha256:31aba2be254a23fac1ca9df0ff7ed23c6f02cd9443e8a5d9126fef7d3c7bee18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17469999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d780465a6f218223949cbdd3131c8eccda6aaa5241371ad35bb98252c39c73e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b3444eeb09c629c9d3bcdbec5cf120853b2342308dfd0b5c460d5ba82a8622`  
		Last Modified: Fri, 14 Feb 2025 21:32:43 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8734443ac9c716799f545d89ccf8397a62a4f1f2af319a6aa04e85bceb4614`  
		Last Modified: Fri, 14 Feb 2025 21:32:43 GMT  
		Size: 1.1 MB (1115995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a208386598da099d59cdb929e35b8e54653564424b7e80bab5dc671ab1754d59`  
		Last Modified: Fri, 14 Feb 2025 21:32:44 GMT  
		Size: 12.7 MB (12723037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b2b70858cd562abe3c90891c3a80761170225aba0d29a6d6962363d2d56b22`  
		Last Modified: Fri, 14 Feb 2025 21:32:44 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba79086bb542341f7e4ffb7708cf8a107e8e8047abfd02d4b4878c24a317f46`  
		Last Modified: Fri, 14 Feb 2025 21:32:44 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:3759dad3fd261cc3648714c96839890fbdd5f86a5b991c3ed9498ab08ae02dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 KB (157535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71faf331f37a788fdc348b5c53a68fb84db88b28a24a7c80e352c8c5eb6ad2e8`

```dockerfile
```

-	Layers:
	-	`sha256:d829d4c44533e372d3be0207c6b9adce61112450068b5e3e278eb043ddd6b4db`  
		Last Modified: Fri, 14 Feb 2025 21:30:21 GMT  
		Size: 138.8 KB (138764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56ebb2a93388b0529f8d2ed121d33bf2f35a8c376a332712e914d1a3d073384f`  
		Last Modified: Fri, 14 Feb 2025 21:30:21 GMT  
		Size: 18.8 KB (18771 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:c424dc7cc87f0fb02da042e36bc53a68d41237d871d583a4db7e9fa0a4e9a86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17078725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bb5d3553d651bd5cb523bbb122b336112f7e46312e75aa811231f8822d29d9`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
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
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 19:26:24 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5f5ebafbb9f2620b9c285aaede8b1c01410fa22db544ec4f8395ca66b6cd04`  
		Last Modified: Fri, 14 Feb 2025 21:30:32 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017b325b57e86dbac830719f76716817f84e81dad00dca0c78ecbc42ee10d704`  
		Last Modified: Fri, 14 Feb 2025 21:30:32 GMT  
		Size: 1.1 MB (1130373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5553baed849de0dced619d727239c90267a454e1d5082375d078bfedc1b65694`  
		Last Modified: Fri, 14 Feb 2025 21:30:33 GMT  
		Size: 12.6 MB (12571748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980845efd2922d60733f7e65dcfbb2556351dfb3591970c373d7bfd67798a65b`  
		Last Modified: Fri, 14 Feb 2025 21:30:32 GMT  
		Size: 2.0 KB (1951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30d6fc859cd8b7e9a6a4b46f6b7295071ba5c48ceb31a012a94caafc4507166`  
		Last Modified: Fri, 14 Feb 2025 21:30:32 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:f54b495c9c22b0995def5f43ca925e63fd4b5854c332b06affb7245522809ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14913f8a5509822846bba45db715b832cc66b1f59b6de920c3d43bb3df359630`

```dockerfile
```

-	Layers:
	-	`sha256:aa90550c8b30a98ec74106530300ce5280cd706061d04406387bf47797628f97`  
		Last Modified: Fri, 14 Feb 2025 21:30:22 GMT  
		Size: 18.7 KB (18658 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:4035c5598844741674c04c76c922d8a7af24752fbc6788e8e9e6fbf59dd1b1d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18164152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7eb6d38e506b0c3ce3f15e5c7567ccad8fdff392d00179c87d4b2cc101445ef`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
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
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4f5e522137cc417a3f98ddcfca8b939a1bde2f1bfa06284389e632bd47f3dc`  
		Last Modified: Sat, 15 Feb 2025 02:01:23 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c5632ada7a032e4a40a385ac269d30d344dd48f333fa9490a2d9fddf33be97`  
		Last Modified: Sat, 15 Feb 2025 02:01:23 GMT  
		Size: 1.2 MB (1211974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16738349d7ac4181dbc287f636b71089e230b7b39a10bc59dbd3c275941d9b59`  
		Last Modified: Sat, 15 Feb 2025 02:01:24 GMT  
		Size: 12.9 MB (12856941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b878c75135710003b9e72ef4b408ab2f3c4ededfff0cf034a9351b9c3fdf74`  
		Last Modified: Sat, 15 Feb 2025 02:01:23 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d1412b27a55491a2489826aa90d806d17e53e4427a7f51f03086ebb8dd9304`  
		Last Modified: Sat, 15 Feb 2025 02:01:23 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:7f123e51f800694ec3f3d2c2c46c6b1223181862a3c9b03ff4ed5fed4e051dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 KB (157724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c175b098b6ebbacf38438e2d9c1d4f6c6721baea7fb22b24ce757f60b5cc8f`

```dockerfile
```

-	Layers:
	-	`sha256:f4df0395fc7c5af9220eb15a11239d51fa69940e9ae3747f5f630e9f46edbbbc`  
		Last Modified: Sat, 15 Feb 2025 00:30:43 GMT  
		Size: 138.8 KB (138820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6f7123b133f1bbd79f1bb1a494afff036ed9f5373aa8f7dc72fa235be2e2f6d`  
		Last Modified: Sat, 15 Feb 2025 00:30:43 GMT  
		Size: 18.9 KB (18904 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:538cb8a3a26d486dbd78ebe4d1ab370e70973a1787fe56023aa1a5d57af318ab
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
$ docker pull eggdrop@sha256:31aba2be254a23fac1ca9df0ff7ed23c6f02cd9443e8a5d9126fef7d3c7bee18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17469999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d780465a6f218223949cbdd3131c8eccda6aaa5241371ad35bb98252c39c73e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b3444eeb09c629c9d3bcdbec5cf120853b2342308dfd0b5c460d5ba82a8622`  
		Last Modified: Fri, 14 Feb 2025 21:32:43 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8734443ac9c716799f545d89ccf8397a62a4f1f2af319a6aa04e85bceb4614`  
		Last Modified: Fri, 14 Feb 2025 21:32:43 GMT  
		Size: 1.1 MB (1115995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a208386598da099d59cdb929e35b8e54653564424b7e80bab5dc671ab1754d59`  
		Last Modified: Fri, 14 Feb 2025 21:32:44 GMT  
		Size: 12.7 MB (12723037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b2b70858cd562abe3c90891c3a80761170225aba0d29a6d6962363d2d56b22`  
		Last Modified: Fri, 14 Feb 2025 21:32:44 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba79086bb542341f7e4ffb7708cf8a107e8e8047abfd02d4b4878c24a317f46`  
		Last Modified: Fri, 14 Feb 2025 21:32:44 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:3759dad3fd261cc3648714c96839890fbdd5f86a5b991c3ed9498ab08ae02dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 KB (157535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71faf331f37a788fdc348b5c53a68fb84db88b28a24a7c80e352c8c5eb6ad2e8`

```dockerfile
```

-	Layers:
	-	`sha256:d829d4c44533e372d3be0207c6b9adce61112450068b5e3e278eb043ddd6b4db`  
		Last Modified: Fri, 14 Feb 2025 21:30:21 GMT  
		Size: 138.8 KB (138764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56ebb2a93388b0529f8d2ed121d33bf2f35a8c376a332712e914d1a3d073384f`  
		Last Modified: Fri, 14 Feb 2025 21:30:21 GMT  
		Size: 18.8 KB (18771 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:c424dc7cc87f0fb02da042e36bc53a68d41237d871d583a4db7e9fa0a4e9a86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17078725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bb5d3553d651bd5cb523bbb122b336112f7e46312e75aa811231f8822d29d9`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
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
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 19:26:24 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5f5ebafbb9f2620b9c285aaede8b1c01410fa22db544ec4f8395ca66b6cd04`  
		Last Modified: Fri, 14 Feb 2025 21:30:32 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017b325b57e86dbac830719f76716817f84e81dad00dca0c78ecbc42ee10d704`  
		Last Modified: Fri, 14 Feb 2025 21:30:32 GMT  
		Size: 1.1 MB (1130373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5553baed849de0dced619d727239c90267a454e1d5082375d078bfedc1b65694`  
		Last Modified: Fri, 14 Feb 2025 21:30:33 GMT  
		Size: 12.6 MB (12571748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980845efd2922d60733f7e65dcfbb2556351dfb3591970c373d7bfd67798a65b`  
		Last Modified: Fri, 14 Feb 2025 21:30:32 GMT  
		Size: 2.0 KB (1951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30d6fc859cd8b7e9a6a4b46f6b7295071ba5c48ceb31a012a94caafc4507166`  
		Last Modified: Fri, 14 Feb 2025 21:30:32 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:f54b495c9c22b0995def5f43ca925e63fd4b5854c332b06affb7245522809ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14913f8a5509822846bba45db715b832cc66b1f59b6de920c3d43bb3df359630`

```dockerfile
```

-	Layers:
	-	`sha256:aa90550c8b30a98ec74106530300ce5280cd706061d04406387bf47797628f97`  
		Last Modified: Fri, 14 Feb 2025 21:30:22 GMT  
		Size: 18.7 KB (18658 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:4035c5598844741674c04c76c922d8a7af24752fbc6788e8e9e6fbf59dd1b1d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18164152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7eb6d38e506b0c3ce3f15e5c7567ccad8fdff392d00179c87d4b2cc101445ef`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
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
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4f5e522137cc417a3f98ddcfca8b939a1bde2f1bfa06284389e632bd47f3dc`  
		Last Modified: Sat, 15 Feb 2025 02:01:23 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c5632ada7a032e4a40a385ac269d30d344dd48f333fa9490a2d9fddf33be97`  
		Last Modified: Sat, 15 Feb 2025 02:01:23 GMT  
		Size: 1.2 MB (1211974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16738349d7ac4181dbc287f636b71089e230b7b39a10bc59dbd3c275941d9b59`  
		Last Modified: Sat, 15 Feb 2025 02:01:24 GMT  
		Size: 12.9 MB (12856941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b878c75135710003b9e72ef4b408ab2f3c4ededfff0cf034a9351b9c3fdf74`  
		Last Modified: Sat, 15 Feb 2025 02:01:23 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d1412b27a55491a2489826aa90d806d17e53e4427a7f51f03086ebb8dd9304`  
		Last Modified: Sat, 15 Feb 2025 02:01:23 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:7f123e51f800694ec3f3d2c2c46c6b1223181862a3c9b03ff4ed5fed4e051dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 KB (157724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c175b098b6ebbacf38438e2d9c1d4f6c6721baea7fb22b24ce757f60b5cc8f`

```dockerfile
```

-	Layers:
	-	`sha256:f4df0395fc7c5af9220eb15a11239d51fa69940e9ae3747f5f630e9f46edbbbc`  
		Last Modified: Sat, 15 Feb 2025 00:30:43 GMT  
		Size: 138.8 KB (138820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6f7123b133f1bbd79f1bb1a494afff036ed9f5373aa8f7dc72fa235be2e2f6d`  
		Last Modified: Sat, 15 Feb 2025 00:30:43 GMT  
		Size: 18.9 KB (18904 bytes)  
		MIME: application/vnd.in-toto+json
