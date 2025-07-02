## `sapmachine:jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:346345ca5de07eb4152b2b8a7f7a658720b732eb4b6db609302b72273cff8012
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:fc8b174dbd5b8e419bad1ca2e71c7ec9cb0649ea29c07cfd539f62a7a8682575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96003729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:222834945f9414bbaeea6832fd06c3d7def41dd6bcec1ee86c0c3dc8404c0f93`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c393b3b7faf03fbd79b5629b3258806f56dd91ee1aa2ce656d054c5213d4c6d`  
		Last Modified: Wed, 02 Jul 2025 03:12:36 GMT  
		Size: 66.5 MB (66468043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:26cd07a75befa43b0632d2db15bc393b24a1176d958d3ef9f141d615ce6503ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3422932cda90d8f4735da5eb0fbe3b2bec849f39157638db800cdc8e096373e3`

```dockerfile
```

-	Layers:
	-	`sha256:9d49a13573245a7a6b7be608aae83a5c8e62e849a62d9ffcfd2b54a9039cc46f`  
		Last Modified: Wed, 02 Jul 2025 06:09:54 GMT  
		Size: 2.3 MB (2301833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:590ccc96119766d4f2bda924e9c1056fb9db330a6dc2ea08dc41a422886d1073`  
		Last Modified: Wed, 02 Jul 2025 06:09:54 GMT  
		Size: 9.6 KB (9610 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a4122426568f84b9dc8385245d1630b44cf31a49f43b42a66511b28645e6dfee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92811716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84dcbd33911b41b2ad173656754574f50867b325a0b721d010762710f954bde4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71ca7ac7aa5bade2abd11d2a9f11c1110ac6bf14f31b226beab4de8c34e4de0`  
		Last Modified: Thu, 05 Jun 2025 08:30:25 GMT  
		Size: 65.5 MB (65456135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:27e63842d06f62423854fcb014c5f8968d5918b1daa4bb3602ae23df8b027cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2128d71788196f82c0f0f0bab7ae36a1ba119325ca761e41ada15738c175bcad`

```dockerfile
```

-	Layers:
	-	`sha256:b99605ff0436efcdaabf40e4c27d423d35a123794e14f72f58c243c6f4ba6300`  
		Last Modified: Wed, 02 Jul 2025 06:09:58 GMT  
		Size: 2.2 MB (2196739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc7a8dc5930a0ddca9b81133699df55e33da7cf46b4f08bdcfa9bd41ec3ce4d`  
		Last Modified: Wed, 02 Jul 2025 06:09:59 GMT  
		Size: 9.7 KB (9739 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:56675823503e4733982de2cc72e25484d2dabc1bca9ab359ef61f7515a2f6c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101998340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122e42ef79247a4e3918e5900b805a3f42861c4043a83933a4ae40ca29225299`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5be5ae1301ae0011e5afff99ad73ad01b6bd5dfc96f9c2624e2c759e31752d7`  
		Last Modified: Wed, 02 Jul 2025 04:46:04 GMT  
		Size: 67.6 MB (67555719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7d6f25a0fa3767f664d6d91da14c29b43cb5a20e21160c0db8e2474aa79e6fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35de9f867a3df7d7d0179eef66eaf7684df73a5921aa360e1b296f463a5e9cb3`

```dockerfile
```

-	Layers:
	-	`sha256:da5af56a368a80a340a42345b871452d26c7e1cb65f2ff597388b1c0a1dcb476`  
		Last Modified: Wed, 02 Jul 2025 06:10:03 GMT  
		Size: 2.3 MB (2305256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ceb4d03428934831ff61376e90441fc014e0776ae23631ceb677b5a3c4dc0ab`  
		Last Modified: Wed, 02 Jul 2025 06:10:04 GMT  
		Size: 9.7 KB (9667 bytes)  
		MIME: application/vnd.in-toto+json
