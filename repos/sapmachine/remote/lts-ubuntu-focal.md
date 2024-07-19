## `sapmachine:lts-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:8539cc2dae72cbcdb0a8cc231bd2448c20c7aa3c34368462f1e1b861fd082767
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
$ docker pull sapmachine@sha256:ca4c119e480f311719f763284a5d28fa4a7d810909ee7229419a7546b29dac6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242272057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db7b0008a3237ffb644e54edf31e7542dbe2c938861ad4e3b9490812456d6de`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71471dc2de9f4d33e8a4b92b2fe209972d7f44f5776879c3f3cddb751b90c63a`  
		Last Modified: Fri, 19 Jul 2024 18:00:38 GMT  
		Size: 214.8 MB (214760288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1ec4325d840376a705111a1b6ff020f791b99894a7cc69a3fab46935254179ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0df16f25bc86a7a9c053817464a2d1550e3d3ae5258f8ef2f11d1eefa85280`

```dockerfile
```

-	Layers:
	-	`sha256:081c8a7e05a1f6429d86e48f2408e057fbdf783c17f66d02b3cde347bc706a77`  
		Last Modified: Fri, 19 Jul 2024 18:00:35 GMT  
		Size: 2.4 MB (2367821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47fdc51f0ca908d1a0b77a77069751f9d60f8ad3ce2041367343561912d41ee5`  
		Last Modified: Fri, 19 Jul 2024 18:00:35 GMT  
		Size: 11.2 KB (11191 bytes)  
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
