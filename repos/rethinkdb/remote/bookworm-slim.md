## `rethinkdb:bookworm-slim`

```console
$ docker pull rethinkdb@sha256:f582224bf18646363f8268db167c19dae24115750db24ea83f96bcfdb2fbcf7c
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
$ docker pull rethinkdb@sha256:5c5371c581a8709a89a567de0f521baed0300294cd18b97498896b6548b009bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47020509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7612734c97932ba5c99422fc7f4e074a863be51202cf3e3d48b57dd55afeaea`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5c41d7df34103873e4b3a53b47a399043137855dc9902260963df8b17acdbe`  
		Last Modified: Tue, 08 Apr 2025 05:41:34 GMT  
		Size: 9.6 MB (9588899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302ff2d8f35503f6aeaaf306edf813247bc1bdb6235ddb330c4ee7aac0f882e7`  
		Last Modified: Tue, 08 Apr 2025 05:41:34 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d6871fe2d09569f5f0c3b54d372a096405393f2c1628af94d1e37171305bc6`  
		Last Modified: Tue, 08 Apr 2025 05:41:35 GMT  
		Size: 9.4 MB (9362529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e3e63b76df9d3e6437c46304eb11377e3a81a5fcaef2441e298b1a2b01ee7f`  
		Last Modified: Tue, 08 Apr 2025 05:41:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:6b2df1553355708c44f2a38e018480db78105c0f2262a0ea77819603732892cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2641459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51acb788a6effe10f05ee79d6c9469116fc1133f12ca9e26cc1edcf7527fa9e0`

```dockerfile
```

-	Layers:
	-	`sha256:829e4050c00cd6672e9319d4fddc55bb7bf3c15ccfe12c662d31cc0a67d9ac47`  
		Last Modified: Tue, 08 Apr 2025 05:41:34 GMT  
		Size: 2.6 MB (2627830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c9835bb805f12c75b30607a16db2da7d2fc558986a6a46b2c9efec4e42f7ef2`  
		Last Modified: Tue, 08 Apr 2025 05:41:34 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:483d224beced46f3d6bbd30bb815db6ee2823517d8baa0c1d452db576dfc318f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45480716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f32885565da3a8bf7f5e9fde7e530a56fb4e88b41b23478c9b007893bdbcb5`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
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
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04712f5951f8adb14bc54f13362570945bbef142c63c9b073c5921a043ecd01`  
		Last Modified: Tue, 08 Apr 2025 03:35:08 GMT  
		Size: 9.3 MB (9289833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256049fe69f39a358a6165cf47ce440c1e83816f3e9c8d730a12c7649dd21655`  
		Last Modified: Tue, 08 Apr 2025 03:35:07 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2fc7bc3882cbadfc569e4fbc9a65d1255b5b4053fa7e1185c3d225896d404d`  
		Last Modified: Tue, 08 Apr 2025 03:35:07 GMT  
		Size: 9.3 MB (9303516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7c11a82e003409658a2d04b6e3253bbcc3477017642a3329300d2220499d68`  
		Last Modified: Tue, 08 Apr 2025 03:35:07 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:e8c7d3d74e50a1b9a671558caa5579e9ff279d7401ed714efa2a9612a0b3eaa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5f6910b5702320e5cb083d4d2cf33e36b47e011d0879a7f5b3d742f0c9b57d`

```dockerfile
```

-	Layers:
	-	`sha256:4f7f05bbfddfd0290649bc76e0e8a6c6639d641e89e9f771a77180a311b08ee4`  
		Last Modified: Tue, 08 Apr 2025 03:35:07 GMT  
		Size: 2.6 MB (2626589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f01140599d70241c244ac60b1dc6877de95b1078f392e58afe7dcce8134d8d9`  
		Last Modified: Tue, 08 Apr 2025 03:35:07 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json
