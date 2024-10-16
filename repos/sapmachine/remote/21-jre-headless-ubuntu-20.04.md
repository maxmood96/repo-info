## `sapmachine:21-jre-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:f9a185c40dc323be4cf8285347d9fbf727b2c5d48c8bdb100567bed00dc20870
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
$ docker pull sapmachine@sha256:da50abe0ede9764139542a97c43e1cfffa91047d97f6150b2d0cefc068e26a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85797756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad1b8bc7f9efd94a6bf60a55c5fce70b664d4e25f9f095923ed4647a11da47e`
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
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
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
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8ea28a66bf45a370149362e79d57d7b67b04f1be24eed3a547d75ec8f2dda0`  
		Last Modified: Wed, 02 Oct 2024 01:59:50 GMT  
		Size: 58.3 MB (58286704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bbbe0e50f0a487023e2c2b693fba44f237637554b8ef57c759714f5910c0b907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aad9ac8922d672faea50ef633705fd83097bfbc6a6a1eb6f390105fce0c77cc`

```dockerfile
```

-	Layers:
	-	`sha256:ba17f6db4a797227cfffcb449e98b0b2373c6c85aa9ad1394ca3adf616debbae`  
		Last Modified: Wed, 02 Oct 2024 01:59:49 GMT  
		Size: 2.0 MB (2044966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c385f2ff7f73728c0d67374d5202dd018508913ac2da6ae2a2d1bc7f42d5db6c`  
		Last Modified: Wed, 02 Oct 2024 01:59:49 GMT  
		Size: 9.4 KB (9378 bytes)  
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
