## `sapmachine:21-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:4274f8d270147b88ed210b2eb409e6e3af59165ecd26b02e90cff4c4b7950ce7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:9960be402274af12def1644275028bf25d94d3c511b97d2302a025df2a10cd99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88133619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9edeebfa4617c60b3613457d72e3d0442b8005691e2e1c3c24658690f625821f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb83b6893393e17e8f599fb2f1fc78cb362679b3ae0d606220a44912e270333`  
		Last Modified: Thu, 02 Oct 2025 15:21:32 GMT  
		Size: 58.6 MB (58596801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:05c682b1343e9c1bd3fbe6a8c0b1ca7c71e9777b8632e0b2a7d499a707df3ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd46dc605c1e633fa85c358f0fef788f341bed6a42487ef99e6ada60307f337`

```dockerfile
```

-	Layers:
	-	`sha256:5f228276799612c4a0b8530aa02b72d02453ecc07785594334cab7359bd84f44`  
		Last Modified: Thu, 02 Oct 2025 09:09:58 GMT  
		Size: 2.3 MB (2294109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c78ab3d2a49a91f0766e73800531ef2bac01f5203bf193b92b14fddc403ed0e8`  
		Last Modified: Thu, 02 Oct 2025 09:09:59 GMT  
		Size: 8.9 KB (8923 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f21aa199a608005341084aa83de8b458159aa8e16dd85dd07c94874afa60eb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85155147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e7b80db205fe2054007c4d34091b425db33151085e16ed87c1cc564f734412`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a5e41077bd523f5172fb6982e0d1f0bf1f22d672c7161e949b3bb50558ca49`  
		Last Modified: Wed, 22 Oct 2025 00:05:57 GMT  
		Size: 57.8 MB (57772040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b8322b7996f3a67b3c053740cdea358d3385d1dddd67b30425047e689e664903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537031dae9343a776994c13af037f27bea75d505e20837b6166a1f0bc328f221`

```dockerfile
```

-	Layers:
	-	`sha256:77de99528f0d893d98db3028c7d858d0cb4dbcf5319345bbfccfb44d287bafe0`  
		Last Modified: Wed, 22 Oct 2025 03:08:03 GMT  
		Size: 2.3 MB (2293781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39747a816f294f4339bc9523735eabf1e6d6cab6856c3e2bcc06d53ac1bdc3c9`  
		Last Modified: Wed, 22 Oct 2025 03:08:04 GMT  
		Size: 9.0 KB (9027 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b3f13cfb74ac5a460e4fc3b0cd03058fcd89b48047f63b4f5645b2739248a1b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (93992177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940eecb8c36bcad33b61328c5e9b80e2cebabaf9310b58d8e2ae596dc9adf0ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91da728f2d0a82b453c9741a3bde8cc4c3add71916c67b2a1d728429a9aef170`  
		Last Modified: Thu, 02 Oct 2025 04:41:09 GMT  
		Size: 59.5 MB (59545388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:854300dd1fbeb4cef9f9dba2e973561e0b19641a337da508da5b49009507d169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952f148239db4104b64e8200afcfee7245abc7e593373a02a9ff80caf1008fc1`

```dockerfile
```

-	Layers:
	-	`sha256:7a83fe2df33f5ba1e2a710354f14d9e199fa49ae044b23163e39a8e442fbf74c`  
		Last Modified: Thu, 02 Oct 2025 06:08:29 GMT  
		Size: 2.3 MB (2292134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a841a4c5531068c47dc8eb98498b7072a7e8d4a500b2f4f0bee8f17ed3b84e0`  
		Last Modified: Thu, 02 Oct 2025 06:08:30 GMT  
		Size: 9.0 KB (8967 bytes)  
		MIME: application/vnd.in-toto+json
