## `sapmachine:jre-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:39818833e93e7a471b348fe42944c4731a60e3a949e9df4b504a97fd8a8f046b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:49104d62c7b4cfab85fabfb94a787dbc54de85810a51e3bbecca9baa238059b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85228181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e182436104f7c37ba6cf58a65eec00b407259a7d292c6868d103108e4ebfe1c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de67f5b0c3389b7c868171d7b3cb2889c6fdc96fea79d8ef286de3b34740eda4`  
		Last Modified: Wed, 02 Oct 2024 02:00:00 GMT  
		Size: 57.7 MB (57717129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fd245f2f2b25098152397e2c93319bae0175b5a717fa5355ef08edbe5f5e7a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e8d8767ded616556f8085f943e996d0466e053209e7bf8b6adc68682129d47`

```dockerfile
```

-	Layers:
	-	`sha256:30c7e8ee9cda76f0af79bea663e21e18cdef2a4c8a4547b88d1d0b1eb097fdfc`  
		Last Modified: Wed, 02 Oct 2024 01:59:59 GMT  
		Size: 2.0 MB (2045498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9a05ea157f9112cf8b3035c227190347ff61afe181640b28f5eabf74d94231f`  
		Last Modified: Wed, 02 Oct 2024 01:59:58 GMT  
		Size: 8.6 KB (8638 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:45c553d6158567fffe5bf74eab26b0f82d286b0a26b2b38e49418f4b8d05c2d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82730897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7a274f65060e8b060d1dba6f4ea60015277192b8fbca09710f1caafd8673ca`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b5b2f527964b9b1f4cf8632387984ea7781657bb5d82385453569f8667aa18`  
		Last Modified: Wed, 16 Oct 2024 04:27:34 GMT  
		Size: 56.8 MB (56757069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:78ad385451ef694fa8f090be5932cfc5c1cac9f2868d01447a7748b862d026c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2053262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994df846bed56acfe76229117371006372549fa51676f05a9ed5e8e8cd2bfede`

```dockerfile
```

-	Layers:
	-	`sha256:d938a201f3649c30c44e30b246d7cd876d2a2bb435e4282029643c7e60b6ce0a`  
		Last Modified: Wed, 16 Oct 2024 04:27:32 GMT  
		Size: 2.0 MB (2044494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:818ffe0bcd0cb2dd571f544d71fe7aa8317dacb25f82533e1b62df0443a62875`  
		Last Modified: Wed, 16 Oct 2024 04:27:32 GMT  
		Size: 8.8 KB (8768 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e6c996030f9544b2eceb9858b8826127617a0cf08e812c5aa3d2b5480280c945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90635869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e08df597ef314f0d852e58477763d29198ba23d68ed4c59d74b286d9208e3d8b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de06c6368c9dc446d47b08ec5ddad16ab5fa4d4413804b173674a8068d700d4`  
		Last Modified: Wed, 16 Oct 2024 02:43:40 GMT  
		Size: 58.6 MB (58559363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:47ca3b1697667ed6cade728790b87f55d370b3919cb3a282d8ebe8be7168ca61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2057278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ef4d5bda1e0b593603ab1a021502c7739b416e5fb1f4df3da2f023b9a127e3`

```dockerfile
```

-	Layers:
	-	`sha256:67270db969de8271d80eb04fa9dd7832afa6fe2192be2bf53494f1671c1c2689`  
		Last Modified: Wed, 16 Oct 2024 02:43:39 GMT  
		Size: 2.0 MB (2048569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0dff173adb9b4c186c6d819c071101cf607d32892b4c02838f915182d15b545`  
		Last Modified: Wed, 16 Oct 2024 02:43:38 GMT  
		Size: 8.7 KB (8709 bytes)  
		MIME: application/vnd.in-toto+json
