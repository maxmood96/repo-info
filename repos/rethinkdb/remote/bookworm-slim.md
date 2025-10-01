## `rethinkdb:bookworm-slim`

```console
$ docker pull rethinkdb@sha256:020c7cf551d11897db254b8d9d2882e66baaef2c535b4d57be5851ba303481bb
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
$ docker pull rethinkdb@sha256:5a18e673ce85f3ef619dae1ff5d007aac763a3be8da9d8268ae553d6a9553792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6c829515e216481c4bf4ff1254c815e142c8c185514b757a8165e583e2993c`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21178eaa9ee52ef9aeb518bbe7298d50ea4db803734e34250d6899297757eaf`  
		Last Modified: Tue, 30 Sep 2025 01:05:05 GMT  
		Size: 9.8 MB (9797341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a40a5bc2fe437f2b0280daceb165e2a627bce07891a4f55bcd8241d9971bd6`  
		Last Modified: Tue, 30 Sep 2025 00:25:13 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5490cb8d309240642f1897831c644827ce471aebaa68a8f05df988bf3f78abc`  
		Last Modified: Tue, 30 Sep 2025 01:05:07 GMT  
		Size: 10.0 MB (9993135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00085c9c88c2277759525e6fa7dd05c92ff43c5b4e2b7d7018467ecf723f2141`  
		Last Modified: Tue, 30 Sep 2025 00:25:16 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:f4210cbcaf6a033f2a9e5a3d583bbdd8f15fbf41dcd4e9f7a214ed88583baf63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011236d719b67dfc54b23510f46199e819c7a772990d1b6e5c69502fda864c0b`

```dockerfile
```

-	Layers:
	-	`sha256:1f509e54e78c57161cdfa3bf94b9776f852b0ae94c050fd2fc0e844f823b41ee`  
		Last Modified: Tue, 30 Sep 2025 01:03:18 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1daa488e0e504cbf08110ce934f59f68cd8b82a637ae63fecab4a4afc874e89`  
		Last Modified: Tue, 30 Sep 2025 01:03:19 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:277c04c62b163225dcbe6048562b38a849e62191569e825b288792c9b1371e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536350e22afda81b9a6b5a61189e0c60af1914b7a61b27cf9b78d74be38d2156`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b95cd747690d3966db74c005b579dc0acc5d3d5dd2dc3953aa1b7fc6b2c3319`  
		Last Modified: Tue, 30 Sep 2025 00:13:07 GMT  
		Size: 9.6 MB (9627792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140f894af5ccfce1600e9ef1aec68862bb572a6c05cdaf4fe21f8d4f59adcd0f`  
		Last Modified: Tue, 30 Sep 2025 00:13:05 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c50f1aecdff6d3a90c06de0fa3b75ae6a7ef656f55abe521fc8033315d90446`  
		Last Modified: Tue, 30 Sep 2025 00:13:07 GMT  
		Size: 9.4 MB (9362962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e887eb8931bbe87cbc8ec34c5adb7da8dad6c5c8ed818299f0dc3aefbf0003ff`  
		Last Modified: Tue, 30 Sep 2025 00:13:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:f7ec9f740563e67cbccc3b78c217fc472bbf798c083777a623e2dc6e6a1fdf78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2799000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052ad9a18c0162e5dbf41510ff9dd35c41d913460032c24a43f64d63732f362a`

```dockerfile
```

-	Layers:
	-	`sha256:d1c79bfa1ad00c0f524d4aaf49281ab7c0fe084f4b6013dffa63826cd5c179a8`  
		Last Modified: Tue, 30 Sep 2025 13:03:23 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97fe6b31b7b04136764c6a2d82e2fc70e8ddf4fd6343212e0e0546f41ef822ef`  
		Last Modified: Tue, 30 Sep 2025 13:03:24 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:b770845b090bdf4639b77e9ee12369c9afd92d0e282dd57b610263afe968d0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308633830b96b68c5e07b96af72381ce77d6415d05bfad34b467b58206c6bcee`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
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
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf662b355e5de86c77256adfc954dee5cce6d2614fe72443febe2fb16f03ce1`  
		Last Modified: Tue, 09 Sep 2025 01:21:27 GMT  
		Size: 9.3 MB (9296844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a076e924a1e934ba26a0477f279dcf0c91b124a74e84c92dcf8c970fd95a2d14`  
		Last Modified: Tue, 09 Sep 2025 00:53:46 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee77faf040dd79cc41c07f3f5e3c9b3335482f517928bb76c6bb570867c58bab`  
		Last Modified: Tue, 09 Sep 2025 01:21:25 GMT  
		Size: 9.3 MB (9303766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab61c038a36813ec9a6b71c15912c6dd0d4dbcc0c3bec31648e33e0aa7f729a`  
		Last Modified: Tue, 09 Sep 2025 00:53:45 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:87f61dfde84994957f259312ed2a2ba492ec19caa3dbc9b5c3c5314d15f63999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16d1599331cfe7b05e6902e1c35ccf267c455ec2c400785796ebdf14afcdfec`

```dockerfile
```

-	Layers:
	-	`sha256:04d7b61e68a2079826165d956ef71a101cbe1d7545e1d12282ba8db1a9b0e382`  
		Last Modified: Tue, 09 Sep 2025 04:03:24 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5732513c7fc613ec19236210a049ce07a1453a231eb3fed0f69af2830533d970`  
		Last Modified: Tue, 09 Sep 2025 04:03:24 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json
