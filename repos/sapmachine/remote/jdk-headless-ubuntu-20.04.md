## `sapmachine:jdk-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:5a196b8a12600891a5125f5bc92a483f93cf9d3ee1edd810e2c3def687f06e84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:feb044cd310b7963b1d532dbd6a3ee24350456f92180fed91bcee136d3748f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257909514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83e67a028e2d65a6f0c953f6d75381e811310788ded01baed079c8901c1507a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db14b3780e1c3d7887e9af17fc13b94209ab09228db7233c3a8b64fa4fd9252`  
		Last Modified: Wed, 16 Apr 2025 16:14:09 GMT  
		Size: 230.4 MB (230399120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e25902781b793ee4d1189e3b0e7d258a4ba4fd899a9ea9fedaa6112c275c7ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2147223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a8cc2eaf6db76579caf8ba0c06956855a0867cda7cfb330553bee0af4be12f`

```dockerfile
```

-	Layers:
	-	`sha256:79f7c2ccc2ff4057d23547722a56800677e67936d4019126e6b113e1e61908af`  
		Last Modified: Wed, 16 Apr 2025 16:14:05 GMT  
		Size: 2.1 MB (2137611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:703f5c77adb16ef87e2c5fecc3c02fa0adbba984e9044e84cf9fc4cc75ecd4ff`  
		Last Modified: Wed, 16 Apr 2025 16:14:05 GMT  
		Size: 9.6 KB (9612 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:b6709139e85238452833a3e3df01f2f3fc11838fccd6876de7879dd35307ae3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254279873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1cda7add6722451b572777924b23fe0fdf467b3bee1088b6fba280a52340190`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca221f9e3ea90948be788167c159da334034bc817f610dfac75db2a567a33149`  
		Last Modified: Wed, 16 Apr 2025 16:23:27 GMT  
		Size: 228.3 MB (228302212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:685ca19bd136528906dd7b97889a0737d0db1687db25f0e202770a5b2dd0b198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2147000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d99c26b39f2a42330767b13e002d5fa2d74c4f954ca6731ecc63d745f24da26`

```dockerfile
```

-	Layers:
	-	`sha256:b731b56cb0b3d5f8577608d7b920137540db4b8fb24ea32b1d626a71e8468e58`  
		Last Modified: Wed, 16 Apr 2025 16:23:22 GMT  
		Size: 2.1 MB (2137261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39d53df89559bbd0a338a2a614f3dcc4173639e630e1404cf040541a0d1ded8c`  
		Last Modified: Wed, 16 Apr 2025 16:23:22 GMT  
		Size: 9.7 KB (9739 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4ae128331378d59ee280eac19f32e89dc66a45f1bab80bb6721be00425a8ef85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263142447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36a36c920e2df33fcba217c06f7956ca04037977f6d2310ca200008a25d3986`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:47:01 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:47:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:47:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:47:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:47:04 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Tue, 08 Apr 2025 10:47:05 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Thu, 08 May 2025 21:39:31 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3c30444c6cccc80c16d12bb61f461d24c8ec3757db22fb14b4139016bb65bd`  
		Last Modified: Wed, 16 Apr 2025 16:35:13 GMT  
		Size: 231.1 MB (231065501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d6ec27b6f0e7582d329add4e9b9d35633128cc8d8b48a54a79b98541045dd025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2148431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de8db64f8d08c7972ed8163897cf47771d11f1f48120c8cf923e8c9d3b0a585`

```dockerfile
```

-	Layers:
	-	`sha256:345f06071c634807929801bf3e8a9b379f93230c972c87546942545951cf5d13`  
		Last Modified: Wed, 16 Apr 2025 16:35:07 GMT  
		Size: 2.1 MB (2138763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b8da47412194bf5ce4529c08b00b828e3ee33f00038c19d372b462062f1a735`  
		Last Modified: Wed, 16 Apr 2025 16:35:06 GMT  
		Size: 9.7 KB (9668 bytes)  
		MIME: application/vnd.in-toto+json
