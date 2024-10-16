## `sapmachine:jdk-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:fc7de1c7392b9fff9e7782072876551fa85c86233f9675b8dd295e45de88882b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:8b1e5aa974d3338a54e221fc9afdd8b0d3b2c9a9540e3abb136938ef3ca367ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247654698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6dda2be94971f830c861a81713613f386268841ea069f63422abfb6bb5f531e`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054b9fa1ebdfd924d982c445bf406718f9a2dd093c953a89933dbb534d961583`  
		Last Modified: Wed, 16 Oct 2024 16:18:00 GMT  
		Size: 220.1 MB (220143638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c361c00bcaf14daf7c313df19596ed34831bb455d1a54342239c661f3b087d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224f3ab349b45dbc5a9b1e4622fd8f231c32efa97d75a8f830d54cc8f7ee2306`

```dockerfile
```

-	Layers:
	-	`sha256:5be4e4fe5d63a3e0dc21a3699218cd3dc830d1aa5fb7807dce668af5ea3040c6`  
		Last Modified: Wed, 16 Oct 2024 16:17:58 GMT  
		Size: 2.1 MB (2129812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:029ec56adf82253f39214be9e0e8c6d2090e9cb51fedf88f2599e3c986d869d0`  
		Last Modified: Wed, 16 Oct 2024 16:17:58 GMT  
		Size: 8.7 KB (8670 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2ea39545600c50c25b043c17c6349f5278b74de9e563e8dcf51b56bfe068049c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244090969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc30f6cfb3b50378623b568e8c8da0ea787d229fde598755d1f4fdf1d40306c`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:4c1162600f0bbf898f9cf4f8588a8eefc32bd0ddf9e7e28d356a2cf9c43084c9`  
		Last Modified: Wed, 16 Oct 2024 04:24:32 GMT  
		Size: 218.1 MB (218117141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b17cd6de8b6de21727980e11e1f8981109d6ebb6b518d038d7d24e895cdf7ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6244907a235ef8034d05991fc6ea680c056257500f8c707f948b6441c4c784e0`

```dockerfile
```

-	Layers:
	-	`sha256:bd3b63dc216f2db286e5737b399ef7cc10ea7134571a0aed69ec9c63445c0711`  
		Last Modified: Wed, 16 Oct 2024 04:24:27 GMT  
		Size: 2.1 MB (2128808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb5577b29180c92e75efc85add518bc04085fa0cd676e403b53210dad57d43f5`  
		Last Modified: Wed, 16 Oct 2024 04:24:27 GMT  
		Size: 8.8 KB (8770 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c432fabea1e42c0d703cd86e3df0395c251650cf89a14f99143b52f605698628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252657951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c0ad5f0a68df59837344290850a2a37b3f661a1582226e91e9d5b80cb2e14d`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:5a854de10e3d61f4dfabb93d00f6886bc5ae7676da72b91f6e3e60001eb157ae`  
		Last Modified: Wed, 16 Oct 2024 02:41:12 GMT  
		Size: 220.6 MB (220581445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f6a2867418a5a66e86953a58ac6278af4676d9965997896377b87af92e02cbf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5486526ed42a20edf4bfa6f80cc80ad9a8f4b61041548ff13dbbc3939292087b`

```dockerfile
```

-	Layers:
	-	`sha256:ab1d52f6a9f1d5c5df3a79c3bd3e7bc337a63a8cd626b56b53eb6ffc64d611b8`  
		Last Modified: Wed, 16 Oct 2024 02:41:07 GMT  
		Size: 2.1 MB (2130946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7f25af5b8a327dec7d4501df5440d246a7557d921d8323d11c71751ce8dee77`  
		Last Modified: Wed, 16 Oct 2024 02:41:06 GMT  
		Size: 8.7 KB (8709 bytes)  
		MIME: application/vnd.in-toto+json
