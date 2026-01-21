## `rethinkdb:2-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:2bf57c7fe70f1703393285be7ea743e876bb31f31304206124d03bddc4ad7f3c
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
$ docker pull rethinkdb@sha256:efc649d68880fde5db602b7ae7e443b26bf228b9e4c9a2030be8d38bf587e46f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48023059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1593843ed0b26d260f37c64ec67c1d4a97042e37dae9562d8a78e7cda49881d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:03:22 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:03:23 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 13 Jan 2026 02:03:28 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 13 Jan 2026 02:03:28 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:03:28 GMT
VOLUME [/data]
# Tue, 13 Jan 2026 02:03:28 GMT
WORKDIR /data
# Tue, 13 Jan 2026 02:03:28 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 13 Jan 2026 02:03:28 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f133c90bc86e830f88b7bcadac5d93db2a73f3e819c2343f6c6b83e7c42e96`  
		Last Modified: Tue, 13 Jan 2026 02:03:42 GMT  
		Size: 9.8 MB (9798649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e069fa8ec988543278e6e414ec2811af1283faee216f3fb659d0bb437df14d3`  
		Last Modified: Tue, 13 Jan 2026 02:03:41 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552f379d6cc9f691eece9254dabd40eeae15ebdef5775f68ebd9aab4d7ef5db3`  
		Last Modified: Tue, 13 Jan 2026 02:03:42 GMT  
		Size: 10.0 MB (9993077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a12d4dca08a14cffee32c42679cbe2bb10d5f785535574b29a17ed15c23456`  
		Last Modified: Tue, 13 Jan 2026 02:03:41 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:ab226c32d903861788cd6ae170edaaa353955f6c586ff00db668d576c1d5613f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4812b502d60da243dbe80499cb1edcaf462ad2b86fa4db429c71ae081057827`

```dockerfile
```

-	Layers:
	-	`sha256:d52b4389a1f0002c89958382fe8375259852266905f6e4b3ceb8e6691ab498f9`  
		Last Modified: Tue, 13 Jan 2026 05:03:37 GMT  
		Size: 2.8 MB (2785046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c626efe821ddde01e61f80e8e86f65f17991b1c7c1c592af6138f532923e8659`  
		Last Modified: Tue, 13 Jan 2026 05:03:37 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:e61ee69c517af0b84c54f34667eac035df120b62b524b6643e90c5c044ea5e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47102147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aabd34f2b681ed7f268d3cf4b0f222812cf24e7ba833e3e90b44a4763f51ed1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:09:04 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:09:05 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 13 Jan 2026 02:09:10 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 13 Jan 2026 02:09:10 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:09:10 GMT
VOLUME [/data]
# Tue, 13 Jan 2026 02:09:10 GMT
WORKDIR /data
# Tue, 13 Jan 2026 02:09:10 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 13 Jan 2026 02:09:10 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2f7ebce60574b9eaf32c4aedf30042064ee09d9cbb64c9b79f6f656f364d95`  
		Last Modified: Tue, 13 Jan 2026 02:09:27 GMT  
		Size: 9.6 MB (9628500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6358aaa4c8bb733767f54a5746a2086944512978ea1d7e4996a87a7c3008168c`  
		Last Modified: Tue, 13 Jan 2026 02:09:26 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d271cfdcba3da61dc729e8dee4ef6946bbca0d7e103571f8dca3a70dd1b1b4c5`  
		Last Modified: Tue, 13 Jan 2026 02:09:19 GMT  
		Size: 9.4 MB (9362997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ac5c2d4bf93c087587e2bf7db7449c6cccb37a8cb28fcb0777afe8bb12f303`  
		Last Modified: Tue, 13 Jan 2026 02:09:26 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:4fdea369d9c9cf8f7aa68a43208c9f685076e57a2e652987f94cd53ddbfe6de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1cc70858cb691c5f3cd07cfada4ba737fe88d2c373b2a6663587e10e8c99091`

```dockerfile
```

-	Layers:
	-	`sha256:e98c680b3ba03f9ff3da68c23de94f748ddd9827c99d746c8cf66500e26624ac`  
		Last Modified: Tue, 13 Jan 2026 05:03:42 GMT  
		Size: 2.8 MB (2785381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae5ac6f37241ba626cdb766b37a14fa53ad5c717fbe03601759d139dcb2c26a9`  
		Last Modified: Tue, 13 Jan 2026 02:09:19 GMT  
		Size: 13.6 KB (13585 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:c313ea3e7cfd52265bbc727b6a605ac5c623bf235382907dabc41b29a394b7d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45488055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0bf544ee7b971b11f7560123fb482b4b2720467b5159f4abef640a199357ab8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:10 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:08:11 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 13 Jan 2026 02:08:16 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 13 Jan 2026 02:08:16 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:08:16 GMT
VOLUME [/data]
# Tue, 13 Jan 2026 02:08:16 GMT
WORKDIR /data
# Tue, 13 Jan 2026 02:08:16 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 13 Jan 2026 02:08:16 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5213af6f86a4b50993097752db36d4a2507c96069dc31c9f4893b24c3872a8ca`  
		Last Modified: Tue, 13 Jan 2026 02:08:28 GMT  
		Size: 9.3 MB (9297088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c166cffdd421f3f723bb7355b79fd3298125d06ba92679fe687327f5078d18`  
		Last Modified: Tue, 13 Jan 2026 02:08:32 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3651a1889bddf7cb328b27ead9eba7114c3becf65467bb198da1a366be2ab9`  
		Last Modified: Tue, 13 Jan 2026 02:08:36 GMT  
		Size: 9.3 MB (9303790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b23b3842acedf8ab84d4ec67a0880029efe23d444a92264dc36d47b694e4c5`  
		Last Modified: Tue, 13 Jan 2026 02:08:32 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:3ce1df9adf274a1e87ec0d8140d7fffedf8517ee595ae1a8f3be6735f9ff11bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ae0480b2cb888f1b13d2267289dc67f039adfb29b95a010984cc70ab3c225b`

```dockerfile
```

-	Layers:
	-	`sha256:85e7323da23c4fe7342507de305516e84c5e078c94a78a08a85ac652e22788fa`  
		Last Modified: Tue, 13 Jan 2026 05:03:53 GMT  
		Size: 2.8 MB (2781248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9705464e74edb398ef4b487c4a03884aad3f3c76200d63534e8430e3d2d7f56`  
		Last Modified: Tue, 13 Jan 2026 02:08:27 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json
