## `sapmachine:21-jre-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:80a86d180a5992f508242713ab209583f38f7812e33b7133c4ad913f6ebb53a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:82059f9a0964a1cce94cdd4d6b56c61fabe8a7f41a5f3191b268ec5695d5253f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86943251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22670017441261c0b55032f4409416451787b28b38f79bc09be44436f8432c97`
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
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
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
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93535e80f5967ebc1fd9772d2e7f63295e03f67297f0fc0992b86393681f54f5`  
		Last Modified: Tue, 25 Jun 2024 22:58:51 GMT  
		Size: 59.4 MB (59431482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9850695d5301a8d49ffffedc8de2218e9ae5dd4101214417f995a0e59956c837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2264859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52158e9ce7a1298b2e96cd267a0b6bf0e4d3e9e4e168184bf0a3cfdd69aa2abd`

```dockerfile
```

-	Layers:
	-	`sha256:8cdbecd5c0150180670f364aba450120365cae4fb17518429cc1c226c866ffe5`  
		Last Modified: Tue, 25 Jun 2024 22:58:51 GMT  
		Size: 2.3 MB (2255616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bf935c80ad5f7fccb90b932fc42ffee44fea5a2a3bc78e89ae95e3e9a138a0b`  
		Last Modified: Tue, 25 Jun 2024 22:58:50 GMT  
		Size: 9.2 KB (9243 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-focal` - linux; arm64 variant v8

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

### `sapmachine:21-jre-ubuntu-focal` - unknown; unknown

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

### `sapmachine:21-jre-ubuntu-focal` - linux; ppc64le

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

### `sapmachine:21-jre-ubuntu-focal` - unknown; unknown

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
