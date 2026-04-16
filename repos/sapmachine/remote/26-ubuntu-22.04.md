## `sapmachine:26-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:e34217f7c458fc0d8adc0ac04c5625622b96406a6be782892070c9341edf2907
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:26-ubuntu-22.04` - linux; amd64

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

### `sapmachine:26-ubuntu-22.04` - unknown; unknown

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

### `sapmachine:26-ubuntu-22.04` - linux; arm64 variant v8

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

### `sapmachine:26-ubuntu-22.04` - unknown; unknown

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

### `sapmachine:26-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:00eea3d35056fb2d2f4d4729f2d8507c7ac018a8f5b214da7f99a369e1fa9ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261780059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569189008ed2f6a50097304e286accf01070665e74881a0053e16cc37cfd5e10`
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
# Wed, 01 Apr 2026 20:40:54 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:40:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 01 Apr 2026 20:40:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bd6753a676d1b87e9c2339dac138500afae05ccdccee82acf2846d6d097c8a`  
		Last Modified: Wed, 01 Apr 2026 20:41:40 GMT  
		Size: 227.1 MB (227130399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:482179cf07fa062103ddb5d51b691701452bf48f82818304d77ac670d83059e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92540f6d3ac1f8f1492d65580f9a4e64cf3b0b233e6fb8d5b33de805f0557b0`

```dockerfile
```

-	Layers:
	-	`sha256:687fcf00d15cc19b01b8a069e548c666bf9630c5d5b7620d5b8f322c86df6cf7`  
		Last Modified: Wed, 01 Apr 2026 20:41:33 GMT  
		Size: 2.6 MB (2616585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:426ff8323409f8ca5bea282368a2fca5edd9dcd9af1b48b9cc6578d80f186589`  
		Last Modified: Wed, 01 Apr 2026 20:41:33 GMT  
		Size: 10.1 KB (10086 bytes)  
		MIME: application/vnd.in-toto+json
