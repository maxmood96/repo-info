## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:b2669d5762331fc52bcbb9a8e34d15d82ea638d666ed947c0adddc0a701f76bc
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
$ docker pull eggdrop@sha256:65cc22a60f99216392fb7444c6f683b45b1ccfaac36f45f19701cb26bea488bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16113894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b275de5dfb14c1a9b3b251ad6f5cbe8f430f67082458240c5579c9a391aa66`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:48:56 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sat, 27 Jan 2024 03:48:56 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Sat, 27 Jan 2024 03:48:58 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Sat, 27 Jan 2024 03:48:58 GMT
ENV EGGDROP_SHA256=a155625d2ac3a0673e69c9d0149293910583c1623cd1f90f38ad2bcba7b2b766
# Sat, 27 Jan 2024 03:48:58 GMT
ENV EGGDROP_COMMIT=322bddbd102d58cdb00864a3a335b086beaf042c
# Sat, 27 Jan 2024 03:50:43 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Sat, 27 Jan 2024 03:50:43 GMT
ENV NICK=
# Sat, 27 Jan 2024 03:50:43 GMT
ENV SERVER=
# Sat, 27 Jan 2024 03:50:44 GMT
ENV LISTEN=3333
# Sat, 27 Jan 2024 03:50:44 GMT
ENV USERFILE=eggdrop.user
# Sat, 27 Jan 2024 03:50:44 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 27 Jan 2024 03:50:44 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 27 Jan 2024 03:50:44 GMT
EXPOSE 3333
# Sat, 27 Jan 2024 03:50:44 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Sat, 27 Jan 2024 03:50:44 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in ./scripts/ 
# Sat, 27 Jan 2024 03:50:44 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 27 Jan 2024 03:50:44 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f5d2dade0d7e6a20a16b8a5cdcc1c302ea4d4f28f6bbc8cc8d6dca0004d7bf`  
		Last Modified: Sat, 27 Jan 2024 03:54:49 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba8624f02b83c7a3f5af243614e34dbcd6a9e76e8403e6cf5bcfe5ec0d56c74`  
		Last Modified: Sat, 27 Jan 2024 03:54:49 GMT  
		Size: 1.2 MB (1235875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1e73f39f98537af81579408d6cf792f89dee69387db3a016a358a13e73a83f`  
		Last Modified: Sat, 27 Jan 2024 03:54:51 GMT  
		Size: 11.6 MB (11615448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279119fd0575711d2018a46804fff96bc5b36f7d8cbd9f9cf8f66880aad2e273`  
		Last Modified: Sat, 27 Jan 2024 03:54:49 GMT  
		Size: 2.0 KB (1953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038850e52b1ea1a6ec38e9eab8b4b34b13826863bd64d72c0aba8793929735b3`  
		Last Modified: Sat, 27 Jan 2024 03:54:49 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
