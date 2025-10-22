## `sapmachine:lts-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:d000decdb60158f1bf8e3279ecda344773db7252767a77f124df3d03d0d12173
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:1ee7aa3c9bd9415f6fd69e25c30466f4852ef88f05b006ff04bac0eee21f2bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.3 MB (263347916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488b41b3f08ae763692965c392b8d8d520ba1c2903a8e8f7b65a39a99a216bc6`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e483ff2ca34711c43e347ae8fc5bde5aab7e4c7a93cdcd880ba28e48a326a93`  
		Last Modified: Thu, 09 Oct 2025 22:55:14 GMT  
		Size: 233.6 MB (233624769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1ea553f07f4a5f0a0de474a52ba3888e9d4febc86f5a8f91646f87991fe3214a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2612998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e86056dcc5e7fb10b824cca3c7922dad6dceed33fd554da76fe1b42cd654690`

```dockerfile
```

-	Layers:
	-	`sha256:6a5052deaa839b838ed6d375d779a22aeb683e9df0d2aeb35f55dc455d41c727`  
		Last Modified: Fri, 10 Oct 2025 00:17:31 GMT  
		Size: 2.6 MB (2598219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17ea9d80bccc85e1d39f589e576ecbf1664211f890d3b71364e294513b401b9`  
		Last Modified: Fri, 10 Oct 2025 00:17:33 GMT  
		Size: 14.8 KB (14779 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6e32110324adc5e68d7616b38f79b07acb88fcc55374faa00f7885a52a9984cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.0 MB (247048631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8fd64827a56d3be2970be052a6f45a4a5277ca9867f72d7acf487f2800e4e9e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Oct 2025 21:30:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157ce77536b5daf0347576278dd3fb0a406c2799910b78b4b87e76df67eb7ebb`  
		Last Modified: Wed, 22 Oct 2025 00:10:50 GMT  
		Size: 218.2 MB (218186919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6631255799740d3efb408cb6f100e8c23691ebca4547efccc9bea171a8ec23e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a59209f44adbb26c8edf34d45f864a84e056528b9e701bcb0ca7c408dcbdd0c`

```dockerfile
```

-	Layers:
	-	`sha256:200cac0cfb80354655c07a6b33f7947226f9d8f5622a03c7e609c1c3e7be76cc`  
		Last Modified: Wed, 22 Oct 2025 03:01:20 GMT  
		Size: 2.6 MB (2599714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf80d73e02007d6fbcd3a834d4ba2c3b77bfe1579e2d6767185d2441cc7f8541`  
		Last Modified: Wed, 22 Oct 2025 03:01:21 GMT  
		Size: 17.8 KB (17827 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:17f6a4a39c73244281e6fa5b498b9da79cd24d1ce27b50b46455f84b8608689b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268800024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9c5ed4e56d2c0c80f4a330746db2311673188e8209b726d1e0602183ce5a84`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de7992186a5d9414f41a7b47b18ca6cd0bc4c109f085a0520ff54bfb5ab1d54`  
		Last Modified: Fri, 10 Oct 2025 16:10:03 GMT  
		Size: 234.5 MB (234496499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f1fc94cacbf661291e80f611773a798e175cf8dbc8f2a75ce1e50e277c8ba3ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2608763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36d11a3165a795cc705f0535b211d7235fe0981c208bef69030138a288eb036`

```dockerfile
```

-	Layers:
	-	`sha256:ff1bcba0c66f6c3024f5304374c188d950c324a72d24bdbcfef09c9eedfcf5cd`  
		Last Modified: Fri, 10 Oct 2025 00:18:25 GMT  
		Size: 2.6 MB (2593826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97861f7875708fc97ac8f1decd20011e2c1949504fb7a8feaca6b3c15b494f02`  
		Last Modified: Fri, 10 Oct 2025 00:18:26 GMT  
		Size: 14.9 KB (14937 bytes)  
		MIME: application/vnd.in-toto+json
