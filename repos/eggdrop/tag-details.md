<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.10`](#eggdrop110)
-	[`eggdrop:1.10.1`](#eggdrop1101)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.10`

```console
$ docker pull eggdrop@sha256:08d135f49c8c983b685644c44df27bae2c744a02ff9b7294757eaaa512ed82cb
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
$ docker pull eggdrop@sha256:5d171b38421fe7bc8a72c368e175d3265744fb7829a9a9aab9c0b684e61124e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15565657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb94c0ae33f68189af54b6de7f5c0145bfab04ab385adc3b4352c59750b9b68`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:14:16 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 15 Apr 2026 23:14:16 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 15 Apr 2026 23:14:17 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 15 Apr 2026 23:17:27 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz.asc   && gpg --batch --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1.tar.gz.asc eggdrop-1.10.1.tar.gz   && gpgconf --kill all   && rm eggdrop-1.10.1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1.tar.gz   && rm eggdrop-1.10.1.tar.gz   && ( cd eggdrop-1.10.1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 15 Apr 2026 23:17:27 GMT
ENV NICK=
# Wed, 15 Apr 2026 23:17:27 GMT
ENV SERVER=
# Wed, 15 Apr 2026 23:17:27 GMT
ENV LISTEN=3333
# Wed, 15 Apr 2026 23:17:27 GMT
ENV USERFILE=eggdrop.user
# Wed, 15 Apr 2026 23:17:27 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 15 Apr 2026 23:17:28 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 15 Apr 2026 23:17:28 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 15 Apr 2026 23:17:28 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 15 Apr 2026 23:17:28 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 15 Apr 2026 23:17:28 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 15 Apr 2026 23:17:28 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c209b08b29ce83885852263414073aefed7cac9e232b76ae57152e1eece61f3b`  
		Last Modified: Wed, 15 Apr 2026 23:17:34 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19e8c421d8a0bd2f54014a2e51097343778cb22d6693193ddcca8aefec71c8a`  
		Last Modified: Wed, 15 Apr 2026 23:17:34 GMT  
		Size: 3.4 MB (3407097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4caa010fc1b94160a654004e2ce27cbac439082c568fef7654fda4977954eeb`  
		Last Modified: Wed, 15 Apr 2026 23:17:34 GMT  
		Size: 8.5 MB (8510759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1ccf005bd8ad6910ee629138d0326911f6de9e7e5b0288cbe5b34dab140abd`  
		Last Modified: Wed, 15 Apr 2026 23:17:34 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c1805be816fa0749705a4bcf5e75e484976e63474c1465e8be8a141216a676`  
		Last Modified: Wed, 15 Apr 2026 23:17:35 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10` - unknown; unknown

```console
$ docker pull eggdrop@sha256:72535bbe7a2fc471a255f0050d6896c8748fb04d8bb7b0c579fa4ecaa87190ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 KB (164344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95932f5bb9df8a68c36453f9d6176f34b28dac8da668c34fac79d55234e125c`

```dockerfile
```

-	Layers:
	-	`sha256:c48b17163cbccdefb0df63af915d30a44963fefbfdc3bdd485852efd1bd92536`  
		Last Modified: Wed, 15 Apr 2026 23:17:34 GMT  
		Size: 146.0 KB (145994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd518cde3ddeac191da477649cbd37c3658e02c4a6fdae5d644760615cfb219`  
		Last Modified: Wed, 15 Apr 2026 23:17:34 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:d619fdb9ce50eea17c0361953e1614000526503daf85c72b6a14d9e2072d7306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14769130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7f80741aa6838886a467b403dec6fc44aac1988d96eb4bd91650942060cd22`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.21.6-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:13:21 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 15 Apr 2026 23:13:21 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 15 Apr 2026 23:13:22 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 15 Apr 2026 23:18:16 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz.asc   && gpg --batch --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1.tar.gz.asc eggdrop-1.10.1.tar.gz   && gpgconf --kill all   && rm eggdrop-1.10.1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1.tar.gz   && rm eggdrop-1.10.1.tar.gz   && ( cd eggdrop-1.10.1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 15 Apr 2026 23:18:16 GMT
ENV NICK=
# Wed, 15 Apr 2026 23:18:16 GMT
ENV SERVER=
# Wed, 15 Apr 2026 23:18:16 GMT
ENV LISTEN=3333
# Wed, 15 Apr 2026 23:18:16 GMT
ENV USERFILE=eggdrop.user
# Wed, 15 Apr 2026 23:18:16 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 15 Apr 2026 23:18:16 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 15 Apr 2026 23:18:16 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 15 Apr 2026 23:18:16 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 15 Apr 2026 23:18:16 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 15 Apr 2026 23:18:16 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 15 Apr 2026 23:18:16 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a7fd0d978b605e6a6ed974adfe73f3035a5a60d1bebd2c9d5bb111651502c33e`  
		Last Modified: Wed, 28 Jan 2026 01:18:08 GMT  
		Size: 3.4 MB (3365870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9441c2310bd656e7ad2cb8a3d35fe1676c90bcccc140d53cb4c46ff6952ec71e`  
		Last Modified: Wed, 15 Apr 2026 23:18:21 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc2e1af5e377bfff332edeeefe1527f18503bf00153ae73bc8d6b8689efe3bd`  
		Last Modified: Wed, 15 Apr 2026 23:18:21 GMT  
		Size: 3.1 MB (3076252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4ba4813ca5c38ab1c114e1b67b8e8471d4c9919046274e5847c1ce696ec1ee`  
		Last Modified: Wed, 15 Apr 2026 23:18:21 GMT  
		Size: 8.3 MB (8322941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554113e79ea3f9a788f298a09771242c989884fe6bd86f3aa293035385f8f5f9`  
		Last Modified: Wed, 15 Apr 2026 23:18:21 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17895c5dd373524390034c773d87fff653b7f8641d8a349452a3004358b57ea0`  
		Last Modified: Wed, 15 Apr 2026 23:18:22 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10` - unknown; unknown

```console
$ docker pull eggdrop@sha256:f8fd8de3cf4cb83f53f93102846e9622b266162cf3afb9a7dba9e9fa2f985da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fe16aba2353cbd94ac34d30a21d2d8c8c1528ab57b3489960117b288a536ce`

```dockerfile
```

-	Layers:
	-	`sha256:b309d42f28e884e0829955798ca0731edc85243b50f177491b9ab46df686a879`  
		Last Modified: Wed, 15 Apr 2026 23:18:21 GMT  
		Size: 18.2 KB (18241 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:32c9709246f525349b7673b26b48865ae2eac7883d823777f227666f2b1d59e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16333774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24538fd30da3ded0b76d47bf15c520f0b5d75248e02b1f239039fdde21831471`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:14:12 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 15 Apr 2026 23:14:12 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 15 Apr 2026 23:14:13 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 15 Apr 2026 23:18:05 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz.asc   && gpg --batch --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1.tar.gz.asc eggdrop-1.10.1.tar.gz   && gpgconf --kill all   && rm eggdrop-1.10.1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1.tar.gz   && rm eggdrop-1.10.1.tar.gz   && ( cd eggdrop-1.10.1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 15 Apr 2026 23:18:05 GMT
ENV NICK=
# Wed, 15 Apr 2026 23:18:05 GMT
ENV SERVER=
# Wed, 15 Apr 2026 23:18:05 GMT
ENV LISTEN=3333
# Wed, 15 Apr 2026 23:18:05 GMT
ENV USERFILE=eggdrop.user
# Wed, 15 Apr 2026 23:18:05 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 15 Apr 2026 23:18:05 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 15 Apr 2026 23:18:05 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 15 Apr 2026 23:18:05 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 15 Apr 2026 23:18:05 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 15 Apr 2026 23:18:05 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 15 Apr 2026 23:18:05 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6f59a843adb27b7856e4d35a57e285ff6ee6e0489fd2f71fd305af70c15d0a`  
		Last Modified: Wed, 15 Apr 2026 23:18:11 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5322ea15110e272eb2fa108f7824ff76350b4b02d221ffab492baf0daaebbd4`  
		Last Modified: Wed, 15 Apr 2026 23:18:11 GMT  
		Size: 3.8 MB (3773617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964d33f9be0696f4a62682ee36578ebdbaff836e2eee5b0055b2235c1927c70c`  
		Last Modified: Wed, 15 Apr 2026 23:18:12 GMT  
		Size: 8.6 MB (8563214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9609e921af887592121877325056eaa6421a8a9d7a25f931280db556343b40c`  
		Last Modified: Wed, 15 Apr 2026 23:18:11 GMT  
		Size: 1.9 KB (1950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765d3671346423e43c32453bc2f41a65a749568e1a9d06b18de89adfd7f78f34`  
		Last Modified: Wed, 15 Apr 2026 23:18:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10` - unknown; unknown

```console
$ docker pull eggdrop@sha256:6bf107b85ef0332efe7166e4243ffa778728dbf5a3805d25e729db8e5e35dd30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 KB (164534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ccd7ea2fe64cb99fe52f0be3f35e34e7274007933542fe8fd9779ac828aa70`

```dockerfile
```

-	Layers:
	-	`sha256:ecf02737a699a21fda090418f32dd1674c81d6de2ef17f4d88aba0173ee6ecb7`  
		Last Modified: Wed, 15 Apr 2026 23:18:11 GMT  
		Size: 146.1 KB (146050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33388028f91f6acff118c365a280d284aca755bb9901e3db6d3209226e588bc5`  
		Last Modified: Wed, 15 Apr 2026 23:18:11 GMT  
		Size: 18.5 KB (18484 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:1.10.1`

```console
$ docker pull eggdrop@sha256:08d135f49c8c983b685644c44df27bae2c744a02ff9b7294757eaaa512ed82cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:1.10.1` - linux; amd64

```console
$ docker pull eggdrop@sha256:5d171b38421fe7bc8a72c368e175d3265744fb7829a9a9aab9c0b684e61124e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15565657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb94c0ae33f68189af54b6de7f5c0145bfab04ab385adc3b4352c59750b9b68`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:14:16 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 15 Apr 2026 23:14:16 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 15 Apr 2026 23:14:17 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 15 Apr 2026 23:17:27 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz.asc   && gpg --batch --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1.tar.gz.asc eggdrop-1.10.1.tar.gz   && gpgconf --kill all   && rm eggdrop-1.10.1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1.tar.gz   && rm eggdrop-1.10.1.tar.gz   && ( cd eggdrop-1.10.1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 15 Apr 2026 23:17:27 GMT
ENV NICK=
# Wed, 15 Apr 2026 23:17:27 GMT
ENV SERVER=
# Wed, 15 Apr 2026 23:17:27 GMT
ENV LISTEN=3333
# Wed, 15 Apr 2026 23:17:27 GMT
ENV USERFILE=eggdrop.user
# Wed, 15 Apr 2026 23:17:27 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 15 Apr 2026 23:17:28 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 15 Apr 2026 23:17:28 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 15 Apr 2026 23:17:28 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 15 Apr 2026 23:17:28 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 15 Apr 2026 23:17:28 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 15 Apr 2026 23:17:28 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c209b08b29ce83885852263414073aefed7cac9e232b76ae57152e1eece61f3b`  
		Last Modified: Wed, 15 Apr 2026 23:17:34 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19e8c421d8a0bd2f54014a2e51097343778cb22d6693193ddcca8aefec71c8a`  
		Last Modified: Wed, 15 Apr 2026 23:17:34 GMT  
		Size: 3.4 MB (3407097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4caa010fc1b94160a654004e2ce27cbac439082c568fef7654fda4977954eeb`  
		Last Modified: Wed, 15 Apr 2026 23:17:34 GMT  
		Size: 8.5 MB (8510759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1ccf005bd8ad6910ee629138d0326911f6de9e7e5b0288cbe5b34dab140abd`  
		Last Modified: Wed, 15 Apr 2026 23:17:34 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c1805be816fa0749705a4bcf5e75e484976e63474c1465e8be8a141216a676`  
		Last Modified: Wed, 15 Apr 2026 23:17:35 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.1` - unknown; unknown

```console
$ docker pull eggdrop@sha256:72535bbe7a2fc471a255f0050d6896c8748fb04d8bb7b0c579fa4ecaa87190ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 KB (164344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95932f5bb9df8a68c36453f9d6176f34b28dac8da668c34fac79d55234e125c`

```dockerfile
```

-	Layers:
	-	`sha256:c48b17163cbccdefb0df63af915d30a44963fefbfdc3bdd485852efd1bd92536`  
		Last Modified: Wed, 15 Apr 2026 23:17:34 GMT  
		Size: 146.0 KB (145994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd518cde3ddeac191da477649cbd37c3658e02c4a6fdae5d644760615cfb219`  
		Last Modified: Wed, 15 Apr 2026 23:17:34 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10.1` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:d619fdb9ce50eea17c0361953e1614000526503daf85c72b6a14d9e2072d7306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14769130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7f80741aa6838886a467b403dec6fc44aac1988d96eb4bd91650942060cd22`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.21.6-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:13:21 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 15 Apr 2026 23:13:21 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 15 Apr 2026 23:13:22 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 15 Apr 2026 23:18:16 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz.asc   && gpg --batch --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1.tar.gz.asc eggdrop-1.10.1.tar.gz   && gpgconf --kill all   && rm eggdrop-1.10.1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1.tar.gz   && rm eggdrop-1.10.1.tar.gz   && ( cd eggdrop-1.10.1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 15 Apr 2026 23:18:16 GMT
ENV NICK=
# Wed, 15 Apr 2026 23:18:16 GMT
ENV SERVER=
# Wed, 15 Apr 2026 23:18:16 GMT
ENV LISTEN=3333
# Wed, 15 Apr 2026 23:18:16 GMT
ENV USERFILE=eggdrop.user
# Wed, 15 Apr 2026 23:18:16 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 15 Apr 2026 23:18:16 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 15 Apr 2026 23:18:16 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 15 Apr 2026 23:18:16 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 15 Apr 2026 23:18:16 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 15 Apr 2026 23:18:16 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 15 Apr 2026 23:18:16 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a7fd0d978b605e6a6ed974adfe73f3035a5a60d1bebd2c9d5bb111651502c33e`  
		Last Modified: Wed, 28 Jan 2026 01:18:08 GMT  
		Size: 3.4 MB (3365870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9441c2310bd656e7ad2cb8a3d35fe1676c90bcccc140d53cb4c46ff6952ec71e`  
		Last Modified: Wed, 15 Apr 2026 23:18:21 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc2e1af5e377bfff332edeeefe1527f18503bf00153ae73bc8d6b8689efe3bd`  
		Last Modified: Wed, 15 Apr 2026 23:18:21 GMT  
		Size: 3.1 MB (3076252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4ba4813ca5c38ab1c114e1b67b8e8471d4c9919046274e5847c1ce696ec1ee`  
		Last Modified: Wed, 15 Apr 2026 23:18:21 GMT  
		Size: 8.3 MB (8322941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554113e79ea3f9a788f298a09771242c989884fe6bd86f3aa293035385f8f5f9`  
		Last Modified: Wed, 15 Apr 2026 23:18:21 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17895c5dd373524390034c773d87fff653b7f8641d8a349452a3004358b57ea0`  
		Last Modified: Wed, 15 Apr 2026 23:18:22 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.1` - unknown; unknown

```console
$ docker pull eggdrop@sha256:f8fd8de3cf4cb83f53f93102846e9622b266162cf3afb9a7dba9e9fa2f985da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fe16aba2353cbd94ac34d30a21d2d8c8c1528ab57b3489960117b288a536ce`

```dockerfile
```

-	Layers:
	-	`sha256:b309d42f28e884e0829955798ca0731edc85243b50f177491b9ab46df686a879`  
		Last Modified: Wed, 15 Apr 2026 23:18:21 GMT  
		Size: 18.2 KB (18241 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10.1` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:32c9709246f525349b7673b26b48865ae2eac7883d823777f227666f2b1d59e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16333774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24538fd30da3ded0b76d47bf15c520f0b5d75248e02b1f239039fdde21831471`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:14:12 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 15 Apr 2026 23:14:12 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 15 Apr 2026 23:14:13 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 15 Apr 2026 23:18:05 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz.asc   && gpg --batch --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1.tar.gz.asc eggdrop-1.10.1.tar.gz   && gpgconf --kill all   && rm eggdrop-1.10.1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1.tar.gz   && rm eggdrop-1.10.1.tar.gz   && ( cd eggdrop-1.10.1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 15 Apr 2026 23:18:05 GMT
ENV NICK=
# Wed, 15 Apr 2026 23:18:05 GMT
ENV SERVER=
# Wed, 15 Apr 2026 23:18:05 GMT
ENV LISTEN=3333
# Wed, 15 Apr 2026 23:18:05 GMT
ENV USERFILE=eggdrop.user
# Wed, 15 Apr 2026 23:18:05 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 15 Apr 2026 23:18:05 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 15 Apr 2026 23:18:05 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 15 Apr 2026 23:18:05 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 15 Apr 2026 23:18:05 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 15 Apr 2026 23:18:05 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 15 Apr 2026 23:18:05 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6f59a843adb27b7856e4d35a57e285ff6ee6e0489fd2f71fd305af70c15d0a`  
		Last Modified: Wed, 15 Apr 2026 23:18:11 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5322ea15110e272eb2fa108f7824ff76350b4b02d221ffab492baf0daaebbd4`  
		Last Modified: Wed, 15 Apr 2026 23:18:11 GMT  
		Size: 3.8 MB (3773617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964d33f9be0696f4a62682ee36578ebdbaff836e2eee5b0055b2235c1927c70c`  
		Last Modified: Wed, 15 Apr 2026 23:18:12 GMT  
		Size: 8.6 MB (8563214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9609e921af887592121877325056eaa6421a8a9d7a25f931280db556343b40c`  
		Last Modified: Wed, 15 Apr 2026 23:18:11 GMT  
		Size: 1.9 KB (1950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765d3671346423e43c32453bc2f41a65a749568e1a9d06b18de89adfd7f78f34`  
		Last Modified: Wed, 15 Apr 2026 23:18:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.1` - unknown; unknown

```console
$ docker pull eggdrop@sha256:6bf107b85ef0332efe7166e4243ffa778728dbf5a3805d25e729db8e5e35dd30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 KB (164534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ccd7ea2fe64cb99fe52f0be3f35e34e7274007933542fe8fd9779ac828aa70`

```dockerfile
```

-	Layers:
	-	`sha256:ecf02737a699a21fda090418f32dd1674c81d6de2ef17f4d88aba0173ee6ecb7`  
		Last Modified: Wed, 15 Apr 2026 23:18:11 GMT  
		Size: 146.1 KB (146050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33388028f91f6acff118c365a280d284aca755bb9901e3db6d3209226e588bc5`  
		Last Modified: Wed, 15 Apr 2026 23:18:11 GMT  
		Size: 18.5 KB (18484 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:666e4a892765cda5c7c970df1af74a2a39fc8d666eb589dd7051da729fb277e8
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
$ docker pull eggdrop@sha256:e9950121ce910ba4202bad49480397ca324582ab5e488d198c40b19dd29d6713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11287423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b54173944d710f2d965fe321e1df5aa13d39e7b212cb477483bd6e6a1b0443d`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:13:43 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 15 Apr 2026 23:13:43 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 15 Apr 2026 23:13:45 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl tcl9 tcl9-dev # buildkit
# Wed, 15 Apr 2026 23:13:45 GMT
ENV EGGDROP_SHA256=e42668f102c1446901b066d13fe0bf39622afca8d723f356ac2390d5faaf6e5e
# Wed, 15 Apr 2026 23:13:45 GMT
ENV EGGDROP_COMMIT=541e8ac17e549a40e177b5eea54e4abf24629a33
# Wed, 15 Apr 2026 23:14:01 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 15 Apr 2026 23:14:01 GMT
ENV NICK=
# Wed, 15 Apr 2026 23:14:01 GMT
ENV SERVER=
# Wed, 15 Apr 2026 23:14:01 GMT
ENV LISTEN=3333
# Wed, 15 Apr 2026 23:14:01 GMT
ENV USERFILE=eggdrop.user
# Wed, 15 Apr 2026 23:14:01 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 15 Apr 2026 23:14:01 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 15 Apr 2026 23:14:01 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 15 Apr 2026 23:14:01 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 15 Apr 2026 23:14:01 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 15 Apr 2026 23:14:01 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 15 Apr 2026 23:14:01 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d3f36bc274178e9cf0c997c9995ccae73b4483b90dc54812a57e09e58046a1`  
		Last Modified: Wed, 15 Apr 2026 23:14:07 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7f29b577422ce2a44c969d5f946cf87c68ff68076d1d78010f2d2c5c9415ac`  
		Last Modified: Wed, 15 Apr 2026 23:14:07 GMT  
		Size: 4.7 MB (4749966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed8515cc3aa2ef55ff12dbb1b49aa29c23aff53788847667c63efd93d4e7bf9`  
		Last Modified: Wed, 15 Apr 2026 23:14:07 GMT  
		Size: 2.7 MB (2669196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1eec04bdb91d8c45196ec27e91a5f1c33ff97cae6e884d5472c92a5443a6baa`  
		Last Modified: Wed, 15 Apr 2026 23:14:07 GMT  
		Size: 2.0 KB (1963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8136ba79ce0f9fc46d084dccfc5ca0b7d51a4cdffa0f9db244156e6e4f86ab`  
		Last Modified: Wed, 15 Apr 2026 23:14:08 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:d34b0451d989c0795f490f73921baa3e35aa28105ef3d636365953e7e156d4d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **754.0 KB (754019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85d3eb681a399e7aa2394d95f91cb369f47a54899152646aa9b43005c5157ac`

```dockerfile
```

-	Layers:
	-	`sha256:8d18ab7f6050c0bf6a8a11a75e4e7ea14ac7fcdb9217f5b81996b79ac497353e`  
		Last Modified: Wed, 15 Apr 2026 23:14:07 GMT  
		Size: 738.2 KB (738227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe9f1842f8e1a6418f24751c4b4ae2a2c4307abdb88bf47ce573cc46e38fdea2`  
		Last Modified: Wed, 15 Apr 2026 23:14:07 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:0a9fd250fcab458c40735a85e42d6e95b0d63d775afd599b2d5d3f0943173497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (10966036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0189d93460064e265df5513975bbffc3378bf4b85555dbdfc0a6b54ecb55b04`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:13:08 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 15 Apr 2026 23:13:08 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 15 Apr 2026 23:13:10 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl tcl9 tcl9-dev # buildkit
# Wed, 15 Apr 2026 23:13:10 GMT
ENV EGGDROP_SHA256=e42668f102c1446901b066d13fe0bf39622afca8d723f356ac2390d5faaf6e5e
# Wed, 15 Apr 2026 23:13:10 GMT
ENV EGGDROP_COMMIT=541e8ac17e549a40e177b5eea54e4abf24629a33
# Wed, 15 Apr 2026 23:13:30 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 15 Apr 2026 23:13:30 GMT
ENV NICK=
# Wed, 15 Apr 2026 23:13:30 GMT
ENV SERVER=
# Wed, 15 Apr 2026 23:13:30 GMT
ENV LISTEN=3333
# Wed, 15 Apr 2026 23:13:30 GMT
ENV USERFILE=eggdrop.user
# Wed, 15 Apr 2026 23:13:30 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 15 Apr 2026 23:13:31 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 15 Apr 2026 23:13:31 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 15 Apr 2026 23:13:31 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 15 Apr 2026 23:13:31 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 15 Apr 2026 23:13:31 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 15 Apr 2026 23:13:31 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5ac7e0d6f968ff7f1963fd26ee579d9958c1bee0d2d5eb55acdaf5d5dd1126`  
		Last Modified: Wed, 15 Apr 2026 23:13:35 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7adba4b481ebecd1aa5ad5ddcd9208d17d014302c93399f60e89165aba3bc0`  
		Last Modified: Wed, 15 Apr 2026 23:13:36 GMT  
		Size: 4.7 MB (4708171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85d4f9a5f70b9df5160b0bafbe61fe83d8a4093998914c54e6711c3482df315`  
		Last Modified: Wed, 15 Apr 2026 23:13:36 GMT  
		Size: 2.7 MB (2681923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031ef5c760f5deaead1ed263ac8ed7fee8b59b5972c6985423643ef5b5869a14`  
		Last Modified: Wed, 15 Apr 2026 23:13:36 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196e78aca3c655572a461d79618618158cfac06449b877ade5987542f0a65b8d`  
		Last Modified: Wed, 15 Apr 2026 23:13:37 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:5857c7c4a8a6c8d948158bf9edc168b9945f6564da05c1420e64fe1034ebbbea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 KB (15659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7fb3668341d0ccb54bdc157fb98b9d76db15045ab5c9a04fcbdf0b60cd5c33b`

```dockerfile
```

-	Layers:
	-	`sha256:f5bd723bd399876662b1201a5b67868a6f07af8f01e39137bb5ab0d91243abb6`  
		Last Modified: Wed, 15 Apr 2026 23:13:35 GMT  
		Size: 15.7 KB (15659 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:2c9332a895e9b8a0cc500ccde5c1f1ef252dbdf354468727cdadd67757b6afd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11712810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83526d1b3273ce138fd04307fc90b68a37604dec4a5eaf712ee81952047f5e19`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:13:18 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 15 Apr 2026 23:13:18 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 15 Apr 2026 23:13:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl tcl9 tcl9-dev # buildkit
# Wed, 15 Apr 2026 23:13:19 GMT
ENV EGGDROP_SHA256=e42668f102c1446901b066d13fe0bf39622afca8d723f356ac2390d5faaf6e5e
# Wed, 15 Apr 2026 23:13:19 GMT
ENV EGGDROP_COMMIT=541e8ac17e549a40e177b5eea54e4abf24629a33
# Wed, 15 Apr 2026 23:13:35 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 15 Apr 2026 23:13:35 GMT
ENV NICK=
# Wed, 15 Apr 2026 23:13:35 GMT
ENV SERVER=
# Wed, 15 Apr 2026 23:13:35 GMT
ENV LISTEN=3333
# Wed, 15 Apr 2026 23:13:35 GMT
ENV USERFILE=eggdrop.user
# Wed, 15 Apr 2026 23:13:35 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 15 Apr 2026 23:13:35 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 15 Apr 2026 23:13:35 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 15 Apr 2026 23:13:35 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 15 Apr 2026 23:13:36 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 15 Apr 2026 23:13:36 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 15 Apr 2026 23:13:36 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0917f956f3193e362e9996b0aaf09dfcbec0dd4237ec2b5586573c8ad3d12300`  
		Last Modified: Wed, 15 Apr 2026 23:13:41 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f134e415348636293acd9fb5208ff982aaab8ffb1b9ade56a98396a8341732`  
		Last Modified: Wed, 15 Apr 2026 23:13:41 GMT  
		Size: 4.8 MB (4823830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c981992008899ae79291752bebfcf3e31ee3ab8fd8acb29ede1d35cf4746d6`  
		Last Modified: Wed, 15 Apr 2026 23:13:41 GMT  
		Size: 2.7 MB (2685032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3727664a4c7d8f3e385cd64bd918176db313d61d3d92239adb0c837994001c`  
		Last Modified: Wed, 15 Apr 2026 23:13:41 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acedb75c1470eb5b6132f256ccfb72bf3690eb28c816e1a485163f4650f42cd`  
		Last Modified: Wed, 15 Apr 2026 23:13:42 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:cbe0b6a7ff924773eb2d6e31c5c853385cd434b14727163c10e1def4e208da6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **753.5 KB (753486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a98fb89a483b596747ffcc7616399dae88c944ce937478e178dbb4214c1077`

```dockerfile
```

-	Layers:
	-	`sha256:9dda099678bfba2422cf3d1510550671a2ae23b9485830b25af0c5c266af858a`  
		Last Modified: Wed, 15 Apr 2026 23:13:41 GMT  
		Size: 737.6 KB (737597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb426b300dfc66628ab8ddf6389d6b207dc8746ff469e1031db48a0b9799c3a6`  
		Last Modified: Wed, 15 Apr 2026 23:13:41 GMT  
		Size: 15.9 KB (15889 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:08d135f49c8c983b685644c44df27bae2c744a02ff9b7294757eaaa512ed82cb
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
$ docker pull eggdrop@sha256:5d171b38421fe7bc8a72c368e175d3265744fb7829a9a9aab9c0b684e61124e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15565657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb94c0ae33f68189af54b6de7f5c0145bfab04ab385adc3b4352c59750b9b68`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:14:16 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 15 Apr 2026 23:14:16 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 15 Apr 2026 23:14:17 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 15 Apr 2026 23:17:27 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz.asc   && gpg --batch --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1.tar.gz.asc eggdrop-1.10.1.tar.gz   && gpgconf --kill all   && rm eggdrop-1.10.1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1.tar.gz   && rm eggdrop-1.10.1.tar.gz   && ( cd eggdrop-1.10.1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 15 Apr 2026 23:17:27 GMT
ENV NICK=
# Wed, 15 Apr 2026 23:17:27 GMT
ENV SERVER=
# Wed, 15 Apr 2026 23:17:27 GMT
ENV LISTEN=3333
# Wed, 15 Apr 2026 23:17:27 GMT
ENV USERFILE=eggdrop.user
# Wed, 15 Apr 2026 23:17:27 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 15 Apr 2026 23:17:28 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 15 Apr 2026 23:17:28 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 15 Apr 2026 23:17:28 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 15 Apr 2026 23:17:28 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 15 Apr 2026 23:17:28 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 15 Apr 2026 23:17:28 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c209b08b29ce83885852263414073aefed7cac9e232b76ae57152e1eece61f3b`  
		Last Modified: Wed, 15 Apr 2026 23:17:34 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19e8c421d8a0bd2f54014a2e51097343778cb22d6693193ddcca8aefec71c8a`  
		Last Modified: Wed, 15 Apr 2026 23:17:34 GMT  
		Size: 3.4 MB (3407097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4caa010fc1b94160a654004e2ce27cbac439082c568fef7654fda4977954eeb`  
		Last Modified: Wed, 15 Apr 2026 23:17:34 GMT  
		Size: 8.5 MB (8510759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1ccf005bd8ad6910ee629138d0326911f6de9e7e5b0288cbe5b34dab140abd`  
		Last Modified: Wed, 15 Apr 2026 23:17:34 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c1805be816fa0749705a4bcf5e75e484976e63474c1465e8be8a141216a676`  
		Last Modified: Wed, 15 Apr 2026 23:17:35 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:72535bbe7a2fc471a255f0050d6896c8748fb04d8bb7b0c579fa4ecaa87190ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 KB (164344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95932f5bb9df8a68c36453f9d6176f34b28dac8da668c34fac79d55234e125c`

```dockerfile
```

-	Layers:
	-	`sha256:c48b17163cbccdefb0df63af915d30a44963fefbfdc3bdd485852efd1bd92536`  
		Last Modified: Wed, 15 Apr 2026 23:17:34 GMT  
		Size: 146.0 KB (145994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd518cde3ddeac191da477649cbd37c3658e02c4a6fdae5d644760615cfb219`  
		Last Modified: Wed, 15 Apr 2026 23:17:34 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:d619fdb9ce50eea17c0361953e1614000526503daf85c72b6a14d9e2072d7306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14769130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7f80741aa6838886a467b403dec6fc44aac1988d96eb4bd91650942060cd22`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.21.6-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:13:21 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 15 Apr 2026 23:13:21 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 15 Apr 2026 23:13:22 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 15 Apr 2026 23:18:16 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz.asc   && gpg --batch --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1.tar.gz.asc eggdrop-1.10.1.tar.gz   && gpgconf --kill all   && rm eggdrop-1.10.1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1.tar.gz   && rm eggdrop-1.10.1.tar.gz   && ( cd eggdrop-1.10.1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 15 Apr 2026 23:18:16 GMT
ENV NICK=
# Wed, 15 Apr 2026 23:18:16 GMT
ENV SERVER=
# Wed, 15 Apr 2026 23:18:16 GMT
ENV LISTEN=3333
# Wed, 15 Apr 2026 23:18:16 GMT
ENV USERFILE=eggdrop.user
# Wed, 15 Apr 2026 23:18:16 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 15 Apr 2026 23:18:16 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 15 Apr 2026 23:18:16 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 15 Apr 2026 23:18:16 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 15 Apr 2026 23:18:16 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 15 Apr 2026 23:18:16 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 15 Apr 2026 23:18:16 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a7fd0d978b605e6a6ed974adfe73f3035a5a60d1bebd2c9d5bb111651502c33e`  
		Last Modified: Wed, 28 Jan 2026 01:18:08 GMT  
		Size: 3.4 MB (3365870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9441c2310bd656e7ad2cb8a3d35fe1676c90bcccc140d53cb4c46ff6952ec71e`  
		Last Modified: Wed, 15 Apr 2026 23:18:21 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc2e1af5e377bfff332edeeefe1527f18503bf00153ae73bc8d6b8689efe3bd`  
		Last Modified: Wed, 15 Apr 2026 23:18:21 GMT  
		Size: 3.1 MB (3076252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4ba4813ca5c38ab1c114e1b67b8e8471d4c9919046274e5847c1ce696ec1ee`  
		Last Modified: Wed, 15 Apr 2026 23:18:21 GMT  
		Size: 8.3 MB (8322941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554113e79ea3f9a788f298a09771242c989884fe6bd86f3aa293035385f8f5f9`  
		Last Modified: Wed, 15 Apr 2026 23:18:21 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17895c5dd373524390034c773d87fff653b7f8641d8a349452a3004358b57ea0`  
		Last Modified: Wed, 15 Apr 2026 23:18:22 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:f8fd8de3cf4cb83f53f93102846e9622b266162cf3afb9a7dba9e9fa2f985da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fe16aba2353cbd94ac34d30a21d2d8c8c1528ab57b3489960117b288a536ce`

```dockerfile
```

-	Layers:
	-	`sha256:b309d42f28e884e0829955798ca0731edc85243b50f177491b9ab46df686a879`  
		Last Modified: Wed, 15 Apr 2026 23:18:21 GMT  
		Size: 18.2 KB (18241 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:32c9709246f525349b7673b26b48865ae2eac7883d823777f227666f2b1d59e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16333774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24538fd30da3ded0b76d47bf15c520f0b5d75248e02b1f239039fdde21831471`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:14:12 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 15 Apr 2026 23:14:12 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 15 Apr 2026 23:14:13 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 15 Apr 2026 23:18:05 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz.asc   && gpg --batch --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1.tar.gz.asc eggdrop-1.10.1.tar.gz   && gpgconf --kill all   && rm eggdrop-1.10.1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1.tar.gz   && rm eggdrop-1.10.1.tar.gz   && ( cd eggdrop-1.10.1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 15 Apr 2026 23:18:05 GMT
ENV NICK=
# Wed, 15 Apr 2026 23:18:05 GMT
ENV SERVER=
# Wed, 15 Apr 2026 23:18:05 GMT
ENV LISTEN=3333
# Wed, 15 Apr 2026 23:18:05 GMT
ENV USERFILE=eggdrop.user
# Wed, 15 Apr 2026 23:18:05 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 15 Apr 2026 23:18:05 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 15 Apr 2026 23:18:05 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 15 Apr 2026 23:18:05 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 15 Apr 2026 23:18:05 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 15 Apr 2026 23:18:05 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 15 Apr 2026 23:18:05 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6f59a843adb27b7856e4d35a57e285ff6ee6e0489fd2f71fd305af70c15d0a`  
		Last Modified: Wed, 15 Apr 2026 23:18:11 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5322ea15110e272eb2fa108f7824ff76350b4b02d221ffab492baf0daaebbd4`  
		Last Modified: Wed, 15 Apr 2026 23:18:11 GMT  
		Size: 3.8 MB (3773617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964d33f9be0696f4a62682ee36578ebdbaff836e2eee5b0055b2235c1927c70c`  
		Last Modified: Wed, 15 Apr 2026 23:18:12 GMT  
		Size: 8.6 MB (8563214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9609e921af887592121877325056eaa6421a8a9d7a25f931280db556343b40c`  
		Last Modified: Wed, 15 Apr 2026 23:18:11 GMT  
		Size: 1.9 KB (1950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765d3671346423e43c32453bc2f41a65a749568e1a9d06b18de89adfd7f78f34`  
		Last Modified: Wed, 15 Apr 2026 23:18:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:6bf107b85ef0332efe7166e4243ffa778728dbf5a3805d25e729db8e5e35dd30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 KB (164534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ccd7ea2fe64cb99fe52f0be3f35e34e7274007933542fe8fd9779ac828aa70`

```dockerfile
```

-	Layers:
	-	`sha256:ecf02737a699a21fda090418f32dd1674c81d6de2ef17f4d88aba0173ee6ecb7`  
		Last Modified: Wed, 15 Apr 2026 23:18:11 GMT  
		Size: 146.1 KB (146050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33388028f91f6acff118c365a280d284aca755bb9901e3db6d3209226e588bc5`  
		Last Modified: Wed, 15 Apr 2026 23:18:11 GMT  
		Size: 18.5 KB (18484 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:08d135f49c8c983b685644c44df27bae2c744a02ff9b7294757eaaa512ed82cb
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
$ docker pull eggdrop@sha256:5d171b38421fe7bc8a72c368e175d3265744fb7829a9a9aab9c0b684e61124e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15565657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb94c0ae33f68189af54b6de7f5c0145bfab04ab385adc3b4352c59750b9b68`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:14:16 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 15 Apr 2026 23:14:16 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 15 Apr 2026 23:14:17 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 15 Apr 2026 23:17:27 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz.asc   && gpg --batch --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1.tar.gz.asc eggdrop-1.10.1.tar.gz   && gpgconf --kill all   && rm eggdrop-1.10.1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1.tar.gz   && rm eggdrop-1.10.1.tar.gz   && ( cd eggdrop-1.10.1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 15 Apr 2026 23:17:27 GMT
ENV NICK=
# Wed, 15 Apr 2026 23:17:27 GMT
ENV SERVER=
# Wed, 15 Apr 2026 23:17:27 GMT
ENV LISTEN=3333
# Wed, 15 Apr 2026 23:17:27 GMT
ENV USERFILE=eggdrop.user
# Wed, 15 Apr 2026 23:17:27 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 15 Apr 2026 23:17:28 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 15 Apr 2026 23:17:28 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 15 Apr 2026 23:17:28 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 15 Apr 2026 23:17:28 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 15 Apr 2026 23:17:28 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 15 Apr 2026 23:17:28 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c209b08b29ce83885852263414073aefed7cac9e232b76ae57152e1eece61f3b`  
		Last Modified: Wed, 15 Apr 2026 23:17:34 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19e8c421d8a0bd2f54014a2e51097343778cb22d6693193ddcca8aefec71c8a`  
		Last Modified: Wed, 15 Apr 2026 23:17:34 GMT  
		Size: 3.4 MB (3407097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4caa010fc1b94160a654004e2ce27cbac439082c568fef7654fda4977954eeb`  
		Last Modified: Wed, 15 Apr 2026 23:17:34 GMT  
		Size: 8.5 MB (8510759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1ccf005bd8ad6910ee629138d0326911f6de9e7e5b0288cbe5b34dab140abd`  
		Last Modified: Wed, 15 Apr 2026 23:17:34 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c1805be816fa0749705a4bcf5e75e484976e63474c1465e8be8a141216a676`  
		Last Modified: Wed, 15 Apr 2026 23:17:35 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:72535bbe7a2fc471a255f0050d6896c8748fb04d8bb7b0c579fa4ecaa87190ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 KB (164344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95932f5bb9df8a68c36453f9d6176f34b28dac8da668c34fac79d55234e125c`

```dockerfile
```

-	Layers:
	-	`sha256:c48b17163cbccdefb0df63af915d30a44963fefbfdc3bdd485852efd1bd92536`  
		Last Modified: Wed, 15 Apr 2026 23:17:34 GMT  
		Size: 146.0 KB (145994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd518cde3ddeac191da477649cbd37c3658e02c4a6fdae5d644760615cfb219`  
		Last Modified: Wed, 15 Apr 2026 23:17:34 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:d619fdb9ce50eea17c0361953e1614000526503daf85c72b6a14d9e2072d7306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14769130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7f80741aa6838886a467b403dec6fc44aac1988d96eb4bd91650942060cd22`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.21.6-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:13:21 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 15 Apr 2026 23:13:21 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 15 Apr 2026 23:13:22 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 15 Apr 2026 23:18:16 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz.asc   && gpg --batch --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1.tar.gz.asc eggdrop-1.10.1.tar.gz   && gpgconf --kill all   && rm eggdrop-1.10.1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1.tar.gz   && rm eggdrop-1.10.1.tar.gz   && ( cd eggdrop-1.10.1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 15 Apr 2026 23:18:16 GMT
ENV NICK=
# Wed, 15 Apr 2026 23:18:16 GMT
ENV SERVER=
# Wed, 15 Apr 2026 23:18:16 GMT
ENV LISTEN=3333
# Wed, 15 Apr 2026 23:18:16 GMT
ENV USERFILE=eggdrop.user
# Wed, 15 Apr 2026 23:18:16 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 15 Apr 2026 23:18:16 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 15 Apr 2026 23:18:16 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 15 Apr 2026 23:18:16 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 15 Apr 2026 23:18:16 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 15 Apr 2026 23:18:16 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 15 Apr 2026 23:18:16 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a7fd0d978b605e6a6ed974adfe73f3035a5a60d1bebd2c9d5bb111651502c33e`  
		Last Modified: Wed, 28 Jan 2026 01:18:08 GMT  
		Size: 3.4 MB (3365870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9441c2310bd656e7ad2cb8a3d35fe1676c90bcccc140d53cb4c46ff6952ec71e`  
		Last Modified: Wed, 15 Apr 2026 23:18:21 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc2e1af5e377bfff332edeeefe1527f18503bf00153ae73bc8d6b8689efe3bd`  
		Last Modified: Wed, 15 Apr 2026 23:18:21 GMT  
		Size: 3.1 MB (3076252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4ba4813ca5c38ab1c114e1b67b8e8471d4c9919046274e5847c1ce696ec1ee`  
		Last Modified: Wed, 15 Apr 2026 23:18:21 GMT  
		Size: 8.3 MB (8322941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554113e79ea3f9a788f298a09771242c989884fe6bd86f3aa293035385f8f5f9`  
		Last Modified: Wed, 15 Apr 2026 23:18:21 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17895c5dd373524390034c773d87fff653b7f8641d8a349452a3004358b57ea0`  
		Last Modified: Wed, 15 Apr 2026 23:18:22 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:f8fd8de3cf4cb83f53f93102846e9622b266162cf3afb9a7dba9e9fa2f985da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fe16aba2353cbd94ac34d30a21d2d8c8c1528ab57b3489960117b288a536ce`

```dockerfile
```

-	Layers:
	-	`sha256:b309d42f28e884e0829955798ca0731edc85243b50f177491b9ab46df686a879`  
		Last Modified: Wed, 15 Apr 2026 23:18:21 GMT  
		Size: 18.2 KB (18241 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:32c9709246f525349b7673b26b48865ae2eac7883d823777f227666f2b1d59e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16333774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24538fd30da3ded0b76d47bf15c520f0b5d75248e02b1f239039fdde21831471`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:14:12 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 15 Apr 2026 23:14:12 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 15 Apr 2026 23:14:13 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 15 Apr 2026 23:18:05 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz.asc   && gpg --batch --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1.tar.gz.asc eggdrop-1.10.1.tar.gz   && gpgconf --kill all   && rm eggdrop-1.10.1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1.tar.gz   && rm eggdrop-1.10.1.tar.gz   && ( cd eggdrop-1.10.1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 15 Apr 2026 23:18:05 GMT
ENV NICK=
# Wed, 15 Apr 2026 23:18:05 GMT
ENV SERVER=
# Wed, 15 Apr 2026 23:18:05 GMT
ENV LISTEN=3333
# Wed, 15 Apr 2026 23:18:05 GMT
ENV USERFILE=eggdrop.user
# Wed, 15 Apr 2026 23:18:05 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 15 Apr 2026 23:18:05 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 15 Apr 2026 23:18:05 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 15 Apr 2026 23:18:05 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 15 Apr 2026 23:18:05 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 15 Apr 2026 23:18:05 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 15 Apr 2026 23:18:05 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6f59a843adb27b7856e4d35a57e285ff6ee6e0489fd2f71fd305af70c15d0a`  
		Last Modified: Wed, 15 Apr 2026 23:18:11 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5322ea15110e272eb2fa108f7824ff76350b4b02d221ffab492baf0daaebbd4`  
		Last Modified: Wed, 15 Apr 2026 23:18:11 GMT  
		Size: 3.8 MB (3773617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964d33f9be0696f4a62682ee36578ebdbaff836e2eee5b0055b2235c1927c70c`  
		Last Modified: Wed, 15 Apr 2026 23:18:12 GMT  
		Size: 8.6 MB (8563214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9609e921af887592121877325056eaa6421a8a9d7a25f931280db556343b40c`  
		Last Modified: Wed, 15 Apr 2026 23:18:11 GMT  
		Size: 1.9 KB (1950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765d3671346423e43c32453bc2f41a65a749568e1a9d06b18de89adfd7f78f34`  
		Last Modified: Wed, 15 Apr 2026 23:18:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:6bf107b85ef0332efe7166e4243ffa778728dbf5a3805d25e729db8e5e35dd30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 KB (164534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ccd7ea2fe64cb99fe52f0be3f35e34e7274007933542fe8fd9779ac828aa70`

```dockerfile
```

-	Layers:
	-	`sha256:ecf02737a699a21fda090418f32dd1674c81d6de2ef17f4d88aba0173ee6ecb7`  
		Last Modified: Wed, 15 Apr 2026 23:18:11 GMT  
		Size: 146.1 KB (146050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33388028f91f6acff118c365a280d284aca755bb9901e3db6d3209226e588bc5`  
		Last Modified: Wed, 15 Apr 2026 23:18:11 GMT  
		Size: 18.5 KB (18484 bytes)  
		MIME: application/vnd.in-toto+json
