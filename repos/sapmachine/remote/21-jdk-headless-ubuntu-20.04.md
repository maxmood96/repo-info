## `sapmachine:21-jdk-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:308aef7c677d61e4a4561bf9f03bbcad44e751d8d58f67bddb23c2354430459e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:6ed81a53f337019597ca2fe4ffe5971ccf2fe4ec5781c4775fc2cf680be5438d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240498768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd625caf21ae88d23f7cb29065e6a2fa76ceee4e418d6a89104da03d4e5b649b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f122d8c78945818b85223225b8fe2a887b2a9d5ee3639f5357ae1c5f3b242a7`  
		Last Modified: Wed, 09 Apr 2025 01:21:56 GMT  
		Size: 213.0 MB (212988374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:38b837ea6f8a24aefd27a799d44f7c08b568a469d95e0e49c0e823d18879ed9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2156529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fa6cd6e407a83bf88e9f37d1f20a91d5a75f085031a3fc2b25cfea2f2e4bd27`

```dockerfile
```

-	Layers:
	-	`sha256:d51a3cfbac123289515383580ade990b5490b1b5fcbc9e812ef37ac832734091`  
		Last Modified: Wed, 09 Apr 2025 01:21:51 GMT  
		Size: 2.1 MB (2146901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1c25e51a288ed37d5335a3a72a04e040eadcef762ce9bb6693f3270838395ba`  
		Last Modified: Wed, 09 Apr 2025 01:21:50 GMT  
		Size: 9.6 KB (9628 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:eaefd1dd56a97095b1dd4e20b6c05a2dc642128dd1de941106363799d032637a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237204126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dddd66b16091d294df1d907a0d7f9b31f2e4c84560970fc866d103641cb0fd0`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a3459d4f8d81a753a35d6602307f5abfb212c2ddb9349f0c98d961413b8894`  
		Last Modified: Wed, 09 Apr 2025 09:37:36 GMT  
		Size: 211.2 MB (211226465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f10ea5b1653680ac596efdc4c5b1ae20f58b3a90775b4f0307286c36e948e858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2156310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527bddc7768e0f1a49eb1da4fd02e945b0ae892a330224f5ae1277b4574a2b12`

```dockerfile
```

-	Layers:
	-	`sha256:6a2fdaeb56d71e84cc502d8402b7001710023e7d88ef29b50a6acf985e8809d2`  
		Last Modified: Wed, 09 Apr 2025 09:37:30 GMT  
		Size: 2.1 MB (2146554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf627abfd17c7cc9892d5a278e8725a5b7726c00d2947e879cd6b05f634051ae`  
		Last Modified: Wed, 09 Apr 2025 09:37:30 GMT  
		Size: 9.8 KB (9756 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:47ee9d5f21d887c498c926d1c86a2935c1af9badf765f7388ddd57ff5377d194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245826361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c3babf0014ecdae765716d5469bcfe0a229f8455e6dd5d564306e242caaac5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Tue, 08 Apr 2025 11:48:44 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4b004de83464c818c08589b69c08ca3a9a568a95430c7a3b23077aac4e0be4`  
		Last Modified: Wed, 09 Apr 2025 07:06:02 GMT  
		Size: 213.7 MB (213749415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:30838e3a3598074c303d274f2679d21ca29b5b138f2d163c8e1a815d58eb64d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2158355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf37616e115fd1eab246c9dec8edaa9eb01e0bff72c03fe75ae9aa7d9968ae7`

```dockerfile
```

-	Layers:
	-	`sha256:403de48065c68d8f311fa7e1814fc36a74d0c9d5ba5094e4a4b0ce41c136f54f`  
		Last Modified: Wed, 09 Apr 2025 07:05:54 GMT  
		Size: 2.1 MB (2148671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6a0ea59911792e4bfeca0e7f2e8850a4fb13262817409e8009b3a901359fa89`  
		Last Modified: Wed, 09 Apr 2025 07:05:53 GMT  
		Size: 9.7 KB (9684 bytes)  
		MIME: application/vnd.in-toto+json
