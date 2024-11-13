## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:cb98da9ab56ffbc911b81ef05e8dfacad9586e0fef32fe1b12ebc2c8ee67ada7
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
$ docker pull rethinkdb@sha256:893bdf35d4af43a2ce5cb138441b59464b21a7a18ca928173bcf809aec35281d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48914590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ed574d3fa53ec4c15aada82981a32e3a3a4018918c534ea008e107588082e7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["bash"]
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fdc03a2f46b636b786a50815edc85f995e3cd5deaaa0600a3c04545414f217`  
		Last Modified: Wed, 13 Nov 2024 05:50:01 GMT  
		Size: 9.8 MB (9791034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ed3185010da5feca544a6f42074f2ad16ab8a3ea7f15ea1c780f6c4a4f9865`  
		Last Modified: Wed, 13 Nov 2024 05:50:00 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73ae34fbd222f94e77643478fbe9958422c19816d8800be2cb21687fe1cd3f5`  
		Last Modified: Wed, 13 Nov 2024 05:50:01 GMT  
		Size: 10.0 MB (9992799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6025322772b670a780b7a241cef3a2b387e5055ddedb103dade4a66f569fb72`  
		Last Modified: Wed, 13 Nov 2024 05:50:00 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:b39ba6477fd2fb40e4a0ed4b84543de93ca1908cf04b26d7bc532d196a653097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2643102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58cebaeb7e68073dc67e5fd2b03c3ddbf4506d92359a574e4724c1e49a78c65`

```dockerfile
```

-	Layers:
	-	`sha256:c9dfd04237a9be6626f34a024e0275742bcf590489c6f37921157b5fed00cd0a`  
		Last Modified: Wed, 13 Nov 2024 05:50:01 GMT  
		Size: 2.6 MB (2629655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:025a390026f566afd7650093adfec10db9959f8e44aa8ecbde8e92775931f915`  
		Last Modified: Wed, 13 Nov 2024 05:50:00 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:2c8a1e506940b3388c0e159425b111c84b3615fedf6e187aa078d8d1b54d4551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48111307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1781c6df7e07e24ac9f1c58c2e2abd53d8ee86f05c08a9269a2950f406fd5f7c`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["bash"]
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80281751a20dc2a8c85ad97c1fccb82f3b7183b00e5c9562ec7b067aae220ee`  
		Last Modified: Wed, 13 Nov 2024 07:53:16 GMT  
		Size: 9.6 MB (9588652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd29dc2945ae1bac8195137942ef5213d190dd5f5abb0e5f9a6396ffd35e294`  
		Last Modified: Wed, 13 Nov 2024 07:53:15 GMT  
		Size: 2.7 KB (2671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6176a4b2e1343bac53425c213e74a2f76dc1076f6259a8b537831c6f2a28199`  
		Last Modified: Wed, 13 Nov 2024 07:53:16 GMT  
		Size: 9.4 MB (9362534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b75b93b125d39778899d521150478121bddde0e2b7cda67bfb07e742844f693`  
		Last Modified: Wed, 13 Nov 2024 07:53:16 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:cd087fe82aa50496a313540668a9e9dbf738c4b4302e252260e18076d7e8aa52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2643618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60992e02f2baa9ac9b6996fd57b5eaac021c88c71ced637ba0c74178bae7a94e`

```dockerfile
```

-	Layers:
	-	`sha256:b764f113491df7d2dde4e6efc2bf3a5b499e65602b8b659c9c8fbd358d88ff64`  
		Last Modified: Wed, 13 Nov 2024 07:53:16 GMT  
		Size: 2.6 MB (2629989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf149c0f6804f5a6f397e9f944b9965ee209ebbf8ba67585f5e803ae8ff86902`  
		Last Modified: Wed, 13 Nov 2024 07:53:15 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; s390x

```console
$ docker pull rethinkdb@sha256:c0690d6ee10edd5557c21eb8f57cc126bb600f88f951497b76643a77692d27d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46087422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1732ce56df9816bd349aa11d0b3ce45c9837f516d08ca9b9ab1a5780d840a032`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["bash"]
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
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c368691119cf3c299fd490eb622130c1f078f33f139b3bb21cce944da3b5e35`  
		Last Modified: Wed, 13 Nov 2024 12:09:03 GMT  
		Size: 9.3 MB (9289477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091ce68a710de3c7b62b70787c7afd06750680de1fde0c7a839898b55044c231`  
		Last Modified: Wed, 13 Nov 2024 12:09:02 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db740bd77fd24c7f63d8e481dd8d858e0ab6fa64285048ae01dff05367184e5`  
		Last Modified: Wed, 13 Nov 2024 12:09:02 GMT  
		Size: 9.3 MB (9303557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f4d474069dbcb99c485358ab17cb198df298690badbac2c907f54a6ac5036c`  
		Last Modified: Wed, 13 Nov 2024 12:09:02 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:9dd846d6d186400ea5b2da46130cda489b3b9fdcb3149bbcfa94a76fadb366d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2642196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982b6fa298b9ee8027b43eb50bb207088a33a5aea2ad2d6c60745c8c38bdc194`

```dockerfile
```

-	Layers:
	-	`sha256:72ae33b071ceeebf6c274e0c76e967b97c906b9d1b443be7112d13f54c9ae5ae`  
		Last Modified: Wed, 13 Nov 2024 12:09:02 GMT  
		Size: 2.6 MB (2628749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c8ac726abbf456ee7528b98198ad530fb08653e25877b223d52d752a831609e`  
		Last Modified: Wed, 13 Nov 2024 12:09:02 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json
