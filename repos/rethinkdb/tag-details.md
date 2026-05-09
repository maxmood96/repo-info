<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rethinkdb`

-	[`rethinkdb:2`](#rethinkdb2)
-	[`rethinkdb:2-bookworm-slim`](#rethinkdb2-bookworm-slim)
-	[`rethinkdb:2.4`](#rethinkdb24)
-	[`rethinkdb:2.4-bookworm-slim`](#rethinkdb24-bookworm-slim)
-	[`rethinkdb:2.4.3`](#rethinkdb243)
-	[`rethinkdb:2.4.4-bookworm-slim`](#rethinkdb244-bookworm-slim)
-	[`rethinkdb:bookworm-slim`](#rethinkdbbookworm-slim)
-	[`rethinkdb:latest`](#rethinkdblatest)

## `rethinkdb:2`

```console
$ docker pull rethinkdb@sha256:0bc26dd1ddcc98daa59ce2b8d411a612e83fd69939c61a516b1a239ed40c3f87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:65ef63b04a02288f9b7da0c33b72ce005f4628cf255eecb8dce2962aef253e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48032601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348a73cb65421607e53298dfa8ba2eb75d76c498b02e34b7a3f5aabfe80cec58`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:34:52 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:34:53 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Fri, 08 May 2026 19:34:59 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Fri, 08 May 2026 19:34:59 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:34:59 GMT
VOLUME [/data]
# Fri, 08 May 2026 19:34:59 GMT
WORKDIR /data
# Fri, 08 May 2026 19:34:59 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 08 May 2026 19:34:59 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be42315b74021fc821e3d4f8dea28bc96efa4566bc77d119be47c4a15b5d718`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 9.8 MB (9800379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90352bb79e31597db22e449a1099f44111c7179772a8e53703917b27a9524337`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e75085611ad52c683edddc2974803ee701e1ef8e6cbc8fcc1732d604df55b`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 10.0 MB (9993177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9460c31950998ea3065b9e1eed7e7963d15dfd8c2f329dc4d90aace6e47462fa`  
		Last Modified: Fri, 08 May 2026 19:35:05 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:bdba3937f096a4aef1f4f53582fcfb397fe5323af6a28934942d054926ee9dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0a484b1cefe9f6ecb2d602ec1887c044b5ce7d5d57f49047658614aebf5077`

```dockerfile
```

-	Layers:
	-	`sha256:52fa4a02b9688d6dd2be556f1e87d263d31e2ade80948dfec07f114b69439c58`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51bf7af16f16a82790238619e2fcfbf2b230947887b860e59f69985703e09b71`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:c57d246b12b6bdac8d00af576810c3329a460e6d262a61db87aab1255456604f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47111528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582739fdd9909b17297270b551db471f03e47a396ff37c61ae3035fdf6639cd8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:36:29 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:36:30 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Fri, 08 May 2026 19:36:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Fri, 08 May 2026 19:36:35 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:36:35 GMT
VOLUME [/data]
# Fri, 08 May 2026 19:36:35 GMT
WORKDIR /data
# Fri, 08 May 2026 19:36:35 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 08 May 2026 19:36:35 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008686a7c703c914115ea0c85877764c6ef3ef40df8a0ec96c1b449eecb0b9bd`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 9.6 MB (9629636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6ff60a4ba799ab9025e0b99743829d490a7e021e0cbde7aa64670d5efbb5da`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 2.7 KB (2672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fa0892b7f895e51796d00e79259613b40d439285ec7a96bea52e27a92a2017`  
		Last Modified: Fri, 08 May 2026 19:36:43 GMT  
		Size: 9.4 MB (9362961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5ecdd83a3e0130849b0f770b6511b27fa5d6d4d55d7cf9754b34f1417365fb`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:59444f28d1005b9f738081badfac33e5d75f22978ebab9b0e5ef9e4903e7d6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f7cf0c623491b6b0b0b0d7ca1fa24211aaa8cf0e60a8ed38d21796713027ef`

```dockerfile
```

-	Layers:
	-	`sha256:1039c022f54b90684969ded63b1c65825dc7f362dce123bd9e4a07f5de7d5047`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:616418d243a44e68ca534809dc3f62061612fe821c6a24d080770b73d11489e3`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2` - linux; s390x

```console
$ docker pull rethinkdb@sha256:ae0a1a1dc9d60a1489c1e3de485db0b79bb6850e982bdbc0578ef03df8b610c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45496570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455656e6c9b6e39b6fb1ab5a9b0ea929a78fbcb3f1e799cc269967c8da73df95`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:51:41 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:51:42 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Fri, 08 May 2026 20:51:47 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Fri, 08 May 2026 20:51:47 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:51:47 GMT
VOLUME [/data]
# Fri, 08 May 2026 20:51:47 GMT
WORKDIR /data
# Fri, 08 May 2026 20:51:47 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 08 May 2026 20:51:47 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088b07e1d4ab6851c27e72ca04845c64afb9e2e874810b60c7d7ee315087f078`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 9.3 MB (9298427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cf8b3ac1199ea21d4bee7ac7fe307e373b7f82ebfc12cac84937a3530314c9`  
		Last Modified: Fri, 08 May 2026 20:52:00 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9429beadbe53e7cc00504d69272fd52a73280b0b4bcd141d43d91e50ed5bb23e`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 9.3 MB (9303780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da307de32ecd3c2ca014572ee61a176728536770780dd50d1dea146cbe7d1f1d`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:923cedeaf12a838f49051d8f4c54712822cd6c237da03f9735be44c056f68708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248009493c8e501134086960f3c13eec9a35942321ea589e02e9ed888adc2e80`

```dockerfile
```

-	Layers:
	-	`sha256:bda4b75a16269d180e761c8b60f265f5a629bc501619a49c801bdf42d45b0c6f`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c550857a14d97696e3b3318780c7e115cbf73e3cdfbaec81edaa7934b69e2b5`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:0bc26dd1ddcc98daa59ce2b8d411a612e83fd69939c61a516b1a239ed40c3f87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2-bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:65ef63b04a02288f9b7da0c33b72ce005f4628cf255eecb8dce2962aef253e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48032601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348a73cb65421607e53298dfa8ba2eb75d76c498b02e34b7a3f5aabfe80cec58`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:34:52 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:34:53 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Fri, 08 May 2026 19:34:59 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Fri, 08 May 2026 19:34:59 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:34:59 GMT
VOLUME [/data]
# Fri, 08 May 2026 19:34:59 GMT
WORKDIR /data
# Fri, 08 May 2026 19:34:59 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 08 May 2026 19:34:59 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be42315b74021fc821e3d4f8dea28bc96efa4566bc77d119be47c4a15b5d718`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 9.8 MB (9800379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90352bb79e31597db22e449a1099f44111c7179772a8e53703917b27a9524337`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e75085611ad52c683edddc2974803ee701e1ef8e6cbc8fcc1732d604df55b`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 10.0 MB (9993177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9460c31950998ea3065b9e1eed7e7963d15dfd8c2f329dc4d90aace6e47462fa`  
		Last Modified: Fri, 08 May 2026 19:35:05 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:bdba3937f096a4aef1f4f53582fcfb397fe5323af6a28934942d054926ee9dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0a484b1cefe9f6ecb2d602ec1887c044b5ce7d5d57f49047658614aebf5077`

```dockerfile
```

-	Layers:
	-	`sha256:52fa4a02b9688d6dd2be556f1e87d263d31e2ade80948dfec07f114b69439c58`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51bf7af16f16a82790238619e2fcfbf2b230947887b860e59f69985703e09b71`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:c57d246b12b6bdac8d00af576810c3329a460e6d262a61db87aab1255456604f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47111528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582739fdd9909b17297270b551db471f03e47a396ff37c61ae3035fdf6639cd8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:36:29 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:36:30 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Fri, 08 May 2026 19:36:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Fri, 08 May 2026 19:36:35 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:36:35 GMT
VOLUME [/data]
# Fri, 08 May 2026 19:36:35 GMT
WORKDIR /data
# Fri, 08 May 2026 19:36:35 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 08 May 2026 19:36:35 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008686a7c703c914115ea0c85877764c6ef3ef40df8a0ec96c1b449eecb0b9bd`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 9.6 MB (9629636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6ff60a4ba799ab9025e0b99743829d490a7e021e0cbde7aa64670d5efbb5da`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 2.7 KB (2672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fa0892b7f895e51796d00e79259613b40d439285ec7a96bea52e27a92a2017`  
		Last Modified: Fri, 08 May 2026 19:36:43 GMT  
		Size: 9.4 MB (9362961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5ecdd83a3e0130849b0f770b6511b27fa5d6d4d55d7cf9754b34f1417365fb`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:59444f28d1005b9f738081badfac33e5d75f22978ebab9b0e5ef9e4903e7d6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f7cf0c623491b6b0b0b0d7ca1fa24211aaa8cf0e60a8ed38d21796713027ef`

```dockerfile
```

-	Layers:
	-	`sha256:1039c022f54b90684969ded63b1c65825dc7f362dce123bd9e4a07f5de7d5047`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:616418d243a44e68ca534809dc3f62061612fe821c6a24d080770b73d11489e3`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:ae0a1a1dc9d60a1489c1e3de485db0b79bb6850e982bdbc0578ef03df8b610c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45496570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455656e6c9b6e39b6fb1ab5a9b0ea929a78fbcb3f1e799cc269967c8da73df95`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:51:41 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:51:42 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Fri, 08 May 2026 20:51:47 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Fri, 08 May 2026 20:51:47 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:51:47 GMT
VOLUME [/data]
# Fri, 08 May 2026 20:51:47 GMT
WORKDIR /data
# Fri, 08 May 2026 20:51:47 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 08 May 2026 20:51:47 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088b07e1d4ab6851c27e72ca04845c64afb9e2e874810b60c7d7ee315087f078`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 9.3 MB (9298427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cf8b3ac1199ea21d4bee7ac7fe307e373b7f82ebfc12cac84937a3530314c9`  
		Last Modified: Fri, 08 May 2026 20:52:00 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9429beadbe53e7cc00504d69272fd52a73280b0b4bcd141d43d91e50ed5bb23e`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 9.3 MB (9303780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da307de32ecd3c2ca014572ee61a176728536770780dd50d1dea146cbe7d1f1d`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:923cedeaf12a838f49051d8f4c54712822cd6c237da03f9735be44c056f68708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248009493c8e501134086960f3c13eec9a35942321ea589e02e9ed888adc2e80`

```dockerfile
```

-	Layers:
	-	`sha256:bda4b75a16269d180e761c8b60f265f5a629bc501619a49c801bdf42d45b0c6f`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c550857a14d97696e3b3318780c7e115cbf73e3cdfbaec81edaa7934b69e2b5`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:0bc26dd1ddcc98daa59ce2b8d411a612e83fd69939c61a516b1a239ed40c3f87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2.4` - linux; amd64

```console
$ docker pull rethinkdb@sha256:65ef63b04a02288f9b7da0c33b72ce005f4628cf255eecb8dce2962aef253e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48032601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348a73cb65421607e53298dfa8ba2eb75d76c498b02e34b7a3f5aabfe80cec58`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:34:52 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:34:53 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Fri, 08 May 2026 19:34:59 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Fri, 08 May 2026 19:34:59 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:34:59 GMT
VOLUME [/data]
# Fri, 08 May 2026 19:34:59 GMT
WORKDIR /data
# Fri, 08 May 2026 19:34:59 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 08 May 2026 19:34:59 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be42315b74021fc821e3d4f8dea28bc96efa4566bc77d119be47c4a15b5d718`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 9.8 MB (9800379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90352bb79e31597db22e449a1099f44111c7179772a8e53703917b27a9524337`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e75085611ad52c683edddc2974803ee701e1ef8e6cbc8fcc1732d604df55b`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 10.0 MB (9993177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9460c31950998ea3065b9e1eed7e7963d15dfd8c2f329dc4d90aace6e47462fa`  
		Last Modified: Fri, 08 May 2026 19:35:05 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:bdba3937f096a4aef1f4f53582fcfb397fe5323af6a28934942d054926ee9dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0a484b1cefe9f6ecb2d602ec1887c044b5ce7d5d57f49047658614aebf5077`

```dockerfile
```

-	Layers:
	-	`sha256:52fa4a02b9688d6dd2be556f1e87d263d31e2ade80948dfec07f114b69439c58`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51bf7af16f16a82790238619e2fcfbf2b230947887b860e59f69985703e09b71`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:c57d246b12b6bdac8d00af576810c3329a460e6d262a61db87aab1255456604f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47111528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582739fdd9909b17297270b551db471f03e47a396ff37c61ae3035fdf6639cd8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:36:29 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:36:30 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Fri, 08 May 2026 19:36:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Fri, 08 May 2026 19:36:35 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:36:35 GMT
VOLUME [/data]
# Fri, 08 May 2026 19:36:35 GMT
WORKDIR /data
# Fri, 08 May 2026 19:36:35 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 08 May 2026 19:36:35 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008686a7c703c914115ea0c85877764c6ef3ef40df8a0ec96c1b449eecb0b9bd`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 9.6 MB (9629636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6ff60a4ba799ab9025e0b99743829d490a7e021e0cbde7aa64670d5efbb5da`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 2.7 KB (2672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fa0892b7f895e51796d00e79259613b40d439285ec7a96bea52e27a92a2017`  
		Last Modified: Fri, 08 May 2026 19:36:43 GMT  
		Size: 9.4 MB (9362961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5ecdd83a3e0130849b0f770b6511b27fa5d6d4d55d7cf9754b34f1417365fb`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:59444f28d1005b9f738081badfac33e5d75f22978ebab9b0e5ef9e4903e7d6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f7cf0c623491b6b0b0b0d7ca1fa24211aaa8cf0e60a8ed38d21796713027ef`

```dockerfile
```

-	Layers:
	-	`sha256:1039c022f54b90684969ded63b1c65825dc7f362dce123bd9e4a07f5de7d5047`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:616418d243a44e68ca534809dc3f62061612fe821c6a24d080770b73d11489e3`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4` - linux; s390x

```console
$ docker pull rethinkdb@sha256:ae0a1a1dc9d60a1489c1e3de485db0b79bb6850e982bdbc0578ef03df8b610c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45496570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455656e6c9b6e39b6fb1ab5a9b0ea929a78fbcb3f1e799cc269967c8da73df95`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:51:41 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:51:42 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Fri, 08 May 2026 20:51:47 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Fri, 08 May 2026 20:51:47 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:51:47 GMT
VOLUME [/data]
# Fri, 08 May 2026 20:51:47 GMT
WORKDIR /data
# Fri, 08 May 2026 20:51:47 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 08 May 2026 20:51:47 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088b07e1d4ab6851c27e72ca04845c64afb9e2e874810b60c7d7ee315087f078`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 9.3 MB (9298427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cf8b3ac1199ea21d4bee7ac7fe307e373b7f82ebfc12cac84937a3530314c9`  
		Last Modified: Fri, 08 May 2026 20:52:00 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9429beadbe53e7cc00504d69272fd52a73280b0b4bcd141d43d91e50ed5bb23e`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 9.3 MB (9303780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da307de32ecd3c2ca014572ee61a176728536770780dd50d1dea146cbe7d1f1d`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:923cedeaf12a838f49051d8f4c54712822cd6c237da03f9735be44c056f68708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248009493c8e501134086960f3c13eec9a35942321ea589e02e9ed888adc2e80`

```dockerfile
```

-	Layers:
	-	`sha256:bda4b75a16269d180e761c8b60f265f5a629bc501619a49c801bdf42d45b0c6f`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c550857a14d97696e3b3318780c7e115cbf73e3cdfbaec81edaa7934b69e2b5`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:0bc26dd1ddcc98daa59ce2b8d411a612e83fd69939c61a516b1a239ed40c3f87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2.4-bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:65ef63b04a02288f9b7da0c33b72ce005f4628cf255eecb8dce2962aef253e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48032601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348a73cb65421607e53298dfa8ba2eb75d76c498b02e34b7a3f5aabfe80cec58`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:34:52 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:34:53 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Fri, 08 May 2026 19:34:59 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Fri, 08 May 2026 19:34:59 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:34:59 GMT
VOLUME [/data]
# Fri, 08 May 2026 19:34:59 GMT
WORKDIR /data
# Fri, 08 May 2026 19:34:59 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 08 May 2026 19:34:59 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be42315b74021fc821e3d4f8dea28bc96efa4566bc77d119be47c4a15b5d718`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 9.8 MB (9800379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90352bb79e31597db22e449a1099f44111c7179772a8e53703917b27a9524337`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e75085611ad52c683edddc2974803ee701e1ef8e6cbc8fcc1732d604df55b`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 10.0 MB (9993177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9460c31950998ea3065b9e1eed7e7963d15dfd8c2f329dc4d90aace6e47462fa`  
		Last Modified: Fri, 08 May 2026 19:35:05 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:bdba3937f096a4aef1f4f53582fcfb397fe5323af6a28934942d054926ee9dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0a484b1cefe9f6ecb2d602ec1887c044b5ce7d5d57f49047658614aebf5077`

```dockerfile
```

-	Layers:
	-	`sha256:52fa4a02b9688d6dd2be556f1e87d263d31e2ade80948dfec07f114b69439c58`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51bf7af16f16a82790238619e2fcfbf2b230947887b860e59f69985703e09b71`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:c57d246b12b6bdac8d00af576810c3329a460e6d262a61db87aab1255456604f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47111528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582739fdd9909b17297270b551db471f03e47a396ff37c61ae3035fdf6639cd8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:36:29 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:36:30 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Fri, 08 May 2026 19:36:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Fri, 08 May 2026 19:36:35 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:36:35 GMT
VOLUME [/data]
# Fri, 08 May 2026 19:36:35 GMT
WORKDIR /data
# Fri, 08 May 2026 19:36:35 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 08 May 2026 19:36:35 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008686a7c703c914115ea0c85877764c6ef3ef40df8a0ec96c1b449eecb0b9bd`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 9.6 MB (9629636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6ff60a4ba799ab9025e0b99743829d490a7e021e0cbde7aa64670d5efbb5da`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 2.7 KB (2672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fa0892b7f895e51796d00e79259613b40d439285ec7a96bea52e27a92a2017`  
		Last Modified: Fri, 08 May 2026 19:36:43 GMT  
		Size: 9.4 MB (9362961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5ecdd83a3e0130849b0f770b6511b27fa5d6d4d55d7cf9754b34f1417365fb`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:59444f28d1005b9f738081badfac33e5d75f22978ebab9b0e5ef9e4903e7d6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f7cf0c623491b6b0b0b0d7ca1fa24211aaa8cf0e60a8ed38d21796713027ef`

```dockerfile
```

-	Layers:
	-	`sha256:1039c022f54b90684969ded63b1c65825dc7f362dce123bd9e4a07f5de7d5047`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:616418d243a44e68ca534809dc3f62061612fe821c6a24d080770b73d11489e3`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:ae0a1a1dc9d60a1489c1e3de485db0b79bb6850e982bdbc0578ef03df8b610c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45496570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455656e6c9b6e39b6fb1ab5a9b0ea929a78fbcb3f1e799cc269967c8da73df95`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:51:41 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:51:42 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Fri, 08 May 2026 20:51:47 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Fri, 08 May 2026 20:51:47 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:51:47 GMT
VOLUME [/data]
# Fri, 08 May 2026 20:51:47 GMT
WORKDIR /data
# Fri, 08 May 2026 20:51:47 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 08 May 2026 20:51:47 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088b07e1d4ab6851c27e72ca04845c64afb9e2e874810b60c7d7ee315087f078`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 9.3 MB (9298427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cf8b3ac1199ea21d4bee7ac7fe307e373b7f82ebfc12cac84937a3530314c9`  
		Last Modified: Fri, 08 May 2026 20:52:00 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9429beadbe53e7cc00504d69272fd52a73280b0b4bcd141d43d91e50ed5bb23e`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 9.3 MB (9303780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da307de32ecd3c2ca014572ee61a176728536770780dd50d1dea146cbe7d1f1d`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:923cedeaf12a838f49051d8f4c54712822cd6c237da03f9735be44c056f68708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248009493c8e501134086960f3c13eec9a35942321ea589e02e9ed888adc2e80`

```dockerfile
```

-	Layers:
	-	`sha256:bda4b75a16269d180e761c8b60f265f5a629bc501619a49c801bdf42d45b0c6f`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c550857a14d97696e3b3318780c7e115cbf73e3cdfbaec81edaa7934b69e2b5`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4.3`

```console
$ docker pull rethinkdb@sha256:0bc26dd1ddcc98daa59ce2b8d411a612e83fd69939c61a516b1a239ed40c3f87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2.4.3` - linux; amd64

```console
$ docker pull rethinkdb@sha256:65ef63b04a02288f9b7da0c33b72ce005f4628cf255eecb8dce2962aef253e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48032601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348a73cb65421607e53298dfa8ba2eb75d76c498b02e34b7a3f5aabfe80cec58`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:34:52 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:34:53 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Fri, 08 May 2026 19:34:59 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Fri, 08 May 2026 19:34:59 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:34:59 GMT
VOLUME [/data]
# Fri, 08 May 2026 19:34:59 GMT
WORKDIR /data
# Fri, 08 May 2026 19:34:59 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 08 May 2026 19:34:59 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be42315b74021fc821e3d4f8dea28bc96efa4566bc77d119be47c4a15b5d718`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 9.8 MB (9800379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90352bb79e31597db22e449a1099f44111c7179772a8e53703917b27a9524337`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e75085611ad52c683edddc2974803ee701e1ef8e6cbc8fcc1732d604df55b`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 10.0 MB (9993177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9460c31950998ea3065b9e1eed7e7963d15dfd8c2f329dc4d90aace6e47462fa`  
		Last Modified: Fri, 08 May 2026 19:35:05 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:bdba3937f096a4aef1f4f53582fcfb397fe5323af6a28934942d054926ee9dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0a484b1cefe9f6ecb2d602ec1887c044b5ce7d5d57f49047658614aebf5077`

```dockerfile
```

-	Layers:
	-	`sha256:52fa4a02b9688d6dd2be556f1e87d263d31e2ade80948dfec07f114b69439c58`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51bf7af16f16a82790238619e2fcfbf2b230947887b860e59f69985703e09b71`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.3` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:c57d246b12b6bdac8d00af576810c3329a460e6d262a61db87aab1255456604f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47111528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582739fdd9909b17297270b551db471f03e47a396ff37c61ae3035fdf6639cd8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:36:29 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:36:30 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Fri, 08 May 2026 19:36:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Fri, 08 May 2026 19:36:35 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:36:35 GMT
VOLUME [/data]
# Fri, 08 May 2026 19:36:35 GMT
WORKDIR /data
# Fri, 08 May 2026 19:36:35 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 08 May 2026 19:36:35 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008686a7c703c914115ea0c85877764c6ef3ef40df8a0ec96c1b449eecb0b9bd`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 9.6 MB (9629636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6ff60a4ba799ab9025e0b99743829d490a7e021e0cbde7aa64670d5efbb5da`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 2.7 KB (2672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fa0892b7f895e51796d00e79259613b40d439285ec7a96bea52e27a92a2017`  
		Last Modified: Fri, 08 May 2026 19:36:43 GMT  
		Size: 9.4 MB (9362961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5ecdd83a3e0130849b0f770b6511b27fa5d6d4d55d7cf9754b34f1417365fb`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:59444f28d1005b9f738081badfac33e5d75f22978ebab9b0e5ef9e4903e7d6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f7cf0c623491b6b0b0b0d7ca1fa24211aaa8cf0e60a8ed38d21796713027ef`

```dockerfile
```

-	Layers:
	-	`sha256:1039c022f54b90684969ded63b1c65825dc7f362dce123bd9e4a07f5de7d5047`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:616418d243a44e68ca534809dc3f62061612fe821c6a24d080770b73d11489e3`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.3` - linux; s390x

```console
$ docker pull rethinkdb@sha256:ae0a1a1dc9d60a1489c1e3de485db0b79bb6850e982bdbc0578ef03df8b610c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45496570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455656e6c9b6e39b6fb1ab5a9b0ea929a78fbcb3f1e799cc269967c8da73df95`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:51:41 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:51:42 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Fri, 08 May 2026 20:51:47 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Fri, 08 May 2026 20:51:47 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:51:47 GMT
VOLUME [/data]
# Fri, 08 May 2026 20:51:47 GMT
WORKDIR /data
# Fri, 08 May 2026 20:51:47 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 08 May 2026 20:51:47 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088b07e1d4ab6851c27e72ca04845c64afb9e2e874810b60c7d7ee315087f078`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 9.3 MB (9298427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cf8b3ac1199ea21d4bee7ac7fe307e373b7f82ebfc12cac84937a3530314c9`  
		Last Modified: Fri, 08 May 2026 20:52:00 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9429beadbe53e7cc00504d69272fd52a73280b0b4bcd141d43d91e50ed5bb23e`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 9.3 MB (9303780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da307de32ecd3c2ca014572ee61a176728536770780dd50d1dea146cbe7d1f1d`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:923cedeaf12a838f49051d8f4c54712822cd6c237da03f9735be44c056f68708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248009493c8e501134086960f3c13eec9a35942321ea589e02e9ed888adc2e80`

```dockerfile
```

-	Layers:
	-	`sha256:bda4b75a16269d180e761c8b60f265f5a629bc501619a49c801bdf42d45b0c6f`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c550857a14d97696e3b3318780c7e115cbf73e3cdfbaec81edaa7934b69e2b5`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4.4-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:0bc26dd1ddcc98daa59ce2b8d411a612e83fd69939c61a516b1a239ed40c3f87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2.4.4-bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:65ef63b04a02288f9b7da0c33b72ce005f4628cf255eecb8dce2962aef253e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48032601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348a73cb65421607e53298dfa8ba2eb75d76c498b02e34b7a3f5aabfe80cec58`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:34:52 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:34:53 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Fri, 08 May 2026 19:34:59 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Fri, 08 May 2026 19:34:59 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:34:59 GMT
VOLUME [/data]
# Fri, 08 May 2026 19:34:59 GMT
WORKDIR /data
# Fri, 08 May 2026 19:34:59 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 08 May 2026 19:34:59 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be42315b74021fc821e3d4f8dea28bc96efa4566bc77d119be47c4a15b5d718`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 9.8 MB (9800379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90352bb79e31597db22e449a1099f44111c7179772a8e53703917b27a9524337`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e75085611ad52c683edddc2974803ee701e1ef8e6cbc8fcc1732d604df55b`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 10.0 MB (9993177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9460c31950998ea3065b9e1eed7e7963d15dfd8c2f329dc4d90aace6e47462fa`  
		Last Modified: Fri, 08 May 2026 19:35:05 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:bdba3937f096a4aef1f4f53582fcfb397fe5323af6a28934942d054926ee9dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0a484b1cefe9f6ecb2d602ec1887c044b5ce7d5d57f49047658614aebf5077`

```dockerfile
```

-	Layers:
	-	`sha256:52fa4a02b9688d6dd2be556f1e87d263d31e2ade80948dfec07f114b69439c58`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51bf7af16f16a82790238619e2fcfbf2b230947887b860e59f69985703e09b71`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.4-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:c57d246b12b6bdac8d00af576810c3329a460e6d262a61db87aab1255456604f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47111528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582739fdd9909b17297270b551db471f03e47a396ff37c61ae3035fdf6639cd8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:36:29 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:36:30 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Fri, 08 May 2026 19:36:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Fri, 08 May 2026 19:36:35 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:36:35 GMT
VOLUME [/data]
# Fri, 08 May 2026 19:36:35 GMT
WORKDIR /data
# Fri, 08 May 2026 19:36:35 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 08 May 2026 19:36:35 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008686a7c703c914115ea0c85877764c6ef3ef40df8a0ec96c1b449eecb0b9bd`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 9.6 MB (9629636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6ff60a4ba799ab9025e0b99743829d490a7e021e0cbde7aa64670d5efbb5da`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 2.7 KB (2672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fa0892b7f895e51796d00e79259613b40d439285ec7a96bea52e27a92a2017`  
		Last Modified: Fri, 08 May 2026 19:36:43 GMT  
		Size: 9.4 MB (9362961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5ecdd83a3e0130849b0f770b6511b27fa5d6d4d55d7cf9754b34f1417365fb`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:59444f28d1005b9f738081badfac33e5d75f22978ebab9b0e5ef9e4903e7d6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f7cf0c623491b6b0b0b0d7ca1fa24211aaa8cf0e60a8ed38d21796713027ef`

```dockerfile
```

-	Layers:
	-	`sha256:1039c022f54b90684969ded63b1c65825dc7f362dce123bd9e4a07f5de7d5047`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:616418d243a44e68ca534809dc3f62061612fe821c6a24d080770b73d11489e3`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.4-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:ae0a1a1dc9d60a1489c1e3de485db0b79bb6850e982bdbc0578ef03df8b610c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45496570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455656e6c9b6e39b6fb1ab5a9b0ea929a78fbcb3f1e799cc269967c8da73df95`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:51:41 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:51:42 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Fri, 08 May 2026 20:51:47 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Fri, 08 May 2026 20:51:47 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:51:47 GMT
VOLUME [/data]
# Fri, 08 May 2026 20:51:47 GMT
WORKDIR /data
# Fri, 08 May 2026 20:51:47 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 08 May 2026 20:51:47 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088b07e1d4ab6851c27e72ca04845c64afb9e2e874810b60c7d7ee315087f078`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 9.3 MB (9298427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cf8b3ac1199ea21d4bee7ac7fe307e373b7f82ebfc12cac84937a3530314c9`  
		Last Modified: Fri, 08 May 2026 20:52:00 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9429beadbe53e7cc00504d69272fd52a73280b0b4bcd141d43d91e50ed5bb23e`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 9.3 MB (9303780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da307de32ecd3c2ca014572ee61a176728536770780dd50d1dea146cbe7d1f1d`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:923cedeaf12a838f49051d8f4c54712822cd6c237da03f9735be44c056f68708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248009493c8e501134086960f3c13eec9a35942321ea589e02e9ed888adc2e80`

```dockerfile
```

-	Layers:
	-	`sha256:bda4b75a16269d180e761c8b60f265f5a629bc501619a49c801bdf42d45b0c6f`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c550857a14d97696e3b3318780c7e115cbf73e3cdfbaec81edaa7934b69e2b5`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:bookworm-slim`

```console
$ docker pull rethinkdb@sha256:0bc26dd1ddcc98daa59ce2b8d411a612e83fd69939c61a516b1a239ed40c3f87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:65ef63b04a02288f9b7da0c33b72ce005f4628cf255eecb8dce2962aef253e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48032601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348a73cb65421607e53298dfa8ba2eb75d76c498b02e34b7a3f5aabfe80cec58`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:34:52 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:34:53 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Fri, 08 May 2026 19:34:59 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Fri, 08 May 2026 19:34:59 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:34:59 GMT
VOLUME [/data]
# Fri, 08 May 2026 19:34:59 GMT
WORKDIR /data
# Fri, 08 May 2026 19:34:59 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 08 May 2026 19:34:59 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be42315b74021fc821e3d4f8dea28bc96efa4566bc77d119be47c4a15b5d718`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 9.8 MB (9800379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90352bb79e31597db22e449a1099f44111c7179772a8e53703917b27a9524337`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e75085611ad52c683edddc2974803ee701e1ef8e6cbc8fcc1732d604df55b`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 10.0 MB (9993177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9460c31950998ea3065b9e1eed7e7963d15dfd8c2f329dc4d90aace6e47462fa`  
		Last Modified: Fri, 08 May 2026 19:35:05 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:bdba3937f096a4aef1f4f53582fcfb397fe5323af6a28934942d054926ee9dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0a484b1cefe9f6ecb2d602ec1887c044b5ce7d5d57f49047658614aebf5077`

```dockerfile
```

-	Layers:
	-	`sha256:52fa4a02b9688d6dd2be556f1e87d263d31e2ade80948dfec07f114b69439c58`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51bf7af16f16a82790238619e2fcfbf2b230947887b860e59f69985703e09b71`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:c57d246b12b6bdac8d00af576810c3329a460e6d262a61db87aab1255456604f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47111528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582739fdd9909b17297270b551db471f03e47a396ff37c61ae3035fdf6639cd8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:36:29 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:36:30 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Fri, 08 May 2026 19:36:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Fri, 08 May 2026 19:36:35 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:36:35 GMT
VOLUME [/data]
# Fri, 08 May 2026 19:36:35 GMT
WORKDIR /data
# Fri, 08 May 2026 19:36:35 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 08 May 2026 19:36:35 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008686a7c703c914115ea0c85877764c6ef3ef40df8a0ec96c1b449eecb0b9bd`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 9.6 MB (9629636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6ff60a4ba799ab9025e0b99743829d490a7e021e0cbde7aa64670d5efbb5da`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 2.7 KB (2672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fa0892b7f895e51796d00e79259613b40d439285ec7a96bea52e27a92a2017`  
		Last Modified: Fri, 08 May 2026 19:36:43 GMT  
		Size: 9.4 MB (9362961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5ecdd83a3e0130849b0f770b6511b27fa5d6d4d55d7cf9754b34f1417365fb`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:59444f28d1005b9f738081badfac33e5d75f22978ebab9b0e5ef9e4903e7d6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f7cf0c623491b6b0b0b0d7ca1fa24211aaa8cf0e60a8ed38d21796713027ef`

```dockerfile
```

-	Layers:
	-	`sha256:1039c022f54b90684969ded63b1c65825dc7f362dce123bd9e4a07f5de7d5047`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:616418d243a44e68ca534809dc3f62061612fe821c6a24d080770b73d11489e3`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:ae0a1a1dc9d60a1489c1e3de485db0b79bb6850e982bdbc0578ef03df8b610c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45496570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455656e6c9b6e39b6fb1ab5a9b0ea929a78fbcb3f1e799cc269967c8da73df95`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:51:41 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:51:42 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Fri, 08 May 2026 20:51:47 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Fri, 08 May 2026 20:51:47 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:51:47 GMT
VOLUME [/data]
# Fri, 08 May 2026 20:51:47 GMT
WORKDIR /data
# Fri, 08 May 2026 20:51:47 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 08 May 2026 20:51:47 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088b07e1d4ab6851c27e72ca04845c64afb9e2e874810b60c7d7ee315087f078`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 9.3 MB (9298427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cf8b3ac1199ea21d4bee7ac7fe307e373b7f82ebfc12cac84937a3530314c9`  
		Last Modified: Fri, 08 May 2026 20:52:00 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9429beadbe53e7cc00504d69272fd52a73280b0b4bcd141d43d91e50ed5bb23e`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 9.3 MB (9303780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da307de32ecd3c2ca014572ee61a176728536770780dd50d1dea146cbe7d1f1d`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:923cedeaf12a838f49051d8f4c54712822cd6c237da03f9735be44c056f68708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248009493c8e501134086960f3c13eec9a35942321ea589e02e9ed888adc2e80`

```dockerfile
```

-	Layers:
	-	`sha256:bda4b75a16269d180e761c8b60f265f5a629bc501619a49c801bdf42d45b0c6f`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c550857a14d97696e3b3318780c7e115cbf73e3cdfbaec81edaa7934b69e2b5`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:0bc26dd1ddcc98daa59ce2b8d411a612e83fd69939c61a516b1a239ed40c3f87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:65ef63b04a02288f9b7da0c33b72ce005f4628cf255eecb8dce2962aef253e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48032601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348a73cb65421607e53298dfa8ba2eb75d76c498b02e34b7a3f5aabfe80cec58`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:34:52 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:34:53 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Fri, 08 May 2026 19:34:59 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Fri, 08 May 2026 19:34:59 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:34:59 GMT
VOLUME [/data]
# Fri, 08 May 2026 19:34:59 GMT
WORKDIR /data
# Fri, 08 May 2026 19:34:59 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 08 May 2026 19:34:59 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be42315b74021fc821e3d4f8dea28bc96efa4566bc77d119be47c4a15b5d718`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 9.8 MB (9800379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90352bb79e31597db22e449a1099f44111c7179772a8e53703917b27a9524337`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e75085611ad52c683edddc2974803ee701e1ef8e6cbc8fcc1732d604df55b`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 10.0 MB (9993177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9460c31950998ea3065b9e1eed7e7963d15dfd8c2f329dc4d90aace6e47462fa`  
		Last Modified: Fri, 08 May 2026 19:35:05 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:bdba3937f096a4aef1f4f53582fcfb397fe5323af6a28934942d054926ee9dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0a484b1cefe9f6ecb2d602ec1887c044b5ce7d5d57f49047658614aebf5077`

```dockerfile
```

-	Layers:
	-	`sha256:52fa4a02b9688d6dd2be556f1e87d263d31e2ade80948dfec07f114b69439c58`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51bf7af16f16a82790238619e2fcfbf2b230947887b860e59f69985703e09b71`  
		Last Modified: Fri, 08 May 2026 19:35:06 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:c57d246b12b6bdac8d00af576810c3329a460e6d262a61db87aab1255456604f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47111528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582739fdd9909b17297270b551db471f03e47a396ff37c61ae3035fdf6639cd8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:36:29 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:36:30 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Fri, 08 May 2026 19:36:35 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Fri, 08 May 2026 19:36:35 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:36:35 GMT
VOLUME [/data]
# Fri, 08 May 2026 19:36:35 GMT
WORKDIR /data
# Fri, 08 May 2026 19:36:35 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 08 May 2026 19:36:35 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008686a7c703c914115ea0c85877764c6ef3ef40df8a0ec96c1b449eecb0b9bd`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 9.6 MB (9629636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6ff60a4ba799ab9025e0b99743829d490a7e021e0cbde7aa64670d5efbb5da`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 2.7 KB (2672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fa0892b7f895e51796d00e79259613b40d439285ec7a96bea52e27a92a2017`  
		Last Modified: Fri, 08 May 2026 19:36:43 GMT  
		Size: 9.4 MB (9362961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5ecdd83a3e0130849b0f770b6511b27fa5d6d4d55d7cf9754b34f1417365fb`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:59444f28d1005b9f738081badfac33e5d75f22978ebab9b0e5ef9e4903e7d6c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f7cf0c623491b6b0b0b0d7ca1fa24211aaa8cf0e60a8ed38d21796713027ef`

```dockerfile
```

-	Layers:
	-	`sha256:1039c022f54b90684969ded63b1c65825dc7f362dce123bd9e4a07f5de7d5047`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:616418d243a44e68ca534809dc3f62061612fe821c6a24d080770b73d11489e3`  
		Last Modified: Fri, 08 May 2026 19:36:42 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; s390x

```console
$ docker pull rethinkdb@sha256:ae0a1a1dc9d60a1489c1e3de485db0b79bb6850e982bdbc0578ef03df8b610c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45496570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455656e6c9b6e39b6fb1ab5a9b0ea929a78fbcb3f1e799cc269967c8da73df95`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:51:41 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:51:42 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Fri, 08 May 2026 20:51:47 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Fri, 08 May 2026 20:51:47 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:51:47 GMT
VOLUME [/data]
# Fri, 08 May 2026 20:51:47 GMT
WORKDIR /data
# Fri, 08 May 2026 20:51:47 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 08 May 2026 20:51:47 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088b07e1d4ab6851c27e72ca04845c64afb9e2e874810b60c7d7ee315087f078`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 9.3 MB (9298427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cf8b3ac1199ea21d4bee7ac7fe307e373b7f82ebfc12cac84937a3530314c9`  
		Last Modified: Fri, 08 May 2026 20:52:00 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9429beadbe53e7cc00504d69272fd52a73280b0b4bcd141d43d91e50ed5bb23e`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 9.3 MB (9303780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da307de32ecd3c2ca014572ee61a176728536770780dd50d1dea146cbe7d1f1d`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:923cedeaf12a838f49051d8f4c54712822cd6c237da03f9735be44c056f68708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248009493c8e501134086960f3c13eec9a35942321ea589e02e9ed888adc2e80`

```dockerfile
```

-	Layers:
	-	`sha256:bda4b75a16269d180e761c8b60f265f5a629bc501619a49c801bdf42d45b0c6f`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c550857a14d97696e3b3318780c7e115cbf73e3cdfbaec81edaa7934b69e2b5`  
		Last Modified: Fri, 08 May 2026 20:52:01 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json
