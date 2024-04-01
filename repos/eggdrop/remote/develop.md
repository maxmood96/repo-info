## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:2bd519dc7301eef1bda0f0e250c7ff5f11dd10afd48acbe26ea7348ba58e0154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:d3bf47606c9fb02fe7c32997b1c93d6cfb04b04057c0c3a957439e8949766587
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16095231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85193ba96e72cff112ca0e132f55e78289189987ae101f4cfb087d04295df91a`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 01 Apr 2024 17:53:55 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Mon, 01 Apr 2024 17:53:55 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Mon, 01 Apr 2024 17:53:57 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Mon, 01 Apr 2024 17:53:57 GMT
ENV EGGDROP_SHA256=a46bf0e77ed2af907fe6e15b77bddf0c55706258070a05c92810e0bd40a1fe3b
# Mon, 01 Apr 2024 17:53:57 GMT
ENV EGGDROP_COMMIT=4703f71067437c361ca8d5c8c4a09d41561a7a20
# Mon, 01 Apr 2024 17:56:24 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Mon, 01 Apr 2024 17:56:24 GMT
ENV NICK=
# Mon, 01 Apr 2024 17:56:24 GMT
ENV SERVER=
# Mon, 01 Apr 2024 17:56:24 GMT
ENV LISTEN=3333
# Mon, 01 Apr 2024 17:56:24 GMT
ENV USERFILE=eggdrop.user
# Mon, 01 Apr 2024 17:56:25 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 01 Apr 2024 17:56:25 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 01 Apr 2024 17:56:25 GMT
EXPOSE 3333
# Mon, 01 Apr 2024 17:56:25 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Mon, 01 Apr 2024 17:56:25 GMT
COPY file:61da6bdf6e84c41c8486cddfad6cc1d25ced9bbeaa056bab87034428f2134436 in ./scripts/ 
# Mon, 01 Apr 2024 17:56:25 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 01 Apr 2024 17:56:25 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc8a36fd2fdee81c9926e705a41740df18a69d30586b6bfe4c840cad14b851a`  
		Last Modified: Mon, 01 Apr 2024 17:56:42 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687be1d96a29a2b29dd5902cb3870e479175969b487a68c5a8251ec369f76426`  
		Last Modified: Mon, 01 Apr 2024 17:56:42 GMT  
		Size: 1.1 MB (1093055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14db582761e32b97e1892ffe514d06d1688a9489460315a330540429e180b4ab`  
		Last Modified: Mon, 01 Apr 2024 17:56:43 GMT  
		Size: 11.6 MB (11589088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e632c154f9ab04f67d438a081878d472929ba6343314831ce4b51678da241b94`  
		Last Modified: Mon, 01 Apr 2024 17:56:42 GMT  
		Size: 2.0 KB (1954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f62eed83eb06910486ca6d6a74d3a516a38dca697b3d64099693f1b1c75058`  
		Last Modified: Mon, 01 Apr 2024 17:56:42 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:f62beefbca486cb9c6e7cb78836855e6fc188606d814686f3f3eea0b468e6ce7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15738594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf0a379b126de020a4aca5c0c9f385e4c29d9f9f0ef86b35023de3b0c797c5e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Mon, 01 Apr 2024 22:00:14 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Mon, 01 Apr 2024 22:00:14 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Mon, 01 Apr 2024 22:00:16 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Mon, 01 Apr 2024 22:00:16 GMT
ENV EGGDROP_SHA256=a46bf0e77ed2af907fe6e15b77bddf0c55706258070a05c92810e0bd40a1fe3b
# Mon, 01 Apr 2024 22:00:16 GMT
ENV EGGDROP_COMMIT=4703f71067437c361ca8d5c8c4a09d41561a7a20
# Mon, 01 Apr 2024 22:02:55 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Mon, 01 Apr 2024 22:02:55 GMT
ENV NICK=
# Mon, 01 Apr 2024 22:02:55 GMT
ENV SERVER=
# Mon, 01 Apr 2024 22:02:55 GMT
ENV LISTEN=3333
# Mon, 01 Apr 2024 22:02:55 GMT
ENV USERFILE=eggdrop.user
# Mon, 01 Apr 2024 22:02:55 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 01 Apr 2024 22:02:55 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 01 Apr 2024 22:02:56 GMT
EXPOSE 3333
# Mon, 01 Apr 2024 22:02:56 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Mon, 01 Apr 2024 22:02:56 GMT
COPY file:61da6bdf6e84c41c8486cddfad6cc1d25ced9bbeaa056bab87034428f2134436 in ./scripts/ 
# Mon, 01 Apr 2024 22:02:56 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 01 Apr 2024 22:02:56 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5061c19a985574b0e9db873e9afa9fbe251b480ce88f32448e0449e099a8e3f`  
		Last Modified: Mon, 01 Apr 2024 22:03:12 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb9be1abe116bc33b2e5fca4adab8a04133b57c38fc6f2c029607b927006a7d`  
		Last Modified: Mon, 01 Apr 2024 22:03:12 GMT  
		Size: 1.1 MB (1106312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c548ac214504edfe175ba36c8de78b9ea08af655e802215f8830bd0425182b5e`  
		Last Modified: Mon, 01 Apr 2024 22:03:14 GMT  
		Size: 11.5 MB (11462529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734c7850ce123a4313ebc3762c549f511a1f244c03e02b5cd0fc327384855d63`  
		Last Modified: Mon, 01 Apr 2024 22:03:11 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39d809a13762e11706e5fca2cb165b60f6501340bbba44e04af809693ad9d3b`  
		Last Modified: Mon, 01 Apr 2024 22:03:12 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:e5108c49b6ad5de2f90b6e4a0f91ac1acfcc1b9a3ba4d0f10a6d143b0c71f53d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16218902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab0459b69ae5de28ddb6f95c206d82fde68860df20509fa4affef53a8e3e4c1`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 01 Apr 2024 18:09:16 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Mon, 01 Apr 2024 18:09:16 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Mon, 01 Apr 2024 18:09:17 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Mon, 01 Apr 2024 18:09:17 GMT
ENV EGGDROP_SHA256=a46bf0e77ed2af907fe6e15b77bddf0c55706258070a05c92810e0bd40a1fe3b
# Mon, 01 Apr 2024 18:09:17 GMT
ENV EGGDROP_COMMIT=4703f71067437c361ca8d5c8c4a09d41561a7a20
# Mon, 01 Apr 2024 18:11:14 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Mon, 01 Apr 2024 18:11:15 GMT
ENV NICK=
# Mon, 01 Apr 2024 18:11:15 GMT
ENV SERVER=
# Mon, 01 Apr 2024 18:11:15 GMT
ENV LISTEN=3333
# Mon, 01 Apr 2024 18:11:15 GMT
ENV USERFILE=eggdrop.user
# Mon, 01 Apr 2024 18:11:15 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 01 Apr 2024 18:11:15 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 01 Apr 2024 18:11:15 GMT
EXPOSE 3333
# Mon, 01 Apr 2024 18:11:15 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Mon, 01 Apr 2024 18:11:15 GMT
COPY file:61da6bdf6e84c41c8486cddfad6cc1d25ced9bbeaa056bab87034428f2134436 in ./scripts/ 
# Mon, 01 Apr 2024 18:11:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 01 Apr 2024 18:11:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0324dc57ab492c18add828859dfe3b783b32671cab482a484a29d4948ce56e08`  
		Last Modified: Mon, 01 Apr 2024 18:11:31 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35ebfbd2ee49804d05022386da852ade6ef72ef87853762a12a59565e07fb79`  
		Last Modified: Mon, 01 Apr 2024 18:11:31 GMT  
		Size: 1.2 MB (1188152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5935cf17256ca211b6e5413117b6b0739376ad97e9689919ff49480cfc4cebe2`  
		Last Modified: Mon, 01 Apr 2024 18:11:33 GMT  
		Size: 11.7 MB (11678686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f44d4fe85a03bee8781b17511c95cd3606888a995df7f89633aef2c6a65881`  
		Last Modified: Mon, 01 Apr 2024 18:11:31 GMT  
		Size: 2.0 KB (1951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d408ab23b63e971991a9852e06d4b55c0ef0674b8df740d1f98413f9365ea3`  
		Last Modified: Mon, 01 Apr 2024 18:11:31 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
