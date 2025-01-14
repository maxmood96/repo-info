## `rethinkdb:2-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:a5d007eec9dd05de214c950bdfec5836861895bb838fd558b2645c0565886163
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
$ docker pull rethinkdb@sha256:c8f80b539d3a35527205fa6a554330e0dbb3a9eea82e6783a3445b45acf255bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47999057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf36e2d6689f0798114e76407808b9b578761f55d98ccf112326539bd9d4d753`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b317757ce552f84e46ab3604991fd729ef9433d898d51377b9fff839ebde17`  
		Last Modified: Tue, 14 Jan 2025 02:17:34 GMT  
		Size: 9.8 MB (9791112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0748dbe510a21dc65f1509bdae6c6ffd96e621520bc38f41b75b992586d924`  
		Last Modified: Tue, 14 Jan 2025 02:17:33 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9560fda69aef2c08ff6a43137936fcbdfafbc4b3c9c2467d14a5c17eccfb72d5`  
		Last Modified: Tue, 14 Jan 2025 23:01:28 GMT  
		Size: 10.0 MB (9992764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc10313b31323fd5d1f14f6cf0bb196813d1d2943ba0ae55702973431fc5d6d1`  
		Last Modified: Tue, 14 Jan 2025 02:17:33 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:be0eb10a9afeea5419df3ec6658001ae006b3293695e9fca92a9dd2fc8db042c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2639572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aedc0b471bf97bffab5065575202198a5fa9e74b29e839b5685fe75d9ce8753`

```dockerfile
```

-	Layers:
	-	`sha256:bb3cb4e84b32a03504d2d7e1ce7e3050803c44d79b30ee9477afb287fd830d63`  
		Last Modified: Tue, 14 Jan 2025 02:17:33 GMT  
		Size: 2.6 MB (2626125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d728d06dec7bc50355f141c1d225b2dabb4290b72f599f57f4f70d0143a3683`  
		Last Modified: Tue, 14 Jan 2025 02:17:33 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:c2396135f5da400e6dacfbfed38c92e5d937e51ccea665ed963fbff89c928525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46994901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c07c0f93042310c4ee4a59e341d4dde31d0e0617f3640561db059d64bf56703`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8342b9d830b235f12b97f672094236abbfa26f61b2b7854c2db3819643e69c1c`  
		Last Modified: Tue, 14 Jan 2025 06:38:08 GMT  
		Size: 9.6 MB (9588624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7372fc88445fa517d4204c45e13ac32107d047cc2c5b02da38d7398770bcf449`  
		Last Modified: Tue, 14 Jan 2025 22:56:37 GMT  
		Size: 2.7 KB (2671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995f3b184f7093532fc8f2aee0185bd1137957864793b006448f54ffac848bca`  
		Last Modified: Tue, 14 Jan 2025 06:38:08 GMT  
		Size: 9.4 MB (9362481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2235f7889880ae2e929574a1eb8d1de0ee609c98e4e8034a304b5084609f35b3`  
		Last Modified: Tue, 14 Jan 2025 06:38:08 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:7a955c9cd2ad1ce3ef802a85e6ce7906cf7b030d34a394b55726b7215843e3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6193f81ba3274241556070a632f97c031c918d2ed4d115948d47ab52b9564e09`

```dockerfile
```

-	Layers:
	-	`sha256:3342b9f8ed459de1be3985f083910d2df5af80eab52f6cdefff932cfff0ed974`  
		Last Modified: Tue, 14 Jan 2025 06:38:08 GMT  
		Size: 2.6 MB (2626460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c52f8601bc631ecbac7abe7a626c25d90763db929f8e07c75185102f9ec376`  
		Last Modified: Tue, 14 Jan 2025 06:38:08 GMT  
		Size: 13.6 KB (13628 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:53791ce39a3bb561fd69e4d1b4e4bbb43eef112d6a01c82b251dbdeba7c96049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45454479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031e2224b93caba58bf7986776c7180d28d2777a8a8cde80ca379a23c38c9c86`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
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
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ab9e5c0b240697d08d36dda903448142c4117366f5258f43505a880c1ab903`  
		Last Modified: Tue, 14 Jan 2025 04:48:50 GMT  
		Size: 9.3 MB (9289503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a800dd90c42dba6d5dfe85119877bc22817a06cc701a6a18a4890f6ce26a24`  
		Last Modified: Tue, 14 Jan 2025 04:48:50 GMT  
		Size: 2.7 KB (2672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb5c3d96ce67a977b3333f98368330fbc59fc1adbc20066ef72e3696e81b2a4`  
		Last Modified: Tue, 14 Jan 2025 04:48:50 GMT  
		Size: 9.3 MB (9303472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0d3110ed94e5cd8bb694f0b19c06e4307b0c95076c6e70fce88001051e1836`  
		Last Modified: Tue, 14 Jan 2025 04:48:50 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:8fc6e286098f939e25e48b01478138e291f71226006056e116d316a4d57de829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2638666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450fc051c6010d74c38b544b1ec44dc8989c8f55b30f68995582a59cb7c83bca`

```dockerfile
```

-	Layers:
	-	`sha256:6d8ca72902b1989bdfde574201a92c699153bf28211b9358862731e4d2df3717`  
		Last Modified: Tue, 14 Jan 2025 04:48:51 GMT  
		Size: 2.6 MB (2625219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1cb220b79e802c33143b3f05d9e3ecc72f728adfe219d08ac6e4dae23892b9b`  
		Last Modified: Tue, 14 Jan 2025 04:48:50 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json
