## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:d23b5417b34961010a3893691d517f023757fc949ecde98f3af6393e6c20f274
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
$ docker pull eggdrop@sha256:729927695d6b2733b5f38e504ec604d2c9c8f80172eddc8ccb192b225103224f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12702028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c9401764e0065d8945dc3388e63c29e65d8b689ba5e66e5216bb87244d889a7`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV EGGDROP_SHA256=34c09905c2e9df1e8ca4bae5bc395a8c60f4ca93123599788bae5164ebd8f8f5
# Sun, 05 Jan 2025 16:36:07 GMT
ENV EGGDROP_COMMIT=0f5599e1fafa97454dc7a8b147c6076638e95ba8
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b15aa9d6bb751bc2ece118d1ceeac1fd953ae91ce5115ffcdb0dcc56737a9a`  
		Last Modified: Tue, 07 Jan 2025 03:18:03 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76175a7efd4beb0a08f7c5063e39f1d5c80c933c9e7d5107b381732ce74d001`  
		Last Modified: Tue, 07 Jan 2025 03:18:03 GMT  
		Size: 1.1 MB (1115388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727fa829d75cb787449e0e3594665a300878adedfe696bfa08e71ed6a0ac8f50`  
		Last Modified: Tue, 07 Jan 2025 03:18:03 GMT  
		Size: 8.0 MB (7968570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7fbc78fac6b8fd4e84b93e1fa4c5c884efca69c43b42ea0b79bcbb0c3a8f0f`  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dbe94fac61f2cfba4aaeca506a96bf634db016fa2f575d15824422978e32ea`  
		Last Modified: Tue, 07 Jan 2025 03:18:04 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:807bbe9848a3195e9aea8fe4d0f8de4d85a59aadabd8f7a8e8a5462efa8bda86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 KB (153052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7665172d5d5443041b175bcdafef08c78c5473ff43e9853d4090c4a680393b6f`

```dockerfile
```

-	Layers:
	-	`sha256:5010838aef7880701b352f6ad3add65d197cdebc42c1c81bad39f597d4450568`  
		Size: 136.0 KB (135961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20056e31e28aea909b171c218ea154a9ee39e5ae364a1bfa1c130d6bad19a12c`  
		Size: 17.1 KB (17091 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:b7b6b09ebd2f02a2cd293bddf0bbc8debd665445d5b70128928525c6b4d21cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12307747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafc558c82cabfc6caa6ecd1a7c80ec47f29168063bc9e3bba8bbfbd46364659`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV EGGDROP_SHA256=34c09905c2e9df1e8ca4bae5bc395a8c60f4ca93123599788bae5164ebd8f8f5
# Sun, 05 Jan 2025 16:36:07 GMT
ENV EGGDROP_COMMIT=0f5599e1fafa97454dc7a8b147c6076638e95ba8
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
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
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87c49c56e3d5c9303824a8cad20f5b05da63b8c632ee40628c3929f67d96cac`  
		Last Modified: Tue, 07 Jan 2025 03:41:06 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff887413f70f9ad52edadcf99d87efb7034a0479a51ab3dbfce367e24df84f0`  
		Last Modified: Tue, 07 Jan 2025 03:41:07 GMT  
		Size: 1.1 MB (1129559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df10738378fc797ed8a92e24288f8705f31564312ebfd5ae09b1d7ab4dba8b16`  
		Last Modified: Tue, 07 Jan 2025 03:41:07 GMT  
		Size: 7.8 MB (7810172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d116c4f58f7dda53eb922ff7292f3786748682a17d0c924c893881f9498dc88d`  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7829735c271e7a6b3d77e05fc88df3b3192cea9230ccc12c38433cae1f5548a`  
		Last Modified: Tue, 07 Jan 2025 03:41:07 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:8b8b5931e6aa45504808ed42f3fa770e88bfa03b30cd1be92ccfe712e8ee28a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (16954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cddb7acee4888f793ae1577df1c8f14a6f85254f4786bc6d35217fecd70ae306`

```dockerfile
```

-	Layers:
	-	`sha256:5fa8568ba8b239621bf35ae9442bc99692e1f7eb94655f84ec6d4ecf62921509`  
		Last Modified: Tue, 07 Jan 2025 03:41:06 GMT  
		Size: 17.0 KB (16954 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:a3350406045f7d6b859918a7683d2d57ca06880b4849faba54e86806d549760e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13316342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3abac401f8439ce552a61ed6c1a9e17b701103a39db0cf2fa755d2a4e8bb573`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV EGGDROP_SHA256=34c09905c2e9df1e8ca4bae5bc395a8c60f4ca93123599788bae5164ebd8f8f5
# Sun, 05 Jan 2025 16:36:07 GMT
ENV EGGDROP_COMMIT=0f5599e1fafa97454dc7a8b147c6076638e95ba8
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
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
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adba3ad06ebd31a48135af820872fd883c103f9fd47fb46b953a0d826867c58`  
		Last Modified: Tue, 07 Jan 2025 04:03:52 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6504725a30a01dfb79c3839e72991ba0790ded436ec4b8b28f5b2a462d5297`  
		Last Modified: Tue, 07 Jan 2025 04:03:53 GMT  
		Size: 1.2 MB (1210975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300703333265e1956b3afca6b0dadc62a0cbcb6c0e5b689c5a72f152be0b8570`  
		Last Modified: Tue, 07 Jan 2025 04:03:53 GMT  
		Size: 8.0 MB (8014610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fad5d492ce46807009d3fc2d44ae9a1149700e436e2f9b5430ba0b1a04571c`  
		Last Modified: Tue, 07 Jan 2025 04:03:53 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45782f8ec381ea791c592888c258bb51bb0430b51cde85b19625728336aec985`  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:4376743a3b70242a30ec81364d7d96e5f86385150421a38e4dcfaf5ef2c6cd4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 KB (153169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9b2411c3aa324a99ac14bbad73487660a4f7e0dd6113c8a318a88e02347f4d`

```dockerfile
```

-	Layers:
	-	`sha256:cef8090bb5cb0d18ee43925e291fd53947605cdc575a6657f2a35fceee074ff7`  
		Last Modified: Tue, 07 Jan 2025 04:03:53 GMT  
		Size: 136.0 KB (135981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:040e8e3fdc8363e8ef0704ab8249897dd37cd31aba4b3aa405e4d38300e939eb`  
		Last Modified: Tue, 07 Jan 2025 04:03:52 GMT  
		Size: 17.2 KB (17188 bytes)  
		MIME: application/vnd.in-toto+json
