## `sapmachine:21-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:986aeb09e0d99eef4d7bd50386c73ace3ffffcf318b40d2ade0b7790924dd467
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:dec5804efbae1b0c11baf5a4eced9357bf3a16e52e88cb96c959aefcfcaa2d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243900318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80ea4b916ba868e07e1ef105747353624c45922fc4f8bf6ec88fc2e1d754785`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:38:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:38:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 13 Nov 2025 23:38:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e408dc3501f6786fc4c2366373e8d12877abd7b19e922636957d8c40d74c68f8`  
		Last Modified: Thu, 13 Nov 2025 23:38:45 GMT  
		Size: 214.2 MB (214175630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d8ba2f25d379be393b8bf0c6f24f9e67c7e7c7c5f52f3df77771a40a3c954e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b79a6998fb6747c7e3ad67086ea0f68a4abe9b9241d89a8f4023ba88186cbf5`

```dockerfile
```

-	Layers:
	-	`sha256:cfc2563e58ae8e248df041dee0965c7e7ecc7620a737566f890ec5789838ff80`  
		Last Modified: Fri, 14 Nov 2025 01:09:38 GMT  
		Size: 2.4 MB (2356331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad98753c308facbc2398a1cfe67500e85a90fd34a46187ecb8fcb100d289788e`  
		Last Modified: Fri, 14 Nov 2025 01:09:39 GMT  
		Size: 10.2 KB (10221 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ed912ddbc064e90826166b446429b61826daa9f48a26cf30f058e3540beb57f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241277545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb309ad283e8fdca5b607f159f9c7057cc939aa67ec5402fc6820a620be8751a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:37:38 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 13 Nov 2025 23:37:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4b516cc66d6dbae7fbd3c247b33af46be9521800c3987aa4cec77494b7f367`  
		Last Modified: Thu, 13 Nov 2025 23:38:02 GMT  
		Size: 212.4 MB (212415588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:36bac5ed87b86a630c9a8525e81f009c6c45961f54a09f7badbda027e33c4452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2367211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3efd69d7c3cb8a2b30c52693355273e562764b6b2794e8c34b4f77716267d7`

```dockerfile
```

-	Layers:
	-	`sha256:99bcaf5b8b549f4440d1887a5fe272cdc1f15d2eb9e068e86728ce52b007c0e4`  
		Last Modified: Fri, 14 Nov 2025 01:09:43 GMT  
		Size: 2.4 MB (2356838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9a90bd2ef617e6299d6d700636b66c0e649a8397c4dc6ec7d4f384e3d5eb120`  
		Last Modified: Fri, 14 Nov 2025 01:09:43 GMT  
		Size: 10.4 KB (10373 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b3b0500a47a7babe7be32b8a17fec9b6683ccd1b68ba899684f0ba4fee87724d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249224261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e80811210f75370e9a10c5081a276db0a3bb49c7929c384d99278c9c73ef14`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167a6fde701a50fb92bde38568b7fe4227ffe080d87fed9250b65f078550e1de`  
		Last Modified: Mon, 27 Oct 2025 04:51:07 GMT  
		Size: 214.9 MB (214920736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:487d79b191cf03c4cd95b9ae5be186986fa173316c9556148d2d46e4fd0c0fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2362717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae07ba94bcb8f41bd4b7cad8ba4f7d17a3a51da7a67b3fbdef8f1284ccc2a65`

```dockerfile
```

-	Layers:
	-	`sha256:84eef12e521effa74f4a880ee44bb0c948a96cb712d5623c449167a4c6cbbd21`  
		Last Modified: Wed, 22 Oct 2025 15:07:27 GMT  
		Size: 2.4 MB (2352385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0266f172cb1e58b9ee0a7841e481ac9d7d8ec7f2e8cd2f6023d485aab742141`  
		Last Modified: Wed, 22 Oct 2025 15:07:28 GMT  
		Size: 10.3 KB (10332 bytes)  
		MIME: application/vnd.in-toto+json
