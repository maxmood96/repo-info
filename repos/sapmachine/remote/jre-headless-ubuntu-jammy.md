## `sapmachine:jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:a7db04bb4d01c8e1e411577e72418374cfa6c4cc7e0f4ada7da192a793c01110
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:796c5d28f3b70854da3d5f35ab3db28565dc9ef94d490087ab1e8677a593f332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (88014492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5539e4d651660f31ba1575fd9d4e2420033e751e0bc0ef9586a3362a5163b269`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdd4891fc1ef81e8f3af0e74a781723fc364eb31f8b5022473ed144782eade0`  
		Last Modified: Wed, 16 Oct 2024 18:58:29 GMT  
		Size: 58.5 MB (58478804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:18b17631bd1e3be2a95b61322329272bf5b963ca43c1cb518519c685972b8809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2164190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af56d5f6386ec9dbf59c33c4cfe9c9773a6f269380ae8799ed4592b44f54e51c`

```dockerfile
```

-	Layers:
	-	`sha256:5480700279af9d8be8e5cff77f63c19f908483d5ace14f7ec7a08326b0724397`  
		Size: 2.2 MB (2154795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51839d693c0bf488e2712649bc43d6d5ec129fc8701baf17f4e70b3283871fbd`  
		Last Modified: Wed, 16 Oct 2024 18:58:28 GMT  
		Size: 9.4 KB (9395 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:1fc497571770b1f1b3ab5aaf2e83bbc083ad343ee3aa72b1a318055466096109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84834873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfb15e9a10e411af8387a605368793dfdedcd2b089a905e0b098680847ffaf2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62fd618e389aeb96455c4750786bf3132c5336830dbd6417545b3fd44677503`  
		Last Modified: Wed, 16 Oct 2024 19:07:22 GMT  
		Size: 57.5 MB (57476544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e624f63b33d8b7f82491a3c1741b9dfcb7382fc0012c8dad8f8331cfc60b3324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2163375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b167d40e18b21d013cc0008c5d7c9748b06f370a9f42cb4057a8a397775ce8c4`

```dockerfile
```

-	Layers:
	-	`sha256:28ed844471fde8039fe32afd6d1d6b40605d08dcd5b766aebccf11041c8262c3`  
		Last Modified: Wed, 16 Oct 2024 19:07:20 GMT  
		Size: 2.2 MB (2153858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22d13db859d4fce8f0847292025ee15805bfc2645de66ba4d0bb5b60d2fc722d`  
		Last Modified: Wed, 16 Oct 2024 19:07:20 GMT  
		Size: 9.5 KB (9517 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ab1ac7aad27d53995a6ea04ac4583c241b9722b0041a6103d2d43a21e885e387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94185542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd65869b1a248c67ed3d420740492d8d65b3a6a6505eab838c9bc41ddaefda35`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b95b076ae15a34aee14d8e03fb428d4d424e8372406c7c9b621cfce98f53468`  
		Last Modified: Wed, 16 Oct 2024 19:13:40 GMT  
		Size: 59.7 MB (59737300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:697e11750004696e85b6a4ed60e9052807a43244e5493bff219d651f9fef384d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2167530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84ddefcadfc83262f974cf7fc1380003decb2cf18653584846be40b33919b24`

```dockerfile
```

-	Layers:
	-	`sha256:bab824e4db249acb0fa588ca9a4cc196cf116c279fee72ee952a9dc16f58a806`  
		Last Modified: Wed, 16 Oct 2024 19:13:38 GMT  
		Size: 2.2 MB (2158085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c2dbdb2b2d8e7488ff5c77ddcd4102a8868cec79f19ea1aa054ab958984219`  
		Last Modified: Wed, 16 Oct 2024 19:13:38 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.in-toto+json
