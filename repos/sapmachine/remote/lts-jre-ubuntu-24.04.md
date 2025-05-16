## `sapmachine:lts-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:b5c62c7bbe1af7e7e4a07c85f227311a25683e8795d67331598f83ca16012afd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:aa197dfe69bf623041a1635d74f7996ad1f85d435386fcb2cc9ff23c9038ad89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89833794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61790b17227b8f192bb519212c4deb9d1a71a6072d2ac3a1e06c7e536e385979`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbea40ab7164f73876a94bf36d17cb1b64793ef01367341cd0455a771b92ad67`  
		Last Modified: Thu, 08 May 2025 21:05:48 GMT  
		Size: 60.1 MB (60116265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0746fba91bf63cf7db57f40cd40c0887b6fcaf440001a4f4b17cc3bbd4d68a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bafd6eeee6aedf5dd058fd82b5e8208e24da04aa165097ed472270275e9fd023`

```dockerfile
```

-	Layers:
	-	`sha256:882988d61f427b8f01583f549507d0311ff2d598912a4df7fdfb569f92103e02`  
		Last Modified: Mon, 05 May 2025 16:36:42 GMT  
		Size: 2.4 MB (2387822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f236371f102da36585a72e5973660b6e3baee1692ef4fc3b00be71b482e04f68`  
		Last Modified: Mon, 05 May 2025 16:36:42 GMT  
		Size: 10.4 KB (10449 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e8b2d674683c06a254399bdd882e2b08d0eea83c61c8dfbc2433ba4fb628af61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88158343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91fb49c51458fa6d59fe6370d0a7cada91812e70dfc74361563c69626f62fa44`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af60e061588fc38bae9310f89fd9a4adbccfeb28e76a7def0e70d19dc039e34b`  
		Last Modified: Fri, 16 May 2025 21:14:39 GMT  
		Size: 59.3 MB (59311467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dc59fee4382a9d7271c8cc7bae862aff512162594888141542b39584c12af39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e44686b4d5fdd03d10c5da318b8e800b0d889c24ba5fd7e8c3956f4a990d789`

```dockerfile
```

-	Layers:
	-	`sha256:e0e9f05bbc6097a3e03db4e8a2e1ea1d387bded84b8cfe7eb4af3c9960e90f45`  
		Last Modified: Mon, 05 May 2025 18:32:43 GMT  
		Size: 2.4 MB (2388350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f923e82cf85846f63d8d83be912523a566ee66c29574980007b707d555ef3be`  
		Last Modified: Mon, 05 May 2025 18:32:43 GMT  
		Size: 10.6 KB (10614 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c8b88a2e110b45007ec1ac570b4f8e509435ece44cb1889aa771c7b6e01ac3a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96155691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f37c8ab0bbe3b613675b2cf5123e25a7a593c8677992704329e361a9ce6f5c8`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Thu, 08 May 2025 17:06:29 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392374eb79ad979631ceb1963ccafe661842d11bd5783726d5cbb074fb3d7195`  
		Last Modified: Mon, 05 May 2025 18:25:33 GMT  
		Size: 61.8 MB (61814853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0697136bdbd92ae9e3cbb166a67a8af3091626a16611befcbeb28108aa882da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:082a5f2b6d9c1acd4f30054efd7b149a450401e911efb60425fd68ce39e8b299`

```dockerfile
```

-	Layers:
	-	`sha256:d0975b3d0d9ceb7048e4eeb4d7a7f7c8c4177edf2c200de6a88ca1e346143926`  
		Last Modified: Mon, 05 May 2025 18:25:31 GMT  
		Size: 2.4 MB (2391791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:340b565b7dcf3dc3cee27b03a014b8066dca63410e00a9192491d311856c96f6`  
		Last Modified: Mon, 05 May 2025 18:25:31 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json
