## `sapmachine:21-jre-headless`

```console
$ docker pull sapmachine@sha256:9bea0d3bc2ba4ff75b538b74c798bdd032c3141537e652de33b3dd93a6295a3f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless` - linux; amd64

```console
$ docker pull sapmachine@sha256:f51626124751602bb4fabf651093576847bdee165a069ed4859b3dda952becd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88739031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dedade8ae85821d60917192958ff48a34915ae51459628090eff505033f95e8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
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
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7a2555ae0178fa2edd9d657cbf584142726b9b909bc73b0b013185744da646`  
		Last Modified: Wed, 17 Sep 2025 17:38:49 GMT  
		Size: 59.0 MB (59015581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e7df37ba152f2e4269f5b687061e42ebbd4709e5a555c581272d8642224e9d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c12d89881fafd3c38066f31f69f62cbab5c6da1359f175acea231f7bafd7940`

```dockerfile
```

-	Layers:
	-	`sha256:dea522d01fdce6fb016c31bc4592bbd4a5313561d9af18efbdccce39ebdeac30`  
		Last Modified: Wed, 17 Sep 2025 21:08:31 GMT  
		Size: 2.3 MB (2272810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:effeb54be25fcbdb1066c0c8be55ac28be95cb5a7e1ca8d0bd842951f577fcbd`  
		Last Modified: Wed, 17 Sep 2025 21:08:32 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:35f488db14034af2a36fccd4fc29c173404afa6974b9fa8626544c194fe2defe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89271383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b94af45bcfba3c9ec089dd7f8cddc74c03cdeca0af0f81b0f6b96678a6fa57`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
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
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e11b84c98248a2f0615ed374a7a058ac9395aeea564190ab4ca9bf2bed618c7`  
		Last Modified: Thu, 02 Oct 2025 01:34:23 GMT  
		Size: 60.4 MB (60409808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e4cbd3cd604ee004f91b9bceafdd23c67c79a113583484c31597621a6e7d4e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c83f1d712a02b307ffa973c92319bf28ed4942adb918330e93111d2ec43a7e`

```dockerfile
```

-	Layers:
	-	`sha256:dca2681f7fb448b655669c5d3841020a54308bcc75b61001aa9f22d056d1e95f`  
		Last Modified: Thu, 02 Oct 2025 03:08:12 GMT  
		Size: 2.3 MB (2273317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e314bd51d08a63f159321659c72739e8459ce072e4c16d533765b69dba3744a7`  
		Last Modified: Thu, 02 Oct 2025 03:08:13 GMT  
		Size: 10.4 KB (10414 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:bd7003b402102bf78eb355074d71f03e191574e41953c9f9773059f79611543e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94359917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad137ade9c0eae5167b7dbe68a662a28dab57a9c38844a4ab1f8cfe9556f430`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
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
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03c6a9a73c12cfc676640bd3d2777e2a855f6d504610b7bf666b92299652244`  
		Last Modified: Mon, 15 Sep 2025 23:45:44 GMT  
		Size: 60.1 MB (60056790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a4b3c80042be4f84405b7857b48d21d8e40eccc1c1fb14e6ca73a9b0df20e908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2281140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e0add1b3840ba63d1584dc2284324cab6568807dc659b7a7eaa310266baae7`

```dockerfile
```

-	Layers:
	-	`sha256:ec04092917b108a7662d9eb907cc45e722389dd1001276578024cb3e5fb97432`  
		Last Modified: Wed, 17 Sep 2025 21:08:40 GMT  
		Size: 2.3 MB (2270810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99350060a7728d43da897ec814aecc8955755c94152061d977ea82950071c5e6`  
		Last Modified: Wed, 17 Sep 2025 21:08:40 GMT  
		Size: 10.3 KB (10330 bytes)  
		MIME: application/vnd.in-toto+json
