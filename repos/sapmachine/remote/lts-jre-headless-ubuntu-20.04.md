## `sapmachine:lts-jre-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:244cf1bb782e99c0af729430f41f26a3b0d3d7b32653225e7e45ef5a11869c89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:a7874eb140cfbd66bf965cd831c29c8ac59af1720928342c8f5020f6d4ea8a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85578034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a365bea17dec21acfd2cb86f84f13b5dd722872752b8886fe111178c9edd6b5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f04e63beb3f1fc4f1b2e46e244f648781c15601256c405258fccada493d638b`  
		Last Modified: Wed, 09 Apr 2025 01:21:45 GMT  
		Size: 58.1 MB (58067640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:33e3b1870b26d9593c5b45a85204da6acfffd1028780d289a68bf151bc1702f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2073007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90477655042fcc50afb82cc1b7271e480b8df0739dba3795ff0dd07dfde5bf1e`

```dockerfile
```

-	Layers:
	-	`sha256:b69077f013b5e679a160b38ab71d45e425dd56c7946ff7010406237ffabfcbd4`  
		Last Modified: Wed, 09 Apr 2025 01:21:42 GMT  
		Size: 2.1 MB (2063380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2e93025582c6517414647647aaa5a284c2aefba8323b544513e568865688a2d`  
		Last Modified: Wed, 09 Apr 2025 01:21:42 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:769fcb5c47fbdb5638571f704a14f7bf8b20828f6db53acb47aa117dffcdd7dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83216313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54777f009211ee4b5344120f5c3fb065aaf0598727b251085215b2b7017015ca`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0749cef575245998836588b670bb38d1fcfa470de9bc3bef08cfd56bcb0c6a`  
		Last Modified: Tue, 28 Jan 2025 02:47:23 GMT  
		Size: 57.2 MB (57242485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a8f8b8875dce705da281f22de23429f4ab9ecc51268507d0e5cf4b0c9fd74394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2072719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc14210a53b6e1e1ed16750a9883786d897f6b33bf5ebb05ca9d4ecdc20970c2`

```dockerfile
```

-	Layers:
	-	`sha256:5b46582602a494be03cadab7eaccc2ded5d15b25dfd56047a42cdea2e395d2b3`  
		Last Modified: Tue, 28 Jan 2025 02:47:21 GMT  
		Size: 2.1 MB (2062967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67db2d4ac8ef5d5c93fcab96e69fd80e8c45a29f7449c6d9643a7e4b79e7ebcc`  
		Last Modified: Tue, 28 Jan 2025 02:47:20 GMT  
		Size: 9.8 KB (9752 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e109b3f54b2bceb2ed75e5b0fb7e0cf13ce15cbc97b32a58c1b3ebb347140914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91179973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e48e95f675cfd9cf8710a6941887ee685582c932b26c2c3f735445e58385bc7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Tue, 08 Apr 2025 11:48:44 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53cab0736efd55ac8511e9b7a71970713d3642d157c257244d6f9131627bbaca`  
		Last Modified: Wed, 09 Apr 2025 07:08:33 GMT  
		Size: 59.1 MB (59103027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:92af7bd9f8b4d2dd169a906d47841e12abcc0eb3e90b6934fdf6c56d30433562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2076779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7add6dca1832289ad81433159311e25691b956d5a09638a1f6dfb86f02cd27`

```dockerfile
```

-	Layers:
	-	`sha256:1021ea7a0a340a71434fed8b9347e07193599d5b6ea81c5d500fc116c36116d0`  
		Last Modified: Wed, 09 Apr 2025 07:08:31 GMT  
		Size: 2.1 MB (2067096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cebeb7480f646eb3e60a39d4706eb2447716ab843b44f9aafc35ad4bc7f6bf7d`  
		Last Modified: Wed, 09 Apr 2025 07:08:31 GMT  
		Size: 9.7 KB (9683 bytes)  
		MIME: application/vnd.in-toto+json
