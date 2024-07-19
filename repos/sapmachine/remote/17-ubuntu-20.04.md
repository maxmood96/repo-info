## `sapmachine:17-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:cd46b27939f059f5db6c1acd47daac122e41d9d99f8bb7972137c33201777aa6
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
$ docker pull sapmachine@sha256:c3d2fe64dec19ed2136b1a93685b90c9658a1b367afcc15ae8707bb87f7ab11d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224052388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dbe5682782451e5ef522a45e342e0f6b714458a869b4dd70a8d477c2b60e7ce`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9fbe30a544a1ac9879407ea8ff67588894ac006c70e8b021dacb2d4e993455d`  
		Last Modified: Wed, 26 Jun 2024 00:22:56 GMT  
		Size: 198.1 MB (198078171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d9fbd854d672245c42296c5ef8e7e1463170be6883f503b02810d373f54a9340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2346077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2fb01be96be9d3120b93cb2e5fe54bfef9db51e00893ad44234bf3f6021565`

```dockerfile
```

-	Layers:
	-	`sha256:37e2f71e03e65b694a00e91bec08f3c1893528f2812e4276e7f1849d8f2eb716`  
		Last Modified: Wed, 26 Jun 2024 00:22:51 GMT  
		Size: 2.3 MB (2335826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:707eabf328459392890c82d57bddbb56028a19ca3ce41dad5192350ed3729a1a`  
		Last Modified: Wed, 26 Jun 2024 00:22:51 GMT  
		Size: 10.3 KB (10251 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1ea02ae5beb061a83db15a3994fbc8424af62d6126648e74b40e27b0243f9ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232210396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196159f34fd8c85f9ddfb9bb2a71a1d2b216b10489dc67a5e977be8eaec0ddc4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0cfda876f818c95d36d5639c3f8c7788b0f4541fab014a75b35081a7b74f85`  
		Last Modified: Wed, 26 Jun 2024 01:00:34 GMT  
		Size: 200.1 MB (200133256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1b72b978017c5e2fd3d8c7173cf089c501f90b81889583f9384b48cd1c0ec76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2347946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969179664ed2ec8ca6a304061b074f59c1c6265dbf25cbb9caf4812cc7ca85bb`

```dockerfile
```

-	Layers:
	-	`sha256:fdea71af21aec4db6708242bf1b3d19645ff55a1aa38fa5a0fd7112fbb205281`  
		Last Modified: Wed, 26 Jun 2024 01:00:29 GMT  
		Size: 2.3 MB (2337982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21626fc3c1bcb70259df7c77311e1f6513883da580279260bd5a6f195b298133`  
		Last Modified: Wed, 26 Jun 2024 01:00:28 GMT  
		Size: 10.0 KB (9964 bytes)  
		MIME: application/vnd.in-toto+json
