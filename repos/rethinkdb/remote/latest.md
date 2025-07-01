## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:07d069e3ea7a835daf31f3f69438fee5707d7b5db0d5800e47bad3edc12b2e56
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
$ docker pull rethinkdb@sha256:c02994a66debb9c42204ce5e6ceb15687a597ffffe773cf12f02a2a88ec20f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48020761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965be68736528e41f7e3fb1e03869be919337ad0f53531b42f2d37d0c786c7cb`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfab3a5b4090702540debf3b3b5167a6a61071d9f00d104ff5d6d9726b011b21`  
		Last Modified: Tue, 01 Jul 2025 02:24:59 GMT  
		Size: 9.8 MB (9795011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e844dfe49d4a0fcf03ff6db31b7d171defd1e014568ea353a576db122040abf9`  
		Last Modified: Tue, 01 Jul 2025 02:24:58 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d19b361d71c49fff9b3863fa889abebb7211d49e356b67eaec7a600eba43799`  
		Last Modified: Tue, 01 Jul 2025 02:24:59 GMT  
		Size: 10.0 MB (9992847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97be8f25ae604c8ae013c763497b5306775064d05b6d92f9108e6b5a18779ba`  
		Last Modified: Tue, 01 Jul 2025 02:24:58 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:027e89c7987aa760c3acfbc4f6829c74a7404a70b7998a56ccd5d25a6b2cd88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2796188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d4a78492a88d97ce62622b7ba410b1518d7f067036933f331d7b4b7c73e02b`

```dockerfile
```

-	Layers:
	-	`sha256:21b1668d8a7ef461f47201d9e2adfd85cde303d541006e1ba43bf3f58ae98107`  
		Last Modified: Tue, 01 Jul 2025 04:03:17 GMT  
		Size: 2.8 MB (2782741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0628af1da5dec632611749147921288755d8223591193e4f9516f7d37f6d944f`  
		Last Modified: Tue, 01 Jul 2025 04:03:18 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:3f14962d8250ce9ad24bab16c7782bfd8d9e544c39aab742c2286d39f3b5f3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47032963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e30f624e812dd326f5e2a82fdc8d16e47de3fb694faad6f64af012a6306ef1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8a011433d3c427a0c26eec72e2fde5f5f4b7b1f0e81011e292bcb0f29b527e`  
		Last Modified: Wed, 11 Jun 2025 02:34:52 GMT  
		Size: 9.6 MB (9589891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02b0b0e94dc8307bd2a7cb995a7e9548c32788cfb0f1070678831d22263e7d7`  
		Last Modified: Wed, 11 Jun 2025 02:34:51 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1599ebd64c17d37175000678d046f6970e068abfcb989c00772eaa4e2613aea6`  
		Last Modified: Wed, 11 Jun 2025 02:34:51 GMT  
		Size: 9.4 MB (9362634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7cc5e7fd8957749e21ba918af08b2d61d016ba2466eee16f26b862b2fb03c0`  
		Last Modified: Wed, 11 Jun 2025 02:34:52 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:0eff4eb5359209b0d7fec4c6c9d4731802cbd90a9158ee66eb6b0d54fbf1b64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2795349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f5f9392e46fa375f4b12a27f2a7e3fd65512b59e6d011102c0267612732361`

```dockerfile
```

-	Layers:
	-	`sha256:68157b7d7e4463a4188bdfef8106efa3b5e8cce9b00a699af9e2fcdf7e9b4cf7`  
		Last Modified: Wed, 11 Jun 2025 04:03:25 GMT  
		Size: 2.8 MB (2781720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87512993611693c48dab1067cf8393d80aeabb6b77f9a5a85eea0bc5ab0508c3`  
		Last Modified: Wed, 11 Jun 2025 04:03:26 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; s390x

```console
$ docker pull rethinkdb@sha256:70da5d41cbfc1abc193ebe8c43bbfe832ec87266f8a0c047aba3414d85a998ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45486874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb415605e956d50fa05962beb2d27de1458dd1a21b28a00351aa2fcb472a0885`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cb38e85a321e10717dd8c23a92bbf7ac7d5152b4b04b6faced3643a465769b`  
		Last Modified: Wed, 11 Jun 2025 02:39:53 GMT  
		Size: 9.3 MB (9292735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83200d3338e9ed15920307f3f0164b3453ca6bb56757c724fb51d67573481e9`  
		Last Modified: Wed, 11 Jun 2025 02:39:52 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b2c521066fbc18b88851f919ff4d5632e1a935fb30ebf548137b2ed945f823`  
		Last Modified: Wed, 11 Jun 2025 02:39:53 GMT  
		Size: 9.3 MB (9303523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42638e964d3c4dd0715cdac4a3c94e06d6301323699c2bc2ae3acbb165a3a37e`  
		Last Modified: Wed, 11 Jun 2025 02:39:52 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:82c86c1e06eed1a074b8a7af85a6fad09df170b0cd57dc24aa4665c337c88238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2791033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cdcd2436b98104c86bd77d9eed29330db04e418510733c1778c6589a6d003c8`

```dockerfile
```

-	Layers:
	-	`sha256:6d2a54d92e8e4a1107ae2fbcafb8b8e275fe30f5adb4d10129b0a530e1e1f4b6`  
		Last Modified: Wed, 11 Jun 2025 04:03:31 GMT  
		Size: 2.8 MB (2777587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9a501ce79e8cc5f6cf3e8f1ac386dd60e0ca3aad4a365bb8ba102c50fd61d88`  
		Last Modified: Wed, 11 Jun 2025 04:03:31 GMT  
		Size: 13.4 KB (13446 bytes)  
		MIME: application/vnd.in-toto+json
