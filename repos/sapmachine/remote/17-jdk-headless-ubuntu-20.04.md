## `sapmachine:17-jdk-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:4a6406079c773d24b70325e6dd0fe81d1e8b5f92442d5a864ab271adb06278a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:0f5abe7f04c2b8fba9e34690cd854b90dec8da006fe5d38bf48fa6026e13bc07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 MB (225900018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21235c435527a021aa582f6673fbefe9e2c090fb2dced533d4ce747fd4bf0193`
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
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ea158b6dbb39c255910d7c410ecd8fdf8ca6c1534ca50bd6adfad0c69cab89`  
		Last Modified: Fri, 19 Jul 2024 18:00:33 GMT  
		Size: 198.4 MB (198388249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d0ef345fa5e3729666a1a739bb3eb2358587c42a2a261cd317d1e937c46784a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe02e32269258822db058b6d7a6bb57aa51cab3854bfe2c72dc307d5a9a1aafd`

```dockerfile
```

-	Layers:
	-	`sha256:7f5f630477c07a8fac626565e6259ceba60aa8e63fb25ea38b6f82f26253772e`  
		Last Modified: Fri, 19 Jul 2024 18:00:30 GMT  
		Size: 2.1 MB (2125393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37c5f9310fb8de30a288678dd4b3b9029a4298dad72bdcf51a5c9aae803d3403`  
		Last Modified: Fri, 19 Jul 2024 18:00:29 GMT  
		Size: 8.7 KB (8679 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ed15064c06313e0913074f64481ddb7acf6aae1220adbd4dd3d75992b119ab5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222996044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7deeb9c43660020300d6bb98a6497cd4b3a9c0c1cd37fe2da7c549295659403f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49d505876de3fddd8f594a81adbbe63dce4c35917b20f014e6c324d530e9bb2`  
		Last Modified: Sat, 20 Jul 2024 00:31:13 GMT  
		Size: 197.0 MB (197021827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:052b2f3c6d81e67a639fd66824a6a6c2f573c1d728b14a0e7d6aa457fadada26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270284bf74071a4347c411898191c40cb3a1db372aaa7e25f441ac0ccef871c8`

```dockerfile
```

-	Layers:
	-	`sha256:2ed52257b51e7cfa93f26a039c70c574b05cb296e5a5121278e1f7bb5e307634`  
		Last Modified: Sat, 20 Jul 2024 00:31:08 GMT  
		Size: 2.1 MB (2125020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f713fade297300df490de4b616305194fa3d8014af7612cd5bc8f8ce70a6661f`  
		Last Modified: Sat, 20 Jul 2024 00:31:08 GMT  
		Size: 9.0 KB (8980 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c4ca7f8f6591a6f1c90c55876cc0b4a02af8f0060c59d6b2186a7ccb3cc6bcbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231006749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e61f93ab0f99f2ac64812b4622ff6f570a0bc31557600936239d934b36b06c8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:42 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:45 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 03 Jun 2024 17:10:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0ac07deb90b2592adbec488c8fc311f7837415bff92df232e613cc0eda728a`  
		Last Modified: Fri, 19 Jul 2024 23:46:06 GMT  
		Size: 198.9 MB (198929609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:112919bcd0cff5a4b64a72cd564a50b11b12f0ef24954785890fba32b5ff557d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9ff6726597f9bf664b68b6e1a7802faf76089e1728cc9ae301ba2d1bbb82c0`

```dockerfile
```

-	Layers:
	-	`sha256:f92fc089456a4cb38ba5328addd0826d1b5708f4809efddfafaab4652efdb7f2`  
		Last Modified: Fri, 19 Jul 2024 23:46:00 GMT  
		Size: 2.1 MB (2127146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7a7e7b1d9855f1fc108586a58f7fa2b87942e7c2b121cf5189d1949cac080c6`  
		Last Modified: Fri, 19 Jul 2024 23:46:00 GMT  
		Size: 8.7 KB (8717 bytes)  
		MIME: application/vnd.in-toto+json
