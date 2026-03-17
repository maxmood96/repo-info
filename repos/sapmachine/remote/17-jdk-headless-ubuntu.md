## `sapmachine:17-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:94fafdaed6e41cf17c636129b3d6a7cece6b1982d7e1b56b50acd48508825341
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:48509bda94145d54ecedff964867e0659df370aa96c7eac7a5c7eb140d2e0eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230243936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8b062e911f816c0c649180cbe16f973a9a88bfba48447c90af7050690d0d98`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:25:14 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Mar 2026 02:25:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f368b4dfd5d61cbcfe0cb0674ea08ffd228dcfd95dc8b5da06603bb56fcb1d9`  
		Last Modified: Tue, 17 Mar 2026 02:25:35 GMT  
		Size: 200.5 MB (200511943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e7cdf601eadeed9f043182d462eceb79921ae7d20ed4c4bebe8954d89704a2b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2367120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2ad2bb54c955a9e685b2178fa57688fdc1d17d357af0b8ac471ae1a1dca65e`

```dockerfile
```

-	Layers:
	-	`sha256:2db55f808d93313bf1fe03b9883b313e6bbb1c563495bdeea31244fef5054b9f`  
		Last Modified: Tue, 17 Mar 2026 02:25:31 GMT  
		Size: 2.4 MB (2356888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:541ad6a31da5aef1de5327aa2bae9693a159128f2da93a9d0ffa26a73017b643`  
		Last Modified: Tue, 17 Mar 2026 02:25:31 GMT  
		Size: 10.2 KB (10232 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6e2ed3be6dd30d3c798827273c6ace076da3c919f261ece768768b8fd2fdc1e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 MB (228097222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10538f855157c7afbb2288017fd7426306d243758a83c59836a61f3b28b08be6`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:31:19 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:31:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Mar 2026 02:31:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f6e1012cff8c66521b1e5eb44fde4ad11d98d2f620f38fbeeb3e2b03e18c5a`  
		Last Modified: Tue, 17 Mar 2026 02:31:44 GMT  
		Size: 199.2 MB (199227513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2103472ca252befde582c81cddf2de808191c1eeb400cd2c1325ab27f77b2224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2367781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712df0eb43bdcc8c1c3b78d7230166897e1eb2cc201dd1a65df40f368e479378`

```dockerfile
```

-	Layers:
	-	`sha256:57cda0fb21309dcb70f05906865af5eb0efc8b6e8ff116896dd4b96dea7f2a54`  
		Last Modified: Tue, 17 Mar 2026 02:31:37 GMT  
		Size: 2.4 MB (2357395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601e88f066f55b9b045cb0355649ffa3c7f631e775abbed465baf778b0bbc161`  
		Last Modified: Tue, 17 Mar 2026 02:31:37 GMT  
		Size: 10.4 KB (10386 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:784ae2e3f55b6c4fe25d45c068ccd94c2eb000169c42d317019e2ec2ee3ce7bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235487458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2c2ca2f3981e8d5b7e57a775fa458ccdbd60dda2fc0c1145c494a48d9b4920`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 09:49:42 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 09:49:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Mar 2026 09:49:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094b5a1676220a8e4a5c3ef06b2175d6715dfc566d12aec5d9cf6e3d25140855`  
		Last Modified: Tue, 17 Mar 2026 09:50:34 GMT  
		Size: 201.2 MB (201177407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:714de3d50acb58be9092d0c027ce25b50444b1a71acf904f5f94fab46c7b957d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5045664aa22e05325a7ccf08804eac0cc07bc028ad09865b83c4acdf2e121d2b`

```dockerfile
```

-	Layers:
	-	`sha256:a8d2eb7969546f8def0eba8975806b36a80013d6ab1d1bef8696ff7888a0d2ed`  
		Last Modified: Tue, 17 Mar 2026 09:50:30 GMT  
		Size: 2.4 MB (2354359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c5d72e0c010f92911bdc81ff92e82a31a67c7c800b137d6cc89cdc99a01aa1`  
		Last Modified: Tue, 17 Mar 2026 09:50:29 GMT  
		Size: 10.3 KB (10302 bytes)  
		MIME: application/vnd.in-toto+json
