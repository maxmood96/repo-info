## `sapmachine:17-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:9430787a844ed1c05662bd8887193e1748fb2b3cf1d2dabba8bb60a85f87a72a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:c0afecf2999277d3ce95f1411ba53ed651f8b21b5c67b85103746cfcae57aa33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227109477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7eacd1d38dc626a7a225c703050cf16658f826792e3f1bc273d7cac7ec0b68`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:c2cbb7ad72f217d7ac6c8e402bcd9f180d4b8fc6c04054728915a225db2d51ed`  
		Last Modified: Fri, 19 Jul 2024 18:00:32 GMT  
		Size: 199.6 MB (199597708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1a05cb3d2d44f9aadc71ebd8d6ec7c3c648727f03474deed943d7f3569a3ed12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c551624312ee08a8390b36a9a229070afb6de3eb28eca03bbe873b51e4f88476`

```dockerfile
```

-	Layers:
	-	`sha256:bb1e9b93791c4e68c999a0f34b83a59b57bfa9f6accf3e38eece0cf5289b7b07`  
		Last Modified: Fri, 19 Jul 2024 18:00:29 GMT  
		Size: 2.4 MB (2363996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61d3879b9ab10c32236481f0b58d8da9e357d47eddff1f261ca58573793f390f`  
		Last Modified: Fri, 19 Jul 2024 18:00:29 GMT  
		Size: 9.9 KB (9884 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d608ef20739413f7253b851ce5e8b3dcfa2aeb82aa462ac8df73d69da91aead2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224193241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d06752be2620e0d0bc524a4a8183a47a9c3161aabfb9d05c803f0d5fcae2c02`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:f9d99ae8d1424db8d63fb1704404ff963db294628da4a0a909536bb6eeb12f9f`  
		Last Modified: Sat, 17 Aug 2024 04:38:04 GMT  
		Size: 198.2 MB (198219024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6fce7e32fbb9b11cfae6caa5cd6adf313da55668c8f005747729c210174544e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1621060070e0a985f785cf72af29cbe7c0148b470434a62425c2ddde5c7bb6c0`

```dockerfile
```

-	Layers:
	-	`sha256:91eaa74a2e69bf2a87f8eba638da285470f83a55cf36e1e35edc3eda2279d3ab`  
		Last Modified: Sat, 17 Aug 2024 04:38:00 GMT  
		Size: 2.4 MB (2363680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5383c4f7defca561c2a9ed3d6634b55bf409d4baaf3f4621ce91dee4be2a53c9`  
		Last Modified: Sat, 17 Aug 2024 04:37:59 GMT  
		Size: 10.2 KB (10233 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9a899accc8027b6d3c8814c7fc8215d32935fe1f6be14d5812908e63e0b442eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232363878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2acec45d0083ee84adc8b089f565d6ee9a177ca395a5b4c5860e079fe915fa2c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:2cca5efaa1061e5f3cd1c24be042a0cef8e9ec2bc2e34b32c9cb77f083756eae`  
		Last Modified: Sat, 17 Aug 2024 03:21:19 GMT  
		Size: 200.3 MB (200286738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6431f124a5cc5eff24eb331f7f582235c1c13c7d2108ce29be8ff682b2ae6d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2375782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85c9b2c595040c82158132a765328a9e901d10e7664aca0990ef38428691eee`

```dockerfile
```

-	Layers:
	-	`sha256:85d00d81622de7c3b60775199e360ad45e3ec47e688db44027d7aa080168e44b`  
		Last Modified: Sat, 17 Aug 2024 03:21:14 GMT  
		Size: 2.4 MB (2365836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc74f6bfa099d849bee223257a0f1af837fd9816e771dc0b40dcc9838879e3dc`  
		Last Modified: Sat, 17 Aug 2024 03:21:13 GMT  
		Size: 9.9 KB (9946 bytes)  
		MIME: application/vnd.in-toto+json
