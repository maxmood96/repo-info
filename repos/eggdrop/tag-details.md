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
$ docker pull eggdrop@sha256:858360ee8ee58d2579ffad42b6e494c8067beb66ddaea7154c7932da48e5b77b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:1.10.0rc1` - linux; amd64

```console
$ docker pull eggdrop@sha256:914c048e431613819e306c9c50f4f195d8be6f4554534a05480816946046f3ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19733445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32acc7087fb5ba23b19927354064e84645b7e44ab93ee278617e9b97462e5317`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:45:15 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:45:15 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Thu, 08 Aug 2024 15:45:15 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0rc1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0rc1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0rc1.tar.gz.asc eggdrop-1.10.0rc1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0rc1.tar.gz.asc   && tar -zxvf eggdrop-1.10.0rc1.tar.gz   && rm eggdrop-1.10.0rc1.tar.gz   && ( cd eggdrop-1.10.0rc1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10rc1.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:45:15 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:45:15 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:45:15 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:45:15 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:45:15 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:45:15 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:45:15 GMT
COPY entrypoint.sh ./ # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
COPY docker.tcl ./scripts/ # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:45:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d722220e1204a5082d3474e410936fec183591603689939760942449fd4fc9dd`  
		Last Modified: Tue, 12 Nov 2024 03:07:43 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106c3c6b16fcaab89ee4a82110f85643ee04b9c460c0d0ab9713fbf614537e0e`  
		Last Modified: Tue, 12 Nov 2024 03:07:43 GMT  
		Size: 3.4 MB (3391833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b921b500ce0d3e0bdd2916475c1ec129a3ccb65f3983a14b14f771ec9be95d2a`  
		Last Modified: Tue, 12 Nov 2024 03:07:43 GMT  
		Size: 12.7 MB (12713632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69241846017b1344bde0af724768ea9e70580f00323a538624e7ba396e44cd98`  
		Last Modified: Tue, 12 Nov 2024 03:07:43 GMT  
		Size: 2.0 KB (1951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c0b9c16a075d7a3a3b659dd945e86ed7a7de0c7afc7c0ea3a50baacc6698be`  
		Last Modified: Tue, 12 Nov 2024 03:07:44 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.0rc1` - unknown; unknown

```console
$ docker pull eggdrop@sha256:288321bb470084b1f8a119a515b1b5801bd3bdefa691f6c297ffd84d6f255a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 KB (154098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3be032efb42d4120502b8964dbe46f7806512bf1aa28413095ea101693f6b3b`

```dockerfile
```

-	Layers:
	-	`sha256:21648e464930f465d659f94fbcafe341f273a36b353d7681b097d2a094267b4e`  
		Last Modified: Tue, 12 Nov 2024 03:07:43 GMT  
		Size: 136.1 KB (136149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c44e3b5853c98b39bfa7948ef7c77af7e1d19a38cbca53088ab0ceedd4bfd4f3`  
		Last Modified: Tue, 12 Nov 2024 03:07:43 GMT  
		Size: 17.9 KB (17949 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10.0rc1` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:a99b258d2507c1f3fd790c0521f1da74ca4306978080ffcbdea5e006e811f0f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (19001012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2e9a498c27e073d1132f5dafbeb2bf08c58c8638bc365be26674764a56a83e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:45:15 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:45:15 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Thu, 08 Aug 2024 15:45:15 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0rc1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0rc1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0rc1.tar.gz.asc eggdrop-1.10.0rc1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0rc1.tar.gz.asc   && tar -zxvf eggdrop-1.10.0rc1.tar.gz   && rm eggdrop-1.10.0rc1.tar.gz   && ( cd eggdrop-1.10.0rc1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10rc1.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:45:15 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:45:15 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:45:15 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:45:15 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:45:15 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:45:15 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:45:15 GMT
COPY entrypoint.sh ./ # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
COPY docker.tcl ./scripts/ # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:45:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cac87bfb663f752a8011ed98eb099ed601a6cbe4afbf6ce337a41eb855f0686`  
		Last Modified: Tue, 12 Nov 2024 02:24:42 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c84d6eb76cadcb16be0776aa51ef30c354c643dcb86ef8ee598176657855c7`  
		Last Modified: Tue, 12 Nov 2024 02:24:43 GMT  
		Size: 3.1 MB (3075746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892e8626aa9202f952874ba49d71aec6010614b2b7ff3f207ad27a08fce8ee3f`  
		Last Modified: Tue, 12 Nov 2024 02:33:51 GMT  
		Size: 12.6 MB (12554586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96d924e2298044703ea51fe711017c5c7d5c02c9173c3119b1e26eb8a0340b7`  
		Last Modified: Tue, 12 Nov 2024 02:33:50 GMT  
		Size: 2.0 KB (1954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f214276362ad0298e8b54ab5d321ab9fc7986aa5cd9ef30d4670f06d8dcfaa6`  
		Last Modified: Tue, 12 Nov 2024 02:33:51 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.0rc1` - unknown; unknown

```console
$ docker pull eggdrop@sha256:06ffff3701a9a00a7720270e7bf4411a920974744b152d9af8571eccdff8f219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 KB (17813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dddfbc6a376664d67c3a39e3fad2fef6868145521aae6e9f2832125ca64874d2`

```dockerfile
```

-	Layers:
	-	`sha256:455a6c3df1d81bbaabdb51df902fbae2baa3e6c97a56c80fb53b46e3422460ec`  
		Last Modified: Tue, 12 Nov 2024 02:33:50 GMT  
		Size: 17.8 KB (17813 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10.0rc1` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:75c5958d938e1eb61e60f0a47250d9676f62f820603dd4d3e45a3a0a935b6c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20841090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8adeb71b8a781319cd2611a96dd43e7d87f7a061bd559553eaac40002a6e0ce0`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:45:15 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:45:15 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Thu, 08 Aug 2024 15:45:15 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0rc1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0rc1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0rc1.tar.gz.asc eggdrop-1.10.0rc1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0rc1.tar.gz.asc   && tar -zxvf eggdrop-1.10.0rc1.tar.gz   && rm eggdrop-1.10.0rc1.tar.gz   && ( cd eggdrop-1.10.0rc1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10rc1.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:45:15 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:45:15 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:45:15 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:45:15 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:45:15 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:45:15 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:45:15 GMT
COPY entrypoint.sh ./ # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
COPY docker.tcl ./scripts/ # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:45:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b24a36091226bb8c146bddc8fab67e5ef8c1531389d34ef378e12b2a3d5fe5`  
		Last Modified: Tue, 12 Nov 2024 02:29:12 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f27dc5a2159bfe066d5067029ddbf05706fa282121e219aaa7706e20210f9a`  
		Last Modified: Tue, 12 Nov 2024 02:29:13 GMT  
		Size: 3.9 MB (3899863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c933b59405a4984f6bf3219018512c05c9a66ed11fa3478137807611c4c94dc`  
		Last Modified: Tue, 12 Nov 2024 02:35:50 GMT  
		Size: 12.8 MB (12849427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2681845726d80367230fedc822bd906cf5ceb4fa37a72297f963e0f7300f3c05`  
		Last Modified: Tue, 12 Nov 2024 02:35:49 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776b62d46e233e54ce00d37d88180b4e077c5cbc9639887866f6185d3b00cd46`  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.0rc1` - unknown; unknown

```console
$ docker pull eggdrop@sha256:4a250e06dc4265beb24a51420fad1accc281ee199d81925b3b8f2494839ce95f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 KB (154217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85b5cb290738687c5c6eee45d4cc8a192779ae6836c6234695c553f2ad3a5260`

```dockerfile
```

-	Layers:
	-	`sha256:086e983a7161fea546aea111a5daf7c9c425b9cb10502ded2801fa56534cf77d`  
		Last Modified: Tue, 12 Nov 2024 02:35:49 GMT  
		Size: 136.2 KB (136169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4b8e69e7ae3a26a81a9586aa09fe5569d8d0261556fe35d96ad931093907816`  
		Last Modified: Tue, 12 Nov 2024 02:35:49 GMT  
		Size: 18.0 KB (18048 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:1.9`

```console
$ docker pull eggdrop@sha256:6ee7a03529bacfb25e561f73737e642dde9ea6ebc07f578963aa8144dbc2753a
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
$ docker pull eggdrop@sha256:d58182d4fd2dfe38317305c74ee30b8be0e52991e816c4e3ae067d7e0efaeb17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14368318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277fb4aa7baeffb69e6aacb80ae72caea16fd6a6ba5af257e6941016954728f5`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e5a7b569dd4e69ba5137350e899653a5069a9676dfecc0b11d1ece82bf84e2`  
		Last Modified: Tue, 12 Nov 2024 02:18:23 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb16bc7b4a18332cb57e9fa464d2a363626a06bf67415a744def82cf9f9f3c98`  
		Last Modified: Tue, 12 Nov 2024 02:18:23 GMT  
		Size: 10.8 KB (10829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520c184b55f5b30d05e1abfdd4f7231be69a6f2855f55a3aed2bdb8895f65157`  
		Last Modified: Tue, 12 Nov 2024 02:18:23 GMT  
		Size: 5.0 MB (4969738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bd752aab17f337de75cadeaee28c031c9c0b7b009188d30e1c67d08892940f`  
		Size: 6.0 MB (5964216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edde18f7388fa2007b95f1aa3ab0b23a05fc37bb0d43c2b581a50e17f89c2c49`  
		Last Modified: Tue, 12 Nov 2024 02:18:24 GMT  
		Size: 1.8 KB (1828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9e8a2edb1344326fa5cb2deda3da8c9f03e441794a344a725e2d2cd3d21f11`  
		Last Modified: Tue, 12 Nov 2024 02:18:24 GMT  
		Size: 697.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9` - unknown; unknown

```console
$ docker pull eggdrop@sha256:d1d8c07ab3dc7de6e3db80e9b4f35d9271ba9894b2e46cfc3c681e14bf90516c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1065402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15624c9b09a5427c5e1a943395feb598f04bb45223c2dce6fbf7b5be8abcf0a`

```dockerfile
```

-	Layers:
	-	`sha256:51096e0f3fef4161df922c1306ef3b383e7f5793a3083518be4c85b8d570131f`  
		Last Modified: Tue, 12 Nov 2024 02:18:23 GMT  
		Size: 1.0 MB (1045446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae6ea397ae092007ed59c7e1fcd445852994f27256f77fa20e6178988ba3ba8a`  
		Last Modified: Tue, 12 Nov 2024 02:18:23 GMT  
		Size: 20.0 KB (19956 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:b53e8fd4b10afde38be4d8a68d45cc07339719c6a1ddeb6048091ea49eaf9672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13702581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c170d5dde2f48342c087942e4d7f9b1941995e02b44b49defd72d0154eef76`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
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
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42543951434ad86416c7a8c0be29ac67595e8ac14f508b1240afbe83dffd507`  
		Last Modified: Tue, 12 Nov 2024 02:30:14 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad8c6af06d108b01ff71d6c749ac67ea69b4960d2ae9df15b01aaf8d4125fef`  
		Last Modified: Tue, 12 Nov 2024 02:30:14 GMT  
		Size: 11.0 KB (10964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09f3e72f08335a7430883d658ea085c666cdbcea93e6412d0e0cb197c3ad9b`  
		Last Modified: Tue, 12 Nov 2024 02:30:15 GMT  
		Size: 4.7 MB (4651990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4729354c95a3340d54acfeeff80f1cb4a76a395312667a741fbb175fe98add4e`  
		Last Modified: Tue, 12 Nov 2024 02:30:15 GMT  
		Size: 5.9 MB (5859375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ad2caa1d94bd6007c7de4122de1f392d3b9d61e094686febb10206cccbf61d`  
		Last Modified: Tue, 12 Nov 2024 02:30:15 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9764e26e29b2f3f20759751eabc011e21188260b69bae51b3324407b44aab11a`  
		Last Modified: Tue, 12 Nov 2024 02:30:16 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9` - unknown; unknown

```console
$ docker pull eggdrop@sha256:8a2bf8939dea48d54ab7012ad76727d9c572d87af20717b7235914e973f1dd98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 KB (19855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38ec1ffb1a3eebcaa9100b122a8259170ca005741882b60db4c63cc29acfc96`

```dockerfile
```

-	Layers:
	-	`sha256:81dccc98cdf6eed0ea511af2301373bfe683c18b01215474f455c4632cdd7b6d`  
		Last Modified: Tue, 12 Nov 2024 02:30:14 GMT  
		Size: 19.9 KB (19855 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.9` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:142795ca9803ebffcd4c103aae10422b781e4bfac9de5ec76b2f7a318147fff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14381185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b6ea32313b2339c85108c1afca03c0ef93d943c65b67de1a46c4a79e592a62`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9c737ec1b35deb5c0e22bf4475ee18a2e023d4b4cd4a5249299536f6a37a6b`  
		Last Modified: Tue, 12 Nov 2024 02:33:15 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eda39ca2af7c4932d683ac6faaa4025363de707e9e2f1798ff5ab5744b57bd4`  
		Last Modified: Tue, 12 Nov 2024 02:33:14 GMT  
		Size: 11.4 KB (11354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc3310efece93421f24d59c6e91a9fc8fcc3e10490402449a281d99023a769f`  
		Last Modified: Tue, 12 Nov 2024 02:33:15 GMT  
		Size: 5.0 MB (4992041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ebefd0bf29a416273c31e56363b57fe1a6aad39fb7f163f662870f59e40ea8`  
		Last Modified: Tue, 12 Nov 2024 02:33:15 GMT  
		Size: 6.0 MB (6014735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c6b84cf6fe01c7550dbba6ff7134c934b8ef2d7a91710e1d68d1154811f8d1`  
		Last Modified: Tue, 12 Nov 2024 02:33:16 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189bf2641f0e1f37538fa11ad51ddcbe9717bc260118e9e96ebaaced54be7ab2`  
		Last Modified: Tue, 12 Nov 2024 02:33:16 GMT  
		Size: 697.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9` - unknown; unknown

```console
$ docker pull eggdrop@sha256:5c01b7b867557ccc08bc4790d5e507fca00ab193777b5c480d88585104b1e81e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1065607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb3954922b6b362f71d3b1b0415188566bfbef538f586ea9423d06d6ec96bd8`

```dockerfile
```

-	Layers:
	-	`sha256:ba42a25a9561e6bc41752ae23f9816b355382c13bdd228b58b74324a91366d2c`  
		Last Modified: Tue, 12 Nov 2024 02:33:15 GMT  
		Size: 1.0 MB (1045502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:501129403a4599e7fee7f3d300ff4ac10f8289a8fb4c9cc23918020543eb83e7`  
		Last Modified: Tue, 12 Nov 2024 02:33:15 GMT  
		Size: 20.1 KB (20105 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:1.9.5`

```console
$ docker pull eggdrop@sha256:6ee7a03529bacfb25e561f73737e642dde9ea6ebc07f578963aa8144dbc2753a
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
$ docker pull eggdrop@sha256:d58182d4fd2dfe38317305c74ee30b8be0e52991e816c4e3ae067d7e0efaeb17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14368318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277fb4aa7baeffb69e6aacb80ae72caea16fd6a6ba5af257e6941016954728f5`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e5a7b569dd4e69ba5137350e899653a5069a9676dfecc0b11d1ece82bf84e2`  
		Last Modified: Tue, 12 Nov 2024 02:18:23 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb16bc7b4a18332cb57e9fa464d2a363626a06bf67415a744def82cf9f9f3c98`  
		Last Modified: Tue, 12 Nov 2024 02:18:23 GMT  
		Size: 10.8 KB (10829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520c184b55f5b30d05e1abfdd4f7231be69a6f2855f55a3aed2bdb8895f65157`  
		Last Modified: Tue, 12 Nov 2024 02:18:23 GMT  
		Size: 5.0 MB (4969738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bd752aab17f337de75cadeaee28c031c9c0b7b009188d30e1c67d08892940f`  
		Size: 6.0 MB (5964216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edde18f7388fa2007b95f1aa3ab0b23a05fc37bb0d43c2b581a50e17f89c2c49`  
		Last Modified: Tue, 12 Nov 2024 02:18:24 GMT  
		Size: 1.8 KB (1828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9e8a2edb1344326fa5cb2deda3da8c9f03e441794a344a725e2d2cd3d21f11`  
		Last Modified: Tue, 12 Nov 2024 02:18:24 GMT  
		Size: 697.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9.5` - unknown; unknown

```console
$ docker pull eggdrop@sha256:d1d8c07ab3dc7de6e3db80e9b4f35d9271ba9894b2e46cfc3c681e14bf90516c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1065402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15624c9b09a5427c5e1a943395feb598f04bb45223c2dce6fbf7b5be8abcf0a`

```dockerfile
```

-	Layers:
	-	`sha256:51096e0f3fef4161df922c1306ef3b383e7f5793a3083518be4c85b8d570131f`  
		Last Modified: Tue, 12 Nov 2024 02:18:23 GMT  
		Size: 1.0 MB (1045446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae6ea397ae092007ed59c7e1fcd445852994f27256f77fa20e6178988ba3ba8a`  
		Last Modified: Tue, 12 Nov 2024 02:18:23 GMT  
		Size: 20.0 KB (19956 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.9.5` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:b53e8fd4b10afde38be4d8a68d45cc07339719c6a1ddeb6048091ea49eaf9672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13702581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c170d5dde2f48342c087942e4d7f9b1941995e02b44b49defd72d0154eef76`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
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
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42543951434ad86416c7a8c0be29ac67595e8ac14f508b1240afbe83dffd507`  
		Last Modified: Tue, 12 Nov 2024 02:30:14 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad8c6af06d108b01ff71d6c749ac67ea69b4960d2ae9df15b01aaf8d4125fef`  
		Last Modified: Tue, 12 Nov 2024 02:30:14 GMT  
		Size: 11.0 KB (10964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09f3e72f08335a7430883d658ea085c666cdbcea93e6412d0e0cb197c3ad9b`  
		Last Modified: Tue, 12 Nov 2024 02:30:15 GMT  
		Size: 4.7 MB (4651990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4729354c95a3340d54acfeeff80f1cb4a76a395312667a741fbb175fe98add4e`  
		Last Modified: Tue, 12 Nov 2024 02:30:15 GMT  
		Size: 5.9 MB (5859375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ad2caa1d94bd6007c7de4122de1f392d3b9d61e094686febb10206cccbf61d`  
		Last Modified: Tue, 12 Nov 2024 02:30:15 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9764e26e29b2f3f20759751eabc011e21188260b69bae51b3324407b44aab11a`  
		Last Modified: Tue, 12 Nov 2024 02:30:16 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9.5` - unknown; unknown

```console
$ docker pull eggdrop@sha256:8a2bf8939dea48d54ab7012ad76727d9c572d87af20717b7235914e973f1dd98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 KB (19855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38ec1ffb1a3eebcaa9100b122a8259170ca005741882b60db4c63cc29acfc96`

```dockerfile
```

-	Layers:
	-	`sha256:81dccc98cdf6eed0ea511af2301373bfe683c18b01215474f455c4632cdd7b6d`  
		Last Modified: Tue, 12 Nov 2024 02:30:14 GMT  
		Size: 19.9 KB (19855 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.9.5` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:142795ca9803ebffcd4c103aae10422b781e4bfac9de5ec76b2f7a318147fff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14381185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b6ea32313b2339c85108c1afca03c0ef93d943c65b67de1a46c4a79e592a62`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9c737ec1b35deb5c0e22bf4475ee18a2e023d4b4cd4a5249299536f6a37a6b`  
		Last Modified: Tue, 12 Nov 2024 02:33:15 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eda39ca2af7c4932d683ac6faaa4025363de707e9e2f1798ff5ab5744b57bd4`  
		Last Modified: Tue, 12 Nov 2024 02:33:14 GMT  
		Size: 11.4 KB (11354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc3310efece93421f24d59c6e91a9fc8fcc3e10490402449a281d99023a769f`  
		Last Modified: Tue, 12 Nov 2024 02:33:15 GMT  
		Size: 5.0 MB (4992041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ebefd0bf29a416273c31e56363b57fe1a6aad39fb7f163f662870f59e40ea8`  
		Last Modified: Tue, 12 Nov 2024 02:33:15 GMT  
		Size: 6.0 MB (6014735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c6b84cf6fe01c7550dbba6ff7134c934b8ef2d7a91710e1d68d1154811f8d1`  
		Last Modified: Tue, 12 Nov 2024 02:33:16 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189bf2641f0e1f37538fa11ad51ddcbe9717bc260118e9e96ebaaced54be7ab2`  
		Last Modified: Tue, 12 Nov 2024 02:33:16 GMT  
		Size: 697.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9.5` - unknown; unknown

```console
$ docker pull eggdrop@sha256:5c01b7b867557ccc08bc4790d5e507fca00ab193777b5c480d88585104b1e81e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1065607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb3954922b6b362f71d3b1b0415188566bfbef538f586ea9423d06d6ec96bd8`

```dockerfile
```

-	Layers:
	-	`sha256:ba42a25a9561e6bc41752ae23f9816b355382c13bdd228b58b74324a91366d2c`  
		Last Modified: Tue, 12 Nov 2024 02:33:15 GMT  
		Size: 1.0 MB (1045502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:501129403a4599e7fee7f3d300ff4ac10f8289a8fb4c9cc23918020543eb83e7`  
		Last Modified: Tue, 12 Nov 2024 02:33:15 GMT  
		Size: 20.1 KB (20105 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:8707e287bf7430406b3f2048b34658ab548a5bc2cf9ef91dfe09ce749ef7f1e0
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
$ docker pull eggdrop@sha256:ba872aff23094a30eaa6838554ce70381e66f2c91683eda5ab1f49c88ccf1ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18687102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b5c179ad9f8f493ed49092acce6fdea3424edb41cc5bdb43082dc99ceb7d6b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:45:15 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:45:15 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Thu, 08 Aug 2024 15:45:15 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENV EGGDROP_SHA256=d185512ad282aeee49a75328e847f604c762e94be19fb1e01a7e8a4f927730b8
# Thu, 08 Aug 2024 15:45:15 GMT
ENV EGGDROP_COMMIT=f80f8ae468fd7bcec83407134ef5941225131104
# Thu, 08 Aug 2024 15:45:15 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:45:15 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:45:15 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:45:15 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:45:15 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:45:15 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:45:15 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:45:15 GMT
COPY entrypoint.sh ./ # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
COPY docker.tcl ./scripts/ # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:45:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6256f4e54550df2409efdfa86ba3d8fcdbcfe40a1d10756972ce4785955a906a`  
		Last Modified: Tue, 12 Nov 2024 02:12:36 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478d342f80b75ef32a72040d548e8c478c8ba4e23878854f6e3a01999d502126`  
		Last Modified: Tue, 12 Nov 2024 02:12:36 GMT  
		Size: 3.4 MB (3391840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1769cb2904e96950eaff9506da16b7f793a76ea655bec0e47e91037d97df608c`  
		Last Modified: Tue, 12 Nov 2024 02:12:36 GMT  
		Size: 11.7 MB (11667279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686e5158e92ce1a2fd02a75d20a7e569b7aa7ca15d9b6cc98f852b74e58d1672`  
		Last Modified: Tue, 12 Nov 2024 02:12:36 GMT  
		Size: 2.0 KB (1953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3c56ae5709b9b9491adb3450185a90c252d0317ac8f2c12405df534e4340e8`  
		Last Modified: Tue, 12 Nov 2024 02:12:37 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:3ed26bbf051068437c26b68731788fd36143dd5a289ddd6b9a6234109cfdbcce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 KB (153497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e072ad35bcc6c2c938ebdb9e2abf2dd61ff562ded949276b82afd816f659e3b`

```dockerfile
```

-	Layers:
	-	`sha256:b6a41726558387ec03eb989d5799932432e545776af9c2e37517c1fa9910c72f`  
		Last Modified: Tue, 12 Nov 2024 02:12:36 GMT  
		Size: 136.1 KB (136145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55aa27aae26f19058cd9a17b8c43e9086d579d150da90577411bb3bf19431c98`  
		Last Modified: Tue, 12 Nov 2024 02:12:36 GMT  
		Size: 17.4 KB (17352 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:1c9b0d50c0238dd28314f0398989fbfe8ca4ac9aa89c06165d7fcd0aaf281301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17928152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9087700c46ac352bf3ba19d5cbe6a7d2842ecf6b5e266795723a27ae42e96ff`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:45:15 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:45:15 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Thu, 08 Aug 2024 15:45:15 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENV EGGDROP_SHA256=d185512ad282aeee49a75328e847f604c762e94be19fb1e01a7e8a4f927730b8
# Thu, 08 Aug 2024 15:45:15 GMT
ENV EGGDROP_COMMIT=f80f8ae468fd7bcec83407134ef5941225131104
# Thu, 08 Aug 2024 15:45:15 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:45:15 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:45:15 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:45:15 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:45:15 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:45:15 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:45:15 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:45:15 GMT
COPY entrypoint.sh ./ # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
COPY docker.tcl ./scripts/ # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:45:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cac87bfb663f752a8011ed98eb099ed601a6cbe4afbf6ce337a41eb855f0686`  
		Last Modified: Tue, 12 Nov 2024 02:24:42 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c84d6eb76cadcb16be0776aa51ef30c354c643dcb86ef8ee598176657855c7`  
		Last Modified: Tue, 12 Nov 2024 02:24:43 GMT  
		Size: 3.1 MB (3075746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6b597093a50a142a5d153836590ce1c2e2995bd61012c89507c02f4ec12a7c`  
		Last Modified: Tue, 12 Nov 2024 02:24:43 GMT  
		Size: 11.5 MB (11481729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a7b7ce164f3d48c708f20a9a1aa8b3fb87a572995fbb8d399fdd8bb78ecf68`  
		Last Modified: Tue, 12 Nov 2024 02:24:43 GMT  
		Size: 2.0 KB (1953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca06d6fa793bc7d8d6af585a9c03547ee7884e5d426118a9c92fcbd2c421a17`  
		Last Modified: Tue, 12 Nov 2024 02:24:43 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:98cea7a58fb4a0481593899e5b32448ef851b2fe68efdcbdff8023c1991884f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6afc4ce9f06124dc33d58b31c0b43663aab16779d437e1cb707a370f38db07`

```dockerfile
```

-	Layers:
	-	`sha256:ebdbcd7ce4e9dec86cff2884513e5c520f7b56737afe9a2f7e2169877169e57f`  
		Last Modified: Tue, 12 Nov 2024 02:24:42 GMT  
		Size: 17.2 KB (17213 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:88aa7d8cd9448fb3073fdc8853bd7355bac7a55d858e9d960cc1a58ca14a52c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19692377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0b4998bd6e5f8f225401db4722cfabc6363da0c609235f29cd5b18e8e1846e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:45:15 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:45:15 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Thu, 08 Aug 2024 15:45:15 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENV EGGDROP_SHA256=d185512ad282aeee49a75328e847f604c762e94be19fb1e01a7e8a4f927730b8
# Thu, 08 Aug 2024 15:45:15 GMT
ENV EGGDROP_COMMIT=f80f8ae468fd7bcec83407134ef5941225131104
# Thu, 08 Aug 2024 15:45:15 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:45:15 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:45:15 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:45:15 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:45:15 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:45:15 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:45:15 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:45:15 GMT
COPY entrypoint.sh ./ # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
COPY docker.tcl ./scripts/ # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:45:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b24a36091226bb8c146bddc8fab67e5ef8c1531389d34ef378e12b2a3d5fe5`  
		Last Modified: Tue, 12 Nov 2024 02:29:12 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f27dc5a2159bfe066d5067029ddbf05706fa282121e219aaa7706e20210f9a`  
		Last Modified: Tue, 12 Nov 2024 02:29:13 GMT  
		Size: 3.9 MB (3899863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c71e23d2642c516ce7d1d841af4edd4bd81a5f1d339df3b12b2c8dd96fba1c`  
		Last Modified: Tue, 12 Nov 2024 02:29:13 GMT  
		Size: 11.7 MB (11700720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7203e1f99f97dc3c9f3cdbbce78220c78516e9e78b1a1ab5c527e0b56091f5a5`  
		Last Modified: Tue, 12 Nov 2024 02:29:13 GMT  
		Size: 1.9 KB (1946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e719535dc74af0ce666ecdb6d83b7526b0bb16aa75cefb6d9806ba7725cfac18`  
		Last Modified: Tue, 12 Nov 2024 02:29:13 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:f36a88d0badfdb240f6b12a2258fa2f2e30421a2da8a26a41e3f5451401a0016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.6 KB (153613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9e90a993788b8c70f50ab5d803b1aca5b17283d52cdb7fad4932bee38670e7`

```dockerfile
```

-	Layers:
	-	`sha256:5e653517d20bd52b6dce266706d7ce37f12e41e8f2fc654ca84ae5095129e7eb`  
		Last Modified: Tue, 12 Nov 2024 02:29:12 GMT  
		Size: 136.2 KB (136165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:262bd4d83b8b9d33ea97bf81c5f473269ce5928a184636c1ac267dcb77e7dcfb`  
		Last Modified: Tue, 12 Nov 2024 02:29:12 GMT  
		Size: 17.4 KB (17448 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:6ee7a03529bacfb25e561f73737e642dde9ea6ebc07f578963aa8144dbc2753a
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
$ docker pull eggdrop@sha256:d58182d4fd2dfe38317305c74ee30b8be0e52991e816c4e3ae067d7e0efaeb17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14368318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277fb4aa7baeffb69e6aacb80ae72caea16fd6a6ba5af257e6941016954728f5`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e5a7b569dd4e69ba5137350e899653a5069a9676dfecc0b11d1ece82bf84e2`  
		Last Modified: Tue, 12 Nov 2024 02:18:23 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb16bc7b4a18332cb57e9fa464d2a363626a06bf67415a744def82cf9f9f3c98`  
		Last Modified: Tue, 12 Nov 2024 02:18:23 GMT  
		Size: 10.8 KB (10829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520c184b55f5b30d05e1abfdd4f7231be69a6f2855f55a3aed2bdb8895f65157`  
		Last Modified: Tue, 12 Nov 2024 02:18:23 GMT  
		Size: 5.0 MB (4969738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bd752aab17f337de75cadeaee28c031c9c0b7b009188d30e1c67d08892940f`  
		Size: 6.0 MB (5964216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edde18f7388fa2007b95f1aa3ab0b23a05fc37bb0d43c2b581a50e17f89c2c49`  
		Last Modified: Tue, 12 Nov 2024 02:18:24 GMT  
		Size: 1.8 KB (1828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9e8a2edb1344326fa5cb2deda3da8c9f03e441794a344a725e2d2cd3d21f11`  
		Last Modified: Tue, 12 Nov 2024 02:18:24 GMT  
		Size: 697.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:d1d8c07ab3dc7de6e3db80e9b4f35d9271ba9894b2e46cfc3c681e14bf90516c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1065402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15624c9b09a5427c5e1a943395feb598f04bb45223c2dce6fbf7b5be8abcf0a`

```dockerfile
```

-	Layers:
	-	`sha256:51096e0f3fef4161df922c1306ef3b383e7f5793a3083518be4c85b8d570131f`  
		Last Modified: Tue, 12 Nov 2024 02:18:23 GMT  
		Size: 1.0 MB (1045446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae6ea397ae092007ed59c7e1fcd445852994f27256f77fa20e6178988ba3ba8a`  
		Last Modified: Tue, 12 Nov 2024 02:18:23 GMT  
		Size: 20.0 KB (19956 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:b53e8fd4b10afde38be4d8a68d45cc07339719c6a1ddeb6048091ea49eaf9672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13702581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c170d5dde2f48342c087942e4d7f9b1941995e02b44b49defd72d0154eef76`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
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
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42543951434ad86416c7a8c0be29ac67595e8ac14f508b1240afbe83dffd507`  
		Last Modified: Tue, 12 Nov 2024 02:30:14 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad8c6af06d108b01ff71d6c749ac67ea69b4960d2ae9df15b01aaf8d4125fef`  
		Last Modified: Tue, 12 Nov 2024 02:30:14 GMT  
		Size: 11.0 KB (10964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09f3e72f08335a7430883d658ea085c666cdbcea93e6412d0e0cb197c3ad9b`  
		Last Modified: Tue, 12 Nov 2024 02:30:15 GMT  
		Size: 4.7 MB (4651990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4729354c95a3340d54acfeeff80f1cb4a76a395312667a741fbb175fe98add4e`  
		Last Modified: Tue, 12 Nov 2024 02:30:15 GMT  
		Size: 5.9 MB (5859375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ad2caa1d94bd6007c7de4122de1f392d3b9d61e094686febb10206cccbf61d`  
		Last Modified: Tue, 12 Nov 2024 02:30:15 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9764e26e29b2f3f20759751eabc011e21188260b69bae51b3324407b44aab11a`  
		Last Modified: Tue, 12 Nov 2024 02:30:16 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:8a2bf8939dea48d54ab7012ad76727d9c572d87af20717b7235914e973f1dd98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 KB (19855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38ec1ffb1a3eebcaa9100b122a8259170ca005741882b60db4c63cc29acfc96`

```dockerfile
```

-	Layers:
	-	`sha256:81dccc98cdf6eed0ea511af2301373bfe683c18b01215474f455c4632cdd7b6d`  
		Last Modified: Tue, 12 Nov 2024 02:30:14 GMT  
		Size: 19.9 KB (19855 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:142795ca9803ebffcd4c103aae10422b781e4bfac9de5ec76b2f7a318147fff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14381185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b6ea32313b2339c85108c1afca03c0ef93d943c65b67de1a46c4a79e592a62`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9c737ec1b35deb5c0e22bf4475ee18a2e023d4b4cd4a5249299536f6a37a6b`  
		Last Modified: Tue, 12 Nov 2024 02:33:15 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eda39ca2af7c4932d683ac6faaa4025363de707e9e2f1798ff5ab5744b57bd4`  
		Last Modified: Tue, 12 Nov 2024 02:33:14 GMT  
		Size: 11.4 KB (11354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc3310efece93421f24d59c6e91a9fc8fcc3e10490402449a281d99023a769f`  
		Last Modified: Tue, 12 Nov 2024 02:33:15 GMT  
		Size: 5.0 MB (4992041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ebefd0bf29a416273c31e56363b57fe1a6aad39fb7f163f662870f59e40ea8`  
		Last Modified: Tue, 12 Nov 2024 02:33:15 GMT  
		Size: 6.0 MB (6014735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c6b84cf6fe01c7550dbba6ff7134c934b8ef2d7a91710e1d68d1154811f8d1`  
		Last Modified: Tue, 12 Nov 2024 02:33:16 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189bf2641f0e1f37538fa11ad51ddcbe9717bc260118e9e96ebaaced54be7ab2`  
		Last Modified: Tue, 12 Nov 2024 02:33:16 GMT  
		Size: 697.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:5c01b7b867557ccc08bc4790d5e507fca00ab193777b5c480d88585104b1e81e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1065607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb3954922b6b362f71d3b1b0415188566bfbef538f586ea9423d06d6ec96bd8`

```dockerfile
```

-	Layers:
	-	`sha256:ba42a25a9561e6bc41752ae23f9816b355382c13bdd228b58b74324a91366d2c`  
		Last Modified: Tue, 12 Nov 2024 02:33:15 GMT  
		Size: 1.0 MB (1045502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:501129403a4599e7fee7f3d300ff4ac10f8289a8fb4c9cc23918020543eb83e7`  
		Last Modified: Tue, 12 Nov 2024 02:33:15 GMT  
		Size: 20.1 KB (20105 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:6ee7a03529bacfb25e561f73737e642dde9ea6ebc07f578963aa8144dbc2753a
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
$ docker pull eggdrop@sha256:d58182d4fd2dfe38317305c74ee30b8be0e52991e816c4e3ae067d7e0efaeb17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14368318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277fb4aa7baeffb69e6aacb80ae72caea16fd6a6ba5af257e6941016954728f5`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e5a7b569dd4e69ba5137350e899653a5069a9676dfecc0b11d1ece82bf84e2`  
		Last Modified: Tue, 12 Nov 2024 02:18:23 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb16bc7b4a18332cb57e9fa464d2a363626a06bf67415a744def82cf9f9f3c98`  
		Last Modified: Tue, 12 Nov 2024 02:18:23 GMT  
		Size: 10.8 KB (10829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520c184b55f5b30d05e1abfdd4f7231be69a6f2855f55a3aed2bdb8895f65157`  
		Last Modified: Tue, 12 Nov 2024 02:18:23 GMT  
		Size: 5.0 MB (4969738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bd752aab17f337de75cadeaee28c031c9c0b7b009188d30e1c67d08892940f`  
		Size: 6.0 MB (5964216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edde18f7388fa2007b95f1aa3ab0b23a05fc37bb0d43c2b581a50e17f89c2c49`  
		Last Modified: Tue, 12 Nov 2024 02:18:24 GMT  
		Size: 1.8 KB (1828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9e8a2edb1344326fa5cb2deda3da8c9f03e441794a344a725e2d2cd3d21f11`  
		Last Modified: Tue, 12 Nov 2024 02:18:24 GMT  
		Size: 697.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:d1d8c07ab3dc7de6e3db80e9b4f35d9271ba9894b2e46cfc3c681e14bf90516c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1065402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15624c9b09a5427c5e1a943395feb598f04bb45223c2dce6fbf7b5be8abcf0a`

```dockerfile
```

-	Layers:
	-	`sha256:51096e0f3fef4161df922c1306ef3b383e7f5793a3083518be4c85b8d570131f`  
		Last Modified: Tue, 12 Nov 2024 02:18:23 GMT  
		Size: 1.0 MB (1045446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae6ea397ae092007ed59c7e1fcd445852994f27256f77fa20e6178988ba3ba8a`  
		Last Modified: Tue, 12 Nov 2024 02:18:23 GMT  
		Size: 20.0 KB (19956 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:b53e8fd4b10afde38be4d8a68d45cc07339719c6a1ddeb6048091ea49eaf9672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13702581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c170d5dde2f48342c087942e4d7f9b1941995e02b44b49defd72d0154eef76`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
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
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42543951434ad86416c7a8c0be29ac67595e8ac14f508b1240afbe83dffd507`  
		Last Modified: Tue, 12 Nov 2024 02:30:14 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad8c6af06d108b01ff71d6c749ac67ea69b4960d2ae9df15b01aaf8d4125fef`  
		Last Modified: Tue, 12 Nov 2024 02:30:14 GMT  
		Size: 11.0 KB (10964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09f3e72f08335a7430883d658ea085c666cdbcea93e6412d0e0cb197c3ad9b`  
		Last Modified: Tue, 12 Nov 2024 02:30:15 GMT  
		Size: 4.7 MB (4651990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4729354c95a3340d54acfeeff80f1cb4a76a395312667a741fbb175fe98add4e`  
		Last Modified: Tue, 12 Nov 2024 02:30:15 GMT  
		Size: 5.9 MB (5859375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ad2caa1d94bd6007c7de4122de1f392d3b9d61e094686febb10206cccbf61d`  
		Last Modified: Tue, 12 Nov 2024 02:30:15 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9764e26e29b2f3f20759751eabc011e21188260b69bae51b3324407b44aab11a`  
		Last Modified: Tue, 12 Nov 2024 02:30:16 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:8a2bf8939dea48d54ab7012ad76727d9c572d87af20717b7235914e973f1dd98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 KB (19855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38ec1ffb1a3eebcaa9100b122a8259170ca005741882b60db4c63cc29acfc96`

```dockerfile
```

-	Layers:
	-	`sha256:81dccc98cdf6eed0ea511af2301373bfe683c18b01215474f455c4632cdd7b6d`  
		Last Modified: Tue, 12 Nov 2024 02:30:14 GMT  
		Size: 19.9 KB (19855 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:142795ca9803ebffcd4c103aae10422b781e4bfac9de5ec76b2f7a318147fff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14381185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b6ea32313b2339c85108c1afca03c0ef93d943c65b67de1a46c4a79e592a62`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9c737ec1b35deb5c0e22bf4475ee18a2e023d4b4cd4a5249299536f6a37a6b`  
		Last Modified: Tue, 12 Nov 2024 02:33:15 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eda39ca2af7c4932d683ac6faaa4025363de707e9e2f1798ff5ab5744b57bd4`  
		Last Modified: Tue, 12 Nov 2024 02:33:14 GMT  
		Size: 11.4 KB (11354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc3310efece93421f24d59c6e91a9fc8fcc3e10490402449a281d99023a769f`  
		Last Modified: Tue, 12 Nov 2024 02:33:15 GMT  
		Size: 5.0 MB (4992041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ebefd0bf29a416273c31e56363b57fe1a6aad39fb7f163f662870f59e40ea8`  
		Last Modified: Tue, 12 Nov 2024 02:33:15 GMT  
		Size: 6.0 MB (6014735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c6b84cf6fe01c7550dbba6ff7134c934b8ef2d7a91710e1d68d1154811f8d1`  
		Last Modified: Tue, 12 Nov 2024 02:33:16 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189bf2641f0e1f37538fa11ad51ddcbe9717bc260118e9e96ebaaced54be7ab2`  
		Last Modified: Tue, 12 Nov 2024 02:33:16 GMT  
		Size: 697.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:5c01b7b867557ccc08bc4790d5e507fca00ab193777b5c480d88585104b1e81e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1065607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb3954922b6b362f71d3b1b0415188566bfbef538f586ea9423d06d6ec96bd8`

```dockerfile
```

-	Layers:
	-	`sha256:ba42a25a9561e6bc41752ae23f9816b355382c13bdd228b58b74324a91366d2c`  
		Last Modified: Tue, 12 Nov 2024 02:33:15 GMT  
		Size: 1.0 MB (1045502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:501129403a4599e7fee7f3d300ff4ac10f8289a8fb4c9cc23918020543eb83e7`  
		Last Modified: Tue, 12 Nov 2024 02:33:15 GMT  
		Size: 20.1 KB (20105 bytes)  
		MIME: application/vnd.in-toto+json
