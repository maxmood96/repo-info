## `rethinkdb:2-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:5f0cf448b27877974cf0d3b3eb73e95aba497627285e03cf84d6239116883915
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
$ docker pull rethinkdb@sha256:8114ead12c7e17f7765784a417dec971f03609268872e04574f2426f223ac4f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48022709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b13de971baf4c87ba337709dc14746809cf80a4172a905081e31fc100cb4ed4`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc2cbdc68100f2fdbb0378a8f62a115e71d1fb73cfa5b6b81e77325c7ad8b4e`  
		Last Modified: Tue, 12 Aug 2025 21:20:49 GMT  
		Size: 9.8 MB (9796835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe40f036027d2444a30a15f19d55e8938a247f048d4710bd00bf5c33223e8b5`  
		Last Modified: Tue, 12 Aug 2025 21:20:48 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f03c42d9655dfce6213e9e4e1ff62782c8124eff6d12a00af8e2b01320f85c`  
		Last Modified: Tue, 12 Aug 2025 21:20:50 GMT  
		Size: 10.0 MB (9992858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c06effb108b36432f4031908a32541ac0ee3076def1aaf34f42fe8e2cd74789`  
		Last Modified: Tue, 12 Aug 2025 21:20:49 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:c6ec6806113d99eb3c28725153330338705740ad95992c01c9a7d6ebd814f75c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2796188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c796cb92e51eafd7e49b584b92e37db89f35a8cca72a1da650f39190e8950c`

```dockerfile
```

-	Layers:
	-	`sha256:ba53be01829fd98c7060083d8fcead392d441cd5b4e6db56ef2135191ea67a01`  
		Last Modified: Wed, 13 Aug 2025 01:03:21 GMT  
		Size: 2.8 MB (2782741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:536ff781462371706e8f4baecba7969efd6b5c475940a6c8c78d1033dfe728b5`  
		Last Modified: Wed, 13 Aug 2025 01:03:22 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:0141ef41d82bd0ea87b95f9e663effda9defaf04b181635e5d5a01fbd48eef0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47052586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea8cdcba4a057e80b179d1486dbf6d512d6edbb709969da2af7d1b58315d74a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73832e827844c78187df7ba572afb19e49a77454baf06a21c9ae04ef01df5c5b`  
		Last Modified: Wed, 13 Aug 2025 08:25:09 GMT  
		Size: 9.6 MB (9605224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe0237cd185f21205c78b0c266ec0b6aec88a931ce8b88a25df316b82bb6821`  
		Last Modified: Wed, 13 Aug 2025 06:25:36 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaefb1f2707014df99aeedcfe2c1f0a9f2c7caa382e53a23a15f2210124cb8c`  
		Last Modified: Wed, 13 Aug 2025 08:25:15 GMT  
		Size: 9.4 MB (9362599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02193880b48ed47b7c96688c867fe310636d65d221e938478ca449d73ee60385`  
		Last Modified: Wed, 13 Aug 2025 07:16:19 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:f2db00d7250bbc937d88aa389fd8f3d095a7fcf3042e463d8a153d7d331d039a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2796705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e8b1a05f95393ed64f930676c0dccb63b892ff3d58774cdea154dd294c15a5`

```dockerfile
```

-	Layers:
	-	`sha256:a8907ff0372f5c9efa3fc886adfcd617ff1b6fde8bc17e0e882372c46731e0a7`  
		Last Modified: Wed, 13 Aug 2025 10:05:58 GMT  
		Size: 2.8 MB (2783076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91e8ee80c9bbd7f67797c61741c12d70bed9d40c744ca24e3348f202b9e2ebfb`  
		Last Modified: Wed, 13 Aug 2025 10:05:59 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:f232a0464d5b06ee698634922919347e81edcb884e85fc25927753344ed5ca13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45490457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c783018ef1bc553dec6a55f0924baf95939e15c2449653ad878b3446bc55e3`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcd982b4bef14960c940dd5cd6199d3647f190228d258368f074148ed925a25`  
		Last Modified: Wed, 13 Aug 2025 16:05:12 GMT  
		Size: 9.3 MB (9296291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed36af31e11ddb4d00c3e2f12c34e86d8d1aa302d906bda23f8667fb7a189d40`  
		Last Modified: Wed, 13 Aug 2025 15:15:53 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b0a2e8a6959025b56fdf5b3d8797937670a13506964b8fba526c1088ad66a0`  
		Last Modified: Wed, 13 Aug 2025 16:05:15 GMT  
		Size: 9.3 MB (9303567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16993a444890f42435e2ccf2b80c3d3df7c683d18dbf571938d386a410b35e15`  
		Last Modified: Wed, 13 Aug 2025 15:15:59 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:a501a7cfdbd43b58380829850ad551eea7ac27ac4803c9f7b82c7ee98c466d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2792390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4148be9b93b6f6ae1a5a17b3ba4a2dcf97812394ee9279f780d78701af8b4652`

```dockerfile
```

-	Layers:
	-	`sha256:653325a5cb0011ae03fa0679c7b9ea16500d39921064821b5d675012c04167f7`  
		Last Modified: Wed, 13 Aug 2025 16:03:26 GMT  
		Size: 2.8 MB (2778943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5748493c941c7cc0f7b1f61216bfc163e82eca6f7be95f6b509a224dc881710b`  
		Last Modified: Wed, 13 Aug 2025 16:03:26 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json
