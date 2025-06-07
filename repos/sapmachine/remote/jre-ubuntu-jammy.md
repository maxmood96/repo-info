## `sapmachine:jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:05cb492f954f8ddc7c2c6a595abe60f6aa421455b6a7c884c1209d208b3a6a23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:dec5755149fe629a79e27bfb475d801d9643169e429ea089cfc3c3c2b0219e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97213123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5613d33c105176ebd0560ec9f3f3a7e5c8af6d0b423699f7a192998d14e84743`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71a7fbe1c0b9f614af4846f73fd82f151e1eeffe5bfada2b4bc034fd22edee0`  
		Last Modified: Tue, 03 Jun 2025 21:10:01 GMT  
		Size: 67.7 MB (67680120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f4d3e845109bbd329e821b9fef4cb824882eded9bafd8cd61dae24f9ca01b591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2452206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca05543ec3f05e2d7537f74f9f0f03c5c2be5610bc115dda0189df8f7e7004e`

```dockerfile
```

-	Layers:
	-	`sha256:292a4ea47ade91a740de172f055712008a497200086cf4f9da6304d56ecfe068`  
		Last Modified: Tue, 03 Jun 2025 04:17:37 GMT  
		Size: 2.4 MB (2442742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0a027643a16c25fa79ec4691677899e882b67d74222375a5c76b5f31aff50d6`  
		Last Modified: Tue, 03 Jun 2025 04:17:37 GMT  
		Size: 9.5 KB (9464 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e66de456cf99a6fc985071f6d6bbe2fb37d1c4015cf0b5cf0dde30f0fedc600c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94030712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e440ccbf849b374649f9272e961d23405d6bfbfefb8c461abd4eb5e328c2e5`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d3cc58ef489637b488dfbc584acc94cdfa2a6a0d2e1ceca190a0b3fd1d659d`  
		Last Modified: Sat, 07 Jun 2025 16:31:22 GMT  
		Size: 66.7 MB (66675131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bdb6e9f779e7c100def7e9bf2e85844ee744faf0723b8ce515ad116e05f62f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2452037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d05600a62a18d6c9f97776948327eb00937a866c81dbcc42d6c4f658a5b5e6`

```dockerfile
```

-	Layers:
	-	`sha256:a5413416c8cd319260487f36aa3ac27b04f9fc6e18d1234b3d6769e3841e1828`  
		Last Modified: Tue, 03 Jun 2025 05:57:19 GMT  
		Size: 2.4 MB (2442445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fecff613ad1d39509c3b8f15849b22bf29f48ed1b88ef983b14f0dbba5d25d6`  
		Last Modified: Tue, 03 Jun 2025 05:57:18 GMT  
		Size: 9.6 KB (9592 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:381cbbadd76c3ffde42b17d3510d5727be4071775c40e267b9c6222e0967d58a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103390399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1d77092b692de8bb8a6691bb11e3b47d61269210bb07bd659fc2a9a4f3bbaa9`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fdbb794f1a747ec19996ef3126c5c1317ac8f7bcd2514be60d8e9a73522fcf`  
		Last Modified: Tue, 03 Jun 2025 05:54:29 GMT  
		Size: 69.0 MB (68950042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:836ea6efae07a3e7bdb603dd85a028c21d6081d45ecb641756962b5095fd01ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2455775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2449802dfc10dacef83be77f09e619890cda9605fe3dcb32b297fbd5c390c24`

```dockerfile
```

-	Layers:
	-	`sha256:61ef35544df3f1c7f38fe3530810283d1f239e07323a721eb2a2b556b8ef321a`  
		Last Modified: Tue, 03 Jun 2025 05:54:27 GMT  
		Size: 2.4 MB (2446255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee867f367c39ce1dacb5df3ad4c4c89043b675330c105c0fdc3196058b0ce6f6`  
		Last Modified: Tue, 03 Jun 2025 05:54:27 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.in-toto+json
