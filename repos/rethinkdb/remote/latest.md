## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:f1b739464abe0a5986d95d22808b0ede3f24dda8cbea9e74cce779a0af26193d
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
$ docker pull rethinkdb@sha256:0bec186c6c281d5af12611f13a2f21d2f9472ebf8532a7aafff93decf2d636b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47998898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f99af8ae10a4da95d3dd31ba673f50580d231439684f4f89e6b028daf20aeb9`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a19be0f7ddb65ea57285bbae7c005b8cb0172492f03a4129d3b08a21cfd5ad`  
		Last Modified: Tue, 04 Feb 2025 04:23:40 GMT  
		Size: 9.8 MB (9791131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a590901055b4b24c3f1ad44581c0ff92405e99985571c2728a6fff20c5988be`  
		Last Modified: Tue, 04 Feb 2025 04:23:40 GMT  
		Size: 2.7 KB (2672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5553a6a13d52e0f3a174abdeaf8f3333436513d8ae75ac9086b1471b2ca8043b`  
		Last Modified: Tue, 04 Feb 2025 04:23:40 GMT  
		Size: 10.0 MB (9992698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b26ec635460215c7ad415947b656b33e40fb53d4a505879195d4fa06552dc6c`  
		Last Modified: Tue, 04 Feb 2025 04:23:40 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:a194b5c7541a1320f35cd453d73b6871b7ac50ceb4cb8205f7ea688d8f115c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2639571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80dc72e577332dcc0668c7acd8213347595e28675ffd17416be8516ca781905b`

```dockerfile
```

-	Layers:
	-	`sha256:c37a2814c6e32182ad9770966004ea02718fb21a30e7a84ffcd7225a2fbbb03f`  
		Last Modified: Tue, 04 Feb 2025 04:23:40 GMT  
		Size: 2.6 MB (2626125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b420da9b71c7f6125401bf1a23467edf554e812b4eccb61fbaf856984f65bd33`  
		Last Modified: Tue, 04 Feb 2025 04:23:40 GMT  
		Size: 13.4 KB (13446 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; arm64 variant v8

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
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8342b9d830b235f12b97f672094236abbfa26f61b2b7854c2db3819643e69c1c`  
		Last Modified: Tue, 14 Jan 2025 06:38:08 GMT  
		Size: 9.6 MB (9588624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7372fc88445fa517d4204c45e13ac32107d047cc2c5b02da38d7398770bcf449`  
		Last Modified: Tue, 14 Jan 2025 06:38:08 GMT  
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

### `rethinkdb:latest` - unknown; unknown

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

### `rethinkdb:latest` - linux; s390x

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

### `rethinkdb:latest` - unknown; unknown

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
