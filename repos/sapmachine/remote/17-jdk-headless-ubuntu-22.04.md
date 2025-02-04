## `sapmachine:17-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:bdcee0213348ff77450291096589737d2b14b793c3741c2b01a0163d46c7f3c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:14fcb40a76d69665630eff2a52e3d7f4227633400aaa5fffbfc492f7c23953b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228241079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c16602dcd8bbd6ed62ecda8fc8d27f3263c4add5ea58ed87ff69fdf5d230bf`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3934e9e2007b520d098aa7ce11e540dc91a51a21f2b4129a893a1cd2d93292`  
		Last Modified: Tue, 04 Feb 2025 04:49:59 GMT  
		Size: 198.7 MB (198705138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eae99d5e60d4f7317fc873d9c457f94432e7b5403718fc1266a2d08eb443a771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8e7392a7b955ebad3611ba3c8d23ec643d898e50f1aff25970dfef57c969d0`

```dockerfile
```

-	Layers:
	-	`sha256:a596158370204dc0d0f00705edf7271defb8f4dd9745c7313f3c200016827308`  
		Last Modified: Tue, 04 Feb 2025 04:49:56 GMT  
		Size: 2.2 MB (2247796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69b5c569c5bc7605cae8fe534d93483c953a2b49d793f7ad9509977c61e2bbef`  
		Last Modified: Tue, 04 Feb 2025 04:49:56 GMT  
		Size: 8.9 KB (8933 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f90c15d427078b5365a51230dc68ec4446e024e3b9899bbbe12a802ccce140a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224772359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc7a6f12a046bac7112e9a6a73baebe7e2664172d478ba55dd66c3e4c8d03df`
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
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33fe6e149d85da232a486fa75a5303f522329394960d1345eb47ad94091cec1`  
		Last Modified: Tue, 28 Jan 2025 02:53:47 GMT  
		Size: 197.4 MB (197414030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c15d9791276d30f7cb1b0cbb0a8688429afb20c7bfcc9ea13ee070b7e0a6ae96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77476c9d06ef26f17e4b2a55dd47caf89e2d8495cc62b8a1d76cfeff7d34a79`

```dockerfile
```

-	Layers:
	-	`sha256:abc4465c6ba8342a4368d892e265e0b0f358f2df6848dd6a259840bd8760e525`  
		Last Modified: Tue, 28 Jan 2025 02:53:43 GMT  
		Size: 2.2 MB (2247468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78ee79054df89cb620d07e2aef7680fa7dca25e7c5e05a62ee231be849af9c4a`  
		Last Modified: Tue, 28 Jan 2025 02:53:42 GMT  
		Size: 9.0 KB (9037 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a0dde88860e6c4d8a0d91aeffdb2d129690f2072ed0fc2a2f2b6dcd997307f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234057513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff58687a0d54e362d8cdef819b7130bdf292429b537876e05dd0d3b90ce0c68`
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
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26695891378fd56cc7d5a6164bd65a45e4000b490e5447a176f3d0a49646fbb4`  
		Last Modified: Tue, 28 Jan 2025 06:20:03 GMT  
		Size: 199.6 MB (199609271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cda773d31a7efb3c86cd72bc63c94f461b8833ed44564e4786368fb8e0de7718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27318116838e54713645235bf6279e2b93b73d6e8858fcacf3962f6f6ddc34a4`

```dockerfile
```

-	Layers:
	-	`sha256:222741da9a726cc7aebde1469849f0c26b24d81dceb799a87f83367ee8cf7e2d`  
		Last Modified: Tue, 28 Jan 2025 06:19:56 GMT  
		Size: 2.2 MB (2249761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df54246d069e0f3b3c1e1cbb3f443792e19f30323d37322b4653e6c2baf57731`  
		Last Modified: Tue, 28 Jan 2025 06:19:56 GMT  
		Size: 9.0 KB (8977 bytes)  
		MIME: application/vnd.in-toto+json
