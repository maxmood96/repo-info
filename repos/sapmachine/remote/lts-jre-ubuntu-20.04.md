## `sapmachine:lts-jre-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:1b4691ba6733cd4223fb89f55daea97bf79b2f81108c4444081a88fa8b19438d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:481e6280ce05a63c9b0c366c626db65e009c1ab80f3f6b9381e928b51a4bcb24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86998429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ad374fc84d5b4b8936f9e807e5afaaa5f2f536a8a7b5b8facee9274ebca07f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe10d8ce2179aa9d477af97bfef33a1eddbccb68a4a321530fced5946aa6635`  
		Last Modified: Fri, 19 Jul 2024 18:00:23 GMT  
		Size: 59.5 MB (59486660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7f279a2efaf04eb1f1e36cfcedc6c97e9ccdbe1ff9e888176d6dcaf1affc7d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2291430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbc26cc7e58cf86687c490990eb0c0fb421e32b0ac7ffab0b880c3026333f52`

```dockerfile
```

-	Layers:
	-	`sha256:4c12b91bdfc12aa6f3115a2484cace9e7537692390dd463ade905a8e7310ddd6`  
		Last Modified: Fri, 19 Jul 2024 18:00:21 GMT  
		Size: 2.3 MB (2282204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b3d29ae586fc5d346776574d2a3e73371b5d7cbcd7b6f68c7d3eb61c412246b`  
		Last Modified: Fri, 19 Jul 2024 18:00:21 GMT  
		Size: 9.2 KB (9226 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:55fbef41020ce5920d7e06d7407dd025e169e7cc8ebe8706260564d120d2a98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84484892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72520b57027d757b48fc6a63ead9aa2e218fee9335e0277f368ee54c4363817a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b98655eac0340c416ee6ec764167d2808208c05bdac6d98870c3f1c86f06e48`  
		Last Modified: Wed, 26 Jun 2024 00:13:03 GMT  
		Size: 58.5 MB (58510675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8752f88513ccf3edbf8c29000d6e5e4a20d076cd3de42fa000e58b94c85c2bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2264845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cb1f7e66da80d40fae048e3c12229fa630c05a516e1e35f0505dba086afd4c`

```dockerfile
```

-	Layers:
	-	`sha256:740dea13dc57c95961906a37f55b530fb19214ba84f0918a5379d9ceda221419`  
		Last Modified: Wed, 26 Jun 2024 00:13:02 GMT  
		Size: 2.3 MB (2255276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba1ae00b64705353d9b4c18d3d7a3596a120829b2ad6b2473d4401a618678d99`  
		Last Modified: Wed, 26 Jun 2024 00:13:01 GMT  
		Size: 9.6 KB (9569 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a765a1048ca84edda7bfb03eccf9350d8a0ae2e54bb4a367e5f8aa351eb5dfde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92678323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a616d408c8b99f778cd694fac7a034ed9631d7839097077532e670e6c939058d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28bb4d54060d36e10afc7c5f639500b93cef65e1a04b3251f122dd820914a46`  
		Last Modified: Wed, 26 Jun 2024 00:44:11 GMT  
		Size: 60.6 MB (60601183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0252ce8f2a8fb3879a0e0d22bc6efbccc516a51922e1d4ec047c2d5c6dee0d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2268687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1041d5b80bbd027b4713ae2bf06577857f2832a8bec1c00d04badfac3fd39cfd`

```dockerfile
```

-	Layers:
	-	`sha256:b9053cc0a064f41265f7b097a544067d5bbd9b9d7529d7b78e09a128d622d4a4`  
		Last Modified: Wed, 26 Jun 2024 00:44:10 GMT  
		Size: 2.3 MB (2259393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3997c7fcd9c5b9e6d805717565f07ea0c6e5dda45365b236ecd15011e75dfe1e`  
		Last Modified: Wed, 26 Jun 2024 00:44:09 GMT  
		Size: 9.3 KB (9294 bytes)  
		MIME: application/vnd.in-toto+json
