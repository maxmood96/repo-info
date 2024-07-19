## `sapmachine:17-jre-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:08d6296872ed90b8aab7c73dcca26f1b69a785c6c35e4d68393235fcd0105ef2
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
$ docker pull sapmachine@sha256:25dad96b28822fd69f861ac2c3a4618bc49cd98eac502121bbba3dfb8553cce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79558280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213c047926cf6ec11497eef3b7ea17a22a760983f7a182314edee2ea4b669212`
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
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49eea862c58a1faf925d8296a26f5f75bbb95175a3c1e9598b7a4c02f749c55`  
		Last Modified: Fri, 19 Jul 2024 18:00:13 GMT  
		Size: 52.0 MB (52046511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:37c0e948ec16d8180f22f156ce4adbbf5ea56d6a951624aa063c1a5cf8c1743d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2051032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81271dbbda13f8b955d14ab70c025346f847da17ec674608051326f3bfa1e206`

```dockerfile
```

-	Layers:
	-	`sha256:181d0b897c45141dd48ffe704a93b2aa597981002bd3e946af6755292e3041c9`  
		Last Modified: Fri, 19 Jul 2024 18:00:12 GMT  
		Size: 2.0 MB (2042354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70722d47237c4bad0dfc83d002f2b60f10b93f8e2dbed06ae137f7457bd05d7`  
		Last Modified: Fri, 19 Jul 2024 18:00:12 GMT  
		Size: 8.7 KB (8678 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:18dd8d49d9f68f981e69519754beb67649eb4a6675c6135b102f1bbd0eb128fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77348591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990a96902e21e4723d8217cc1122619106a6030ef6b82388ce20f233d7442194`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84886f11a113a5db449bf579908bff51a478ab5737d3e06d7c88915b33cb7c28`  
		Last Modified: Wed, 26 Jun 2024 00:26:37 GMT  
		Size: 51.4 MB (51374374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d6f215a0052c5059979cac69f669bbc55ca8e3796b21a6c83d53249f60fc5c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2555165232599e249de6db5909d5aeba73e67e7afcc259f1cbbdfb1653fd81`

```dockerfile
```

-	Layers:
	-	`sha256:9ce2832c7cd4942de457b19964fb85907b6964f9d47cd2ad9440f83d0735b453`  
		Last Modified: Wed, 26 Jun 2024 00:26:35 GMT  
		Size: 2.0 MB (2018398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa748df635168848f0a35f35b1b9a15fcc912c1ef46d6dbc8042c618bd18a4c8`  
		Last Modified: Wed, 26 Jun 2024 00:26:35 GMT  
		Size: 9.0 KB (8997 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c05b34ab7d9aba0e803eb0d9fe27c712e742e80ae5a64f3c76160ec992a06f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85013854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458cd94be6b0b7a432b7542dec754ec344636e237c2697e683ab3c91e47f1125`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc003019cbab4c117012b964b953562ddc69fce0ff4f7a5eaf412c6678d6199a`  
		Last Modified: Wed, 26 Jun 2024 01:06:19 GMT  
		Size: 52.9 MB (52936714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:76401f0e129cc93753dc1e1153d2f51d7a9c8769eade2a49423b0e573b9a595e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69650d3563710770d8877f1506da4d4a21efacc83d94fea8932e9c6fd03af782`

```dockerfile
```

-	Layers:
	-	`sha256:47a38c0d30fa6097301da799a7ee0ff31a8b73f6a8ae76acfea0f26bb993a424`  
		Last Modified: Wed, 26 Jun 2024 01:06:15 GMT  
		Size: 2.0 MB (2022473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bbf1657862da7d7d3c5e362a659eeb7e705574da7f210445360dbe47c35b8cf`  
		Last Modified: Wed, 26 Jun 2024 01:06:14 GMT  
		Size: 8.7 KB (8733 bytes)  
		MIME: application/vnd.in-toto+json
