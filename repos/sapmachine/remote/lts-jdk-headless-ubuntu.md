## `sapmachine:lts-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:3999d231e0028c31f5368f30a3a1baddd4bf8a397115ecdcb343f05d6e4db2d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:f063ac5f4c1fa652390e0f2f8e860dc346c4f1fd99cc1464c989240a42c512d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.0 MB (250016735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b780f12f993e6dc68ad4e7236378db0f73fe08a07d696a929e0001e977e02f1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 20:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9b7e8d6587bff1310a486bd03d13a17b3c4d51da7b9733e8d302a30f7bf0bf`  
		Last Modified: Wed, 15 Apr 2026 20:58:33 GMT  
		Size: 220.3 MB (220283757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:41dbb57240a5cf9dd1c4f2b63cb3e0980fd8d17814c8125de765501d6f5a51eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2360528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f46bd9199c23449f86c8d7ed7d439886833ced308c85e7aaf1c7840770cc565`

```dockerfile
```

-	Layers:
	-	`sha256:9597265720800172ab4bb7b9a2251ff32786ae767d7a99059f12c43070dd0a59`  
		Last Modified: Wed, 15 Apr 2026 20:58:28 GMT  
		Size: 2.3 MB (2349263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b820213d1a6914c9d71b5c17618b077d88a89ce23cdd831a10cb45712ae062e0`  
		Last Modified: Wed, 15 Apr 2026 20:58:28 GMT  
		Size: 11.3 KB (11265 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c3e98626efb95b279c9ef412eb3a194c7329f5b3e5b53d0f02c5212040f2cada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246944380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afc5ac83ef78a3aa53a280cb0700ce395e2b27c7e701b5c7cb069c70a088a18`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:07:46 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:07:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 21:07:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a4a2f6f07d29b218c6e6f767a5ce8f7e2d83b40f567d9bf0313f3d242eabca`  
		Last Modified: Wed, 15 Apr 2026 21:08:12 GMT  
		Size: 218.1 MB (218068595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:86f110e627070ac8c4da0e052deeba0d388017cff4520c8ce4e2aa5f5ea2d70e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2361255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edf125275a10bd8803de032457a4e45aac2b0da4a3898f65773e9a0ba747bc8`

```dockerfile
```

-	Layers:
	-	`sha256:657d0c509445813a2135aa7350a3d47c436445b088abd86d582491c5a371bb9c`  
		Last Modified: Wed, 15 Apr 2026 21:08:06 GMT  
		Size: 2.3 MB (2349803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:197e5bc59b12ccfdeafb02adf503ff2f850f3ee5cdaf5a570ce8a51d8c7d66ff`  
		Last Modified: Wed, 15 Apr 2026 21:08:05 GMT  
		Size: 11.5 KB (11452 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7d513b0068351cf5836d062f93c305e5f76a0f5b43737e02ec6ae8c2964895fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255281859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afc95de0575c619e74c630dd19bcd8aab2c4d134936943a64e84f538360b3be`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 23:27:03 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:27:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 23:27:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d62d8d3ff045f87db550093e2c7b1c69af923aff3822724f5f96a9cdb31bec`  
		Last Modified: Wed, 15 Apr 2026 23:27:43 GMT  
		Size: 221.0 MB (220967681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:501f0fdec14e1d2412a26e5be4197558833533fc1cd2d22545832e4f877fb546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2357484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b489aea1f84a1f1b7e5be1077e7ab7fcc4955adf3c5623bc9b4697540c6c8794`

```dockerfile
```

-	Layers:
	-	`sha256:70f257b707cb5ba7d8b48926f7bedaf0e43857371070efcb0a5bf8b66fc94c28`  
		Last Modified: Wed, 15 Apr 2026 23:27:39 GMT  
		Size: 2.3 MB (2346134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca2b629aabd877abf037c7825797a390e316f160c569593d51ea9f624447fd83`  
		Last Modified: Wed, 15 Apr 2026 23:27:38 GMT  
		Size: 11.3 KB (11350 bytes)  
		MIME: application/vnd.in-toto+json
