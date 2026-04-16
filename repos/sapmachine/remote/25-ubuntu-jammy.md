## `sapmachine:25-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:3fceda34dbfedb20e09b72759355d52130db7da1a0c2724c643478ef5040c5c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:78a634fe40a4ac72d07f55eb27cb5c83a24a541d8b39644099bed6998185b5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.8 MB (250801759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19956908d819d8a7f5c6d7fd835a53e102fc72fbdc697236a731faf5aa979af`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:58:26 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:58:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 20:58:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb12968ad029c753e37f6aa3bd760333dc4b45de02ca1ed0d12c9c811491487`  
		Last Modified: Wed, 15 Apr 2026 20:58:48 GMT  
		Size: 221.1 MB (221065261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3a06ee71706a0c5e6ab47740d25f13c7ae4a61d1717622a02243b2b1d2f2c73a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b771dc13dc8c345f77474dd2ed14dd8ebc73104388a146482650409dd8d7a90e`

```dockerfile
```

-	Layers:
	-	`sha256:08db4312b11aba8b70157c1e9595359333bc6eda8f4b5ea5a9d3cb908fc50968`  
		Last Modified: Wed, 15 Apr 2026 20:58:43 GMT  
		Size: 2.6 MB (2622884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b778ea83cabd03be3b21736b430385e2d42096f085a94af2c72629ad76181c1`  
		Last Modified: Wed, 15 Apr 2026 20:58:42 GMT  
		Size: 11.4 KB (11402 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8b455bf5e3c30f6efa862ab4838f6de44dc009996076137b4a3b3d82340c38bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246437591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399550449576b6437dd5ed632aaf9b0f0d3fbf302772ec38a9d2512d8bb146e5`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:08:09 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:08:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 21:08:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4ed3e50275571434727ef52d6831a1735a4d35c86dc41f0a5ef58b4406f626`  
		Last Modified: Wed, 15 Apr 2026 21:08:32 GMT  
		Size: 218.8 MB (218831048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:437314fda5dd8c4803acbb96a30833309b387df72d5e0311d9055021a8b2c4a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a9b748e82691446fd31e0831d0bdf4d91b009da8c10c681e27345f840d7f36`

```dockerfile
```

-	Layers:
	-	`sha256:c17d44fe03605e088d2b64e320146524e3ceeab7ca4c1437e03611cfd9c9dc52`  
		Last Modified: Wed, 15 Apr 2026 21:08:28 GMT  
		Size: 2.6 MB (2622659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:313253b6c4afae0ebd77ca373a9ccdb3c354c6988c588f74e7ee92c5ebfea1c2`  
		Last Modified: Wed, 15 Apr 2026 21:08:27 GMT  
		Size: 11.6 KB (11600 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:2f7b160c1207dae993fa6dce3166deaba1cfd28f742fee150e4396aa32b239b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.5 MB (256521761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92dfa016d05981592e601f2395bf5a4c8e0795bbc01572d5565887be267cf0f`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:44:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:44:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 01 Apr 2026 20:44:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b555cb12cbb087e58dab068dedceed0a9f6e84975a9656ed0a02dc01e00e05b6`  
		Last Modified: Wed, 01 Apr 2026 20:44:48 GMT  
		Size: 221.9 MB (221872101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:92ab4b49b31c2471d1697630ac29142b2242ccd8afc1f89e5f3ab648a502f2c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2631393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1397d1ad100b1d59b558f8e130fda4a159cb9fda9af653eb02e260853b406e7a`

```dockerfile
```

-	Layers:
	-	`sha256:c94217af99ab70318de067617928cda83005cef20f707e90b65f36746a0639aa`  
		Last Modified: Wed, 01 Apr 2026 20:44:42 GMT  
		Size: 2.6 MB (2619900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83a538307987c05830825c921cedcfc93a88fcfd7130b5b7a180972a8f955025`  
		Last Modified: Wed, 01 Apr 2026 20:44:42 GMT  
		Size: 11.5 KB (11493 bytes)  
		MIME: application/vnd.in-toto+json
