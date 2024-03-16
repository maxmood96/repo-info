## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:7488d15ca8358f8bc8819a4ad7b4af0a64e5b2bd3985ca0f7165a1639113ebd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:66c6be9a455349691be1ab23d668b6d728d0c1e6bd652fa300131236a13a37c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16146516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9d90d91b3bcbb49713c93e257fa11752bc90f1134a59b65053125a319eaae3`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:42:34 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sat, 27 Jan 2024 03:42:35 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Sat, 27 Jan 2024 03:42:36 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Sat, 27 Jan 2024 03:42:36 GMT
ENV EGGDROP_SHA256=a155625d2ac3a0673e69c9d0149293910583c1623cd1f90f38ad2bcba7b2b766
# Sat, 27 Jan 2024 03:42:36 GMT
ENV EGGDROP_COMMIT=322bddbd102d58cdb00864a3a335b086beaf042c
# Sat, 27 Jan 2024 03:44:44 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Sat, 27 Jan 2024 03:44:44 GMT
ENV NICK=
# Sat, 27 Jan 2024 03:44:44 GMT
ENV SERVER=
# Sat, 27 Jan 2024 03:44:44 GMT
ENV LISTEN=3333
# Sat, 27 Jan 2024 03:44:44 GMT
ENV USERFILE=eggdrop.user
# Sat, 27 Jan 2024 03:44:45 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 27 Jan 2024 03:44:45 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 27 Jan 2024 03:44:45 GMT
EXPOSE 3333
# Sat, 27 Jan 2024 03:44:45 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Sat, 27 Jan 2024 03:44:45 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in ./scripts/ 
# Sat, 27 Jan 2024 03:44:45 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 27 Jan 2024 03:44:45 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ddd64c2d8057eda10c7166d426014e74e8738556292bf935de71ee4b63eabef`  
		Last Modified: Sat, 27 Jan 2024 03:49:12 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91949613a0bda4027dc527d36e254b311df22345b7afef2f447664634d14d6f`  
		Last Modified: Sat, 27 Jan 2024 03:49:12 GMT  
		Size: 1.2 MB (1208567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4216c8f4eb465269be81bdb268d161367a0f72e2f3951acdce7d1e60883146f`  
		Last Modified: Sat, 27 Jan 2024 03:49:14 GMT  
		Size: 11.6 MB (11554262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b3f2968a242962289677e56c14d487c77628da0fe81a370fb105d2a6dfe5fb`  
		Last Modified: Sat, 27 Jan 2024 03:49:12 GMT  
		Size: 1.9 KB (1950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c9791e70e0ed31bce65da218b8e05b2787abbc81313212032580b1cdf69393`  
		Last Modified: Sat, 27 Jan 2024 03:49:12 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:d206a27b4ef580b531a88fd3592278490926e86d05156509d99213d701010625
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15746602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4449e8b4e016503983749d263693857edf4916511d115a0a65ab09416fff4b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:23 GMT
ADD file:ef699a4b52d87def9be5a058091005e5e3f0bb9fb7bf5c9fe3053ba85d79d7af in / 
# Fri, 26 Jan 2024 23:49:23 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 01:13:56 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sat, 16 Mar 2024 01:13:58 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Sat, 16 Mar 2024 01:14:01 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Sat, 16 Mar 2024 01:14:01 GMT
ENV EGGDROP_SHA256=a155625d2ac3a0673e69c9d0149293910583c1623cd1f90f38ad2bcba7b2b766
# Sat, 16 Mar 2024 01:14:02 GMT
ENV EGGDROP_COMMIT=322bddbd102d58cdb00864a3a335b086beaf042c
# Sat, 16 Mar 2024 01:17:33 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Sat, 16 Mar 2024 01:17:33 GMT
ENV NICK=
# Sat, 16 Mar 2024 01:17:33 GMT
ENV SERVER=
# Sat, 16 Mar 2024 01:17:33 GMT
ENV LISTEN=3333
# Sat, 16 Mar 2024 01:17:34 GMT
ENV USERFILE=eggdrop.user
# Sat, 16 Mar 2024 01:17:34 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 16 Mar 2024 01:17:34 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 16 Mar 2024 01:17:34 GMT
EXPOSE 3333
# Sat, 16 Mar 2024 01:17:35 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Sat, 16 Mar 2024 01:17:35 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in ./scripts/ 
# Sat, 16 Mar 2024 01:17:35 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 16 Mar 2024 01:17:36 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:dded572f39df01b407585bbbda3ae89a2d14042e68184c8b3f6af6ac7fe5b86b`  
		Last Modified: Fri, 26 Jan 2024 23:50:01 GMT  
		Size: 3.1 MB (3113120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb82302311f51ac466878a742622f0992f0cb2e8734d1e5857294a462e4c82ff`  
		Last Modified: Sat, 16 Mar 2024 01:24:06 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed3d696d75625936ab9b40d2810cf75477e315eaca22ce53203d1d4c3a349df`  
		Last Modified: Sat, 16 Mar 2024 01:24:06 GMT  
		Size: 1.2 MB (1190273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892b372f1d1f865f5375fbaec12fbb261bb9617cc75f962666c379b149291df4`  
		Last Modified: Sat, 16 Mar 2024 01:24:08 GMT  
		Size: 11.4 MB (11438917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b34938e2ca15c56cc5e2f9cb44eda473eda38d7d204464939500b029fa55bd`  
		Last Modified: Sat, 16 Mar 2024 01:24:06 GMT  
		Size: 2.0 KB (1955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f368ca5d92dee70dac9f2ab26bf6afe912e953c6f9ffaa77eeca31a83d18d7`  
		Last Modified: Sat, 16 Mar 2024 01:24:06 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:05567ff86ba594d768140d5320428f0f8fc00c3d92a52608c055bd298bd2dc71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16114146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5f9c72c6d4f86dd075f1bf8ee20b806900f8a7c8b597f8090c77f5902dc240`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:06:23 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sat, 16 Mar 2024 03:06:24 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Sat, 16 Mar 2024 03:06:25 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Sat, 16 Mar 2024 03:06:25 GMT
ENV EGGDROP_SHA256=a155625d2ac3a0673e69c9d0149293910583c1623cd1f90f38ad2bcba7b2b766
# Sat, 16 Mar 2024 03:06:25 GMT
ENV EGGDROP_COMMIT=322bddbd102d58cdb00864a3a335b086beaf042c
# Sat, 16 Mar 2024 03:08:10 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Sat, 16 Mar 2024 03:08:10 GMT
ENV NICK=
# Sat, 16 Mar 2024 03:08:10 GMT
ENV SERVER=
# Sat, 16 Mar 2024 03:08:10 GMT
ENV LISTEN=3333
# Sat, 16 Mar 2024 03:08:10 GMT
ENV USERFILE=eggdrop.user
# Sat, 16 Mar 2024 03:08:10 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 16 Mar 2024 03:08:10 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 16 Mar 2024 03:08:10 GMT
EXPOSE 3333
# Sat, 16 Mar 2024 03:08:11 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Sat, 16 Mar 2024 03:08:11 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in ./scripts/ 
# Sat, 16 Mar 2024 03:08:11 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 16 Mar 2024 03:08:11 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2f109b5bff81141d645bd97e487b85fe671d1b24d4663220f4944044b7e51f`  
		Last Modified: Sat, 16 Mar 2024 03:12:46 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd29fff9dcc57dba233e4c096ba71ee6b70b8d87dfc514bd36013c8b3d01dbe2`  
		Last Modified: Sat, 16 Mar 2024 03:12:47 GMT  
		Size: 1.2 MB (1235894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ce6674a09b10812bc8b6e54660f43593fe6aa71165bfd759249fbe4733ec6e`  
		Last Modified: Sat, 16 Mar 2024 03:12:48 GMT  
		Size: 11.6 MB (11615679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9baea195a5ed6903299af1e4a70400be5c98a418c59ce15c813d951828bc40`  
		Last Modified: Sat, 16 Mar 2024 03:12:46 GMT  
		Size: 2.0 KB (1953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2e302d4b82c247212a123c007bf12327f6cc3d233bbc31575b77ceb1704eb1`  
		Last Modified: Sat, 16 Mar 2024 03:12:46 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
