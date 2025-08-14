## `sapmachine:21-jre`

```console
$ docker pull sapmachine@sha256:827419b8c65f99e7d6b66c7dacef2bd015d03c7b82d1aba34f1c3854a3ed7972
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre` - linux; amd64

```console
$ docker pull sapmachine@sha256:b12370c64f152955a55177e8d56a9c070d17cf2d15352cfc7e647ebd0eb3145d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89926951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16cee9fbd64bf1c924ca415c75a9bfe5f673d86fa36320afb1f48b66ad049c56`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195aca41963a83e91954aaa9fe35167b634e5c77dc6c8bd6952fd12c9cd49f7f`  
		Last Modified: Tue, 12 Aug 2025 18:10:55 GMT  
		Size: 60.2 MB (60203736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:95e579d876ff870ec6043a4d64d0aec25f7381b4f173ac409e1c45b4fe062180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2530688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb1e93a19708774cfb6f3d267d7d78e6d900c2887fd7d439b5cee8251168a49`

```dockerfile
```

-	Layers:
	-	`sha256:39dea9af373899eac8ea6eee1583bb548cf5cfe1c350f4b8dc79d681cffb1813`  
		Last Modified: Tue, 12 Aug 2025 21:07:06 GMT  
		Size: 2.5 MB (2519618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7fc7f35470e91685768e1fc2310ce3cfc59c6c2e0d179db91370e8bd6029d58`  
		Last Modified: Tue, 12 Aug 2025 21:07:07 GMT  
		Size: 11.1 KB (11070 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:61bbe5ccf305fa8b9cbc0970b3a0abba4b4b6f6ec82322fcb1b320cdc3f94ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88245631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959ac55bce41f00800306c5d39fa5d197ec15b7609e20c2370a1c451e78afa63`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6521719ca6eb1fcca63a7d30f12a0885b0e31b2b62cf950b46708240d770ede`  
		Last Modified: Tue, 12 Aug 2025 21:23:04 GMT  
		Size: 59.4 MB (59385254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:75b1d6bf64aef2c3c559967195242de19494bef588c2c5ab7b6576b15343aad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2531428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6ff51919d5cf694143b4dddda53e43717cd89bf6b92467a4e9ba702e8145f5`

```dockerfile
```

-	Layers:
	-	`sha256:9f6265c29fa0433491e053fb76c8c4705925b8e05de06a407d5d7b1b7cf2d765`  
		Last Modified: Wed, 13 Aug 2025 00:07:24 GMT  
		Size: 2.5 MB (2520170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e78bde8561c3db229e1dd3819960a22894ae9ecc48ca9a72339dbaff7de4b6a`  
		Last Modified: Wed, 13 Aug 2025 00:07:25 GMT  
		Size: 11.3 KB (11258 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:54c4703eef1f6fd412b12a40d1d0ea2833bf1dec8196ea781c805ede46d6d583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95765609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6183505cfcd37be310c34f9c2e5476123c04151c5b1b6ff4cf3379364e98783a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c57373924cb0fe482dec77af9738b3c9220a8762562b2fc4973c5b823227896`  
		Last Modified: Tue, 12 Aug 2025 22:40:46 GMT  
		Size: 61.4 MB (61435959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1bd5952f72e61729e50ee60422fa718aae38c3a4d9ad5f56e82503cbd24d3e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae35cd234cc843332c9665adf4be7b8c6477edf009e884da8667c2131ff7420`

```dockerfile
```

-	Layers:
	-	`sha256:ca403ec43c6f8b28c23caa730dcee94450411f7b88b8f6f1dedc31fac9da2fa1`  
		Last Modified: Wed, 13 Aug 2025 00:07:29 GMT  
		Size: 2.5 MB (2517717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35b9746616a2f0ce1e3e3623cf3b7462af870981092c6fb46fdcb7fb8a0588bc`  
		Last Modified: Wed, 13 Aug 2025 00:07:30 GMT  
		Size: 11.2 KB (11156 bytes)  
		MIME: application/vnd.in-toto+json
