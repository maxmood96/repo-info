## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:44a65e45c0d40d035dbf6969af35288041e7d7dd9466eb01157da9c28c105f95
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
$ docker pull eggdrop@sha256:dd6cdbee6ddab605cfaafddfc743e5276b8eb5fce4008f7c654d885ed0c7fbc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17003534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1462551b94c6a0bc7e27ad9530c4d1be8c67de6c66a993bd3615ccc9b661241e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:45:15 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c587327945fb426b39e951102adf9e314b71a3d364477beeb2256362093e8de0`  
		Last Modified: Sat, 07 Sep 2024 04:53:27 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34205a0f447439bb8964a44e4990e1b5567410f5215329678b781f3644d06139`  
		Last Modified: Sat, 07 Sep 2024 04:53:27 GMT  
		Size: 1.2 MB (1210967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1692ca7db17b6f82a75ae14d31abb253d272ba5e1447c60e0530016d3b8122f1`  
		Last Modified: Sat, 07 Sep 2024 04:53:27 GMT  
		Size: 11.7 MB (11700856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262d5356b35cf1c612e011143b141af90ebcedc484a93e651104657491057bf3`  
		Last Modified: Sat, 07 Sep 2024 04:53:27 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655747fa033d04956cd9383bc497a39d9856181a9cbb0259fa185072bb9a2c38`  
		Last Modified: Sat, 07 Sep 2024 04:53:27 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:52846a482c8e98656e3724790bf5fbbb6007708474a3c4e9912b91e5c03311ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 KB (153459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc37850e4bff845982861090dddda7620cd74715073a2fbc7bdbda002a2fbe10`

```dockerfile
```

-	Layers:
	-	`sha256:cd7d67c2e23be826621f05061d4891d084fe66c70feed7702440c5c87e038502`  
		Last Modified: Sat, 07 Sep 2024 04:53:27 GMT  
		Size: 136.1 KB (136059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bba0a86d3b193ef6bd61a79924cc3178e01e5032a18162d212678c9198fe1d22`  
		Last Modified: Sat, 07 Sep 2024 04:53:27 GMT  
		Size: 17.4 KB (17400 bytes)  
		MIME: application/vnd.in-toto+json
