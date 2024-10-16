## `sapmachine:11-jre-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:d3f38d6e00ef0a9e7b06b2eaa34f4327437c53d42fd80cf74e1051bd30130d4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:3429f16e1a47121b92b39ce60a2f8eabdea023735a428e0bfbf09d80b1e49e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75802487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a65568138f53e2b1f5a281ca6ec8070983c1bccdb7d1d265e10e082b042de66`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72e17bc1e58f3e710d5294a4b90f95cfbd7c1803d98e703930440743f396ce4`  
		Last Modified: Wed, 16 Oct 2024 16:18:19 GMT  
		Size: 48.3 MB (48291427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c2c0847997f06bdd4d18d740bcc4309a4558d609ec53ebc11eebf730ba44fdb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2063149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e67997fc264576f9fca60770e42329093414c25e0c6f00a33a035dabd696f3`

```dockerfile
```

-	Layers:
	-	`sha256:b845e2580eddd417fce940abb657d2fa27767abce73b36df192e75831525f302`  
		Last Modified: Wed, 16 Oct 2024 16:18:18 GMT  
		Size: 2.1 MB (2054433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4436719892211dca815f2927f723389344c43b6b2268d51a5e063e888b8e628`  
		Last Modified: Wed, 16 Oct 2024 16:18:18 GMT  
		Size: 8.7 KB (8716 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:33de1a232040241808d0462fe503004318a97ca3fe82dfa6da2e9b20dcab2844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73587649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d504a4783205464d32ba09d76b766dcb005316374f17631a50490384d1f50d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9e7fb825e4148f8937d8c1a2d5c2ff8a966e159d0b53e4a8412b2f2234f2bc`  
		Last Modified: Wed, 16 Oct 2024 04:54:30 GMT  
		Size: 47.6 MB (47613821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:aabf067cecfa23893be921369f18e391015b734431653da72532ca723d3db369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2063502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca10cba7b1aad5dd08310ca94c4184eeb20130f4100cbb713a5b58654866ba6`

```dockerfile
```

-	Layers:
	-	`sha256:70f3f9e31c4203bf9aee3d3c4f5d3b47d26c4c381c583c2f0e3dd964bcfe83b0`  
		Last Modified: Wed, 16 Oct 2024 04:54:29 GMT  
		Size: 2.1 MB (2054688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2656b8ffdd62cd26f27c1ec67248b84eb9f7a4ee701e0d83be974cefd33d0750`  
		Last Modified: Wed, 16 Oct 2024 04:54:28 GMT  
		Size: 8.8 KB (8814 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4958135263cee4e4f7f68cd7859d7cf5741ad8120566b590f69e54d90c57b4b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78459931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ffb9c4c3d803ff9a003113c07549156cce29e30ea4758ff7e5b92fde2f761f0`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203f190b7008508d05c9c1665d362ccb1498d398e670977145fde045afca84d4`  
		Last Modified: Wed, 16 Oct 2024 06:19:51 GMT  
		Size: 46.4 MB (46383425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9b0cc276c1cd383f9ecd786a4b371c4f50232360d0a3794705e480d6b32ee0ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2066895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509f617d39a8e73353f04651b8eb3416085f5523fa93bbeaab4f5b6f2f38dbe0`

```dockerfile
```

-	Layers:
	-	`sha256:5760a6700ba21561a45089c38d125981eb2f1c839723b069072db1633ae5a549`  
		Last Modified: Wed, 16 Oct 2024 06:19:49 GMT  
		Size: 2.1 MB (2058141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c248ca5f2ab7d381f87632ae734f08d2394d1def1ca89b7d9e6ea186a2028015`  
		Last Modified: Wed, 16 Oct 2024 06:19:49 GMT  
		Size: 8.8 KB (8754 bytes)  
		MIME: application/vnd.in-toto+json
