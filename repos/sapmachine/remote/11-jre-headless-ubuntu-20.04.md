## `sapmachine:11-jre-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:7d59b00aa6bdaa125e189edddfe06a65b7914c64ecbb52756bba4005f061ceec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:8d8346329431168ec9c066b1252f881054d39de57a3cd0c946fbdf959e5e7b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75855360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1daef28f301be586e06c6b45c003feaad218433f25aa61bab737cda4e2f00e78`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28f970a62731e3df6187e7b49abd05eb4ab05b281cf7fbdd98d5f37338fe3a1`  
		Last Modified: Wed, 16 Oct 2024 18:59:53 GMT  
		Size: 48.3 MB (48344300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:91a73d3ecb81d2791d6f6bf1f5723c9a04ca0d8bd66e098eafa3068644b770ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2063783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe897d82e4eb6388aa0294dfa1a053b4e117e78657642ff0c6425fbe94fb177`

```dockerfile
```

-	Layers:
	-	`sha256:ef6a6b9d89cc56fd665ec0766f542f2eb8ab9796041805d9a082972693709136`  
		Last Modified: Wed, 16 Oct 2024 18:59:52 GMT  
		Size: 2.1 MB (2055067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd79e31d5635f44432c167cb798f49171788d38cf90012fa780a77c2df73918b`  
		Last Modified: Wed, 16 Oct 2024 18:59:52 GMT  
		Size: 8.7 KB (8716 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-20.04` - linux; arm64 variant v8

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

### `sapmachine:11-jre-headless-ubuntu-20.04` - unknown; unknown

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

### `sapmachine:11-jre-headless-ubuntu-20.04` - linux; ppc64le

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

### `sapmachine:11-jre-headless-ubuntu-20.04` - unknown; unknown

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
