## `sapmachine:25-jre-headless`

```console
$ docker pull sapmachine@sha256:eccd56b830c65be55861558ce79594a0217283e03bb9902920cea2b54e6e8e16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jre-headless` - linux; amd64

```console
$ docker pull sapmachine@sha256:b3a8fb425beccbb0bd075cb293ceff667b9cb739bd8ef55ec9b9737e7c62f334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85806871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52927bcfcf789c2330165542ae2ee43b9ab14eb31628fa2205cbc9dacd12ace`
-	Default Command: `["bash"]`

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
# Thu, 13 Nov 2025 23:37:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 13 Nov 2025 23:37:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d407d1e5282ed436be3ad7451c72a41df95a69c74c1f768f250e607abd9247e0`  
		Last Modified: Thu, 13 Nov 2025 23:37:40 GMT  
		Size: 56.1 MB (56082183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1ecbdd571f3fa48fc6c630c0a7ba6f5e38e53079056ab0c08c62948474f16a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bd821af250aa85ee752da5e9a5759c6279a2a36404744613abead9937de395`

```dockerfile
```

-	Layers:
	-	`sha256:6d6da72981a343eb630a284b2488542549a1adcc2a20f41dd4cdb945a2014225`  
		Last Modified: Fri, 14 Nov 2025 01:13:19 GMT  
		Size: 2.3 MB (2280346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe7be46b9d8ba41a39328fb2e456fd4aee07c6490310e724827dcb8c63f6eba4`  
		Last Modified: Fri, 14 Nov 2025 01:13:20 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-headless` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6f84a3ed069c746e7f8567cac259288abae28a0d69de153edf5c204da9af9489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83883823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6170bc966f823a481095c2e1469534abed0cd911ab3adfe7f303faf620e6b211`
-	Default Command: `["bash"]`

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
# Thu, 13 Nov 2025 23:36:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 13 Nov 2025 23:36:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674449c286d22e4ae22ba99af96817f812688834512e42323e7b53cea29e9b44`  
		Last Modified: Thu, 13 Nov 2025 23:37:15 GMT  
		Size: 55.0 MB (55021866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dd255ccca0cd289f593be2beae89511e732893779c7b987ffdfe9edd3a5dd4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2293772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bc1184a453ff8ba8fd18f2b5a7d3dbca84581268de5ed612e632a700090ba5`

```dockerfile
```

-	Layers:
	-	`sha256:6493624a4d84d4e46c1c5e34d0fec56e166a2723d855f033f5d39d22be1525c7`  
		Last Modified: Fri, 14 Nov 2025 01:13:24 GMT  
		Size: 2.3 MB (2280934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97abad6fe012612cc08f79bcfe0bdeb843990dc3fe1363d9273eab107ef07c48`  
		Last Modified: Fri, 14 Nov 2025 01:13:25 GMT  
		Size: 12.8 KB (12838 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-headless` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a9f24b06ab1f37ae5e3171a941dde002025e3ca88914727595e8f93913eee848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91106218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f06066fb1136db420bd394eeb9104c20fb79912b6161f55e015eea78523c2c7`
-	Default Command: `["bash"]`

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
# Tue, 21 Oct 2025 21:30:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Oct 2025 21:30:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd00b8e021875bb70a152225e573641c8c895a0e589d731a5c7533bcf7fea84`  
		Last Modified: Mon, 27 Oct 2025 03:33:03 GMT  
		Size: 56.8 MB (56802693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5f7c4d1d54757065beef9602de8d69cb7c69b923fb27819172fde935f3d72832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2290513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e911accc27f73261e12e94714517ebd56ca12029500618075d190ba7f7229450`

```dockerfile
```

-	Layers:
	-	`sha256:7fc6c821347e3a7c477350737cab1eb47f4d8fec50775a7b18e56cc9aedce513`  
		Last Modified: Wed, 22 Oct 2025 15:10:45 GMT  
		Size: 2.3 MB (2277758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:387e5d114044ca89d2f4d6327dfdb661dd71a063db198abd565fbf4f66b35a0a`  
		Last Modified: Wed, 22 Oct 2025 15:10:46 GMT  
		Size: 12.8 KB (12755 bytes)  
		MIME: application/vnd.in-toto+json
