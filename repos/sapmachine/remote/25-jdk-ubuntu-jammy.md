## `sapmachine:25-jdk-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:16142b37f59b6cfb9dbbf2b67a27e92acff0dc98161411848411dcc2ec676314
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jdk-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:e8201ad99869ebf480c936a9c81b511bab086f436bccc76e1011c45b613bceb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249581960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a93a753f5781815fbf35a91697bb75dd4394d7749f4f298b47fdd199b1175f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:37:27 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 13 Nov 2025 23:37:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c144a970a672f500175f70ed7879fe258ad46dd60d3b5bbe5e20052c0d409229`  
		Last Modified: Thu, 13 Nov 2025 23:37:49 GMT  
		Size: 220.0 MB (220045162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8db816d15ccf975b6b9627cde4306f993d0a31a5109fc7949f1fdfa005493e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8cd659e34649b468efca6c520091e3256d3ea60d1e1bc7b4ac6978be8c16632`

```dockerfile
```

-	Layers:
	-	`sha256:dd52dba61e916cf2d57424299096100b6073ed703109fb5cefa80371ec04c99b`  
		Last Modified: Fri, 14 Nov 2025 01:13:03 GMT  
		Size: 2.6 MB (2621784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9f2186e9d4fe365dad1a6f274af82d922fa734f42de5cb339d4c37d4d9a480d`  
		Last Modified: Fri, 14 Nov 2025 01:13:04 GMT  
		Size: 12.7 KB (12690 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:07445e432a5996ff7104cfefa86e7347f0609a0c3f86279dab1b2b225fbad156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245124989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452b77dbbcc628238dcf527c4b6622826a068590a4419564abff184c268e22cd`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:59 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 13 Nov 2025 23:36:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e503216fd6d44139ad105d7dfdc85dba611f1778cb3df872fa2fbeda9f3711`  
		Last Modified: Thu, 13 Nov 2025 23:37:23 GMT  
		Size: 217.7 MB (217741112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:efb8ca5c468f6d50790c9b03930bb66171d68cccc8f8bd69d9a4a26571c2766c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af7eb5d01a43337cde7b5eb5019c343ae1836b4c63e2095813b542de5d7d544`

```dockerfile
```

-	Layers:
	-	`sha256:d528ac22a41bf8360835ab4d123bb171c22aecdc5c87121c3b63fa5859a81b4d`  
		Last Modified: Fri, 14 Nov 2025 01:13:08 GMT  
		Size: 2.6 MB (2621607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c419eacfd6275d749a259380832b0dc617b4f79d0541948f18dd2e97f6a9dac`  
		Last Modified: Fri, 14 Nov 2025 01:13:09 GMT  
		Size: 12.9 KB (12938 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:98c9d2c250a9d2e2d2a3920e8db30885d334424371bcd5a4cf5b12a680ce3773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.2 MB (255217730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15877c17fc79ca96bbf04234a3b54adaeb29e14ef1a099fc938ad082bbcef9b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 07:06:37 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:06:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:06:42 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 01 Oct 2025 07:06:43 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Oct 2025 21:30:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d472cd026e9abad5acc12e56e3029168e202c5b0d517d5aed47db14651d9e1`  
		Last Modified: Fri, 24 Oct 2025 23:30:57 GMT  
		Size: 220.8 MB (220770941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2a1619d59c0c3a553e9cc8ffb1292781042ae2d0c077bbe88b07268f77f4c8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2630255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3cb434edaabb873d4d8e3f428b28ffa2e9c8882d936e7b9b472945088d91696`

```dockerfile
```

-	Layers:
	-	`sha256:e420dd903803cc962fa1bca51f4e0f6a69a3ac119dfb840d733a7c404be40603`  
		Last Modified: Wed, 22 Oct 2025 15:10:27 GMT  
		Size: 2.6 MB (2617407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:407fc25eb6ce751a76bf32bbe1be407ffbc80a593521aea17044cb426252a7c8`  
		Last Modified: Wed, 22 Oct 2025 15:10:28 GMT  
		Size: 12.8 KB (12848 bytes)  
		MIME: application/vnd.in-toto+json
