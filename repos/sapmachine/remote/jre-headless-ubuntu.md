## `sapmachine:jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:86fb69dd25852a79304b7e1b18182157c15808654ddfa954818fc4f65137f51d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu` - linux; amd64

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
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d407d1e5282ed436be3ad7451c72a41df95a69c74c1f768f250e607abd9247e0`  
		Last Modified: Thu, 13 Nov 2025 23:37:40 GMT  
		Size: 56.1 MB (56082183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu` - unknown; unknown

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

### `sapmachine:jre-headless-ubuntu` - linux; arm64 variant v8

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
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674449c286d22e4ae22ba99af96817f812688834512e42323e7b53cea29e9b44`  
		Last Modified: Thu, 13 Nov 2025 23:37:15 GMT  
		Size: 55.0 MB (55021866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu` - unknown; unknown

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

### `sapmachine:jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:125afa8ecdd405cc945843ac771fcecb36f5ce8bb20faea07be4fe2f5dad586a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91107285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf09a41fac87048bd3579ebf21302e535ef8434b2d4e990aa6d5a694428557e2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 01:15:33 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:15:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Fri, 14 Nov 2025 01:15:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Tue, 16 Dec 2025 00:07:47 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855980692efb7d97056fd1e714815226d484da48a154a0e57ec146fddc2212a9`  
		Last Modified: Fri, 14 Nov 2025 01:16:19 GMT  
		Size: 56.8 MB (56802861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:379e78cde137095937cf7580fd2b44644dbf60aba2aa577142c8e1243437589d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2290470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9305191554bed4bf87f41c6f34bbea295fffb96ba5491adf7abe643b7948c325`

```dockerfile
```

-	Layers:
	-	`sha256:ab428c25a258dd60f5fbd4a82ec91781daad7c395997ef2fc2e424748f4e8a52`  
		Last Modified: Fri, 14 Nov 2025 04:11:01 GMT  
		Size: 2.3 MB (2277758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ce2868dada48e461c037c192b3a0d91dcdcb377040bfcc1801d6ebad63882e4`  
		Last Modified: Fri, 14 Nov 2025 04:11:01 GMT  
		Size: 12.7 KB (12712 bytes)  
		MIME: application/vnd.in-toto+json
