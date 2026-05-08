## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:a3e39303c509e73fcf22cf1ba829d6d1df9f0573d965e7199bc6c2c4f1485e6e
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
$ docker pull rethinkdb@sha256:2086aa8a67c9ae1077595bb071e54edf7b1b64eec7b98dfe3785e5065be13f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48032501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d96800e66a266e558089cd86156e521f716dc44a114dd74f50d4184e9bc18092`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:34:25 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:34:26 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 22 Apr 2026 01:34:32 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 22 Apr 2026 01:34:32 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:34:32 GMT
VOLUME [/data]
# Wed, 22 Apr 2026 01:34:32 GMT
WORKDIR /data
# Wed, 22 Apr 2026 01:34:32 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 22 Apr 2026 01:34:32 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e958ea025e14b511e3326e816bcb82096261cd0d8a2d6ef6f2fa68a97e3293b9`  
		Last Modified: Wed, 22 Apr 2026 01:34:39 GMT  
		Size: 9.8 MB (9800360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fa9ab09fa87148e4a53b34ce4342170a36f3661ad11f1eedabfda29ab212b8`  
		Last Modified: Wed, 22 Apr 2026 01:34:39 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1e04e76e6e04b2043bff8943b9b99de874b3bc691bc815f5742938f8705f4d`  
		Last Modified: Wed, 22 Apr 2026 01:34:39 GMT  
		Size: 10.0 MB (9993128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19be2c8a48203b245dcff292f6a1f48570b52dd7bc3b0c0d55e9f133600331b`  
		Last Modified: Wed, 22 Apr 2026 01:34:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:2598a2906c610e237e41f9d4414d441db2a85567d4587ea6550e1b484618df88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928ecaf366154c9a9083977ef01a4f91c3769ff05399a3a51f343afb6dac5793`

```dockerfile
```

-	Layers:
	-	`sha256:1bac12430332c225cca7407d94ec4380be1fa74c99f52feb755146fe6bfb1d08`  
		Last Modified: Wed, 22 Apr 2026 01:34:39 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71670eac4b0f8b04a3afc7d767169a0acf95a2f9221c81ff26cf0b2ccf51d291`  
		Last Modified: Wed, 22 Apr 2026 01:34:39 GMT  
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
$ docker pull rethinkdb@sha256:05fd8ea89a2795d5afdeb8a59b90908ec267d92a5ebe76523db790a22c1082c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45496465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdb0aace22c0968d06fcf1956b553281978bf122b67ce8dce534dec569a0d80`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:31:01 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:31:03 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 22 Apr 2026 02:31:07 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 22 Apr 2026 02:31:07 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:31:07 GMT
VOLUME [/data]
# Wed, 22 Apr 2026 02:31:07 GMT
WORKDIR /data
# Wed, 22 Apr 2026 02:31:07 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 22 Apr 2026 02:31:07 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746bd5cd5771084cb5653941da7bafb70c3df721ed2afd64c3553c4fdb229060`  
		Last Modified: Wed, 22 Apr 2026 02:31:21 GMT  
		Size: 9.3 MB (9298370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63218eed7f5c56fd5bc12e7f7c2c23180471af9e4f26fa2ddfaa2f1a69bfdb89`  
		Last Modified: Wed, 22 Apr 2026 02:31:20 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23203512060223d3da20bd0b12133a8ccc28df4c0fe67021fe7220f70d621e3c`  
		Last Modified: Wed, 22 Apr 2026 02:31:21 GMT  
		Size: 9.3 MB (9303770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8663632e5b8bb3e46df0e6d933af14d230a36aec9dbcc198312d3040defbaabc`  
		Last Modified: Wed, 22 Apr 2026 02:31:20 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:d9740f237b8568d789bc8791e4657e7e9b68e68a6b30119ff834a456dd9eb3c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227b5e348691bad1a2dd27ef14e4bb1ee0df30102ce9461236e2da075d2014b0`

```dockerfile
```

-	Layers:
	-	`sha256:735c804ff5119b9f3c125677c7e60394ab74c3860074e40aafd194ba874ad7dd`  
		Last Modified: Wed, 22 Apr 2026 02:31:21 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:995ad82df86d9d59d4de0d395423c1511c1c315a912cc1e7fcdcbd49448b56b2`  
		Last Modified: Wed, 22 Apr 2026 02:31:20 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json
