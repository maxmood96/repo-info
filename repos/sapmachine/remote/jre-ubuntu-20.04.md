## `sapmachine:jre-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:7cbea65cc50f2c3fe6ae1e14b4a0f5c2432716603834738e278dc32bfff95d39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:dacc416eefc876578ef7e4651dcb6a13b7df4e5043d072db2fdd59e5ef254c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94738350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f4cc602a3e05870d289f48f738b574b785c8819e305427799aadf54ea23d98`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bd470365b38407af81bfef87d408c32a1fc6b90c1cf6ac876ca771c656bcbf`  
		Last Modified: Mon, 19 May 2025 15:05:25 GMT  
		Size: 67.2 MB (67227956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b5c67a27ca824aa74dfb7a345b6452eaf4b6ba861d34d41e1b8d956a858cb39d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2317719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd2e74b764904071c03d8464d34c573e355856a2e6dc023afedc28ab204d823`

```dockerfile
```

-	Layers:
	-	`sha256:b3e9ad4131a682a085a757954f748cf0072de5099da9105aa5546aa6312e1417`  
		Last Modified: Wed, 16 Apr 2025 16:13:48 GMT  
		Size: 2.3 MB (2308257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d4f7da815f445bedd06d4fd58d4e1c3936d9f387932827fd80d7d2b9f1207eb`  
		Last Modified: Wed, 16 Apr 2025 16:13:48 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f24b6d03597572345c24ac5ba5f763e69691d889af20b77adf9fc06a7c35a421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92229895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3900a90a3394dd532381811a28a418dcc7d48bd3f184002c9a23553a63b348`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efc9534451498e33bfd1829b0cb280c324f27428e027f9ca38ec5caf0dc32b5`  
		Last Modified: Wed, 16 Apr 2025 16:24:14 GMT  
		Size: 66.3 MB (66252234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4fd9dd54ae6759028c1132f40c1a74c77c21ce62379f2faa5a2bdba9a7f20ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2317508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5608d4ad1a0bece09f7ff41ddaab43d6d5f77314202d0c874baad8fc4062b77d`

```dockerfile
```

-	Layers:
	-	`sha256:c5cf214d89dd7c836919b6fc731cffc8a139137b4baccb1eaf1c2715a418c348`  
		Last Modified: Wed, 16 Apr 2025 16:24:12 GMT  
		Size: 2.3 MB (2307916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:075cc40e68c3fb8f443c4a441cc4e33ca64ca4c0f9b398d23b5fad19eb9ee89c`  
		Last Modified: Wed, 16 Apr 2025 16:24:12 GMT  
		Size: 9.6 KB (9592 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:daa9623e9846e500776558d5574071b602e34495e1e58e477e59e171245692f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.2 MB (100199186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34ee90b149683fc128a7ea410aa9259df9aa29b4e9c0728b81fd7520dc9630b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:47:01 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:47:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:47:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:47:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:47:04 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Tue, 08 Apr 2025 10:47:05 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Thu, 08 May 2025 21:39:31 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2abc7de07dfa0ab8c9a67a0ac92f70894b63530abfb0d4db857f4fcc7269ba`  
		Last Modified: Wed, 16 Apr 2025 16:36:58 GMT  
		Size: 68.1 MB (68122240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ff7b25bd7e6e1bfc1bbd02b60d82fb8de0d9d39d5d9e0b478a3233ba8adbb96b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2320926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f65d0595dd3d576946aee6b2bc646045a58337634e26915130c9d4f88169bc4`

```dockerfile
```

-	Layers:
	-	`sha256:ce45e75a8d37d649d08443734639eae9aa70c1223cd05247ab423db9a1592782`  
		Last Modified: Wed, 16 Apr 2025 16:36:56 GMT  
		Size: 2.3 MB (2311406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfc90494226049f7d1539d50e4e736faa9daf47728f5d5ffd4f602cddcef8320`  
		Last Modified: Wed, 16 Apr 2025 16:36:55 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.in-toto+json
