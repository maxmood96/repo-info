## `sapmachine:23-jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:5f17510fb37373c12872b933850c943292e6c7e30e6e3e5c085c5a6f744bf80a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:18c585d5546190900ba5baa2b85ca92a0b124e86da47440f535c7c9c58874c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.3 MB (251333958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0537124a97631a2a2af00a17113582514707f19d96ea401779edbf582e4e09`
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
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981d7f4f94347e0f331ffed63f1e2ad7384b96da1371618fe5aa45e8cc2f61ab`  
		Last Modified: Fri, 20 Sep 2024 16:58:17 GMT  
		Size: 221.8 MB (221798270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:575dee5c149ff3d6d66c8c3a55d223d512f3de55cdb7da11ef4bb26f0e127d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 KB (13450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64fae470bd8fff950477fffd5477b3b797cafdc6fd34d4052d8f33bac434e20`

```dockerfile
```

-	Layers:
	-	`sha256:55d7a27073ce5ed3e30702081a4abf5fee978368c6594129b7c1c7dbc5b1af11`  
		Last Modified: Fri, 20 Sep 2024 16:58:11 GMT  
		Size: 3.6 KB (3643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd5f44a8c1f02c89925b56fcfee4a94f2d042ea30632c0684ed10e8515e6848`  
		Last Modified: Fri, 20 Sep 2024 16:58:11 GMT  
		Size: 9.8 KB (9807 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:bf875005830681e12c5b42bb0c4d659be3e89c214c01eb45b66ab256924da64a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247085871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c515c44e81db750802ca60abcd92911ce2441ac0dc10f7eed2ff1235880e29`
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
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d1acb0c0355f4ad6ba3b04e494e64dc0eb5c1ad9f09039dd8b0ce4c5a99d7a`  
		Last Modified: Fri, 20 Sep 2024 17:06:04 GMT  
		Size: 219.7 MB (219727542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ebfa3b75a7d1704cc08ac88f17f1bd653973bdcd27a4f9f62fcc16018d0880c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2484844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a43659f2d1eeecfa851f38a6e5f50ff50b3b0b3667b562a9adab730371d17b`

```dockerfile
```

-	Layers:
	-	`sha256:9f8704bc0ae1d70b4c65e620f0c031a6c5893f024bc672c76895174514211cbf`  
		Last Modified: Fri, 20 Sep 2024 17:05:59 GMT  
		Size: 2.5 MB (2474688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cd64306c309e92075e55ffe5b1d24ae3a2d0f89ab3be4e63f1e43df965c0bdc`  
		Last Modified: Fri, 20 Sep 2024 17:05:59 GMT  
		Size: 10.2 KB (10156 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a04494e3518b8e477768ca8286213eddf1019f9ad0132323ed71ca1520566238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 MB (257224740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c37e66ae84dbfb6006d3519f9b07ac5d32f48580b72ffce83e4189641e11528`
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
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63762f99ac7592d1e49125b017615112ffc51432407b2504fab3a56b1266e5e7`  
		Last Modified: Fri, 20 Sep 2024 17:07:29 GMT  
		Size: 222.8 MB (222776498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2d43f293a5f67892fd72862ac56ade79cca64b4109a816c0a6c0d4f7fbf2c829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2486895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc8920016649f050598e7650f9c0e5fe96206395f542cb31267a077cebf4957`

```dockerfile
```

-	Layers:
	-	`sha256:9d4f4050984c8892c83bde8d121028f1ee7f8a25213e9be95ad21349b1cf9478`  
		Last Modified: Fri, 20 Sep 2024 17:07:22 GMT  
		Size: 2.5 MB (2477026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a060712cf7d96ebc3867f762753458ef68161c44d2a36a8a66e7f26c18a01ba`  
		Last Modified: Fri, 20 Sep 2024 17:07:22 GMT  
		Size: 9.9 KB (9869 bytes)  
		MIME: application/vnd.in-toto+json
