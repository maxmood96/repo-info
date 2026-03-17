## `sapmachine:25-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:8ce261ef5c652181602bab401b2546a1aca340e027669c55bae1140a7a0a732e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:7d38db5064439a0730fb88011964b3b86348b423c9594e7a707dc76f6a959960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86286897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c4bfa30109e0d2fd69af093987a96ce2f08a86a845f6c737a5a9d31ba80124`
-	Default Command: `["bash"]`

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
# Tue, 17 Mar 2026 02:23:59 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:23:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 02:23:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911c5776f1573801d6e042784a7d0dedcc18d631b3cfffc52353e3b6c6b79257`  
		Last Modified: Tue, 17 Mar 2026 02:24:11 GMT  
		Size: 56.6 MB (56554904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:90e41bbf5b47e8c9ece41054164b9e0f5d9b1d5daecbabb0fd38dd6c8eb2d4a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1ddb9fe86b73c93e278639a886cf3bce6b17ebc403e6536cc374b5928b0796`

```dockerfile
```

-	Layers:
	-	`sha256:b10bcf4a332e37a1a8aa7d4bdd85d266e126235a7a0c253f54c64a66cb7fba96`  
		Last Modified: Tue, 17 Mar 2026 02:24:10 GMT  
		Size: 2.3 MB (2282762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dd527c141f26df598c75ffe6a174e2e156efb4f5ce3c4e25425c78829e4cb95`  
		Last Modified: Tue, 17 Mar 2026 02:24:10 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:643f97737d37190e4f70f413aed6c029194799cc513670c058b713c3fbb9c049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84373630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba88d793e3c4176295bc74bbd545f6c4c704be2d131befa5eae63d39f2190a43`
-	Default Command: `["bash"]`

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
# Tue, 17 Mar 2026 02:29:48 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:29:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 02:29:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2466c14893823cbf4902b37da53440236db3b0d005864e19bdf788ee7208bd39`  
		Last Modified: Tue, 17 Mar 2026 02:30:02 GMT  
		Size: 55.5 MB (55503921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ce6cfbf7605719d19a9db88f8d2539df4bdb4b686b3984d750c7dea62efe609c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b901697dc6e217a492f8c5d15d9e38eb6870d83d900c04baecf662f1d7aeb7d`

```dockerfile
```

-	Layers:
	-	`sha256:4d41eca7411d8ff32987468a5cdf46f7d57cd54c627a3beffeefd43029f24023`  
		Last Modified: Tue, 17 Mar 2026 02:30:00 GMT  
		Size: 2.3 MB (2283350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53c9d2bafc9fc2f2969d6d9335a467449d77c4b7436fd67b6c762c67c270806d`  
		Last Modified: Tue, 17 Mar 2026 02:30:00 GMT  
		Size: 12.8 KB (12838 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c0e2f23cd5dc5ba437a0c8e3d40bb38681f4de992d8202cedf7c5a8863e166e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91665751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8ad1dbbc91eb3561a834ddde4e1d9174316e088ca4bcb395393cd96236aae8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 21:20:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:20:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Feb 2026 21:20:47 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d10c023ff280a854a7eb6ea707adf9c8988df843748bbcb118ab89acaea468`  
		Last Modified: Tue, 17 Feb 2026 21:21:16 GMT  
		Size: 57.4 MB (57358845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3148b10a8229afba00631a72c1ab51efa222bd12d78625bcda3badb5012b8e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b90502f1d12c389fbb7b4b68f867ae958ce5d373fe36763ed3e60fe91d9fbd`

```dockerfile
```

-	Layers:
	-	`sha256:ae3b319e23e168cc739b298bf145da09afd23ffb3bbf232efd527f9fddc78c3f`  
		Last Modified: Tue, 17 Feb 2026 21:21:15 GMT  
		Size: 2.3 MB (2281551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d06713e5fd0f1d107851f3f39d032a95f24c36d2d06531d04825d76716c4c172`  
		Last Modified: Tue, 17 Feb 2026 21:21:14 GMT  
		Size: 12.7 KB (12712 bytes)  
		MIME: application/vnd.in-toto+json
