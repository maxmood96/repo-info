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
$ docker pull rethinkdb@sha256:6773003a0539d9f6df5f3e0eac90364bf519ddb08548bc76e787fa510df14e54
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
$ docker pull rethinkdb@sha256:146a49694f822cb25c2db9064eb0824c7e7ec3c8e14aca3bafd32e2966be3d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48014493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3967c6dced81d604b0ea5731a04ef075ecd7a5d3ad5fb3d46f885be0ac9edec8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1368caeec38d860ab14fd21f6273c2e65a1982c822d09214dbc987d42dbf609`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 9.8 MB (9791220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b23cb4883335dded490789b5187dc0a9d029e0facbed093a8c0a3f340602ca`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81989d522b62d14a4851ad1ca31704bfd8160054c84081806c46d7341a1f63e9`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 10.0 MB (9992868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36d4f3cbe3d3334572b5b24719f8396b6eadbecce3d65f55119541d7faca87d`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:433027607d1280864b3334bf89982c71eecf7c3fbf682d6a8067b7279829c877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6245972b18ad63665bf9429702af047c588cf5cb743a501ad1101ea60be32f22`

```dockerfile
```

-	Layers:
	-	`sha256:bffcaa740af81c1547444a699457668a016f2ae751bb7ce5fbf7677f5aad31df`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 2.6 MB (2627495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc8e665ffb08a9af6b3c2afc7bf5c482e0cd83bf86e9972d2efa283b12c2bf7`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:db72dc143498796e01d4226d4e2ac3978b48867b541cb823d70904e299824fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47020879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8dd10f87ce1b32d7d27efa40471fb6376967e2e916dad670828b6da6f81b23b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315fe6fed3515ab7ce2e7d3d32ff0be4238c8c82746470392aa876a5641240e1`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 9.6 MB (9588958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165fdf7199a783cb2efe62c25bba9a645cbf4f337155599884e155221950ae78`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e43d85ff9417cdc42920fa0cae03ea0d12ed72ed4934fbf58c9eaab1cb1817`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 9.4 MB (9362540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f35f2e0e1738b3ce469c9961a459ad7ca82f5202da5183f3ec7f5335ae14f4`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:a189e231c4edc1140651af9a6c572a4abf91511ec1474645137890fd44175b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2641459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfedd8acbc43cdd15bb55cc7d4247290471f07b52d5da80adcfe5c8c582e728`

```dockerfile
```

-	Layers:
	-	`sha256:3752ef92f8cacf48d095a37b24e8d26aa6b620da1690f0a7f9de8fdff50415fb`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 2.6 MB (2627830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c2cfc052a1f907ca28c4774d3f93b2f95e6c8e0affca9ce5ac2b30516a04fc`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2` - linux; s390x

```console
$ docker pull rethinkdb@sha256:af53c5fd68b00c68f10bdf45a2a0722f21145198568dea4e234cd29a203ed104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45481049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074879bc8f8fb73a2e0e5c673f899a1f0828155d7cb6438155ca325e9fdb71f1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d786d8441cb12eabd778b4fd3cd47545cf3438274298d60dc913795a4f0bebbe`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 9.3 MB (9289921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ba1c4b3d5eed0f37eae81343bf7ce6567d4b0ed8bd27ce279b931260b52e93`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80796e21756c240d7813b94da57b6bcac341e952f53f3074d48d063aae1dfcb`  
		Last Modified: Mon, 28 Apr 2025 23:52:48 GMT  
		Size: 9.3 MB (9303501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a43adfa4ee7447040e90c8c064b759cb333d0f3708f001e876a681163fb64b`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:ea14c11c9ceb121f78905c25f3e957584210f040fbf45663d752578eeb75c832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd86054f23353807a35ef0654a0954c73e035e293bca3105502f8d999bb57ff`

```dockerfile
```

-	Layers:
	-	`sha256:558fbcefee003feb767420c7c9f16e24bb3c53c98d0b2268fae98ea2eefe3764`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 2.6 MB (2626589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f599bc6bfca25763bad00cd6cabed025519d888b29a5fc013af803be0cf9a7e`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:6773003a0539d9f6df5f3e0eac90364bf519ddb08548bc76e787fa510df14e54
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
$ docker pull rethinkdb@sha256:146a49694f822cb25c2db9064eb0824c7e7ec3c8e14aca3bafd32e2966be3d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48014493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3967c6dced81d604b0ea5731a04ef075ecd7a5d3ad5fb3d46f885be0ac9edec8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1368caeec38d860ab14fd21f6273c2e65a1982c822d09214dbc987d42dbf609`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 9.8 MB (9791220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b23cb4883335dded490789b5187dc0a9d029e0facbed093a8c0a3f340602ca`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81989d522b62d14a4851ad1ca31704bfd8160054c84081806c46d7341a1f63e9`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 10.0 MB (9992868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36d4f3cbe3d3334572b5b24719f8396b6eadbecce3d65f55119541d7faca87d`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:433027607d1280864b3334bf89982c71eecf7c3fbf682d6a8067b7279829c877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6245972b18ad63665bf9429702af047c588cf5cb743a501ad1101ea60be32f22`

```dockerfile
```

-	Layers:
	-	`sha256:bffcaa740af81c1547444a699457668a016f2ae751bb7ce5fbf7677f5aad31df`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 2.6 MB (2627495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc8e665ffb08a9af6b3c2afc7bf5c482e0cd83bf86e9972d2efa283b12c2bf7`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:db72dc143498796e01d4226d4e2ac3978b48867b541cb823d70904e299824fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47020879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8dd10f87ce1b32d7d27efa40471fb6376967e2e916dad670828b6da6f81b23b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315fe6fed3515ab7ce2e7d3d32ff0be4238c8c82746470392aa876a5641240e1`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 9.6 MB (9588958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165fdf7199a783cb2efe62c25bba9a645cbf4f337155599884e155221950ae78`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e43d85ff9417cdc42920fa0cae03ea0d12ed72ed4934fbf58c9eaab1cb1817`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 9.4 MB (9362540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f35f2e0e1738b3ce469c9961a459ad7ca82f5202da5183f3ec7f5335ae14f4`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:a189e231c4edc1140651af9a6c572a4abf91511ec1474645137890fd44175b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2641459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfedd8acbc43cdd15bb55cc7d4247290471f07b52d5da80adcfe5c8c582e728`

```dockerfile
```

-	Layers:
	-	`sha256:3752ef92f8cacf48d095a37b24e8d26aa6b620da1690f0a7f9de8fdff50415fb`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 2.6 MB (2627830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c2cfc052a1f907ca28c4774d3f93b2f95e6c8e0affca9ce5ac2b30516a04fc`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:af53c5fd68b00c68f10bdf45a2a0722f21145198568dea4e234cd29a203ed104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45481049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074879bc8f8fb73a2e0e5c673f899a1f0828155d7cb6438155ca325e9fdb71f1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d786d8441cb12eabd778b4fd3cd47545cf3438274298d60dc913795a4f0bebbe`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 9.3 MB (9289921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ba1c4b3d5eed0f37eae81343bf7ce6567d4b0ed8bd27ce279b931260b52e93`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80796e21756c240d7813b94da57b6bcac341e952f53f3074d48d063aae1dfcb`  
		Last Modified: Mon, 28 Apr 2025 23:52:48 GMT  
		Size: 9.3 MB (9303501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a43adfa4ee7447040e90c8c064b759cb333d0f3708f001e876a681163fb64b`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:ea14c11c9ceb121f78905c25f3e957584210f040fbf45663d752578eeb75c832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd86054f23353807a35ef0654a0954c73e035e293bca3105502f8d999bb57ff`

```dockerfile
```

-	Layers:
	-	`sha256:558fbcefee003feb767420c7c9f16e24bb3c53c98d0b2268fae98ea2eefe3764`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 2.6 MB (2626589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f599bc6bfca25763bad00cd6cabed025519d888b29a5fc013af803be0cf9a7e`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:6773003a0539d9f6df5f3e0eac90364bf519ddb08548bc76e787fa510df14e54
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
$ docker pull rethinkdb@sha256:146a49694f822cb25c2db9064eb0824c7e7ec3c8e14aca3bafd32e2966be3d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48014493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3967c6dced81d604b0ea5731a04ef075ecd7a5d3ad5fb3d46f885be0ac9edec8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1368caeec38d860ab14fd21f6273c2e65a1982c822d09214dbc987d42dbf609`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 9.8 MB (9791220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b23cb4883335dded490789b5187dc0a9d029e0facbed093a8c0a3f340602ca`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81989d522b62d14a4851ad1ca31704bfd8160054c84081806c46d7341a1f63e9`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 10.0 MB (9992868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36d4f3cbe3d3334572b5b24719f8396b6eadbecce3d65f55119541d7faca87d`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:433027607d1280864b3334bf89982c71eecf7c3fbf682d6a8067b7279829c877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6245972b18ad63665bf9429702af047c588cf5cb743a501ad1101ea60be32f22`

```dockerfile
```

-	Layers:
	-	`sha256:bffcaa740af81c1547444a699457668a016f2ae751bb7ce5fbf7677f5aad31df`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 2.6 MB (2627495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc8e665ffb08a9af6b3c2afc7bf5c482e0cd83bf86e9972d2efa283b12c2bf7`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:db72dc143498796e01d4226d4e2ac3978b48867b541cb823d70904e299824fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47020879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8dd10f87ce1b32d7d27efa40471fb6376967e2e916dad670828b6da6f81b23b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315fe6fed3515ab7ce2e7d3d32ff0be4238c8c82746470392aa876a5641240e1`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 9.6 MB (9588958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165fdf7199a783cb2efe62c25bba9a645cbf4f337155599884e155221950ae78`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e43d85ff9417cdc42920fa0cae03ea0d12ed72ed4934fbf58c9eaab1cb1817`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 9.4 MB (9362540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f35f2e0e1738b3ce469c9961a459ad7ca82f5202da5183f3ec7f5335ae14f4`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:a189e231c4edc1140651af9a6c572a4abf91511ec1474645137890fd44175b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2641459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfedd8acbc43cdd15bb55cc7d4247290471f07b52d5da80adcfe5c8c582e728`

```dockerfile
```

-	Layers:
	-	`sha256:3752ef92f8cacf48d095a37b24e8d26aa6b620da1690f0a7f9de8fdff50415fb`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 2.6 MB (2627830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c2cfc052a1f907ca28c4774d3f93b2f95e6c8e0affca9ce5ac2b30516a04fc`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4` - linux; s390x

```console
$ docker pull rethinkdb@sha256:af53c5fd68b00c68f10bdf45a2a0722f21145198568dea4e234cd29a203ed104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45481049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074879bc8f8fb73a2e0e5c673f899a1f0828155d7cb6438155ca325e9fdb71f1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d786d8441cb12eabd778b4fd3cd47545cf3438274298d60dc913795a4f0bebbe`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 9.3 MB (9289921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ba1c4b3d5eed0f37eae81343bf7ce6567d4b0ed8bd27ce279b931260b52e93`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80796e21756c240d7813b94da57b6bcac341e952f53f3074d48d063aae1dfcb`  
		Last Modified: Mon, 28 Apr 2025 23:52:48 GMT  
		Size: 9.3 MB (9303501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a43adfa4ee7447040e90c8c064b759cb333d0f3708f001e876a681163fb64b`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:ea14c11c9ceb121f78905c25f3e957584210f040fbf45663d752578eeb75c832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd86054f23353807a35ef0654a0954c73e035e293bca3105502f8d999bb57ff`

```dockerfile
```

-	Layers:
	-	`sha256:558fbcefee003feb767420c7c9f16e24bb3c53c98d0b2268fae98ea2eefe3764`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 2.6 MB (2626589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f599bc6bfca25763bad00cd6cabed025519d888b29a5fc013af803be0cf9a7e`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:6773003a0539d9f6df5f3e0eac90364bf519ddb08548bc76e787fa510df14e54
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
$ docker pull rethinkdb@sha256:146a49694f822cb25c2db9064eb0824c7e7ec3c8e14aca3bafd32e2966be3d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48014493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3967c6dced81d604b0ea5731a04ef075ecd7a5d3ad5fb3d46f885be0ac9edec8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1368caeec38d860ab14fd21f6273c2e65a1982c822d09214dbc987d42dbf609`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 9.8 MB (9791220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b23cb4883335dded490789b5187dc0a9d029e0facbed093a8c0a3f340602ca`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81989d522b62d14a4851ad1ca31704bfd8160054c84081806c46d7341a1f63e9`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 10.0 MB (9992868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36d4f3cbe3d3334572b5b24719f8396b6eadbecce3d65f55119541d7faca87d`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:433027607d1280864b3334bf89982c71eecf7c3fbf682d6a8067b7279829c877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6245972b18ad63665bf9429702af047c588cf5cb743a501ad1101ea60be32f22`

```dockerfile
```

-	Layers:
	-	`sha256:bffcaa740af81c1547444a699457668a016f2ae751bb7ce5fbf7677f5aad31df`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 2.6 MB (2627495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc8e665ffb08a9af6b3c2afc7bf5c482e0cd83bf86e9972d2efa283b12c2bf7`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:db72dc143498796e01d4226d4e2ac3978b48867b541cb823d70904e299824fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47020879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8dd10f87ce1b32d7d27efa40471fb6376967e2e916dad670828b6da6f81b23b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315fe6fed3515ab7ce2e7d3d32ff0be4238c8c82746470392aa876a5641240e1`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 9.6 MB (9588958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165fdf7199a783cb2efe62c25bba9a645cbf4f337155599884e155221950ae78`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e43d85ff9417cdc42920fa0cae03ea0d12ed72ed4934fbf58c9eaab1cb1817`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 9.4 MB (9362540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f35f2e0e1738b3ce469c9961a459ad7ca82f5202da5183f3ec7f5335ae14f4`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:a189e231c4edc1140651af9a6c572a4abf91511ec1474645137890fd44175b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2641459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfedd8acbc43cdd15bb55cc7d4247290471f07b52d5da80adcfe5c8c582e728`

```dockerfile
```

-	Layers:
	-	`sha256:3752ef92f8cacf48d095a37b24e8d26aa6b620da1690f0a7f9de8fdff50415fb`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 2.6 MB (2627830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c2cfc052a1f907ca28c4774d3f93b2f95e6c8e0affca9ce5ac2b30516a04fc`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:af53c5fd68b00c68f10bdf45a2a0722f21145198568dea4e234cd29a203ed104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45481049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074879bc8f8fb73a2e0e5c673f899a1f0828155d7cb6438155ca325e9fdb71f1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d786d8441cb12eabd778b4fd3cd47545cf3438274298d60dc913795a4f0bebbe`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 9.3 MB (9289921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ba1c4b3d5eed0f37eae81343bf7ce6567d4b0ed8bd27ce279b931260b52e93`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80796e21756c240d7813b94da57b6bcac341e952f53f3074d48d063aae1dfcb`  
		Last Modified: Mon, 28 Apr 2025 23:52:48 GMT  
		Size: 9.3 MB (9303501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a43adfa4ee7447040e90c8c064b759cb333d0f3708f001e876a681163fb64b`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:ea14c11c9ceb121f78905c25f3e957584210f040fbf45663d752578eeb75c832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd86054f23353807a35ef0654a0954c73e035e293bca3105502f8d999bb57ff`

```dockerfile
```

-	Layers:
	-	`sha256:558fbcefee003feb767420c7c9f16e24bb3c53c98d0b2268fae98ea2eefe3764`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 2.6 MB (2626589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f599bc6bfca25763bad00cd6cabed025519d888b29a5fc013af803be0cf9a7e`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4.3`

```console
$ docker pull rethinkdb@sha256:6773003a0539d9f6df5f3e0eac90364bf519ddb08548bc76e787fa510df14e54
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
$ docker pull rethinkdb@sha256:146a49694f822cb25c2db9064eb0824c7e7ec3c8e14aca3bafd32e2966be3d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48014493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3967c6dced81d604b0ea5731a04ef075ecd7a5d3ad5fb3d46f885be0ac9edec8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1368caeec38d860ab14fd21f6273c2e65a1982c822d09214dbc987d42dbf609`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 9.8 MB (9791220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b23cb4883335dded490789b5187dc0a9d029e0facbed093a8c0a3f340602ca`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81989d522b62d14a4851ad1ca31704bfd8160054c84081806c46d7341a1f63e9`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 10.0 MB (9992868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36d4f3cbe3d3334572b5b24719f8396b6eadbecce3d65f55119541d7faca87d`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:433027607d1280864b3334bf89982c71eecf7c3fbf682d6a8067b7279829c877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6245972b18ad63665bf9429702af047c588cf5cb743a501ad1101ea60be32f22`

```dockerfile
```

-	Layers:
	-	`sha256:bffcaa740af81c1547444a699457668a016f2ae751bb7ce5fbf7677f5aad31df`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 2.6 MB (2627495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc8e665ffb08a9af6b3c2afc7bf5c482e0cd83bf86e9972d2efa283b12c2bf7`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.3` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:db72dc143498796e01d4226d4e2ac3978b48867b541cb823d70904e299824fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47020879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8dd10f87ce1b32d7d27efa40471fb6376967e2e916dad670828b6da6f81b23b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315fe6fed3515ab7ce2e7d3d32ff0be4238c8c82746470392aa876a5641240e1`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 9.6 MB (9588958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165fdf7199a783cb2efe62c25bba9a645cbf4f337155599884e155221950ae78`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e43d85ff9417cdc42920fa0cae03ea0d12ed72ed4934fbf58c9eaab1cb1817`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 9.4 MB (9362540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f35f2e0e1738b3ce469c9961a459ad7ca82f5202da5183f3ec7f5335ae14f4`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:a189e231c4edc1140651af9a6c572a4abf91511ec1474645137890fd44175b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2641459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfedd8acbc43cdd15bb55cc7d4247290471f07b52d5da80adcfe5c8c582e728`

```dockerfile
```

-	Layers:
	-	`sha256:3752ef92f8cacf48d095a37b24e8d26aa6b620da1690f0a7f9de8fdff50415fb`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 2.6 MB (2627830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c2cfc052a1f907ca28c4774d3f93b2f95e6c8e0affca9ce5ac2b30516a04fc`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.3` - linux; s390x

```console
$ docker pull rethinkdb@sha256:af53c5fd68b00c68f10bdf45a2a0722f21145198568dea4e234cd29a203ed104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45481049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074879bc8f8fb73a2e0e5c673f899a1f0828155d7cb6438155ca325e9fdb71f1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d786d8441cb12eabd778b4fd3cd47545cf3438274298d60dc913795a4f0bebbe`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 9.3 MB (9289921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ba1c4b3d5eed0f37eae81343bf7ce6567d4b0ed8bd27ce279b931260b52e93`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80796e21756c240d7813b94da57b6bcac341e952f53f3074d48d063aae1dfcb`  
		Last Modified: Mon, 28 Apr 2025 23:52:48 GMT  
		Size: 9.3 MB (9303501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a43adfa4ee7447040e90c8c064b759cb333d0f3708f001e876a681163fb64b`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:ea14c11c9ceb121f78905c25f3e957584210f040fbf45663d752578eeb75c832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd86054f23353807a35ef0654a0954c73e035e293bca3105502f8d999bb57ff`

```dockerfile
```

-	Layers:
	-	`sha256:558fbcefee003feb767420c7c9f16e24bb3c53c98d0b2268fae98ea2eefe3764`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 2.6 MB (2626589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f599bc6bfca25763bad00cd6cabed025519d888b29a5fc013af803be0cf9a7e`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4.4-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:6773003a0539d9f6df5f3e0eac90364bf519ddb08548bc76e787fa510df14e54
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
$ docker pull rethinkdb@sha256:146a49694f822cb25c2db9064eb0824c7e7ec3c8e14aca3bafd32e2966be3d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48014493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3967c6dced81d604b0ea5731a04ef075ecd7a5d3ad5fb3d46f885be0ac9edec8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1368caeec38d860ab14fd21f6273c2e65a1982c822d09214dbc987d42dbf609`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 9.8 MB (9791220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b23cb4883335dded490789b5187dc0a9d029e0facbed093a8c0a3f340602ca`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81989d522b62d14a4851ad1ca31704bfd8160054c84081806c46d7341a1f63e9`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 10.0 MB (9992868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36d4f3cbe3d3334572b5b24719f8396b6eadbecce3d65f55119541d7faca87d`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:433027607d1280864b3334bf89982c71eecf7c3fbf682d6a8067b7279829c877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6245972b18ad63665bf9429702af047c588cf5cb743a501ad1101ea60be32f22`

```dockerfile
```

-	Layers:
	-	`sha256:bffcaa740af81c1547444a699457668a016f2ae751bb7ce5fbf7677f5aad31df`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 2.6 MB (2627495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc8e665ffb08a9af6b3c2afc7bf5c482e0cd83bf86e9972d2efa283b12c2bf7`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.4-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:db72dc143498796e01d4226d4e2ac3978b48867b541cb823d70904e299824fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47020879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8dd10f87ce1b32d7d27efa40471fb6376967e2e916dad670828b6da6f81b23b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315fe6fed3515ab7ce2e7d3d32ff0be4238c8c82746470392aa876a5641240e1`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 9.6 MB (9588958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165fdf7199a783cb2efe62c25bba9a645cbf4f337155599884e155221950ae78`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e43d85ff9417cdc42920fa0cae03ea0d12ed72ed4934fbf58c9eaab1cb1817`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 9.4 MB (9362540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f35f2e0e1738b3ce469c9961a459ad7ca82f5202da5183f3ec7f5335ae14f4`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:a189e231c4edc1140651af9a6c572a4abf91511ec1474645137890fd44175b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2641459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfedd8acbc43cdd15bb55cc7d4247290471f07b52d5da80adcfe5c8c582e728`

```dockerfile
```

-	Layers:
	-	`sha256:3752ef92f8cacf48d095a37b24e8d26aa6b620da1690f0a7f9de8fdff50415fb`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 2.6 MB (2627830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c2cfc052a1f907ca28c4774d3f93b2f95e6c8e0affca9ce5ac2b30516a04fc`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.4-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:af53c5fd68b00c68f10bdf45a2a0722f21145198568dea4e234cd29a203ed104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45481049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074879bc8f8fb73a2e0e5c673f899a1f0828155d7cb6438155ca325e9fdb71f1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d786d8441cb12eabd778b4fd3cd47545cf3438274298d60dc913795a4f0bebbe`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 9.3 MB (9289921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ba1c4b3d5eed0f37eae81343bf7ce6567d4b0ed8bd27ce279b931260b52e93`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80796e21756c240d7813b94da57b6bcac341e952f53f3074d48d063aae1dfcb`  
		Last Modified: Mon, 28 Apr 2025 23:52:48 GMT  
		Size: 9.3 MB (9303501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a43adfa4ee7447040e90c8c064b759cb333d0f3708f001e876a681163fb64b`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:ea14c11c9ceb121f78905c25f3e957584210f040fbf45663d752578eeb75c832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd86054f23353807a35ef0654a0954c73e035e293bca3105502f8d999bb57ff`

```dockerfile
```

-	Layers:
	-	`sha256:558fbcefee003feb767420c7c9f16e24bb3c53c98d0b2268fae98ea2eefe3764`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 2.6 MB (2626589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f599bc6bfca25763bad00cd6cabed025519d888b29a5fc013af803be0cf9a7e`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:bookworm-slim`

```console
$ docker pull rethinkdb@sha256:6773003a0539d9f6df5f3e0eac90364bf519ddb08548bc76e787fa510df14e54
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
$ docker pull rethinkdb@sha256:146a49694f822cb25c2db9064eb0824c7e7ec3c8e14aca3bafd32e2966be3d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48014493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3967c6dced81d604b0ea5731a04ef075ecd7a5d3ad5fb3d46f885be0ac9edec8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1368caeec38d860ab14fd21f6273c2e65a1982c822d09214dbc987d42dbf609`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 9.8 MB (9791220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b23cb4883335dded490789b5187dc0a9d029e0facbed093a8c0a3f340602ca`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81989d522b62d14a4851ad1ca31704bfd8160054c84081806c46d7341a1f63e9`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 10.0 MB (9992868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36d4f3cbe3d3334572b5b24719f8396b6eadbecce3d65f55119541d7faca87d`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:433027607d1280864b3334bf89982c71eecf7c3fbf682d6a8067b7279829c877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6245972b18ad63665bf9429702af047c588cf5cb743a501ad1101ea60be32f22`

```dockerfile
```

-	Layers:
	-	`sha256:bffcaa740af81c1547444a699457668a016f2ae751bb7ce5fbf7677f5aad31df`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 2.6 MB (2627495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc8e665ffb08a9af6b3c2afc7bf5c482e0cd83bf86e9972d2efa283b12c2bf7`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:db72dc143498796e01d4226d4e2ac3978b48867b541cb823d70904e299824fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47020879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8dd10f87ce1b32d7d27efa40471fb6376967e2e916dad670828b6da6f81b23b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315fe6fed3515ab7ce2e7d3d32ff0be4238c8c82746470392aa876a5641240e1`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 9.6 MB (9588958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165fdf7199a783cb2efe62c25bba9a645cbf4f337155599884e155221950ae78`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e43d85ff9417cdc42920fa0cae03ea0d12ed72ed4934fbf58c9eaab1cb1817`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 9.4 MB (9362540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f35f2e0e1738b3ce469c9961a459ad7ca82f5202da5183f3ec7f5335ae14f4`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:a189e231c4edc1140651af9a6c572a4abf91511ec1474645137890fd44175b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2641459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfedd8acbc43cdd15bb55cc7d4247290471f07b52d5da80adcfe5c8c582e728`

```dockerfile
```

-	Layers:
	-	`sha256:3752ef92f8cacf48d095a37b24e8d26aa6b620da1690f0a7f9de8fdff50415fb`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 2.6 MB (2627830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c2cfc052a1f907ca28c4774d3f93b2f95e6c8e0affca9ce5ac2b30516a04fc`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:af53c5fd68b00c68f10bdf45a2a0722f21145198568dea4e234cd29a203ed104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45481049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074879bc8f8fb73a2e0e5c673f899a1f0828155d7cb6438155ca325e9fdb71f1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d786d8441cb12eabd778b4fd3cd47545cf3438274298d60dc913795a4f0bebbe`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 9.3 MB (9289921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ba1c4b3d5eed0f37eae81343bf7ce6567d4b0ed8bd27ce279b931260b52e93`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80796e21756c240d7813b94da57b6bcac341e952f53f3074d48d063aae1dfcb`  
		Last Modified: Mon, 28 Apr 2025 23:52:48 GMT  
		Size: 9.3 MB (9303501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a43adfa4ee7447040e90c8c064b759cb333d0f3708f001e876a681163fb64b`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:ea14c11c9ceb121f78905c25f3e957584210f040fbf45663d752578eeb75c832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd86054f23353807a35ef0654a0954c73e035e293bca3105502f8d999bb57ff`

```dockerfile
```

-	Layers:
	-	`sha256:558fbcefee003feb767420c7c9f16e24bb3c53c98d0b2268fae98ea2eefe3764`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 2.6 MB (2626589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f599bc6bfca25763bad00cd6cabed025519d888b29a5fc013af803be0cf9a7e`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:6773003a0539d9f6df5f3e0eac90364bf519ddb08548bc76e787fa510df14e54
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
$ docker pull rethinkdb@sha256:146a49694f822cb25c2db9064eb0824c7e7ec3c8e14aca3bafd32e2966be3d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48014493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3967c6dced81d604b0ea5731a04ef075ecd7a5d3ad5fb3d46f885be0ac9edec8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1368caeec38d860ab14fd21f6273c2e65a1982c822d09214dbc987d42dbf609`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 9.8 MB (9791220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b23cb4883335dded490789b5187dc0a9d029e0facbed093a8c0a3f340602ca`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81989d522b62d14a4851ad1ca31704bfd8160054c84081806c46d7341a1f63e9`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 10.0 MB (9992868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36d4f3cbe3d3334572b5b24719f8396b6eadbecce3d65f55119541d7faca87d`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:433027607d1280864b3334bf89982c71eecf7c3fbf682d6a8067b7279829c877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6245972b18ad63665bf9429702af047c588cf5cb743a501ad1101ea60be32f22`

```dockerfile
```

-	Layers:
	-	`sha256:bffcaa740af81c1547444a699457668a016f2ae751bb7ce5fbf7677f5aad31df`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 2.6 MB (2627495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc8e665ffb08a9af6b3c2afc7bf5c482e0cd83bf86e9972d2efa283b12c2bf7`  
		Last Modified: Mon, 28 Apr 2025 21:54:37 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:db72dc143498796e01d4226d4e2ac3978b48867b541cb823d70904e299824fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47020879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8dd10f87ce1b32d7d27efa40471fb6376967e2e916dad670828b6da6f81b23b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315fe6fed3515ab7ce2e7d3d32ff0be4238c8c82746470392aa876a5641240e1`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 9.6 MB (9588958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165fdf7199a783cb2efe62c25bba9a645cbf4f337155599884e155221950ae78`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e43d85ff9417cdc42920fa0cae03ea0d12ed72ed4934fbf58c9eaab1cb1817`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 9.4 MB (9362540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f35f2e0e1738b3ce469c9961a459ad7ca82f5202da5183f3ec7f5335ae14f4`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:a189e231c4edc1140651af9a6c572a4abf91511ec1474645137890fd44175b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2641459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfedd8acbc43cdd15bb55cc7d4247290471f07b52d5da80adcfe5c8c582e728`

```dockerfile
```

-	Layers:
	-	`sha256:3752ef92f8cacf48d095a37b24e8d26aa6b620da1690f0a7f9de8fdff50415fb`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 2.6 MB (2627830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c2cfc052a1f907ca28c4774d3f93b2f95e6c8e0affca9ce5ac2b30516a04fc`  
		Last Modified: Tue, 29 Apr 2025 01:25:40 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; s390x

```console
$ docker pull rethinkdb@sha256:af53c5fd68b00c68f10bdf45a2a0722f21145198568dea4e234cd29a203ed104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45481049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074879bc8f8fb73a2e0e5c673f899a1f0828155d7cb6438155ca325e9fdb71f1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d786d8441cb12eabd778b4fd3cd47545cf3438274298d60dc913795a4f0bebbe`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 9.3 MB (9289921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ba1c4b3d5eed0f37eae81343bf7ce6567d4b0ed8bd27ce279b931260b52e93`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80796e21756c240d7813b94da57b6bcac341e952f53f3074d48d063aae1dfcb`  
		Last Modified: Mon, 28 Apr 2025 23:52:48 GMT  
		Size: 9.3 MB (9303501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a43adfa4ee7447040e90c8c064b759cb333d0f3708f001e876a681163fb64b`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:ea14c11c9ceb121f78905c25f3e957584210f040fbf45663d752578eeb75c832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd86054f23353807a35ef0654a0954c73e035e293bca3105502f8d999bb57ff`

```dockerfile
```

-	Layers:
	-	`sha256:558fbcefee003feb767420c7c9f16e24bb3c53c98d0b2268fae98ea2eefe3764`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 2.6 MB (2626589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f599bc6bfca25763bad00cd6cabed025519d888b29a5fc013af803be0cf9a7e`  
		Last Modified: Mon, 28 Apr 2025 23:52:47 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json
