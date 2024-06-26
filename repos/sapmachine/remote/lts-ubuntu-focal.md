## `sapmachine:lts-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:7ebd6abf6a426a997ad909196f3e118d573465e2ea57e7e28dff3bb675bf51be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:a287672db42b2744c6c856a10e6100a9a5c800b3f11893ac671f17687bc73563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242131097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852b8e88908e404c51183e98449c67ca9ae5d6a373a40ce73ddd4172bfd1911f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307f5a6c8e4c2a38e0ed761723dc964702fb311dff58682bd2f4f6a22870a465`  
		Last Modified: Tue, 25 Jun 2024 22:59:06 GMT  
		Size: 214.6 MB (214619328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fefbead28752d88b21b0ccc00c8c09bcf372e37628711e88186fe310fa0ccb62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2351807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548ca768676db742929b085ab9fa655ebb5d4d0e5e4ca7b0dcb7e6a6dcdfd6f7`

```dockerfile
```

-	Layers:
	-	`sha256:a877b0d926a36f032d3ae3ad31a646f1d0b9882b6cc50f984031b6127ef41f10`  
		Last Modified: Tue, 25 Jun 2024 22:59:02 GMT  
		Size: 2.3 MB (2340599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73cfae9c6d08f72d3cdbad6597b50596145e435256014cc500a4c3c74d1c5626`  
		Last Modified: Tue, 25 Jun 2024 22:59:02 GMT  
		Size: 11.2 KB (11208 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:754abe192d35946f579dc325634e654fd506e2b37477792e8f399ced90a642db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.7 MB (238674091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ddf38c319b2dd4990f01700cb5228624fd2d44977519a2c7e07cf3a82c3a40`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a646ba83300e86a6fd673dd402e4acab15e85c782cea5deddd044af566b5a5`  
		Last Modified: Wed, 26 Jun 2024 00:10:58 GMT  
		Size: 212.7 MB (212699874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:de24ca7caf026bbb6d39d50347d45a1810f40982b5cdfddb1802dd1cb7deb25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2351937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73de6366525e9b8c4c09b8a3b409d90680fc2a616a68d9fd11bc7095fe858226`

```dockerfile
```

-	Layers:
	-	`sha256:d390bc38e11d3c8dfa349bf28e4001a4535f68f8c956b5146012354e74484399`  
		Last Modified: Wed, 26 Jun 2024 00:10:53 GMT  
		Size: 2.3 MB (2340331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ede59a6137022e38f3abf76646c3694720355297b5a70e953aab4e898757a518`  
		Last Modified: Wed, 26 Jun 2024 00:10:53 GMT  
		Size: 11.6 KB (11606 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:bf5a8691d051a0ca7ac627a580fa6bb764b8386c37d5e0188942e91dbfd57f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247625173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b433ee90574e8cf5c94491b1d18fccc5c35d55338154282f98dfbac29e239cca`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4a4fcdb5b519aadef3b5a8b04a11ef1cb9d8cf73e1394da7c755d03c654846`  
		Last Modified: Wed, 26 Jun 2024 00:40:24 GMT  
		Size: 215.5 MB (215548033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:01252489478bd756c062da7e08ceee17ae349c47ce45ea6a8fba31dd5ac0a0b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2353758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6d2a11441cce9cf66e6c41dfbe3129515ecfadf503a48f8e83c5229654491e`

```dockerfile
```

-	Layers:
	-	`sha256:42a5b4dae235143a3bc6ba8026a6cbf15645eaeb965480060413e5267df867fb`  
		Last Modified: Wed, 26 Jun 2024 00:40:18 GMT  
		Size: 2.3 MB (2342463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa8d60568d2c35ce9eccf3836098e225d999e49a5bac255f6adaf4032445f429`  
		Last Modified: Wed, 26 Jun 2024 00:40:18 GMT  
		Size: 11.3 KB (11295 bytes)  
		MIME: application/vnd.in-toto+json
