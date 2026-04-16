## `sapmachine:26-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:65b438feba4df990b2176f482af788d7162de25657f6c2827a936e630043881e
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
$ docker pull sapmachine@sha256:95406e8155b7b0cdd9716b1715000f06e4fb28b9e822dc14737c7acb0ca759d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.5 MB (254492189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3a38ddeb5496c7405a0d71db1a906b3e5095442cb6d371712d7b76010e7baa`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:57:34 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:57:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 20:57:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1584eef762f3af2500f37ea503ca7f142671f1e2e7af227d5f1e231dffbe1f2e`  
		Last Modified: Wed, 15 Apr 2026 20:57:57 GMT  
		Size: 224.8 MB (224755691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:072f3b1922ece8a5fc35ab19f290e9ef6ebe13f1c96c25c4c95910264b57b13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbef691cafd331496cfa6871f73fe9153a9a0e7932f5cb156b3658994037c255`

```dockerfile
```

-	Layers:
	-	`sha256:11ca1554c92e05ff34b7e543b3712e6ccd097e32f06fd84f8ce30251c9a02570`  
		Last Modified: Wed, 15 Apr 2026 20:57:52 GMT  
		Size: 2.4 MB (2367547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4e7f47de42f9656bc26279bc59fdf26acc7abc11fef929dd288203fb08a370b`  
		Last Modified: Wed, 15 Apr 2026 20:57:52 GMT  
		Size: 8.8 KB (8845 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:fef5c13e67d09eee391bddc4b8b5fc1c0375b9f98ad196356627250dfa17b3d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250174688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00f1491118322a5c7e67b9722fffe4d0195add334a78c75c35064dbdcbc5ef2`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:07:03 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:07:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 21:07:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50d7904b0bfcf2b8e040e4c74cae9b96bfe01b0b54da6dc4cbcd74fd375306a`  
		Last Modified: Wed, 15 Apr 2026 21:07:28 GMT  
		Size: 222.6 MB (222568145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c47e5c7a597ff1d12c380c881454229be0f912c982c0328fee5dcaa77931d984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df1427bc1c608bd9a151ae87b6c863a4616070579922ca2f59c5c39d6a48c35`

```dockerfile
```

-	Layers:
	-	`sha256:9fee3cf23169c45a52d8e168ccd9f9158325538e64249dd8d6f146aff49c8f0c`  
		Last Modified: Wed, 15 Apr 2026 21:07:22 GMT  
		Size: 2.4 MB (2367216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5d7bcd2464c75c66e57b6704f2f28fa93869dfb8bc08f3abdb78de1eca9e325`  
		Last Modified: Wed, 15 Apr 2026 21:07:22 GMT  
		Size: 8.9 KB (8948 bytes)  
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
