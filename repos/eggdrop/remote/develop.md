## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:5ecef503547b119fcf74cf2b6ea0fbf37ee13edd0b7db7b4ef8c4930a048f44d
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
$ docker pull eggdrop@sha256:dabfcf059c265dce23afcf0c50c74d50885f34e80ef2e479c8341a7f29947132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12783005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:635ee8f865d9b80af29f2b6e0bd723d6223902e8ec9cf3317a40bbe5a507d5fd`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 03 Feb 2025 02:59:38 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Mon, 03 Feb 2025 02:59:38 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENV EGGDROP_SHA256=e42668f102c1446901b066d13fe0bf39622afca8d723f356ac2390d5faaf6e5e
# Mon, 03 Feb 2025 02:59:38 GMT
ENV EGGDROP_COMMIT=541e8ac17e549a40e177b5eea54e4abf24629a33
# Mon, 03 Feb 2025 02:59:38 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENV NICK=
# Mon, 03 Feb 2025 02:59:38 GMT
ENV SERVER=
# Mon, 03 Feb 2025 02:59:38 GMT
ENV LISTEN=3333
# Mon, 03 Feb 2025 02:59:38 GMT
ENV USERFILE=eggdrop.user
# Mon, 03 Feb 2025 02:59:38 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 03 Feb 2025 02:59:38 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 03 Feb 2025 02:59:38 GMT
EXPOSE map[3333/tcp:{}]
# Mon, 03 Feb 2025 02:59:38 GMT
COPY entrypoint.sh ./ # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
COPY docker.tcl ./scripts/ # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 03 Feb 2025 02:59:38 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122c69717639f8f256364490094110a9b1d7df56ceeb8b13a8d1b39f244d6f0c`  
		Last Modified: Mon, 03 Feb 2025 21:31:41 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8bde30c3b94071f7844cf5bb2e2274e51f5cceb7ef5f197a271fa8c83a24de`  
		Last Modified: Mon, 03 Feb 2025 21:31:40 GMT  
		Size: 1.1 MB (1115812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec388b64790efbb9db340f4dc80ff4899a6b71a814c8a2168c0234e8f3d0cbd`  
		Last Modified: Mon, 03 Feb 2025 21:31:41 GMT  
		Size: 8.0 MB (8021396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c05351390994af83d27d0cba64c41501ae8fcf9416e81e1b1b55b59e2d6dce0`  
		Last Modified: Mon, 03 Feb 2025 21:31:41 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bf7b3a5bc3a95ed12410f09561e43d7e4988b7f1d4c1eb977f77c40ac144bb`  
		Last Modified: Mon, 03 Feb 2025 21:31:41 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:d7733f68b9587cc8ddd5d0a5e87d4ae804c4f8fadef4db20b2e83f1fb595d6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 KB (157998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8375dc6928b79c66f37f6fd0966f5576446a8176af47e4ddf851b92e3a5e100c`

```dockerfile
```

-	Layers:
	-	`sha256:f6e3eac3c72850023dd63fa450bacdeda03c45f90b1e71b8592b5eb3b99d0b32`  
		Last Modified: Mon, 03 Feb 2025 21:31:40 GMT  
		Size: 140.9 KB (140907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caaf4736ea1b75742ee2d3123aba3def171951d2e2bf457400e8fe104a48574d`  
		Last Modified: Mon, 03 Feb 2025 21:31:40 GMT  
		Size: 17.1 KB (17091 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:1cdf139a4989d2ad5ffd7ed840d1697d4ffb35cf76e617d89c6bb3ad12ff8d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12335343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:465ec1c7e929eb858e0c6bf6914b06ac69ca9fec1f8948ff74f8d539d0240dc1`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 03 Feb 2025 02:59:38 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Mon, 03 Feb 2025 02:59:38 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENV EGGDROP_SHA256=e42668f102c1446901b066d13fe0bf39622afca8d723f356ac2390d5faaf6e5e
# Mon, 03 Feb 2025 02:59:38 GMT
ENV EGGDROP_COMMIT=541e8ac17e549a40e177b5eea54e4abf24629a33
# Mon, 03 Feb 2025 02:59:38 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENV NICK=
# Mon, 03 Feb 2025 02:59:38 GMT
ENV SERVER=
# Mon, 03 Feb 2025 02:59:38 GMT
ENV LISTEN=3333
# Mon, 03 Feb 2025 02:59:38 GMT
ENV USERFILE=eggdrop.user
# Mon, 03 Feb 2025 02:59:38 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 03 Feb 2025 02:59:38 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 03 Feb 2025 02:59:38 GMT
EXPOSE map[3333/tcp:{}]
# Mon, 03 Feb 2025 02:59:38 GMT
COPY entrypoint.sh ./ # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
COPY docker.tcl ./scripts/ # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 03 Feb 2025 02:59:38 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8f92d7debdb4d79633eeee7d89d5ec7468cde32925a38203f69b85781f316c`  
		Last Modified: Mon, 03 Feb 2025 21:32:10 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15725b51278e03d3c324719d25c1799bd692ea6b3b003c819fb6d28a8893325`  
		Last Modified: Mon, 03 Feb 2025 21:32:11 GMT  
		Size: 1.1 MB (1128397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a804f50c83cd24a866317a2805d790c695557d5e51454e82b1f2ff6ca44d58`  
		Last Modified: Mon, 03 Feb 2025 21:32:11 GMT  
		Size: 7.8 MB (7838980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0603e1c6d079da7203b313e2436309b43dac0c1e80b5d16cc4ad992f099526dc`  
		Last Modified: Mon, 03 Feb 2025 21:32:10 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5395b5804db45aeffd996b34b5d4aada3319ae0e66fd60bbd416b8e010d8269d`  
		Last Modified: Mon, 03 Feb 2025 21:32:11 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:b751bbe2e315c71ea63cbac948079d70650b5bb5ef935c5ae90b66dca64f1c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (16954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd816744d1b75356db445fe3e76d4067145ac6730d2bb7c8b78a36ef0a724ce`

```dockerfile
```

-	Layers:
	-	`sha256:2893f80852f7c4cfcb5dfb30ebe9bfda73be170ef50f0e8b619914742f940594`  
		Last Modified: Mon, 03 Feb 2025 21:32:10 GMT  
		Size: 17.0 KB (16954 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:50d1d13c591a6216d72854f73613b558524d8bafc2546b227efbda6676ea0f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13234211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fee526bbe500fb6844da3a7e43ee8483a0177f94d0e2d9b70b71bdc43fe4f59`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 03 Feb 2025 02:59:38 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Mon, 03 Feb 2025 02:59:38 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENV EGGDROP_SHA256=e42668f102c1446901b066d13fe0bf39622afca8d723f356ac2390d5faaf6e5e
# Mon, 03 Feb 2025 02:59:38 GMT
ENV EGGDROP_COMMIT=541e8ac17e549a40e177b5eea54e4abf24629a33
# Mon, 03 Feb 2025 02:59:38 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENV NICK=
# Mon, 03 Feb 2025 02:59:38 GMT
ENV SERVER=
# Mon, 03 Feb 2025 02:59:38 GMT
ENV LISTEN=3333
# Mon, 03 Feb 2025 02:59:38 GMT
ENV USERFILE=eggdrop.user
# Mon, 03 Feb 2025 02:59:38 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 03 Feb 2025 02:59:38 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 03 Feb 2025 02:59:38 GMT
EXPOSE map[3333/tcp:{}]
# Mon, 03 Feb 2025 02:59:38 GMT
COPY entrypoint.sh ./ # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
COPY docker.tcl ./scripts/ # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 03 Feb 2025 02:59:38 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51e44dcc35225de03a01a04dd3e872ead2ffb431dc6ea6c1ba4642baad081cb`  
		Last Modified: Mon, 03 Feb 2025 21:31:20 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374bceaeb5647a8e79c93eb68141d61aef47d1ec39c4b5e070cbc625038eb685`  
		Last Modified: Mon, 03 Feb 2025 21:31:20 GMT  
		Size: 1.2 MB (1169751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d19e42b835cfdd5d7e7d74a70e38e8da5b9cf7d88f72c2abc258b9bf27ffbf`  
		Last Modified: Mon, 03 Feb 2025 21:31:20 GMT  
		Size: 8.1 MB (8068017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891218d2ab450d92507655dc2bb8596d02036d1d381bab3f4a91c9c7ed164e77`  
		Last Modified: Mon, 03 Feb 2025 21:31:20 GMT  
		Size: 2.0 KB (1965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481bb921d265f236b4768010107ea10865418f0cc106017acc03c6d2dc445352`  
		Last Modified: Mon, 03 Feb 2025 21:31:21 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:ef72f33e2126e4aa7cd68ce36a068846df8f098681e61771ce8762068d97bc3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 KB (158116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5b370b58af939337011efb63acac525614c4b3b8864b23af1462e04fea6edc`

```dockerfile
```

-	Layers:
	-	`sha256:4a4c3057aea11e609e871a2c9333907c8d57d60e1d21cc1ad69ee12ff99c0ebd`  
		Last Modified: Mon, 03 Feb 2025 21:31:20 GMT  
		Size: 140.9 KB (140927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dffef19ea40c320b1ea56d51134fea4040cb324076b72d92c2b1b21c93aa9dba`  
		Last Modified: Mon, 03 Feb 2025 21:31:20 GMT  
		Size: 17.2 KB (17189 bytes)  
		MIME: application/vnd.in-toto+json
