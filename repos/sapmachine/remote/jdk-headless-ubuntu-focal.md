## `sapmachine:jdk-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:d2e6db7ab05a958a2e0ddc1628db16e1b42c7e871e4c1b6551349a89222b0917
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:fa92fd4e2af24a0d5e6cef1714e1078fb4408c5a8fed9629754e586af5475e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247654482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d57d917047bc26bc1bf2defe415300182229199b46a255e2894d29b164eb25e`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:5e9aaf467bcfc75a57f93fb0e8dcaa93d38813459587c25616d682be9baa40bb`  
		Last Modified: Wed, 02 Oct 2024 02:00:14 GMT  
		Size: 220.1 MB (220143430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0ce73457554cbfcb1a28081814e5c424dee729eddf03d56393362cba4c472ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3786a21a4ff2eb2491658fb6ba638eec2289d6238438b5e3614503b4ce84e72c`

```dockerfile
```

-	Layers:
	-	`sha256:1dabed6218d855666cdb6b26cf8975cb4204c0f38e8f48bb17c42397962e9e13`  
		Last Modified: Wed, 02 Oct 2024 02:00:10 GMT  
		Size: 2.1 MB (2129812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06965fc8a2926d6e497baf527fa73747c8ba0463f695464aaf9869ddeb1e2c54`  
		Last Modified: Wed, 02 Oct 2024 02:00:10 GMT  
		Size: 8.6 KB (8639 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-focal` - linux; arm64 variant v8

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

### `sapmachine:jdk-headless-ubuntu-focal` - unknown; unknown

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

### `sapmachine:jdk-headless-ubuntu-focal` - linux; ppc64le

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

### `sapmachine:jdk-headless-ubuntu-focal` - unknown; unknown

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
