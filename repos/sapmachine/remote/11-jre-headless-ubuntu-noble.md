## `sapmachine:11-jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:f716a9a0786c753feba006971335ec00d8af011b193ab21f72301834b66e961f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:2c2cb6811d00de8992ea435a353f98bd403bcf2a1b80ad922ee71537bb993b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78848267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8600db1c5301bde45d86cbe411d1a41104d49ff187e5e08cc11be4180ba66c9f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f1da786d5b84e980a6637b00e97a0eb74c2f482431d7bfd447a011adbde418`  
		Last Modified: Fri, 19 Jul 2024 18:00:10 GMT  
		Size: 49.1 MB (49143114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a4a0c128188f760413f55667c43cc57e463de73db9c458ca23211b209596c043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb3c58a5d62d97dffa1fc9a70b42e58b5d8597b8ada35c49ba9eb026cd0cc6a`

```dockerfile
```

-	Layers:
	-	`sha256:afb5e2aefbad7d8c9caf0f41f8d32b3c973299f682eb7d515d91d5d09234e5d0`  
		Last Modified: Fri, 19 Jul 2024 18:00:09 GMT  
		Size: 2.1 MB (2136172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69159d1463fc9a1eef9a07148eff086856ec5d6ab5d3be9f1471f88a355ba8a4`  
		Last Modified: Fri, 19 Jul 2024 18:00:09 GMT  
		Size: 9.4 KB (9364 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2dee9430abaa1fffd2b7a1ee29586bd6fd70aac9f8a1478d3d917117e5daf2c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77299521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaac7e1856988ed336998fdca728371df339315e5c93e8eb8b7a4c7fc83a8bc`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5035e812084e6db184a8d34a6801a5269076f4e76f90760fdda85bb2b70b3659`  
		Last Modified: Wed, 26 Jun 2024 00:30:10 GMT  
		Size: 48.5 MB (48456478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8ccb1a918e2c0b954b4cfe38c901aad956a7f4eaaac4b23f9ff36c74aae457ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa4a8a303c8d05daff4c4b69cfbfd43867cdaf2d48a7880dbe12a8dfa8503d6`

```dockerfile
```

-	Layers:
	-	`sha256:86ba4d3fed68366f42c1df2aa406cbc0b140bacaa0d73609b1dc1db5b420daaa`  
		Last Modified: Wed, 26 Jun 2024 00:30:09 GMT  
		Size: 2.1 MB (2114107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:968df06242100e7e088184a04059a46fd936a405d28642f82594f866fe367809`  
		Last Modified: Wed, 26 Jun 2024 00:30:08 GMT  
		Size: 9.7 KB (9707 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9b91e9b7aca97af88d2fd241452cf52b341600c34fcf395e4a4ef3162f96e6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.2 MB (82208485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c594bfdadb8e19e8684307784cbf14b17e2529ac02d66f796029fc12494a716`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f387833a9e633b6adbbb4debad1640fc421fa0d6c653b7a6eee9b9fd24bc36`  
		Last Modified: Wed, 26 Jun 2024 01:12:20 GMT  
		Size: 47.7 MB (47702456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:76400750013b0b64f2d2e37a758833b8eea0735ba0318e5f5822c2bb2d4c0bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2126321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad527cc31321541f3f84fdcade4582f6b01826184d69b085d681150270e52f1`

```dockerfile
```

-	Layers:
	-	`sha256:d06a2b593b7501b97e64dd453be6c378c0cd6db7abf20dfeb520686771670949`  
		Last Modified: Wed, 26 Jun 2024 01:12:18 GMT  
		Size: 2.1 MB (2116889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec050b71d5ec965c33bbc1cfa8941f150d9d462fc5dbca01d08af799cc81065b`  
		Last Modified: Wed, 26 Jun 2024 01:12:17 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json
