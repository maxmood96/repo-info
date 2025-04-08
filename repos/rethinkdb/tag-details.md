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
$ docker pull rethinkdb@sha256:1f5a4ab7d6d2dbd53c1ddd86663ee6c4b8c0621f26e72dfed14d77d978038c1e
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
$ docker pull rethinkdb@sha256:f8fb4417ea3dca38493d55c5fec89d82ddeeb26792f1cb3f77d58366f69c6ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48014042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0ba9c97763591b2ae2d18be39a1ad292921b6fdc89fd3cebc51cf646b39c02`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d7daae9c5a1c4ba4ffc37faa7c7700f5ab8ad643842cfec369468b8d7568c8`  
		Last Modified: Tue, 08 Apr 2025 01:23:18 GMT  
		Size: 9.8 MB (9791245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de024b2daa7a1b54f19ff15c4db73639eb8fed62ad23dc70858243ce2ba546b`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54728432da2f59cb3e1d4c46faf1289fe55f52d4070f2f0bd0b85bf9b51f2505`  
		Last Modified: Tue, 08 Apr 2025 01:23:18 GMT  
		Size: 10.0 MB (9992777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec834a72c5025af158858223403acada80c599e3789d18d9768d43ae4c1f119`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:dc90105cf4e1c7e2cbdc87035275e48d6a85a1ba603922d36ba0c3683b84395d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53cd07d600f85a06d73fa07ab9bdb2628216f4294c08fa0da1587e03a866541`

```dockerfile
```

-	Layers:
	-	`sha256:4ba3589c13b6989265b1cf52ac907a2521ae76c6ab42a3e255d63d819fcfd6d1`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 2.6 MB (2627495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39881eafd1c4454992962595e39dbfbac71c713493749c73a9fead63487cca4d`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 13.4 KB (13446 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2` - linux; arm64 variant v8

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

### `rethinkdb:2` - unknown; unknown

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

### `rethinkdb:2` - linux; s390x

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

### `rethinkdb:2` - unknown; unknown

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

## `rethinkdb:2-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:1f5a4ab7d6d2dbd53c1ddd86663ee6c4b8c0621f26e72dfed14d77d978038c1e
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
$ docker pull rethinkdb@sha256:f8fb4417ea3dca38493d55c5fec89d82ddeeb26792f1cb3f77d58366f69c6ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48014042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0ba9c97763591b2ae2d18be39a1ad292921b6fdc89fd3cebc51cf646b39c02`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d7daae9c5a1c4ba4ffc37faa7c7700f5ab8ad643842cfec369468b8d7568c8`  
		Last Modified: Tue, 08 Apr 2025 01:23:18 GMT  
		Size: 9.8 MB (9791245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de024b2daa7a1b54f19ff15c4db73639eb8fed62ad23dc70858243ce2ba546b`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54728432da2f59cb3e1d4c46faf1289fe55f52d4070f2f0bd0b85bf9b51f2505`  
		Last Modified: Tue, 08 Apr 2025 01:23:18 GMT  
		Size: 10.0 MB (9992777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec834a72c5025af158858223403acada80c599e3789d18d9768d43ae4c1f119`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:dc90105cf4e1c7e2cbdc87035275e48d6a85a1ba603922d36ba0c3683b84395d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53cd07d600f85a06d73fa07ab9bdb2628216f4294c08fa0da1587e03a866541`

```dockerfile
```

-	Layers:
	-	`sha256:4ba3589c13b6989265b1cf52ac907a2521ae76c6ab42a3e255d63d819fcfd6d1`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 2.6 MB (2627495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39881eafd1c4454992962595e39dbfbac71c713493749c73a9fead63487cca4d`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 13.4 KB (13446 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; arm64 variant v8

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

### `rethinkdb:2-bookworm-slim` - unknown; unknown

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

### `rethinkdb:2-bookworm-slim` - linux; s390x

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

### `rethinkdb:2-bookworm-slim` - unknown; unknown

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

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:1f5a4ab7d6d2dbd53c1ddd86663ee6c4b8c0621f26e72dfed14d77d978038c1e
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
$ docker pull rethinkdb@sha256:f8fb4417ea3dca38493d55c5fec89d82ddeeb26792f1cb3f77d58366f69c6ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48014042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0ba9c97763591b2ae2d18be39a1ad292921b6fdc89fd3cebc51cf646b39c02`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d7daae9c5a1c4ba4ffc37faa7c7700f5ab8ad643842cfec369468b8d7568c8`  
		Last Modified: Tue, 08 Apr 2025 01:23:18 GMT  
		Size: 9.8 MB (9791245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de024b2daa7a1b54f19ff15c4db73639eb8fed62ad23dc70858243ce2ba546b`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54728432da2f59cb3e1d4c46faf1289fe55f52d4070f2f0bd0b85bf9b51f2505`  
		Last Modified: Tue, 08 Apr 2025 01:23:18 GMT  
		Size: 10.0 MB (9992777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec834a72c5025af158858223403acada80c599e3789d18d9768d43ae4c1f119`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:dc90105cf4e1c7e2cbdc87035275e48d6a85a1ba603922d36ba0c3683b84395d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53cd07d600f85a06d73fa07ab9bdb2628216f4294c08fa0da1587e03a866541`

```dockerfile
```

-	Layers:
	-	`sha256:4ba3589c13b6989265b1cf52ac907a2521ae76c6ab42a3e255d63d819fcfd6d1`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 2.6 MB (2627495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39881eafd1c4454992962595e39dbfbac71c713493749c73a9fead63487cca4d`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 13.4 KB (13446 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4` - linux; arm64 variant v8

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

### `rethinkdb:2.4` - unknown; unknown

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

### `rethinkdb:2.4` - linux; s390x

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

### `rethinkdb:2.4` - unknown; unknown

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

## `rethinkdb:2.4-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:1f5a4ab7d6d2dbd53c1ddd86663ee6c4b8c0621f26e72dfed14d77d978038c1e
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
$ docker pull rethinkdb@sha256:f8fb4417ea3dca38493d55c5fec89d82ddeeb26792f1cb3f77d58366f69c6ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48014042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0ba9c97763591b2ae2d18be39a1ad292921b6fdc89fd3cebc51cf646b39c02`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d7daae9c5a1c4ba4ffc37faa7c7700f5ab8ad643842cfec369468b8d7568c8`  
		Last Modified: Tue, 08 Apr 2025 01:23:18 GMT  
		Size: 9.8 MB (9791245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de024b2daa7a1b54f19ff15c4db73639eb8fed62ad23dc70858243ce2ba546b`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54728432da2f59cb3e1d4c46faf1289fe55f52d4070f2f0bd0b85bf9b51f2505`  
		Last Modified: Tue, 08 Apr 2025 01:23:18 GMT  
		Size: 10.0 MB (9992777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec834a72c5025af158858223403acada80c599e3789d18d9768d43ae4c1f119`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:dc90105cf4e1c7e2cbdc87035275e48d6a85a1ba603922d36ba0c3683b84395d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53cd07d600f85a06d73fa07ab9bdb2628216f4294c08fa0da1587e03a866541`

```dockerfile
```

-	Layers:
	-	`sha256:4ba3589c13b6989265b1cf52ac907a2521ae76c6ab42a3e255d63d819fcfd6d1`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 2.6 MB (2627495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39881eafd1c4454992962595e39dbfbac71c713493749c73a9fead63487cca4d`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 13.4 KB (13446 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4-bookworm-slim` - linux; arm64 variant v8

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

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

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

### `rethinkdb:2.4-bookworm-slim` - linux; s390x

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

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

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

## `rethinkdb:2.4.3`

```console
$ docker pull rethinkdb@sha256:1f5a4ab7d6d2dbd53c1ddd86663ee6c4b8c0621f26e72dfed14d77d978038c1e
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
$ docker pull rethinkdb@sha256:f8fb4417ea3dca38493d55c5fec89d82ddeeb26792f1cb3f77d58366f69c6ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48014042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0ba9c97763591b2ae2d18be39a1ad292921b6fdc89fd3cebc51cf646b39c02`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d7daae9c5a1c4ba4ffc37faa7c7700f5ab8ad643842cfec369468b8d7568c8`  
		Last Modified: Tue, 08 Apr 2025 01:23:18 GMT  
		Size: 9.8 MB (9791245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de024b2daa7a1b54f19ff15c4db73639eb8fed62ad23dc70858243ce2ba546b`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54728432da2f59cb3e1d4c46faf1289fe55f52d4070f2f0bd0b85bf9b51f2505`  
		Last Modified: Tue, 08 Apr 2025 01:23:18 GMT  
		Size: 10.0 MB (9992777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec834a72c5025af158858223403acada80c599e3789d18d9768d43ae4c1f119`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:dc90105cf4e1c7e2cbdc87035275e48d6a85a1ba603922d36ba0c3683b84395d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53cd07d600f85a06d73fa07ab9bdb2628216f4294c08fa0da1587e03a866541`

```dockerfile
```

-	Layers:
	-	`sha256:4ba3589c13b6989265b1cf52ac907a2521ae76c6ab42a3e255d63d819fcfd6d1`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 2.6 MB (2627495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39881eafd1c4454992962595e39dbfbac71c713493749c73a9fead63487cca4d`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 13.4 KB (13446 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.3` - linux; arm64 variant v8

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

### `rethinkdb:2.4.3` - unknown; unknown

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

### `rethinkdb:2.4.3` - linux; s390x

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

### `rethinkdb:2.4.3` - unknown; unknown

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

## `rethinkdb:2.4.4-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:1f5a4ab7d6d2dbd53c1ddd86663ee6c4b8c0621f26e72dfed14d77d978038c1e
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
$ docker pull rethinkdb@sha256:f8fb4417ea3dca38493d55c5fec89d82ddeeb26792f1cb3f77d58366f69c6ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48014042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0ba9c97763591b2ae2d18be39a1ad292921b6fdc89fd3cebc51cf646b39c02`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d7daae9c5a1c4ba4ffc37faa7c7700f5ab8ad643842cfec369468b8d7568c8`  
		Last Modified: Tue, 08 Apr 2025 01:23:18 GMT  
		Size: 9.8 MB (9791245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de024b2daa7a1b54f19ff15c4db73639eb8fed62ad23dc70858243ce2ba546b`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54728432da2f59cb3e1d4c46faf1289fe55f52d4070f2f0bd0b85bf9b51f2505`  
		Last Modified: Tue, 08 Apr 2025 01:23:18 GMT  
		Size: 10.0 MB (9992777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec834a72c5025af158858223403acada80c599e3789d18d9768d43ae4c1f119`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:dc90105cf4e1c7e2cbdc87035275e48d6a85a1ba603922d36ba0c3683b84395d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53cd07d600f85a06d73fa07ab9bdb2628216f4294c08fa0da1587e03a866541`

```dockerfile
```

-	Layers:
	-	`sha256:4ba3589c13b6989265b1cf52ac907a2521ae76c6ab42a3e255d63d819fcfd6d1`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 2.6 MB (2627495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39881eafd1c4454992962595e39dbfbac71c713493749c73a9fead63487cca4d`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 13.4 KB (13446 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.4-bookworm-slim` - linux; arm64 variant v8

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

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

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

### `rethinkdb:2.4.4-bookworm-slim` - linux; s390x

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

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

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

## `rethinkdb:bookworm-slim`

```console
$ docker pull rethinkdb@sha256:1f5a4ab7d6d2dbd53c1ddd86663ee6c4b8c0621f26e72dfed14d77d978038c1e
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
$ docker pull rethinkdb@sha256:f8fb4417ea3dca38493d55c5fec89d82ddeeb26792f1cb3f77d58366f69c6ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48014042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0ba9c97763591b2ae2d18be39a1ad292921b6fdc89fd3cebc51cf646b39c02`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d7daae9c5a1c4ba4ffc37faa7c7700f5ab8ad643842cfec369468b8d7568c8`  
		Last Modified: Tue, 08 Apr 2025 01:23:18 GMT  
		Size: 9.8 MB (9791245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de024b2daa7a1b54f19ff15c4db73639eb8fed62ad23dc70858243ce2ba546b`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54728432da2f59cb3e1d4c46faf1289fe55f52d4070f2f0bd0b85bf9b51f2505`  
		Last Modified: Tue, 08 Apr 2025 01:23:18 GMT  
		Size: 10.0 MB (9992777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec834a72c5025af158858223403acada80c599e3789d18d9768d43ae4c1f119`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:dc90105cf4e1c7e2cbdc87035275e48d6a85a1ba603922d36ba0c3683b84395d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53cd07d600f85a06d73fa07ab9bdb2628216f4294c08fa0da1587e03a866541`

```dockerfile
```

-	Layers:
	-	`sha256:4ba3589c13b6989265b1cf52ac907a2521ae76c6ab42a3e255d63d819fcfd6d1`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 2.6 MB (2627495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39881eafd1c4454992962595e39dbfbac71c713493749c73a9fead63487cca4d`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 13.4 KB (13446 bytes)  
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

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:1f5a4ab7d6d2dbd53c1ddd86663ee6c4b8c0621f26e72dfed14d77d978038c1e
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
$ docker pull rethinkdb@sha256:f8fb4417ea3dca38493d55c5fec89d82ddeeb26792f1cb3f77d58366f69c6ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48014042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0ba9c97763591b2ae2d18be39a1ad292921b6fdc89fd3cebc51cf646b39c02`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d7daae9c5a1c4ba4ffc37faa7c7700f5ab8ad643842cfec369468b8d7568c8`  
		Last Modified: Tue, 08 Apr 2025 01:23:18 GMT  
		Size: 9.8 MB (9791245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de024b2daa7a1b54f19ff15c4db73639eb8fed62ad23dc70858243ce2ba546b`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54728432da2f59cb3e1d4c46faf1289fe55f52d4070f2f0bd0b85bf9b51f2505`  
		Last Modified: Tue, 08 Apr 2025 01:23:18 GMT  
		Size: 10.0 MB (9992777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec834a72c5025af158858223403acada80c599e3789d18d9768d43ae4c1f119`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:dc90105cf4e1c7e2cbdc87035275e48d6a85a1ba603922d36ba0c3683b84395d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53cd07d600f85a06d73fa07ab9bdb2628216f4294c08fa0da1587e03a866541`

```dockerfile
```

-	Layers:
	-	`sha256:4ba3589c13b6989265b1cf52ac907a2521ae76c6ab42a3e255d63d819fcfd6d1`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 2.6 MB (2627495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39881eafd1c4454992962595e39dbfbac71c713493749c73a9fead63487cca4d`  
		Last Modified: Tue, 08 Apr 2025 01:23:17 GMT  
		Size: 13.4 KB (13446 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; arm64 variant v8

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

### `rethinkdb:latest` - unknown; unknown

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

### `rethinkdb:latest` - linux; s390x

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

### `rethinkdb:latest` - unknown; unknown

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
