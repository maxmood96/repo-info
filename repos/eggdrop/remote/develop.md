## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:121554e168ac0bd8b7ddcb6419401ce75024dcee2ad35d9f82354b23253848c2
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
$ docker pull eggdrop@sha256:e35a60699d0a9d8fd305a5ecc44b2f9a3673c2a3d5923116834b79437d0e0c8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16410625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bac9601bf3a0ea9df0d8cb4c39aab7d4f819ea81ccf60895582c6e9180da064`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:45:15 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb209af1764bcbfa0c48f2a65dde47657f4c675b7e5057a08e0aa5848d873a69`  
		Last Modified: Fri, 06 Sep 2024 23:17:42 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630d7778d2e0f9a12663737b02fd1fb5fb0a0a7ae5e5d345a88026b9d744c2d9`  
		Last Modified: Fri, 06 Sep 2024 23:17:42 GMT  
		Size: 1.1 MB (1115387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d842f35428ec42446199c23e29c853f224985bed198b70aebc2d43d30bfea77e`  
		Last Modified: Fri, 06 Sep 2024 23:17:43 GMT  
		Size: 11.7 MB (11667370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fc40472f1c1aba83f44cd0cb87bfb11fcef0ebee915a583ea9ec78cbe89e44`  
		Last Modified: Fri, 06 Sep 2024 23:17:42 GMT  
		Size: 1.9 KB (1943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a761a8fc913603544268c090bf12a12aba2e1fe908e680bd84121078493a44`  
		Last Modified: Fri, 06 Sep 2024 23:17:43 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:d580133230e25693533e6667d990b3cb77d3d04b8dc757e2e80d30b0b5e6f8b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 KB (153176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6970303d5fa6fc06468129aed534dca0d9cf4f28735757fb534a225b052622e7`

```dockerfile
```

-	Layers:
	-	`sha256:1f633f4305ad71fbcab58f89a16a9a558b51ebc891f7dd5dd906beecf88601a6`  
		Last Modified: Fri, 06 Sep 2024 23:17:43 GMT  
		Size: 136.0 KB (136039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e817be8d5d55f1b25595aeebae172ea3d367c5bdb3a7eb830a822dcc7c55153`  
		Last Modified: Fri, 06 Sep 2024 23:17:43 GMT  
		Size: 17.1 KB (17137 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:703af55a65bd4090edfecfb2d0cd4a90c47e42360570d125268893d7612b1c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15981594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99694726327382853c402217a5725aa7c5a4a4391bf81b80fdc292c716bf7b45`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:45:15 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
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
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751b1216441bfe0b44e07cc74ccf88bc4716b7c5b2e425d66523bfcd5b91249c`  
		Last Modified: Sat, 07 Sep 2024 02:21:55 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270187252bf6c021f79e98c1cea95c1e2acb55bbeda016cc30f19fe46c38b4e8`  
		Last Modified: Sat, 07 Sep 2024 02:21:55 GMT  
		Size: 1.1 MB (1129549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a2ef9812cfa83698770b09cab785fd6ee7827f9c213dc16c035d32247b953b`  
		Last Modified: Sat, 07 Sep 2024 02:21:55 GMT  
		Size: 11.5 MB (11481468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c47aac3530ee7435879ebf62210c7ef99f4afe311e1ed834867ba0e454b2fcc`  
		Last Modified: Sat, 07 Sep 2024 02:21:55 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b74195e288772c74b542098f217f1c239a20e559304140b3e7bc7f7790d1615`  
		Last Modified: Sat, 07 Sep 2024 02:21:56 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:43927f2a4d05640721266dd173f345532f11c5d72bd49a966ace6d14981bf9be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (16990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381b7294cbad17e73a33dfb1e3c1a30b92941a79ae93309d28b3f9e3425daefc`

```dockerfile
```

-	Layers:
	-	`sha256:48ce81bb265867e6497566f85dadbdc7047e857f5c467e0dd763ee989ea10594`  
		Last Modified: Sat, 07 Sep 2024 02:21:55 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:10404346ebe84c0a3e1284c1520f9f5bfb028da95b652ff475320321c950b180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19691828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04faecc878c513320b7b2dd111aa0936379a3a9a7e47ac2531449f77dc7c3ce8`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
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
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0202e46c7eaaa3458319ea625e1b1f0f395e4f26ea1c18d8499037c9a6b52b8a`  
		Last Modified: Fri, 06 Sep 2024 21:53:05 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d90021f9b06c4f6889543781e83377c49ee76d2e58106decd025eabaa9e181`  
		Last Modified: Fri, 06 Sep 2024 21:53:06 GMT  
		Size: 3.9 MB (3899862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c66e69595c791ff1bb0e6b981a48f8f1c24365372f8b7f558ae7fbb627fcb5`  
		Last Modified: Fri, 06 Sep 2024 21:53:07 GMT  
		Size: 11.7 MB (11700962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d12e9f784ce42ad980c85295ea3eb3144c5464de595c044fb9fed4d83b4eb72`  
		Last Modified: Fri, 06 Sep 2024 21:53:06 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335e6facd6c5699da79c670cac9dfc3e5c487f6f775d9991e956a770b2c46c72`  
		Last Modified: Fri, 06 Sep 2024 21:53:06 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:61c1e9cf583c20b4ac97351ef7eb2cda57eef37855fc7e606c2339ffcd61d7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 KB (153460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04293dbf50e139e1331444b5ef75e5cec396b4754eb80e9b3e3e1c68ea254ac`

```dockerfile
```

-	Layers:
	-	`sha256:afcb3c8b3e4fcc113af26ffa6e6746ca6d2af83ceb11d2ce812d3431e3217135`  
		Last Modified: Fri, 06 Sep 2024 21:53:05 GMT  
		Size: 136.1 KB (136059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d2054ca69dda263c3d356f0a25380012fd5c4f9f87129a0846b6a509e5d8491`  
		Last Modified: Fri, 06 Sep 2024 21:53:05 GMT  
		Size: 17.4 KB (17401 bytes)  
		MIME: application/vnd.in-toto+json
