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
$ docker pull rethinkdb@sha256:11378bdfcc055393ce2da3fe24de738869891ead462392a92a4da7953bd80928
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
$ docker pull rethinkdb@sha256:8f7423dd1f41a688b80bb0e1887b43762c320f03ae9796e7e7c2b480b931ac95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53b431f52c4c559b5ccd1d32c233f6d61e7298a5af346a11680688a48429333`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d9ce707ef17f4c8fd60d5058c3abacfb2e7f9774483e03c5c0423a4ffb9759`  
		Last Modified: Mon, 08 Sep 2025 22:05:06 GMT  
		Size: 9.8 MB (9797279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34f32bf54faf3386fbe830874347f40a5cda2b2c2e5c539bcd188f9331c7ea8`  
		Last Modified: Mon, 08 Sep 2025 21:42:41 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896ac436f91ce527089294d5b257078b3c3688dc064eaa7c5cfcf2025e0e4593`  
		Last Modified: Mon, 08 Sep 2025 22:05:07 GMT  
		Size: 10.0 MB (9993087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fed90b7a046dc8e7dd5803feeaf73a818682990571ecb7b30410b6adc241a7`  
		Last Modified: Mon, 08 Sep 2025 21:42:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:69f02a2de1a801ed95573f2b3c284421dae13fd0c6fc0e54c10440cd278a5d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034d2d992a02976531f60469827b4d496c7efc0a6cad0afc6333dc2fa3f3b98f`

```dockerfile
```

-	Layers:
	-	`sha256:5d03657237ab4df91bf7114fa3846ab459916737dd580df86bc86398397e0a08`  
		Last Modified: Mon, 08 Sep 2025 22:03:21 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bd3d65adcd873ba27eb553c87828e17c94a84781455c96c415b970cffeb2106`  
		Last Modified: Mon, 08 Sep 2025 22:03:22 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:f473360bea40a8efb96a01b4b50e9af896c177ee5ba4bb826f0e673f69b2a3cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f6c60ed54f95b2cbdbce39e2ce1d7e928b0992badafcb46767929c5133dac2`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b9ee04b8a9ae158f121f72948c36e732641afad1f1f9a0ed789384bff7d0cb`  
		Last Modified: Mon, 08 Sep 2025 22:05:12 GMT  
		Size: 9.6 MB (9627773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485a83ba6b46c686ab541c8a03d6ecec6ffe043910b812ee403d6bc880f8eefd`  
		Last Modified: Mon, 08 Sep 2025 22:05:12 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70ebfe6e003c63f8337966d941bb8d96c33c1eafc09551f32133a5478dd47cb`  
		Last Modified: Mon, 08 Sep 2025 22:05:14 GMT  
		Size: 9.4 MB (9362877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b1d52472a5577af2fb30f3d6944b5b750283110d695145d7ba9c995f9fba41`  
		Last Modified: Mon, 08 Sep 2025 22:05:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:54fb283582da8a5388612e9e86b608305d073ebdb1e2e3bc531af4b73cbe9b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2799000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c3cb04def3c579bac4ee8cbb5246c9d3ec6817795c3521a1560623c67f2db1`

```dockerfile
```

-	Layers:
	-	`sha256:198bc7a4ac37485fe88820d0a6bc2db673295a04f632bd28d75454c70a95a5f0`  
		Last Modified: Mon, 08 Sep 2025 22:03:27 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:581a3dfe90fe51f489d54879d2dc8d1bb20e5a969740c06e4dd3b8ef3c8315aa`  
		Last Modified: Mon, 08 Sep 2025 22:03:28 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2` - linux; s390x

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

### `rethinkdb:2` - unknown; unknown

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

## `rethinkdb:2-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:11378bdfcc055393ce2da3fe24de738869891ead462392a92a4da7953bd80928
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
$ docker pull rethinkdb@sha256:8f7423dd1f41a688b80bb0e1887b43762c320f03ae9796e7e7c2b480b931ac95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53b431f52c4c559b5ccd1d32c233f6d61e7298a5af346a11680688a48429333`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d9ce707ef17f4c8fd60d5058c3abacfb2e7f9774483e03c5c0423a4ffb9759`  
		Last Modified: Mon, 08 Sep 2025 22:05:06 GMT  
		Size: 9.8 MB (9797279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34f32bf54faf3386fbe830874347f40a5cda2b2c2e5c539bcd188f9331c7ea8`  
		Last Modified: Mon, 08 Sep 2025 21:42:41 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896ac436f91ce527089294d5b257078b3c3688dc064eaa7c5cfcf2025e0e4593`  
		Last Modified: Mon, 08 Sep 2025 22:05:07 GMT  
		Size: 10.0 MB (9993087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fed90b7a046dc8e7dd5803feeaf73a818682990571ecb7b30410b6adc241a7`  
		Last Modified: Mon, 08 Sep 2025 21:42:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:69f02a2de1a801ed95573f2b3c284421dae13fd0c6fc0e54c10440cd278a5d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034d2d992a02976531f60469827b4d496c7efc0a6cad0afc6333dc2fa3f3b98f`

```dockerfile
```

-	Layers:
	-	`sha256:5d03657237ab4df91bf7114fa3846ab459916737dd580df86bc86398397e0a08`  
		Last Modified: Mon, 08 Sep 2025 22:03:21 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bd3d65adcd873ba27eb553c87828e17c94a84781455c96c415b970cffeb2106`  
		Last Modified: Mon, 08 Sep 2025 22:03:22 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:f473360bea40a8efb96a01b4b50e9af896c177ee5ba4bb826f0e673f69b2a3cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f6c60ed54f95b2cbdbce39e2ce1d7e928b0992badafcb46767929c5133dac2`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b9ee04b8a9ae158f121f72948c36e732641afad1f1f9a0ed789384bff7d0cb`  
		Last Modified: Mon, 08 Sep 2025 22:05:12 GMT  
		Size: 9.6 MB (9627773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485a83ba6b46c686ab541c8a03d6ecec6ffe043910b812ee403d6bc880f8eefd`  
		Last Modified: Mon, 08 Sep 2025 22:05:12 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70ebfe6e003c63f8337966d941bb8d96c33c1eafc09551f32133a5478dd47cb`  
		Last Modified: Mon, 08 Sep 2025 22:05:14 GMT  
		Size: 9.4 MB (9362877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b1d52472a5577af2fb30f3d6944b5b750283110d695145d7ba9c995f9fba41`  
		Last Modified: Mon, 08 Sep 2025 22:05:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:54fb283582da8a5388612e9e86b608305d073ebdb1e2e3bc531af4b73cbe9b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2799000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c3cb04def3c579bac4ee8cbb5246c9d3ec6817795c3521a1560623c67f2db1`

```dockerfile
```

-	Layers:
	-	`sha256:198bc7a4ac37485fe88820d0a6bc2db673295a04f632bd28d75454c70a95a5f0`  
		Last Modified: Mon, 08 Sep 2025 22:03:27 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:581a3dfe90fe51f489d54879d2dc8d1bb20e5a969740c06e4dd3b8ef3c8315aa`  
		Last Modified: Mon, 08 Sep 2025 22:03:28 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; s390x

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

### `rethinkdb:2-bookworm-slim` - unknown; unknown

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

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:11378bdfcc055393ce2da3fe24de738869891ead462392a92a4da7953bd80928
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
$ docker pull rethinkdb@sha256:8f7423dd1f41a688b80bb0e1887b43762c320f03ae9796e7e7c2b480b931ac95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53b431f52c4c559b5ccd1d32c233f6d61e7298a5af346a11680688a48429333`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d9ce707ef17f4c8fd60d5058c3abacfb2e7f9774483e03c5c0423a4ffb9759`  
		Last Modified: Mon, 08 Sep 2025 22:05:06 GMT  
		Size: 9.8 MB (9797279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34f32bf54faf3386fbe830874347f40a5cda2b2c2e5c539bcd188f9331c7ea8`  
		Last Modified: Mon, 08 Sep 2025 21:42:41 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896ac436f91ce527089294d5b257078b3c3688dc064eaa7c5cfcf2025e0e4593`  
		Last Modified: Mon, 08 Sep 2025 22:05:07 GMT  
		Size: 10.0 MB (9993087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fed90b7a046dc8e7dd5803feeaf73a818682990571ecb7b30410b6adc241a7`  
		Last Modified: Mon, 08 Sep 2025 21:42:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:69f02a2de1a801ed95573f2b3c284421dae13fd0c6fc0e54c10440cd278a5d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034d2d992a02976531f60469827b4d496c7efc0a6cad0afc6333dc2fa3f3b98f`

```dockerfile
```

-	Layers:
	-	`sha256:5d03657237ab4df91bf7114fa3846ab459916737dd580df86bc86398397e0a08`  
		Last Modified: Mon, 08 Sep 2025 22:03:21 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bd3d65adcd873ba27eb553c87828e17c94a84781455c96c415b970cffeb2106`  
		Last Modified: Mon, 08 Sep 2025 22:03:22 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:f473360bea40a8efb96a01b4b50e9af896c177ee5ba4bb826f0e673f69b2a3cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f6c60ed54f95b2cbdbce39e2ce1d7e928b0992badafcb46767929c5133dac2`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b9ee04b8a9ae158f121f72948c36e732641afad1f1f9a0ed789384bff7d0cb`  
		Last Modified: Mon, 08 Sep 2025 22:05:12 GMT  
		Size: 9.6 MB (9627773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485a83ba6b46c686ab541c8a03d6ecec6ffe043910b812ee403d6bc880f8eefd`  
		Last Modified: Mon, 08 Sep 2025 22:05:12 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70ebfe6e003c63f8337966d941bb8d96c33c1eafc09551f32133a5478dd47cb`  
		Last Modified: Mon, 08 Sep 2025 22:05:14 GMT  
		Size: 9.4 MB (9362877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b1d52472a5577af2fb30f3d6944b5b750283110d695145d7ba9c995f9fba41`  
		Last Modified: Mon, 08 Sep 2025 22:05:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:54fb283582da8a5388612e9e86b608305d073ebdb1e2e3bc531af4b73cbe9b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2799000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c3cb04def3c579bac4ee8cbb5246c9d3ec6817795c3521a1560623c67f2db1`

```dockerfile
```

-	Layers:
	-	`sha256:198bc7a4ac37485fe88820d0a6bc2db673295a04f632bd28d75454c70a95a5f0`  
		Last Modified: Mon, 08 Sep 2025 22:03:27 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:581a3dfe90fe51f489d54879d2dc8d1bb20e5a969740c06e4dd3b8ef3c8315aa`  
		Last Modified: Mon, 08 Sep 2025 22:03:28 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4` - linux; s390x

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

### `rethinkdb:2.4` - unknown; unknown

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

## `rethinkdb:2.4-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:11378bdfcc055393ce2da3fe24de738869891ead462392a92a4da7953bd80928
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
$ docker pull rethinkdb@sha256:8f7423dd1f41a688b80bb0e1887b43762c320f03ae9796e7e7c2b480b931ac95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53b431f52c4c559b5ccd1d32c233f6d61e7298a5af346a11680688a48429333`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d9ce707ef17f4c8fd60d5058c3abacfb2e7f9774483e03c5c0423a4ffb9759`  
		Last Modified: Mon, 08 Sep 2025 22:05:06 GMT  
		Size: 9.8 MB (9797279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34f32bf54faf3386fbe830874347f40a5cda2b2c2e5c539bcd188f9331c7ea8`  
		Last Modified: Mon, 08 Sep 2025 21:42:41 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896ac436f91ce527089294d5b257078b3c3688dc064eaa7c5cfcf2025e0e4593`  
		Last Modified: Mon, 08 Sep 2025 22:05:07 GMT  
		Size: 10.0 MB (9993087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fed90b7a046dc8e7dd5803feeaf73a818682990571ecb7b30410b6adc241a7`  
		Last Modified: Mon, 08 Sep 2025 21:42:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:69f02a2de1a801ed95573f2b3c284421dae13fd0c6fc0e54c10440cd278a5d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034d2d992a02976531f60469827b4d496c7efc0a6cad0afc6333dc2fa3f3b98f`

```dockerfile
```

-	Layers:
	-	`sha256:5d03657237ab4df91bf7114fa3846ab459916737dd580df86bc86398397e0a08`  
		Last Modified: Mon, 08 Sep 2025 22:03:21 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bd3d65adcd873ba27eb553c87828e17c94a84781455c96c415b970cffeb2106`  
		Last Modified: Mon, 08 Sep 2025 22:03:22 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:f473360bea40a8efb96a01b4b50e9af896c177ee5ba4bb826f0e673f69b2a3cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f6c60ed54f95b2cbdbce39e2ce1d7e928b0992badafcb46767929c5133dac2`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b9ee04b8a9ae158f121f72948c36e732641afad1f1f9a0ed789384bff7d0cb`  
		Last Modified: Mon, 08 Sep 2025 22:05:12 GMT  
		Size: 9.6 MB (9627773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485a83ba6b46c686ab541c8a03d6ecec6ffe043910b812ee403d6bc880f8eefd`  
		Last Modified: Mon, 08 Sep 2025 22:05:12 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70ebfe6e003c63f8337966d941bb8d96c33c1eafc09551f32133a5478dd47cb`  
		Last Modified: Mon, 08 Sep 2025 22:05:14 GMT  
		Size: 9.4 MB (9362877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b1d52472a5577af2fb30f3d6944b5b750283110d695145d7ba9c995f9fba41`  
		Last Modified: Mon, 08 Sep 2025 22:05:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:54fb283582da8a5388612e9e86b608305d073ebdb1e2e3bc531af4b73cbe9b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2799000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c3cb04def3c579bac4ee8cbb5246c9d3ec6817795c3521a1560623c67f2db1`

```dockerfile
```

-	Layers:
	-	`sha256:198bc7a4ac37485fe88820d0a6bc2db673295a04f632bd28d75454c70a95a5f0`  
		Last Modified: Mon, 08 Sep 2025 22:03:27 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:581a3dfe90fe51f489d54879d2dc8d1bb20e5a969740c06e4dd3b8ef3c8315aa`  
		Last Modified: Mon, 08 Sep 2025 22:03:28 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4-bookworm-slim` - linux; s390x

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

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

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

## `rethinkdb:2.4.3`

```console
$ docker pull rethinkdb@sha256:11378bdfcc055393ce2da3fe24de738869891ead462392a92a4da7953bd80928
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
$ docker pull rethinkdb@sha256:8f7423dd1f41a688b80bb0e1887b43762c320f03ae9796e7e7c2b480b931ac95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53b431f52c4c559b5ccd1d32c233f6d61e7298a5af346a11680688a48429333`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d9ce707ef17f4c8fd60d5058c3abacfb2e7f9774483e03c5c0423a4ffb9759`  
		Last Modified: Mon, 08 Sep 2025 22:05:06 GMT  
		Size: 9.8 MB (9797279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34f32bf54faf3386fbe830874347f40a5cda2b2c2e5c539bcd188f9331c7ea8`  
		Last Modified: Mon, 08 Sep 2025 21:42:41 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896ac436f91ce527089294d5b257078b3c3688dc064eaa7c5cfcf2025e0e4593`  
		Last Modified: Mon, 08 Sep 2025 22:05:07 GMT  
		Size: 10.0 MB (9993087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fed90b7a046dc8e7dd5803feeaf73a818682990571ecb7b30410b6adc241a7`  
		Last Modified: Mon, 08 Sep 2025 21:42:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:69f02a2de1a801ed95573f2b3c284421dae13fd0c6fc0e54c10440cd278a5d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034d2d992a02976531f60469827b4d496c7efc0a6cad0afc6333dc2fa3f3b98f`

```dockerfile
```

-	Layers:
	-	`sha256:5d03657237ab4df91bf7114fa3846ab459916737dd580df86bc86398397e0a08`  
		Last Modified: Mon, 08 Sep 2025 22:03:21 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bd3d65adcd873ba27eb553c87828e17c94a84781455c96c415b970cffeb2106`  
		Last Modified: Mon, 08 Sep 2025 22:03:22 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.3` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:f473360bea40a8efb96a01b4b50e9af896c177ee5ba4bb826f0e673f69b2a3cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f6c60ed54f95b2cbdbce39e2ce1d7e928b0992badafcb46767929c5133dac2`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b9ee04b8a9ae158f121f72948c36e732641afad1f1f9a0ed789384bff7d0cb`  
		Last Modified: Mon, 08 Sep 2025 22:05:12 GMT  
		Size: 9.6 MB (9627773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485a83ba6b46c686ab541c8a03d6ecec6ffe043910b812ee403d6bc880f8eefd`  
		Last Modified: Mon, 08 Sep 2025 22:05:12 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70ebfe6e003c63f8337966d941bb8d96c33c1eafc09551f32133a5478dd47cb`  
		Last Modified: Mon, 08 Sep 2025 22:05:14 GMT  
		Size: 9.4 MB (9362877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b1d52472a5577af2fb30f3d6944b5b750283110d695145d7ba9c995f9fba41`  
		Last Modified: Mon, 08 Sep 2025 22:05:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:54fb283582da8a5388612e9e86b608305d073ebdb1e2e3bc531af4b73cbe9b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2799000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c3cb04def3c579bac4ee8cbb5246c9d3ec6817795c3521a1560623c67f2db1`

```dockerfile
```

-	Layers:
	-	`sha256:198bc7a4ac37485fe88820d0a6bc2db673295a04f632bd28d75454c70a95a5f0`  
		Last Modified: Mon, 08 Sep 2025 22:03:27 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:581a3dfe90fe51f489d54879d2dc8d1bb20e5a969740c06e4dd3b8ef3c8315aa`  
		Last Modified: Mon, 08 Sep 2025 22:03:28 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.3` - linux; s390x

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

### `rethinkdb:2.4.3` - unknown; unknown

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

## `rethinkdb:2.4.4-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:11378bdfcc055393ce2da3fe24de738869891ead462392a92a4da7953bd80928
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
$ docker pull rethinkdb@sha256:8f7423dd1f41a688b80bb0e1887b43762c320f03ae9796e7e7c2b480b931ac95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53b431f52c4c559b5ccd1d32c233f6d61e7298a5af346a11680688a48429333`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d9ce707ef17f4c8fd60d5058c3abacfb2e7f9774483e03c5c0423a4ffb9759`  
		Last Modified: Mon, 08 Sep 2025 22:05:06 GMT  
		Size: 9.8 MB (9797279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34f32bf54faf3386fbe830874347f40a5cda2b2c2e5c539bcd188f9331c7ea8`  
		Last Modified: Mon, 08 Sep 2025 21:42:41 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896ac436f91ce527089294d5b257078b3c3688dc064eaa7c5cfcf2025e0e4593`  
		Last Modified: Mon, 08 Sep 2025 22:05:07 GMT  
		Size: 10.0 MB (9993087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fed90b7a046dc8e7dd5803feeaf73a818682990571ecb7b30410b6adc241a7`  
		Last Modified: Mon, 08 Sep 2025 21:42:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:69f02a2de1a801ed95573f2b3c284421dae13fd0c6fc0e54c10440cd278a5d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034d2d992a02976531f60469827b4d496c7efc0a6cad0afc6333dc2fa3f3b98f`

```dockerfile
```

-	Layers:
	-	`sha256:5d03657237ab4df91bf7114fa3846ab459916737dd580df86bc86398397e0a08`  
		Last Modified: Mon, 08 Sep 2025 22:03:21 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bd3d65adcd873ba27eb553c87828e17c94a84781455c96c415b970cffeb2106`  
		Last Modified: Mon, 08 Sep 2025 22:03:22 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.4-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:f473360bea40a8efb96a01b4b50e9af896c177ee5ba4bb826f0e673f69b2a3cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f6c60ed54f95b2cbdbce39e2ce1d7e928b0992badafcb46767929c5133dac2`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b9ee04b8a9ae158f121f72948c36e732641afad1f1f9a0ed789384bff7d0cb`  
		Last Modified: Mon, 08 Sep 2025 22:05:12 GMT  
		Size: 9.6 MB (9627773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485a83ba6b46c686ab541c8a03d6ecec6ffe043910b812ee403d6bc880f8eefd`  
		Last Modified: Mon, 08 Sep 2025 22:05:12 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70ebfe6e003c63f8337966d941bb8d96c33c1eafc09551f32133a5478dd47cb`  
		Last Modified: Mon, 08 Sep 2025 22:05:14 GMT  
		Size: 9.4 MB (9362877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b1d52472a5577af2fb30f3d6944b5b750283110d695145d7ba9c995f9fba41`  
		Last Modified: Mon, 08 Sep 2025 22:05:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:54fb283582da8a5388612e9e86b608305d073ebdb1e2e3bc531af4b73cbe9b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2799000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c3cb04def3c579bac4ee8cbb5246c9d3ec6817795c3521a1560623c67f2db1`

```dockerfile
```

-	Layers:
	-	`sha256:198bc7a4ac37485fe88820d0a6bc2db673295a04f632bd28d75454c70a95a5f0`  
		Last Modified: Mon, 08 Sep 2025 22:03:27 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:581a3dfe90fe51f489d54879d2dc8d1bb20e5a969740c06e4dd3b8ef3c8315aa`  
		Last Modified: Mon, 08 Sep 2025 22:03:28 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.4-bookworm-slim` - linux; s390x

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

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

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

## `rethinkdb:bookworm-slim`

```console
$ docker pull rethinkdb@sha256:11378bdfcc055393ce2da3fe24de738869891ead462392a92a4da7953bd80928
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
$ docker pull rethinkdb@sha256:8f7423dd1f41a688b80bb0e1887b43762c320f03ae9796e7e7c2b480b931ac95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53b431f52c4c559b5ccd1d32c233f6d61e7298a5af346a11680688a48429333`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d9ce707ef17f4c8fd60d5058c3abacfb2e7f9774483e03c5c0423a4ffb9759`  
		Last Modified: Mon, 08 Sep 2025 22:05:06 GMT  
		Size: 9.8 MB (9797279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34f32bf54faf3386fbe830874347f40a5cda2b2c2e5c539bcd188f9331c7ea8`  
		Last Modified: Mon, 08 Sep 2025 21:42:41 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896ac436f91ce527089294d5b257078b3c3688dc064eaa7c5cfcf2025e0e4593`  
		Last Modified: Mon, 08 Sep 2025 22:05:07 GMT  
		Size: 10.0 MB (9993087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fed90b7a046dc8e7dd5803feeaf73a818682990571ecb7b30410b6adc241a7`  
		Last Modified: Mon, 08 Sep 2025 21:42:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:69f02a2de1a801ed95573f2b3c284421dae13fd0c6fc0e54c10440cd278a5d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034d2d992a02976531f60469827b4d496c7efc0a6cad0afc6333dc2fa3f3b98f`

```dockerfile
```

-	Layers:
	-	`sha256:5d03657237ab4df91bf7114fa3846ab459916737dd580df86bc86398397e0a08`  
		Last Modified: Mon, 08 Sep 2025 22:03:21 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bd3d65adcd873ba27eb553c87828e17c94a84781455c96c415b970cffeb2106`  
		Last Modified: Mon, 08 Sep 2025 22:03:22 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:f473360bea40a8efb96a01b4b50e9af896c177ee5ba4bb826f0e673f69b2a3cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f6c60ed54f95b2cbdbce39e2ce1d7e928b0992badafcb46767929c5133dac2`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b9ee04b8a9ae158f121f72948c36e732641afad1f1f9a0ed789384bff7d0cb`  
		Last Modified: Mon, 08 Sep 2025 22:05:12 GMT  
		Size: 9.6 MB (9627773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485a83ba6b46c686ab541c8a03d6ecec6ffe043910b812ee403d6bc880f8eefd`  
		Last Modified: Mon, 08 Sep 2025 22:05:12 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70ebfe6e003c63f8337966d941bb8d96c33c1eafc09551f32133a5478dd47cb`  
		Last Modified: Mon, 08 Sep 2025 22:05:14 GMT  
		Size: 9.4 MB (9362877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b1d52472a5577af2fb30f3d6944b5b750283110d695145d7ba9c995f9fba41`  
		Last Modified: Mon, 08 Sep 2025 22:05:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:54fb283582da8a5388612e9e86b608305d073ebdb1e2e3bc531af4b73cbe9b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2799000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c3cb04def3c579bac4ee8cbb5246c9d3ec6817795c3521a1560623c67f2db1`

```dockerfile
```

-	Layers:
	-	`sha256:198bc7a4ac37485fe88820d0a6bc2db673295a04f632bd28d75454c70a95a5f0`  
		Last Modified: Mon, 08 Sep 2025 22:03:27 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:581a3dfe90fe51f489d54879d2dc8d1bb20e5a969740c06e4dd3b8ef3c8315aa`  
		Last Modified: Mon, 08 Sep 2025 22:03:28 GMT  
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

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:11378bdfcc055393ce2da3fe24de738869891ead462392a92a4da7953bd80928
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
$ docker pull rethinkdb@sha256:8f7423dd1f41a688b80bb0e1887b43762c320f03ae9796e7e7c2b480b931ac95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53b431f52c4c559b5ccd1d32c233f6d61e7298a5af346a11680688a48429333`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d9ce707ef17f4c8fd60d5058c3abacfb2e7f9774483e03c5c0423a4ffb9759`  
		Last Modified: Mon, 08 Sep 2025 22:05:06 GMT  
		Size: 9.8 MB (9797279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34f32bf54faf3386fbe830874347f40a5cda2b2c2e5c539bcd188f9331c7ea8`  
		Last Modified: Mon, 08 Sep 2025 21:42:41 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896ac436f91ce527089294d5b257078b3c3688dc064eaa7c5cfcf2025e0e4593`  
		Last Modified: Mon, 08 Sep 2025 22:05:07 GMT  
		Size: 10.0 MB (9993087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fed90b7a046dc8e7dd5803feeaf73a818682990571ecb7b30410b6adc241a7`  
		Last Modified: Mon, 08 Sep 2025 21:42:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:69f02a2de1a801ed95573f2b3c284421dae13fd0c6fc0e54c10440cd278a5d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034d2d992a02976531f60469827b4d496c7efc0a6cad0afc6333dc2fa3f3b98f`

```dockerfile
```

-	Layers:
	-	`sha256:5d03657237ab4df91bf7114fa3846ab459916737dd580df86bc86398397e0a08`  
		Last Modified: Mon, 08 Sep 2025 22:03:21 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bd3d65adcd873ba27eb553c87828e17c94a84781455c96c415b970cffeb2106`  
		Last Modified: Mon, 08 Sep 2025 22:03:22 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:f473360bea40a8efb96a01b4b50e9af896c177ee5ba4bb826f0e673f69b2a3cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f6c60ed54f95b2cbdbce39e2ce1d7e928b0992badafcb46767929c5133dac2`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b9ee04b8a9ae158f121f72948c36e732641afad1f1f9a0ed789384bff7d0cb`  
		Last Modified: Mon, 08 Sep 2025 22:05:12 GMT  
		Size: 9.6 MB (9627773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485a83ba6b46c686ab541c8a03d6ecec6ffe043910b812ee403d6bc880f8eefd`  
		Last Modified: Mon, 08 Sep 2025 22:05:12 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70ebfe6e003c63f8337966d941bb8d96c33c1eafc09551f32133a5478dd47cb`  
		Last Modified: Mon, 08 Sep 2025 22:05:14 GMT  
		Size: 9.4 MB (9362877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b1d52472a5577af2fb30f3d6944b5b750283110d695145d7ba9c995f9fba41`  
		Last Modified: Mon, 08 Sep 2025 22:05:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:54fb283582da8a5388612e9e86b608305d073ebdb1e2e3bc531af4b73cbe9b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2799000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c3cb04def3c579bac4ee8cbb5246c9d3ec6817795c3521a1560623c67f2db1`

```dockerfile
```

-	Layers:
	-	`sha256:198bc7a4ac37485fe88820d0a6bc2db673295a04f632bd28d75454c70a95a5f0`  
		Last Modified: Mon, 08 Sep 2025 22:03:27 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:581a3dfe90fe51f489d54879d2dc8d1bb20e5a969740c06e4dd3b8ef3c8315aa`  
		Last Modified: Mon, 08 Sep 2025 22:03:28 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; s390x

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

### `rethinkdb:latest` - unknown; unknown

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
