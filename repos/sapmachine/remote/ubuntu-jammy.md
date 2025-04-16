## `sapmachine:ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:ef8608297bcb17594e411b25e1ad9f2ae74870e38e24d456976f16a22f0bd291
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:5ed9fbb5b1aac7abf009612edc44fc1dc3c48fa335d5b5ec65d7ba78d98645c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261581356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c2398c42fd9083ccee80ffd2a62c000f0f4b7ccfb26b9996b4f4f6482b615a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 07:24:14 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:24:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:24:17 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 07 Apr 2025 07:24:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0faca470783147d0aad7358f04c6d4077fe64a91b536142e9c578bc9f8533e5`  
		Last Modified: Wed, 16 Apr 2025 16:14:16 GMT  
		Size: 232.0 MB (232048991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fba5233d358d09e5d3a22fec46d9b1a4b84f680ff27c1d135d7754c4c68e218f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2496964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c35f88389104302e1ecfce0a921869006d4559173631785085015c003b6220f`

```dockerfile
```

-	Layers:
	-	`sha256:212e98fee56cf7ba5a6223d5ab7087c06f913f19a88638986ab36265f6f4b40b`  
		Last Modified: Wed, 16 Apr 2025 16:14:12 GMT  
		Size: 2.5 MB (2485551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:975b55666e83ce9dc53f79c19e5d636987dac57ebc36a4df7fa2d59416440af4`  
		Last Modified: Wed, 16 Apr 2025 16:14:11 GMT  
		Size: 11.4 KB (11413 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f2df2b7c723bb227a0d065b61f5d24bd4be93e239ebf8529e377c9dc334c8fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 MB (257268130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea63524b6f235ee6c206e11dfb34c909c09947d3bb956448f1f091f4ba16b2d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 07:27:02 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:27:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:27:04 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Mon, 07 Apr 2025 07:27:05 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae4077107b3b126d79b9a66fbc3b7899e89705f6fd381671db934d611c11e0c`  
		Last Modified: Wed, 16 Apr 2025 16:17:58 GMT  
		Size: 229.9 MB (229913899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6dfe3b554df76156a3a14bf89c586b4734148c47381821ffc302a0f47cccc452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2496939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6fae0adf6c11993b0e64a027106332f8654ed903dedef03a8b8d41f0b60357`

```dockerfile
```

-	Layers:
	-	`sha256:c908c2ea4bf2727bce55f6659750f655a1c356ba9cbdac67ce306c8a35e059fd`  
		Last Modified: Wed, 16 Apr 2025 16:17:48 GMT  
		Size: 2.5 MB (2485326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1e7986da7aaa3c62c35db4e0a7c7bf5a2145e277e9e93716b5aef6fdafd18c2`  
		Last Modified: Wed, 16 Apr 2025 16:17:47 GMT  
		Size: 11.6 KB (11613 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:83ebfa69e370738d06f7857a19b59974c517533b35831998514817cb9eb355a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267694377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec7a691e1d86c1188e7c06a939069c1ed3b0d5fc6e82e802e2c5817a3207469`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 07:25:40 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:25:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:25:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:25:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:25:44 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Mon, 07 Apr 2025 07:25:45 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce45a2bf4f9c789f7568e463bdd20c72b4807e0525e7fa64bcae724aa8bc44e`  
		Last Modified: Wed, 16 Apr 2025 16:23:30 GMT  
		Size: 233.3 MB (233251681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:90f42ac365b277e28c28540dd07c854f68f118309fc8df7e7b82eed1ab63511d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2498521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43b89ebd5ce5811561cfe2fc566d15867a1abeeebf6fd98e5dbda67578568c6`

```dockerfile
```

-	Layers:
	-	`sha256:1026b4840c82dd174ddeb9adee79e012f6845fe9046aad74e3e9c7ddd5ac01aa`  
		Last Modified: Wed, 16 Apr 2025 16:23:22 GMT  
		Size: 2.5 MB (2487016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:665b8819fcd315c4461e1220c4b05b67819c7bd10a7988bee2aa835edfbd91c0`  
		Last Modified: Wed, 16 Apr 2025 16:23:21 GMT  
		Size: 11.5 KB (11505 bytes)  
		MIME: application/vnd.in-toto+json
