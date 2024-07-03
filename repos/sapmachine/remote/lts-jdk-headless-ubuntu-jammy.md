## `sapmachine:lts-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:264af7e70dfd5426f6a71df757001691020e79000e86675ff37f1c06f4c0b628
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:c5ef0df8d8ee798baa913a6812608a5fe73ada3953ba3c812e6c16eb1f5efdbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243394747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bdc32d8747362c1a30a98e1eff71957d0c215b36bcaef7d6eb5d4293cafde35`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55d160000b94e6a2b24bf11a9e5aa25d02d3126a9694b7d34169b3d3fe8a655`  
		Last Modified: Tue, 02 Jul 2024 03:32:12 GMT  
		Size: 213.9 MB (213860692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8c9daae1ad6b2c1bc6b5dd464b5182d5d6b102cdd3ab49431b2ec197b6f51554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2213767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9c6360040f8c68176d22deea3195ace077a5e980b5428c1b49d20cf0fd9f1a`

```dockerfile
```

-	Layers:
	-	`sha256:5b2b42d30e52fecf89d9a417c6ed8df56bdd0b28871a4d1873561372487a0ca7`  
		Last Modified: Tue, 02 Jul 2024 03:32:08 GMT  
		Size: 2.2 MB (2204375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99c0cc09f660cb7faf35499a5b7ab1d5ef20a25284d0288bb1443cf10154681f`  
		Last Modified: Tue, 02 Jul 2024 03:32:07 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:834427b31c285cefe8cfb232c8779eb9ac9fbc477133a1e781a9fd0dad9a5f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.3 MB (239268181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa37410d575ce7da1542bba013a4152051f16724719b2ce6d5beb194b01eb9a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22c20abd463383fcd096f33708e463f18c5ba7bd7dbc1f865eb278878cfa6f5`  
		Last Modified: Wed, 26 Jun 2024 00:08:06 GMT  
		Size: 211.9 MB (211906399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:99509b487e51d8cbf77599f03ad0e4b0eba75ed7a4778b3ce674f0b19ea50fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2213786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e919f01a87fd35e9124458f5d15a4f85d1b864d50c210e0fb14bb9784c25af`

```dockerfile
```

-	Layers:
	-	`sha256:df528925196af3a1a9efb977074aba0d00749cdd64f994046b84d3d0b8900b74`  
		Last Modified: Wed, 26 Jun 2024 00:08:01 GMT  
		Size: 2.2 MB (2204069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24af71df72c9daf786a65038f146226e6bd76ed047f171bfd3df60fb8056d840`  
		Last Modified: Wed, 26 Jun 2024 00:08:01 GMT  
		Size: 9.7 KB (9717 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:108ee996ade8e245223d2482d0267faf13ea49921afd6e87eed344be82e0cd1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.5 MB (249463265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e539344479cc309ec3258f880e3953b118ebf3640c1d04d8d9721adccec06ac1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1962d4435d08ba61c23622c4093f70f3e7e0697381f6c2a0245649aee417122`  
		Last Modified: Tue, 02 Jul 2024 21:27:15 GMT  
		Size: 215.0 MB (215002184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1469a6aea21fd98e81b83d078b1bd835fd5021a9d0da9dcf5f8000a515253096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2215789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b44fca1010676b219ee55608bff7ed6af76592c1d728927dc037841cfa365bc`

```dockerfile
```

-	Layers:
	-	`sha256:b4ce7ba64b477890d51660b85c3523a59dbba1ff3903b9792db222d8e146e609`  
		Last Modified: Tue, 02 Jul 2024 21:27:10 GMT  
		Size: 2.2 MB (2206347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e86c4cc76917cfca419baa9b24528036985fa937ebd8cfd3553018832b2a0039`  
		Last Modified: Tue, 02 Jul 2024 21:27:09 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.in-toto+json
