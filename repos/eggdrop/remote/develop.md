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
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b24a36091226bb8c146bddc8fab67e5ef8c1531389d34ef378e12b2a3d5fe5`  
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
		Size: 136.2 KB (136165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:262bd4d83b8b9d33ea97bf81c5f473269ce5928a184636c1ac267dcb77e7dcfb`  
		Last Modified: Tue, 12 Nov 2024 02:29:12 GMT  
		Size: 17.4 KB (17448 bytes)  
		MIME: application/vnd.in-toto+json
