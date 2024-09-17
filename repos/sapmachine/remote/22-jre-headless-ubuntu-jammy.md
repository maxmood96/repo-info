## `sapmachine:22-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:36a142e6d8ca1c06657ecbb4d34e22657e3eeba3e8831895283ff558f82d2a29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:3dfb4b15c87dea7d101b886756142855e99d30b00ae9ec00bd1eef1e3fa68e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87450718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7182bcf9c0495bf3fc289bfb0b78d9a6ab363007bcad8018b0cf246815f4f192`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1933ea20e815622b28c36ea300483dcac41fb829e80a37ce420bd514d3c1a3`  
		Last Modified: Tue, 17 Sep 2024 01:00:56 GMT  
		Size: 57.9 MB (57915030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4d338f9d1e221fd9dbd359d22e8190f0192856ea1dcdbb175cbaca23727e59f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af0ac041de5e60d367735d18426d301d783c66983e59a0271e496fde73c68f1`

```dockerfile
```

-	Layers:
	-	`sha256:16df2a5982a7328805721613987f637bb0e4896cd6dcd7faf4829e475b0b30b8`  
		Last Modified: Tue, 17 Sep 2024 01:00:54 GMT  
		Size: 2.1 MB (2148130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d501ae11059b2ca39aa90df6388d74d9e66cd15f06aec71520fab6391b19fc95`  
		Last Modified: Tue, 17 Sep 2024 01:00:54 GMT  
		Size: 9.4 KB (9356 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2427188bfe316b64d5ea13ad501e43aca063fa4bc30811719b6a9f1426555dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84271941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0594a949a0c5fc30ced4c29267cecce4d36f8924647c400931bedd46d8507a5d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8066bcdb9d97181a129ee12b600e775b6344278016d192ae0cdf405b24cbf3f8`  
		Last Modified: Sat, 17 Aug 2024 04:10:47 GMT  
		Size: 56.9 MB (56913258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7140d8dd3236c96de3764cafeeb5c47e319295f5c633e9691d30d683eea1cbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2156875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8301e0f76ca4c7d015f5d149ca24b4fc8710e9086f9c1736a7fc72aad7c0ab`

```dockerfile
```

-	Layers:
	-	`sha256:f0c105897098a5b5ce6c7c50dce00332da65587dd54d61633cab747dc1cb5b06`  
		Last Modified: Sat, 17 Aug 2024 04:10:45 GMT  
		Size: 2.1 MB (2147193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:839ec02eef7a08665ce5c1c7f5b642befd4134d7f33eebdb6532eaa0f05159a0`  
		Last Modified: Sat, 17 Aug 2024 04:10:45 GMT  
		Size: 9.7 KB (9682 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5f320d83f10bf868ba26a469999d03bbe824e1b621faa0c221d5bcc0951f048e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93637256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c480c57ab8b56dd752240b3e63087c297ce10171c5626abe0c98c78985699235`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19946e898fd4b25257bc3da3c59d1a687cb013267cb82bf0007cd74b16772bbd`  
		Last Modified: Sat, 17 Aug 2024 02:37:15 GMT  
		Size: 59.2 MB (59173078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5ef299760340a06e9938cfbe2ee5eb8231ed944d0fe14de587ee9ffe0f184150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2160827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc637027274984dcfe1ea27d3ad8b71541725f10d1d2b29ed23524bb07e52ed`

```dockerfile
```

-	Layers:
	-	`sha256:c3e2cdda4b32288e281b3f4a2baf03a40979d0d55c812d80339104aba7436493`  
		Last Modified: Sat, 17 Aug 2024 02:37:13 GMT  
		Size: 2.2 MB (2151420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6a1c473c16c30ee0adbb41c04cbf8eebe05f54db99eb133a9516c7ac43c825d`  
		Last Modified: Sat, 17 Aug 2024 02:37:12 GMT  
		Size: 9.4 KB (9407 bytes)  
		MIME: application/vnd.in-toto+json
