## `sapmachine:26-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:5fb92525a0f3e0441cacb0fdac53dd851bb0f9f199c461eee9d9bb56c32748aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:26-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:1a30c27bdc5a16e6749f1d0671d0ce23e9c6288f419e090bcad8924abcf4d431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.5 MB (254492128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca691f72e24ecd96c97e684d58b907ea926d948f6f4956fa7099d5f066c1b08`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:15:50 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 01 Apr 2026 20:15:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9981af0573e3de28b0d5a8c9055f0953c882682fb33ac4d2f7b8c28e920204f0`  
		Last Modified: Wed, 01 Apr 2026 20:16:14 GMT  
		Size: 224.8 MB (224755715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:950bc71926e5d7f6497983bb447407e2937d6c702b9abce4cf2b6b0e3bccb176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d57f12ceb08f082b5aa0b566b7c74c0b6fc2ea7c47298426466de24168fa93`

```dockerfile
```

-	Layers:
	-	`sha256:111a9c8c6150a985053e114f3def0685c9653db2a717c8853966305e927ea513`  
		Last Modified: Wed, 01 Apr 2026 20:16:07 GMT  
		Size: 2.4 MB (2367547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e620c42176a78c2a96698c901031712026bc2354b093f9b7ce4b3c717b31bb0`  
		Last Modified: Wed, 01 Apr 2026 20:16:06 GMT  
		Size: 8.8 KB (8845 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:143993b991640d1ee6d45d1d9f94865f02498aa321c32d3959ccf850af10b19f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250175016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9edc7b8bcc8e42117d27f9559e4434a85fb5e6c163eded8ce32759105acd104`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:15:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 01 Apr 2026 20:15:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5ea1cfdc5d9d82eaf3be5fade3617d42ac96645fd92da86312a00b99813013`  
		Last Modified: Wed, 01 Apr 2026 20:15:43 GMT  
		Size: 222.6 MB (222568073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0f3557a79a8709c6b5b95e44f1d8411f911254ba7d987a92d3e502457ae30629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa851b25b2cfc8c999db61d3eb21a1383dd13e096b4d12d50db08282fa55c63b`

```dockerfile
```

-	Layers:
	-	`sha256:4aada7a6b23f0a2a3bf0aed119c30f403fce98e36f2717a47b30fb8d00cfbcdd`  
		Last Modified: Wed, 01 Apr 2026 20:15:39 GMT  
		Size: 2.4 MB (2367216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0e0ca463029d8c968e67d95bfd4cb34676923c4ebdd5a1a1771b2247dcfb476`  
		Last Modified: Wed, 01 Apr 2026 20:15:39 GMT  
		Size: 8.9 KB (8949 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ee0afe5d13ef394f2eb27f7b8dc89d31fcd6dd4191799ade6bd5abaccb8db3cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.4 MB (260391635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc708d6e60f85a7aa4f4ba23170beb1cb37e7cb0a7e4d8f828e98a98bf1b93e1`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:42:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:42:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 01 Apr 2026 20:42:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b509d4a58d6032388564040092f85acd53641ea1f24d7382aa0e248402fe9a7`  
		Last Modified: Wed, 01 Apr 2026 20:43:00 GMT  
		Size: 225.7 MB (225741975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b12d7e460759a942da06d666edea4e1625c7a33f59c5367f6d604263bd2a8a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da6a3c10eb46c156f0335a27504f75a9b8e086610cbcb6894ea1875421beff7`

```dockerfile
```

-	Layers:
	-	`sha256:a2f6e24347da11968bd9e47617089639c89239e9b2066a3fa30fe84c38c7ad4b`  
		Last Modified: Wed, 01 Apr 2026 20:42:53 GMT  
		Size: 2.4 MB (2364425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78d3bb6522ef194573a758d8e436436ce2658c1d6e51d6bf5d18f5228ce29fc4`  
		Last Modified: Wed, 01 Apr 2026 20:42:53 GMT  
		Size: 8.9 KB (8888 bytes)  
		MIME: application/vnd.in-toto+json
