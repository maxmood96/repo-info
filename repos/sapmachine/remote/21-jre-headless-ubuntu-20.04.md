## `sapmachine:21-jre-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:9f75bd870e73e6648071ebd43c6ef4ef3f9a2bfbc95c579eef75deac1a7d2b14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:c9d5cf735d354052e89ef85ce419c5792a40a3f5f9790d160081edca9be37639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85797999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fca95fe41719c64fb88884a948c8c88f7679122e79aeb370250eb9072dd0ef`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db1c97f72e9356f97fb1bcee544bfe51732a729ea8d89963c18195bff39dfea`  
		Last Modified: Wed, 16 Oct 2024 16:17:46 GMT  
		Size: 58.3 MB (58286939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:36a934611e253bf452fe4280fe6d5e33b66ad0a48ba30edb8d74c5aec9f2b263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0618976a4d651753474a6d4b2919b4349cdfcdc2c662deb52b3c95897e3dbcb0`

```dockerfile
```

-	Layers:
	-	`sha256:122c195133592d725eeb8e80ec366a2ec9fbe51d106c84150766a1ec1320e67c`  
		Last Modified: Wed, 16 Oct 2024 16:17:46 GMT  
		Size: 2.0 MB (2044966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d7331f3c832d3a4ea10fac7fc8e544daa24c4101ca6df9e5bdb6701ea904d66`  
		Last Modified: Wed, 16 Oct 2024 16:17:45 GMT  
		Size: 9.4 KB (9411 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:1d2d983a3d331e223a975879a83e2f19248f57e293c3782909e5841fb3c27af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83355820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c4a8ab5eceb05f77bfd3d9c68f21a8e0bf59e175b21b3dfca90e0bb3457124d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166cf8508a62834b5f20ff75b3eb09f84ff6b62e8c09f966b33eb8ce6e994cec`  
		Last Modified: Wed, 16 Oct 2024 04:37:17 GMT  
		Size: 57.4 MB (57381992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2edd14f127750ab59a70c2d0476d32d21ab56fb704c23681702cba57a012da4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a18fd43e016f3aef0835f49b78ac1665466715ce6174d49fec7b130b83a426`

```dockerfile
```

-	Layers:
	-	`sha256:61b1bc148c5da416717b2c972177bd85afa78a9dd14c3c7b493706fb0345f3b8`  
		Last Modified: Wed, 16 Oct 2024 04:37:15 GMT  
		Size: 2.0 MB (2044617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e0a57eff748654eddb73ce12227510e9ae95d60cf875d50457dfef2e5be60ce`  
		Last Modified: Wed, 16 Oct 2024 04:37:15 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f48710d991c48f0c46ae76e93f19c0f03d79ee3f08941fd4fdbda8b67b75da65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91385343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085505a0e073b98240d83dbf0416a158730b1f76a44eab73e1a5278af2ed28d5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07cf50af0398c4bc8c32ea79468b87040b74bb58866d38d3957f53c71df8e67`  
		Last Modified: Wed, 16 Oct 2024 02:55:46 GMT  
		Size: 59.3 MB (59308837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:43439e7f1ff15ce1ac8ad0a5e73714c6808cd8120498652f972abc1f2f6a8cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2058141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ff8951fb3e9d538abc1b8b5301d6f854ed98c2e9e2c3dd0e3b2725aa2fca07`

```dockerfile
```

-	Layers:
	-	`sha256:85b62d3b72394a164de75710356d4b2b6d241ccb59db4671740fd167df11d36e`  
		Last Modified: Wed, 16 Oct 2024 02:55:44 GMT  
		Size: 2.0 MB (2048680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95904104c6402f227149d83546479848b266f9f2babc8f6a89dfbfb6c6f3550e`  
		Last Modified: Wed, 16 Oct 2024 02:55:44 GMT  
		Size: 9.5 KB (9461 bytes)  
		MIME: application/vnd.in-toto+json
