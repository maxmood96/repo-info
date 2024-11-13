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
$ docker pull rethinkdb@sha256:156eaa990ae33d86aea441f2022b915ad2a675ae0e43a0359daa90daeebb01d1
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

### `rethinkdb:2` - unknown; unknown

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

### `rethinkdb:2` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:e0ff18a124115f56a010f72f69b2fee46fa4f08544afefe10358329b7f49622e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48109893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218f35396e32df55a6f17a1478d8b605dff492fc6fe3aad3e7c0cbdb6e452ed5`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4514e7920c831f42f110e58920a5108f8295461d06354fbba06af7a2c51fd5`  
		Last Modified: Thu, 17 Oct 2024 20:10:27 GMT  
		Size: 9.6 MB (9588300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07174a2b9b2a5de8579535848eec9d30c61e3ec69657eff0138207f2ce4bc970`  
		Last Modified: Thu, 17 Oct 2024 20:10:26 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57119ae4ad419a5cb989ab5004a37e0717b2275eb12f4a72d44a58d77c30cc7`  
		Last Modified: Thu, 17 Oct 2024 20:10:27 GMT  
		Size: 9.4 MB (9362493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e3d0808a0bb2e7a8c6cead213181cda160950f7dc76291a739a2741e10775f`  
		Last Modified: Thu, 17 Oct 2024 20:10:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:c7565f7b744d297afe04db4ab1c9cf51733fe790257e7259abb237f8cc32e16c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21666e4f054e2f7d35187522c6fa8aae4f51c6c20872ab3e47308aba49e85dc2`

```dockerfile
```

-	Layers:
	-	`sha256:b4f50fc23f1f68b198562474e1ec024481c73677c71a8cea280d516e4658b40e`  
		Last Modified: Thu, 17 Oct 2024 20:10:27 GMT  
		Size: 2.6 MB (2613536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bab72b971a05dcbab1c76c2138efedfd1150abd4d42d6917f4d77a5666e4a40`  
		Last Modified: Thu, 17 Oct 2024 20:10:26 GMT  
		Size: 13.5 KB (13461 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2` - linux; s390x

```console
$ docker pull rethinkdb@sha256:7ec1fa2a9a89a9385f8f706f23c7d0ddae6bdede71bafc6dd77e6f10f4194d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46084746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b5e5e1ca421946b56d76c32bbc2388b51eb791d54ff4465bc6d251f034d52f`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
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
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcf598850e58f691c35de94287bea3ee866836b5668ffa7bceaad7b4e5129b3`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 9.3 MB (9288411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09322b26fa173bb65d017b571876b83f4b828dd683f92142b64156b606e7e4a9`  
		Last Modified: Thu, 17 Oct 2024 17:57:05 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d87c8977528ca7a88c1d9a3c09528019f9c987013f3e817e3b2885cab914c09`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 9.3 MB (9303490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158357543fe22e9b74a145cc21c8ec0600b74a5cc76b60a95e896103beb378b4`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:475e87adbfca52acccc0d4adf0f708932c436788551fb82fed860e1a20685d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2625687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee73f8caa07997d5947ca80a64fe788fd88fec2b6832761418734133f3e0e7f`

```dockerfile
```

-	Layers:
	-	`sha256:bc51596511c08465c6804970c5fc20a82935b75edefab072f8a28af1a557cf1a`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 2.6 MB (2612402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30ea236b2060bfe207c4827df90320af797ab620618865c7f1af25ee712d1c0b`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 13.3 KB (13285 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:156eaa990ae33d86aea441f2022b915ad2a675ae0e43a0359daa90daeebb01d1
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

### `rethinkdb:2-bookworm-slim` - unknown; unknown

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

### `rethinkdb:2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:e0ff18a124115f56a010f72f69b2fee46fa4f08544afefe10358329b7f49622e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48109893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218f35396e32df55a6f17a1478d8b605dff492fc6fe3aad3e7c0cbdb6e452ed5`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4514e7920c831f42f110e58920a5108f8295461d06354fbba06af7a2c51fd5`  
		Last Modified: Thu, 17 Oct 2024 20:10:27 GMT  
		Size: 9.6 MB (9588300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07174a2b9b2a5de8579535848eec9d30c61e3ec69657eff0138207f2ce4bc970`  
		Last Modified: Thu, 17 Oct 2024 20:10:26 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57119ae4ad419a5cb989ab5004a37e0717b2275eb12f4a72d44a58d77c30cc7`  
		Last Modified: Thu, 17 Oct 2024 20:10:27 GMT  
		Size: 9.4 MB (9362493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e3d0808a0bb2e7a8c6cead213181cda160950f7dc76291a739a2741e10775f`  
		Last Modified: Thu, 17 Oct 2024 20:10:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:c7565f7b744d297afe04db4ab1c9cf51733fe790257e7259abb237f8cc32e16c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21666e4f054e2f7d35187522c6fa8aae4f51c6c20872ab3e47308aba49e85dc2`

```dockerfile
```

-	Layers:
	-	`sha256:b4f50fc23f1f68b198562474e1ec024481c73677c71a8cea280d516e4658b40e`  
		Last Modified: Thu, 17 Oct 2024 20:10:27 GMT  
		Size: 2.6 MB (2613536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bab72b971a05dcbab1c76c2138efedfd1150abd4d42d6917f4d77a5666e4a40`  
		Last Modified: Thu, 17 Oct 2024 20:10:26 GMT  
		Size: 13.5 KB (13461 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:7ec1fa2a9a89a9385f8f706f23c7d0ddae6bdede71bafc6dd77e6f10f4194d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46084746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b5e5e1ca421946b56d76c32bbc2388b51eb791d54ff4465bc6d251f034d52f`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
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
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcf598850e58f691c35de94287bea3ee866836b5668ffa7bceaad7b4e5129b3`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 9.3 MB (9288411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09322b26fa173bb65d017b571876b83f4b828dd683f92142b64156b606e7e4a9`  
		Last Modified: Thu, 17 Oct 2024 17:57:05 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d87c8977528ca7a88c1d9a3c09528019f9c987013f3e817e3b2885cab914c09`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 9.3 MB (9303490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158357543fe22e9b74a145cc21c8ec0600b74a5cc76b60a95e896103beb378b4`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:475e87adbfca52acccc0d4adf0f708932c436788551fb82fed860e1a20685d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2625687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee73f8caa07997d5947ca80a64fe788fd88fec2b6832761418734133f3e0e7f`

```dockerfile
```

-	Layers:
	-	`sha256:bc51596511c08465c6804970c5fc20a82935b75edefab072f8a28af1a557cf1a`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 2.6 MB (2612402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30ea236b2060bfe207c4827df90320af797ab620618865c7f1af25ee712d1c0b`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 13.3 KB (13285 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:156eaa990ae33d86aea441f2022b915ad2a675ae0e43a0359daa90daeebb01d1
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

### `rethinkdb:2.4` - unknown; unknown

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

### `rethinkdb:2.4` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:e0ff18a124115f56a010f72f69b2fee46fa4f08544afefe10358329b7f49622e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48109893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218f35396e32df55a6f17a1478d8b605dff492fc6fe3aad3e7c0cbdb6e452ed5`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4514e7920c831f42f110e58920a5108f8295461d06354fbba06af7a2c51fd5`  
		Last Modified: Thu, 17 Oct 2024 20:10:27 GMT  
		Size: 9.6 MB (9588300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07174a2b9b2a5de8579535848eec9d30c61e3ec69657eff0138207f2ce4bc970`  
		Last Modified: Thu, 17 Oct 2024 20:10:26 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57119ae4ad419a5cb989ab5004a37e0717b2275eb12f4a72d44a58d77c30cc7`  
		Last Modified: Thu, 17 Oct 2024 20:10:27 GMT  
		Size: 9.4 MB (9362493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e3d0808a0bb2e7a8c6cead213181cda160950f7dc76291a739a2741e10775f`  
		Last Modified: Thu, 17 Oct 2024 20:10:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:c7565f7b744d297afe04db4ab1c9cf51733fe790257e7259abb237f8cc32e16c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21666e4f054e2f7d35187522c6fa8aae4f51c6c20872ab3e47308aba49e85dc2`

```dockerfile
```

-	Layers:
	-	`sha256:b4f50fc23f1f68b198562474e1ec024481c73677c71a8cea280d516e4658b40e`  
		Last Modified: Thu, 17 Oct 2024 20:10:27 GMT  
		Size: 2.6 MB (2613536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bab72b971a05dcbab1c76c2138efedfd1150abd4d42d6917f4d77a5666e4a40`  
		Last Modified: Thu, 17 Oct 2024 20:10:26 GMT  
		Size: 13.5 KB (13461 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4` - linux; s390x

```console
$ docker pull rethinkdb@sha256:7ec1fa2a9a89a9385f8f706f23c7d0ddae6bdede71bafc6dd77e6f10f4194d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46084746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b5e5e1ca421946b56d76c32bbc2388b51eb791d54ff4465bc6d251f034d52f`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
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
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcf598850e58f691c35de94287bea3ee866836b5668ffa7bceaad7b4e5129b3`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 9.3 MB (9288411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09322b26fa173bb65d017b571876b83f4b828dd683f92142b64156b606e7e4a9`  
		Last Modified: Thu, 17 Oct 2024 17:57:05 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d87c8977528ca7a88c1d9a3c09528019f9c987013f3e817e3b2885cab914c09`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 9.3 MB (9303490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158357543fe22e9b74a145cc21c8ec0600b74a5cc76b60a95e896103beb378b4`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:475e87adbfca52acccc0d4adf0f708932c436788551fb82fed860e1a20685d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2625687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee73f8caa07997d5947ca80a64fe788fd88fec2b6832761418734133f3e0e7f`

```dockerfile
```

-	Layers:
	-	`sha256:bc51596511c08465c6804970c5fc20a82935b75edefab072f8a28af1a557cf1a`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 2.6 MB (2612402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30ea236b2060bfe207c4827df90320af797ab620618865c7f1af25ee712d1c0b`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 13.3 KB (13285 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:156eaa990ae33d86aea441f2022b915ad2a675ae0e43a0359daa90daeebb01d1
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

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

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

### `rethinkdb:2.4-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:e0ff18a124115f56a010f72f69b2fee46fa4f08544afefe10358329b7f49622e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48109893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218f35396e32df55a6f17a1478d8b605dff492fc6fe3aad3e7c0cbdb6e452ed5`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4514e7920c831f42f110e58920a5108f8295461d06354fbba06af7a2c51fd5`  
		Last Modified: Thu, 17 Oct 2024 20:10:27 GMT  
		Size: 9.6 MB (9588300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07174a2b9b2a5de8579535848eec9d30c61e3ec69657eff0138207f2ce4bc970`  
		Last Modified: Thu, 17 Oct 2024 20:10:26 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57119ae4ad419a5cb989ab5004a37e0717b2275eb12f4a72d44a58d77c30cc7`  
		Last Modified: Thu, 17 Oct 2024 20:10:27 GMT  
		Size: 9.4 MB (9362493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e3d0808a0bb2e7a8c6cead213181cda160950f7dc76291a739a2741e10775f`  
		Last Modified: Thu, 17 Oct 2024 20:10:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:c7565f7b744d297afe04db4ab1c9cf51733fe790257e7259abb237f8cc32e16c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21666e4f054e2f7d35187522c6fa8aae4f51c6c20872ab3e47308aba49e85dc2`

```dockerfile
```

-	Layers:
	-	`sha256:b4f50fc23f1f68b198562474e1ec024481c73677c71a8cea280d516e4658b40e`  
		Last Modified: Thu, 17 Oct 2024 20:10:27 GMT  
		Size: 2.6 MB (2613536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bab72b971a05dcbab1c76c2138efedfd1150abd4d42d6917f4d77a5666e4a40`  
		Last Modified: Thu, 17 Oct 2024 20:10:26 GMT  
		Size: 13.5 KB (13461 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:7ec1fa2a9a89a9385f8f706f23c7d0ddae6bdede71bafc6dd77e6f10f4194d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46084746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b5e5e1ca421946b56d76c32bbc2388b51eb791d54ff4465bc6d251f034d52f`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
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
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcf598850e58f691c35de94287bea3ee866836b5668ffa7bceaad7b4e5129b3`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 9.3 MB (9288411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09322b26fa173bb65d017b571876b83f4b828dd683f92142b64156b606e7e4a9`  
		Last Modified: Thu, 17 Oct 2024 17:57:05 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d87c8977528ca7a88c1d9a3c09528019f9c987013f3e817e3b2885cab914c09`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 9.3 MB (9303490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158357543fe22e9b74a145cc21c8ec0600b74a5cc76b60a95e896103beb378b4`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:475e87adbfca52acccc0d4adf0f708932c436788551fb82fed860e1a20685d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2625687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee73f8caa07997d5947ca80a64fe788fd88fec2b6832761418734133f3e0e7f`

```dockerfile
```

-	Layers:
	-	`sha256:bc51596511c08465c6804970c5fc20a82935b75edefab072f8a28af1a557cf1a`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 2.6 MB (2612402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30ea236b2060bfe207c4827df90320af797ab620618865c7f1af25ee712d1c0b`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 13.3 KB (13285 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4.3`

```console
$ docker pull rethinkdb@sha256:156eaa990ae33d86aea441f2022b915ad2a675ae0e43a0359daa90daeebb01d1
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

### `rethinkdb:2.4.3` - unknown; unknown

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

### `rethinkdb:2.4.3` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:e0ff18a124115f56a010f72f69b2fee46fa4f08544afefe10358329b7f49622e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48109893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218f35396e32df55a6f17a1478d8b605dff492fc6fe3aad3e7c0cbdb6e452ed5`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4514e7920c831f42f110e58920a5108f8295461d06354fbba06af7a2c51fd5`  
		Last Modified: Thu, 17 Oct 2024 20:10:27 GMT  
		Size: 9.6 MB (9588300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07174a2b9b2a5de8579535848eec9d30c61e3ec69657eff0138207f2ce4bc970`  
		Last Modified: Thu, 17 Oct 2024 20:10:26 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57119ae4ad419a5cb989ab5004a37e0717b2275eb12f4a72d44a58d77c30cc7`  
		Last Modified: Thu, 17 Oct 2024 20:10:27 GMT  
		Size: 9.4 MB (9362493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e3d0808a0bb2e7a8c6cead213181cda160950f7dc76291a739a2741e10775f`  
		Last Modified: Thu, 17 Oct 2024 20:10:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:c7565f7b744d297afe04db4ab1c9cf51733fe790257e7259abb237f8cc32e16c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21666e4f054e2f7d35187522c6fa8aae4f51c6c20872ab3e47308aba49e85dc2`

```dockerfile
```

-	Layers:
	-	`sha256:b4f50fc23f1f68b198562474e1ec024481c73677c71a8cea280d516e4658b40e`  
		Last Modified: Thu, 17 Oct 2024 20:10:27 GMT  
		Size: 2.6 MB (2613536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bab72b971a05dcbab1c76c2138efedfd1150abd4d42d6917f4d77a5666e4a40`  
		Last Modified: Thu, 17 Oct 2024 20:10:26 GMT  
		Size: 13.5 KB (13461 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.3` - linux; s390x

```console
$ docker pull rethinkdb@sha256:7ec1fa2a9a89a9385f8f706f23c7d0ddae6bdede71bafc6dd77e6f10f4194d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46084746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b5e5e1ca421946b56d76c32bbc2388b51eb791d54ff4465bc6d251f034d52f`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
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
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcf598850e58f691c35de94287bea3ee866836b5668ffa7bceaad7b4e5129b3`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 9.3 MB (9288411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09322b26fa173bb65d017b571876b83f4b828dd683f92142b64156b606e7e4a9`  
		Last Modified: Thu, 17 Oct 2024 17:57:05 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d87c8977528ca7a88c1d9a3c09528019f9c987013f3e817e3b2885cab914c09`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 9.3 MB (9303490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158357543fe22e9b74a145cc21c8ec0600b74a5cc76b60a95e896103beb378b4`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:475e87adbfca52acccc0d4adf0f708932c436788551fb82fed860e1a20685d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2625687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee73f8caa07997d5947ca80a64fe788fd88fec2b6832761418734133f3e0e7f`

```dockerfile
```

-	Layers:
	-	`sha256:bc51596511c08465c6804970c5fc20a82935b75edefab072f8a28af1a557cf1a`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 2.6 MB (2612402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30ea236b2060bfe207c4827df90320af797ab620618865c7f1af25ee712d1c0b`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 13.3 KB (13285 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4.4-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:156eaa990ae33d86aea441f2022b915ad2a675ae0e43a0359daa90daeebb01d1
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

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

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

### `rethinkdb:2.4.4-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:e0ff18a124115f56a010f72f69b2fee46fa4f08544afefe10358329b7f49622e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48109893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218f35396e32df55a6f17a1478d8b605dff492fc6fe3aad3e7c0cbdb6e452ed5`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4514e7920c831f42f110e58920a5108f8295461d06354fbba06af7a2c51fd5`  
		Last Modified: Thu, 17 Oct 2024 20:10:27 GMT  
		Size: 9.6 MB (9588300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07174a2b9b2a5de8579535848eec9d30c61e3ec69657eff0138207f2ce4bc970`  
		Last Modified: Thu, 17 Oct 2024 20:10:26 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57119ae4ad419a5cb989ab5004a37e0717b2275eb12f4a72d44a58d77c30cc7`  
		Last Modified: Thu, 17 Oct 2024 20:10:27 GMT  
		Size: 9.4 MB (9362493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e3d0808a0bb2e7a8c6cead213181cda160950f7dc76291a739a2741e10775f`  
		Last Modified: Thu, 17 Oct 2024 20:10:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:c7565f7b744d297afe04db4ab1c9cf51733fe790257e7259abb237f8cc32e16c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21666e4f054e2f7d35187522c6fa8aae4f51c6c20872ab3e47308aba49e85dc2`

```dockerfile
```

-	Layers:
	-	`sha256:b4f50fc23f1f68b198562474e1ec024481c73677c71a8cea280d516e4658b40e`  
		Last Modified: Thu, 17 Oct 2024 20:10:27 GMT  
		Size: 2.6 MB (2613536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bab72b971a05dcbab1c76c2138efedfd1150abd4d42d6917f4d77a5666e4a40`  
		Last Modified: Thu, 17 Oct 2024 20:10:26 GMT  
		Size: 13.5 KB (13461 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.4-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:7ec1fa2a9a89a9385f8f706f23c7d0ddae6bdede71bafc6dd77e6f10f4194d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46084746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b5e5e1ca421946b56d76c32bbc2388b51eb791d54ff4465bc6d251f034d52f`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
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
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcf598850e58f691c35de94287bea3ee866836b5668ffa7bceaad7b4e5129b3`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 9.3 MB (9288411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09322b26fa173bb65d017b571876b83f4b828dd683f92142b64156b606e7e4a9`  
		Last Modified: Thu, 17 Oct 2024 17:57:05 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d87c8977528ca7a88c1d9a3c09528019f9c987013f3e817e3b2885cab914c09`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 9.3 MB (9303490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158357543fe22e9b74a145cc21c8ec0600b74a5cc76b60a95e896103beb378b4`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:475e87adbfca52acccc0d4adf0f708932c436788551fb82fed860e1a20685d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2625687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee73f8caa07997d5947ca80a64fe788fd88fec2b6832761418734133f3e0e7f`

```dockerfile
```

-	Layers:
	-	`sha256:bc51596511c08465c6804970c5fc20a82935b75edefab072f8a28af1a557cf1a`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 2.6 MB (2612402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30ea236b2060bfe207c4827df90320af797ab620618865c7f1af25ee712d1c0b`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 13.3 KB (13285 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:bookworm-slim`

```console
$ docker pull rethinkdb@sha256:156eaa990ae33d86aea441f2022b915ad2a675ae0e43a0359daa90daeebb01d1
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

### `rethinkdb:bookworm-slim` - unknown; unknown

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

### `rethinkdb:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:e0ff18a124115f56a010f72f69b2fee46fa4f08544afefe10358329b7f49622e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48109893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218f35396e32df55a6f17a1478d8b605dff492fc6fe3aad3e7c0cbdb6e452ed5`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4514e7920c831f42f110e58920a5108f8295461d06354fbba06af7a2c51fd5`  
		Last Modified: Thu, 17 Oct 2024 20:10:27 GMT  
		Size: 9.6 MB (9588300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07174a2b9b2a5de8579535848eec9d30c61e3ec69657eff0138207f2ce4bc970`  
		Last Modified: Thu, 17 Oct 2024 20:10:26 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57119ae4ad419a5cb989ab5004a37e0717b2275eb12f4a72d44a58d77c30cc7`  
		Last Modified: Thu, 17 Oct 2024 20:10:27 GMT  
		Size: 9.4 MB (9362493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e3d0808a0bb2e7a8c6cead213181cda160950f7dc76291a739a2741e10775f`  
		Last Modified: Thu, 17 Oct 2024 20:10:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:c7565f7b744d297afe04db4ab1c9cf51733fe790257e7259abb237f8cc32e16c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21666e4f054e2f7d35187522c6fa8aae4f51c6c20872ab3e47308aba49e85dc2`

```dockerfile
```

-	Layers:
	-	`sha256:b4f50fc23f1f68b198562474e1ec024481c73677c71a8cea280d516e4658b40e`  
		Last Modified: Thu, 17 Oct 2024 20:10:27 GMT  
		Size: 2.6 MB (2613536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bab72b971a05dcbab1c76c2138efedfd1150abd4d42d6917f4d77a5666e4a40`  
		Last Modified: Thu, 17 Oct 2024 20:10:26 GMT  
		Size: 13.5 KB (13461 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:7ec1fa2a9a89a9385f8f706f23c7d0ddae6bdede71bafc6dd77e6f10f4194d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46084746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b5e5e1ca421946b56d76c32bbc2388b51eb791d54ff4465bc6d251f034d52f`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
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
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcf598850e58f691c35de94287bea3ee866836b5668ffa7bceaad7b4e5129b3`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 9.3 MB (9288411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09322b26fa173bb65d017b571876b83f4b828dd683f92142b64156b606e7e4a9`  
		Last Modified: Thu, 17 Oct 2024 17:57:05 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d87c8977528ca7a88c1d9a3c09528019f9c987013f3e817e3b2885cab914c09`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 9.3 MB (9303490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158357543fe22e9b74a145cc21c8ec0600b74a5cc76b60a95e896103beb378b4`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:475e87adbfca52acccc0d4adf0f708932c436788551fb82fed860e1a20685d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2625687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee73f8caa07997d5947ca80a64fe788fd88fec2b6832761418734133f3e0e7f`

```dockerfile
```

-	Layers:
	-	`sha256:bc51596511c08465c6804970c5fc20a82935b75edefab072f8a28af1a557cf1a`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 2.6 MB (2612402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30ea236b2060bfe207c4827df90320af797ab620618865c7f1af25ee712d1c0b`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 13.3 KB (13285 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:156eaa990ae33d86aea441f2022b915ad2a675ae0e43a0359daa90daeebb01d1
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
$ docker pull rethinkdb@sha256:e0ff18a124115f56a010f72f69b2fee46fa4f08544afefe10358329b7f49622e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48109893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218f35396e32df55a6f17a1478d8b605dff492fc6fe3aad3e7c0cbdb6e452ed5`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4514e7920c831f42f110e58920a5108f8295461d06354fbba06af7a2c51fd5`  
		Last Modified: Thu, 17 Oct 2024 20:10:27 GMT  
		Size: 9.6 MB (9588300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07174a2b9b2a5de8579535848eec9d30c61e3ec69657eff0138207f2ce4bc970`  
		Last Modified: Thu, 17 Oct 2024 20:10:26 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57119ae4ad419a5cb989ab5004a37e0717b2275eb12f4a72d44a58d77c30cc7`  
		Last Modified: Thu, 17 Oct 2024 20:10:27 GMT  
		Size: 9.4 MB (9362493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e3d0808a0bb2e7a8c6cead213181cda160950f7dc76291a739a2741e10775f`  
		Last Modified: Thu, 17 Oct 2024 20:10:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:c7565f7b744d297afe04db4ab1c9cf51733fe790257e7259abb237f8cc32e16c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21666e4f054e2f7d35187522c6fa8aae4f51c6c20872ab3e47308aba49e85dc2`

```dockerfile
```

-	Layers:
	-	`sha256:b4f50fc23f1f68b198562474e1ec024481c73677c71a8cea280d516e4658b40e`  
		Last Modified: Thu, 17 Oct 2024 20:10:27 GMT  
		Size: 2.6 MB (2613536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bab72b971a05dcbab1c76c2138efedfd1150abd4d42d6917f4d77a5666e4a40`  
		Last Modified: Thu, 17 Oct 2024 20:10:26 GMT  
		Size: 13.5 KB (13461 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; s390x

```console
$ docker pull rethinkdb@sha256:7ec1fa2a9a89a9385f8f706f23c7d0ddae6bdede71bafc6dd77e6f10f4194d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46084746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b5e5e1ca421946b56d76c32bbc2388b51eb791d54ff4465bc6d251f034d52f`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
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
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcf598850e58f691c35de94287bea3ee866836b5668ffa7bceaad7b4e5129b3`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 9.3 MB (9288411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09322b26fa173bb65d017b571876b83f4b828dd683f92142b64156b606e7e4a9`  
		Last Modified: Thu, 17 Oct 2024 17:57:05 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d87c8977528ca7a88c1d9a3c09528019f9c987013f3e817e3b2885cab914c09`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 9.3 MB (9303490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158357543fe22e9b74a145cc21c8ec0600b74a5cc76b60a95e896103beb378b4`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:475e87adbfca52acccc0d4adf0f708932c436788551fb82fed860e1a20685d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2625687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee73f8caa07997d5947ca80a64fe788fd88fec2b6832761418734133f3e0e7f`

```dockerfile
```

-	Layers:
	-	`sha256:bc51596511c08465c6804970c5fc20a82935b75edefab072f8a28af1a557cf1a`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 2.6 MB (2612402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30ea236b2060bfe207c4827df90320af797ab620618865c7f1af25ee712d1c0b`  
		Last Modified: Thu, 17 Oct 2024 17:57:06 GMT  
		Size: 13.3 KB (13285 bytes)  
		MIME: application/vnd.in-toto+json
