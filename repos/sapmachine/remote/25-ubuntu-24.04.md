## `sapmachine:25-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:e2d2c7219f05f6da06df823ced73f6fef3e7ad14aaf068261814c3a1dc448a86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:cb8c923dfb8250381b671237ee58503d107981e068edffa269edca90d4b14f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250152963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb70ec9e0b09dfe887db24d43f487002ce0a04c1275b2d552c75f5ad19f2bc6`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Oct 2025 21:30:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcfc77348e4d1c8aadf49e5cb7aaf67a47e20832ddd2e2acc289a6d2daf0e50`  
		Last Modified: Wed, 22 Oct 2025 05:49:12 GMT  
		Size: 220.4 MB (220429816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0140775ff77a0beb365ba9a46ede56b3b4bc049e1ecbd403176cb9ea97135238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2616323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdde480bb7c6992ea89d991954c6412df4c0b60d33e53cab1fadd0662c2b10c5`

```dockerfile
```

-	Layers:
	-	`sha256:68413c238055aa738e59cb7e11a2b78fae57ab7f0003fe2d092b2c1f9f9644e1`  
		Last Modified: Wed, 22 Oct 2025 06:12:51 GMT  
		Size: 2.6 MB (2598925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7a3045f3d71fc69cb34fa04a9b405d2d1bef2b860d65e8f7f2a66725431f414`  
		Last Modified: Wed, 22 Oct 2025 06:12:52 GMT  
		Size: 17.4 KB (17398 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-ubuntu-24.04` - linux; arm64 variant v8

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

### `sapmachine:25-ubuntu-24.04` - unknown; unknown

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

### `sapmachine:25-ubuntu-24.04` - linux; ppc64le

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

### `sapmachine:25-ubuntu-24.04` - unknown; unknown

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
