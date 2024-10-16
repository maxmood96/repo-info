## `sapmachine:lts-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:540da87510e42e9e71b3bdda4c490237d3879819bee39fc8b5b4c09702bf7900
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
$ docker pull sapmachine@sha256:a913f1cbb6bc2ce2ff08ff0f57c12baa251ee933391e1e143e5a164a061ae50a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90080000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69c5055056edf575b9a5ca7cc1b25cb4f7a8f92360cdbfffbb858eb76a20c8f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45a96f398bbac2593ac9889f4fd40397339e342a116fefbcee7cdf46814a537`  
		Last Modified: Sat, 12 Oct 2024 00:01:18 GMT  
		Size: 60.3 MB (60329543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:531d8d50a81bb8e5cbf3685d4790392c3a14d01494c073822ade376284fcbf15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2d8c6e40e1527e41e87985e1afa45669a1003570f1081c8e0a7917bb4a4c7f`

```dockerfile
```

-	Layers:
	-	`sha256:a61965cb2d6bef533c3700ac862c9c31bc3edd74cd6de58bead7f4e55ed28d4c`  
		Last Modified: Sat, 12 Oct 2024 00:01:17 GMT  
		Size: 2.4 MB (2366294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f78c3b688882946397fbdb74b0f5adbece29f092eccaf10322a7dd45d4e0725e`  
		Last Modified: Sat, 12 Oct 2024 00:01:16 GMT  
		Size: 10.2 KB (10233 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6f03fd6a633dde3821a1fb8ba0d40904c0db189f5c405c8588b4c886ae1f89a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88324449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523d538333c7e5bd280d86eae9d0a317c4132b68e10e4845a358021961800c9c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1892d8ca9bf385bd37d1ae76187b83aa28986549f9bf5949d192d93e3e51b06e`  
		Last Modified: Wed, 16 Oct 2024 04:31:06 GMT  
		Size: 59.4 MB (59438604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:177906e30a2a41d062250b5c3ebf8dcc4ce328707ba838aca45c7bf11092342c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06665d1ecdff5dc0f4ffd51ecf9ced6a355939777bcf1779c2f0468533ba9d71`

```dockerfile
```

-	Layers:
	-	`sha256:3c7a23ccf4424539dde23f547d76c218bd779e6f1ac03c18bdc19644b09730ff`  
		Last Modified: Wed, 16 Oct 2024 04:31:04 GMT  
		Size: 2.4 MB (2366821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5020491ddaf9ce2b7d9f84d25dddf25ff12cc3d269adfe2dc1ec90fd8b71ada9`  
		Last Modified: Wed, 16 Oct 2024 04:31:04 GMT  
		Size: 10.4 KB (10392 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:bd5334fd4ea9c911cc36393c1e73ae053763e8786e8f8b0b9162750014022491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96403592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0bf110124e072ea67077cc51568af06a06c5cf3c72b8fa9a38f6fca63557d44`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97916f71f27e537c2ed49135a45fedbb69b953fb55074d9182cd44faacb727b4`  
		Last Modified: Wed, 16 Oct 2024 02:48:09 GMT  
		Size: 62.0 MB (62014623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:68d285c1db2eab4b9cd8f1dcb5611469d797e1d11fff50ce2bce7ac4a517346c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae0d438fdbcac33a14a20039f09730cf26737c6cfaf78add7da28d6e48d4933`

```dockerfile
```

-	Layers:
	-	`sha256:703c34df91fa275a234c1a0a912c63fcf15371539773b7813179e58251226174`  
		Last Modified: Wed, 16 Oct 2024 02:48:07 GMT  
		Size: 2.4 MB (2370261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfba3addf8b5b05813cdd561533769e4b20f3201180b984ca4b44698d253d490`  
		Last Modified: Wed, 16 Oct 2024 02:48:07 GMT  
		Size: 10.3 KB (10302 bytes)  
		MIME: application/vnd.in-toto+json
