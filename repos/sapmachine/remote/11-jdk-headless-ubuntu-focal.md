## `sapmachine:11-jdk-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:5010f3e725e29ebecaed15d5b61be372df64a31048f0d0846684a8382e2eefdd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:e3ff140e3cb69023e157e7dd388b0acff22ffca917dbbd76da0729ff6e557dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226580222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969ba19779ff208e36524f2b4bbf9f07526e030b44880a81d4bb00c29d0601ec`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71417c99b8592e421d64809a7117b7dd72fca3319db73ef826a450d3d8b7f532`  
		Last Modified: Wed, 02 Oct 2024 02:00:25 GMT  
		Size: 199.1 MB (199069170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9ee7f0863be332eb1a699c9de2795c651a259f64f67d0ca0415f94c72592a4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2152025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1702a3756e78c6e80c557eaa679e0a9a9becf9f20a112231b1fa08b99bc9286`

```dockerfile
```

-	Layers:
	-	`sha256:bf11dd9072fbb43f682c758dda2d37b15b44d429704c5c7bf936a6022fbe0030`  
		Last Modified: Wed, 02 Oct 2024 02:00:21 GMT  
		Size: 2.1 MB (2143341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:186c5c0ec455472cf50d655c2008f2f222d3ef7908fc78dc800926610cab1478`  
		Last Modified: Wed, 02 Oct 2024 02:00:21 GMT  
		Size: 8.7 KB (8684 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0ceadcad1aefb27cad988e8b1a3c81963693ede1c7287bd83a48bd1d08c5a23b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.6 MB (223556761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93631a817d85ca495190398ca01a357df906d3ad24cddaa953090bbfe1012ed`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a06e37bb6acef6ced099972ad30ffc3797b14b19ed50047ac6370e7e75e2a87`  
		Last Modified: Wed, 02 Oct 2024 04:09:19 GMT  
		Size: 197.6 MB (197583169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c9c6b4f63e7bb908253aac278e8f35e317424eeabc765e18b8bbb0a16e4d581d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2152378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4fa9651df9caeab5eb6f10093509a9e2e63aa298203eac44fa217852f3796c`

```dockerfile
```

-	Layers:
	-	`sha256:aeb065e11e361709ffdbc021fb15504bee123f4916ca2fec9ea1d85b9664e458`  
		Last Modified: Wed, 02 Oct 2024 04:09:10 GMT  
		Size: 2.1 MB (2143596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1d5336d434025060ee1e92bd2b423e9395c3c74f612589c267faacaca4b5186`  
		Last Modified: Wed, 02 Oct 2024 04:09:10 GMT  
		Size: 8.8 KB (8782 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8261e39b23d10c0a3acd372c711bd855eab1ed99746559d58d973cb21954aea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217266988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aff523cf4873058dfb12dc4d39a77cb7830ae88586313d0c2a7066ac4bd6ae9`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cafd57629abc05d597016161b87b83b544a17d39d1016cfb289a60295fc7d492`  
		Last Modified: Wed, 18 Sep 2024 05:32:58 GMT  
		Size: 32.1 MB (32076334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32df1738abb106e16853d3c3c0dbb45fca601bca27103b6f7036a95ae467709`  
		Last Modified: Wed, 02 Oct 2024 03:27:52 GMT  
		Size: 185.2 MB (185190654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3f4776a57cb513bae647d0ac99d07ee3bb3a6a4b4ba32520ab51d4bba1ebe67d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2153189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d017b97edebd79adecf3ec56ea43671f9a561a02c03ea1bd0eff23fce2aed2`

```dockerfile
```

-	Layers:
	-	`sha256:5e2b314feffeaa9624209ddcf3b77a440030cea95fe572aa48b6b57ea55981e8`  
		Last Modified: Wed, 02 Oct 2024 03:27:48 GMT  
		Size: 2.1 MB (2144469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be50e42537818e37b9ea9d8f05e81074b4be684062ba8a940153a243e1e136ba`  
		Last Modified: Wed, 02 Oct 2024 03:27:47 GMT  
		Size: 8.7 KB (8720 bytes)  
		MIME: application/vnd.in-toto+json
