## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:7c52c6349ac565ae223d149ecf9c08a72480ec03ac1a240cef4974e9a6190606
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
$ docker pull eggdrop@sha256:1de45d62f49830dd834a295f02c5c529aed23f36b2438fd4cf074a364167b66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11243580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68fda12c9f7b5373168423949b8dc695c449e581fcba731be5e7c6bfcc4716a1`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:12 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Mon, 22 Jun 2026 19:46:12 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Mon, 22 Jun 2026 19:46:13 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl tcl9 tcl9-dev # buildkit
# Mon, 22 Jun 2026 19:46:13 GMT
ENV EGGDROP_SHA256=e42668f102c1446901b066d13fe0bf39622afca8d723f356ac2390d5faaf6e5e
# Mon, 22 Jun 2026 19:46:13 GMT
ENV EGGDROP_COMMIT=541e8ac17e549a40e177b5eea54e4abf24629a33
# Mon, 22 Jun 2026 19:46:28 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Mon, 22 Jun 2026 19:46:28 GMT
ENV NICK=
# Mon, 22 Jun 2026 19:46:28 GMT
ENV SERVER=
# Mon, 22 Jun 2026 19:46:28 GMT
ENV LISTEN=3333
# Mon, 22 Jun 2026 19:46:28 GMT
ENV USERFILE=eggdrop.user
# Mon, 22 Jun 2026 19:46:28 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 22 Jun 2026 19:46:28 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 22 Jun 2026 19:46:28 GMT
EXPOSE map[3333/tcp:{}]
# Mon, 22 Jun 2026 19:46:28 GMT
COPY entrypoint.sh ./ # buildkit
# Mon, 22 Jun 2026 19:46:28 GMT
COPY docker.tcl ./scripts/ # buildkit
# Mon, 22 Jun 2026 19:46:28 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:28 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b070ceba434db40bc35d163ebed5d3dcb00e5f09ca2d0b861e1f769a7dd97f`  
		Last Modified: Mon, 22 Jun 2026 19:46:33 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12273298b9efe5cb4f1fe848b5cfc223b56cd96f9119be22952656610723116`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 4.7 MB (4749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdaca1884234da244c3aba2cac59550782540a3edd0fa2fd8fe1c43525f6c24a`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 2.6 MB (2645238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe920fd265aac2f04f6b0ece594238dd6c0482584faca802d16bd7eb8b2a6b3e`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 2.0 KB (1958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a65fbc9fd4daafddf4083d0fe39076b5fe351ef111513d59b780f53dfbcae0`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:7998a016b1449296d0d297ee3a0e92c84693beac8b6d452171ba20dde6b70ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **754.0 KB (754019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13542526a024fcf91c280e24bb1aa690b31e25b5e74545a49cc372264785000b`

```dockerfile
```

-	Layers:
	-	`sha256:948b6d1b77c1ad7f9b082cd8171fc225e1fcb652fb81365907120c39e912d293`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 738.2 KB (738227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cbb429c5014ca649e07d5faca424f32694a4c7671a9f0b0c69dccfad7b389f8`  
		Last Modified: Mon, 22 Jun 2026 19:46:33 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:3d199d50c51cea7cd1de7c4805aa28a084105e7b03faae4d69e5bf4e523ccb5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10927156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d80cbac22d46a69f551b2c1ba1e7130ffef17e4c848765f193d67bbab481dd7`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:45:43 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Mon, 22 Jun 2026 19:45:43 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Mon, 22 Jun 2026 19:45:45 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl tcl9 tcl9-dev # buildkit
# Mon, 22 Jun 2026 19:45:45 GMT
ENV EGGDROP_SHA256=e42668f102c1446901b066d13fe0bf39622afca8d723f356ac2390d5faaf6e5e
# Mon, 22 Jun 2026 19:45:45 GMT
ENV EGGDROP_COMMIT=541e8ac17e549a40e177b5eea54e4abf24629a33
# Mon, 22 Jun 2026 19:46:06 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Mon, 22 Jun 2026 19:46:06 GMT
ENV NICK=
# Mon, 22 Jun 2026 19:46:06 GMT
ENV SERVER=
# Mon, 22 Jun 2026 19:46:06 GMT
ENV LISTEN=3333
# Mon, 22 Jun 2026 19:46:06 GMT
ENV USERFILE=eggdrop.user
# Mon, 22 Jun 2026 19:46:06 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 22 Jun 2026 19:46:06 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 22 Jun 2026 19:46:06 GMT
EXPOSE map[3333/tcp:{}]
# Mon, 22 Jun 2026 19:46:06 GMT
COPY entrypoint.sh ./ # buildkit
# Mon, 22 Jun 2026 19:46:06 GMT
COPY docker.tcl ./scripts/ # buildkit
# Mon, 22 Jun 2026 19:46:06 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:06 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ff6befc072d7df2a002766997ea94b67e3af6d5653c9017c39b0e8ca4a7881`  
		Last Modified: Mon, 22 Jun 2026 19:46:10 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e60d8115e3b933ff6aed3375deb0ccfdc96bc8a48dfd9ed25b326a8cb6af65`  
		Last Modified: Mon, 22 Jun 2026 19:46:10 GMT  
		Size: 4.7 MB (4708193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd43a8e8431cf4313e1dfbb347f0a0f575d3f56078bb146f40ca4bb6de4d28a1`  
		Last Modified: Mon, 22 Jun 2026 19:46:10 GMT  
		Size: 2.7 MB (2662294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255c34a048e4b6795233ec626d75ae884e9712829cf66aeb554297ff93522548`  
		Last Modified: Mon, 22 Jun 2026 19:46:10 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c36ed67821b0ab746ef4c066fc2d0348d2357fc6ad1d30dd710904b7d1b9254`  
		Last Modified: Mon, 22 Jun 2026 19:46:11 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:e07f8d1173f6558596c020af2edc701b7517d587b87698267abfab3ed6e8a7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 KB (15659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a55a9179da25fb564baf3c87b7bb66208668b320d243abe525450e7a86eff6`

```dockerfile
```

-	Layers:
	-	`sha256:a281ebaeeb069412b51c7976e2106c32d13da9721fa29ea45947ed25c3b75e59`  
		Last Modified: Mon, 22 Jun 2026 19:46:10 GMT  
		Size: 15.7 KB (15659 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:0103ae89f8bc17e7218ad8c552081abc2eac69570e28e3dd0380edd5a7b4a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11670137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd0cdcc825862d384bb7968516e5d1e905b2804725a20192b0c083796739012`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:55 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Mon, 22 Jun 2026 19:46:55 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Mon, 22 Jun 2026 19:46:56 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl tcl9 tcl9-dev # buildkit
# Mon, 22 Jun 2026 19:46:56 GMT
ENV EGGDROP_SHA256=e42668f102c1446901b066d13fe0bf39622afca8d723f356ac2390d5faaf6e5e
# Mon, 22 Jun 2026 19:46:56 GMT
ENV EGGDROP_COMMIT=541e8ac17e549a40e177b5eea54e4abf24629a33
# Mon, 22 Jun 2026 19:47:13 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Mon, 22 Jun 2026 19:47:13 GMT
ENV NICK=
# Mon, 22 Jun 2026 19:47:13 GMT
ENV SERVER=
# Mon, 22 Jun 2026 19:47:13 GMT
ENV LISTEN=3333
# Mon, 22 Jun 2026 19:47:13 GMT
ENV USERFILE=eggdrop.user
# Mon, 22 Jun 2026 19:47:13 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 22 Jun 2026 19:47:13 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 22 Jun 2026 19:47:13 GMT
EXPOSE map[3333/tcp:{}]
# Mon, 22 Jun 2026 19:47:13 GMT
COPY entrypoint.sh ./ # buildkit
# Mon, 22 Jun 2026 19:47:13 GMT
COPY docker.tcl ./scripts/ # buildkit
# Mon, 22 Jun 2026 19:47:13 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 22 Jun 2026 19:47:13 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a6678e82d80efd9efcb24a47993940cc934a4c7a4e4852262ae525ddddc70a`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90595943eb024bb62787931b93996d3780d7a573c3872eb301f2e2e1ad8dc41e`  
		Last Modified: Mon, 22 Jun 2026 19:47:19 GMT  
		Size: 4.8 MB (4823734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c578a5d2c01376d5ec9a0d2407811fdf719d1c17e16eee09fde77460666c5dab`  
		Last Modified: Mon, 22 Jun 2026 19:47:19 GMT  
		Size: 2.7 MB (2660473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76353eda4c9e040bf5d2cab45e04a3395c7f86481167a2b124583e3b8daf7f07`  
		Last Modified: Mon, 22 Jun 2026 19:47:19 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1668f6d47a72570b1ffa667e77dc96f083b2a546334b5e57f6a0a33df4d1d9c`  
		Last Modified: Mon, 22 Jun 2026 19:47:21 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:712c594b6e75907ba3440964f21c0268a06011d0649e188b4e585e6fbcbeacd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **753.5 KB (753487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56128c1c853f455e7c3d9b157551a5880c6403bfec82e8c747d5faf64b28b13e`

```dockerfile
```

-	Layers:
	-	`sha256:fcf85ecdb36d750c6542f2a781026e82feb78d20d5cfc0c3699fe6bd5a395234`  
		Last Modified: Mon, 22 Jun 2026 19:47:19 GMT  
		Size: 737.6 KB (737597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ff973a28729a4de88b1c521f5c394dff9dd043dd7b4af7140c976a1695a1795`  
		Last Modified: Mon, 22 Jun 2026 19:47:19 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json
