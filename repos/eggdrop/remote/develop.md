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
