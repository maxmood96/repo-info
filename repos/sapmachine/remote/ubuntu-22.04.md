## `sapmachine:ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:317f0f1a5b8c0eef40c554ec93a2b46eac1b00bb8b0854fa89035a11b9923d78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:34122e0141034741133cab3809538960314c9379974fddf1421bfe96d2e4e954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255711031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7820e7efdedefaa81069e36e0726de516c4455740ad37a7120f3bedc824895`
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
# Wed, 15 Apr 2026 20:57:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:57:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 20:57:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963788a40472d4b359e938b5d48a3c2e0552583888809b2799957e4498e7dcf9`  
		Last Modified: Wed, 15 Apr 2026 20:57:51 GMT  
		Size: 226.0 MB (225974533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:771163209d3ba44dda3d392665468eb5615acc436597bedfb233c51951cbc91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2629611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56fe0253eaefdf03e1c57a9287572f75239aa5d25883269ee58bd24dc38ff8d9`

```dockerfile
```

-	Layers:
	-	`sha256:e7abb347003c9f34732ebc65f9143c457abe27a2480daba071fc92d6eee1c5a6`  
		Last Modified: Wed, 15 Apr 2026 20:57:47 GMT  
		Size: 2.6 MB (2619593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3cbb63c3c4907a8cd231ba75e20588f7b7896a509f354f04966ceb32670299`  
		Last Modified: Wed, 15 Apr 2026 20:57:47 GMT  
		Size: 10.0 KB (10018 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0847ee63844571815f0317cf066c59671b06f1f9f78053109761b9c377b8448f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251403572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b07d6819f249c0b4422a0786315bf409aeacf1c8ff900bd8483eec43cd6e20`
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
# Wed, 15 Apr 2026 21:06:33 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:06:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 21:06:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5d81262ed87badec796250104499e7c580081ef47874157733e5fdb0b25dec`  
		Last Modified: Wed, 15 Apr 2026 21:06:59 GMT  
		Size: 223.8 MB (223797029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:90f17dce62143268228d9d6da284465f8455fa72c26444277c5299f777033681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2629490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809a81d742929aa992a78aa41e447a964ce50b5e58a34147342a6a6a3e905728`

```dockerfile
```

-	Layers:
	-	`sha256:d5f775f404bb6ff703afc41177281e1156bcb22596733b09633cb805f3132631`  
		Last Modified: Wed, 15 Apr 2026 21:06:53 GMT  
		Size: 2.6 MB (2619320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f399a6b8d459c87dcc5a37dc5d13db8dc8da0188762901080478ac2994c5d298`  
		Last Modified: Wed, 15 Apr 2026 21:06:53 GMT  
		Size: 10.2 KB (10170 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:67898e2496437480b1a977ca5f21dfe7c5b5e8d7e706c4cb624800af4c5d1d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261778503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af80956d2c6f961fe8bbd4a702dbf19103df15be74757b44f70099994ebe6d3`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 23:22:55 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:22:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 23:22:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b363f15650e30bb65bcae1712a41375986b5aceede08b5f50fd19b7b8909df`  
		Last Modified: Wed, 15 Apr 2026 23:23:39 GMT  
		Size: 227.1 MB (227130105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5bb86cb7b7e9c1cd97b34c854afd15a3c21ef964a09168e3c90b9d458acb7e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f778731999e82a833e70a439108dc968241769d62d5d6d832adb013068ca151b`

```dockerfile
```

-	Layers:
	-	`sha256:fb6ba47a5219dd88c5a116f27a2ee1a0c0a1729e097b39740b02b18a64b91128`  
		Last Modified: Wed, 15 Apr 2026 23:23:34 GMT  
		Size: 2.6 MB (2616585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82c9d6cd11b79e854e6a0c6ef800c574abacb3bd9fd84933c6c9a7e1f2048cee`  
		Last Modified: Wed, 15 Apr 2026 23:23:34 GMT  
		Size: 10.1 KB (10086 bytes)  
		MIME: application/vnd.in-toto+json
