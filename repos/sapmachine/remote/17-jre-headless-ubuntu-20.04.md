## `sapmachine:17-jre-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:5f0ac1c14cf6ca19a1e637ad6adab199c57f5df013fc797778b5c2cb34d8b289
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:3ce2d3bb4453b6442658d73d45713cb72d298b461be4d30385a0ce67ec0e1d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79557995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c19347cce079764ca8e719ca8b7b104dd67e23b63a35feb2035f8a8766da426`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54cd7e11a6ff835d59c6fddd6c0abde80c4bd63a2313753ffbb3bb6d6e04b78`  
		Last Modified: Wed, 16 Oct 2024 16:18:25 GMT  
		Size: 52.0 MB (52046935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:03b74b92db4f1b3666ff3b6c1fd37ed2f6f6572898c4ad0728e1b28bdb5a8037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2051083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ccf460ecfeceb8a0f31bd53014a2c8fd1a1ec3c94a0b8449feb4c42425b1c7`

```dockerfile
```

-	Layers:
	-	`sha256:25f555eed1eecf7b34c5c3bda5c9089233392af5141ae0ab2e60355891567c21`  
		Last Modified: Wed, 16 Oct 2024 16:18:24 GMT  
		Size: 2.0 MB (2042367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aecd70895e180e5736e6915cceabd48109f8c558efa93f6fa5d24d3df1c3431`  
		Last Modified: Wed, 16 Oct 2024 16:18:24 GMT  
		Size: 8.7 KB (8716 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f3db66e6ec70639abcaf8ea93fe0f59f88a0d79220f74f49e9589824282f168e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77399556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39cd2ce8520cd23e6fdce3a419c02ebabe0eadec8ade2d9c40217e2ce37de37f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec3b04af2d499c4377d0248347ca55594061a85e15998b118adf0bea8c0dbd5`  
		Last Modified: Wed, 16 Oct 2024 04:45:56 GMT  
		Size: 51.4 MB (51425728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bc12e084ea81f9e55c9fdf91f8ec22cdd0d2e36e8174a0494d7fb1df99bb2c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2050808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:016aa0aa7065285bb010a302c97d0e655b38376aea8c466985706079e27a7d4e`

```dockerfile
```

-	Layers:
	-	`sha256:8465fa4a767123a281d963ff46864c8c907da3d9bf26fd256ff20c981af1c737`  
		Last Modified: Wed, 16 Oct 2024 04:45:54 GMT  
		Size: 2.0 MB (2041994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57f990b40804baa909db321c3a204f70ece4825c1f8a2ef3f0ba217ce0488c68`  
		Last Modified: Wed, 16 Oct 2024 04:45:54 GMT  
		Size: 8.8 KB (8814 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:6ade01b262b57e5339dd534b7ee19e48bb87d4ba3cf7651fde8358069a36413e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85074878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4677ff991b628dde0ac41118e098bbe8663b7e057ed2b434a40380f02133f88`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4276a4c407ea5d5d74ea880c2faad2a2276b3366172e5614b19c9fa64bc23e43`  
		Last Modified: Wed, 16 Oct 2024 03:08:00 GMT  
		Size: 53.0 MB (52998372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:75a06e40a01bc9dac2de684e450ddc710bde5eb8fc9cac648c6f688369ea0932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bc13c5115056f704eecd6f97d51f5267ca14123b5d3aa085fa9ae35f1fcc02`

```dockerfile
```

-	Layers:
	-	`sha256:e6e2046e69e2984b0e7a9f900578263e221154579621b4d1fd1c2e97340b7096`  
		Last Modified: Wed, 16 Oct 2024 03:07:59 GMT  
		Size: 2.0 MB (2046069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3039e696f2b46732b887b6a524045a9634bd130f94ca4a1eb654a0207c073519`  
		Last Modified: Wed, 16 Oct 2024 03:07:59 GMT  
		Size: 8.8 KB (8754 bytes)  
		MIME: application/vnd.in-toto+json
