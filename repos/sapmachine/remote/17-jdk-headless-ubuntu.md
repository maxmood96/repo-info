## `sapmachine:17-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:28e7e2054db7c568b448ad917661bfcb52898c5cc41c8d2e4835ed37b206b15f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:4139e69137691446ebde647f12fc72ac79fc14fb85fb2ca249a3b86421abb185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228931405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503b3d7a11b77e79ea04a3a657231010689f1d9d5fcefdd988d0acc3878f5432`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded58e9166a1c7b0d8e237fd5d756c4b8952809a95d0ae3e207ace538298e084`  
		Last Modified: Wed, 02 Jul 2025 08:24:18 GMT  
		Size: 199.2 MB (199213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cb517be4a52021c898455d64842497916f15cc1a0692001a78f27b829449cbfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2363419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41ac249631f4e7a4213e6538ec0af1a136d9d380d1d4c4e8f06f69bf0e794cb`

```dockerfile
```

-	Layers:
	-	`sha256:127553277b2a95fe8e25d45929c6f45519b84a405be0a4cbc56bc79f61e219c6`  
		Last Modified: Wed, 02 Jul 2025 06:05:26 GMT  
		Size: 2.4 MB (2353800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6759eeb8d1ae2c94fcb652d0662661dec8b59543495ed4cc5af937569e9954aa`  
		Last Modified: Wed, 02 Jul 2025 06:05:27 GMT  
		Size: 9.6 KB (9619 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0fbb6d22c8a1c23fd9308415cd955077c99a002a371ac3485c738673e0f02fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226815906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed135eb927f5f089126c8f47724a740f9bda7cb9bf2c5717cc5eae4a37d9cce`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5786d8c85e7d575b455eddee9040c3cd12265acd6fbb0e659600eb26ad6c37a3`  
		Last Modified: Wed, 02 Jul 2025 21:49:15 GMT  
		Size: 198.0 MB (197959888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9db669abe84e4eec6fa6465d4ae151fdcebb4855e702b72713aaa5e8788697a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e145ff842728df92a83bf45fb706121bb7fc742131b6044ff6026002785dd0`

```dockerfile
```

-	Layers:
	-	`sha256:9ffc78e332f50d6dd58660ef11a50940359a200912d8a16db7f3221ca95ec8c1`  
		Last Modified: Wed, 02 Jul 2025 09:04:46 GMT  
		Size: 2.4 MB (2354283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21443381194f10374bdce3aba399a1b91b7a96d7ff5528b0929a42fb921b5a08`  
		Last Modified: Wed, 02 Jul 2025 09:04:46 GMT  
		Size: 9.7 KB (9746 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:fee1d98252812175190553cc205753f6a16279d1280ec9ebb2cb5959f63206ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.5 MB (234524145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1442a622b9d98222b286ecb4d5a56fb32533c9bf584bf0cab137ca6329eff42d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dec67a6c20913f171b7930c70833ba1147a1afbd91f324117ea5f04e2545feb`  
		Last Modified: Tue, 08 Jul 2025 14:14:25 GMT  
		Size: 200.2 MB (200202639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:15de024a8958bae0afc43cf4450a143819cb3d4197fa9b30a4c37a9038377dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0eb2d6520cc7996d7c34ec1e413bc835efd87f1948fbace8a82737550997c5`

```dockerfile
```

-	Layers:
	-	`sha256:f5270670d7d07c424255878fb4bee2a25f24a1d47a20bb5c0f0c6e5649c4bda5`  
		Last Modified: Wed, 02 Jul 2025 06:05:37 GMT  
		Size: 2.4 MB (2355858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ad9b0d8033d155c85108b929f3b383bc428511a110eb0a2e379e86c4c74c04`  
		Last Modified: Wed, 02 Jul 2025 06:05:38 GMT  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.in-toto+json
