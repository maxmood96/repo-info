## `rethinkdb:2-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:a792c2dcb2135231e857e61ee4aab0797c589ad31777e342cf7dae86ab69ca21
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
$ docker pull rethinkdb@sha256:8c94cc020c6706aa11acfe5acd178a8ab95dcc41d978286938e21b704e0c0679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48017850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759432c629fe2d7beb3c2abacf5b33d5b6d3742f1ed5bd84f516060daa9f01dc`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522c9098de3381526c32c8527ede9b5e7c22d2129c795fa46ef8d780c84ac309`  
		Last Modified: Wed, 11 Jun 2025 01:05:02 GMT  
		Size: 9.8 MB (9792153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa742047c1de1ba742611a6b15b5fbc9b24cd9dad5f1c3009530166f38600338`  
		Last Modified: Wed, 11 Jun 2025 00:04:35 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4b5f5e0760190bcc02a63024b89ad787ccbf66708a60b2de5a2bdbf9dd3032`  
		Last Modified: Wed, 11 Jun 2025 01:05:04 GMT  
		Size: 10.0 MB (9992805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5f4af383ac6a80b7591866853e17bbebe28a34156a48b1d82f63df17e82dee`  
		Last Modified: Wed, 11 Jun 2025 00:04:38 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:74a00baaafe845838f9ddfd283987750c2c65791bb25f8fcce4f9a494a931f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c333dd6d6f28e73ecc933927e6dc84908139ccd8800b0841678eba4291c7354`

```dockerfile
```

-	Layers:
	-	`sha256:86a0de94427d6f94929fa22232098a5498a0c6e4d2c0c94dd4379ba9ee9b38db`  
		Last Modified: Wed, 11 Jun 2025 01:03:19 GMT  
		Size: 2.8 MB (2781385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f2f47178c53d6b7d2f7be6e776c89298d05dc16f51605aca986c5c33bbcf359`  
		Last Modified: Wed, 11 Jun 2025 01:03:20 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:a6f922110fa8c7426d10ed31441ac45c1ed18703836af7a822a49b14533565bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47020454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831c086b345961f7ca51e1b3f6f53030df82c3bdff769bff2ea1edbea418e23e`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb94695bfc030766a66ce0796e55ecef7e7b702be7494d4c7bde5c7b7b046c58`  
		Last Modified: Tue, 03 Jun 2025 14:36:48 GMT  
		Size: 9.6 MB (9589803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a71d090dcf3818f810ad29c2ad46daa4a13f5498a6819fc476031c9f528ed70`  
		Last Modified: Tue, 03 Jun 2025 14:36:46 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1c10d87c07e7b8fd0f74cb1e810480b8154db627969ef54ea2ad9330dbe8a6`  
		Last Modified: Tue, 03 Jun 2025 14:36:46 GMT  
		Size: 9.4 MB (9362609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf17f4e23c69c270e79184e5974fa20ce3efaf49694f160a45eb1db29b68832`  
		Last Modified: Tue, 03 Jun 2025 14:36:46 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:619833f07679d07964c9ea7185ab516de90a23e9dbdaafc40eabc31c9ce69aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2667124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f59453309944f12ede7584f44b963b3f645d3083abbc0d19d716e738b14133`

```dockerfile
```

-	Layers:
	-	`sha256:0692410934cb656b90987e8c5820207bf82af005b846bb9bd4a6dcdcbcd967f2`  
		Last Modified: Tue, 10 Jun 2025 03:12:38 GMT  
		Size: 2.7 MB (2653495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aabc87525136ea07e1c85ae840a616878a77f87724b52b4a73cd27817cf40a5`  
		Last Modified: Tue, 10 Jun 2025 03:12:40 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:d6334638a23241246ec413b1419f3ebb1fbc309d2dfeb5fbaf56773f45cbaaae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45481908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85086822907076eac6a822c85c5d47c51c7845a599ad533105c7d12b685736d8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457be9c2126e4fdd01cec5c728a279168eb0b50e87c83df6011eb3aaa3493fc5`  
		Last Modified: Tue, 10 Jun 2025 03:12:51 GMT  
		Size: 9.3 MB (9292732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fc7bf661ca4d2459b2c23bdc4262c5cdcf37653a63f9ef1ebed864503c4714`  
		Last Modified: Tue, 10 Jun 2025 03:12:54 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17dabc9e1d040f108b78cd9128cf25930b5b2fa3cdec3ab0c06169aa7e12be87`  
		Last Modified: Tue, 10 Jun 2025 03:12:57 GMT  
		Size: 9.3 MB (9303609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c3518847a4038bfa159b0ed74ae77277be50df52fb7edd322281579e8492a9`  
		Last Modified: Tue, 10 Jun 2025 03:12:59 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:0a836ee62a61ef36a6d22b15c9dbaf01fb1afeb129ee62393367b50a0a12c950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8b0247d9a9e53d09bf798962871f9cffa95311ca7854fdebecd3b594b281d7`

```dockerfile
```

-	Layers:
	-	`sha256:c9d91beee6b09b4f16b10faaf1b3e188a964a5fe1b16f54d89f208824aea65b1`  
		Last Modified: Tue, 10 Jun 2025 03:13:15 GMT  
		Size: 2.7 MB (2652254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41069d10932dd748b79f80130bc20b6a4c68c5216d0ae09e870d6d9332be46b4`  
		Last Modified: Tue, 10 Jun 2025 03:13:18 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json
