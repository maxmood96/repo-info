## `sapmachine:11-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:7b0ef4742a514eabe9b7ea4ec34c5372198eb16d0a20a24b3ca36e619efbb019
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:b7fb064a76f88862bc3ca377bddbc06f7bfaffff6ef29c5bc3500b1298e13a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78843910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134cd99b17721ec7905512b29533c374aa5b6d6453d3e4c3d2d96b00ce122108`
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
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
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
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e98e1b078bba34e16981c27caa7a108e77c1f2ea2a68fa619817c65978d96f`  
		Last Modified: Tue, 25 Jun 2024 22:58:58 GMT  
		Size: 49.1 MB (49138757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:97eca843e917298adf8b7e96da0a7401fe09c294270ce4f7f3e870387365e937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2122378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed4fc1e7240ad62771046b4fdd2e6334edba4b029874eaf14cc7f7a4ee9456f`

```dockerfile
```

-	Layers:
	-	`sha256:e4a069d8a055a69effe3a4ee516e084fa23a8b870c5398778bf3f6d958f483f6`  
		Last Modified: Tue, 25 Jun 2024 22:58:57 GMT  
		Size: 2.1 MB (2112997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:924e2a62c65d32ae24a0d5b53f57fcd083c76c28d0caebe5fdc40a9f3c44fcc3`  
		Last Modified: Tue, 25 Jun 2024 22:58:56 GMT  
		Size: 9.4 KB (9381 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-24.04` - linux; arm64 variant v8

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

### `sapmachine:11-jre-headless-ubuntu-24.04` - unknown; unknown

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

### `sapmachine:11-jre-headless-ubuntu-24.04` - linux; ppc64le

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

### `sapmachine:11-jre-headless-ubuntu-24.04` - unknown; unknown

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
