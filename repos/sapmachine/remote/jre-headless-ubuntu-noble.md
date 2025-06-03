## `sapmachine:jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:3c2f70ff5ce0a1f8fb7df74c5893b894b4ec54aeed7bc003f801345c1f373ae1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:8c905afbd0d0beeaf7fe8e52bac6375971cc5bdc9742be091690f18c1e46966e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 MB (96601147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae643ff0cc3109d37eaf838732ad45aefc1f713fb17040d792e8602ca7ffb09`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Thu, 29 May 2025 06:11:31 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e697426247ba011272d67d96d0947a538ab47c782ef764503fc96fb100a26ab`  
		Last Modified: Tue, 03 Jun 2025 04:17:35 GMT  
		Size: 66.9 MB (66885810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c57b6a0a92e25b0cca9d6070084a265dfddf0d9304584b5cc737426a33073285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d845fd180e2ca455f8286a9d9365f4ff02db9211ba7dd38256ab829682de6957`

```dockerfile
```

-	Layers:
	-	`sha256:ba730196f9f7de1157577f2b3d7e54e7493eb0d2779d6029daa595bef02b2ecb`  
		Last Modified: Tue, 03 Jun 2025 04:17:34 GMT  
		Size: 2.2 MB (2179260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cacad6db05f0bb26346c35e794c8d51bee578a6deff9251b01b0488a13403aa`  
		Last Modified: Tue, 03 Jun 2025 04:17:34 GMT  
		Size: 10.6 KB (10627 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9bd9187909b8720cfc9ca926ecb16e1d6790c13fa1a27ae4670c76e9f77211c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94767411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9ae899fde74d133864cdbe99a4bbbba25ed2602060e623dd5aaebf7a77ef15`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8998dd6de3fb3135977b40ddeee9b974aab3580de3c879047e58e9cc6fef9d`  
		Last Modified: Mon, 05 May 2025 18:25:54 GMT  
		Size: 65.9 MB (65920535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d74f45d146972d4219579db830d6568a338719db67de8322c86857d47e512fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21ef366ebebbc1f8e332e7f458fb41f2598ae9c60086cd9d5441e24f9be5ff7`

```dockerfile
```

-	Layers:
	-	`sha256:62ba5f20902f898a0e36b80977608109456312d54a36e7b2794494dabff0acc8`  
		Last Modified: Mon, 05 May 2025 18:25:52 GMT  
		Size: 2.2 MB (2158532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5bf6835f26f7287725fa2d0b874a7460c1fbcd8e11d33818b43123a64697c88`  
		Last Modified: Mon, 05 May 2025 18:25:52 GMT  
		Size: 10.8 KB (10791 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8b477cb52a3d37d62659864c967fda20a12151a87715015e5b3377351c477b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102404973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc5f92fc9a1281979387d307399e4b839e86d85a4c0e904b68501c1e6e2608b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Mon, 28 Apr 2025 10:54:08 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6cf615ca0b2c8cff98d89432fd742ad3d500bfe65bcad07b824ee6fe75d9ed`  
		Last Modified: Mon, 05 May 2025 18:15:08 GMT  
		Size: 68.1 MB (68064135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:39967f8cca47bff28d4225375dac963125046ef9cf588d045e976fbee1900b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2171993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959beab4c5be1cbf8aff20b8ad742c1881d2e0b8fba1e01d98c3763b5b7b6ad5`

```dockerfile
```

-	Layers:
	-	`sha256:bdc1a251d6db09111b644f70cdbfe4574e57107d013d1b77620e372906ac9cbf`  
		Last Modified: Mon, 05 May 2025 18:15:06 GMT  
		Size: 2.2 MB (2161292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f7caa323b6e25de7c0b175809d8bfaac4148c5365b95a313ee8dcc657d7558c`  
		Last Modified: Mon, 05 May 2025 18:15:06 GMT  
		Size: 10.7 KB (10701 bytes)  
		MIME: application/vnd.in-toto+json
