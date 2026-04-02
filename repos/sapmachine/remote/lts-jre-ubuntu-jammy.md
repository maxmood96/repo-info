## `sapmachine:lts-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:79d9f77c0fb7e89cfec457589273c87196a3ff4777ad4cc7e82c8b0d56375e1a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:ab9f74edcd99bb0354ebcf72d04a2436099dc50805f1533f027acc0c4f0eaa61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87083317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3329b6b05c4c1078bad178c637ad659d6e26ca1ce4a0b3489a0678584f9ecf`
-	Default Command: `["bash"]`

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
# Wed, 01 Apr 2026 20:16:25 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 01 Apr 2026 20:16:25 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4f3e384784b9dce86a7e9f32c0a9f3546ecc4d4269ced403eddc54d11727e8`  
		Last Modified: Wed, 01 Apr 2026 20:16:37 GMT  
		Size: 57.3 MB (57346904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:14657a118ac7e91e9b67e2f7fd55cba8cfa2f2100194664123cd24a9fc6db289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2562518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4de94f67ff7be78c0bd836f0f37dcd98ffe300cb2108f2523c056edfa25f23`

```dockerfile
```

-	Layers:
	-	`sha256:f00c7e2a6c635602ae36b41f8ad542261b9855ec1a67a4d4160d4e70873ddf0a`  
		Last Modified: Wed, 01 Apr 2026 20:16:36 GMT  
		Size: 2.6 MB (2553081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecdcf6d7200a422390f9950198f7e1d4f9f7426f37bf7368e771967b935a14f7`  
		Last Modified: Wed, 01 Apr 2026 20:16:35 GMT  
		Size: 9.4 KB (9437 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:81ec1268b492084b502b424082a257dc41a70db3cd294ff721a4e09f8f6dfd1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83868228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2545dab8f4a57b7ac3f7afb9a7aefdfadbe098f118a035530e5ec89a312fdc9a`
-	Default Command: `["bash"]`

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
# Wed, 01 Apr 2026 20:16:07 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 01 Apr 2026 20:16:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44750e1326910d74755a52fed498c95e56d85ce057afe4e46386cbd4ba2b443e`  
		Last Modified: Wed, 01 Apr 2026 20:16:21 GMT  
		Size: 56.3 MB (56261285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:db82e49285a752a7d5e0579e7af0bda248181a41eddf1557136a7a281493f0ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2562347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69074c506969df928067d56f22f9269c4654ce71c715f5036f6a8e9cb303d3a0`

```dockerfile
```

-	Layers:
	-	`sha256:4683fe525389379296f01e7c30e5aee15bcd22b16678d46cd5c8ab72f2ab8b09`  
		Last Modified: Wed, 01 Apr 2026 20:16:19 GMT  
		Size: 2.6 MB (2552784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db308365bb0e6dbb7420a12d7f8d5689a7b9fe2470279120e86c8bd0af313196`  
		Last Modified: Wed, 01 Apr 2026 20:16:19 GMT  
		Size: 9.6 KB (9563 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c41bc5d78f3c03b71ce817a50b05ba0e3ad8227d01172c16f8f2b7923b6f52d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92873788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0305b391f38c642bdaf9d5d23859800bbb1345c079b9802a4608342dbb1db274`
-	Default Command: `["bash"]`

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
# Wed, 01 Apr 2026 20:45:46 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:45:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 01 Apr 2026 20:45:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8f87dc4b0d2e9002cbd31c12f64b21963f42f01858922b649e8d10cac80f20`  
		Last Modified: Wed, 01 Apr 2026 20:46:15 GMT  
		Size: 58.2 MB (58224128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bfd0ea592104f09b1012116ca7ee9940e13eb9fe390bf03d562aea48dbe4d4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2561488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64633fe8669be48aa5fc89f0e3aa5b8f9028e563b6b297e334c56d6699fc143`

```dockerfile
```

-	Layers:
	-	`sha256:fb3df36bab19eb1bccd62ff6963c7e2c3e77c78eafafcfb066326fda6e1fa91e`  
		Last Modified: Wed, 01 Apr 2026 20:46:14 GMT  
		Size: 2.6 MB (2551995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa4065864972c05a2429e2922f86d110637f26b583855ed9031c0ad1b65a260f`  
		Last Modified: Wed, 01 Apr 2026 20:46:13 GMT  
		Size: 9.5 KB (9493 bytes)  
		MIME: application/vnd.in-toto+json
