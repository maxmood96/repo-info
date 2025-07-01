## `rethinkdb:2-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:3c9583f9476c3cf65c58656fef0d84526255231fdf1b8c9f99d42cc73d64552f
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

### `rethinkdb:2-bookworm-slim` - unknown; unknown

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

### `rethinkdb:2-bookworm-slim` - linux; arm64 variant v8

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

### `rethinkdb:2-bookworm-slim` - unknown; unknown

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

### `rethinkdb:2-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:09e40e75dea04aa229df4e2cdecf9fbed834d2c496c66f999a6fabb4aeaead9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45489001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9c6ba5ec052281b30b93a3d05aba682b3743802bcc33020321a2f3a209c6f8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
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
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5847fb9b069f59d4ce66168c1f54a4dbe670f73d4331e65574cca7882cdd2b9f`  
		Last Modified: Tue, 01 Jul 2025 07:15:15 GMT  
		Size: 9.3 MB (9294841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edfadc81db7c966fef3b3dacd9eb5b5608b34be6c5e672d8971392ded9fb49a`  
		Last Modified: Tue, 01 Jul 2025 05:28:02 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8007b984f94fc3235b760d53481eacd6f88bb75e4d91b80d7503797cfc28b9f3`  
		Last Modified: Tue, 01 Jul 2025 07:15:18 GMT  
		Size: 9.3 MB (9303589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3d8383d8c1fe16615fb5f5801725d71b4688e1c7494ada35f30109d15e6b4d`  
		Last Modified: Tue, 01 Jul 2025 05:28:04 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:6acf490a8c9915f859f4a13f5ff3ba288db467275aef468929bbbce683181da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2792390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26414e8b813ef16b7ec710ad362f38fdf09a45825e97b8623da1f0fe167b4f6b`

```dockerfile
```

-	Layers:
	-	`sha256:16de27150723681cc73cbca893fdff2c0a92c4d18504925b3e17878c9934fead`  
		Last Modified: Tue, 01 Jul 2025 07:03:24 GMT  
		Size: 2.8 MB (2778943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c56376b28eae1e4eecb292572ca2a98d173f4b35a0cb232562790b7161136ef1`  
		Last Modified: Tue, 01 Jul 2025 07:03:25 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json
