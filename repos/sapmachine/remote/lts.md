## `sapmachine:lts`

```console
$ docker pull sapmachine@sha256:763dde459bce1b048555db5eea7291e8ff9956d038e30bb4085badbf6c36cb0c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts` - linux; amd64

```console
$ docker pull sapmachine@sha256:a8819386da3b68a5cfaea9acc9848404f2cc698591b208ed5871ccc73f9e2a3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.8 MB (244837981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0fa529967154a268eca25ebc71569784cc45b987da4c7620cf57e2db1e16d5`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6cf2a0bedaf71eb120ccd1f27cad034b3600e2128d82634ce5acea71ac2ac7`  
		Last Modified: Mon, 05 May 2025 16:36:56 GMT  
		Size: 215.1 MB (215120452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7f71ad3c1c70d26d5c0dc4911ac40ff83d192c6f17df9755bf5325f819fc7d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2487530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcccb56f1f001b1533b285795cc9810f54921c3e8303377882563def584b8b5b`

```dockerfile
```

-	Layers:
	-	`sha256:cba25efb2794c9b78a4fe7cf98be175ebd29c7455734ceb3a18c270a0501003b`  
		Last Modified: Mon, 05 May 2025 16:36:53 GMT  
		Size: 2.5 MB (2474211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f74eef0a76beac2ce376cedd94ea45e542446c2706cc33f59dc0fe199c1885e`  
		Last Modified: Mon, 05 May 2025 16:36:53 GMT  
		Size: 13.3 KB (13319 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c3c41b1a9abd3c6ca830d06c01a1fffa02bcb4586dbce4155be540d301ca4690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242233534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2467947a9692a98f80948bb1593628d60d34d24ce8d4168f58ebb19e36e05e23`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c2e358d2b41df079fc922c2377505411d22bb1106722324a21da4bf4a25aa`  
		Last Modified: Mon, 05 May 2025 18:31:07 GMT  
		Size: 213.4 MB (213386658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts` - unknown; unknown

```console
$ docker pull sapmachine@sha256:00d831fa74a28f2265f6d40320f859ecd1b28936d7c9dbd7c64c928e590927d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2488438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3764fd889d3a14bfb2d91f2b65622c9aa029981c26cbf6d8907e25aed0badb0`

```dockerfile
```

-	Layers:
	-	`sha256:a583dfbbcaa800c75a1cbbc49c239df74a11060c605a62d2a21f4999b0989530`  
		Last Modified: Mon, 05 May 2025 18:31:00 GMT  
		Size: 2.5 MB (2474847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5c3a1e61f64b96ee28fb42420e4588d3b2a0639494c68f02ecb48829e057942`  
		Last Modified: Mon, 05 May 2025 18:30:59 GMT  
		Size: 13.6 KB (13591 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:42123a596f6136230ffdf48dee04f0924d645eb8baaddc52dbab8ffb4b642976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250871537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88994d655d82321adf17100906f48cc2ae8519dcea5e4ed09b7ba19cd57e81ae`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Mon, 28 Apr 2025 10:54:08 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3772178e2ced5c18004c67a9f500c7ad2e8b10841d86432905ba108d473bfa2a`  
		Last Modified: Mon, 05 May 2025 18:22:53 GMT  
		Size: 216.5 MB (216530699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f348f99ec73e30b69c6b15187ad5cfec437fb13d39d5f73f4bb3738c44de27f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2489734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab671f78ea7e657162d4e4e0fa43b21dfd7e45e71797b492a3cbd26637bbe83`

```dockerfile
```

-	Layers:
	-	`sha256:14eb423612f1cba9e2c33d95d8b0c533e8a09451fbc34051d7e31feece7fca7f`  
		Last Modified: Mon, 05 May 2025 18:22:48 GMT  
		Size: 2.5 MB (2476288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73e5b9f09b8d9d38128847e429196e01be74f3672943344d462593669c82c790`  
		Last Modified: Mon, 05 May 2025 18:22:47 GMT  
		Size: 13.4 KB (13446 bytes)  
		MIME: application/vnd.in-toto+json
