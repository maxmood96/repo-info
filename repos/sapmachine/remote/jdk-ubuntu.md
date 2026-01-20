## `sapmachine:jdk-ubuntu`

```console
$ docker pull sapmachine@sha256:431ae385735440fb867fba32c1d245b73fc6309649c8c5049b1511eec9e92864
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:7be4ce6e6708f3a90a69b614c6402be9ab894d6d5a34c325c26a9c0fe5845976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250157771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0b48690cb014d1342ab265a1be6cd3bfa46dce5864c7cbd506d12deeea6d0e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:41:12 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 15 Jan 2026 22:41:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303b99354d8af11e83eb528e90503d5bd33591402ee730adb92cda7c6ebd1899`  
		Last Modified: Thu, 15 Jan 2026 22:41:51 GMT  
		Size: 220.4 MB (220431760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:53983334614b1546b227992a342e18d0f4f7fd9c05b934f3c380a5dd5ae12bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2616293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d00a7006c2134ee4ddd7609268678833c7adcda6879ca36fbf0f64664948b9f`

```dockerfile
```

-	Layers:
	-	`sha256:ab6412ffdb42b95aaa7662e40c0334e050069f318cf244894621726b1ed50302`  
		Last Modified: Fri, 16 Jan 2026 01:14:17 GMT  
		Size: 2.6 MB (2598937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f84de3801a166abc59061d1f3c4796952678d7e9322e52deedd04edc6f872bf6`  
		Last Modified: Thu, 15 Jan 2026 22:41:30 GMT  
		Size: 17.4 KB (17356 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:492b611eaa51004ab4acc32c8ebfdf516a3be589c9a6fc81981998b9508cf610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247051052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ff2b487adc8aec7afe1a73bf9daff1beda3caf40a1130b5418aa21e7642f97`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:44:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 15 Jan 2026 22:44:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc460e5d6f0b3a9d87cdede28cdcaaaaec1f543a2cde2fdc20fd49d72e77686a`  
		Last Modified: Thu, 15 Jan 2026 22:46:29 GMT  
		Size: 218.2 MB (218187228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6aac2bfafd9473a8fe4f398087c9a3dd1bb7ac2ce4b9d1060db54299058ec480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9187ae08a7d86ebf691bd5824904a51f11f22a7994ebc15dbad09acf99d6592`

```dockerfile
```

-	Layers:
	-	`sha256:7229c528908b0eb03e68f483131d0bd25051001a6d2691df222dadbb055b0305`  
		Last Modified: Fri, 16 Jan 2026 01:14:22 GMT  
		Size: 2.6 MB (2599726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35961cc41afc11db574685678d0c4c9a28815359f425d71b226c764a42711ada`  
		Last Modified: Fri, 16 Jan 2026 01:14:23 GMT  
		Size: 17.8 KB (17784 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7298c99815fcb51ab6eebf5fc8dd2f4d823c1a7ad91e568a4ccf048a4a592166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.6 MB (255564307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84bcbb4c4cb1513037a9e61d1da7e5686c7080b926a70c9ca95ffdc626acb96`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:24:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:24:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 15 Jan 2026 23:24:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 07:12:18 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a538241808dd2bb4b1e6d3e273073eb16068ab678d2c5371a46e9eac1bc4262`  
		Last Modified: Thu, 15 Jan 2026 23:25:00 GMT  
		Size: 221.3 MB (221258148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:144b7613a8f946011bc6d4847a95a98f845c28cfe6dfdf63808350c9f5bb2d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2612153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d607aa5fc2a2b14ab0e17590c229498f9d3ba6772d870e1d31534397fde47646`

```dockerfile
```

-	Layers:
	-	`sha256:43b9c3eef67376eaaeba282cf6a8de5622f582aa79b1d3e536c2ac2e99682092`  
		Last Modified: Fri, 16 Jan 2026 01:14:28 GMT  
		Size: 2.6 MB (2594592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42761e104cda5746eb5507c38d0f2f5c15b45cd9bbcdbe4c787dd4f6eaed7867`  
		Last Modified: Fri, 16 Jan 2026 01:14:28 GMT  
		Size: 17.6 KB (17561 bytes)  
		MIME: application/vnd.in-toto+json
